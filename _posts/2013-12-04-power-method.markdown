---
layout: post
status: publish
published: true
title: 'Power Method still Powerful '
author: Moritz Hardt
date: '2013-12-04 08:20:16 -0800'
categories:
- optimization
- learning
tags:
- algorithms
- tcs
- theory
- power method
- eigenvalues
- matrix completion
- robustness
comments:
- id: 149
  author: Andy D
  author_email: andy.drucker@gmail.com
  author_url: ''
  date: '2013-12-04 11:58:19 -0800'
  date_gmt: '2013-12-04 19:58:19 -0800'
  content: "Nice post!   \r\n\r\nOne of the disappointing things about math/TCS is
    that most of our \"celebrated\" results have in fact never had a party thrown
    in their honor.  Glad you are trying to change that."
- id: 155
  author: Moritz Hardt
  author_email: m@mrtz.org
  author_url: ''
  date: '2013-12-04 13:20:29 -0800'
  date_gmt: '2013-12-04 21:20:29 -0800'
  content: That's right. What do we even mean by "celebrated result" when nobody's
    actually celebrating?
- id: 206
  author: CS
  author_email: Global@hotmail.com
  author_url: ''
  date: '2013-12-05 01:20:35 -0800'
  date_gmt: '2013-12-05 09:20:35 -0800'
  content: "Very interesting post. \r\nBut could you explain what is Forbenius norm?"
- id: 233
  author: Moritz Hardt
  author_email: m@mrtz.org
  author_url: ''
  date: '2013-12-05 07:32:41 -0800'
  date_gmt: '2013-12-05 15:32:41 -0800'
  content: Sure. I added a sentence. Frobenius squared norm of a matrix A is the sum
    of squared entries of A.
- id: 631
  author: Rebekah
  author_email: bex25ni@hotmail.co.uk
  author_url: ''
  date: '2013-12-16 01:15:09 -0800'
  date_gmt: '2013-12-16 09:15:09 -0800'
  content: "Hello,\r\nI'm writing a report on the power method and I have been trying
    to get information on who discovered it and when, Wikipedia mentions Von Mises
    but I have seen other names mention elsewhere, I can't seem to get a definite
    answer anywhere. Would you be able to help me?"
- id: 640
  author: Moritz Hardt
  author_email: m@mrtz.org
  author_url: ''
  date: '2013-12-16 07:49:40 -0800'
  date_gmt: '2013-12-16 15:49:40 -0800'
  content: I'm not exactly sure. I mainly relied on the Wiki page myself. Von Mises
    original paper talks about solving equation. So possibly there are later references
    that first used the power method specifically to find eigenvalues. Let me know
    if you find out more :-)
- id: 2755
  author: Jan Peter
  author_email: schaefermeyer@alumni.tu-berlin.de
  author_url: ''
  date: '2014-06-29 10:45:03 -0700'
  date_gmt: '2014-06-29 17:45:03 -0700'
  content: "Sorry folks, but the 100th birthday of the power method is already over.
    It was Chaim Müntz who presented it to the French Academy of Sciences in 1913.\r\nhttp://gallica.bnf.fr/ark:/12148/bpt6k3109m/f43.image.langFR\r\nhttp://gallica.bnf.fr/ark:/12148/bpt6k3109m/f860.image.langFR"
- id: 3161
  author: Robustness versus Acceleration | Moody Rd
  author_email: ''
  author_url: http://mrtz.org/blog/robustness-versus-acceleration/
  date: '2014-08-18 17:39:23 -0700'
  date_gmt: '2014-08-19 00:39:23 -0700'
  content: '[&#8230;] formally, can we show that any Krylov subspace method that converges
    asymptotically faster than the power method must accumulate [&#8230;]'
- id: 3861
  author: Zack
  author_email: kop.mazhuang@gmail.com
  author_url: ''
  date: '2014-09-26 18:57:12 -0700'
  date_gmt: '2014-09-27 01:57:12 -0700'
  content: "Really Helpful. \r\n\r\nBut could you please explain why ||V^TAX_{t-1}||&lt;\\sigma_{k+1}sin(\\theta)(U,
    X_{t-1}) during the proof of the lemma?"
