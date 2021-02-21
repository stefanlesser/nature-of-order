---
title: Growing a LISP with structure-preserving transformations
---

*An experiment to find ways to explore the solution space of program implementations in a way that resembles unfolding and preserves the structure of previous steps.*

See also: [[Unfolding a LISP]]

### Process
I started with [an extremely simple LISP I wrote in Swift](https://github.com/stefanlesser/TinyLisp), inspired by [this LISP written in Ruby](https://github.com/fogus/ulithp).

[My first working implementation](https://github.com/stefanlesser/TinyLisp/blob/891b6b598570b6f61f34a9cd13c1744101931a36/Sources/TinyLisp/TinyLisp.swift) is about ~150 lines of uncommented Swift code and was deliberately designed to only work with lists and string atoms. There was no capability to work with numbers at that point. I wrote a few tests (by far not enough), and they pass. It seems to work.

[I then added the capability to distinguish string and number atoms in the most naive way I could think of.](https://github.com/stefanlesser/TinyLisp/commit/a167ec7cf6d21c453aea42ae65a58714fa078cab?branch=a167ec7cf6d21c453aea42ae65a58714fa078cab&diff=unified) The change requires touching a lot of the core functions — changing the structure significantly. It works as far as the existing tests and two added tests implementing a Fibonacci algorithm can tell.

### Adding features with structure-preserving transformations
I wonder, is it possible to add the capability to work with numbers *without* changing the structure of the previous, strings-only version?

* Which methods allow to extend the existing working system by only making additive changes (preferably in a separate source file)? *In my mind, this would be a structure-preserving transformation: the previous version isn’t changed, it’s structure preserved, and the additions differentiate the previous version enough to enable new functionality, without destroying what worked before. The interesting bit is to make this work under the constraints that both versions need to keep working.*
* What would the structure of the previous version ideally look like to enable and perhaps even encourage differentiation in future steps? *This is the key question, with potential to figure out techniques that enable actively designing for not yet anticipated changes.*

#### Potential approaches
One option to achieve this could be with **inheritance**. However, the original version would need to be written very differently in an object-oriented style.

Another — more “swift-y” way — could be to leverage the **type system** and generalize the strings-only version enough such that the differentiated numbers-version could inject more concrete types.

Usually, we leverage generics to make specific implementations more widely usable in other contexts. We go from most specific to less specific/more generic. There is also a sentiment that this is the right way to do this.

But what if we went the other direction? What if we started with abstract types everywhere and carefully and gradually added more specifics — in the form of protocol conformances on parametric types? That sounds to me like a pretty literal translation of Alexander’s process to software development.

*I’m not sure if this already counts as a proof-of-concept, but [I’m surprised how straightforward that was in this rather simple example.](https://github.com/stefanlesser/TinyLisp/commit/96890b2508cdc86e0ca7eeab011efbe362162264)*