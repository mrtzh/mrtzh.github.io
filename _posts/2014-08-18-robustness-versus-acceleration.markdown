---
layout: post
status: publish
published: true
title: Robustness versus Acceleration
author: Moritz Hardt
date: '2014-08-18 12:31:57 -0700'
categories:
- optimization
tags:
- algorithms
- tcs
- complexity
- theory
- gradient descent
- convexity
- optimization
- robustness
comments:
- id: 3181
  author: u
  author_email: urish22@gmail.com
  author_url: http://gravatar.com/u
  date: '2014-08-20 04:25:18 -0700'
  date_gmt: '2014-08-20 11:25:18 -0700'
  content: "Hi Moritz, great post as usual, this is a very interesting result I was
    not aware of. And knowing this will have practical implications for my work.\r\n\r\nHave
    you seen the recent paper by Allen-Zhu &amp; Orecchia where they derive AGD as
    a Combination of Gradient and Mirror Descent? Seems this could be a relevant POV
    for this discussion."
- id: 3184
  author: Moritz Hardt
  author_email: m@mrtz.org
  author_url: ''
  date: '2014-08-20 07:58:26 -0700'
  date_gmt: '2014-08-20 14:58:26 -0700'
  content: Thanks! I have seen that paper on arxiv and it's definitely been on my
    reading list for some time now. Perhaps once I read it and on the off chance I
    happen to understand it properly, I'll blog about it.
- id: 6025
  author: Yuan Gao
  author_email: tjcharlesgao@gmail.com
  author_url: https://plus.google.com/102599756496880487918
  date: '2014-12-29 23:10:14 -0800'
  date_gmt: '2014-12-30 07:10:14 -0800'
  content: '"Let’s recall what an exact first-order oracle does for an (unconstrained)
    convex function f with Lipschitz constant L." Do you mean that the derivative
    of f has Lipschitz constant L?'
- id: 6030
  author: Moritz Hardt
  author_email: m@mrtz.org
  author_url: ''
  date: '2014-12-30 07:40:08 -0800'
  date_gmt: '2014-12-30 15:40:08 -0800'
  content: Yes, you are correct. What I meant was "smooth" and not "Lipschitz". Equivalently,
    as you say, the gradient of f is Lipschitz. To avoid confusion with the word Lipschitz,
    I've now changed it to "smooth" everywhere. Thanks for pointing this out.
- id: 6227
  author: Ravi Ganti
  author_email: gmravi2003@gmail.com
  author_url: ''
  date: '2015-01-12 15:47:14 -0800'
  date_gmt: '2015-01-12 23:47:14 -0800'
  content: Neat post, Moritz. Can you maybe elaborate a bit on the second open problem
    that you stated?
- id: 6245
  author: Moritz Hardt
  author_email: m@mrtz.org
  author_url: ''
  date: '2015-01-13 09:40:40 -0800'
  date_gmt: '2015-01-13 17:40:40 -0800'
  content: Thanks. You might want to check out my post on gradient descent for background.
    The idea is that there are eigenvalue methods that converge faster than the power
    method (e.g., Lanczos), but they have similar issues with noise tolerance as Nesterov's
    method. So, what I'm asking is a result which shows that provably any improvement
    over the power method in terms of convergence speed comes at the cost of noise
    tolerance.