- id: 3891
  author: Moritz Hardt
  author_email: m@mrtz.org
  author_url: ''
  date: '2014-09-28 08:56:44 -0700'
  date_gmt: '2014-09-28 15:56:44 -0700'
  content: Sure. You use the fact that you can write A as A = U\Sigma_U U^T + V \Sigma_V
    V^T, where V^T U = 0 and V^T V = Id. Therefore, V^T A X = \Sigma_V V^T X. Now,
    ||\Sigma_V V^T X|| \le ||\Sigma_V|| * ||V^T X|| by the submultiplicativity of
    the spectral norm. But the top singular value of \Sigma_V is \sigma_{k+1} and
    ||V^T X|| is just the definition of \sin\theta(U,X).
- id: 3892
  author: Moritz Hardt
  author_email: m@mrtz.org
  author_url: ''
  date: '2014-09-28 08:57:43 -0700'
  date_gmt: '2014-09-28 15:57:43 -0700'
  content: Jan, I forgot to respond to this when I saw it. This is really great! Thanks
    for those pointers. You should definitely update the wiki page on the power method
    when you get a chance.
- id: 6159
  author: Bo
  author_email: bo.xie@gatech.edu
  author_url: ''
  date: '2015-01-07 12:36:57 -0800'
  date_gmt: '2015-01-07 20:36:57 -0800'
  content: "Thanks for the post. It is really helpful.\r\n\r\nI was reading the proof
    in your NIPS paper and I am confused about the following inequality. Could you
    explain a little bit?\r\n\r\nIn the appendix, when you want to bound the effect
    of the noise projected on U, you have the following inequality\r\n\r\nmax_{||w||_2
    = 1, \\Pi^* w = w} ||U' G w|| / || U' X w||  \\le ||U' G|| / cos\\theta_k(U, X)\r\n\r\nMy
    confusion is that, cos\\theta_k(U, X) = ||U' X w|| / ||X w||. But in the numerator
    you only have ||U' G w||. How did ||X w|| come in? Using the property of the norm,
    you would only get ||U' G w|| \\le ||U' G|| ||w|| = ||U' G|| since ||w|| = 1.\r\n\r\nThanks!"
- id: 6168
  author: Zhao Song
  author_email: zhaos@utexas.edu
  author_url: ''
  date: '2015-01-08 22:28:18 -0800'
  date_gmt: '2015-01-09 06:28:18 -0800'
  content: Hi Moritz, In the newest arxiv version of your paper the noisy power method
    a meta algorithm with applications. In page 7, section 1.4, the reference in the
    last sentence of that page is missing. Which paper do you cite?
- id: 6173
  author: Moritz Hardt
  author_email: m@mrtz.org
  author_url: ''
  date: '2015-01-09 07:16:37 -0800'
  date_gmt: '2015-01-09 15:16:37 -0800'
  content: Oops. We'll update the arxiv version shortly. This is a reference to the
    Halko, Martinson and Tropp paper that is also referenced elsewhere in the paper.
