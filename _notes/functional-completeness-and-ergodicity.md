---
tags: Functional completeness and ergodicity
tags: software
---

### [Prabros](https://t.me/nature_of_order_chat/467)
That cliff hanger question is a pretty interesting one. I have been mulling over that aspect a bit and what I have come to notice is that there’s this idea of **ergodicity / functional completeness** that comes into play here which leads to a contextual fit.

As you rightly outlined, you can do any kind of **arbitrary labelling** to the entities of the tree structure here. But, if it is to play nicely with the (a)symmetries of the space, there’s a way to label them so that you can **traverse the entire space of possibilities with a parsimonious set of primitives**. And that is what is meant by making it ergodic as seen in these tweets: <https://twitter.com/metadiogenes/status/1280682762996011008>

So if you follow that labelling Eli has done there and use just nand or nor gate from that labelling, you would be able to **generate all the rest of the combinations**. For completeness in computation, we usually take up the set of { and, or, not } + recursion. This can be seen nicely explained by Wolfram here: <https://writings.stephenwolfram.com/2018/11/logic-explainability-and-the-future-of-understanding/>

So about the structure itself, I think there’s something about functional completeness that makes some labelling more **accessible/traversible/reachable** in some sense than others which **limit our explorability** of the system.

So I guess this in some ways ties up with your idea of creating a system which you can **differentiate to solve the problem**. So if there’s a fit as in the Alexandrian sense, I think that is when the solutions to the set of problems you are trying to optimize for are **algebraically captured by the unfolding of the initial system**. Let me know if that writing made sense.

### [Prabros](https://t.me/nature_of_order_chat/469)
> And choosing an ontology, picking those labels, is not arbitrary! It theoretically can be, of course. But that wouldn’t make sense — literally: we only pick labels that make sense to us in some way. This, I think, is how metaphorical structuring connects to this.

Yes and I think there are sensible or rather **“complete” ways to partition the space of possibilities** so that we can “commute” with ease through the whole space with a **carefully constructed map** of the space. This is in some sense what **axiomatization in mathematics** is, when it succeeds to capture the underlying space of possibilities.

Great to see you draw parallel with Alexander’s Pattern Language here. My exposure is via NoFS, so I would probably need to read his literature further to grok the different aspects where it can be seen as this sort of map of possibilities. Also, looking forward to the second half’s reply.

### [Stefan](https://t.me/nature_of_order_chat/471)
[…] It might very well be that Alexander's 15 properties are **inevitable "residue" in ergodic systems** — I'm not sure that's the correct way to characterize it, I'm just learning about ergodicity myself, but it seems intuitively similar. […]

### [Prabros](https://t.me/nature_of_order_chat/483)
> I'm still mulling over the "functional completeness" part of it. The way I see it, a grammar does play a role in filtering out some forms that become the equivalent of syntax errors, so they reduce the solution space somewhat, but that is probably not in violence of what you mean by "functional completeness"?

* what I mean by the term: <https://en.wikipedia.org/wiki/Functional_completeness>
* the set { or, and, not }, { nand }, { nor }, { imply, not } etc. are **minimally functionally complete**: <https://en.wikipedia.org/wiki/Functional_completeness#Minimal_functionally_complete_operator_sets>
* **those set of operators are the only ones needed for you to construct any logical propositions representable in boolean algebra**. 
* Of particular interest might be the characterization given by Emil Post and his construction of the so called **“Post Lattice”** there: <https://en.wikipedia.org/wiki/Post%27s_lattice>
* The idea of completeness is explained in a somewhat accessible manner in **Wolfram’s post on building minimal axiom systems** I shared above. The parallel I have drawn between ergodicity and functional completeness is that both of them **reflect the capability to explore the full extend of the language that respect the grammar**.
* So thinking in a Chomskian sense, we have a machine that accepts/generates a language generated by a grammar. **Designing the grammar well** for a certain context **would allow the machine to generate the whole range of possibilities**.
* For instance, for a regular language, this would be the **Kleene algebra** with its set of primitives that allows one to express any regular language out there. So when creating a formal system, if one has the context thoroughly in mind and then design the logical steps necessary to cover it, you get “completeness” in my mind and it is ergodic in the sense: <https://www.johndcook.com/blog/2014/11/22/ergodic/>
* To be sure, there are **distinct advantages to making a system non-ergodic**, though I lack the (physics + logic)-fu to see how just yet.

