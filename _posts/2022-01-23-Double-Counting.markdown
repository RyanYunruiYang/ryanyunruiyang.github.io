---
layout: post
title:  "The Mathematical Power of Self-Consistent Measurements (Global Combinatorics)"
date:   2022-01-23 20:50:32 -0400
categories: jekyll update, essay
---

> sabbe saṅkhārā aniccā 
> (All conditioned things are impermanent)
\- Buddha

One of the most beautiful parts of mathematics is that once you construct an object, it is truly permanent, and self-consistent to measurement. This property of mathematics is taken advantage of by a mathematically technique called "considering global values." [1] This post will outline the basic mathematical techniques, and then pivot to interesting non-mathematical application where the technique is still true up to approximation.

# Part 1

This general trick is referred to in a number of ways:
- Counting in two ways
- Global ideas

And the following mathematical ideas are special cases of the more general principle:
- Swapping the order of summation
- Linearity of Expectation

## Canonical Math Example (1 of 2): Pecking Decks
I'd like to start with the example that first exposed me to this idea
> In a barn, 100 chicks sit peacefully in a circle. Suddenly, each chick randomly pecks the chick immediately to its left or right. What is the expected number of unpecked chicks? ([MATHCOUNTS 2017][nats-cd])


The direct solution is to apply the "Linearity of Expectation." The argument there would be that the probability that any individual chick is pecked is 1/4, so each pick is expected to contribute "1/4" to the number of unpecked chicks. This is true for all 100 chicks, for a total expectation of 25 unpecked chicks. 

But there's something deeper happening here. There is a very deep and fundamental idea which is that objects exist and have permanence. 

For this problem, consider all $2^100$ different multiverses, where each chick pecks left or right. Then, consider the number of (unpecked chick, multiverse) pairs. Let $X$ be the number of such pairs.

This is a degenerate case so this first method is weirder than normal. Nevertheless, let $Y$ be the expected number of unpecked chicks in some universe. Then, $2^{100}\cdot Y$ should be the total number of (unpecked chicks, multiverse) pairs.

So now let's count it in a second way. Consider a specific chick A. How many multiverses are there in which chick A is unpecked? It ends up being $2^{98}$. The two neighboring chicks must peck away, and the other 98 can peck either way. Thus, for chick A, there are $2^{98}$ multiverses for which the (unpicked chick where that chick is A, multiverse) pair exists. But the unpicked chick can be any of the 100 chicks, and each of them are a chosen chick in $$2^{98}$$ multiverses, so $X= 100 \cdot 2^{98}$.

Put together,
$$2^{100}\cdot Y = X = 100 \cdot 2^{98}$$
Which gives $$Y = 100\cdot \frac{2^{98}}{2^{100}} = 100\cdot \frac14=25$$.

## Canonical Math Example (2 of 2): Handshake Lemma
Another canonical example is the following, given first abstractly and then more concretely, with the real life example making the proof seemingly obvious.
> Abstract: Let G be a simple graph (a set of vertices where each pair of vertices either has an edge between or not). Then the sum of all the degrees of vertices (number of edges into the vertex) of G is twice the number of edges.

But when you phrase it like this
> Handshake: A group of people are at a party. While there, some pairs of people shake hands. Let the degree of a person be the number of hands that person shook. Then, the sum of the degrees of all people is equal two twice the number of handshakes.

A lot more obvious in the second one right? Clearly each handshake counts to two people's degrees.

But the point of using "global" ideas is to measure one well-defined quantity in two ways because every well-defined quantity has a single value. Here, this would be done by counting the number of (V,E) pairs where V is a person and E is a handshake they partook in. If $X$ is the number of such pairs, then
$$\sum deg(V) = X = 2E $$
Since each vertex is in deg(V) such pairs, and each edge is in two such pairs.

## Part 2
And now for a hard pivot. I don't have *great* intuition about why this is the same as global combinatorics, but it feels similar?

## Lottery Math is Overcomplicated
The way that people usually claim that the lottery is a scam is by multiplying a bunch of numbers to find that the probability of winning. For examples, with a lot of calculations, the probability of winning the Mega Millions is “1 in 302,575,350”, and since the payout is less than 2$ * 302,575,350, you’d lose money on average. This is absurd though, it plays into the lottery’s abuse of human’s inability to intuitively grasp large numbers, and it’s so complicated that Khan Academy used it as a math exercise.

There’s a far simpler way to show that lotteries are a cash grab by the state. Instead of considering cash flow on the consumers end, consider it from the side of the government. (By law, lotteries must be run by the government) Even before taxes, a simple way to see that you cannot make money on it is the following quote:

