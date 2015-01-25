---
layout: post
status: publish
published: true
title: The NIPS Experiment
author: Eric Price
date: '2014-12-15 11:45:39 -0800'
categories:
- conference
tags:
- tcs
comments:
- id: 5751
  author: same here
  author_email: same@here.yu
  author_url: ''
  date: '2014-12-15 12:43:41 -0800'
  date_gmt: '2014-12-15 20:43:41 -0800'
  content: "\"the basic committee process was that almost everything above 6.5 was
    accepted, almost everything below 6 was rejected, and the committee mainly debated
    the papers in between.\"\r\n\r\nThis is already part of the problem. \r\n\r\nThe
    range of disagreement which is discussed is too narrow. I would expect a conference
    with P acceptances to almost automatically accept the top P/2 papers, then reject
    all but P of the remaining papers, and spend most of their time discussing the
    remaining papers left (i.e. P papers if you do the math)  which are vying for
    the remaining P/2 acceptance slots.\r\n\r\nSecond, the size of the conference
    needs to be expanded/shrunk to a place where referees are no longer trying to
    separate papers because of formatting or technical complexity, which are second
    order signals. A well run conference will vary in size from year to year by up
    to 10-15%. On a good year you accept an extra 7-20 papers, in a bad year you drop
    the same number. A badly run conference accepts the same number of papers year
    after year after year."