- id: 6175
  author: Moritz Hardt
  author_email: m@mrtz.org
  author_url: ''
  date: '2015-01-09 07:38:50 -0800'
  date_gmt: '2015-01-09 15:38:50 -0800'
  content: "Thanks! Just to be clear, we're talking about Lemma 2.3 in the full version
    (arxiv). Reading your comment, Eric and I realized that there's an assumption
    missing in the statement lemma, namely that X has orthonormal columns, so X'X=I.
    This is always the case when we apply the lemma (by definition of the algorithm).
    \n\nNow, in general, we have ||U'Xw|| is at least \\sigma_k(U'X), since w is a
    unit vector and U'X has only k columns. Now, with the extra assumption that X
    is orthonormal, we have that \\sigma_k(U'X) is just the definition of \\cos\\theta_k(U,X)
    and so the inequality follows.\n\nI hope this clears up things. I'm grateful for
    your comment!"
- id: 6294
  author: Zhao Song
  author_email: zhaos@utexas.edu
  author_url: ''
  date: '2015-01-15 20:51:33 -0800'
  date_gmt: '2015-01-16 04:51:33 -0800'
  content: "Hi Moritz,\r\n\r\nI think you're talking about this paper. http://arxiv.org/pdf/0909.4061.pdf\r\nIn
    the page 7 of your paper, it said that that reference can spectrally approximate
    A after O(sigma_{k+1}/epsilon* log d) steps.\r\n\r\nTheir paper is very long,
    I only see :\r\nIn page 61, they claim that q = log (min{m,n})\r\n\r\nWhere do
    they claim the results as you wrote \"O(sigma_{k+1}/epsilon* log d)  steps\"?\r\n\r\nzhao"
- id: 6295
  author: Moritz Hardt
  author_email: m@mrtz.org
  author_url: ''
  date: '2015-01-15 21:05:20 -0800'
  date_gmt: '2015-01-16 05:05:20 -0800'
  content: "Yes, that's the paper. We just refer to what follows from (1.11).\r\n\r\nBut
    you're right, there's a typo. I believe it should just be O(\\log(d/\\epsilon)).
    The bound we state makes no sense, since scaling down the matrix would make \\sigma_{k+1}
    smaller and hence improve convergence. \r\n\r\nSorry for the confusion and thanks
    for pointing out the typo. As mentioned before, we need to update that whole paragraph
    anyway :-)"
- id: 6318
  author: Zhao Song
  author_email: zhaos@utexas.edu
  author_url: ''
  date: '2015-01-16 21:08:55 -0800'
  date_gmt: '2015-01-17 05:08:55 -0800'
  content: "Hi Moritz,\r\n\r\nIn Halko, Martinsson, and Tropp's work, page 10:\r\nthe
    difference between (1.10) and (1.11) is only one sigma_{k+1}, since formula (1.11)
    is the result of truncating 2k SVD to k SVD.\r\n\r\nLet's discuss the number of
    steps based on (1.10):\r\n\r\nE || A- U \\Sigma V^\\top || \\leq (something complicated)
    * sigma_{k+1}\r\nWe can simplify the \"something complicated\" to \r\n(n/k)^{1/q}
    by assuming m = n.\r\n\r\nIt is easy to see that (n/k)^{1/q} can not be smaller
    than 1.\r\nAssume that 1+epsilon = (n/k)^{1/q},\r\nthen we can get:\r\n =&gt;
    log ( 1 + epsilon ) = ( 1 / q ) * log( n / k )\r\n =&gt; epsilon = (1/q) * log
    (n/k)\r\n =&gt; q = (1/epsilon) * log (n/k)\r\n\r\nIt means, choosing at least
    O( (1/epsilon) * log (n/k) ) steps, to reach:\r\nE|| A- U\\Sigma V^\\top || \\leq
    (1+epsilon ) sigma_{k+1}\r\n\r\nThe above result is something like multiplicative
    error.\r\nReplacing epsilon by epsilon/sigma_{k+1}, \r\nwe can get some similar
    results as you wrote in the page 7 of your paper.\r\nRight?\r\n\r\nI don't think
    the way you defined open problem in page 8 is the most reasonable way.\r\n\r\nIn
    fact, you should assume that\r\n||G_l || \\leq eta \r\n|| U^\\top G_l || \\leq
    eta * sqrt{k/d}\r\n|| (I -X_L X_L^\\top) A || \\leq  (1+epsilon ) * sigma_{k+1}
    \ + eta\r\n\r\nThe desired steps might be O( poly(1/eta,1/epsilon, log(n/k)) )
    -- I'm not sure the about the exact form.\r\n\r\nHere, I use epsilon to denote
    the approximation error, eta to denote the noise.\r\nUser can choose as small
    epsilon as they needed, but they shouldn't control eta. On the other hand, eta
    is small, but not arbitrarily small.\r\n\r\nbest,\r\n\r\nzhao"
