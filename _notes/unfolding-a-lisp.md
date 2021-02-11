---
title: Unfolding a LISP
---

Building a LISP interpreter in a way that resembles Alexander’s process of unfolding.

*Inspired and roughly based on <https://github.com/kanaka/mal/blob/master/process/guide.md>.*

## Mapping architecture concepts to software
How do concepts from architecture map to software? Let’s try:

The material we build software with is code of a particular programming language. The technology we use are language-specific features and techniques common in that language. The result is a program running in an execution environment, either compiled for a certain machine instruction set or interpreted in the host process.

* Programming language code = *material*
* Language features = *technology*
* Execution environment = *site*
	* compiled: (virtual) machine instruction set + state
	* interpreted: host process + runtime + state

> Materials and technology change from era to era. It is in the nature of human society that these things evolve and will be different with each period of history. But within the enormous variation of materials and technique which inevitably change from age to age, we may identify certain invariants that must arise repeatedly, from the fundamental process.[^b3.c16.s13]

If code and language features are the material and technology of building software, and if these are expected to change, then we need a more abstract pattern language to describe generic sequences that can be used to describe certain functionality, but in a language-agnostic way.

## A project that unfolds
The *Make-A-Lisp* project describes the implementation of an application — a LISP interpreter — in a sequence of 11 steps. Each step builds on the result of the former step. And each step results in an executable, and testable, application. In that way, the project guide can be considered a *sequence* written in a *pattern language* in the Alexandrian sense. And if you look at the architecture diagrams for each step, you’ll find that the structure unfolds in differentiating steps.

As far as I can tell, the project wasn’t designed with Alexander in mind; it just happens to be an example of an unfolding process.

Let’s look which centers we can find in each step.

### Step 0: Read-Eval-Print loop (REPL)
> This step is basically just creating a skeleton of your interpreter.

The largest structure established in the first step is (a) a common pattern and (b) closely related to the user interface: users are expected to interact through a text-based terminal-like interface. You can enter a command, it will be processed, and the result will be printed on screen. Then it starts over, waiting for the next command. This is a REPL — a read-eval-print loop.

The REPL becomes the first center, with a circular structure — it repeats, potentially endlessly. As part of it, smaller centers are established within it as the steps that are repeated with each iteration:

1. The read step: read a command from the user
2. The evaluation step: evaluate the command and compute the result
3. The print step: print the result

We end up with an executable program which doesn’t do much yet, but it does loop through reading a command and printing it (without any evaluation).

*What’s a bit confusing is that the structure of a program is more of a process than it is a static structure. Although we can clearly see how the process has more static parts — the 3-step loop structure isn’t going to change — and more dynamic parts — the exact user input will be unknown until we run the finished program, so we won’t be able to assume much about it (apart from its structure… oh well, more meta levels of circular references).*

### Step 1: Read and Print
> In this step, your interpreter will "read" the string from the user and parse it into an internal tree data structure (an abstract syntax tree) and then take that data structure and "print" it back to a string.

The second step focuses on the *Read* and the *Print* centers. Although much of the interesting stuff is going to happen with the *Evaluate* center, we can’t quite do anything there until we put some infrastructure in place — we need to be able to work with the input from the user.

First, we need to parse the input from its text representation into a structure we can work with: we break the input down into smaller components and arrange them in a tree structure — in a way this is also a differentiation process strengthening the latent centers in the string and turning them into strong centers. This process is known as parsing; we basically created a *Parser* as a new center within *Read*. The parsed abstract syntax tree (AST) is then passed over to the *Evaluate* center/step.

*Parsing is another one of these well-understood patterns with lots of different flavors of implementation. A parser, therefore, can be seen as a complex center which has itself been unfolded from a generic sequence that describes how to build a parser. In software development we usually default to a pre-made component and many of the implementations that are part of the _Mal_ project do import libraries for this.*

We ignore *Evaluate* for now and just pass the AST through to the *Print* center/step.

Then, in the *Print* center/step, we need to do the opposite of parsing to turn the tree back into a string. This direction is much easier because we go from a more complex hierarchical structure to a much simpler sequential structure. We create a *Printer* as a new center within *Print*.

*Here the project diverges somewhat from a “proper” unfolding process as it suggests implementing a parser for the whole language in this step, including constructs that won’t become essential until much later in the sequence. A properly unfolded process would restrict itself to only what is required in this step, or otherwise the most simple version of differentiation that strengthens latent centers (in this case I’d interpret “latent” as functionality which might not be required right now in this step, but is already clearly visible on the horizon for the step likely to be taken next.).*

This step in the sequence is made of two steps which each take a center and strengthen it by introducing a smaller center within it:

1. *Read*: *Parser*
2. *Print*: *Printer*

*Not sure how useful it is to split these into separate steps in the sequence…? To get to an executable program, both centers need to be in place. They are duals that depend on each other — perhaps one way symmetries manifest in the structure of this application.*

### Step 2: 
> In step 1 your mal interpreter was basically just a way to validate input and eliminate extraneous white space. In this step you will turn your interpreter into a simple number calculator by adding functionality to the evaluator (EVAL).

This step now focuses on the *Evaluate* center/step, and establishes three new centers within it: It introduces an environment (holding four operations) and then differentiates the existing `eval` function into two `eval` and `eval_ast` functions.

*I have yet to fully understand why that second part — splitting `eval` into two separate functions — is necessary. In my implementation I kept them as one and it works fine. Perhaps this is another premature introduction of structure that will become important much later in the sequence?*