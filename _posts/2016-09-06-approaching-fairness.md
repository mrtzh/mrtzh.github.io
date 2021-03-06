---
layout: post
title: Approaching fairness in machine learning
author: Moritz Hardt
published:  true
comments: true
date: '2016-09-06 07:30:00 -0800'
tags:
- fairness
- machine learning
- statistics
---

As machine learning increasingly affects domains protected by anti-discrimination law, there is much interest in the problem of algorithmically measuring and ensuring fairness in machine learning. Across academia and industry, experts are finally embracing this important research direction that has long been marred by sensationalist clickbait overshadowing scientific efforts.

This sequence of posts is a sober take on the subtleties and difficulties in engaging productively with the issue of fairness in machine learning. Prudence is necessary, since a poor regulatory proposal could easily do more harm than doing nothing at all.

In this first post, I will focus on a sticky idea I call *demographic parity* that through its many variants has been proposed as a fairness criterion in dozens of papers. I will argue that demographic parity not only cripples machine learning, it also fails to guarantee fairness.

In a second post, I will introduce you to a measure of fairness put forward in a recent joint work with [Price](http://www.cs.utexas.edu/~ecprice/) and [Srebro](http://ttic.uchicago.edu/~nati/) that addresses the main conceptual shortcomings of demographic parity, while being fairly easy to apply and to interpret. A third post will use our framework to interpret the recent controversy on COMPAS scores. Finally, I’ll have an entire post on limitations of our work, and avenues for future research. My claims of future posts have been mostly wrong in the past except these posts are actually already written.

So, if you're interested in the topic, but less so in seeing pictures of Terminator alongside vague claims about AI, stay on for this blog post series and join the discussion.

## A call to action

Domains such as advertising, credit, education, and employment can all hugely benefit from modern machine learning techniques, but some are concerned that algorithms might introduce new biases or perpetuate existing ones. Indeed, the Obama Administration's Big Data Working Group [argued in 2014](https://www.whitehouse.gov/sites/default/files/docs/big_data_privacy_report_may_1_2014.pdf) that discrimination may &quot;be the inadvertent outcome of the way big
data technologies are structured and used&quot; and pointed toward &quot;the potential
of encoding discrimination in automated decisions&quot;.

It's important to understand on technical grounds how decisions based on machine learning might wind up being unfair without any explicit wrongdoing. I wrote a post on this [a while back](https://medium.com/@mrtz/how-big-data-is-unfair-9aa544d739de#.llzo69u3p). Some will be disappointed to find that the core issues have little to do with Silicon Valley billionaires or the singularity, and more to do with fundamental conceptual and technical challenges.

But it’s also important to understand that often the use of algorithms exposes biases present in society rather than creating new ones. There is an exciting opportunity of reducing bias as we move to an algorithmic ecosystem.

Despite the need, a vetted methodology for measuring fairness in machine learning is lacking. Historically, the naive approach to fairness has been to assert that the algorithm simply doesn’t look at *protected attributes* such as race, color, religion, gender, disability, or family status. So, how could it discriminate? This idea of *fairness through blindness*, however, fails due to the existence of *redundant encodings*. There are almost always ways of predicting unknown protected attributes from other seemingly innocuous features. 

## Demographic parity

After ruling out *fairness through blindness*, the next idea that springs to mind is *demographic parity*. Demographic parity requires that a decision---such as accepting or denying a loan application---be independent of the protected attribute. In the case of a binary decision $$C\in\{0,1\}$$ and a binary protected attribute $$A\in\{0,1\}$$, this constraint can be formalized by asking that

$$\mathbb{P}\{C=1 \mid A=0\}=\mathbb{P}\{C=1 \mid A=1\}.$$

In other words, membership in a protected class should have no correlation with the decision. Through its various equivalent formalizations and other variants this idea appears in numerous papers. For example, in the context of representation learning, it is tempting to ask that the 
learned representation has zero [mutual information](https://en.wikipedia.org/wiki/Mutual_information) with the protected attribute. Any classifier based on the learned representation will then inevitably satisfy demographic parity.

Unfortunately, the notion is seriously flawed on two counts. 

### Demographic parity doesn't ensure fairness

The notion permits that a classifier selects qualified applicants in the demographic $$A=0$$, but unqualified individuals in $$A=1$$, so long as the percentages of acceptance match. Consider, for example, a luxury hotel chain that renders a promotion to a subset of wealthy whites (who are likely to visit the hotel) and a subset of less affluent blacks (who are unlikely to visit the hotel). The situation is obviously quite icky, but demographic parity is completely fine with it so long as the same fraction of people in each group see the promotion.

You might argue that it’s never in the advertiser’s interest to lose potential customers. But the above scenario can arise naturally when there is less training data available about a minority group. As a result, the advertiser might have a much better understanding of who to target in the majority group, while essentially random guessing within the minority.

### Demographic parity cripples machine learning

Imagine we could actually see into the future, or, equivalently we had a perfect predictor of future events. Formally, this predictor $$C$$ would equal the *target variable* $$Y$$ that we're trying to predict with probability one. Oversimplifying the example of advertising, this predictor would tell us precisely who will actually purchase the product and who won't. Assuming for a moment that such a perfect predictor exists, using $$C$$ for targeted advertising can then hardly be considered discriminatory as it reflects actual purchase intent. But in advertising, and many other problems, the variable $$Y$$ usually has some positive or negative correlation with membership in the protected group $$A$$. This isn't by itself a cause for concern as interests naturally vary from one group to another. But in any such setting, demographic parity would rule out the ideal predictor $$C = Y$$. As a result, the loss in utility of imposing demographic parity can be substantial *for no good reason*. Demographic parity is simply misaligned with the fundamental goal of achieving higher prediction accuracy.

To be sure, there is a set of applications for which demographic parity is not unreasonable, but this seems to be a subtle case to make. Any paper adopting demographic parity as a general measure of fairness is fundamentally flawed.

## Moving forward

As I argued, demographic parity is both too strong and too weak. Hence, if you find a different condition that's strictly stronger, it'll still be flawed. If you come up with something strictly weaker, it'll still be flawed. You also won't salvage demographic parity by finding more impressive ways of achieving it such as backpropping through a 1200 layer neural net with spatial attention and unconscious sigmund activations.

If demographic parity is broken, why did I belabor its failure at such length? 

One reason is to discourage people from writing more and more papers about it without a compelling explanation of why it makes sense for their application. The more important reason, however, is that the failure of demographic parity is actually quite an instructive lesson to learn. In particular, we will see how it suggests a much more reasonable notion that I will introduce in my next post.

*Stay on top of future posts. Subscribe to the [RSS feed](http://blog.mrtz.org/feed.xml), or follow me on [Twitter](https://twitter.com/mrtz).*
