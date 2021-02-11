---
title: Beauty in code
---

*Can code itself have beauty?*

*How does the beauty of code relate to the architecture of the program that it describes?*

### Knuth’s four criteria of elegance for code
1. Leanness of code
2. Clarity of problem definition
3. Spareness of use of resources (time, processor cycles)
4. Implementation in most suitable language and system

> Matthew Fuller describes Knuth's aesthetic in his essay Elegance (2006) collected in the classic book of essays Software Studies:

> > In Literate Programming, Donald Knuth suggests that the best programs can be said to possess the quality of elegance. Elegance is defined by four criteria: the **leanness** of the code; the **clarity** with which the problem is defined; **spareness of use of resources** such as time and processor cycles; and, implementation in the **most suitable language** on the **most suitable system** for its execution.

> This is all to say that Knuthian elegance is **algorithmic elegance**, and that this draws from the **aesthetics of math**, with its latent Platonism, emphasis on axiomatics, and "beauty in simplicity" that Fazi describes in her computational idealism.

> But imagine if we changed the name of the only function in the program so that the fork bomb read like this:

    f(){ f|f& };f

> Now it is much easier to understand. It declares a function, f(), which calls itself twice. Even if you're not familiar with the \| and & symbols (& runs a process in the background), the logic of the program becomes clear. The semi-colon near the end separates the function definition from the final command: an initial call to f. That is the fuse that ignites the bomb. […]

> The aesthetic of the fork bomb, in other words, is not entirely determined by necessity and brevity, but also involves the conscious choice to make the short program appear **alien** and **inscrutable**, written in all punctuation. It makes the script **feel machinic**, not at all intended for the human reader. Jaromil's fork bomb is perhaps the shortest program that one could call obfuscated.

From <https://esoteric.codes/blog/esoprogramming-and-computational-idealism>