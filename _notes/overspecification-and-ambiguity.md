---
title: Successively adding detail — over-specification and ambiguity
---

> Successively adding detail to a description of a process (meta, I know), is exactly how you make software.
> 
> Software development is little more than mapping a desired outcome to a precise procedure for achieving that outcome, and as we carry this mapping-out, we successively add detail.
> 
> — [Place, Space, Time](https://dorian.substack.com/p/place-space-time)



> Code both over-specifies the business logic, and specifies it inaccurately.
> 
> — [Code Only Says What it Does](http://brooker.co.za/blog/2020/06/23/code)

This almost rhymes with: 

> Beauty comes when form fits function. The real world is bumpy, and the most efficient solutions are tailored to that bumpiness. Hence Alexander likes everything to be specialized; he doesn't go for much low-level reuse. He does go for reuse at higher levels. He has symmetries and recurring patterns. He seems to believe beauty involves the tension between high-level symmetry and low-level bumpiness.
> 
> — [Software Lacks a Body](http://wiki.c2.com/?SoftwareLacksaBody)

In natural (spoken/written) language we deal with concepts that are only roughly defined in our heads, just enough that we understand the meaning. And in those situations where we don’t understand, we can often learn about it just enough by asking a quick question.

There is power in wielding symbols as stand-ins for concepts and accepting the ambiguity that comes with it. We don’t have to specify ideas down to their last bits and atoms, we just need to get to a level of abstraction that is far enough down to make sense.

We can’t do that in software. I mean, we can, and design patterns are one way of doing exactly that (and [[Unfolding a LISP|here I’m thinking of another]]), but to get from a pattern to a working software application we need to get all our bits in order — we have to over-specify it such that a dumb machine knows exactly what to do.

> In the process of making software, a subject that is near and dear to me, I have found that the information gathered that yields the decisions that configure the final product tends to get tossed when that product is realized. This I consider to be a grievous mistake.
> 
> […]
> 
> Source code is far and away the most perishable part of the system, but it’s treated as the most valuable because it’s the part that does the work. Effort into the precursor material is only as much as it takes to get to the code, and then it’s locked away in formats that are not (at least conveniently and/or persistently) addressable. I believe this is a terrific waste and I endeavour to do something about it.
> 
> — [Place, Space, Time](https://dorian.substack.com/p/place-space-time)

### Documentation as higher-level specs
We mostly think of higher-level specs as documentation for making changes later or maintenance and we tend to do it after the fact, if we do it at all.

> I'm not advocating for Big Design Up Front. Many of the most important things we learn about a project we learn during the implementation. Some of the most important things we learn years after the implementation is complete. Design documentation isn't a static one-time ahead-of-time deliverable, but an ongoing process. Most importantly, design documentation is not a commitment to bad ideas. If it's wrong, fix it and move forward. Documentation is not a deal with the devil.
> 
> […]
> 
> Building long-lasting, maintainable, systems requires not only communicating with computers, but also communicating in space with other people, and in time with our future selves. Communicating, recording, and indexing the intent behind our designs is an important part of that picture. Make time for it, or regret it later.
> 
> — [Code Only Says What it Does](http://brooker.co.za/blog/2020/06/23/code)

It seems that we have it backwards. Higher-level specs should help us *generate* a fully detailed result. Not in a planning kind of way. More in a pattern (or sequence) kind of way. Those patterns can potentially be reused if we ever need a similar solution again, although re-use is not the main reason to do it. The main reason is that it helps us do what looks like maintenance, even though it is just further unfolding the whole in response to its environment, after that arbitrary chosen moment in time when it was supposed to be “done”.

### Specifying process vs. specifying results
This also seems connected to the connection between specifying process and specifying results, or imperative vs. declarative. Sometimes it’s easier to precisely specify the result, and sometimes it’s easier to specify the process instead. Alexander seems to make a point that to create living structure, it is much easier to describe the process to generate a living result and that it is next to impossible for us to describe the intricate details of the result.

Specifying a (generative) process allows creating much more complex output than what we could come up with if we had to describe the structure of that output. Complexity needs to grow. It shouldn’t be designed.