“For Mega Millions (and Powerball) tickets, 50 percent of the sales goes to the prize pool. The remaining 50 percent is used to pay for the states’ retailer commissions, vendor fees, lottery administration, and the state beneficiaries or good causes of that state,” she told ABC News.

https://abcnews.go.com/US/mega-millions-lottery-lottery-money-states/story?id=58661412
Thus, on average, you will get back 50% of your ticket price. This is a lot simpler than figuring out the probabilities of each payout, and finding the expected payout that way.

But wait there’s more! When the payout finally happens, these massive sums of money are taxed at the highest interest bracket. The lottery is especially brilliant because it takes money from people who are usually lower income, and thus have untaxable money, and then put that together into one massive pot that can be taxed at the 50% maximum tax rate (federal + state taxes).

Somewhat expectedly, Vox says that

You hear it a lot: The lottery is a tax on people who are bad at math.

https://www.vox.com/identities/2016/1/13/10763268/lottery-poor-prey
But even the people who are “good at math” and calculate the probabilities are thinking about it in the wrong way. It is far simpler to consider it from the dual questions of “why does the government bother doing this?” and “what’s their profit margin?”

## Economic Production and Energy Consumption
A surprising example of a nonmathematician using these ideas is Li Keqiang, the current Premier of the PRC. The story goes that in order to measure economic growth, he created his own list of indicators to track because he did not trust GDP estimates. The Li Keqiang index tracks railway cargo volume, electricity consumption, and loans disbursed by banks.

This is another example of double counting because instead of calculating GDP as the sum of all economic activities, (calculating sum_{v\in G} deg v in the first example), one can simply record some economic indicators which should go up with economic activity instead. (like counting 2*|E|).

Pyramid Schemes
Another fun double counting example is this scam that went around on instagram awhile ago. I happened across it when I went on instagram for the first time in a week.


From the internet. The ones that the people I follow posted were much flashier.
I’m looking for people to participate in a huge book exchange pyramid scheme. You can be anywhere in the world. All you have to do is buy your favorite book (just one) and send it to a stranger (I’ll send their details through in a private message).

You’ll receive roughly a maximum of 36 books back to you, to keep (we have sponsors or something). They’ll be favorite books from strangers around the world!

If you’re interested in taking part, please send a message saying “GULLIBLE”

My satirical version which I posted to my story. It got shoutouted/reposted by a Choate meme account 🙂
This is absurd by double counting. Firstly, this is obviously a pyramid scheme and some people will end up with no books because it’s impossible for everyone to receive more books than they buy.

Formally though, this violates the fact that in a directed graph, the sum of indegrees = number of edges = sum of outdegrees. (indegree is the number of arrows pointing to a graph, corresponding to buying a book for someone, and outdegree is the number of outward pointing arrows, corresponding to getting a book bought for you.)

Fermi Problems
Finally, this idea works pretty well in Fermi problems. Pretty much all Fermi problems where you don’t follow the most obvious thought process is a form of Double Counting. My favorite Fermi problem/solution pair is an answer to

“ How many hairs are present on your head?”

Instead of directly counting, we consider the balding process. Usually men lose hair and eventually go bald over the period from age 50 to age 80, so a period of 30 years. You don’t hear about balding men losing more hair than young people, and it seems reasonable to lose around 20 hairs a day. This gives

20 hairs/day * 30 years * 365 days/year = 219,000 hairs

The actual answer is ~100,000, which is surprisingly close to the estimate generated by considering balding men.

Conclusion
There’s a lot of olympiad math ideas which are extremely powerful in math, but also very useful in real life. There are people like Li Keqiang who have a decent informal grasp of ideas like counting in two ways. However, understanding the formal mathematical version makes the usage more conscious and therefore more powerful.

There’s two other ideas that I want to talk about, sharp ness and equality[1]. These are more philosophical, but they are also very powerful.

One thing I need to figure out is whether showing the informal examples first, and then the math, would be more accessible to a non-mathematical reader. I might try doing that in the post about sharpness or equality.

I guess leave a comment about which structure you would prefer?

[1] Unfortunately unaccessible if you’re not in OTIS 🙁 There doesn’t seem to be any good online source on what equality is, so this means that I’ll probably write about equality next.

## Footnotes
[1] A good formal introduction can be found in Chapter 7 of the [OTIS Excerpts][otis-excerpts]. 

[nats-cd]: https://www.nytimes.com/2017/05/15/us/math-counts-national-competition.html
[otis-Excerpts]: https://web.evanchen.cc/textbooks/OTIS-Excerpts.pdf