### [Stefan](https://t.me/nature_of_order_chat/509)
Thanks for the link to Stephen Wolfram's writings about minimal axiomatic systems.

I had forgotten how good a writer Stephen Wolfram is and how capable he is to describe deep mathematical concepts in an extremely accessible way.

I’m also impressed by how much he has internalized how computation can be applied to solve problems that involve traversal or exploration of huge solution spaces — exactly what computers can help us with. The way he gets to the proof is not much different to what he did in A New Kind of Science.

This also makes me want to re-read A New Kind of Science. I had read it so long ago; I’m sure I’m in a very different headspace now that will likely make my experience of reading it again like reading a book I’ve never read before. (Godel, Escher, Bach is in the same re-read category for me now.)

As I was reading Wolfram's article, one of the many links in it caught my attention: 

Picking good primitives and rules for a grammar does feel like what Stephen Wolfram describes [in this article](https://writings.stephenwolfram.com/2008/01/ten-thousand-hours-of-design-reviews/) as the core of the design process by working out the “correct fundamental primitives to cover the area”.

That sounds a lot like what Alexander's theory is all about and I can't help but see connections to Alexander in almost every sentence in that article.

### [Stefan](https://t.me/nature_of_order_chat/510)
The whole article is absolutely worth reading, but this is the part that got me excited:

In fundamental science, one starts from a bunch of phenomena, and then one tries to drill down to find out what’s underneath them—to try to find the root causes, the ultimate primitives, of what’s going on.

Well, in software design, one starts from a bunch of functionality, and then one needs to drill down to find out just what ultimate primitives one needs to support them.

In science, if one does a good job at finding the primitives, then one can have a very broad theory that covers not just the phenomena one started from, but lots of others too.

And in software design, it’s the same kind of thing.

If one does a good job at finding the primitives, then one can build a very broad system that gives one not just the functionality one was first thinking about, but lots more too.

---

## Thoughts on this discussion
* I do not yet fully grasp the role of functional completeness in structuring the solution space in a way that fewer primitives allow the reconstruction of all possible solutions.
	* What is an intuitive understanding of "generating the rest of all possibilities" from a subset of selected primitives?
	* Is this what yields the felt benefit of "compression", or does that compression also include restricting which solutions are expressible?
* I'm also still confused by the importance of completeness. Is it necessary to be able to describe all possible solutions, or is it beneficial to restrict which solutions can be described by a grammar? 
	* This seems to relate to @Prabros' comment about "distinct advantages to making a system non-ergodic". Is this also connected to Turing-completeness vs. limited domain-specific languages?
* If NAND is sufficient to express all possibilities, we still prefer the combination of AND + OR + NOT, which can also express all possibilities. 
	* Multiple different functionally complete subsets exist. How do we decide which set is "better" than another?
	* Where does the preference for a not minimal set come from? Does it map better to cognitive primitives (embodied schemas)?
	* Note the "symmetry" that exists in the { AND, OR, NOT } set! Is that another key to what makes it "feel better"?
	* This could explain why a minimalistic solution might not automatically be considered the simplest solution. "As simple as possible, but not simpler." -> Alexander's fundamental property [[Simplicity and inner calm]].
* When I use the term "differentiate", I denote Alexander's meaning as in growing a system by specializing it further, similar to the development of an embryo, as Alexander likes to use as an example. @Prabros might take its mathematical definition instead. I wonder if that causes an interesting dissonance?
	* As I think of the mathematical meaning of differentiation, I can see a connection (probably the connection @Prabros makes), and now I wonder how mathematical differentiation and integration relate to this. Intuitively, a derivative is sort of an abstraction and therefore "compression" of a more detailed function, and an integral is sort of the reverse.

---

## References
- [x] <https://twitter.com/metadiogenes/status/1280682762996011008>
- [x] <https://writings.stephenwolfram.com/2018/11/logic-explainability-and-the-future-of-understanding/>
- [ ] <https://en.wikipedia.org/wiki/Functional_completeness>
- [x] <https://en.wikipedia.org/wiki/Functional_completeness#Minimal_functionally_complete_operator_sets>
- [ ] <https://en.wikipedia.org/wiki/Post%27s_lattice>
- [x] <https://www.johndcook.com/blog/2014/11/22/ergodic/>
- [x] <https://writings.stephenwolfram.com/2008/01/ten-thousand-hours-of-design-reviews/>