---
<p>The Power Method is the oldest practical method for finding the eigenvector of a matrix corresponding to the eigenvalue of largest modulus. Most of us will live to celebrate the Power Method's 100th birthday around 2029. I plan to throw a party. What's surprising is that the Power Method continues to be highly relevant in a number of recent applications in algorithms and machine learning. I see primarily two reasons for this. One is computational efficiency. The Power Method happens to be  highly efficient both in terms of memory footprint and running time. A few iterations often suffice to find a good approximate solution. The second less appreciated but no less important aspect is <em>robustness</em>. The Power Method is quite well-behaved in the presence of noise making it an ideal candidate for a number of applications. It's also easy to modify and to extend it without breaking it. Robust algorithms live longer. The Power Method is a great example. We saw another good one before. (Hint: <a href="http://mrtz.org/blog/the-zen-of-gradient-descent/">Gradient Descent</a>) In this post I'll describe a very useful robust analysis of the Power Method that is not as widely known as it sould be. It characterizes the convergence behavior of the algorithm in a strong noise model and comes with a neat geometric intuition.</p>
<h2>Power Method: Basics</h2>
<p>Let's start from scratch. The problem that the power method solves is this:</p>
<p style="text-align: center;">Given \({A,}\) find the rank \({1}\) matrix \({B}\) that minimizes \({\|A-B\|_F^2.}\)</p>
<p>Here, \({\|A-B\|_F^2}\) is the squared Frobenius norm of the difference between \({A}\) and \({B.}\) (Recall that this is the sum of squared entries of \(A-B\)). Any rank \({1}\) matrix can of course be written as \({xy^T}\) (allowing for rectangular \({A}\)). On the face of it, this is a non-convex optimization problem and there is no a priori reason that it should be easy! Still, if we think of \({f(x,y) = \|A-xy^T\|_F^2}\) as our objective function, we can check that setting the gradient of \({f}\) with respect to \({x}\) to zero gives us the equation by \({x=Ay}\) provided that we normalized \({y}\) to be a unit vector. Likewise taking the gradient of \({f}\) with respect to \({y}\) after normalizing \({x}\) to have unit norm leads to the equation \(y={A^T x.}\) The Power Method is the simple algorithm which repeatedly performs these update steps. As an aside, this idea of solving a non-convex low-rank optimization problem via alternating minimization steps is a powerful heuristic for a number of related problems.</p>
<p>For simplicity from here on we'll assume that \({A}\) is symmetric. In this case there is only one update rule: \({x_{t+1} = Ax_{t}.}\) It is also prudent to normalize \({x_t}\) after each step by dividing the vector by its norm.</p>
<p>The same derivation of the Power Method applies to the more general problem: Given a symmetric \({n\times n}\) matrix \({A,}\) find the rank \({k}\) matrix \({B}\) that minimizes \({\|A-B\|_F^2}\). Note that the optimal rank \({k}\) matrix is also given by the a truncated singular value decomposition of \({A.}\) Hence, the problem is equivalent to finding the first \({k}\) singular vectors of \({A.}\)</p>
<p>A symmetric rank \({k}\) matrix can be written as \({B= XX^T}\) where \({X}\) is an \({n\times k}\) matrix. The update rule is therefore \({X_{t+1} = AX_{t}}\). There are multiple ways to normalize \({X_t}\). The one we choose here is to ensure that \({X_t}\) has orthonormal columns. That is each column has unit norm and is orthogonal to the other columns. This is can be done using good ol' boys  <a title="Gram Schmidt" href="http://en.wikipedia.org/wiki/Gram%E2%80%93Schmidt_process">Gram-Schmidt</a> (though in practice people prefer the Householder method).</p>
<p>The resulting algorithm is often called Subspace Iteration. I like this name. It stresses the point that the only thing that will matter to us is the subspace spanned by the columns of \({X_t}\) and not the particular basis that the algorithm happens to produce. This viewpoint is important in the analysis of the algorithm that we'll see next.</p>
<h2>A Robust Geometric Analysis of Subspace Iteration</h2>
<p>Most of us know one analysis of the power method. You write your vector \({x_t}\) in the eigenbasis of \({A}\) and keep track of how matrix vector multiplication manipulates the coefficients of the vector in this basis. It works and it's simple, but it has a couple of issues. First, it doesn't generalize easily to the case of Subspace Iteration. Second, it becomes messy in the presence of errors. So what is a better way? What I'm going to describe was possibly done by numerical analysts in the sixties before the community moved on to analyze more modern eigenvalue methods.</p>
<h3>Principal Angles</h3>
<p>To understand what happens in Subspace Iteration at each step, it'll be helpful to have a potential function and to understand under which circumstances it decreases. As argued before the potential function should be basis free to avoid syntactic arguments. The tool we're going to use is the <strong>principal angle</strong> between subspaces. Before we see a formal definition, it turns out that much of what's true for the angle between two vectors can be lifted to the case of subspaces of equal dimension. In fact, much of what's true for the angle between spaces of equal dimension generalizes to unequal dimensions with some extra care.</p>
<p>The two subspaces we want to compare are the space spanned by the \({k}\) columns of \({X_t}\) and the space \({U}\) spanned by the \({r}\) dominant singular vectors of \({A.}\) For now, we'll discuss the case where \({r=k.}\) I'll be a bit sloppy in my notation and use the letters \({U,X_t}\) for these subspaces.</p>
<p>Let's start with \({k=1}\). Here the cosine of the angle \({\theta}\) between the two unit vectors \({X_t}\) and \({U}\) is of course defined as \({\cos\theta(U,X_t)= |U^T X_t|.}\) It turns out that the natural generalization for \({k&gt;1}\) is to define</p>
<p style="text-align: center;">\(\displaystyle \cos\theta(U,X_t)=\sigma_{\mathrm{min}}(U^T X_t). \)</p>
<p>In words, the cosine of the angle between \({U}\) and \({X_t}\) is the smallest singular value of the \({k\times k}\) matrix \({U^T X_t}\). Here's a sanity check on our definition. If the smallest singular value is \({0}\) then there is a nonzero vector in the range of the matrix \({X_t}\) that is orthogonal to the range of \({U}\). In an intuitive sense this shows that the subspaces are quite dissimilar. To get some more intuition, consider a basis \({V}\) for the orthogonal complement of \({U.}\) It makes sense to define \({\sin\theta(U,X_t)= \sigma_{\mathrm{max}}(V^T X_t)}\). Indeed, we can convince ourselves that this satisfies the familiar rule \({1= \sin^2\theta + \cos^2\theta}\). Finally, we define \({\tan\theta}\) as the ratio of sine to cosine.</p>
<h3>A strong noise model</h3>
<p>Let's be ambitious and analyze Subspace Iteration in a strong noise model. It turns out that this will not actually make the analysis a lot harder, but a lot more general. The noise model I like is one in which each matrix-vector product is followed by the addition of a possibly adversarial noise term. Specifically, the only way we can access the matrix \(A\) is through an operation of the form</p>
<p style="text-align: center;">\(\displaystyle Y = AX + G. \)</p>
<p>Here, \({X}\) is what we get to choose and \({G}\) is the noise matrix we may not get to choose. We assume that \(G$ is the only source of error and that arithmetic is exact. In this model our algorithm proceeds as follows:</p>
<div style="border: 1px solid #bbb; padding: 10px;">Pick \({X_0.}\) For \({t = 1}\) to \({t=L:}\)</p>
<ol>
<li>\({Y_t = AX_{t-1} + G_t}\)</li>
<li>\({X_t = \text{Orthonormalize}(Y_t)}\)</li>
</ol>
</div>
<h3>The main geometric lemma</h3>
<p>To analyze the above algorithm, we will consider the potential function \({\tan\theta(U,X_t).}\) If we pick \({X_0}\) randomly it's not so hard to show that it starts out being something like \({O(\sqrt{kn})}\) with high probability. We'll argue that \({\tan\theta(U,X_t)}\) decreases geometrically at the rate of \({\sigma_{k+1}/\sigma_{k}}\) under some assumptions on \({G_t}\). Here, \({\sigma_k}\) is the \({k}\)-th largest singular value. The analysis therefore requires a separation between \({\sigma_k}\) and \({\sigma_{k+1}}\). (NB: We can get around that by taking the dimension \({r}\) of \({U}\) to be larger than \({k.}\) In that case we'd get a convergence rate of the form \({\sigma_{r+1}/\sigma_k.}\) The argument is a bit more complicated, but can be found <a title="Robust Subspace Iteration and Privacy-Preserving Spectral Analysis" href="http://arxiv.org/abs/1311.2495">here</a>.)</p>
<p>Now the lemma we'll prove is this:</p>
<p style="text-align: left;"><strong>Lemma.</strong> For every \({t\ge 1,}\)</p>
<p style="text-align: center;">\(\displaystyle \tan\theta(U,X_t) \le \frac{\sigma_{k+1}\sin\theta(U,X_{t-1})+\|V^T G_t\|} {\sigma_k\cos\theta(U,X_{t-1})-\|U^T G_t\|}. \)</p>
<p>This lemma is quite neat. First of all if \({G_t=0,}\) then we recover the noise-free convergence rate of Subspace Iteration that I claimed above. Second what this lemma tells us is that the sine of the angle between \({U}\) and \({X_{t-1}}\) gets perturbed by the norm of the projection of \({G_t}\) onto \({V}\), the orthogonal complement of \({U.}\) This should not surprise us, since \({\sin\theta(U,X_{t-1})=\|V^T X_{t-1}\|.}\) Similarly, the cosine of the angle is only perturbed by the projection of \({G_t}\) onto \({U.}\) This again seems intuitive given the definition of the cosine. An important consequence is this. Initially, the cosine between \({U}\) and \({X_0}\) might be very small, e.g. \({\Omega(\sqrt{k/n})}\) if we pick \({X_0}\) randomly. Fortunately, the cosine is only affected by a \({k}\)-dimensional projection of \({G_t}\) which we expect to be much smaller than the total norm of \({G_t.}\)</p>
<p>The lemma has an intuitive geometric interpretation expressed in the following picture:</p>
<p><a href="http://mrtz.org/blog/wp-content/uploads/2013/11/power-method.png"><img class="aligncenter size-full wp-image-278" alt="power-method" src="http://mrtz.org/blog/wp-content/uploads/2013/11/power-method.png" width="500" /></a></p>
<p>It's straightforward to prove the lemma when \({k=1}\). We simply write out the definition on the left hand side, plug in the update rule that generated \({X_t}\) and observe that the normalization terms in the numerator and denominator cancel. This leaves us with the stated expression after some simple manipulations. For larger dimension we might be troubled by the fact that we applied the Gram-Schmidt algorithm. Why would that cancel out? Interestingly it does. Here's why. The tangent satisfies the identity:</p>
<p style="text-align: center;">\(\displaystyle \tan\theta(U,X_t) = \|(V^T X_t)(U^TX_t)^{-1}\|. \)</p>
<p>It's perhaps not obvious, but not more than an exercise to check this. On the other hand, \({X_t = Y_t R}\) for some invertible linear transformation \({R.}\) This is a property of orthonormalization. Namely, \({X_t}\) and \({Y_t}\) must have the same range. But \({(U^TY_tR)^{-1}=R^{-1}(U^T Y_t)^{-1}}\). Hence</p>
<p style="text-align: center;">\(\displaystyle \|(V^T X_t)(U^TX_t)^{-1}\| = \|(V^T Y_t)(U^TY_t)^{-1}\|. \)</p>
<p>It's now easy to proceed. First, by the submultiplicativity of the spectral norm,</p>
<p style="text-align: center;">\(\displaystyle \|(V^T Y_t)(U^TY_t)^{-1}\| \le \|(V^T Y_t)\|\cdot\|(U^TY_t)^{-1}\|. \)</p>
<p>Consider the first term on the right hand side. We can bound it as follows:</p>
<p style="text-align: center;">\(\displaystyle \|(V^T Y_t)\|\!\le\!\|V^TAX_{t-1}\| + \|V^T G_t\|\!\le\! \sigma_{k+1}\sin\theta(U,X_{t-1}) + \|V^T G_t\|. \)</p>
<p>Here we used that the operation \({V^T A}\) eliminates the first \({k}\) singular vectors of \({A.}\) The resulting matrix has spectral norm at most \({\sigma_{k+1}}\).</p>
<p>The second term follows similarly. We have \({\|(U^T Y_t)^{-1}\| = 1/\sigma_{\mathrm{min}}(U^TY_t)}\) and</p>
<p style="text-align: center;">\(\displaystyle\!\!\!\sigma_{\mathrm{min}}(U^TY_{t})\!\ge\!\sigma_{\mathrm{min}}(U^TAX_{t-1})\!-\!\|U^T G_t\|\!\ge\! \sigma_k\cos\theta(U,X_{t-1})\!-\!\|U^T G_t\|\!\!\!\)</p>
<p>This concludes the proof of the lemma.</p>
<h2>Applications and Pointers</h2>
<p>It's been a long post, but it'd be a shame not to mention some applications. There are primarily three applications that sparked my interest in the robustness of the Power Method.</p>
<p>The first application is in <strong>privacy-preserving singular vector computation</strong>. Here the goal is to compute the dominant singular vectors of a matrix without leaking too much information about individual entries of the matrix. We can formalize this constraint using the notion of Differential Privacy. To get a differentially private version of the Power Method we must add a significant amount of Gaussian noise at each step. To get tight error bounds it's essential to distinguish between the projections of the noise term onto the space spanned by the top singular vectors and its orthogonal complement. You can see the full analysis <a href="http://arxiv.org/abs/1311.2495">here</a>.</p>
<p>Another exciting motivation comes from the area of <strong>Matrix Completion</strong>. Here, we only see a subsample of the matrix \({A}\) and we wish to compute its dominant singular vectors from this subsample. Alternating Minimization (as briefly mentioned above) is a popular and successful heuristic in this setting, but rather difficult to analyze. <a href="http://dl.acm.org/citation.cfm?doid=2488608.2488693">Jain, Netrapalli and Sanghavi</a> observed that it can be seen and analyzed as an instance of the noisy power method that we discussed here. The error term in this case arises because we only see a subsample of the matrix and cannot evaluate exact inner products with \({A.}\) These observations lead to rigorous convergence bounds for Alternating Minimization. I recently <a href="http://arxiv.org/abs/1312.0925">posted some improvements</a>.</p>
<p>Surprisingly, there's a fascinating connection between the privacy setting and the matrix completion setting. In both cases the fundamental parameter that controls the error rate is the <em>coherence</em> of the matrix \({A}\). Arguing about the coherence of various intermediate solutions in the Power Method is a non-trivial issue that arises in both settings and is beyond the scope of this post.</p>
<p>Finally, there are very interesting <strong>tensor generalizations of the Power Method </strong>and robustness continues to be a key concern. See, for example, <a href="http://arxiv.org/abs/1210.7559">here </a>and <a href="http://arxiv.org/abs/1311.2972">here</a>. These tensor methods have a number of applications in algorithms and machine learning that are becoming increasingly relevant. While there has been some progress, I think it is fair to say that much remains to be understood in the tensor case. I may decide to work on this once my fear of tensor notation recedes to bearable levels.</p>
