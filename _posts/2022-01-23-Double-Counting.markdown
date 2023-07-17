---
layout: post
title:  "(unfinished) The Double Counting Trick, but IRL"
date:   2022-01-23 20:50:32 -0400
categories: jekyll update
---

This is an attempt to showcase the mathematical trick of considering "global values" in real world scenarios. A good introduction can be found in Chapter 7 of the [OTIS Excerpts][otis-excerpts]. 

Firstly a note on definitions. This general trick is referred to in a number of ways:
- Double Counting
- Counting in two ways
- Considering global ideas

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

## Lotteries


[nats-cd]: https://www.nytimes.com/2017/05/15/us/math-counts-national-competition.html
[otis-Excerpts]: https://web.evanchen.cc/textbooks/OTIS-Excerpts.pdf