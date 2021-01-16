---
title: Geometry in software
---

*My slightly edited posts from a thread originally discussed on the Beautiful Software seminar forum in November 2020, as I was in the middle of reading book 2:*

Alexander is mostly concerned about the **arrangement of matter in space**. This means looking at **geometry** makes total sense.

Software, however, is made of bits, not atoms. It doesn’t directly manifest in physical space, only indirectly through its user interface. And the laws (of physics) that apply to atoms, do not necessarily apply to bits.

Because of that, it is unclear to me how the fifteen properties can apply to the structure of software programs. (To be fair, nobody said that they should; I still want them to.)

I can see how to apply them to **user interfaces**, which have a geometric representation in physical space (sort of), even though user interfaces frequently go slightly beyond what is governed by laws of physics in the real world. For instance, think of scrolling through a long list or a long article that wouldn't likely exist with the same dimensions in the physical environment, or views that effortlessly change their size and shape, which couldn't really happen with actual matter in space.

I still fundamentally believe that there must be some equivalent of the fifteen properties for **software programs**. Programs certainly have structure, but it is structure of a different, more flexible kind, which is mostly unaffected by physical forces and processes in the real world.

Which all leads me to the now obvious question: what would these properties be and what exactly would they be based on?

---

> In short, I believe there is not that much of a difference between UI and code. Everything on screen is a symbolic representation of bits.

Hmm… I disagree, but need to think about this more. Code seems to me even more abstract, or better: less rooted in physicality and therefore geometry, than a (visual) user interface does. That's also why I believe that (simulated) physicality in modern user interfaces has a big future in touchscreens with haptic feedback and direct manipulation of virtual objects that "feels" like moving them around as if they were physical, and have a certain weight, for instance.

> As we form memories and learn things we are building “structures” in our minds about the world around us that exhibit those properties.

I suspect — but that is certainly something we haven't properly figured out yet — that it is somewhat more the other way around: the properties are manifestations of living process in the world, and we are tuned to perceive them as something more special than random arrangements of matter, or purposefully but artificially arranged matter.