- id: 5758
  author: Eric Price
  author_email: ecprice@gmail.com
  author_url: ''
  date: '2014-12-15 14:19:43 -0800'
  date_gmt: '2014-12-15 22:19:43 -0800'
  content: "For your first point, I suspect that NIPS does do something like this
    (we'll find out when they release the reviews).  The issue is that it turns out
    that the top p/2 and bottom 1-3p/2 are not actually clear -- it might seem that
    way to one PC, but it turns out that another PC with different reviewers doesn't
    actually agree with those choices.\r\n\r\nFor your second point, NIPS does vary
    the number of accepted papers:\r\n<a href=\"http://mrtz.org/blog/wp-content/uploads/2014/12/nips_paper_count.png\"
    rel=\"nofollow\">http://mrtz.org/blog/wp-content/uploads/2014/12/nips_paper_count.png</a>\r\n"
- id: 5760
  author: Gary Cottrell
  author_email: gary@ucsd.edu
  author_url: https://cseweb.ucsd.edu/~gary/
  date: '2014-12-15 15:06:16 -0800'
  date_gmt: '2014-12-15 23:06:16 -0800'
  content: "Another way to look at this is that there were about 37+21=58 papers that
    were NIPS-acceptable. \r\n\r\nSo, given that they were acceptable, about 37/58
    or roughly 64% of acceptable papers got in.\r\n\r\nGiven that base rate, they
    disagreed on 21/58, or 36% of acceptable papers."
- id: 5761
  author: Quaid Morris
  author_email: quaid.morris@gmail.com
  author_url: ''
  date: '2014-12-15 15:14:08 -0800'
  date_gmt: '2014-12-15 23:14:08 -0800'
  content: "Eric: Great analysis!\r\n\r\nOne comment: I think it would be more illustrative
    to divide the \"Fractions of submissions that are clear accepts\" by the fraction
    of submissions that were accepted (.225) to get the \"y = Fraction of accepted
    submissions that are clear accepts\". If you do that, you get numbers like y=25%
    versus 30% of submissions that are clear rejects; this sounds about right to me
    and doesn't sound nearly as random."
- id: 5764
  author: Eric Price
  author_email: ecprice@gmail.com
  author_url: ''
  date: '2014-12-15 17:06:15 -0800'
  date_gmt: '2014-12-16 01:06:15 -0800'
  content: "Yeah, paper quality is an important aspect that I didn't really discuss
    directly.\r\n\r\nI don't see why you would think that only 58 were NIPS-acceptable
    -- because it's a random process, a decent number will be missed by both committees.
    \ If we go with the \"messy middle\" model, at least 50% of papers are acceptable,
    so at most 37/83 = 45% of acceptable papers got in.  If some papers are clear
    accepts, then this percentage would be even lower.\r\n\r\nThat said, I don't think
    \"NIPS-acceptable\" is a good way of thinking about things, and the noisy scoring
    model gives a better view.  The quality of papers is continuous, we have a noisy
    estimate of this quality, NIPS wants to take the top k, and there are lots of
    papers near the boundary that could make it in.  If NIPS decided to expand or
    contract in size, there'd still be lots of papers near the new boundary.\r\n\r\nThe
    NIPS organizers briefly showed a plot of the results of the NIPS experiment if
    you varied the acceptance rate, but I didn't have time to understand it clearly."
- id: 5765
  author: Eric Price
  author_email: ecprice@gmail.com
  author_url: ''
  date: '2014-12-15 17:12:55 -0800'
  date_gmt: '2014-12-16 01:12:55 -0800'
  content: "I included that number in the text above the graph, but I think it makes
    sense to keep the two axes on the same scale.\r\n\r\nNote that your number still
    seems pretty random: with those parameters, 25% of the papers at the conference
    are clear accepts and the other 75% are drawn uniformly from a pool of 4 times
    the size (giving 25% + 75% / 4 = 44% consistency as desired)."
- id: 5766
  author: David Karger
  author_email: karger@mit.edu
  author_url: http://people.csail.mit.edu/karger
  date: '2014-12-15 17:13:13 -0800'
  date_gmt: '2014-12-16 01:13:13 -0800'
  content: "Eric, I was delighted to learn about this experiment.  I agree that there's
    lots of randomness in conference acceptance, but I think we deal with it through
    repeated trials.  When a paper doesn't get in, it's submitted elsewhere, and I
    believe any good paper eventually gets in.  \r\n\r\nHere's some other data that
    you might want to look at: I did an analysis of CHI reviewing to assess whether
    we actually needed 3 reviewers.  Included is a list of distributions of review
    scores, which you might be able to use to tune your model:\r\nhttp://haystack.csail.mit.edu/blog/2014/01/15/allocating-chi-reviewers-2014-edition/"
- id: 5767
  author: Eric Price
  author_email: ecprice@gmail.com
  author_url: ''
  date: '2014-12-15 17:47:13 -0800'
  date_gmt: '2014-12-16 01:47:13 -0800'
  content: "&gt; I think we deal with it through repeated trials.\r\n\r\nYeah, this
    is an important effect.  But it introduces biases of its own, since the payoff
    is the maximum rather than the average of the repeated trials.  So you have one
    incentive to keep submitting to top conferences, and social pressure/time pressure
    to give up and go for a lower tier.\r\n\r\nA concrete example is my SODA best
    student paper, which I very nearly submitted to a weaker conference after getting
    3 rejections.  There's a tendency to think that because the maximum evaluation
    was high it must be a very good paper.  I personally think it is, but I'm biased
    and the average review has not been great.\r\n\r\n&gt; Here’s some other data
    that you might want to look at\r\n\r\nNice!  Would it be possible to get the complete
    set of review triples, rather than just the 2-way marginals?"
- id: 5768
  author: Grigory Yaroslavtsev
  author_email: grigory@grigory.us
  author_url: http://grigory.us
  date: '2014-12-15 18:02:57 -0800'
  date_gmt: '2014-12-16 02:02:57 -0800'
  content: Great post, Eric! I'd love to see results of a similar experiment at a
    theory conference. One potential challenge in the interpretation of the results
    is that splitting the committee in 2 parts may lead to disproportionate representation
    of different areas and thus introduce a bias.
- id: 5776
  author: Eric Price
  author_email: ecprice@gmail.com
  author_url: ''
  date: '2014-12-15 22:49:40 -0800'
  date_gmt: '2014-12-16 06:49:40 -0800'
  content: "Replicating it in a theory conference would be great.  It's harder, though,
    because the theory conferences are not delegated out as much as NIPS (with area
    chairs, etc).\r\n\r\nI suspect the main cause of the variation in the NIPS experiment
    is variation in representation of different areas between the two committees.
    \ If one PC thinks topic A is more interesting than topic B and the other PC thinks
    the opposite, this may cause different decisions for marginal papers on the two
    topics.\r\n\r\nBut I'm not sure why you would expect splitting the committee to
    introduce a bias. I can see it increasing variance, but it seems like it should
    preserve the expectation, right?"
- id: 5777
  author: David Karger
  author_email: karger@mit.edu
  author_url: http://people.csail.mit.edu/karger
  date: '2014-12-15 23:02:13 -0800'
  date_gmt: '2014-12-16 07:02:13 -0800'
  content: I don't currently have permission to share more than I published, but I
    can ask....
- id: 5779
  author: Duncan
  author_email: duncan@microsoft.com
  author_url: http://Watts
  date: '2014-12-15 23:25:31 -0800'
  date_gmt: '2014-12-16 07:25:31 -0800'
  content: 'Great experiment. Reminds me of Steve Ceci''s experiment with psychology
    journals:  http://journals.cambridge.org/action/displayAbstract?fromPage=online&amp;aid=6577844&amp;fileId=S0140525X00011183'
- id: 5781
  author: Ingo Keck
  author_email: ingokeck@ingokeck.de
  author_url: http://ingokeck.de
  date: '2014-12-16 01:13:32 -0800'
  date_gmt: '2014-12-16 09:13:32 -0800'
  content: "The 'double-blind' review is never really blind. You generally know who
    is working in your field, and you know from other conferences what they are working
    on. I have seen a few authors posting on twitter that they have submitted something
    to NIPS, which makes it even easier to guess where the paper is coming from.\r\n\r\nIt
    gets even worse thanks to the rebuttal phase:\r\n(1) Imagine me being a bad reviewer
    who just wants to let friends in, independent of the article quality. If I accidentally
    reject a friend's paper, the rebuttal phase plus maybe the information of this
    friend that his paper on xyz got rejected, allows me to reject the rejection.\r\n(2)
    Imagine me as a normal reviewer, then the rebuttal phase is additional work that
    I am probably not very keen to do and to rethink everything to maybe change my
    decision.\r\n\r\nThe only way out that I see is to open up the review process.
    At least the reviewers should not be able to hide and be forced to stand to their
    decisions.\r\n\r\nDisclaimer: I am not a reviewer for NIPS, but have reviewed
    for quite a lot of other conferences and journals."
- id: 5784
  author: orzuk
  author_email: orzuk@broad.mit.edu
  author_url: ''
  date: '2014-12-16 01:39:14 -0800'
  date_gmt: '2014-12-16 09:39:14 -0800'
  content: "Interesting analysis. \r\n\r\nShameless plug: A long time ago we calculated
    the overlap in top-k lists (i.e. 'accepted papers') in a very similar model as
    a function of variance between items (e.g. papers 'true' score) and variance in
    their assessment (e.g. 'between reviewers')\r\nin a paper, which as far as I remember
    was rejected by NIPS ..\r\nhttp://pluto.huji.ac.il/~orzu/publications/uai_ranking_2007_06_25.pdf"
- id: 5785
  author: 'Fairly interesting reflections on peer reviewing: &#8220;The NIPS Experiment&#8221;
    | Thomas Heide Clausen'
  author_email: ''
  author_url: http://www.thomasclausen.net/fairly-interesting-reflections-on-peer-reviewing-the-nips-experiment/
  date: '2014-12-16 02:26:17 -0800'
  date_gmt: '2014-12-16 10:26:17 -0800'
  content: '[&#8230;] Not sure to which degree these observations on the academic
    review process generalize, but they are interesting all the same: http://mrtz.org/blog/the-nips-experiment/.
    [&#8230;]'
- id: 5787
  author: The NIPS Experiment | Inverse Probability
  author_email: ''
  author_url: http://inverseprobability.com/2014/12/16/the-nips-experiment/
  date: '2014-12-16 04:23:44 -0800'
  date_gmt: '2014-12-16 12:23:44 -0800'
  content: '[&#8230;] There was also an amount of debate at the conference about what
    the results mean, a few attempts to answer this question (based only on the inconsistency
    score and the expected accept rate for the conference) are available here in this
    little Facebook discussion and on this blog post. [&#8230;]'
- id: 5788
  author: lawrennd
  author_email: lawrennd@gmail.com
  author_url: http://inverseprobability.wordpress.com
  date: '2014-12-16 04:39:29 -0800'
  date_gmt: '2014-12-16 12:39:29 -0800'
  content: "Hi,\r\n\r\nJust to confirm that Corinna and I will be releasing a full
    analysis of the experiment and our conclusions in due course. \r\n\r\nIt's great
    that the preliminary results of the experiment are already triggering so much
    interest. Many of you many will already know that we've been very open with our
    approach to the reviewing process throughout the conference. \r\n\r\nSince some
    of the speculation about the full results is missing links to the background (and
    some of the other speculation) I've added a quick blog post on the background
    here:\r\n\r\nhttp://inverseprobability.com/2014/12/16/the-nips-experiment/\r\n\r\nNeil"
- id: 5789
  author: koala
  author_email: koala@post.com
  author_url: ''
  date: '2014-12-16 05:20:12 -0800'
  date_gmt: '2014-12-16 13:20:12 -0800'
  content: How did you calculate the confidence interval?
- id: 5790
  author: Grigory Yaroslavtsev
  author_email: grigory@grigory.us
  author_url: http://grigory.us
  date: '2014-12-16 05:35:08 -0800'
  date_gmt: '2014-12-16 13:35:08 -0800'
  content: Yes, exactly, that's what I meant.
- id: 5791
  author: Stephen Borstelmann (@drsxr)
  author_email: drsxr@twitter.example.com
  author_url: http://twitter.com/drsxr
  date: '2014-12-16 05:35:16 -0800'
  date_gmt: '2014-12-16 13:35:16 -0800'
  content: I am so sorry to ask this but how did you do those lovely graphs?  Haven't
    seen that before!
- id: 5793
  author: Sam Wang
  author_email: sswang@princeton.edu
  author_url: https://www.facebook.com/braingeek
  date: '2014-12-16 06:28:48 -0800'
  date_gmt: '2014-12-16 14:28:48 -0800'
  content: This is an interesting analysis - as a computational data type, I am always
    glad to see a critical eye turned to peer review. I wonder if it's possible to
    see the detailed data set. Or, if not, are you willing to make a scatter plot
    where Xaxis=mean review score, Yaxis=sigma, and different symbols for both-accept,
    both-reject, and one-accept-one-reject?
- id: 5794
  author: Boaz Barak
  author_email: blog@boazbarak.org
  author_url: http://www.boazbarak.org
  date: '2014-12-16 06:38:09 -0800'
  date_gmt: '2014-12-16 14:38:09 -0800'
  content: "At some point I plan to write down some of the conclusions I had from
    my experience as FOCS PC chair, but theory conferences are a very different beast
    than NIPS. For starters, it's a completely different scale - we had ~270 submissions
    out of each we accepted ~70 papers, where NIPS had ~1700 submissions out of each
    ~400 were accepted. \r\nThe smaller scale means that we were able to do manually
    a lot of the things that are delegated or automated at NIPS. \r\n\r\nFor example,
    I (and many of the previous FOCS/STOC PC chairs) manually assigned all papers
    to reviewers. Every paper that was accepted (and many that weren't) was discussed
    in the physical PC meeting.  I don't know how it worked with NIPS, but our use
    of the reviewing scores was fairly limited. The scores were mostly used for initial
    filtering, but once papers got through that, we tended to have a more qualitative
    discussion on it. Certainly there was no score threshold for a paper to be automatically
    accepted. I didn't try to analyze this but I don't think the average score (or
    even the confidence weighed average) was a particularly good predictor for acceptance,
    perhaps the maximum score would have been a better one. All of these things are
    simply not possible in a conference at the scale of NIPS. \r\n\r\nI don't know
    if running an experiment like that for FOCS/STOC is possible. For many theory
    papers, there are 5-10 people that are truly the top experts in this field and,
    if the PC is doing its job, are very likely to be asked to review the paper. So
    you would very likely have many collisions, with the same reviewer getting asked
    to review the paper from the two different PC's. (The latter is also one of the
    reasons why I don't think double blind reviewing is a good idea for theory conference,
    but this deserves a separate discussion.) \r\n\r\nOne way to analyze randomness
    is to check the fraction of resubmissions from prior conference that are accepted.
    In FOCS we had 60 papers that were resubmitted from a prior conference, 14 of
    which were accepted (~23% rate as opposed to %25 in general) . I took a brief
    look at the reviews for these 14 submissions and noted that 6 of those the reviewers
    noted significant changes from the prior version. Perhaps the theory community
    can try to do a more serious study of this question.\r\n\r\nAbout your last note
    that \"we should rethink the importance we give [conferences] in terms of the
    job search, tenure process\". I actually don't believe they are as important as
    you think. I believe scanning the publication list for familiar venues might serve
    as an initial filtering mechanism for candidates you don't know. But when you
    start to seriously evaluate a candidate, you look at the actual work they've done,
    based on your and the reference letter writers' assessment, so you care more about
    what the work was than where it appeared. At least this has been the case for
    all institutions I was involved in.\r\n\r\nI'm not saying publishing in a good
    venue is not important. It gets your work noticed, which could open up possibilities
    for future impact and collaboration, which in turn will affect your prospects
    for hiring and promotion. It's just (in my experience) not used as strongly as
    a direct input in the hiring/promotion process itself as you portray it."
- id: 5795
  author: SaMat
  author_email: matt2@virgilio.it
  author_url: ''
  date: '2014-12-16 07:36:38 -0800'
  date_gmt: '2014-12-16 15:36:38 -0800'
  content: 'this might help: http://www.walkingrandomly.com/?p=4731'
- id: 5796
  author: Adam Smith
  author_email: adamdavisonsmith@gmail.com
  author_url: http://www.cse.psu.edu/~asmith
  date: '2014-12-16 07:51:42 -0800'
  date_gmt: '2014-12-16 15:51:42 -0800'
  content: "From my experience running and serving on PC's, the noisy scoring model
    seems like a good first-order approximation. \r\n\r\nThe only term I would add
    to the model is that the variance of the reviews varies based on the *type* of
    paper. Papers with a well-defined contribution in a well-established area tend
    to have little variance, since it is easy enough to judge the magnitude of the
    increment over previous work. Papers establishing a new model, or papers that
    live at the intersection of a few fields tend to get much higher variance. \r\n\r\n\r\nBoaz
    wrote:\r\n&gt; I believe scanning the publication list for familiar venues might
    serve as an initial filtering mechanism for candidates you don’t know. But when
    you start to seriously evaluate a candidate, you look at the actual work they’ve
    done, [...]\r\n\r\nThis procedure only works in areas where your institution already
    has significant expertise. When hiring someone in an area where your department
    or group has less representation, you have to use other signals. The best signals
    are opinions solicited from outside experts, but I think that publication history
    ends up also playing a role, if only subconsciously. \r\n\r\nMore generally, despite
    their best intentions to judge only based on quality, committees and individuals
    often end up taking the easy route and using an available proxy (publication record)
    instead of the real thing. Raising awareness of just how bad a signal publication
    record is seems like a worthy exercise."
- id: 5798
  author: Eric Price
  author_email: ecprice@gmail.com
  author_url: ''
  date: '2014-12-16 08:11:17 -0800'
  date_gmt: '2014-12-16 16:11:17 -0800'
  content: "Yeah.  In python/matplotlib, just run\r\n\r\n<code>&gt;&gt;&gt; pylab.xkcd()</code>\r\n\r\nbefore
    the regular plotting code.  It's the recommended style for Moritz's blog. =)"
- id: 5799
  author: Eric Price
  author_email: ecprice@gmail.com
  author_url: ''
  date: '2014-12-16 08:21:58 -0800'
  date_gmt: '2014-12-16 16:21:58 -0800'
  content: "That's a good question, and I'm not sure I did it right.  I just used
    a poisson approximation and did\r\n\r\n&gt;&gt;&gt; scipy.stats.poisson.interval(0.95,
    42)\r\n\r\nthen converted from (number of papers) to (percentage of accepted papers).
    \ You can shave a couple percentage points off using a binomial instead of poisson,
    but that's probably swamped by the modeling assumptions for the calculation.\r\n\r\nThis
    model is that each paper was independently and equally likely to appear in the
    discrepancy.  Independence seems reasonable, and while equal probability isn't
    very reasonable I think it maximizes the variation."
- id: 5800
  author: Eric Price
  author_email: ecprice@gmail.com
  author_url: ''
  date: '2014-12-16 08:24:14 -0800'
  date_gmt: '2014-12-16 16:24:14 -0800'
  content: Once they release the full data, I'll definitely look at it in more detail.
- id: 5801
  author: koala
  author_email: koala@post.com
  author_url: ''
  date: '2014-12-16 08:32:42 -0800'
  date_gmt: '2014-12-16 16:32:42 -0800'
  content: "Thanks for the answer. Yes, when I used binomial confidence intervals,
    \r\n\r\np = 0.56\r\ntmp = 1.96*np.sqrt((1/42.)*p*(1-p))\r\nprint p-tmp, p+tmp\r\n\r\nI
    got \r\n\r\n40%-71%\r\n\r\nBut your approach makes sense as well."
- id: 5802
  author: しましま (@shima__shima)
  author_email: shima__shima@twitter.example.com
  author_url: http://twitter.com/shima__shima
  date: '2014-12-16 08:38:36 -0800'
  date_gmt: '2014-12-16 16:38:36 -0800'
  content: "Some related information related to NIP2014 experiments:\r\n- Conference
    paper selectivity and impact http://dx.doi.org/10.1145/1743546.1743569 --- if
    acceptance ratio is less than 15%, innovative papers may be rejected\r\n- ICDE2010:
    DBMS: Lessons from the First 50 Years, Speculations for the Next 50 http://www.slideshare.net/zukun/icde2010-dbms-lessons-from-the-first-50-years-speculations-for-the-next-50
    --- from P41\r\n- What's wrong with STOC/FOCS? http://www.wisdom.weizmann.ac.il/~oded/on-stocfocs.html\r\n-
    Novel Tools To Streamline the Conference Review Process: Experiences from SIGKDD09
    http://dx.doi.org/10.1145/1809400.1809413"
- id: 5803
  author: Eric Price
  author_email: ecprice@gmail.com
  author_url: ''
  date: '2014-12-16 08:43:23 -0800'
  date_gmt: '2014-12-16 16:43:23 -0800'
  content: "I guess I think double-blind reviewing is imperfect, but better than the
    alternative.  While it's true that the reviewer will be aware of the authorship
    of many submissions, they also won't be aware of the authorship of many good submissions
    -- lots of established researchers are slow to put stuff online.\r\n\r\nI suspect
    this gives a large increase to the chance that a paper from Podunk U gets a fair
    hearing.  Maybe I'm overestimating the effect here, though, since a lot of the
    bias comes from other factors, like outsiders not knowing the conventional language.\r\n\r\nI
    don't think your worry (1) is reasonable, in that I think a reviewer acting in
    bad faith is exceedingly rare.\r\n\r\nYour point (2) is an interesting one, and
    relates to David Karger's point that we deal with randomness through repeated
    trials.  The rebuttal phase is kind of like resubmitting to the next conference:
    it's faster and takes less reviewer effort, but also gives less independence.
    \ I hadn't thought of it that way, and I'm not sure whether the tradeoff is good."
- id: 5804
  author: Moritz Hardt
  author_email: m@mrtz.org
  author_url: ''
  date: '2014-12-16 08:50:34 -0800'
  date_gmt: '2014-12-16 16:50:34 -0800'
  content: I just think no plot should ever be taken for face value. It's just one
    way of looking at a broader phenomenon and tends to distract from what is usually
    more important, e.g., the methodology. In a sense all plots are just cartoons.
    XKCD is a great way of making that point.
- id: 5805
  author: Eric Price
  author_email: ecprice@gmail.com
  author_url: ''
  date: '2014-12-16 08:53:33 -0800'
  date_gmt: '2014-12-16 16:53:33 -0800'
  content: "That's great to hear, Neil!  This whole post is based on like five numbers
    from your presentation, so I'm looking forward to getting more data. =)\r\n\r\nThe
    prediction market is interesting, but I'm not sure what to make of it -- a large
    fraction of the predictions are mathematically impossible.  This suggests a lot
    of forecasters didn't understand the question, so I don't know whether anything
    meaningful can be extracted."
- id: 5806
  author: Tanvir Amin
  author_email: tanviralamin@gmail.com
  author_url: http://tanviramin.com
  date: '2014-12-16 08:57:21 -0800'
  date_gmt: '2014-12-16 16:57:21 -0800'
  content: "The problem a review committee is solving is \"estimating\" the quality
    of the submitted papers. It is highly likely that the actual qualities has a power
    law distribution, and in that case the randomness is probably an effect of that.\r\n\r\nA
    small fraction of the submitted papers are very high quality. A smaller number
    of review samples are enough to confidently filter those in. In this zone, the
    larger spacing in quality difference from paper to paper also allows a higher
    measurement error without harm. \r\n\r\nAs we go down the knee of the distribution,
    its a crowded zone with many papers having very similar quality value. It is hard
    to differentiate between those as the sequence can look like 6.124, 6.122, 6.117,
    6.114, 6.113 and a slight error is enough to change the ranking. \r\n\r\nIf the
    10% papers under the experiment all received the same number of reviews (measurement
    samples), this outcome is likely. For ordinary papers, we actually need many more
    review samples to be confident about the estimated quality scores, or the error
    in measurement will change the ranking, and show up as \"randomness of the committee\"."
- id: 5808
  author: same here
  author_email: same@here.yu
  author_url: ''
  date: '2014-12-16 09:41:34 -0800'
  date_gmt: '2014-12-16 17:41:34 -0800'
  content: "\"I suspect this gives a large increase to the chance that a paper from
    Podunk U gets a fair hearing.\"\r\n\r\nIt does. This is well known and documented
    when SIGMOD went to double blind reviews. \r\n\r\nAlso experiments have been run
    on how often one can guess authorship and it was somewhere around 30-50% of the
    time, which means at least the other 50% get a fair sharing. Moreover, when you
    guess correctly there is no confirmation of this fact, so during the reviewing
    you are always hesitating if your guess is correct.\r\n\r\nLastly as you point
    out, the claim isn't that double blind is perfect, rather that is better than
    single blind. \r\n\r\ntl;dr  the points brought up by Ingo all have been refuted
    with experiments."
- id: 5809
  author: Eric Price
  author_email: ecprice@gmail.com
  author_url: ''
  date: '2014-12-16 09:49:11 -0800'
  date_gmt: '2014-12-16 17:49:11 -0800'
  content: Interesting! Do you have references for those experiments?
- id: 5810
  author: same here
  author_email: same@here.yu
  author_url: ''
  date: '2014-12-16 10:45:26 -0800'
  date_gmt: '2014-12-16 18:45:26 -0800'
  content: "Samuel Madden and David DeWitt. 2006. Impact of double-blind reviewing
    on SIGMOD publication rates. SIGMOD Rec. 35, 2 (June 2006), 29-32. DOI=10.1145/1147376.1147381
    http://doi.acm.org/10.1145/1147376.1147381 \r\n\r\nRichard Snodgrass. 2006. Single-
    versus double-blind reviewing: an analysis of the literature. SIGMOD Rec. 35,
    3 (September 2006), 8-21. DOI=10.1145/1168092.1168094 http://doi.acm.org/10.1145/1168092.1168094\r\n\r\nShawndra
    Hill and Foster Provost. 2003. The myth of the double-blind review?: author identification
    using only citations. SIGKDD Explor. Newsl. 5, 2 (December 2003), 179-184. DOI=10.1145/980972.981001
    http://doi.acm.org/10.1145/980972.981001\r\n\r\nAnja Feldmann. 2005. Experiences
    from the Sigcomm 2005 European shadow PC experiment. SIGCOMM Comput. Commun. Rev.
    35, 3 (July 2005), 97-102. DOI=10.1145/1070873.1070889 http://doi.acm.org/10.1145/1070873.1070889"
- id: 5811
  author: same here
  author_email: same@here.yu
  author_url: ''
  date: '2014-12-16 11:06:49 -0800'
  date_gmt: '2014-12-16 19:06:49 -0800'
  content: "\"Papers with a well-defined contribution in a well-established area tend
    to have little variance, since it is easy enough to judge the magnitude of the
    increment over previous work. Papers establishing a new model, or papers that
    live at the intersection of a few fields tend to get much higher variance. \"
    \r\n\r\nThis was my experience. My modest increments in well established problems
    got accepted without incident, while the rare breakthroughs that altered the landscape
    were routinely rejected, for example a paper that is now in the top 2% by citations
    in one of the top CS conferences was rejected three times prior. \r\n\r\nWe also
    know of many cases like Eric's where papers went from the reject pile to the best
    paper award pile. I know from first hand accounts of at least six such cases.
    This tell us something above and beyond the data above: the magnitude of the random
    noise in the quality measure can be very large."
- id: 5813
  author: Boaz Barak
  author_email: blog@boazbarak.org
  author_url: http://www.boazbarak.org
  date: '2014-12-16 12:49:29 -0800'
  date_gmt: '2014-12-16 20:49:29 -0800'
  content: Adam, I completely agree with your statement that raising awareness of
    how bad publications are as a signal is a worthy exercise. Thus, I think it's
    great that NIPS ran this experiment and that Eric wrote up this blog post.
- id: 5814
  author: Avan Suinesiaputra (@asui085)
  author_email: asui085@twitter.example.com
  author_url: http://twitter.com/asui085
  date: '2014-12-16 13:12:54 -0800'
  date_gmt: '2014-12-16 21:12:54 -0800'
  content: I really love your graph. How did you make it looks like doodling? And
    are these experimental data open for public use? Would it interesting to analyse
    it.
- id: 5816
  author: Gregory Murphy
  author_email: gregory.l.murphy@gmail.com
  author_url: ''
  date: '2014-12-16 15:02:28 -0800'
  date_gmt: '2014-12-16 23:02:28 -0800'
  content: "The example of your SODA award-winning paper is a good one, but it isn't
    clear where the error lies: It could be in the three rejections or in the award.
    Given the replication of rejections, one might argue that the award process is
    the unreliable process (sorry!). And the criteria for the award might not be the
    same for conference acceptance (e.g., greater weight on creativity or author independence).
    It may be wrong to think that everything is graded on a single quality scale.\r\n\r\nNone
    of this denies the basic variability of all these judgments that your blog reveals."
- id: 5819
  author: David Meyer
  author_email: dmeyer@math.ucsd.edu
  author_url: ''
  date: '2014-12-16 16:27:03 -0800'
  date_gmt: '2014-12-17 00:27:03 -0800'
  content: Regarding Boaz' statement that conferences are not as important as Eric
    thinks, I've heard top theory faculty members say that a student would not get
    a faculty position because he had not published in STOC or FOCS.  Perhaps that
    was shorthand for the quality of the work itself, but I don't think so since he
    had published in CCC.
- id: 5821
  author: Hal Daume III
  author_email: haldaume3@gmail.com
  author_url: ''
  date: '2014-12-16 17:23:47 -0800'
  date_gmt: '2014-12-17 01:23:47 -0800'
  content: 'hmmmm... small request: given that this post is getting so much circulation
    outside the nips community, and given that most people don''t read costs or Twitter
    or facebook and given that it''s factually flawed in ways that have been pointed
    out here and on Twitter and Facebook, I (and I imagine many others) would really
    appreciate if an edit were put at the top that said something like: "this post
    describes an analysis of a process somewhat like the nips experiment but not exactly
    that experiment. if you want to know about the *actual* nips experiment please
    wait for Neil and Corinna to post what actually happened."'
- id: 5822
  author: Tom
  author_email: tom@dmw.fr
  author_url: ''
  date: '2014-12-16 18:08:17 -0800'
  date_gmt: '2014-12-17 02:08:17 -0800'
  content: 'Out of topic question: did you hand draw the graphs? If not what did you
    use? I like the ''xkcd'' like drawings.'
- id: 5823
  author: ctwardy
  author_email: ctwardy@alumni.iu.edu
  author_url: http://blog.scicast.org
  date: '2014-12-16 19:30:27 -0800'
  date_gmt: '2014-12-17 03:30:27 -0800'
  content: "Two things at least:  (1) A lot of people really *didn't* understand the
    question or know what to expect: that's important information, esp. as I suspect
    most of our new forecasters came from the UAI list; (2) Despite the noise, the
    central tendency (driven in large part by experienced forecasters) wasn't too
    bad.  An active market should tolerate or even thrive on noise. \r\n\r\nAlso,
    the comments show a large range of opinions.  Market aside, that's a handy record
    that's unavailable after the answer becomes what everyone knew all along."
- id: 5825
  author: namvo
  author_email: nam.poke@gmail.com
  author_url: http://namvo.wordpress.com
  date: '2014-12-16 20:51:33 -0800'
  date_gmt: '2014-12-17 04:51:33 -0800'
  content: '"The committees did not know which of the ~900 papers they were reviewing
    were the 166 duplicated ones, so there can be some variation in how many papers
    to accept, but this is a minor effect." -&gt; Shouldn''t this effect significant.
    This becomes obvious if we scale the number up: each committee review about 9mil
    papers, the number of duplicated ones is say 16. In such case, the number of accepted
    papers agreed by 2 committees would approach 22.5% * 22.5% * 16'
- id: 5826
  author: Moritz Hardt
  author_email: m@mrtz.org
  author_url: ''
  date: '2014-12-16 21:02:42 -0800'
  date_gmt: '2014-12-17 05:02:42 -0800'
  content: Must be missing something. How is it "factually flawed"?
- id: 5829
  author: Sasho Nikolov
  author_email: anikolov@cs.rutgers.edu
  author_url: https://paul.rutgers.edu/~anikolov
  date: '2014-12-16 22:16:01 -0800'
  date_gmt: '2014-12-17 06:16:01 -0800'
  content: '"Most people don''t read twitter", do you mean of those born before 1924?'
- id: 5830
  author: juanpiblogjuanpi
  author_email: ajuanpi@gmail.com
  author_url: http://gravatar.com/juanpiblog
  date: '2014-12-16 23:00:55 -0800'
  date_gmt: '2014-12-17 07:00:55 -0800'
  content: "Since you are raising the point of \"how to view things\" there is another
    important aspect at the moment of defining perspective. There is not such a thing
    as an absolute measure for the quality of a paper. \r\nOne way of viewing at these
    results is to accept the fact that what is trash for somebody is treasure for
    another, and quality is just a matter of convention.\r\nI guess the noisy model
    somehow captures this better.\r\n\r\nAnother human aspect is the fact that when
    a person is given a scale, although the scale might be linear, their appreciation
    of the paper might not. That is, when is 6 a 6? Have been this scales been tested
    for consistency across subjects? I doubt it, but maybe took the pain of doing
    that. I guess this will just introduce another level of noise in the models.\r\n\r\nAdministrative
    people like to put everything in numbers, in the hope that this will make things
    more objective. I like numbers too, but meaningful ones. I think they are just
    dressing up subjectivity with a number that allows them to divisive themselves
    into thinking that the measure is objective. \r\n\r\nHurra! for the NIPS people
    who push forward this experiment!\r\n\r\nPersonally, I still think that better
    than scales are the comments given by the reviewers. In that way a committee can
    spot lazy reviews as well. That is, who is evaluating the evaluators? :D another
    dilemma. The same should be applied to evaluation of professionals based on their
    publication list: you want to evaluate a person, then read the papers, talk to
    them. Counting publication and weighting them with the *perceived* value of a
    conference/journal is hardly satisfactory and has the huge detrimental effect
    of the self-fulfilling prophecy.\r\n\r\nWe have to accept that reviewing an article
    is, and should be, a human activity. It is of course guided and supported by a
    scientific education (which is getting thinner every year...), but at the end
    of the line there is a person with interests, moods, external pressures, etc...\r\nWe
    need tools to support this human activity and not strive to dehumanize the activity
    to use the current tools we have."
- id: 5831
  author: Ravee
  author_email: ravmalla@gmail.com
  author_url: ''
  date: '2014-12-16 23:07:11 -0800'
  date_gmt: '2014-12-17 07:07:11 -0800'
  content: "Thanks for the detailed analysis, it is very interesting. It made me think
    that we can probably say something that makes about your argument of &gt;57% of
    accepted papers being random even stronger.\r\n\r\nAssume that for the 43 papers
    that had opposite opinions by committees A and B, A had accepted x. Then, B accepted
    43-x. The final list of ~38/166 accepted papers can either come from these 43
    papers or from the remaining 166-43 where both A and B agreed.\r\n\r\nThe rate
    of disagreement on accepted papers between A and B is (max(x, 43-x) / 38). This
    function is at least 57% as in your example when x=21. The best case is a scenario
    where neither A nor B is more inclined to accept or reject a given paper i.e.
    for a paper where A and disagree, A is equally likely to accept or reject. In
    other cases, the randomness is even higher."
- id: 5833
  author: Eric Price
  author_email: ecprice@gmail.com
  author_url: ''
  date: '2014-12-16 23:22:38 -0800'
  date_gmt: '2014-12-17 07:22:38 -0800'
  content: "I actually do take the effect into account in the plots for the messy
    middle and noisy scoring model.  The simplification is just for the explanation
    of how 25.9% of submissions turns into about 57% of accepted papers.\r\n\r\nIt's
    a minor effect because 166 is a decent fraction of 900.  The median difference
    in number of papers accepted will be 2 (out of about 37).  And the effect of this
    variation on the 57% number is that it becomes smaller for one committee's list,
    larger for the other committee's list, and actually slightly higher than 57% on
    average.  (Although I think the proper thing to do is weight the average by size
    of the corresponding list, which brings you back to 57%.)"
- id: 5834
  author: Eric Price
  author_email: ecprice@gmail.com
  author_url: ''
  date: '2014-12-16 23:23:59 -0800'
  date_gmt: '2014-12-17 07:23:59 -0800'
  content: "The XKCD-style plots are made using pylab.xkcd() before running the regular
    matplotlib plotting commands.\r\n\r\nI don't have the experimental data yet, only
    the summary statistics.  However, Neil and Corinna (the NIPS organizers) have
    said that they will eventually release it for us to study."
- id: 5835
  author: Eric Price
  author_email: ecprice@gmail.com
  author_url: ''
  date: '2014-12-16 23:30:43 -0800'
  date_gmt: '2014-12-17 07:30:43 -0800'
  content: "You're definitely right about my paper.  The process for choosing best
    papers might well be noisier than the general review process, since you're picking
    only one paper.   (Particularly if you include the variation from \"will my awesome
    paper collide with another awesome paper\".)  And the best _student_ paper is
    particularly noisy in theory conferences, where it must be written solely by students
    and very few papers qualify.\r\n\r\nAnother point about rejected papers that do
    well in later rounds is that they often do improve over time, even if the core
    of the paper doesn't change much.  Revising the introduction to address reviewer
    confusion may significantly improve the impact of the paper, because if reviewers
    are confused than future readers likely will be as well."
- id: 5836
  author: Eric Price
  author_email: ecprice@gmail.com
  author_url: ''
  date: '2014-12-16 23:51:50 -0800'
  date_gmt: '2014-12-17 07:51:50 -0800'
  content: "This post does describe the actual nips experiment.  With the full data
    we'll be able to do a more refined analysis, but the data released so far is enough
    to reject (say) a null hypothesis that the inconsistency rate is below 40% of
    accepted papers.\r\n\r\nIf you let me know any factual errors, I'll be happy to
    correct them."
- id: 5838
  author: koala
  author_email: koala@post.com
  author_url: ''
  date: '2014-12-17 00:14:42 -0800'
  date_gmt: '2014-12-17 08:14:42 -0800'
  content: That is a good viable explanation - I wonder though if top papers are chosen
    / agreed upon easily because, even the process is blind, the reviewers can tell
    the author is top honcho (known in the field), because the subject area is familiar,
    the approach is similar etc. Then there would an unfair bias, which would make
    it harder for an up-and-coming author / idea to break through.
- id: 5839
  author: Djamé
  author_email: djame.seddah@gmail.com
  author_url: ''
  date: '2014-12-17 00:41:06 -0800'
  date_gmt: '2014-12-17 08:41:06 -0800'
  content: yep, I'd love to hear too. I've seen some posts on twitter telling that
    it contains flaws but none of them explained and all pointing to an upcoming post
    by the original authors.
- id: 5841
  author: Exceptional papers do not need exceptional journals | Forest Vista
  author_email: ''
  author_url: http://majesticforest.wordpress.com/2014/12/17/exceptional-papers-do-not-need-exceptional-journals/
  date: '2014-12-17 01:09:05 -0800'
  date_gmt: '2014-12-17 09:09:05 -0800'
  content: '[&#8230;] the best controlled experiment that I know of on the consistency
    of peer-review has found that one of the most prestigious and double&#8211;blind
    publication venue is more more [&#8230;]'
- id: 5843
  author: Arnaldo
  author_email: arnaldo.spalvieri@polimi.it
  author_url: ''
  date: '2014-12-17 03:25:50 -0800'
  date_gmt: '2014-12-17 11:25:50 -0800'
  content: "I support the noisy score model, but the mean value of the noise should
    depend on the reviewer, meaning that some reviewers hare harsher than others.
    Details about this model can be found in the recent paper entitled ''Weighting
    Peer Reviewers'' by Spalvieri, Mandelli,Magarini; Bianchi, PST 2014, Toronto,
    CA, http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=6890969\r\nEric, let
    me have the data set, I can try to work out mean and variance of reviewers!"
- id: 5845
  author: Eric Price
  author_email: ecprice@gmail.com
  author_url: ''
  date: '2014-12-17 03:54:35 -0800'
  date_gmt: '2014-12-17 11:54:35 -0800'
  content: "Yeah, Boaz, you might be right that the indirect benefits of top publications
    outweigh the direct benefits, particularly for your first few publications.  But
    this actually seems more troubling, because those benefits are huge and it's harder
    to correct for this randomness.\r\n\r\nAnd I think much of the indirect benefit
    is not exactly from getting \"your work\" noticed, but from getting _you_ noticed.
    \ Having a STOC/FOCS paper gives you credibility with people who don't have time
    to read your papers, i.e. almost everyone.  This then helps you get internships,
    collaborations, lunch at the cool kids table, etc.\r\n\r\nSo even if faculty hiring
    committees have the time to understand a candidate's work in depth (which other
    commenters say is often not true), the signal still contains a lot of randomness
    from the review process."
- id: 5846
  author: Eric Price
  author_email: ecprice@gmail.com
  author_url: ''
  date: '2014-12-17 04:07:56 -0800'
  date_gmt: '2014-12-17 12:07:56 -0800'
  content: "I don't have the data set yet!  All I have is a few numbers from the summary
    described in a presentation at the beginning of NIPS.\r\n\r\nThat paper has an
    interesting model, but unfortunately I'm not sure you'll be able to run it on
    the data set once it's released.  They are going to anonymize it, and I don't
    know if they will preserve the information about which reviews are by the same
    reviewer."
- id: 5848
  author: lawrennd
  author_email: lawrennd@gmail.com
  author_url: http://inverseprobability.wordpress.com
  date: '2014-12-17 05:22:40 -0800'
  date_gmt: '2014-12-17 13:22:40 -0800'
  content: "I think there are a lot of good comments in the prediction market, and
    knowing people's prior views is interesting. With regard to some of the more wayward
    predictions, I think some of them are made by scripts which are hedging the market,
    and some clearly didn't understand the question. \r\n\r\nHowever, many predictions
    were very reasonable and were made by people with a lot of experience of the field.
    Peter Grunwald who has program chaired UAI predicted 25%. Pieter Abbeel makes
    some nice comments about what the numbers should mean and others chip in with
    some very sensible observations.\r\n\r\nWe could perhaps have asked for people
    to estimate another figure (such as the figure estimated by you above and separately
    by Zoubin &amp; Joaquin on my Facebook post) but I'm not sure that people would
    have understood that question in the prediction market any better! \r\n\r\nInterestingly,
    there were lots of comments about which figures people *really* care about. I
    think the figure you care about depends on what you are doing: submitting a paper,
    attending the conference etc. \r\n\r\nSo far we've released only the inconsistency
    figure. We could have released more---I was planning a preconference write up
    but was delayed due to illness---but for the moment I think it's interesting to
    see the speculation (some of which is pretty accurate) about what the other figures
    are and what it all means. It shows that our community is really thinking about
    it and that is what's really important."
- id: 5849
  author: lawrennd
  author_email: lawrennd@gmail.com
  author_url: http://inverseprobability.wordpress.com
  date: '2014-12-17 05:35:03 -0800'
  date_gmt: '2014-12-17 13:35:03 -0800'
  content: "Having done AISTATS in 2012 which had 400 submissions, I agree that scaling
    things up does change the process. However, we worked very hard to ensure that
    papers were given as much consideration as they would be at a smaller conference.
    \r\n\r\nAll accepted papers were discussed over the video conferences, although
    more time was spent on those near the decision boundary (including those that
    fell below it). \r\n\r\nScores weren't the only determinator of whether a paper
    was accepted, but there was a broad expectation that area chairs would be calibrated
    against the probabilities of accept we provided (which were based on scores being
    fed into a reviewer calibration model). \r\n\r\nArea Chairs were given a running
    update over several weeks where their papers were in the global calibration, and
    they were encouraged to obtain additional reviews or offer their own detailed
    opinion (as a review) if they disagreed with the paper's current position. All
    this was done within the framework of open discussion amongst the reviewers. \r\n\r\nIn
    the end some papers which seemed to have a high probability of accept were rejected,
    and some with a low probability of accept did get in.\r\n\r\nArea chairs were
    given access to automated warning scores and reports that highlighted papers with
    shorter reviews, low confidence reviews and those around the decision boundary.
    \r\n\r\nAll these details and more (including the software written for doing the
    above) are linked from the post below.\r\n\r\nhttp://inverseprobability.com/2014/12/16/the-nips-experiment/"
- id: 5850
  author: lawrennd
  author_email: lawrennd@gmail.com
  author_url: http://inverseprobability.wordpress.com
  date: '2014-12-17 06:26:19 -0800'
  date_gmt: '2014-12-17 14:26:19 -0800'
  content: "We already calibrate reviews at NIPS and have done since 2002.  Please
    see this blog post:\r\n\r\nhttp://inverseprobability.com/2014/08/02/reviewer-calibration-for-nips/\r\n\r\nLast
    year's calibration process is also implemented in an IPython notebook available
    here:\r\n\r\nhttp://nbviewer.ipython.org/github/sods/conference/blob/master/Reviewer%20Calibration.ipynb\r\n\r\nIt
    is this sort of context that we hope to place in the our write up of the experiment."
- id: 5851
  author: Boaz Barak
  author_email: blog@boazbarak.org
  author_url: http://www.boazbarak.org
  date: '2014-12-17 06:54:28 -0800'
  date_gmt: '2014-12-17 14:54:28 -0800'
  content: "This is the point of a conference (or a journal for that matter) announcing
    to the community what works are worth paying attention to. It may have a lot of
    randomness, but it seems to be the \"least bad option\".   Luckily, there are
    other ways to be noticed including arxiv, internet forums, talks, workshops, variety
    of conferences, etc.. \r\n\r\nI do think that even if it happens that one or two
    of your papers gets rejected through the inherent randomness in the process,  if
    you consistently do work that is interesting to some field X, then eventually
    the other people doing X will hear about it.  After all, it's in their interest
    to learn about the cool new work relevant to their field, and they are fully aware
    that they can't rely on the conferences alone to do that. Once you are known in
    your own subfield, with time you will also get known outside it. I think that
    most times the randomness in publication decisions has an effect on the speed
    of this process, but not as much on its final outcome."
- id: 5853
  author: The NIPS Experiment | Surviving Grad School
  author_email: ''
  author_url: https://guidetogradschoolsurvival.wordpress.com/2014/12/17/the-nips-experiment/
  date: '2014-12-17 08:06:37 -0800'
  date_gmt: '2014-12-17 16:06:37 -0800'
  content: '[&#8230;] this blog post has been floating around Facebook for the last
    couple of days. A guy talks about an experiment that [&#8230;]'
- id: 5854
  author: jsshapiro
  author_email: shap@eros-os.org
  author_url: ''
  date: '2014-12-17 09:23:28 -0800'
  date_gmt: '2014-12-17 17:23:28 -0800'
  content: "In systems, and I suspect in most areas, double blind reviewing is a delusion.
    The community of reviewers is small, and the interesting systems are too readily
    recognized by their designs for double-blind reviewing to be possible at all once
    the first paper on a system has been published. The net effect is single-blind
    reviewing, which in my experience fosters unethical reviewing practices.\r\n\r\nA
    professionally responsible reviewer will review fairly whether the review is blind
    or not. Less professional reviewers use the anonymization of reviews either to
    advance their research agenda by impeding others, or to issue unfounded rants
    and/or uninformed opinions that have no place in a review at all. The number of
    reviews I have seen that have dinged papers based on beliefs expressed by the
    reviewer that are flatly wrong has been astonishing and disheartening. Weak reviewers,
    when anonymous, appear less likely to offer constructive criticism. My opinions
    on this reflect my personal experience as an author, but also my experience and
    observations when serving on committees.\r\n\r\nAccountability is one of the hallmarks
    of proper science. I have long felt that anonymous reviews are unethical, and
    I have consequently insisted on performing my own reviews openly and with attribution.
    Whether my review is supportive or critical, I believe that I am accountable for
    my statements."
- id: 5856
  author: jsshapiro
  author_email: shap@eros-os.org
  author_url: ''
  date: '2014-12-17 09:27:34 -0800'
  date_gmt: '2014-12-17 17:27:34 -0800'
  content: The relative importance of conference and journal publications depends
    a lot on the sub-field. In systems, journal publications are effectively irrelevant
    because their review cycle is too long.
- id: 5860
  author: SB
  author_email: soheyl.b84@gmail.com
  author_url: ''
  date: '2014-12-17 10:59:04 -0800'
  date_gmt: '2014-12-17 18:59:04 -0800'
  content: Wouldn't it be better to analyze the data to see if there is any adversarial
    or "collusive" reviewership? For example, consider a directed bipartite graph
    with authors and reviewers as one partition and the papers as the other partition.
    The edges to and from each paper node, represent "written by" and "accepted by"
    relations, respectively. The size and the number of directed loops or complete
    bipartite subgraphs can be an indicator of biased reviews. I guess more information
    can be extracted by using a graph representation like this jointly with the observed
    data.
- id: 5861
  author: Eric Price
  author_email: ecprice@gmail.com
  author_url: ''
  date: '2014-12-17 11:24:57 -0800'
  date_gmt: '2014-12-17 19:24:57 -0800'
  content: I don't think that reviewers act in bad faith.  There probably are some
    groups that tend to like each other's work, and other groups that tend to dislike
    each other's work, but this bias is probably much weaker than the noise in the
    reviewing process.  Figuring it out would then require seeing how the groups review
    each other over many conferences.
- id: 5862
  author: Eric Price
  author_email: ecprice@gmail.com
  author_url: ''
  date: '2014-12-17 11:28:46 -0800'
  date_gmt: '2014-12-17 19:28:46 -0800'
  content: Yet another way in which NIPS is more advanced than TCS conferences, then.
- id: 5864
  author: same here
  author_email: same@here.yu
  author_url: ''
  date: '2014-12-17 13:20:03 -0800'
  date_gmt: '2014-12-17 21:20:03 -0800'
  content: "\"In systems, and I suspect in most areas, double blind reviewing is a
    delusion.\"\r\n\r\nAgain this has been convincingly disproven. First of all you
    can guess the group only to about 50% accuracy and no one rings a bell if you
    get it right, which means you always have the doubt. Second you still do not know
    which subset of the guessed group submitted the present paper.\r\n\r\nThird, we
    do not need double blind to work every time to be an improvement. For example,
    several double-blind conferences have no problem dealing with reviews where one
    has been able to guess who the authors are. One simply states at the top this
    fact so that the rest of the PC is aware of the situation.\r\n\r\n\"A professionally
    responsible reviewer will review fairly whether the review is blind or not. \"\r\n\r\nThis
    is the same nonsense that was said when medicine went to blind trials. \"Honest
    doctors do not need blind trials\". As it turned out unconscious bias was far
    more common and pernicious than conscious bias and medicine did need blind trials.\r\n\r\nI
    am in favor of eventually removing the anonymity veil from reviewers, after a
    sufficiently long period of time. I'm sure it would make reviewers word their
    comments more carefully and as pointed above, more constructively which is good
    for all parties concerned."
- id: 5865
  author: same here
  author_email: same@here.yu
  author_url: ''
  date: '2014-12-17 13:34:41 -0800'
  date_gmt: '2014-12-17 21:34:41 -0800'
  content: "\"I think that most times the randomness in publication decisions has
    an effect on the speed of this process, but not as much on its final outcome.\"\r\n\r\nI
    agree, but it can take decades before this happens. I can think of over a dozen
    persons like that. One of them is now a major award winner after many years of
    being relatively ignored, though certainly not unknown. Others were trend chasers
    with many papers in top conferences that today no one reads. Some of these you
    might have heard about, others are completely forgotten. \r\n\r\nLastly I can
    think of several people who solved/advanced a major open problem and did not get
    the respect they deserve because they were not already on the inside. In fact
    we have a recent case where two people independently co-discovered the same result
    and their sub-field apportioned the credit asymmetrically, in favor or the person
    who reached the goal last."
- id: 5866
  author: Ingo Keck
  author_email: ingokeck@ingokeck.de
  author_url: http://ingokeck.de
  date: '2014-12-17 14:24:02 -0800'
  date_gmt: '2014-12-17 22:24:02 -0800'
  content: It would be interesting to see if it is actually higher or lower than the
    "noise" down to different views on the submission quality. But apart from that
    I would simply concentrate to make the review process robust against it. Opening
    up the reviewers work obviously would be quite efficient.
- id: 5867
  author: Boaz Barak
  author_email: blog@boazbarak.org
  author_url: http://www.boazbarak.org
  date: '2014-12-17 14:28:37 -0800'
  date_gmt: '2014-12-17 22:28:37 -0800'
  content: "Lets try to separate two issues: one is the randomness in a conference
    selection process, which is the topic of this post. By this I mean the independent
    unbiased noise that is introduced by the choice of the particular program committee
    and the reviewers at that particular point in time. In particular, I think that
    in many reasonable noise models, if you resend the paper to the next conference,
    then this \"noise\" effect is equally likely to act in your favor. \r\n\r\nAnother
    issue is systematic bias, where a certain line of work may be under-appreciated
    by a whole community for a long time. Such examples certainly happen, and it is
    important as researchers for us to try to realize when they occur and bring to
    light these works. This is not just for the sake of recognizing the individuals,
    but more importantly, so their work can be used to progress science.\r\n\r\nSo
    I agree that such things are unfortunate, but this is not really an issue that
    can be fixed by the publication process. Even in the noiseless case, the program
    selection reflects the opinion of the community, and if the community doesn't
    appreciate the work, then it will not be accepted."
- id: 5868
  author: Ingo Keck
  author_email: ingokeck@ingokeck.de
  author_url: http://ingokeck.de
  date: '2014-12-17 14:40:25 -0800'
  date_gmt: '2014-12-17 22:40:25 -0800'
  content: "50% is far from blind. It is also much better than random (given that
    usually you have to choose from ca 5-10 possible groups where the article could
    come from). \r\n\r\nThere is no big sense in looking how honest reviewers react
    if they are able to estimate the correct author: Of course they will do the correct
    thing.\r\n\r\nIt is the not honest reviewers you need to take care of. Pseudo-blind
    authorship will not impede them, they probably even know all the submissions of
    their friends in advance and thus recognise them with 100% accurancy. And in case
    they fail, the rebuttal phase gives the chance to correct that.\r\n\r\nThe only
    way I see to end this game is to remove the anonymity of the reviewers. I personally
    have not problem with that."
- id: 5869
  author: Ingo Keck
  author_email: ingokeck@ingokeck.de
  author_url: http://ingokeck.de
  date: '2014-12-17 14:51:43 -0800'
  date_gmt: '2014-12-17 22:51:43 -0800'
  content: "(1) is based on my personal experience after working as reviewer and session
    organiser for the last 10 years. You need to design your review process to be
    robust against biased (or even malicious) reviewers. \r\n\r\n(2) is just common
    knowledge. A good review is a lot of work. 1 day if I check references and calculations.
    So far no-one has payed me anything for it. \r\n\r\nOpening up the reviews may
    even help getting more volunteers. Good reviews could be honoured, providing a
    direct incentive for the reviewers."
- id: 5870
  author: Eric Price
  author_email: ecprice@gmail.com
  author_url: ''
  date: '2014-12-17 14:57:03 -0800'
  date_gmt: '2014-12-17 22:57:03 -0800'
  content: "I guess one question is, to what extent does conference randomness govern
    the lifecycle of \"fad topics\"?  People often choose problems to work on by looking
    at recent conference proceedings or seeing interesting talks at conferences.  If
    this effect is strong and the noise in conference selection is strong, then randomness
    in the conference selection process could lead to long term variation in the perceived
    value of a body of work.\r\n\r\nFad topics are themselves detrimental to scientific
    progress, so it's worth trying to figure out what causes them and how to mitigate
    them."
- id: 5871
  author: biochemistries
  author_email: naivelocus@gmail.com
  author_url: http://biochemistries.wordpress.com
  date: '2014-12-17 14:58:28 -0800'
  date_gmt: '2014-12-17 22:58:28 -0800'
  content: The XKCD font on these graphs makes me feel like I'm losing my eyesight
    8-O Very interesting though!
- id: 5872
  author: same here
  author_email: same@here.yu
  author_url: ''
  date: '2014-12-17 15:02:33 -0800'
  date_gmt: '2014-12-17 23:02:33 -0800'
  content: "\"if you resend the paper to the next conference, then this “noise” effect
    is equally likely to act in your favor. \"\r\n\r\nBoaz, your comment is quasi-circular.
    Essentially you are saying: \"if we remove systemic effects then the remaining
    noise is truly random\", which first duh! and second even this is false.\r\n\r\nFor
    example  If the system is very sensitive to a single bad review, or needs a champion
    for the paper to be accepted, this amplifies the chances that a good paper will
    be rejected because the area wasn't popular or because the idea is really far
    out. In contrast a system designed differently could compensate against this.
    \r\n\r\nIngo said it best: \"But apart from that I would simply concentrate to
    make the review process robust against it.\""
- id: 5873
  author: Ingo Keck
  author_email: ingokeck@ingokeck.de
  author_url: http://ingokeck.de
  date: '2014-12-17 15:04:31 -0800'
  date_gmt: '2014-12-17 23:04:31 -0800'
  content: "I think there is also a third issue of malicious reviews. Especially if
    the conference is of high reputation (and thus important for building a publication
    history to apply successfully for funds) and the acceptance rate is low, circles
    of authors that are also reviewing have an incentive to favour their own submissions
    and down-rate competition independently from where it is coming from. Double-blind
    reviewing does not help there at all, because the malicious reviewers will know
    the articles they need to favour in advance, and simply down-rate everything else.
    \r\n\r\nOne part of the solution to this problem would be to open up the reviews,
    so malicious reviewing can be shamed by the public. Another part would be lower
    the incentive for bad behaviour, i.e. by keeping the acceptance rates high enough
    so that one or two bad reviews still won't stop a good article."
- id: 5875
  author: Boaz Barak
  author_email: blog@boazbarak.org
  author_url: http://www.boazbarak.org
  date: '2014-12-17 17:52:21 -0800'
  date_gmt: '2014-12-18 01:52:21 -0800'
  content: "@\"same here\" The question in the post was about the effects of random
    noise, as opposed to systematic biases. Peer review is of inherently biased against
    papers that are unpopular with the author's peers. You are right that one can
    try to change the process to achieve different notions of \"popular\". For example,
    in FOCS I tried to favor that a some people really love and some don't like at
    all, over papers that everybody thinks make a solid advance but nobody is very
    excited about. But this is a subjective choice, and I don't think there is a single
    right notion of \"popularity\" that we all should aim for. \r\n\r\n@Eric: I am
    not sure I understand your definition of \"fad topics\". If you mean a line of
    work that many people are excited about but ultimately leads nowhere, then I disagree
    that it's detrimental to science. If all the directions we pursue end up being
    successful then we are not taking enough risks. \r\n\r\nIf a paper appeared in
    a conference due to \"random luck\" but sufficiently many people found the talk
    and paper sufficiently interesting to do followup work so that it became a \"fad
    topic\", then it was probably good that it was accepted in the first place."
- id: 5876
  author: Boaz Barak
  author_email: blog@boazbarak.org
  author_url: http://www.boazbarak.org
  date: '2014-12-17 18:36:50 -0800'
  date_gmt: '2014-12-18 02:36:50 -0800'
  content: "As far as I can tell, your selection process was very thoughtful and well
    executed, and am sure that you ended up with a higher quality process and results
    than many smaller conference. I only mentioned the difference between NIPS and
    theory conferences because Eric's post discussed this point. \r\n\r\nI do think
    that there is an advantage, when the conference is small enough to allow it, for
    a physical PC meeting where all papers are discussed in the same time by the same
    people, and members of the PC have a global view of the entire program.  \r\n\r\nBTW
    I just looked at some statistics for FOCS and let me correct myself  - the average
    score is a decent predictor for acceptance , though I should say that these are
    the final scores, which have been adjusted during the discussion phase. We accepted
    69 papers out of 265 (ignoring papers withdrawn during the process). If instead
    we would have accepted the 69 papers with top mean score, this would intersect
    this list in about 55 papers - which I guess is pretty good agreement based on
    this experiment. However looking at the ~14 papers we would have rejected, I don't
    regret at all spending the two days of the physical meeting to make better choices.
    If we wanted to set the threshold low enough so that all of them would get in,
    we would have had to accept 150 papers"
- id: 5878
  author: Charles Sutton
  author_email: csutton@inf.ed.ac.uk
  author_url: ''
  date: '2014-12-17 19:55:50 -0800'
  date_gmt: '2014-12-18 03:55:50 -0800'
  content: As I recall Neil Lawrence mentioned during the results presentation that
    every effort was made to represent different areas equally among the two committees.
    I'm sure it's impossible to do so perfectly, so this could indeed be a source
    of variation, but at least the programme chairs attempted to correct for it as
    much as possible.
- id: 5879
  author: Eric Price
  author_email: ecprice@gmail.com
  author_url: ''
  date: '2014-12-17 21:32:40 -0800'
  date_gmt: '2014-12-18 05:32:40 -0800'
  content: "@Boaz, I'm defining a \"fad topic\" to be a topic that is getting more
    attention than it should, given the knowledge at the time.  \r\n\r\nIf there are
    two areas that seem equally interesting to me, but the community seems to think
    that one is more interesting than the other -- which I might judge by observing
    recent performance at conferences -- then I'd generally work on the one that seems
    more interesting to the community.  This is because (1) I would revise upward
    my estimation of its value, since the community knows stuff I don't and (2) it
    will be easier to publish subsequent results in top venues.  And it's easier to
    publish later results in top venues because the reviewers will also have a higher
    opinion of the topic just because they've seen it more at better conferences.
    \ This causes a snowball effect where one topic gets much more attention than
    the other, which is inefficient.\r\n\r\nIt seems plausible to me that this effect
    could turn local randomness in individual conference decisions into longer term
    variation.  I'm not sure it's testable, though."
- id: 5880
  author: Eric Price
  author_email: ecprice@gmail.com
  author_url: ''
  date: '2014-12-17 21:41:16 -0800'
  date_gmt: '2014-12-18 05:41:16 -0800'
  content: "I understood that comment to be that they worked hard to cover every area
    in each committee, not that they covered every area _equally_.   Trying to do
    the latter would be a mistake -- the goal of the experiment was to simulate two
    independent PCs, not to simulate two PCs that have been balanced to become more
    similar.\r\n\r\nAnd I think this is likely the main source of variation in theory
    conferences as well as NIPS.  Because theory conferences are less diverse, the
    overall variation is probably smaller."
- id: 5884
  author: Peer Review &#8220;Randomness&#8221; &#8211; A Case for Deliberation | Nature
    is not a Book
  author_email: ''
  author_url: https://anglosaxonmonosyllable.wordpress.com/2014/12/18/peer-review-randomness-a-case-for-deliberation/
  date: '2014-12-18 08:45:47 -0800'
  date_gmt: '2014-12-18 16:45:47 -0800'
  content: '[&#8230;] I&#8217;ve been reading about the NIPS Experiment. Calm down
    at the back there. NIPS stands for Neural Information Processing Systems. It&#8217;s
    all very serious and you can read about the experiment here and here. [&#8230;]'
- id: 5885
  author: On the NIPS Experiment and Review Process &laquo; Bert Huang&#039;s Blog
  author_email: ''
  author_url: https://berthuang.wordpress.com/2014/12/18/on-the-nips-experiment-and-review-process/
  date: '2014-12-18 10:20:59 -0800'
  date_gmt: '2014-12-18 18:20:59 -0800'
  content: '[&#8230;] has been focused on the NIPS experiment on its own reviewing
    system, Eric Price&#8217;s blog post on it, and unfortunately my flippant tweet
    pointing out some inaccuracies in the blog post. So [&#8230;]'
- id: 5888
  author: Kathryn Laskey
  author_email: klaskey@gmu.edu
  author_url: http://seor.gmu.edu/~klaskey/
  date: '2014-12-18 12:50:53 -0800'
  date_gmt: '2014-12-18 20:50:53 -0800'
  content: "Let's consider a Bayesian analysis of the \"messy middle\" model.  The
    model has two parameters, the \"sure accept\" and \"sure reject\" probabilities.
    \r\n\r\n  p = probability of sure accept\r\n  q = probability of sure reject\r\n
    \ r = 1-p-q = probability of coin-flip (50-50) decision\r\n\r\nWe can take it
    down to one parameter by constraining the probability of acceptance to p+r/2 =
    0.225. A little algebra gives us:\r\n\r\n<code>  0 &lt; p &lt; 0.225\r\n  q =
    p + 0.55 \r\n  r = 1 - 2p + 0.55 </code>\r\n\r\nThe probabilities for the experiment
    outcomes are:\r\n  Both committees accept: p + 0.25r \r\n  Both committees reject:
    q + 0.25r\r\n  Committees disagree: 0.5r\r\n\r\nThe blog post implies that 16
    papers were accepted by both committees, 43 were accepted by one committee and
    rejected by the other, and 107 were rejected by both committees.\r\n\r\nLet&#039;s
    place a uniform prior on p, and assume the data are multinomial with size 165
    and probabilities (p, r, q) for both accept, disagree, both reject, respectively.
    \ \r\n\r\nWe can avoid integration by discretizing p into, say, 100 equally spaced
    equiprobable values.  To obtain the posterior distribution on the sure-accept
    probability, we then calculate the multinomial likelihood for each of these values
    and normalize. (A simple simple R program for doing this analysis is given below.)
    \ \r\n\r\nWe find that the most likely a posteriori value for the sure-accept
    rate is p=0, and there is a 99% posterior probability that p is less than 0.05.
    \ That is, under this model, fewer than 5% of all papers are clear accepts, somewhere
    between 55% and 60% are clear rejects, and the rest -- between 35% and 45% of
    the papers -- are in the &quot;messy middle.&quot;\r\n\r\nIt is interesting to
    compare this model with the &quot;purely random&quot; model of flipping a biased
    coin on each paper and accepting it with probability 0.225.  The multinomial probability
    of the observed outcomes under this model is 4.7e-5. The marginal likelihood under
    the &quot;messy middle&quot; model is 3.03e-4, which is 6.4 times the &quot;purely
    random&quot; probability.  This means that if we gave the &quot;purely random&quot;
    and &quot;messy middle&quot; models equal prior probabilities, the experiment
    result would raise the posterior probability of the &quot;messy middle&quot; model
    to about 87%.  It&#039;s good news that the evidence goes against the &quot;purely
    random&quot; model, although one might have hoped it would be stronger than 87-13
    posterior odds.\r\n\r\n=============================\r\n<code>\r\n# R code for
    analyzing NIPS experiment data against &quot;messy middle&quot; and &quot;purely\r\n#
    random&quot; generative models\r\n\r\naccRate = 0.225                    # Conference
    accept rate\r\ndata = c(16,43,107)                # Observed data: 16 AA, 43 AR
    or RA, 107 RR  \r\nnBins=100                          # Number of bins for discretization\r\npSureA
    = (1:numBins-0.5)/numBins*accRate   # Probability of sure accept ranging from
    0 to accept rate \r\n\r\nmultLik = NULL   # vector of multinomial likelihood\r\nfor
    (pSA in pSureA) {              # Loop through values of pSureA\r\n\tpSR = pSA
    + 1-2*accRate        # prob of sure reject\r\n\tpMid = 1 - pSA - pSR           #
    prob of coin-flip\r\n\tpAA = pSA + 0.25*pMid          # prob of agree on accept\r\n\tpRR
    = pSR + 0.25*pMid          # prob of agree on reject\r\n\tprobs = c(pAA, 1-pAA-pRR,
    pRR) # prob of AA, AR/RA, RR\r\n\tmultLik = c(multLik,dmultinom(data,NULL,probs))
    \  # multinomial likelihood                             \r\n\t\r\n}\r\n\r\n# plot
    likelihood against prob of sure accept\r\nplot(pSureA,multLik)   \r\n\r\n# Marginal
    likelihood of data under uniform prior on prob of sure accept\r\nMLunif = mean(multLik)
    \r\n\r\n# Compare against model of &quot;random decision&quot; model - flip biased
    coin to accept\r\n# with probability equal to accept rate\r\nprand = c(accRate^2,
    accRate*(1-accRate)*2, (1-accRate)^2)\r\nlikRand = dmultinom(data,NULL,prand)\r\n\r\n#
    Posterior likelihood of &quot;messy middle&quot; model relative to &quot;random
    decision&quot; model \r\n# if the models have equal prior probability\r\npMessyMiddle=MLunif/(MLunif+likRand)</code>"
- id: 5889
  author: Kathryn Laskey
  author_email: klaskey@gmu.edu
  author_url: http://seor.gmu.edu/~klaskey/
  date: '2014-12-18 12:55:38 -0800'
  date_gmt: '2014-12-18 20:55:38 -0800'
  content: Sorry for the line-wrap screw-ups on the R code.  The preview looked better
    than this.
- id: 5890
  author: Quick comments on the NIPS experiment | Windows On Theory
  author_email: ''
  author_url: http://windowsontheory.org/2014/12/18/quick-comments-on-the-nips-experiment/
  date: '2014-12-18 13:45:40 -0800'
  date_gmt: '2014-12-18 21:45:40 -0800'
  content: '[&#8230;] on the NIPS experiment, enough of it that even my neuro-scientist
    brother sent me a link to Eric Price&#8217;s blog post. The gist of it is that
    the program chairs duplicated the reviewing process for 10% of the papers, [&#8230;]'
- id: 5891
  author: msk2
  author_email: mskmoorthy@yahoo.com
  author_url: ''
  date: '2014-12-18 13:51:50 -0800'
  date_gmt: '2014-12-18 21:51:50 -0800'
  content: I am unable to understand how a paper that gets rejected three times from
    a (similar/same) conference and gets the best paper award (in SODA) the fourth
    time(?) - Does it not contradict the hypothesis that very best papers get accepted,but
    only the middle papers are random?
- id: 5892
  author: Eric Price
  author_email: ecprice@gmail.com
  author_url: ''
  date: '2014-12-18 14:46:33 -0800'
  date_gmt: '2014-12-18 22:46:33 -0800'
  content: "Well, there's a couple things going on here.\r\n\r\nOne is that the best
    _student_ paper means much less than it sounds.  In CS Theory, unlike in many
    other areas, the best student paper can only be awarded to papers with only student
    authors.  There are typically only a handful of eligible papers, and those papers
    are worse on average than the non-student papers.  So one suggestion here is that
    the best student paper is a dumb award and should be removed. =)\r\n\r\nBeyond
    that, papers that get rejected multiple times before being accepted often do improve
    in each round, and my paper was no exception.  The main theorem didn't change,
    but the ancillary results demonstrating its usefulness were improved over time.
    \ So the fourth version was quite similar to the third, but substantially more
    competitive than the first.  In a sense, these rejections were good for science
    because otherwise we never would have polished the paper the way we did.\r\n\r\nSo
    I don't think this example contradicts the hypothesis."
- id: 5894
  author: Udi
  author_email: udi.weinsberg@gmail.com
  author_url: http://paperthon.com
  date: '2014-12-18 21:08:51 -0800'
  date_gmt: '2014-12-19 05:08:51 -0800'
  content: "That's a great study. I've created Paperthon (http://paperthon.com) to
    do similar studies (meta-research) on a broader scale beyond a few conferences.
    The idea is that researchers send the notification emails to log@paperthon.com
    and it tracks the entire submission process (rejected from X, rejected from Y,
    accepted to Z). It supports several conference systems (edas, hotcrp, etc.). Then
    we can bring more transparency into the submission process across research communities,
    conferences and domains. \r\n\r\nSadly, not strong in marketing, so not too many
    people know about it, so I don't have enough data to share insights (yet). Hopefully,
    people reading this will start sending notification emails to get this (meta-)research
    to the next step!"
- id: 5896
  author: Testing peer review by running submissions through the process twice
  author_email: ''
  author_url: http://marginalrevolution.com/marginalrevolution/2014/12/testing-peer-review-by-running-submissions-through-the-process-twice.html
  date: '2014-12-19 00:11:07 -0800'
  date_gmt: '2014-12-19 08:11:07 -0800'
  content: '[&#8230;] That is from Eric Price on the NIPS experiment, there is more
    here. [&#8230;]'
- id: 5898
  author: Testing peer review by running submissions through the process twice | Homines
    Economici
  author_email: ''
  author_url: http://www.homineseconomici.com/archives/1401
  date: '2014-12-19 00:49:46 -0800'
  date_gmt: '2014-12-19 08:49:46 -0800'
  content: '[&#8230;] That is from Eric Price on the NIPS experiment, there is more
    here. [&#8230;]'
- id: 5905
  author: same here
  author_email: same@here.yu
  author_url: ''
  date: '2014-12-19 08:49:31 -0800'
  date_gmt: '2014-12-19 16:49:31 -0800'
  content: This is true for student papers, however the same has happened for regular
    papers going from reject to best paper from STOC to FOCS or sometimes in the same
    conference a year later.
- id: 5907
  author: Testing peer review by running submissions through the process twice | Bydio
  author_email: ''
  author_url: http://bydio.com/2014/12/19/testing-peer-review-by-running-submissions-through-the-process-twice/
  date: '2014-12-19 14:01:16 -0800'
  date_gmt: '2014-12-19 22:01:16 -0800'
  content: '[&#8230;] That is from Eric Price on the NIPS experiment, there is more
    here. [&#8230;]'
- id: 5915
  author: 'Weekend reads: Authorship for sale, STAP stem cell scandal finally over?
    - Retraction Watch at Retraction Watch'
  author_email: ''
  author_url: http://retractionwatch.com/2014/12/20/weekend-reads-authorship-sale-stap-stem-cell-scandal-finally/
  date: '2014-12-20 06:30:58 -0800'
  date_gmt: '2014-12-20 14:30:58 -0800'
  content: '[&#8230;] How random is the conference presentation review process? One
    group of organizers tried to find out, in an experiment. [&#8230;]'
- id: 5917
  author: Dan Riley
  author_email: Daniel.Riley@cornell.edu
  author_url: ''
  date: '2014-12-20 07:55:01 -0800'
  date_gmt: '2014-12-20 15:55:01 -0800'
  content: "That raises what I think is an under-appreciated point.  The committee
    had an acceptance rate target, so this was not a simple good/bad rating, it was
    a partial ranking of the best 22.5%.  Rankings of closely bunched values exaggerate
    noise, as Tanvir's comment illustrates.  To model this properly requires an estimate
    of the distribution of paper quality and an estimate of the expected variability
    of referee evaluations (and the form of the noise).\r\n\r\nThere may be no robust
    selection procedure that doesn't entail a huge review committee.  A less biased
    procedure might be to identify the clear accepts and rejects, and make a weighted
    random selection from what's left in the middle--it would be interesting to run
    some trials with a real dataset."
- id: 5922
  author: lawrennd
  author_email: lawrennd@gmail.com
  author_url: http://inverseprobability.wordpress.com
  date: '2014-12-20 13:29:05 -0800'
  date_gmt: '2014-12-20 21:29:05 -0800'
  content: Sounds (roughly) similar to us Boaz, although I don't have the precise
    figures to hand. When we write up the experiment I think this number will be in
    there (because we'll be releasing agreements over time where we will have to use
    the score, or calibrated score as a proxy).
- id: 5938
  author: sb
  author_email: sb46@sanger.ac.uk
  author_url: ''
  date: '2014-12-22 01:02:56 -0800'
  date_gmt: '2014-12-22 09:02:56 -0800'
  content: A note to the author - I was directed here from Retraction Watch - I'm
    unfamiliar with the work you are writing about, but I am a science policy professional.
    I have to say I found this article totally unaccessible to anyone not well versed
    in NIPS. You have three acronyms in the first 10 lines with no explanation of
    their meaning. I made it as far as the "messy middle model" before abandoning
    the article. I still don't know what NIPS stands for.
- id: 5940
  author: Eric Price
  author_email: ecprice@gmail.com
  author_url: ''
  date: '2014-12-22 01:13:08 -0800'
  date_gmt: '2014-12-22 09:13:08 -0800'
  content: "Thanks for the comment!  This post has gotten a lot wider circulation
    than I was expecting, so it definitely could use being made more accessible.  I've
    tried to make the first paragraph friendlier.\r\n\r\n(Tangentially, learning what
    NIPS stands for would be more confusing than enlightening.  The name is largely
    an historical artifact.)"
- id: 5944
  author: Somewhere else, part 195 | Freakonometrics
  author_email: ''
  author_url: http://freakonometrics.hypotheses.org/18360
  date: '2014-12-22 05:04:05 -0800'
  date_gmt: '2014-12-22 13:04:05 -0800'
  content: '[&#8230;] NIPS Experiment&quot; http://mrtz.org/blog/the-nips-experiment/ …
    &quot;Half the papers appearing at NIPS would be rejected if the review process
    were [&#8230;]'
- id: 6043
  author: 'The zidi retweet #5: our favorite stories of 2014 | zidi publishing'
  author_email: ''
  author_url: http://zidipublishing.wordpress.com/2014/12/30/the-zidi-retweet-5-our-favorite-stories-of-2014/
  date: '2014-12-30 10:44:50 -0800'
  date_gmt: '2014-12-30 18:44:50 -0800'
  content: '[&#8230;] would the NIPS Experiment have to say about this? David Mazières
    and Eddie Kohler—in response to constant spam from [&#8230;]'
- id: 6048
  author: ADC
  author_email: allan.coop@gmail.com
  author_url: ''
  date: '2014-12-30 13:23:19 -0800'
  date_gmt: '2014-12-30 21:23:19 -0800'
  content: I don't do twit or F******K, but I managed to read this far here . . .
- id: 6053
  author: Last Incredible Necessary Kenyan post of the year | taylortoowen
  author_email: ''
  author_url: http://taylortoowen.wordpress.com/2014/12/30/last-incredible-necessary-kenyan-post-of-the-year/
  date: '2014-12-30 18:06:36 -0800'
  date_gmt: '2014-12-31 02:06:36 -0800'
  content: '[&#8230;] Getting your work peer reviewed is like, 50% random [&#8230;]'
- id: 6056
  author: boerzoektvrouw
  author_email: deboer@p.com
  author_url: ''
  date: '2014-12-31 02:46:33 -0800'
  date_gmt: '2014-12-31 10:46:33 -0800'
  content: Yes. It could be either incompetence or self-interest of the reviewers.
    Or maybe just a tool to make people work harder. If it's too easy to get in the
    most skilled people tend to slack off (?)
- id: 6122
  author: 5 interesting things (04/01/2015) | Tom Ron
  author_email: ''
  author_url: http://tomron.net/2015/01/04/5-interesting-things-04012015/
  date: '2015-01-04 05:21:56 -0800'
  date_gmt: '2015-01-04 13:21:56 -0800'
  content: '[&#8230;] Posted on January 4, 2015January 4, 2015 by tom   Is Wikipedia
    a microcsmos of our world? News of 2014 as they are reflected in Wikipedia. http://www.brianckeegan.com/2014/12/the-news-on-wikipedia-in-2014/  Json
    as python modules &#8211; Making life simpler. Making it possible to do -&#8220;import
    x&#8221; for x.json. https://github.com/kragniz/json-sempai    Python the fast
    way &#8211; living on the edge with Python :) Some hints on how to make your code
    run faster. Another possibility &#8211; checking different interpreters. It was
    nice to see the assembly commands, I was expecting something more advanced. http://pythonfasterway.uni.me/   Data
    Science Ontology &#8211; just having fun with d3.js.  http://www.datascienceontology.com/    Nips
    Experiment &#8211; there was relatively a lot of chatter regarding the experiment
    done by NIPS committee. Non the less, it creates a very uncomfortable feeling
    regarding committees. http://mrtz.org/blog/the-nips-experiment/ [&#8230;]'
- id: 6160
  author: The NIPS experiment &laquo; Machine Learning (Theory)
  author_email: ''
  author_url: http://hunch.net/?p=467864
  date: '2015-01-07 12:38:41 -0800'
  date_gmt: '2015-01-07 20:38:41 -0800'
  content: '[&#8230;] The 26% disagreement rate presented at the conference understates
    the meaning in my opinion, given the 22% acceptance rate. The immediate implication
    is that between 1/2 and 2/3 of papers accepted at NIPS would have been rejected
    if reviewed a second time. For analysis details and discussion about that, see
    here. [&#8230;]'
- id: 6166
  author: NIPS 2014 main meeting | Memming
  author_email: ''
  author_url: https://memming.wordpress.com/2015/01/08/nips-2014-main-meeting/
  date: '2015-01-08 11:44:46 -0800'
  date_gmt: '2015-01-08 19:44:46 -0800'
  content: '[&#8230;] between the two pools, so the overall acceptance rate was a
    bit higher this year. For details, see Eric Price&#8217;s blog post and Bert Huang&#8217;s
    [&#8230;]'
- id: 6221
  author: Open Science &amp; Altmetrics Monthly Roundup (December 2014) - Impactstory
    blog
  author_email: ''
  author_url: http://blog.impactstory.org/roundup-december-2014/
  date: '2015-01-12 09:16:55 -0800'
  date_gmt: '2015-01-12 17:16:55 -0800'
  content: '[&#8230;] a study that found&#8211;yet again&#8211;that Open Access publications
    receive more downloads; the results of one conference’s experiment with peer review,
    which showed that peer review is “close to random” in terms of what reviewers
    agree to accept [&#8230;]'
- id: 6288
  author: 'Das NIPS-Experiment: Peer Review oder Münzwurf | Infobib'
  author_email: ''
  author_url: http://infobib.de/2015/01/15/das-nips-experiment-peer-review-oder-muenzwurf/
  date: '2015-01-15 03:09:20 -0800'
  date_gmt: '2015-01-15 11:09:20 -0800'
  content: '[&#8230;] Worum ging es beim NIPS-Experiment? Für die NIPS 2014 wurden
    zwei Programmkommitees eingerichtet. 10% der Einreichungen (166) wurden beiden
    Kommitees zur Begutachtung vorgelegt. Es sollte geprüft werden, wie sehr die Entscheidungen
    übereinstimmen. Das Fazit in zwei Worten: nicht sehr. Die meisten der tatsächlich
    gehaltenen Vorträge wären abgelehnt worden, wenn man die Begutachtung noch einmal
    vom jeweils anderen Kommitee hätte durchführen lassen. Eric Price geht ins Detail:
    [&#8230;]'
- id: 6300
  author: Blogs on the NIPS Experiment | Inverse Probability
  author_email: ''
  author_url: http://inverseprobability.com/2015/01/16/blogs-on-the-nips-experiment/
  date: '2015-01-16 02:08:44 -0800'
  date_gmt: '2015-01-16 10:08:44 -0800'
  content: '[&#8230;] Eric Price&#8217;s original blog which seemed to have the largest
    impact in making the world aware of the experiment. [&#8230;]'
- id: 6348
  author: '&gt;50% of NIPS papers would be rejected if the review process was rerun
    | Joseph Jacobs'
  author_email: ''
  author_url: http://joejacobs.org/2015/01/19/50-of-nips-papers-would-be-rejected-if-the-review-process-was-rerun/
  date: '2015-01-19 14:22:57 -0800'
  date_gmt: '2015-01-19 22:22:57 -0800'
  content: '[&#8230;] Read the full article &#8220;The NIPS Experiment&#8221; by Moritz
    Hardt. [&#8230;]'
- id: 6351
  author: 廖君：机器学习&amp;深度学习资料 &#124; 我爱互联网
  author_email: ''
  author_url: http://www.person168.com/?p=78777
  date: '2015-01-19 19:52:54 -0800'
  date_gmt: '2015-01-20 03:52:54 -0800'
  content: '[&#8230;] 《NIPS 审稿实验》 [&#8230;]'
---
<div style="background-color: #cccccc;text-align: center;padding 5px;margin: auto;width: 60%">TL;DR: Half the papers appearing at NIPS would be rejected if the review process were rerun.</div>
<p>&nbsp;</p>
<p>[This is a guest post by <a href="http://cs.utexas.edu/~ecprice/">Eric Price</a>.]</p>
<p>I was at NIPS (one of the two main machine learning conferences) in Montreal last week, which has a really advanced format relative to the theory conferences. The double blind reviewing, rebuttal phase, and poster+lightning talk system all seem like improvements on the standard in my normal area (theoretical computer science), and having 2400 attendees is impressive and overwhelming. But the most amazing thing about the conference organization this year was the <a href="http://inverseprobability.com/2014/12/16/the-nips-experiment/">NIPS consistency experiment</a>.</p>
<p>A perennial question for academics is how accurate the conference review and acceptance process is. Getting papers into top conferences is hugely important for our careers, yet we all have papers rejected that we think should have gotten in. One of my papers was rejected three times before getting into SODA -- as the best student paper. After rejections, we console ourselves that the reviewing process is random; yet we take acceptances as confirmation that our papers are good. So just how random <i>is</i> the reviewing process?  The NIPS organizers decided to find out.</p>
<h2>The NIPS Experiment</h2>
<p>The NIPS consistency experiment was an amazing, courageous move by the organizers this year to quantify the randomness in the review process. They split the program committee down the middle, effectively forming two independent program committees. Most submitted papers were assigned to a single side, but 10% of submissions (166) were reviewed by <i>both</i> halves of the committee. This let them observe how consistent the two committees were on which papers to accept.  (For fairness, they ultimately accepted any paper that was accepted by either committee.)</p>
<p>The results were revealed this week: of the 166 papers, the two committees disagreed on the fates of 25.9% of them: 43. [Update: the original post said 42 here, but I misremembered.] But this "25%" number is misleading, and most people I've talked to have misunderstood it: it actually means that the two committees <i>disagreed more than they agreed</i> on which papers to accept. Let me explain.</p>
<p>The two committees were each tasked with a 22.5% acceptance rate. This would mean choosing about 37 or 38 of the 166 papers to accept<sup><a href="#footnotes">1</a></sup>. Since they disagreed on 43 papers total, this means one committee accepted 21 papers that the other committee rejected and the other committee accepted 22 papers the first rejected, for 21 + 22 = 43 total papers with different outcomes. Since they accepted 37 or 38 papers, this means they disagreed on 21/37 or 22/38 ≈ 57% of the list of accepted papers.</p>
<p>In particular, about 57% of the papers accepted by the first committee were rejected by the second one and vice versa. In other words, most papers at NIPS would be rejected if one reran the conference review process (with a 95% confidence interval of 40-75%):</p>
<p class="alignnone size-medium wp-image-407" style="text-align: center">  <a href="http://mrtz.org/blog/wp-content/uploads/2014/12/nips-pie11.png"><img class="alignnone size-full wp-image-430" src="http://mrtz.org/blog/wp-content/uploads/2014/12/nips-pie11.png" alt="nips-pie1" width="671" height="546" /></a>Most papers accepted by one committee were rejected by the other, and vice versa.</p>
<p style="text-align: left">This result was surprisingly large to most people I've talked to; they generally expected something like 30% instead of 57%. Relative to what people expected, 57% is actually closer to a purely random committee, which would only disagree on 77.5% of the accepted papers on average:</p>
<p style="text-align: center"><a href="http://mrtz.org/blog/wp-content/uploads/2014/12/randomgraph2.png"><img class="alignnone size-full wp-image-456" src="http://mrtz.org/blog/wp-content/uploads/2014/12/randomgraph2.png" alt="randomgraph2" width="969" height="583" /></a>If the committees were purely random, at a 22.5% acceptance rate they would disagree on 77.5% of their acceptance lists on average.</p>
<p>In the next section, I'll discuss a couple simple models for the conference review process that give the observed level of randomness.</p>
<h2>Models for conference acceptance</h2>
<p>One rough model for paper acceptance, consistent with the experiment, is as follows:</p>
<ol>
<li style="padding-left: 30px">Half the submissions are found to be poor and reliably rejected.</li>
<li style="padding-left: 30px">The other half are accepted based on an unbiased coin flip.</li>
</ol>
<p>This might be a decent rule of thumb, but it's clearly missing something: some really good papers do have a chance of acceptance larger than one half.</p>
<h3>The "messy middle" model</h3>
<p>One simple extension to the above model is the "messy middle" model, where some papers are clear accepts; some papers are clear rejects; and the papers in the middle are largely random.   We can compute what kinds of parameters are consistent with the NIPS experiment.  Options include:</p>
<ol>
<li><strong>The above model.</strong> Half the papers are clear rejects, and everything<br />
else is random.</li>
<li><strong> The opposite.</strong> 7% of all papers (i.e. 30% of accepted papers) are<br />
clear accepts, and the  other 93% are random.</li>
<li><strong>Somewhere in the middle.</strong> For example 6% of all papers (i.e. 25% of accepted papers) are clear accepts, 25% of submitted papers are clear rejects, and the rest are random.<a href="http://mrtz.org/blog/wp-content/uploads/2014/12/messymiddle.png"><img class="alignnone size-full wp-image-445" src="http://mrtz.org/blog/wp-content/uploads/2014/12/messymiddle.png" alt="messymiddle" width="838" height="683" /></a></li>
</ol>
<h3>The "noisy scoring" model</h3>
<p>As I was discussing this over dinner, Jacob Abernethy proposed a "noisy scoring" model based on his experience as an area chair. Each paper typically gets three reviews, each giving a score on 0-10. The committee uses the average score<sup><a href="#footnotes">2</a></sup> as the main signal for paper quality. As I understand it, the basic committee process was that almost everything above 6.5 was accepted, almost everything below 6 was rejected, and the committee mainly debated the papers in between.</p>
<p>A basic simplified model of this would be as follows. Each paper has a "true" score \({v}\) drawn from some distribution (say, \({N(0, \sigma_{between}^2)}\)), and the the reviews for the paper are drawn from \({N(v, \sigma_{within}^2)}\). Then the NIPS experiment's result (number of papers in which the two committees disagree) is a function of the ratio \({\sigma_{between}/\sigma_{within}}\). We find that the observation would be consistent with this model if \({\sigma_{within}}\) is between one and four times \({\sigma_{between}}\):</p>
<p><a href="http://mrtz.org/blog/wp-content/uploads/2014/12/noisyscoring2.png"><img class="alignnone size-full wp-image-455" src="http://mrtz.org/blog/wp-content/uploads/2014/12/noisyscoring2.png" alt="noisyscoring2" width="973" height="568" /></a></p>
<p>Once the NIPS review data is released, we can check the empirical \({\sigma_{within}}\) and \({\sigma_{between}}\) to see if this model is reasonable.</p>
<p>One nice thing about the noisy scoring model is that you don't actually need to run the NIPS experiment to estimate the parameters. Every CS conference could measure the within-paper and between-paper variance in reviewer scores. This lets you measure the expected randomness in the results of the process, assuming the model holds.</p>
<h2>Conclusions</h2>
<p>Computer science conference acceptances seem to be more random than we had previously realized. This suggests that we should rethink the importance we give to them in terms of the job search, tenure process, etc.</p>
<p>I'll close with a few final thoughts:</p>
<ul>
<li>Consistency is not the only goal. Double-blind reviewing probably decreases consistency by decreasing the bias towards established researchers, but this is a good thing and the TCS conferences should adopt the system.</li>
<li>Experiments are good! As scientists, we ought to do more experiments on our processes. The grad school admissions process seems like a good target for this, for example.</li>
<li>I'd like to give a <i>huge</i> shout-out to the NIPS organizers, Corinna Cortes and Neil Lawrence, for running this experiment. It wasn't an easy task -- not only did they review 10% more papers than necessary, they also had the overhead of finding and running two independent PCs. But the results are valuable for the whole computer science community.</li>
</ul>
<h4 id="footnotes">Footnotes</h4>
<ol>
<li>The committees did not know which of the ~900 papers they were reviewing were the 166 duplicated ones, so there can be some variation in how many papers to accept, but this is a minor effect.</li>
<li>They also use a "confidence-weighted" score, but let's ignore that detail.</li>
</ol>
