---
title: General and repurposable tools
---

*A rough draft of an idea inspired by a tweet. Unsure if it has legs.*

> More tiny tools. More tiny composable tools.
> 
> — [@gordonbrander on Twitter](https://twitter.com/gordonbrander/status/1351016903796469763)

This tweet served as a good prompt.

I don’t think *tiny* and *composable* are the most important qualities we need for our tools. They’re not wrong. Tiny and composable is good. But not good enough.

Our tools need to be **general** and **repurposable**.

### Obligatory physical world example
A hammer is a simple tool. It is general and repurposable. The function of a hammer has little to do with nails. Its function is the embodied motion of our arm to hit a small target with it. Sure, hitting a nail to drive it into a wall is a specific action that describes best what to do with a hammer. It is [prototypical, in the Eleanor Rosch sense](https://en.wikipedia.org/wiki/Prototype_theory). But this is not the only thing that can be done with it. As a user of a hammer, it doesn’t take you long to figure out that it’s not about the nail and all about the motion. You are empowered to find other use cases for it, if you desire.

Software tools are not repurposable. At least not out-of-the-box. They are designed for a specific task. And, again, that’s not wrong. It’s just not good enough.

We found a few tricks to make them more adaptable: configuration and composition.

#### Configuration
Configuration is a rather explicit way of adapting a piece of software to another use case (a different environment). That other use case gets another detailed implementation and the user can switch with a configuration option. It’s more like having two separate tools that masquerade as one. Because the implementation is hidden from the user, it looks like the tool became more powerful.

*What I’m really trying to say here, I guess, is that this is an additive way of making something more usable in different contexts. The amount of implementation added is high. The ratio of functionality to implementation (code) is low; we get more functionality, but we also have to write a lot of code for it.*

#### Composition
Composition takes several existing tools and combines them in ways that enable new use cases. The component tools though, likely gain their functionality from configuration. That’s still “better” than configuration, because we don’t explicitly *add* new implementations and rather reuse existing blocks and the new features come from a new arrangement of components.

Yet, we need an environment that supports such composition. And in software, we have to build that ourselves. That’s still an improvement, in particular if that environment is generic. Obvious example: Unix command line and the pipe operator. It gains its power from the fact that most component tools operate on text streams (as filters) and that the Unix command line pipe operator enables concatenation of filters.

### Users and programmers
Both configuration and composition are deeply rooted in the assumption that there is a difference between users and programmers. Programmers, who know how to make a computer what they want because they can program it, encapsulate the complexity of doing so. Users, then, don’t have to become programmers; instead they can learn the much simpler task of configuring or composing the parts that programmers provide. Again, that’s not wrong. It’s good. Just not good enough.

Often, this gets compared to building the tool and using the tool. Naturally, not everyone who uses a hammer should be required to build one themselves. Obviously, there must be a benefit in separating these.

That benefit is economical. And the world we live in today puts a lot of weight on economic benefits. That’s one thing Alexander criticizes about today’s world.

I’m not sure anymore that the economical benefits of separating users from programmers are helpful in an environment where we want to improve the environment. It seems the more people who know how to build, the better? And I’m just looking at the software world here. Alexander asks this questions for the world of architecture.

If good software is adapted to the user’s context and environment — and I very much believe that this is what great software is all about — than the economic benefits of efficient construction, using tricks like configuration and composition, are detrimental to what could be achieved if the user was more empowered to adapt the software to their needs.

### Are there options beyond configuration and composition?
I am convinced there are. My bet is on the embodied part of the hammer example. General, repurposable tools **augment** us. They amplify our abilities. They help us do something better than how we would do it without the tool.

In contrast, software tools often feel like their purpose is **automation** instead. They take something that we do, and do it for us. Without us. They *replace* us. Again, not necessarily wrong in all cases, but not good enough.

What I want is a class of tools that augment our thinking in a way that amplifies our limited abilities to make sense of the world, to come up with better ideas, and to communicate them. We are still in charge. We are not replaced. We are merely enhanced.

### Different substrates
What I don’t yet understand is if our substrate in software — bits instead of atoms — limits us in our ability to build repurposable tools…? 

In the physical world we find a rich environment rooted in physics, chemistry, biology, all giving us plenty of processes to hook into and benefit from when building tools. In software, we only have what someone built before us.

This is why I believe that we need to look at these substrates in more detail. Alexander’s theory is for atoms. Some of it might very well apply to software. But there is a difference in kind of substrates that must have an impact on how we can transfer Alexander’s theory to the software world.