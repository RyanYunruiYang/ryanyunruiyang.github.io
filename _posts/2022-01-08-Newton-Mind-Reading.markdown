---
layout: post
title:  "Missing Token Prediction isn't just for LLMs. Empathy and My Pet Theory for how Newton Actually Came Up With Gravity"
date:   2022-01-08 23:50:32 -0400
categories: jekyll update, essay
---

<blockquote class="wp-block-quote is-style-default"><p>Holmes had been seated for some hours in silence with his long, thin back curved over a chemical vessel in which he was brewing a particularly malodorous product. His head was sunk upon his breast, and he looked from my point of view like a strange, lank bird, with dull grey plumage and a black top-knot.<br><br>“So, Watson,” said he, suddenly, “you do not propose to invest in South African securities?”<br><br>
</p><cite>The Adventure of the Dancing Men", from the collection&nbsp;<em>The Return of Sherlock Holmes</em>&nbsp;(1905)</cite></blockquote>

There are some really cool neuroscience results that come from the study of people who have had the two halves of their brains surgically separated. This is done to prevent some specific kinds of seizures, and allows most people to live normal lives 99% of the times -- but there's still the last one percent.

Notably, the Right Brain processes the visual feed from the Left Eye, and the Left Brain processes the visual feed from the Right Eye. And so experiments have been done where they show the LeftEye/RightBrain of these people a sign that tells them to get up and walk. And then, once they've stood up, they ask participant "why they stood up." Now, since the LeftBrain controls language, but the RightBrain saw/responded to the command, the Left Brain *has have no idea why.* But, without missing a beat, it makes up an explanation, "to stretch my legs," "to get a soda," whatever.

My point with this anecdote is that behavior isn't even explainable to the acter themselves sometimes so it is hubris to attempt to guess what's going on in the minds of others. This question, of whether reading minds and guessing intentions is really interesting, with applications from AI-Box experiment to English course curriculum design, and with new breakthroughs in neuroscience and AI providing new insights.

But nothing I'm doing here is that fancy, I just have three fun examples:
- Newton's Theory of Gravity
- USA IMO TSTST 2021/5
- Trisolaran Metaphors

## How Newton Really Came Up With Gravity 
 The first theory is about how Newton came up with gravity. Everyone knows the story of Newton sitting under an apple tree when the apple falls and bonks his head, and “Eureka!” he figures out that gravity pulls the apple. There’s another, more credible account found in Newton's biography, "Memoirs of Sir Isaac Newton’s Life" by William Stukeley, which says that:
 > After dinner, the weather being warm, we went into the garden and drank tea, under the shade of some apple trees…he told me, he was just in the same situation, as when formerly, the notion of gravitation came into his mind. It was occasion’d by the fall of an apple, as he sat in contemplative mood. Why should that apple always descend perpendicularly to the ground, thought to himself...

But this is sooo boring. Instead, imagine this, and tell me it doesn't sound true:
> Newton is lying down under an apple tree, staring up at a juicy red apple. He wants to get the apple, but doesn’t want to climb up the tree to pick it himself. So he pretends to pull it, somehow applying Force through the medium of the air. Suddenly, the apple falls! Newton has a brief moment where he thinks that he magically pulled the apple down, but this is clearly impossible. Still, he knows that some force must have acted on the apple, and while lying on his back he turns around to see what else could have applied the force. And what was the only thing behind him at the time? The Earth. Thus, the only logical conclusion was that the Earth pulled the apple, and the theory of gravity was born. 

## USA TST 2021/5

Now, believe it or not, this strategy of guessing intentions is in some edge cases useful in mathematics. Most olympiad problems are not susceptible to this -- they are written by considering objects and finding nice properties just like in modern mathematics -- and you can't [read God's mind](https://slatestarcodex.com/2015/06/02/and-i-show-you-how-deep-the-rabbit-hole-goes/).

On Day 2, the second problem (#5 overall), was the following ([Source](https://artofproblemsolving.com/community/c2582544_2021_usa_tstst)):
> Let T be a tree on n vertices with exactly k leaves. Suppose that there exists a subset of at least (n+k-1)/2 vertices of T, no two of which are adjacent. Show that the longest path in T contains an even number of edges. (A tree is a connected graph with no cycles. A leaf is a vertex of degree 1.)

This problem ended up being really funny because I managed to solve it based on a few meta observations. 

The first was that (n+k-1)/2 was likely an upper bound, because if it weren’t, then it would not play well with the parity-based conditions. Then, as I tried to prove that this was an upper bound, I noticed that describing the equality case was incredibly weird, and so 1 hour into the problem I had found the morally correct characterisation. This reformulated problem was "Find the equality case of the inequality f(T)<=(n+k-1)/2, where f(T) is the size of the maximum subset of T which contains no edges”. Then, as a side effect, we will hopefully find that the distance between each pair of edges is even. Importantly though, this is not what we are actually trying to show, the more important thing is to first fully characterize the equality case.</p>

You can read my full solution in [post #4 of the thread](https://artofproblemsolving.com/community/c6h2737024p23864222).



## The Three Body Problem - Trisolaris is China
This one's rather dull, sorry. It's just a normal piece of literature analysis -- made ever more slightly interesting by the possibility of scandalous political disloyalty. 

Namely, in the Three Body Problem, Trisolaris is a metaphor for China, and is a criticism of the things that are holding the nation back. Liu CiXin is not above dodging censors, the Chinese edition had the Cultural Revolution section moved to the more obscure middle to avoid censorship, which was promptly moved back to the front by Ken Liu when he translated it.

Anyways, I like to imagine that Liu Cixin wrote 3BP while having Humanity represent the West and Trisolarans represent China. The origin story of Trisolaris is as follows:
- It's a civilization that emerged on a planet orbiting a chaotic set of three stars, which lead to "chaotic" and "stable" eras with a massive cycle of death and rebirth, disunity and reunification ... *sounds an awful lot like the dynastic cycle of Chinese history no?*
- Politically, Humanity is portrayed as inefficient and materialistic, yet prevails because of their intellectual diversity; on the other hand, Trisolaris is organized and efficient, irreverent towards human rights with an authoritarian government structure thanks to a quirk of biology they directly read each other's thoughts ... *state censorship!*


## Conclusion
Guessing what other people are thinking is an amusing hobby. It has its limits -- the idea that we actually are in control of our own thoughts is an illusion -- but it's also a foundational part of the Theory of Mind. These examples are kinda silly (except the TST one which helped me make TST group). As direct mind reading becomes a real possibility, and indirect mind reading already taking on the triumphant role of "sole commerical application of AI," looking inwards is here to stay.