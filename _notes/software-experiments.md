---
title: Software experiments
published: false
---

*Some rough and random ideas of what I’d like to experiment with when taking insights from _The Nature of Order_ and apply them more or less directly to software design and development.*

### Create a pattern language for an app based on community feedback
I’d like to collaboratively create a pattern language for a (small) app based purely on how a group of potential users describes their ideal solution. The challenge will be to not take their specific descriptions of how they think it should look like and how they think it should work at face value, but to try to find the deeper reasons of what it is they would like to have, and what it is that they would like to do.

> So altogether the pattern language for that campus is really like a poem of two hundred statements going from the very, very big things about this place all the way down to the little tiny ones about window sills and plants and so forth. It describes in almost poetic but concrete fashion what that world could be like.

### *Unfolding interpreters* (working title)
Use a strong type system to formally grow an app with just the abstract functionality defined, iteratively adapting the abstract components (centers) into more detailed, less generic centers, step by step.

### Growing an app through differentiation
Take an existing solution — for instance a Markdown library, or a Rogue-like game — and re-implement it from first principles using an adaptive approach. How can functionality be added in a broad, generic way (e.g., Markdown: first symbol on line determines paragraph type), implemented in such a generic form, and then further differentiated over time? How can we prevent constant additive changes and use differentiation to add features? What does that mean for specifying differentiation at certain levels within such an app?

What would a pattern language for Markdown look like? What would be a version look like that balances functionality with implementation complexity, deliberately making design choices that keep the implementation simpler, even if that means features are not as powerful? *Implement a text editor that can overlay the text with several layers of ranges, which might overlap, that describe context information that applies to these ranges.*

How does this all relate to eDSLs? Is there a language for specifying functionality in a more abstract way? What would such a language look like?

### Process vs. result
Sometimes the process to achieve a result is more difficult to describe in detail than the desired result. Sometimes the process is easier to describe in detail than the result. In which cases is either true? When should we prefer declarative descriptions over imperative ones and vice versa?

### Designing for uncertainty
How can we design and implement abstract features that enable the end user to find creative use cases that were not anticipated in the initial design?