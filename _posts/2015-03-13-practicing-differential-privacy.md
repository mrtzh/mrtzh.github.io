---
layout: post
published: true
title: Towards practicing differential privacy
author: Moritz Hardt
comments: true
date: '2015-03-13 14:30:00 -0800'
tags:
- tcs
- differential privacy
- practice
---

More than a year ago I wrote an article with the provocative title: [Is
Differential Privacy practical?](http://blog.mrtz.org/2013/08/21/dp-practical.html)
The post was essentially one big buildup for
an epic follow-up post that I simply never wrote. Since then dozens
have asked me for an answer to this urgent question. Recently, after the post
hit the front page of Hacker News, half a dozen emails
inquired about the follow-up post that I had promised. Some [speculated](https://news.ycombinator.com/item?id=9184479) that owing to [Betteridge's law of
headlines](http://en.wikipedia.org/wiki/Betteridge%27s_law_of_headlines), the
answer was simply *no*.

Despite my venerable history of failing on various commitments and my apparent
peace with it, this situation went too far even by my own low standards.
So, I decided to write a not so epic version of that promised blog
post.

## The California Public Utilities Commission ##

I'll arrange my thoughts around the case of the [California Public
Utilities Commission](http://www.cpuc.ca.gov/puc/) (CPUC). The CPUC is a
regulatory agency that regulates privately owned public utilities in
California. In recent years there has been political pressure on the utilities
to give third parties access to smart meter data. As discussed in [my previous
post](http://blog.mrtz.org/2013/08/21/dp-practical.html), smart meter data is
of enormous value to many, but comes with serious privacy challenges.

To settle these issues the CPUC organized a major legal proceeding with the
goal of creating rules that provide access to energy usage data to local
government entities, researchers, and state and federal agencies while
establishing procedures that protect the privacy of consumer data.

I served as a privacy expert within the proceeding together with Cynthia Dwork, Lee Tien from the
[EFF](http://www.eff.org), and Jennifer Urban and her team from Berkeley.
Our goal was to inform various parties about the pitfalls
of insufficient privacy mechanisms and to propose better ones. Our proposed
solution focused on differential privacy for the uses cases in which it made
sense. There were a number of use cases that the CPUC considered. Not all of
them were well suited for differential privacy to begin with.

### A proposed decision ###

My involvement with the case ended in 2014 after a [proposed
decision](http://docs.cpuc.ca.gov/PublishedDocs/Efile/G000/M088/K947/88947979.PDF)
of the administrative judge. To summarize a 120 page document in one sentence,
the ruling did not endorse differential privacy strongly enough for me to further pursue the case actively.
Nevertheless, there was still significant interest in differential privacy
from some of the utilities. I believe that one utilities company
engaged with Microsoft with the goal of building a prototype of a
differentially private solution for their data sharing needs.

The ruling was disappointing from my perspective in that it did not advocate
the use of differential privacy in any of the use cases. Meanwhile it shot
down several uses cases essentially not giving the use
case sponsors meaningful access to energy data at all. In those cases
differential privacy could've provided an obviously better trade-off for everyone.

The ruling didn't so much reflect a technical verdict about differential privacy. Rather it reflected our inability to successfully anticipate and maneuver the highly complex political and legal environment in which the decision was made.

### A post mortem ###

Our proposal based on differential privacy initially met with resoundingly positive
responses when we first presented it to the administrative judge and various
parties present in the meeting. We did however face bitter opposition from a
group of researchers who sponsored one use case. Those researchers, who had
been working with raw smart meter data in the past, were worried that differential privacy
would create an obstacle for them. We quickly realized that it would be
difficult to agree with them on the extent to which their research practices
are compatible with differential privacy. So, we specifically excluded their
use case from the scope of our proposal focusing on some of the remaining use cases instead. This
didn't stop the researchers from lobbying relentlessly against differential
privacy. In particular, they filed a last minute comment in which they
attacked differential privacy sharply based on many profound factual misunderstandings
of the privacy notion. Due to the perfect timing of their comment, we were
unable to submit a rebuttal. In the end, I believe this alone was enough for the
administrative judge to conclude that the use of differential privacy was at
present too controversial to be proposed as a solution in the ruling.

My point is not to criticize this group of researchers. I'm sympathetic with
them. They've been working with energy data for many years. They're doing important work which is probably already difficult enough as it is. We respected their
position and did not want to interfere with their research. My guess
is that their research practices are actually largely consistent with what's
possible under differential privacy, but that's an entirely separate
discussion.

What's tragic is that their opposition ended up hurting a consumer advocacy
group who could've used differential privacy as a means to gain *more* access to
energy data than they were able to get in the end (essentially nothing). There was a lot of miscommunication throughout the proceeding that clearly didn't help. For instance, initially the consumer advocacy group proposed their own ad-hoc privacy solution (which we didn't support). Only later did we find some common ground. In hindsight, we should've agreed on and jointly represented the same solution from the beginning. In my understanding, the use case didn't require more than the kind of aggregate usage statistics that we could've easily produced while preserving differential privacy without any major engineering efforts.

## Towards practicing differential privacy ##

Drawing on my experience with the CPUC case, I want to end with some concrete
suggestions and questions hoping that they will help others when applying
differential privacy. When I speak of "the community", I will make some very broad generalizations knowing full well that in each instance there are certainly exceptions to what I claim. The discussion below is by no means a survey as it contains very few links to the rich literature on differential privacy. I strongly encourage you to fill in relevant missing pointers in the comments.

### Focus on win-win applications ###

Apply differential privacy as a tool to provide access to data where
currently access is problematic due to privacy regulations. Don't fight the
data analyst. Don't play the moral police. Imagine you are the analyst.

As a privacy expert,
you will find yourself having to shoot down inadequate solutions all the time.
Why can't we just omit those 18 sensitive attributes like in the HIPAA safe harbor provision?
Why isn't it safe to release any statistic that is aggregated over at least 15 households in which no
single household contributes 15% of the total number (i.e., the "15/15" rule)?
Such ad-hoc rules sound intuitively appealing to non-experts. Refuting them is time-consuming and makes
you look defensive.

Rather than shooting down what doesn't work, point out why differential privacy is better than those solutions not just from a privacy perspective but rather from a *utility* perspective. Unlike these solutions,
differential privacy does not alter your data set at all. In particular, from a statistical perspective
you do not change the distribution from which the data were drawn. This is an incredibly powerful
proposition. I think that data analysis with differential privacy can be vastly more useful than
what you get after applying, for instance, the HIPAA safe harbor mechanism.

My point is that there are many "win/win" applications of differential privacy where it simultaneously can give better utility and better privacy than its alternatives. As the CPUC case showed, sometimes the choice is even between no access at all and differentially private access. It's really a no-brainer. We should start with such applications instead of arguing about completely unrestricted access versus differentially private access.

### Don't empower the naysayers ###

In my opinion, for differential privacy to be a major success in practice it would be sufficient if it were  successful in *some* applications but certainly not in *all*---not even in most. There's a culture of criticizing differential privacy based on the perfectly correct observation that some differentially private algorithm (say, Laplace) didn't give enough utility in some application. These kind of observations---valid as they may be---say very little about the potential of differential privacy in practice. First of all, they only evaluate one algorithm while there could be much better algorithms. Second, they commit to one specific application and, more importantly, one particular modeling of the problem. Perhaps there's a different approach to the same problem that's more compatible with differential privacy. It's simply impossible to rule out differential privacy as a solution through these kind of straw man experiments.

The differential privacy community is partially at blame for empowering the naysayers, since they have advertised differential privacy as a *universal* solution concept to the privacy problem. This is theoretically true in some sense, but the situation in practice is much more delicate. So, stop feeding the naysayers. Start presenting differential privacy as a promising technology for *some* applications but certainly not *all*.

### Change your narrative ###

Don't present differential privacy as a fear inducing crypto hammer
designed to obfuscate data access. That's not what it is.
Differential privacy is a rigorous way of doing machine learning, not a way of
preventing machine learning from being done. We understand perfectly well now
that differential privacy is a stability guarantee which is fundamentally
aligned with the central goal of statistics, namely, to learn from data about the population
as a whole and not about specific individuals. This understanding perhaps wasn't quite there
in the beginning, but it is now. Academics should from time to time come up
with a new page 1 for their papers.

### Build reliable code repositories ###

A  weakness of the differential privacy community has been the scarcity of
available high quality code. There are many academic code pieces available
by emailing someone, but we don't have many visible repositories on github
or elsewhere that provide robust implementations of common differentially
private algorithms. Frank McSherry's [PINQ](http://research.microsoft.com/en-us/projects/pinq/) was a really wonderful step in the right direction,
but it is no longer maintained and by now out of date. Written in C#, it hasn't been easy for many to build on and extend PINQ. A more recent notable effort is the [Dual Query](https://github.com/ejgallego/dualquery) code though it requires CPLEX to run.

What scares me a bit is that even a project as solidly designed and carefully executed as PINQ
did not address low-level implementation issues such as [floating point vulnerabilities](http://dl.acm.org/citation.cfm?id=2382264) in differential privacy.

I'm guilty myself. Many have used or tried to use [MWEM](http://papers.nips.cc/paper/4548-a-simple-and-practical-algorithm-for-differentially-private-data-release.pdf), an algorithm Katrina Ligett, Frank McSherry and I presented at NIPS a few years ago. Yet we don't have a great implementation publicly available. You can email us for a decent C# implementation (alas!), but instead a lot of people have
produced their own implementations of our algorithm over the years. I regularly have the urge to start an open source project for it, but then I realize it's a bit of a bottomless pit. In order to have a solid implementation of MWEM, I'd first need to have a solid implementation of all the primitives with all the low-level issues that come up. In any case, if somebody more brave then myself took the first step on an open source effort (preferably not in C#), I'd be very eager to contribute.

Taking a more modest step, I feel compelled to compile a list of available code repositories.
If you have any pointers, please leave a comment!

### Be less general and more domain-specific ###

Much of the academic research on differential privacy has focused on generality. That makes sense theoretically, but it means that reading the scientific literature on differential privacy from the point of
view of a domain expert can be very frustrating. Most papers start with toy
examples that make perfect sense on a theoretical level, but will appear
alarmingly na&iuml;ve to a domain expert.

The community is at a point where we need to transition *from generality to specificity*.
For example, what's needed are domain-specific tutorials
that walk practitioners through real examples. One reason why such
tutorials don't exist is that they take a lot of time and writing them isn't
incentivized by academia. One way out of this is for journal editors and
conferences to specifically invite such tutorials. Similarly, the community should at this point have very high regard for positive results and case studies in specific application domains even if they are limited in scope and don't contribute technically new solutions.

### Be more entrepreneurial ###

The CPUC case highlighted that the application of differential privacy in
practice can fail as a result of many non-technical issues. These important
issues are often not on the radar of academic researchers. We spent an awful
lot of time talking about the technical strengths or limitations of
differential privacy, while missing out on some very real challenges. It's quite reasonable to argue
that these challenges  should be outside the scope of academia. On the other hand, academics are currently the
only available experts on differential privacy and there's obvious demand for it.
Where should we draw the line?

To be blunt, I think an important ingredient that's missing in the current differential
privacy ecosystem is *money*. There is only so much that academic researchers can do to promote a technology.
Beyond a certain point businesses have to commercialize the technology for it be successful. The CPUC
case was much better suited as the full-time job for a group of paid professionals
rather than a volunteering effort. I'm surprised none of the researchers working on differential privacy
have devoted a sabbatical to running a privacy startup. It's needed and the potential upside is big.
Why not give it a shot? I hear tenured jobs are meant for running startups.

### So, is differential privacy practical? ###

I like the answer Aaron Roth gave when I asked him:

<div style="text-align:center;">
<em>It's within striking distance.</em>
</div>

