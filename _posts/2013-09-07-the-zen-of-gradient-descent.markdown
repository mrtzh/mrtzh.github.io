---
layout: post
status: publish
published: true
title: The Zen of Gradient Descent
author: Moritz Hardt
date: '2013-09-07 02:20:19 -0700'
categories:
- simons
- events
- optimization
tags:
- tcs
- gradient descent
- power method
- eigenvalues
- convexity
- polynomials
- chebyshev
comments:
- id: 10
  author: Hello TCS Aggregator! | Moody Rd
  author_email: ''
  author_url: http://mrtz.org/blog/hello-tcs-aggregator/
  date: '2013-09-09 11:45:28 -0700'
  date_gmt: '2013-09-09 18:45:28 -0700'
  content: '[&#8230;] The Zen of Gradient Descent &#8211; Some thoughts on gradient
    descent, how to accelerate it, and its connection to eigenvalue computation. These
    are things I wish I had learned six years. This post is loosely based on a fantastic
    lecture by Ben Recht at the Institute last week. [&#8230;]'
- id: 16
  author: vznvzn
  author_email: vznuri@yahoo.com
  author_url: http://vzn1.wordpress.com
  date: '2013-09-11 11:38:24 -0700'
  date_gmt: '2013-09-11 18:38:24 -0700'
  content: "it would be very cool if the simons institute talks eventually get archived
    somewhere. is there a schedule anywhere? fyi the link you gave for recht's talk
    states \"Password Protected\r\nThis show has been password protected by the host.
    \r\nPlease provide a valid password to access the show.\""
- id: 17
  author: Moritz Hardt
  author_email: m@mrtz.org
  author_url: ''
  date: '2013-09-11 11:45:28 -0700'
  date_gmt: '2013-09-11 18:45:28 -0700'
  content: I updated the links. It should work now.
- id: 69
  author: Indraneel Mukherjee
  author_email: indraneelenator@gmail.com
  author_url: http://www.cs.princeton.edu/~imukherj
  date: '2013-10-22 12:26:59 -0700'
  date_gmt: '2013-10-22 19:26:59 -0700'
  content: "The polynomial interpretation is very cool. The bounds are somewhat different
    if the minimum curvature (small l) is zero. Does a similar \"polynomial approximation\"
    interpretation work in that case?\r\n\r\nAlso the Beck and Taboulleh proof of
    FISTA in the Bubeck link is concise, but the original Nesterov proof has a nice
    geometric interpretation (which is hard to realize from Nesterov's presentation,
    but you might find it easier to read from our recent paper\r\n\r\nhttp://research.google.com/pubs/pub41341.html\r\n\r\n)"
- id: 99
  author: Sanjeev Arora
  author_email: arora@cs.princeton.edu
  author_url: ''
  date: '2013-11-09 19:28:33 -0800'
  date_gmt: '2013-11-10 03:28:33 -0800'
  content: "Nice post and links! I agree about this being a big hole in the standard
    \"grad algorithms\" course. It is arguably a more basic algorithm than many other
    algorithms in the standard canon like flows or matchings. I am remedying that
    at Princeton this year (COS 521). \r\n\r\nMy only beef is with the exclusive focus
    on convex optimization. The math of nonconvex is going to be tricky because the
    problem is NP-hard.  You mention applications to ML and other fields, and typically
    they involve nonconvex optimization. I wonder if theory can say something more
    than just \"Its NP-hard. Don't go there.\""
- id: 141
  author: Power Method still Powerful | Moody Rd
  author_email: ''
  author_url: http://mrtz.org/blog/power-method/
  date: '2013-12-04 08:08:54 -0800'
  date_gmt: '2013-12-04 16:08:54 -0800'
  content: '[&#8230;] algorithms live longer. The Power Method is a great example.
    We saw another good one before. (Hint: Gradient Descent) In this post I&#8217;ll
    describe a very useful robust analysis of the Power Method that is not as [&#8230;]'
- id: 697
  author: Uri
  author_email: urish22@gmail.com
  author_url: ''
  date: '2013-12-18 04:42:49 -0800'
  date_gmt: '2013-12-18 12:42:49 -0800'
  content: "That was a great post! I wasn't aware of the connection between polynomial
    approximation and accelerated GD. \r\n\r\nWhat can be said about the case where
    we don't know the Lipschitz and/or strong convexity constants? They're often data
    dependent and calculating them might be expensive."
- id: 2279
  author: Christos Dimitrakakis
  author_email: christos.dimitrakakis@gmail.com
  author_url: ''
  date: '2014-03-07 03:54:06 -0800'
  date_gmt: '2014-03-07 11:54:06 -0800'
  content: Awesome, even though I had been aware of accelerated GD and  the inverse
    expansion (and used them both in courses recently) I hadn't made the connection.
- id: 2754
  author: denis
  author_email: denis-bz-py@t-online.de
  author_url: ''
  date: '2014-06-29 08:11:51 -0700'
  date_gmt: '2014-06-29 15:11:51 -0700'
  content: "Would you know of any gradient descent steppers that use 2 or more previous
    steps\r\n\r\n    xnew = smoother( x, xprev, \\nabla f, \\nabla f prev ) ?\r\n\r\nwith
    a smoother() that smooths out zigzags in x ... and \\nabla f ... ?\r\nMaybe GD
    / SGD use just one term because they address problems\r\nwith gradients way noisier
    than in standard theories, so no signal-noise model ?"
- id: 2925
  author: Accelerating first-order methods | Sketches, polytopes
  author_email: ''
  author_url: http://umayrh.wordpress.com/2014/07/21/accelerating-first-order-methods/
  date: '2014-07-23 17:33:43 -0700'
  date_gmt: '2014-07-24 00:33:43 -0700'
  content: '[&#8230;] Report, Caltech, 2009 [Bubeck14] S. Bubeck, Theory of Convex
    Optimization for Machine Learning [Hardt13] M. Hardt. The Zen of Gradient Descent.
    Blog, 2013. [Karniadakis00] G. E. Karniadakis. R. M. Kirby. [&#8230;]'
- id: 3146
  author: Kostya Kanishev
  author_email: kkanishev@gmail.com
  author_url: https://plus.google.com/+KostyaKanishev
  date: '2014-08-15 16:50:26 -0700'
  date_gmt: '2014-08-15 23:50:26 -0700'
  content: in the second section you've forgotten 1/2 when writing f(x)... just saying
- id: 3147
  author: Moritz Hardt
  author_email: m@mrtz.org
  author_url: ''
  date: '2014-08-15 17:01:15 -0700'
  date_gmt: '2014-08-16 00:01:15 -0700'
  content: Thanks. Fixed it.
- id: 3159
  author: Robustness versus Acceleration | Moody Rd
  author_email: ''
  author_url: http://mrtz.org/blog/robustness-versus-acceleration/
  date: '2014-08-18 12:32:04 -0700'
  date_gmt: '2014-08-18 19:32:04 -0700'
  content: '[&#8230;] blog post on the Zen of Gradient Descent hit the front page
    of Hacker News the other day. I don&#8217;t know how that happened. It got me
    [&#8230;]'
- id: 3163
  author: Bookmarks for August 18th | Chris&#039;s Digital Detritus
  author_email: ''
  author_url: http://chris.cothrun.com/2014/08/18/bookmarks-for-august-18th-4/
  date: '2014-08-18 18:00:53 -0700'
  date_gmt: '2014-08-19 01:00:53 -0700'
  content: '[&#8230;] The Zen of Gradient Descent | Moody Rd &#8211; [&#8230;]'
- id: 3210
  author: Antony Mampilly
  author_email: ee13m003@ee.iitm.ac.in
  author_url: ''
  date: '2014-08-25 00:02:08 -0700'
  date_gmt: '2014-08-25 07:02:08 -0700'
  content: In the section-"Deriving the Accelerated Method through Chebyshev magic"
    ; x0 should be tb and not b
- id: 3215
  author: Moritz Hardt
  author_email: m@mrtz.org
  author_url: ''
  date: '2014-08-25 08:48:59 -0700'
  date_gmt: '2014-08-25 15:48:59 -0700'
  content: Good catch. Thanks. I fixed it.
- id: 3240
  author: Alexandre Dalyac
  author_email: adalyac@gmail.com
  author_url: https://plus.google.com/+AlexandreDalyac
  date: '2014-08-28 08:06:06 -0700'
  date_gmt: '2014-08-28 15:06:06 -0700'
  content: Yes! Groundbreaking ML at the moment (well - deep learning) is all about
    going there, so why can't we get more theoretical insights into that? Would to
    see some!
- id: 3246
  author: Alexandre Dalyac
  author_email: adalyac@gmail.com
  author_url: https://plus.google.com/+AlexandreDalyac
  date: '2014-08-28 20:53:52 -0700'
  date_gmt: '2014-08-29 03:53:52 -0700'
  content: I was thinking, can we assume that f is a non-convex function, simply say
    "yep, gradient descent is a local optimisation algorithm", and all of the above
    formulations still hold? So we just don't know whether the local minimum we're
    heading towards is an good, but we can leave that problem aside?
- id: 3250
  author: John
  author_email: john.d.schulman@gmail.com
  author_url: ''
  date: '2014-08-29 11:59:17 -0700'
  date_gmt: '2014-08-29 18:59:17 -0700'
  content: "Great article.\r\nI'm wondering why you never mention the conjugate gradient
    algorithm (but you do mention its close relative, Lanczos.)\r\nMost expositions
    of the conjugate gradient algorithm describes the polynomial interpretation and
    uses it for convergence analysis (e.g. Nocedal &amp; Wright's book).\r\nConjugate
    gradient also looks like a heavy ball method since it adds a multiple of the previous
    step.\r\nI didn't that you end up getting Chebyshev polynomials -- neat!"
- id: 3330
  author: Moritz
  author_email: m@mrtz.org
  author_url: http://mrtz.org/blog
  date: '2014-09-02 09:34:14 -0700'
  date_gmt: '2014-09-02 16:34:14 -0700'
  content: Thanks. It was mainly my ignorance. I didn't know much about conjugate
    gradient at the time of writing. I'm aware that the polynomial interpretation
    is standard, especially in the eigenvalue world, but I hadn't seen it in the context
    of Nesterov's method for solving linear equations.
---
<p><span style="line-height: 1.5;">Ben Recht spoke about optimization a few days ago at the Simons Institute. His talk was a highly entertaining tour de force through about a semester of convex optimization. You should go <a href="http://simons.berkeley.edu/talks/ben-recht-2013-09-04">watch </a>it. It's easy to spend a semester of convex optimization on various guises of Gradient Descent alone. Simply pick one of the following variants and work through the specifics of the analysis: conjugate, accelerated, projected, conditional, mirrored, stochastic, coordinate, online. This is to name a few. You may also choose various pairs of attributes such as "accelerated coordinate" descent. Many triples are also valid such as "online stochastic mirror" descent. An expert unlike me would know exactly which triples are admissible. You get extra credit when you use "subgradient" instead of "gradient". This is really only the beginning of Optimization and it might already seem confusing.</span></p>
<p>Thankfully, Ben kept things simple. There are indeed simple common patterns underlying many (if not all) variants of Gradient Descent. Ben did a fantastic job focusing on the basic template without getting bogged down in the details. He also made a high-level point that I strongly agree with. Much research in optimization focuses on convergence rates. That is, how many update steps do we need to minimize the function up to an epsilon error? Often fairly subtle differences in convergence rates are what motivates one particular variant of Gradient Descent over another. But there are properties of the algorithm that can affect the running time more powerfully than the exact convergence rate. A prime example is robustness. Basic Gradient Descent is robust to noise in several important ways. Accelerated Gradient Descent is much more brittle. Showing that it is even polynomial time (and under what assumptions) is a rather non-trivial exercise depending on the machine model. I've been saying for a while now that small improvements in running time don't trump major losses in robustness. The situation in optimization is an important place where the trade-off between robustness and efficiency deserves attention. Generally speaking, the question "which algorithm is better" is rarely answered by looking at a single proxy such as "convergence rate".</p>
<p>With that said, let me discuss Gradient Descent first. Then I will try to motivate why it makes sense to expect an accelerated method and how one might have discovered it. My exposition is not particularly close to Ben's lecture. In particular, mistakes are mine. So, you should still go and watch that lecture. If you already know Gradient Descent, you can skip/skim the first section.</p>
<h2>The Basic Gradient Descent Method</h2>
<p>The goal is to minimize a convex function \(f\colon\mathbb{R}^n\rightarrow\mathbb{R}\) without any constraints. We'll assume that \(f\) is twice differentiable and strongly convex. This means that we can squeeze a parabola between the tangent plane at \(x\) given by the gradient and the function itself. Formally, for some \(\ell&gt;0\) and all \(x,z\in\mathbb{R}^n:\)</p>
<p align="center">\(\displaystyle f(z) \ge f(x) + \nabla f(x)^T(z-x) + \frac \ell 2 \|z-x\|^2.\)</p>
<p>At the same time, we don't want the function to be "too convex". So, we'll require the condition:</p>
<p align="center">\(\displaystyle f(z) \le f(x) + \nabla f(x)^T(z-x) + \frac L 2 \|z-x\|^2.\)</p>
<p>This is a Lipschitz condition in disguise as it is equivalent to: \(\|\nabla f(x) - \nabla f(z)\|\le L\|x-z\|.\)</p>
<p>Let's be a bit more concrete and consider from here on the important example of a convex function \(f(x) = \frac 12 x^T A x - b^T x,\) where \(A\) is an \(n\times n\) positive definite matrix and \(b\) is a vector. We have \(\nabla f(x) = Ax - b.\) It's an exercise to check that the above conditions boil down to the spectral condition: \(\ell I \preceq A \preceq LI.\) Clearly this problem has a unique minimizer given by \(x^*=A^{-1}b.\) In other words, if we can minimize this function, we'll know how to solve linear systems.</p>
<p>Now, all that Gradient Descent does is to compute the sequence of points</p>
<p align="center">\(\displaystyle x_{k+1} = x_k - t_k \nabla f(x_k)\)</p>
<p>for some choice of the step parameter \(t_k.\) Our hope is that for some positive \(\alpha &lt; 1\),</p>
<p align="center">\(\displaystyle \|x^* - x_{k+1}\| \le \alpha\|x_k-x^*\|,\)</p>
<p>If this happens in every step, Gradient Descent converges exponentially fast towards the optimum. This is soberly called linear convergence in Optimization. Note that since the function is strongly convex, this also guarantees convergence of the objective value.</p>
<p>Choosing the right step size \(t\) is an important task. If we choose it to small, our progress will be unnecessarily slow. If we choose it too large, we will overshoot. A calculation shows that if we put \(t= 2/(\ell + L)\) we get \(\alpha = (L-\ell)/(L+\ell).\) Remember that \(\kappa = L/\ell\) is condition number of the matrix. More generally, you could define the condition number of \(f\) in this way. We have shown that</p>
<p align="center">\(\displaystyle \|x_k-x^*\| \le \left(\frac{\kappa -1}{\kappa + 1}\right)^k\|x_0-x^*\|.\)</p>
<p>So the potential function (or Lyapunov function) drops by a factor of roughly \(1-1/\kappa\) in every step. This is the convergence rate of Gradient Descent.</p>
<h2>Deriving the Accelerated Method through Chebyshev magic</h2>
<p>What Nesterov showed in 1983 is that we can improve the convergence rate of Gradient Descent without using anything more than gradient information at various points of the domain. This is usually when people say something confusing about physics. It's probably helpful to others, but physics metaphors are not my thing. Let me try a different approach. Let's think about why what we were doing above wasn't optimal. Consider the simple example \(f(x)= \frac12 x^T A x- b^T x.\) Recall, the function is minimized at \(A^{-1}b\) and the gradient satisfies \(\nabla f(x) = Ax-b.\) Let's start Gradient Descent at \(x_0=tb.\) We can then check that</p>
<p align="center">\(\displaystyle x_k = (\sum_{j=0}^k (I-A')^k)b'\)</p>
<p>where \(A'=tA\) and \(b'=tb.\) Why does this converge to \(A^{-1}b\)? The reason is that what Gradient Descent is computing is a degree \(k\) polynomial approximation of the inverse function. To see this, recall that for all scalars \(|x|&lt;1,\)</p>
<p align="center">\(\displaystyle \frac{1}{x} = \sum_{k=0}^\infty (1-x)^k.\)</p>
<p>Since the eigenvalues of \(A'\) lie within \((0,1),\) this scalar function extends to the matrix case. Moreover, the approximation error when truncating the series at degree \(k\) is \(O( (1-x)^k)).\) In the matrix case this translates to error \(O(\| (I-A')^k \|) = O( (1-\ell/L)^k).\) This is exactly the convergence rate of Gradient Descent that we determined earlier.</p>
<p>Why did we go through this exercise? The reason is that now we see that to improve on Gradient Descent it suffices to find a better low-degree approximation to the scalar function \(1/x.\) What we'll be able to show is that we can save a square root in the degree while achieving the same error! Anybody familiar with polynomial approximation should have one guess when hearing "quadratic savings in the degree":</p>
<h3 style="text-align: center;">Chebyshev Polynomials</h3>
<p>Let's be clear. Our goal is to find a degree \(k\) polynomial \(q_k(A)\) which minimizes the residual</p>
<p align="center">\(\displaystyle r_k = \|(I-Aq_k(A))b\|.\)</p>
<p>Put differently we are looking for a polynomial of the form \(p_k(z)=1-zq(z).\) What we want is that the polynomial is as small as possible on the location of the eigenvalues of \(A\) which lie in the interval \([\ell,L].\) At the same time, the polynomial must satisfy \(p_k(0)=1.\) This is exactly the property that Chebyshev polynomials achieve with the least possible degree! Quantitatively, we have the following lemma that I learned from Rocco Servedio. As Rocco said in that context:</p>
<blockquote><p>There's only one bullet in the gun. It's called the Chebyshev polynomial.</p></blockquote>
<p><strong>Lemma.</strong> There is a polynomial \(p_k\) of degree \(O(\sqrt{(L/\ell)\log(1/\epsilon)})\) such that \(p_k(0)=1\) and \(p_k(x)\le\epsilon\) for all \(x\in[\ell,L].\)</p>
<p>The lemma implies that we get a quadratic savings in degree. Since we can build \(p_k\) from gradient information alone, we now know how to improve the convergence rate of Gradient Descent. It gets better. The Chebyshev polynomials satisfy a simple recursive definition that defines the \(k\)-th degree polynomial in terms of the previous two polynomials. This means that accelerated gradient descent only needs the previous two gradients with suitable coefficients:</p>
<p align="center">\(\displaystyle x_k = x_{k-1} - \alpha_k \nabla f(x_{k-1}) + \beta_k \nabla f(x_{k-2}).\)</p>
<p>Figuring out the best possible coefficients \(\alpha_k,\beta_k\) leads to the above convergence rate. What's amazing is that this trick works for any convex function satisfying our assumptions and not just the special case we dealt with here!  In fact, this is what Nesterov showed. I should say that the interpretation in terms of polynomial approximations is lost (as far as I know).The polynomial approximation method I described was known much earlier in the context of eigenvalue computations. This is another fascinating connection I'll describe in the next section.</p>
<p>Let me add that it can be shown that this convergence rate is optimal for any first-order (gradient only method) by taking \(A\) to be the Laplacian of a path of length \(n\). This is true even in our special case. It's optimal though in a weak sense: There is a function and a starting point such that the method needs this many steps. I would be interesting to understand how robust this lower bound is.</p>
<h2>The Connection to Eigenvalue Methods</h2>
<p>Our discussion above was essentially about eigenvalue location. What does polynomial approximation have to do with eigenvalues? Recall, that the most basic way of computing the top eigenvalue of a matrix is the Power Method. The Power Method corresponds to a very basic polynomial, namely \(p_k(x) = x^k.\) This polynomial has the effect that it maps \(1\) to \(1\) and moves every number \(|x|&lt;1\) closer to \(0\) at the rate \(|x|^k.\) Hence, if the top eigenvalue is \(\lambda\) and the second eigenvalue is \((1-\epsilon)\lambda,\) then we need about \(k\approx 1/\epsilon\) iterations to  approximately find \(\lambda.\) Using exactly the same Chebyshev idea, we can improve this to \(k=O(\sqrt{1/\epsilon})\) iterations! This method is often called Lanczos method. So, we have the precise correspondence:</p>
<blockquote><p>The Power Method is to Lanczos as Basic Gradient Descent is to Accelerated Gradient Descent!</p></blockquote>
<p>I find this quite amazing. In a future post I will return to the Power Method in greater detail in the context of noise-tolerant eigenvalue computation.</p>
<h2>Why don't we teach Gradient Descent in theory classes?</h2>
<p>I'm embarrassed to admit that the first time I saw Gradient Descent in full generality was in grad school. I had seen the Perceptron algorithm in my last year as an undergraduate. At the time, I was unaware that like so many algorithms it is just a special case of Gradient Descent. Looking at the typical undergraduate curriculum, it seems like we spend a whole lot of time iterating through dozens of combinatorial algorithms for various problems. So much so that we often don't get around to teaching something as fundamental as Gradient Descent. It wouldn't take more than two lectures to teach the contents of this blog post (or one lecture if you're Ben Recht). Knowing Gradient Descent seems quite powerful. It's not only simple and elegant. It's also the algorithmic paradigm behind many algorithms in machine learning, optimization and numerical computation. Teaching it to undergraduates seems like a must. I just now realize that I haven't been an undergraduate in a while. Time flies. So perhaps this is already happening.</p>
<h2>More Pointers</h2>
<ul>
<li>Trefethen-Bau, "Numerical Linear Algebra". My favorite book on the topic of classical numerical methods by far.</li>
<li>Ben Recht's lecture notes <a href="http://pages.cs.wisc.edu/~brecht/cs726docs/HeavyBall.pdf">here</a> and <a href="http://pages.cs.wisc.edu/~brecht/cs726docs/HeavyBallLinear.pdf">here</a>, his Simons <a href="http://simons.berkeley.edu/talks/ben-recht-2013-09-04">talk.</a></li>
<li>Sebastien Bubeck's <a href="http://blogs.princeton.edu/imabandit/2013/04/01/acceleratedgradientdescent/">course notes</a> are great!</li>
<li>For lack of a better reference, the lemma I stated above appears as Claim 5.4 in <a href="http://arxiv.org/pdf/1107.2444v1.pdf">this paper</a> that I may have co-authored.</li>
</ul>
<p style="text-align: center;"><em>To stay on top of future posts, subscribe to the <a style="color: #bc360a;" href="http://mrtz.org/blog/feed/">RSS feed</a> or follow me on <a style="color: #bc360a;" href="http://twitter.com/mrtz">Twitter</a>.</em></p>