There is a famous older paper [The Architecture of Complexity](https://www.cs.brandeis.edu/~cs146a/handouts/papers/simon-complexity.pdf) that talks about how there are hierarchies in nature everywhere and somewhat leaves us with the question in the end, if that is because hierarchies are a fundamental building block of how nature and the universe work, or if it's just our perception and cognition that is tuned to that particular kind of pattern. The answer is likely that it is a little bit of both, but it's good to be aware that there are these two perspectives.

I think something similar is going on here with the fifteen properties. They are perceivable artifacts of living structure and surely have their origin in the fundamental ways the universe works, but then we can only perceive them in certain ways that have much more to do with how our brain works and what specific patterns we are evolved to detect.

Cognitive science makes a strong connection between bodily experience — how it feels when we move and interact in our physical environment — and basic patterns in the brain (I'm sure I dropped "kinesthetic image schemas" somewhere already) that seem to be fundamental low-level building blocks of how we make sense of the world. They particularly manifest in language, which is pretty much the best window we have into how our brains work across cultures.

Well, I can go on and on about that, but in this thread I was actually more interested in the physicality of code (and perhaps user interfaces, too). And it seems to me that it's not that simple that the fifteen properties apply in almost the same way, as most of the substrate — laws of physics, how matter behaves — is taken away from the way we organize mostly abstract concepts and symbols.

---

UI and code are somewhat different. Now that I've read some more, I'd actually refer to Alexander and say UI is more like a descriptive (declarative?) manifestation while (imperative) code is more like a generative manifestation…? UI also mostly visualizes runtime state while program code generally doesn't include runtime state, so they can't be exactly equivalent.

In the physical environment, the 15 properties manifest in different ways, different materials, even somewhat different arrangements. But they have a manifestation in a substrate that allows us to perceive them geometrically.

What's the actual substrate in programming? What would allow us to perceive the 15 properties in code? The arrangement of machine instructions? The symbols? Their semantics? Something else?

Sure, we could express everything formally in lambda calculus or some combinatory logic and transform any kind of programming language back and forth between them and into one another (which sounds more trivial than it is ;-) — but these are isomorphisms and structurally identical from a mathematical perspective.

If I understand Alexander correctly, the fifteen properties are "structure-preserving" in the wholeness sense, but not in the mathematical sense. The beginning and end state of such a transformation are not "equivalent up to isomorphism" as they are not bijective because they add and change centers. But that's somewhat unclear to me too, and I hadn't intended to tackle the formal questions about Alexander's work (yet?). But maybe that's necessary to define the fifteen transformations for code?

I was hoping for a more practical and pragmatic way of perceiving the 15 properties in code and applying the 15 transformations to code — maybe getting more specific would help… something like: what would the GRADIENT transformation look like for a computer program? I have no idea, because I don't know how the gradient would manifest so I can perceive it… if that makes any sense?

---

Yes, we can take all the software things and represent them visually somehow, and then we have something geometrical to apply all the properties to. But when we make that whole or beautiful in the Alexandrian sense, we only did that for that particular representation. In my mind, that does not necessarily mean that the actual software is now more beautiful, just that particular representation of it.

So some things go all the way through to whatever form software has (or is this just another representation?), which could mean that perhaps some of the properties do affect the form, not just the representation. Or maybe (and perhaps likely?) it's not property specific, but it's the fact that the properties are all based on something more generic, abstract, that is the basis of all this.

With matter in space, however, I argue that the arrangement of matter in space is not just a representation. It's a thing where all the laws of physics apply. And it seems that at least some of the properties and their occurrence in nature are tied to exactly that fact.

The way I make sense of this currently is that I imagine looking at a spectrum:

    [atoms] –––––––– [bits] –––– [math]

The world of atoms with all its complex processes based on physics and all the sciences that build on top of it is on the left.
The world of math is on the right. Laws of physics don't matter here. It's all formal. It's all constructed. It's pure model.
The world of bits is somewhere in between, and I think it's a little closer to math. There are a few things, mostly related to data and state, that still have some of the properties that physical things have — they can have "size" and "weight" and use energy and there are certain limitations in play — but it's only a fraction of the complexity atoms in the physical world have.

While I neither know how useful this perspective is, nor how that would actually work out in detail, it does give me hope that the world of bits is orders of magnitude simpler than the world of atoms. And therefore I can imagine an even simpler set of properties to exist which describes these effects that we perceive as complexity. And it might even be easier to close the gap to the formal world of math and define them precisely, without having to figure out some unanswered questions in quantum physics first.

---

It appears to me that what Alexander tries to teach us with the unfolding process is that there is complexity in the form of relations between centers — everything is connected to everything else — and we need to embrace it, and the way we can still create beautiful stuff is by finding a good sequence that allows us to focus on one thing at a time in the right order to build that web of connections properly. But it's never about somehow minimizing the number of connections; it's more like embracing them because they have to exist for it to become coherent and whole.

In software we seemed to have found a different strategy to deal with complexity: we just compartmentalize everything into little isolated decoupled components. That way we never have to look at a whole and can just focus on small things. But perhaps that's why we end up with less cohesive solutions? This is equivalent to the kind of modular architecture that Alexander criticizes in his domain.

It seems that Alexander found a connection between how we perceive complexity and what the nature of complexity is. This is synthesizing physical, geometric/formal, and cognitive aspects of our existence, which Alexander clearly saw, at least intuitively, while the rest of the world is usually stuck within just one of these modes.

---

Thinking about this more:

    [atoms] –––––––– [bits] –––– [math]

It’s probably more like this:

    [atoms] –––––––– [UI] ——— [code] ––– [math]

In UI position has meaning, and things have a size. There’s also a notion of running out of space, although it’s less of a constraint as it is in the physical world. For instance, we can have arbitrary sizes by using scrolling, and it only gets annoying when scrolling far takes too long. In the real world we would run out of material or the stability of the material would no longer hold, if a physical structure becomes too large.

Code, then, is even further to the right because it has even fewer constraints acting on it. We can describe things with it (objects), which have certain relationships (properties), but these all do not exist spatially, they don’t have a position, or a size, etc. — unless we want to represent them visually and give them arbitrary positions and sizes, etc.

It seems this continuum from left to right is about removing or ignoring certain constraints that act on the elements under consideration. The further you move to the right, the fewer constraints, or rules, are in effect. Until you end up with simple mathematical (algebraic?) structures on the right.

Partially inspired by this tweet and thread: <https://twitter.com/prathyvsh/status/1332740035410419713?s=21>
