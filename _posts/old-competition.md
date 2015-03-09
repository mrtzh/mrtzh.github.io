---
layout: post
published: true
title: How to break a machine learning competition
author: Moritz Hardt
comments: true
date: '2015-02-27 09:00:00 -0800'
tags:
- tcs
---

Machine learning competitions have become an extremely popular format for
solving prediction and classification problems of all sorts. The most famous
example is perhaps the Netflix prize. An even better example is
[Kaggle](http://www.kaggle.com), an exciting data science startup that's
organized more than a hundred competitions over the past few years.

Lately I've been fascinated with machine learning competitions even though I'm generally
a sceptic when it comes to competitions of any kind. (As you would expect from
a true sceptic, I really suck at them and criticizing is the obvious way of coping.) Competitions already seem grossly
overused as a solution concept in our society. They clearly make a lot of
sense in professional sports, but do we really need every other part of our
life to look like the finish sprint of a Tour de France stage? I really doubt
it and at any rate it's not a world
I'd like to live in. Nevertheless, the appeal of the format in the context of
machine learning is pretty clear. Much like cyclists on the finish line, it
seems like you can easily and accurately score classifiers on your data, produce a
ranking, and determine a winner. Done.

As it turns out, scoring submissions and maintaining a leaderboard that
accurately reflects the true performance of each team is a suprisingly deep
problem; the more I worked on it the more surprised I was that  machine
learning competitions at all work as well as they do. In this blog post, I
will describe how to *break* a typical leaderboard.  A second post (no, really!) will show how to
(provably) prevent anything like that from happening. While there are decades of
work on estimating the true performance of a model (or set of
models) from a finite sample, the leaderboard application highlights some
challenges that while fundamental have only recently seen increased attention.

Both posts closely follows a [recent paper](http://arxiv.org/abs/1502.04585)
with Avrim Blum, but my interest in the topic goes back to an [earlier work](http://arxiv.org/abs/1411.2664) with Cynthia Dwork, Vitaly Feldman, Toni Pitassi, Omer Reingold and Aaron Roth, as well as [a work](http://arxiv.org/abs/1408.1655) with Jon Ullman.

## The leaderboard problem

Recall the typical format of a competition. Each team can repeatedly submit classifiers to the host of the competition in an attempt to improve on their previously best submission. Each submission receives a score that should ideally reflect the prediction accuracy of the classifier on the underlying distribution from which the data were drawn. Of course, we don't know the underlying distribution and so we must estimate the true score of the classifier from the available sample. There are several ways to go about this and I'll desribe the natural mechanism used by Kaggle and many others. If you're familiar with this, skip ahead to the next section.

### The Kaggle mechanism ###
The Kaggle mechanism is a variant of the classic holdout method. Kaggle partitions the data into two sets: a training set and a holdout set. The training set is publicly available with both the individual instances and their corresponding class labels. The instances of the holdout set are publicly available as well, but the class labels are withheld. Predicting these missing class labels is the goal of the participant and a valid submission is a list of labels---one for each point in the holdout set.

There is a score function \\(s\colon \mathbb{R}^N\to[0,1]\\) that maps a submission consisting of \\(N\\) labels to a numerical score, which we assume to be in \\([0,1]\\). Typically, the score reflects the *average loss* of the classifier with respect to the withheld labels. More formally there is a bounded *loss function*
\\(\ell\colon\mathbb{R}\times\mathbb{R}\to[0,1]\\) so that
<div>
\[
s(y) = \frac1N \sum_{i=1}^N \ell(y_i^*,y_i),
\]
</div>
where \\(y^*\\) is the vector of withheld labels.

The loss function is not very important for this post. For concreteness, take it to be the
0/1-loss, i.e., misclassification rate of a classifier (lower is better). Formally, a submission incurs loss 1 for each incorrect label and loss 0 for each correct label. The sum of all losses is divided by the number of all labels so that the total loss is between 0 and 1.

The central component of any competition is the leaderboard which ranks all
teams in the competition. What Kaggle does is to split the holdout labels randomly into a final test set and an intermediate holdout set \\(H\subseteq[N]\\) of size \\(n\\). The *public score* is defined as
<div>
\[
s_H(y) = \frac 1n \sum_{i\in H} \ell(y_i^*,y_i).
\]
</div>
When a participant submits a vector \\(y\in\mathbb{R}^N\\), Kaggle releases \\(s\_H(y)\\) rounded to five (or more) digits of precision. The public leaderboard simply ranks each team according to the lowest public score achieved so far.

### Static vs interactive data analysis ###

The intuition behind the Kaggle mechanism and similar leaderboard algorithms stems from the classic holdout method. In the clasic method we split data randomly into training and test data and only use the test set for our final model assessment. The idea is the test set serves as a fresh sample providing an unbiased and well-concetrated estimate of the true loss of the classifier on the underlying distribution. One point of departure from the classic method is that participants actually do see the data points corresponding to test labels which can lead to some problems. But even if they don't look at those data points, there's a more fundamental reason why the validity of the classic holdout method breaks down in the Kaggle setting.

The problem is that a submission in general incorporates information about the holdout labels previously released through the leaderboard mechanism. As a result, **there is a statistical dependence between the holdout data and the submission**. Due to this feedback loop, the public score \\(s\_H\\) *may no longer be an unbiased estimate* of the true score. There is no reason not to expect the submissions to eventually overfit to the holdout set.

The problem of overfitting to the holdout set is well known. Kaggle's forums are full of anecdotal evidence reported by various competitors. The primary way Kaggle deals with this problem is by limiting the rate of resubmission and (to some extent) the bit precision of the answers.

In this post and the next I'll try to arrive at a more principled understanding of this phenomenon. Indeed, Kaggle's use of the holdout method is just one example of a widespread disconnect between what I call *static* data analysis and *interactive* data analysis. The holdout method is a static method in that it assumes that the model is independent of the test data on which it is evaluated. Kaggle competitions are interactive, because submissions generally incorporate information from the test set.

![Static vs Interactive](/assets/staticvsint.jpg)

I content that most real world data analysis is interactive. It takes a lot of discipline to use your test set only once. Unfortunately, most of the theory on model validation and statistical estimation falls into the static setting requiring independence between method and test data. We will revisit this picture in the next post when we talk about algorithms that provably prevent overfitting in the interactive setting. In this blog post, I will instead illustrate why accurate loss estimatation in the interactive setting is much trickier than in the static case.

<!---
In other words, there is a feedback loop between the model and the holdout data on which the model is evaluated.

1. There is no a priori understanding of what learning algorithms are going to
be used. In fact, this is the point of a competition. We have no bound on the
complexity (e.g., VC-dimension) of the set of classifiers that we score.

2. Submissions are just a set of labels. There is no information which
learning algorithm was used to produce the labels. In particular, the organizer can't apply cross validation or
bootstrapping in attempt to improve the loss estimate for a submission.

3. Finally, *submissions are adaptively chosen*. This means that
a subission might incorporate information previously released by the
leaderboard mechanism.
-->

## Whacky boosting: a cautionary tale ##

Imagine your most humble blogger in a parallel universe: I'm new to this whole machine learning craze. So, I sign up for a Kaggle competition to get some of those skills. Kaggle tells me that there's an unknown set of labels \\(v\in\\{0,1\\}^N\\) that I need to predict. Well, I know nothing about \\(v\\). So here's what I'm going to do. I try out a bunch of random vectors and keep all those that give me a slightly better than expected score. If we're talking about 0/1-loss, the expected score is 0.5. So, I'm keeping all the vectors with score less than 0.5. Then I recall something about boosting that I saw on the internets. It tells me that I can boost my accuracy by aggregating all predictors into a single predictor using the majority function. Slightly more formally, here's the algorithm I come up with:

**Algorithm** (Whacky Boosting):

1. Choose \\(w_1,\dots,w_k\in\\{0,1\\}^N\\) uniformly at random.
2. Let \\(I = \\{ i\in[k] \colon s\_H(w) < 0.5 \\}\\).
3. Output \\(w=\mathrm{majority} \\{ w_i \colon i \in I \\} \\).

Lo and behold, this is what happens:

<div style="text-align:center">
<object data="/assets/boosting.svg" type="image/svg+xml">
<param name="src" value="/assets/boosting.svg">
  <img src="/assets/boosting.png" />
</object>
<p style="text-align:center">In this plot, \(n=4000\) and all numbers are averaged over 5 independent repetitions.</p>
</div>

As I'm only seeing the public score (bottom red line), I get super excited. I keep climbing the leaderboard! Who would've thought that this machine learning thing was so easy? So, I go write a blog post on Medium about Big Data and score a job at DeepCompeting.ly, the latest data science startup in the city. Life is pretty sweet. I pick up indoor rock climing. Do wood working classes. Read some books about espresso. Two months later the competition closes and Kaggle releases the final score. What an embarrassment! My boosting algorithm does nothing whatsoever on the final test set. I get fired from DeepCompeting.ly days before the buyout. My spouse dumps me. The lease expires. I get evicted from my apartment in the Mission. Inevitably, I hike the Pacific Crest Trail and write a novel about it.

So, let's understand what went wrong and how you can avoid hiking the Pacific Crest Trail. To start out with, each \\(w\_i\\) has loss around \\(1/2\pm1/\sqrt{n}\\). We're selecting the ones that are biased below a half. This introduces a bias in the score and the conditional expected bias of each selected vector \\(w\_i\\) is roughly \\(1/2-c/\sqrt{n}\\) for some positive constat \\(c>0\\). So we made some progress. Put differently, each selected \\(w\_i\\) is giving us a guess about each label in \\(H\\) of the unknown vector \\(v\\) that's correct with probability \\(1/2 + \Omega(1/\sqrt{n})\\). Since the public score doesn't depend on labels outside of \\(H\\), the conditioning does not affect the final test set. The labels outside of \\(H\\) are still unbiased. Finally, using simple properties of the majority function the vector \\(w\\) is giving us a guess for each label in \\(H\\) that's correct with probability
\\[
\frac12 + \Omega\left(\sqrt{k/n}\right).
\\]
Outside of \\(H\\), we're just random guessing.
Hence, the public score of \\(w\\) satisfies
\\[
s\_H(w) < \frac12 - \Omega\left(\sqrt{k/n}\right).
\\]
In words, whacky boosting gives us *a bias of \\(\sqrt{k}\\) standard deviations on the public score with \\(k\\) submissions*. In contrast, the final score will be roughly \\(1/2\pm 1/\sqrt{N}\\).

What's important is that the same algorithm still "works" even if we don't get exact answers. All we need are answers that are accurate to an additive error of \\(1/\sqrt{n}\\). This is important since Kaggle rounds its answers to 5 digits of precision. In particular, this attack will work so long as \\(n< 10^{10}\\).

### A neat generalization ###

Let's switch perspectives and think of whacky boosting as an algorithm we can run to force a difference between the public and final leaderboard. A limitation of the previous algorithm is that it requires the domain to be Boolean and it only gives an advantage over random guessing. It turns out that both of these issues can be resolved nicely with a simple generalization of the previous algorithm. What was really happening in the algorithm is that we had two candidate solutions, the all ones vector and the all zeros vector, and we tried out random coordinate-wise combinations of these vectors. The algorithm ends up finding a coordinate wise combination of the two vectors that improves upon their mean loss, i.e., one half. This way of looking at it generalizes nicely. The resulting algorithm is just a few lines of code.

{% highlight julia %}
# select coordinate from v1 where v is 1 and from v2 where v is 0
combine(v,v1,v2) = v1 .* v + v2 .* (1-v)

function whackyboost(v1,v2,k,score)
    m = mean([score(v1),score(v2)])
    A = rand(0:1,(length(v1),k))
    # select columns of A that give better than mean score
    a = filter(i -> score(combine(A[:,i],v1,v2)) < m,[1:k])
    # take majority vote over all selected columns
    v = float(A[:,a] * ones(length(a)) .> length(a)/2)
    return combine(v,v1,v2)
end
{% endhighlight %}

This generalization applies to essentially any machine learning competition. So let's look into a famous one.

## Breaking the Heritage Health Prize leaderboard

Okay, we're not actually going to do that. First of all, that's not a nice thing to do and against the rules. So, please don't do this on a live competition. Second, the [Heritage Health Prize](http://www.heritagehealthprize.com/c/hhp) competition is long over. We're about two years too late to the party. Third, we don't have the solution file for that competition. Without it there's no sure way of knowing how well this approach would've worked. Nevertheless, we can make some reasonable modeling of what the holdout labels might look like using information that was released by Kaggle and see how well we'd be doing against our random model.

I worked through this fun exercise in a separate Julia notebook. If you're interested in the nitty gritty details I suggest you go [check it out](http://nbviewer.ipython.org/gist/mrtzh/c41fd4c5897fc114a0d6). Here's the picture.

<div style="text-align:center">
<object data="/assets/heritage.svg" type="image/svg+xml">
  <img src="/assets/heritage.png" />
</object>
<p style="text-align:center">We see an improvement from 0.462608 (rank 175) to 0.452039 (rank 6).</p>
</div>

The bottom line is: It seems to work reasonably well (under various semi-principled modeling assumptions I made). From the looks of it this could've given you an improvement *from rank 175ish to 6ish* using at most 700 submissions. Note there was a single team with 671 submissions. There's a pretty good gap between number one on the [public leaderboard](http://www.heritagehealthprize.com/c/hhp/leaderboard/public) and the rest. While possible in principle, it took me a bunch more submissions to get to the top. I should say though that I used the completely generic code from above without any optimizations specific to the competition. I didn't even look at the data points (as I don't have them). It's likely that using the data and domain knowledge could improve things even further. I chose the Heritage Health prize, because it was the highest prized Kaggle competition ever (3 million dollars) and it ran for two years with a substantial number of submissions.

## How robust is your benchmark?

There's a broad lesson to be learned from this example. As computer scientists we love numerical benchmarks and rankings of all sorts. They look so objective and scientific that we easily forget how any benchmark is just a proxy for a more complex question. Every once in a while we should step back and ask: How robust is the benchmark? Do improvements in our benchmark really correspond to progress on the original problem? What I'd love to see in all empirical branches of computer science are adversarial robustness evaluations of various benchmarks. How far can we get by *gaming* rather than by actually making progress towards solving the problem? I have a hunch that not rarely this might lead to interesting new insights into the question.


_Stay tuned and don't miss the next post. Subscribe to the (new) [RSS feed](http://blog.mrtz.org/feed.xml)
or follow me on [Twitter](https://www.twitter.com/mrtz)._
