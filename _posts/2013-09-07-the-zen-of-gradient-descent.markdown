---
layout: post
status: publish
published: true
title: The Zen of Gradient Descent
author: Moritz Hardt
date: '2013-09-07 02:20:19 -0700'
comments: true
tags:
- tcs
- gradient descent
- power method
- eigenvalues
- convexity
- polynomials
- chebyshev
---

Ben Recht spoke about optimization a few days ago at the Simons Institute. His
talk was a highly entertaining tour de force through about a semester of convex
optimization. You should go
[watch](http://simons.berkeley.edu/talks/ben-recht-2013-09-04) it. It's easy to
spend a semester of convex optimization on various guises of Gradient Descent
alone. Simply pick one of the following variants and work through the specifics
of the analysis: conjugate, accelerated, projected, conditional, mirrored,
stochastic, coordinate, online. This is to name a few. You may also choose
various pairs of attributes such as "accelerated coordinate" descent. Many
triples are also valid such as "online stochastic mirror" descent. An expert
unlike me would know exactly which triples are admissible. You get extra credit
when you use "subgradient" instead of "gradient". This is really only the
beginning of optimization and it might already seem confusing.

Thankfully, Ben kept things simple. There are indeed simple common patterns underlying many (if not all) variants of Gradient Descent. Ben did a fantastic job focusing on the basic template without getting bogged down in the details. He also made a high-level point that I strongly agree with. Much research in optimization focuses on convergence rates. That is, how many update steps do we need to minimize the function up to an epsilon error? Often fairly subtle differences in convergence rates are what motivates one particular variant of Gradient Descent over another. But there are properties of the algorithm that can affect the running time more powerfully than the exact convergence rate. A prime example is robustness. Basic Gradient Descent is robust to noise in several important ways. Accelerated Gradient Descent is much more brittle. Showing that it is even polynomial time (and under what assumptions) is a rather non-trivial exercise depending on the machine model. I've been saying for a while now that small improvements in running time don't trump major losses in robustness. The situation in optimization is an important place where the trade-off between robustness and efficiency deserves attention. Generally speaking, the question "which algorithm is better" is rarely answered by looking at a single proxy such as "convergence rate".

With that said, let me discuss Gradient Descent first. Then I will try to motivate why it makes sense to expect an accelerated method and how one might have discovered it. My exposition is not particularly close to Ben's lecture. In particular, mistakes are mine. So, you should still go and watch that lecture. If you already know Gradient Descent, you can skip/skim the first section.


## The Basic Gradient Descent Method

<p>The goal is to minimize a convex function \(f\colon\mathbb{R}^n\rightarrow\mathbb{R}\) without any constraints. We'll assume that \(f\) is twice differentiable and strongly convex. This means that we can squeeze a parabola between the tangent plane at \(x\) given by the gradient and the function itself. Formally, for some \(\ell&gt;0\) and all \(x,z\in\mathbb{R}^n:\)</p>

\\[ f(z) \\ge f(x) + \\nabla f(x)^T(z-x) + \\frac \\ell 2 \\|z-x\\|^2.\\]

At the same time, we don't want the function to be "too convex". So, we'll
require the condition, often called *smoothness*:

\\[ f(z) \\le f(x) + \\nabla f(x)^T(z-x) + \\frac L 2 \\|z-x\\|^2.\\]

This is a Lipschitz condition on the gradient map in disguise as it is equivalent to: 

\\[\\|\\nabla f(x) - \\nabla f(z)\\|\\le L\\|x-z\\|.\\]

<p>Let's be a bit more concrete and consider from here on the important example of a convex function \(f(x) = \frac 12 x^T A x - b^T x,\) where \(A\) is an \(n\times n\) positive definite matrix and \(b\) is a vector. We have \(\nabla f(x) = Ax - b.\) It's an exercise to check that the above conditions boil down to the spectral condition: \(\ell I \preceq A \preceq LI.\) Clearly this problem has a unique minimizer given by \(x^*=A^{-1}b.\) In other words, if we can minimize this function, we'll know how to solve linear systems.</p>
<p>Now, all that Gradient Descent does is to compute the sequence of points</p>

\\[x_{k+1} = x_k - t_k \\nabla f(x_k)\\]

for some choice of the step parameter \\(t_k.\\) 
Our hope is that for some positive \\(\\alpha < 1\\),

\\[\\|x^* - x_{k+1}\\| \\le \\alpha\\|x_k-x^*\\|,\\]

<p>If this happens in every step, Gradient Descent converges exponentially fast
towards the optimum. This is soberly called linear convergence in optimization.
Since the function is smooth, this also guarantees convergence in objective value.</p>

<p>Choosing the right step size \(t\) is an important task. If we choose it to small, our progress will be unnecessarily slow. If we choose it too large, we will overshoot. A calculation shows that if we put \(t= 2/(\ell + L)\) we get \(\alpha = (L-\ell)/(L+\ell).\) Remember that \(\kappa = L/\ell\) is condition number of the matrix. More generally, you could define the condition number of \(f\) in this way. 
We have shown that</p>

\\[\\|x_k-x^\*\\| \\le \\left(\\frac{\\kappa -1}{\\kappa + 1}\\right)^k\\|x_0-x^\*\\|.\\]

<p>So the potential function (or Lyapunov function) drops by a factor of roughly \(1-1/\kappa\) in every step. This is the convergence rate of Gradient Descent.</p>

## Deriving the Accelerated Method through Chebyshev magic

<p>What Nesterov showed in 1983 is that we can improve the convergence rate of Gradient Descent without using anything more than gradient information at various points of the domain. This is usually when people say something confusing about physics. It's probably helpful to others, but physics metaphors are not my thing. Let me try a different approach. Let's think about why what we were doing above wasn't optimal. Consider the simple example \(f(x)= \frac12 x^T A x- b^T x.\) Recall, the function is minimized at \(A^{-1}b\) and the gradient satisfies \(\nabla f(x) = Ax-b.\) Let's start Gradient Descent at \(x_0=tb.\) We can then check that</p>

\\[x_k = \\Big(\sum_{j=0}^k (I-A')^k\\Big)b'\\]

<p>where \(A'=tA\) and \(b'=tb.\) Why does this converge to \(A^{-1}b\)? The reason is that what Gradient Descent is computing is a degree \(k\) polynomial approximation of the inverse function. To see this, recall that for all scalars \(|x|&lt;1,\)</p>

\\[\\frac{1}{x} = \sum_{k=0}^\infty (1-x)^k.\\]

<p>Since the eigenvalues of \(A'\) lie within \((0,1),\) this scalar function extends to the matrix case. Moreover, the approximation error when truncating the series at degree \(k\) is \(O( (1-x)^k)).\) In the matrix case this translates to error \(O(\| (I-A')^k \|) = O( (1-\ell/L)^k).\) This is exactly the convergence rate of Gradient Descent that we determined earlier.</p>
<p>Why did we go through this exercise? The reason is that now we see that to improve on Gradient Descent it suffices to find a better low-degree approximation to the scalar function \(1/x.\) What we'll be able to show is that we can save a square root in the degree while achieving the same error! Anybody familiar with polynomial approximation should have one guess when hearing "quadratic savings in the degree":</p>
<h3 style="text-align: center;">Chebyshev Polynomials</h3>
<p>Let's be clear. Our goal is to find a degree \(k\) polynomial \(q_k(A)\) which minimizes the residual</p>

\\[r_k = \\|(I-Aq_k(A))b\\|.\\]

<p>Put differently we are looking for a polynomial of the form \(p_k(z)=1-zq(z).\) What we want is that the polynomial is as small as possible on the location of the eigenvalues of \(A\) which lie in the interval \([\ell,L].\) At the same time, the polynomial must satisfy \(p_k(0)=1.\) This is exactly the property that Chebyshev polynomials achieve with the least possible degree! Quantitatively, we have the following lemma that I learned from Rocco Servedio. As Rocco said in that context:</p>
<blockquote><p>There's only one bullet in the gun. It's called the Chebyshev polynomial.</p></blockquote>
<p><strong>Lemma.</strong> There is a polynomial \(p_k\) of degree \(O(\sqrt{(L/\ell)\log(1/\epsilon)})\) such that \(p_k(0)=1\) and \(p_k(x)\le\epsilon\) for all \(x\in[\ell,L].\)</p>
<p>The lemma implies that we get a quadratic savings in degree. Since we can build \(p_k\) from gradient information alone, we now know how to improve the convergence rate of Gradient Descent. It gets better. The Chebyshev polynomials satisfy a simple recursive definition that defines the \(k\)-th degree polynomial in terms of the previous two polynomials. This means that accelerated gradient descent only needs the previous two gradients with suitable coefficients:</p>

\\[x_k = x\_{k-1} - \\alpha_k \\nabla f(x\_{k-1}) + \\beta_k \\nabla f(x\_{k-2}).\\]

<p>Figuring out the best possible coefficients \(\alpha_k,\beta_k\) leads to the above convergence rate. What's amazing is that this trick works for any convex function satisfying our assumptions and not just the special case we dealt with here!  In fact, this is what Nesterov showed. I should say that the interpretation in terms of polynomial approximations is lost (as far as I know).The polynomial approximation method I described was known much earlier in the context of eigenvalue computations. This is another fascinating connection I'll describe in the next section.</p>
<p>Let me add that it can be shown that this convergence rate is optimal for any first-order (gradient only method) by taking \(A\) to be the Laplacian of a path of length \(n\). This is true even in our special case. It's optimal though in a weak sense: There is a function and a starting point such that the method needs this many steps. I would be interesting to understand how robust this lower bound is.</p>
<h2>The Connection to Eigenvalue Methods</h2>
<p>Our discussion above was essentially about eigenvalue location. What does polynomial approximation have to do with eigenvalues? Recall, that the most basic way of computing the top eigenvalue of a matrix is the Power Method. The Power Method corresponds to a very basic polynomial, namely \(p_k(x) = x^k.\) This polynomial has the effect that it maps \(1\) to \(1\) and moves every number \(|x|&lt;1\) closer to \(0\) at the rate \(|x|^k.\) Hence, if the top eigenvalue is \(\lambda\) and the second eigenvalue is \((1-\epsilon)\lambda,\) then we need about \(k\approx 1/\epsilon\) iterations to  approximately find \(\lambda.\) Using exactly the same Chebyshev idea, we can improve this to \(k=O(\sqrt{1/\epsilon})\) iterations! This method is often called Lanczos method. So, we have the precise correspondence:</p>
<blockquote><p>The Power Method is to Lanczos as Basic Gradient Descent is to Accelerated Gradient Descent!</p></blockquote>
<p>I find this quite amazing. In a future post I will return to the Power Method in greater detail in the context of noise-tolerant eigenvalue computation.</p>

## Why don't we teach Gradient Descent in theory classes?

I'm embarrassed to admit that the first time I saw Gradient Descent in full generality was in grad school. I had seen the Perceptron algorithm in my last year as an undergraduate. At the time, I was unaware that like so many algorithms it is just a special case of Gradient Descent. Looking at the typical undergraduate curriculum, it seems like we spend a whole lot of time iterating through dozens of combinatorial algorithms for various problems. So much so that we often don't get around to teaching something as fundamental as Gradient Descent. It wouldn't take more than two lectures to teach the contents of this blog post (or one lecture if you're Ben Recht). Knowing Gradient Descent seems quite powerful. It's not only simple and elegant. It's also the algorithmic paradigm behind many algorithms in machine learning, optimization and numerical computation. Teaching it to undergraduates seems like a must. I just now realize that I haven't been an undergraduate in a while. Time flies. So perhaps this is already happening.


## More Pointers

*   Trefethen-Bau, "Numerical Linear Algebra". My favorite book on the topic of classical numerical methods by far.
*   Ben Recht's lecture notes [here](http://pages.cs.wisc.edu/~brecht/cs726docs/HeavyBall.pdf) and [here](http://pages.cs.wisc.edu/~brecht/cs726docs/HeavyBallLinear.pdf), his Simons [talk.](http://simons.berkeley.edu/talks/ben-recht-2013-09-04)
*   Sebastien Bubeck's [course notes](http://blogs.princeton.edu/imabandit/2013/04/01/acceleratedgradientdescent/) are great!
*   For lack of a better reference, the lemma I stated above appears as Claim 5.4 in [this paper](http://arxiv.org/pdf/1107.2444v1.pdf) that I may have co-authored.

_To stay on top of future posts, subscribe to the 
[RSS feed](http://blog.mrtz.org/feed.xml) or follow me on [Twitter](http://twitter.com/mrtz)._
