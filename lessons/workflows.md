#   Workflows & Lifecycles

##  Objectives

- Employ a framework for embarking on a research program (such as the Heilmeier Catechism).
- Explain the standard project lifecycle, from conceptualization to termination.
- Consider what the standard project lifecycle looks like in practical research software and research program efforts.
- Build automatic tools to manage portions of your data analysis.

##  The Research Lifecycle

- What is research?

Research is the process of ideas becoming accepted knowledge within a community of practitioners.

- What does it mean for knowledge to transfer or be disseminated for scientists?

- How should scientists deal with contradictory or absurd claims?  How does authority (nullius in verba) affect this process?  What historical examples can you cite in support of either of these questions?

- What failure modes for research can you think of? (such as "crisis", however defined)

1.  consistent [most science]
    1.  tautology
    2.  discovery/extension ([the Ortega hypothesis](https://en.wikipedia.org/wiki/Ortega_hypothesis))
2.  inconsistent [politicized science]
    1.  absurdity (statements that literally do not make sense _within_ a paradigm)
    2.  Copernican/Galilean paradigm shift [Kuhn, Feyerabend] (properly speaking a subset of 2a)
    3.  politicized science:  [make point horse deer](https://bloodyshovel.wordpress.com/2015/06/03/the-purpose-of-absurdity/), lysenkoism

Primary readings:
- Centola 2015, [The Social Origins of Networks and Diffusion](http://www.journals.uchicago.edu/doi/10.1086/681275) [how information actually travels in social networks, keeping in mind that science is a social/sociological enterprise]
- [Incommensurability in Science](http://www.oxfordbibliographies.com/view/document/obo-9780195396577/obo-9780195396577-0022.xml) [first major paragraph only]

Secondary readings:
- [The Incommensurability of Scientific Theories](http://plato.stanford.edu/entries/incommensurability/) [setting the stage for why theories need to disseminate]
- Greenberg 2009, [How citation distortions create unfounded authority: analysis of a citation network](http://www.bmj.com/content/339/bmj.b2680) [tangential failure mode]

Scientific and engineering research in the latter half of the twentieth century frequently cited [Karl Popper's principle of falsifiability](https://en.wikipedia.org/wiki/Falsifiability) to explain how they related to underlying physical reality.  Analogues have been cited for many other fields, and notably this foundational principle has led to the particular concern over the replication crisis which many fields face.  Put succinctly, falsifiability is a criterion that a particular claim or theory can only be considered scientific if one could construct an empirical test which would confirm or refute it.  Therefore any claim should be predictive and testable.

Over time, Thomas Kuhn's conflicting model of scientific revolutions and paradigm shifts grew more popular.  This conceives of "science as an activity practiced by people called scientists," a more sociological-descriptive view that accounts for changes in theory and practice.

Philosopher of mathematics and science Imre Lakatos fused these into a notion of a “research programme”, marrying a hard core of theoretical assumptions to auxiliary hypotheses.

This motivates why your research efforts, either as an undergrad or even more so as a graduate student, must be founded on a course of study in your discipline, then extended via hypothetical questions.

Your career as a researcher will have several distinct stages.  For the most part, these are now recognized and supported by funding bodies:

1. Undergraduate research
2. Graduate research (master's and doctorate)
3. Post-doctoral research
4. Early-career research (can overlap with postdoc but may just be early faculty or researcher career)
5. Mid-career researcher
6. Late-career researcher
7. Emeritus faculty

Yes, the above list is too faculty-centric.  There has been growing support for non-faculty researcher roles in the past decade.  There has also been a grudging acknowledgement that there really aren't enough faculty seats to go around, so they have find ways of using skilled trained researchers in other ways that are still well-structured fulfilling careers.  Unfortunately, some disciplines are rather set up as a Ponzi scheme relying on cutthroat competition for relatively few tenured seats, with a large pool of competitive cheap labor for teaching.  In addition, industrial research laboratories have historically been extremely productive (Bell Labs, Xerox PARC).

It can be helpful to think of each arc of your professional life explicitly.  In practice, I have observed that for personal and professional reasons a typical project arc takes about seven years from conceptualization to termination.  Manhattan Project physicist Leo Szilard concurs:

> Do your work for six years; but in the seventh, go into solitude or among strangers, so that the memory of your friends does not prevent you from being what you have become.  (Ten Commandments, #9¸ c.1940)

One reason for this is that center grants typically last about four--five years (or twice that with a renewal).  Another is that graduate school nominally takes about seven years from start to finish, perhaps including a postdoc.


##  Formal Frameworks

The NIST [defines](https://www.nist.gov/programs-projects/scientific-workflow) a scientific workflow as, “the encapsulation of all processes and accompanying relevant data necessary to reproduce and validate an experiment. Thus, a workflow must include defining the specific tools (software), parameters and inputs, assumptions, and provenance information, and the way in which they were used to produce a result.”

One research workflow includes the following steps:

1. Conceptualization
2. Research design
3. Funding
4. Collaboration
5. Procedural details (lab management, equipment acquisition, etc.)
6. Data collection
7. Analysis
8. Writing
9. Sharing
10. Submission
11. Review
12. Publication
13. Showcasing
14. Assessment
15. Routinization
16. Termination

(I have constructed this from several sources and my own experience, including [Schonfeld](https://sr.ithaka.org/blog/what-is-researcher-workflow/).)

#### 1. Conceptualization

> Philosophy begins in wonder.
(Plato, Theaetetus 155d)

Where do research questions come from?  What is the source of a hypothesis?  (We need both to proceed!)

> THE big problem for those trying to understand science has been the question of: Where do correct hypotheses come-from - given that there are an unbounded number of incorrect hypotheses. This does not entail assuming that correct hypotheses are either certain or complete (any hypotheses is almost-inevitably a shortened and selective model of reality) - merely that there are so many more ways of being wrong than right; and science could never get going if vast numbers of wrong hypotheses had to be eliminated with every step.  ¶Upon this matter hinges almost the whole of science; because once good hypotheses are available, science becomes more-or-less a matter of applied routine (research and development, as it is called).

- What do you think?

This is where everyone who has seriously dealt with the problem tends to get a little bit mystical.  It's related to the mystery of consciousness itself, in particular to the imagination, our faculty to conceiving of hypothetical structurings of facts and the world.  That is, _where do ideas come from?_

There have been a few attempts by scientists and mathematicians to answer the question, e.g.

Johann Wolfgang von Goethe:

> The uncannily prescient insight of Goethe was that _true hypotheses come from the imagination of an individual scientist—constrained by a direct apprehension of phenomena_. 

Henri Poincaré treats hypothesis as central to the practice of science, distinguishing four kinds:

1. Verifiable hypotheses:  general statements confirmed by experiment
2. Indifferent (or neutral) hypotheses:  ontology, mechanical models of mechanism (like the propagation of heat)
3. Natural hypotheses:  necessary conditions but experimentally inaccessible (like the uniformity of the universe)
4. Apparent hypotheses:  definitions or conventions (like metric geometry)

Owen Barfield:

“Astronomy and physics had taught men that the business of science is to find hypotheses to save the appearances.”

“Barfield hastens to remind us that up until the time of the Copernican Revolution, a hypothesis was widely understood to mean a ‘proposition, the truth or untruth of which is irrelevant’—one intended, that is, to ‘save the appearances.’ ‘All that mattered was, which was the simplest and the most convenient for practical purposes.’”

[“Simply put, saving the appearances means that hypotheses which explain appearances are not for that reason necessarily true. Under this conception, two contradictory hypotheses can both explain—i.e., ‘save’—the appearances, as did both the Ptolemaic and Copernican conceptions of the cosmos.”]

Michael Polanyi:

> A knower does not stand apart from the universe, but participates personally within it. Our intellectual skills are driven by passionate commitments that motivate discovery and validation. According to Polanyi, a great scientist not only identifies patterns, but also chooses significant questions likely to lead to a successful resolution. Innovators risk their reputation by committing to a hypothesis. Polanyi cites the example of Copernicus, who declared that the Earth revolves around the Sun. He claims that Copernicus arrived at the Earth's true relation to the Sun not as a consequence of following a method, but via "the greater intellectual satisfaction he derived from the celestial panorama as seen from the Sun instead of the Earth." His writings on the practice of science influenced Thomas Kuhn and Paul Feyerabend.

Dramatically, [hypnagogia](https://en.wikipedia.org/wiki/Hypnagogia) (the state of being on the edge of sleep) can produce fascinating insights, as cited by August Kekulé in his perception of the structure of benzene.

More prosaically, at least at this point, you are more likely to be simply assigned a question by your research advisor and expected to work it out with fairly minimal supervision.

- [Charlton, “Where Do True Hypotheses Come From?  Imagination and Intuition as the Basis of Science”](https://charltonteaching.blogspot.com/2015/11/where-do-true-hypotheses-come-from.html)
- [Naydler, “Goethe on Science”](https://www.naturalbeekeepingtrust.org/goethe-on-science)
- [Heinzmann & Stump, “Henri Poincaré”](https://plato.stanford.edu/entries/poincare/)


#### 2. Research design

Given the question, you have to decide how you are going to structure your research programme.  This includes your literature search and review as well as your background coursework and experience.

Given your hypothesis, you must decide what evidentiary standard could be produced that would support or falsify it.  This may require a cycle of returning back to the previous stage and reformulating what it is you think is going on, in dialogue with your reading and early explorations.

> What then is a good experiment? It is one that informs us of something besides an isolated fact, one that allows us to make predictions; that is, that allows us to generalize. For without generalization, we cannot make predictions.
(Henri Poincaré)

There have been several aids produced by research managers and scientists over the years designed to assist new researchers in formulating their research programmes; e.g. Heilmeier's Catechism:

> George H. Heilmeier, a former Defense Advanced Research Projects Agency (DARPA) director (1975-1977), crafted a set of questions known as the "Heilmeier Catechism" to help Agency officials think through and evaluate proposed research programs.
>
> - What are you trying to do? Articulate your objectives using absolutely no jargon.
> - How is it done today, and what are the limits of current practice?
> - What is new in your approach and why do you think it will be successful?
> - Who cares? If you are successful, what difference will it make?
> - What are the risks?
> - How much will it cost?
> - How long will it take?
> - What are the mid-term and final “exams” to check for success?
>
> ([“The Heilmeier Catechism”](https://www.darpa.mil/work-with-us/heilmeier-catechism))

The gold standard for research design includes the preregistration of hypotheses.

> When you preregister your research, you're simply specifying your research plan in advance of your study and submitting it to a registry. 
>
> Preregistration separates hypothesis-generating  (exploratory) from hypothesis-testing (confirmatory) research. Both are important. But the same data cannot be used to generate and test a hypothesis, which can happen unintentionally and reduce the credibility of your results. Addressing this problem through planning improves the quality and transparency of your research. This helps you clearly report your study and helps others who may wish to build on it. For instructions on how to submit a preregistration on OSF, please visit our help guides.

Preregistration reduces the likelihood that you are tempted to postdict your outcome, and helps you think more carefully about the structure of the experiments you design to pursue the answer to your question.

Another alternative which has become more common of late is to produce a hash of the hypothesis or claim, then later reveal the text that yields the hash.  (This is [Lindy](https://en.wikipedia.org/wiki/Lindy_effect), by the by:  Robert Hooke did this in 1660 and revealed it in 1678 since no one could solve it:  `ceiiinosssttuv` unscrambles to `ut tensio sic vis`, Hooke's law of springs.)

- [Center for Open Science, “What is Preregistration?”](https://www.cos.io/initiatives/prereg)
- [Nosek et al., “The Preregistration Revolution”](https://www.pnas.org/doi/10.1073/pnas.1708274114)


#### 3. Funding

Most research programmes require substantial funding.  About half of the funding gets eaten up directly by the institution that employs you as a researcher.  Much of the rest goes to salaries and wages for personnel attached to the project, or perhaps physical experimental hardware or software licenses.

It will serve you well to get to know the standard funding agencies and mechanisms in your field, and spend a little bit of extra time on long-shot outside sources, like foundations, patrons, and endowments.  If you are attached to a research institution like an R1 university, then much of this work will be done by professional research staff, but you'll need to be aware of basic numbers and dates even early in your career.  It will also pay off hugely to acquaint yourself with program managers in government funding agencies like NSF and NIH, and they expect you to do so.

(The worst thing that happens to professional researchers, in my opinion, is that they stop talking about ideas and only talk about grants and grantseeking.)

Not all research programmes need money tho, & altho it's the worst _professional_ advice I can possibly give you, it's absolutely fine (and occasionally necessary) to stew on a hard problem for years, possibly a lifetime.

Andrew Wiles solved Fermat's theorem in 1994.  He spent six years cloistered, secretively working on the problem, telling only his wife.

Julian Barbour, a physicist who has championed quantum gravity approaches to solving problems in fundamental physics, never held an academic position since his graduation in 1968, at one point spending ten years thinking about the theory of relativity and its relationship to time.

> This led him to investigate the roots of our understanding of time, contained in the general theory of relativity. He realized that he could not make a conventional academic career worrying about the nature of time. He also realized that if he was going to work on that problem, he would have to concentrate on it fully, without being distracted by the pressures of a normal career in physics. So he bought an old farmhouse in a little village half an hour from Oxford, brought his new wife there, and settled down to think about time. It was ten years or so before he had something to report back to his colleagues. 

- Lee Smolin, _The Trouble with Physics_ (2006)


#### 4. Collaboration

Most research projects will require a fair amount of collaboration.  We can draw a sliding scale from solo research projects to huge teams.

**Solo research** may take place when initially conceiving of a compelling research question, or as a summative effort later in a career.  There's still a fair amount of it done by mid-career and late-career researchers.

**Pair collaboration** is fairly uncommon these days but has a fruitful past.  Long-term pairwise collaborations of researchers yield about 17% more research products (typically articles) over their careers.

> An example of this limiting scenario is … the “dynamic duo” of J. L. Goldstein and M. S. Brown, winners of the 1985 Nobel Prize in Physiology or Medicine; Goldstein and Brown published more than 450 publications each, with roughly 100×fK,i≈95% coauthored together.

This is not common, and there is really no officially-supported path to discover such a professional collaboration, but it is incredibly valuable when two such researchers find each other.

- [Petersen, “Quantifying the Impact of Weak, Strong, and Super Ties in Scientific Careers”](https://www.pnas.org/doi/full/10.1073/pnas.1501444112)
- [Bu et al., “Understanding Persistent Scientific Collaboration”](https://asistdl.onlinelibrary.wiley.com/doi/full/10.1002/asi.23966)

**Research groups** form the legacy interaction format for modern academia, and many faculty still use them as their primary organizational pattern.  A faculty PI obtains funding for a coterie of grad students, postdocs, and others, mainly organized around the one PI and his or her work.

- [Milojević, “Principles of Scientific Research Team Formation and Evolution”](https://www.pnas.org/doi/pdf/10.1073/pnas.1309723111)

**Team collaboration** is a very common model for contemporary academic researchers in science and engineering:  a center or institute is created and funded, providing a way of funding and coordinating efforts between faculty, research scientists, research software engineers, lab technicians, and others.

(I should lead with the caveat that, due to the structure of my graduate and professional career to date, I've never worked on a productive team as a researcher, altho I've worked on educational materials in this context a few times.)

A well-functioning team is rather like a movie studio:  skilled specialists come together for five to ten years to produce a key new research development.

Teams work best with designated recognized roles.  For instance, there is commonly a Principal Investigator, a number of more-or-less involved co-PIs, some research scientists, some research software engineers, any number of graduate students and undergraduates, perhaps lab or hardware technicians, and a bureaucratic support apparatus.

There are some critical challenges you should keep in mind:

> As the ratio of principal investigators to students moves from 1:1 to 1:10 or 1:100, we witness the proliferation of ‘academic orphans’ — fledgling researchers who do not benefit from close interaction with a senior researcher. Treated largely as cogs in a huge machine, such academic orphans are likely to develop behavioural problems, further undermining their scientific output. (Pavlidis et al.)

> We also find that researchers persistently working in large groups tend to publish lower-impact papers. (Bu et al.)

- [Pavlidis, Petersen, & Semedeferi, “Together We Stand”](https://www.researchgate.net/profile/Alexander-Petersen-3/publication/267509944_Together_we_stand/links/545130030cf285a067c6857a/Together-we-stand.pdf)
- [Petersen et al., “Persistence and Uncertainty in the Academic Career”](https://pubmed.ncbi.nlm.nih.gov/22431620/)
- [Pentland, “The New Science of Building Great Teams”](https://www.vip.gatech.edu/sites/default/files/Harvard%20Business%20Review%20-%20The%20New%20Science%20of%20Building%20Great%20Teams.pdf)

In many fields, such as medicine and physics, almost all work is carried out by massive teams that may consist of hundreds of contributors.  This has led to a growing interest in multi-party workflow solutions (sounds like enterprise gobbledygook) or splitting teams into more modular responsibilities.


#### 5. Procedural details

Most projects require more than a laptop and an Internet connection.  Your sponsoring institution should be able to help you arrange equipment acquisition and procurement, provide a lab manager, etc.  You may also need to check with the institutional review board or equivalent body.  There are also mechanisms for acquiring civil service staff support:  secretaries, office managers, and the like.


#### 6. Data collection

Most workflow software focuses on the data collection and data analysis steps.  In fact, much of the discussion in this class has focused on these as well, since this is the effective domain of computer-aided research and reproducibility.


#### 7. Analysis

We've spent a lot of time talking about basic analysis processes using Bash, R, and Python, so we don't have a lot to add here.

Here are a few general-purpose principles to keep in mind:

- Stay grounded in your hypothesis.  A research project can explode in many directions once data start pouring in.  At least early on, stay focused on producing your article or thesis, but tag any interesting sidelines for further exploration someday.

- Be parsimonious in the number of parameters any model you build uses.  John von Neumann famously said:

    > With four parameters I can fit an elephant, and with five I can make him wiggle his trunk.
    
    - [Boué, “Real Numbers, Data Science and Chaos:  How to Fit Any Dataset with a Single Parameter”](https://arxiv.org/pdf/1904.12320.pdf)

- Don't _p_-hack your final results just to make something publishable.  (Journals are gradually becoming more open to publishing negative results.)
    
    * “Decide your statistical parameters early, and report any changes.
    * “Decide when to stop collecting data and what composes an outlier beforehand.
    * “Correct for multiple comparisons, and replicate your own result.”  (All from Amici)
    
    Readings:
    
    - [Amici, “Are You Guilty of _p_-Hacking?”](https://bitesizebio.com/31497/guilty-p-hacking/)
    - [Taleb, “A Short Note on _p_-Value Hacking”](https://www.hersephoria.com/files/books/theory/Nassim_Taleb_A_Short_Note_on_P-Value_Hacking.pdf)
    - [Stefan & Schönbrodt, “Big Little Lies:  A Compendium and Simulation of _p_-Hacking Strategies”](https://psyarxiv.com/xy2dk/)


#### 8. Writing

We'll talk more about document authoring in a later lesson.


#### 9. Sharing

We'll talk more about collaboration in a later lesson.


#### 10. Submission

This is highly journal-dependent, but you should keep in mind when writing if a journal has its own style file for LaTeX or Microsoft Word.


#### 11. Review

This may be the stage at which you, personally, are most grateful for thorough efforts undertaken to make your project reproducible.  This will speed your ability to address questions or issues raised by reviewers, as well as produce an updated product for final submission.


#### 12. Publication

Not a lot to say about this, except that it is worth your while to figure out where the most impact in your field is.  Some fields, like computer science, are actually more driven by conferences than by journal articles.


#### 13. Showcasing

For many researchers, showcasing a portfolio of your work is essential for helping the message get out to those who can use it.  It is uncommon that research finds its own legs and doesn't need someone (you!) to tell its story.  This can include news articles in trade journals or campus publications, as well as conference reports and the like.


#### 14. Assessment

After your work is published, it is in the hands of your colleagues, who may embrace it, shun it, or ignore it.  The consequences of your work may take decades to unfold.  So be patient!

At a conference recently, I met Scott Stornetta.  (Tell this story.)


#### 15. Routinization

As a researcher, you may not ever personally work on converting your research into an industrial product or insight.  But it is reasonably likely that you will run your own lab or workgroup and need to manage how peers and subordinates work with and within the research framework you've established.

(This can include technology release, patenting, transfer to industry, and the like.)

Another aspect is that some verified hypotheses or theoretical advances can suddenly yield access to a large number of low-lying fruit.  A method that worked on one author's corpus can be applied to many others.  A new insight into phonology can be applied to many language communities.  Some of this you can do directly yourself, but for the  most part you'll likely need to farm this out across other researchers.


#### 16. Termination

At some point, you will move on intellectually and professionally from any particular research program.  You'll have to decide whether you will have a successor in the project or whether it all needs to be archived, hosted somewhere, and left for the ages.  Once again, reproducibility is your best friend here, whether you yourself return to old stomping grounds or others come to examine your work.

The value of a formal framework lies in how it encourages you to be aware always of the next and preceding steps.  Naturally, many parts of the workflow bleed over into each other, altho some (like publication) are complete discrete milestone events.


##  Automation

Data collection and data analysis are most susceptible of automation.  Part of automation refers directly to computational automation, and part of it refers to embodying your tasks in management processes.  (We'll talk more about this latter on Wednesday.)

First off, you can build your own automation pipeline using some clever Python or R code as glue.

The [Center for Open Science](https://cos.io/) produces the [Open Science Framework](https://www.cos.io/products/osf), among other open science products.  OSF works as a data pipeline tool targeting publishing, with interactivity with GitHub, Jupyter notebooks, hosted storage like Dropbox, and citation platforms like Mendeley and Zotero.  It's designed to aggregate a lot of single-purpose tooling.

By my background, I am significantly more aware of scientific workflow software, altho I've also used some business workflow software.  A few projects worth checking out include:

- [Open Science Framework](https://www.cos.io/products/osf)
- [Collective Knowledge Framework](https://github.com/mlcommons/ck), which attempts to encourage researchers to build more intercompatible modules from their code to share with others in a citable way
- [Swift](http://swift-lang.org/main/) (not the Apple iOS language), a language for parallel scripting on systems which support concurrent execution (examples in physics, biology, social science, computer science, and humanities)

* Have you seen workflow tools for other domains or disciplines?

There are also a few commercial platforms out there, people selling you something.  That's fine:  there's definitely a place for just paying someone to solve your problems for you.  However, you should be wary of [vendor lock-in](https://scholarlykitchen.sspnet.org/2018/01/02/workflow-lock-taxonomy/), wherein your data and process are made incommensurable with other tools or platforms.

- [Curvenote](https://curvenote.com/) looks pretty good actually.

A good workflow system will test tools and results at various intervention points so that you can have confidence in your system's performance.  We'll discuss this in more detail next week when we talk about testing and integration.

The biggest challenge is that no one platform really does everything.  (This is one reason I personally advocate working in plain text.)  Also, not all processes really gell into a workflow:  I have some personal research projects that have never really sat well with a formal system attached.

> Scientific workflows often begin as research workflows and end up as production workflows. Early in the lifecycle, they require considerable human intervention and collaboration; later they begin to be executed increasingly automatically. Thus in the production mode, there is typically less room for collaboration at the scientific level and the computations are more long-lived. This happens partly because of limitations of the available technology. We speculate that if true workflow technology were available to manage scientific computations, there would be a reduced push to automate everything and the quality of the solutions obtained could be improved by involving the right humans at the appropriate places.
([Singh & Vouk, 1995](https://www.csc2.ncsu.edu/faculty/mpsingh/papers/databases/workflows/sciworkflows.html))

Researchers at Argonne National Laboratory identified four areas that need particular attention still in contemporary workflow software platforms:

1. Task coupling & data movement
2. Programming & usability (incl. monitoring)
3. Efficiency, scalability, & reliability
4. Validation of results

([Deelman et al., 2017](https://www.mcs.anl.gov/papers/P7063-0617.pdf))