---
<p>My blog post on the <a href="http://mrtz.org/blog/the-zen-of-gradient-descent/">Zen of Gradient Descent</a> hit the front page of <a href="https://news.ycombinator.com/item?id=8182991">Hacker News</a> the other day. I don't know how that happened. It got me more views in one day than this most humble blog usually gets in half a year. I thought I should take this as an excuse to extend the post a bit by elaborating on one remark I made only in passing. You don't need to go back to reading that post unless you want to. This one will be self contained.</p>
<p>The point I made is that basic Gradient Descent (GD) is noise tolerant in a way that Accelerated Gradient Descent (AGD) is not. That is to say, if we don't have exact but rather approximate gradient information, GD might very well outperform AGD even though its convergence rate is worse in the exact setting. The truth is I was sort of bluffing. I didn't actually have a proof of a formal statement that would nail down this point in a compelling way. It was more of a gut feeling based on some simple observations.</p>
<p>To break the suspense, I still haven't proved the statement I vaguely thought was true back then, but fortunately somebody else had already done that. This is a thought provoking <a href="http://www.optimization-online.org/DB_FILE/2010/12/2865.pdf">paper by Devolder, Glineur and Nesterov </a>(DGN). Thanks to Cristobal Guzman for pointing me to this paper. Roughly, what they show is that any method that converges faster than the basic gradient descent method must accumulate errors linearly with the number of iterations. Hence, in various noisy settings auch as are common in applications acceleration may not help---in fact, it can actually make things worse!</p>
<p>I'll make this statement more formal below, but let me first explain why I love this result. There is a tendency in algorithm design to optimize computational efficiency first, second and third and then maybe think about some other stuff as sort of an add-on constraint. We generally tend to equate faster with better. The reason why this is not a great methodology is that sometimes acceleration is mutually exclusive with other fundamental design goals. A theory that focuses primarily on speedups without discussing trade-offs with robustness misses a pretty important point.</p>
<h2>When acceleration is good</h2>
<p>Let's build some intuition for the result I mentioned before we go into formal details. Consider my favorite example of minimizing a smooth convex function \({f\colon \mathbb{R}^n\rightarrow\mathbb{R}}\) defined as</p>
<p style="text-align: center;">\(\displaystyle f(x) = \frac 12 x^T L x - b^T x \)</p>
<p>for some positive semidefinite \({n\times n}\) matrix \({L}\) and a vector \({b\in\mathbb{R}^n.}\) Recall that the gradient is \({\nabla f(x)=Lx-b.}\) An illustrative example is the <a href="http://en.wikipedia.org/wiki/Laplacian_matrix">Laplacian </a> of a <a href="http://en.wikipedia.org/wiki/Cycle_graph">cycle graph</a>:</p>
<p style="text-align: center;">\(\displaystyle L = \left[ \begin{array}{ccccccc} 2 &amp; -1 &amp; 0 &amp; 0 &amp; 0 &amp; \cdots &amp; -1 \\ -1 &amp; 2 &amp; -1 &amp; 0 &amp; 0 &amp; \cdots &amp; 0 \\ 0 &amp; -1 &amp; 2 &amp; -1&amp; 0 &amp; \cdots &amp; 0 \\ \vdots &amp; &amp; &amp; &amp; &amp; &amp; \end{array} \right] \)</p>
<p>Since \({L}\) is positive semidefinite like any graph Laplacian, the function \({f}\) is convex. The operator norm of \({L}\) is bounded by~\({4}\) and so we have that for all \({x,y\in\mathbb{R}^n:}\)</p>
<p style="text-align: center;">\(\displaystyle \|\nabla f(x) -\nabla f(y)\| \le \|L\|\cdot\|x-y\|\le 4 \|x-y\|. \)</p>
<p>This means the function is also smooth and we can apply AGD/GD with a suitable step size. Comparing AGD and GD on this instance with \({n=100}\), we get the following picture:</p>
<p><a href="http://mrtz.org/blog/wp-content/uploads/2014/08/no-noise.png"><img class="aligncenter size-large wp-image-376" src="http://mrtz.org/blog/wp-content/uploads/2014/08/no-noise-1024x640.png" alt="no-noise" width="850" height="531" /></a></p>
<p>It looks like AGD is the clear winner. GD is pretty slow and takes a few thousand iterations to decrease the error by an order of magnitude.</p>
<h2>When acceleration is bad</h2>
<p>The situation changes dramatically in the presence of noise. Let's repeat the exact same experiment but now instead of observing \({\nabla f(x)}\) for any given \({x,}\) we can only see \({\nabla f(x) + \xi}\) where \({\xi}\) is sampled from the \({n}\)-dimensional normal distribution \({N(0,\sigma^2)^n.}\) Choosing \({\sigma=0.1}\) we get the following picture:</p>
<p><a href="http://mrtz.org/blog/wp-content/uploads/2014/08/with-noise.png"><img class="aligncenter size-large wp-image-377" src="http://mrtz.org/blog/wp-content/uploads/2014/08/with-noise-1024x640.png" alt="with-noise" width="850" height="531" /></a></p>
<p>Gradient descent pretty quickly converges to essentially the best result that we can hope for given the noisy gradients. In contrast, AGD goes totally nuts. It doesn't converge at all and it adds up errors in sort of linear fashion. In this world, GD is the clear winner.</p>
<h2>A precise trade-off</h2>
<p>The first thing DGN do in their paper is to define a general notion of inexact first order oracle. Let's recall what an exact first-order oracle does for an (unconstrained) convex function \({f\colon\mathbb{R}^n\rightarrow \mathbb{R}}\) with smoothness parameter \({L.}\) Given any point \({x\in\mathbb{R}^n}\) an exact first order oracle returns a pair \({(f_L(x),g_L(x))\in\mathbb{R}\times\mathbb{R}^n}\) so that for all \({y\in\mathbb{R}^n}\) we have</p>
<p style="text-align: center;">\(\displaystyle 0\le f(y) - \big(f_L(x) + \langle g_L(x),y-x\rangle\big)\le \frac L2\|y-x\|^2\,. \)</p>
<p>Pictorially, at every point \({x}\) the function can be sandwiched between a tangent linear function specified by \({(f_L(x),g_L(x))}\) and a parabola. The pair \({(f(x),\nabla f(x))}\) satisfies this constraint as the first inequality follows from convexity and the second from the smoothness condition. In fact, this pair is the only pair that satisfies these conditions. My slightly cumbersome way of desribing a first-order oracle was only so that we may now easily generalize it to an inexact first-order oracle. Specifically, an inexact oracle returns for any given point \({x\in\mathbb{R}^n}\) a pair \({(f_{\delta,L}(x),g_{\delta,L}(x))\in\mathbb{R}\times\mathbb{R}^n}\) so that for all \({y\in\mathbb{R}^n}\) we have</p>
<p style="text-align: center;">\(\displaystyle 0\le f(y) - \big(f_{\delta,L}(x) + \langle g_{\delta,L}(x),y-x\rangle\big)\le \frac L2\|y-x\|^2+\delta\,. \)</p>
<p>It's the same picture as before except now there's some \({\delta}\) slack between the linear approximation and the parabola.<br />
With this notion at hand, what DGN show is that given access to \({\delta}\)-inexact first-order oracle Gradient Descent spits out a point \({x^t}\) after \({t}\) steps so that</p>
<p style="text-align: center;">\(\displaystyle f(x^t) - \min_x f(x) \le O\big(L/t\big) + \delta\,. \)</p>
<p>The big-oh notation is hiding the squared distance between the optimum and the starting point. Accelerated Gradient Descent on the other hand gives you</p>
<p style="text-align: center;">\(\displaystyle f(x^t) - \min_x f(x) \le O\big(L/t^2\big) + O\big(t \delta\big)\,. \)</p>
<p>Moreover, you cannot improve this-tradeoff between acceleration and error accumulation. That is any method that converges as \({1/t^2}\) must accumulate errors as \({t\delta.}\)</p>
<h2>Open questions</h2>
<ol>
<li>The lower bound I just mentioned in the previous paragraph stems from the fact that an inexact first-order oracle can embed non-smooth optimization problems for which a speedup is not possible. This is interesting, but it doesn't resolve, for example, the question of whether there could be a speedup in the simple gaussian noise addition model that I mentioned above. This isn't even a toy model---as you might object---since gaussian noise addition is what you would do to make gradient descent privacy preserving. See for example an upcoming FOCS <a href="http://arxiv.org/pdf/1405.7085.pdf">paper by Bassily, Smith, Thakurta</a> for an analysis of gradient descent with gaussian noise.</li>
<li>Is there an analog of the DGN result in the eigenvalue world? More formally, can we show that any Krylov subspace method that converges asymptotically faster than the <a href="http://mrtz.org/blog/power-method/">power method</a> must accumulate errors?</li>
<li>The cycle example above is often used to show that any blackbox gradient method requires at least \({t\ge \Omega(1/\sqrt{\epsilon})}\) steps to converge to error \({\epsilon}\) provided that \({t}\) is less than the number of vertices of the cycle, that is the dimension \({n}\) of the domain. (See, for example, Theorem 3.9. in Sebastien Bubeck's <a href="http://arxiv.org/pdf/1405.4980v1.pdf">book</a>.) Are there any lower bounds that hold for \({t\gg n}\)?</li>
</ol>
<h2>Pointers:</h2>
<p>The code for these examples is available <a href="http://nbviewer.ipython.org/gist/mrtzh/4dc77fb84c3ba8b8b220">here</a>.</p>
<p style="text-align: center;"><em>To stay on top of future posts, subscribe to the <a style="color: #bc360a;" href="http://mrtz.org/blog/feed/">RSS feed</a> or follow me on <a style="color: #bc360a;" href="http://twitter.com/mrtz">Twitter</a>.</em></p>
