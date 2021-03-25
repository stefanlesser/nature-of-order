---
title: "The mathematical scarcity of good sequences"
---

> A sequence works, or does not work, according to the order of steps.  
> In principle, a good sequence (steps in the right order) can be defined mathematically by asking, for each center, which other centers need to be in position before that center can be formed.  
> One sets up a flow chart among the steps, defining an arrow for every case where one center must precede another. This gives a partial order on the steps: And one can then define a linear sequence (a collapsed partial order) which minimizes the cases where arrows form cycles or are reversed. This is mathematically identical to a well-known problem in flow chart analysis (PERT charts) common in industrial engineering.  

> Since good sequence is mathematically defined in this way, we may infer that one should, in principle, be able to define an unfolding sequence for any problem, **once one knows what the ingredients are**.  

*This is what pattern languages are for!*

> For a given task, the number of all sequences which work is tiny by comparison with the huge number of all possible sequences.  

*This is equivalent to the number of grammatically correct sentences in a language compared to the total number of word combinations, and of course also for formal languages in general — perhaps the difference here is that the number of words or non/terminals is usually not fixed.*

> From observations of working sequences, I believe, further, that the sequences which work are all variants of the same broad flow, all essentially similar, in which one or two steps may be transposed, but which have broadly the same overall pattern of unfolding.  
> Other than these, as sequences get more and more scrambled and out of order, the effect will be that, when being read, incoherence in the unfolding will occur, and important structure will be lost.  

> It is not possible, at present, to give a precisely defined way of identifying the sequences which work, although some progress has been made in this direction. That is to say, we do not yet know a purely mathematical procedure which can identify the sequences which work.  

> However, the sequences which work can be identified experimentally by a well-defined procedure. If one applies a sequence of steps to a given context, and if one then observes the unfolding process, it is possible to identify, unambiguously, whether the process engendered by the sequence at any time contradicts itself — that means, whether one is forced to backtrack, because step B which comes at a certain point in the sequences forces one to undo the results of the previously taken step A.  
> By doing experiments on test cases, it is possible to winnow out, and ultimately to eliminate the bad sequences, thus gradually finding one’s way to the few sequences which have the property that no such backtracking occurs as the project unfolds.  
> One technique for finding good sequences is to identify bad *sub*sequences, and eliminating all sequences which contain these bad subsequences.  
> There are a variety of ways of getting to the good sequences, and it is very hard work. But, with time, it can be done.  

*Something in here sounds a lot like machine learning to me…?*

> Since the identification of backtrack-free sequences can be made experimentally, it is clear that the concept of backtrack-free sequences is — in principle — well-defined even though in practice hard to discover.  

*This has to be a problem that must’ve been researched as part of algorithms!*

> The important thing is that such backtrack-free sequences are relatively stable. Once discovered, a backtrack-free sequence remains backtrack-free for nearly all contexts. Thus the backtrack-free sequences lie at the core of the theory of living process.  

#book/The Nature of Order/2 The process of creating life/11 The sequence of unfolding#