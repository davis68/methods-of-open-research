# Reproducibility & Open Research

## Objectives

- Understand the aims of the open research community.
- Enumerate options for publishing reproducible research
- Describe best practices for creating reproducible products and explain the justification for each.
- Produce and document a project (script plus data files) capable of recreating an entire final product.
- Distinguish strengths and weaknesses of various build management systems.
- Walk through a WholeTale reproducible project and assess compatibility.
  * Access a Docker image containing scripts and data (via WholeTale).
  * Reproduce a pre-packaged pipeline to reproduce published results.
  * Construct a simple container containing data and scripts for reproducibility.

##  Why Reproducibility Matters

Our framing objective throughout the semester has been the conduct of “open research”.  Open research embraces transparency in data sources, analytical procedures, hypothesis generation, and documentation and publication.

Without the capacity to produce an artifact on demand, the artifact is by definition irreproducible.  In some fields, the reproducibility crisis has focused on massive invalidation of research results due to failure t replicate.  Building an open research distributable augments confidence in your own work by making it clear to reviewers and researchers how results were obtained, how they should be used, and any assumptions made about the data and analysis involved.

Alston & Rick enumerate eight benefits of reproducible research:

1. “Reproducible research helps researchers remember how and why they performed specific analyses during the course of a project.”
2. “Reproducible research enables researchers to quickly and simply modify analyses and figures.”
3. “Reproducible research enables quick reconfiguration of previously conducted research tasks so that new projects that require similar tasks become much simpler and easier.”
4. “Conducting reproducible research is a strong indicator to fellow researchers of rigor, trustworthiness, and transparency in scientific research.”
5. “Reproducible research increases paper citation rates and allows other researchers to cite code and data in addition to publications.”
6. “Reproducible research allows others to learn from your work.”
7. “Reproducible research allows others to understand and reproduce a researcher's work.”
8. “Reproducible research allows others to protect themselves from your mistakes.”

- [Jesse Alston, Jessica Rick, “A Beginner's Guide to Conducting Reproducible Research
”](https://esajournals.onlinelibrary.wiley.com/doi/full/10.1002/bes2.1801) (for ecology and evolutionary bioleogy)

A related ideal, _literate programming_ refers to an ambitious goal that documentation and code/analysis result from the same source documents.  This is frequently far too ambitious for research software, but there are several very good ideas to steal from the literate programming community.

- [Randall LeVeque, “Literate Programming”](https://faculty.washington.edu/rjl/lprr.html)

### What Reproducibility Isn't

Reproducibility is a _sine qua non_ of open research, but it narrowly refers to how a particular set of results were obtained and reported.

Reproducibility should not be confused with _replicability_, which requires the generation as well of new independent data for the analysis.

Reproducibility is also distinct from _open access_, which mandates that publications should be available to the public without a paywall.

## Open Research

We have repeatedly emphasized that your research should be automated and reproducible, but for the most part we have framed this as a desirable step for managing your own research and demonstrating confidence and reliability in your code-derived results.  When it comes to publishing reproducible research, however, the landscape is varied and it can be difficult to navigate how to work and communicate your results in a nontraditional way.

We will define "open research" as open access to results, transparency around the process (including analysis and peer review), and access to the data and scripts used to produce the final product.

> Under the status quo, science is shared through a single vehicle: Researchers publish journal articles summarizing their studies’ methods and results. The key word here is summary; to write a clear and succinct article, important details may be omitted. Journal articles are vetted via the peer review process, in which an editor and a few experts assess them for quality before publication. But – perhaps surprisingly – the primary data and materials underlying the article are almost never reviewed. (Gilbert)

I here argue that research and science should be open:  you are free of course to form your own opinions on the matter.  Open research is based on a number of common statements that hearken back to the 17th-century dawn of modern scientific practice.  For instance, the Panton Principles (Cambridge/Open Knowledge Foundation) state:

1. When publishing data make an explicit and robust statement of your wishes.
2. Use a recognized waiver or license that is appropriate for data.
3. If you want your data to be effectively used and added to by others it should be open as defined by the Open Knowledge/Data Definition – in particular non-commercial and other restrictive clauses should not be used.
4. Explicit dedication of data underlying published science into the public domain via Public Domain Dedication and Licence (PDDL) or Creative Commons Zero Waiver (CCZero) is strongly recommended and ensures compliance with both the Science Commons Protocol for Implementing Open Access Data and the Open Knowledge/Data Definition.

Related to this, preregistration of hypotheses can be an important element to diminish the temptation to $p$-hack and increase the likelihood of publishing null-hypothesis results.

The [Center for Open Science](https://osf.io/) is preeminent among several initiatives to both audit the state of reproducibility of existing studies and promote the use of best practices.  COS organizes papers, data, and supporting materials, shows how to design research programs, and provides an e-print server including hosting for data and code.

What's the trouble with open research?

1. There aren't good scripts for it yet.  Figuring out how to work openly can be difficult, and more so if you ever publish something incorrect.
2. Institutionalized habits.  Related, more traditional 20th-century style researchers and publishers prefer to just do things the old way and push back against the use of newer (and potentially less prestigious) journals and platforms.  'Part of the research community is uncomfortable with the inherent messiness of innovation and do not want others to see the process unfold. Others want to protect their “ideas” due to the competitive environment that is science today, created largely by the way funding science and tenure works.' (Will Schroeder)  "Career progression critically depends on the number of first and last author publications in high-profile journals."  (Allen & Mehler)
3. Fear of being scooped.  (_Lucky Jim_'s minor plot)
4. Requirement of new funding models for publishers.  Without paywalls, large traditional publishers struggle to see the value in publishing journals.  Without support, it is difficult to maintain dedicated editors and online platforms indefinitely.
5. What if something goes wrong?  "The more restrictive structures of open science can result in mistakes having greater ramifications than within a more closed approach. Transparent documentation and data come with higher error visibility, and the flexibility to avoid acknowledging mistakes is lost."  (Allen & Mehler)

- [Christopher Allen & David Mehler, "Open science challenges, benefits and tips in early career and beyond"](https://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.3000246) [highly recommended read]
- [Dan Gezelter, "What exactly is Open Science?"](http://openscience.org/what-exactly-is-open-science/)
- [Elizabeth Gilbert, "What Is “Open Science”? (And Why Some Researchers Want It)", _Futurism_](https://futurism.com/what-is-open-science-and-why-some-researchers-want-it)
- [Tal Yarkoni, "I Hate Open Science"](https://www.talyarkoni.org/blog/2019/07/13/i-hate-open-science/)
- [Azoulay et al., "The career effects of scandal: Evidence from scientific retractions"](https://www.sciencedirect.com/science/article/abs/pii/S0048733317301154?via%3Dihub)


## Journals

By following the automation and workflow pipeline we've described throughout this course, you're in good stead to submit your work to an open research journal.

Several journals have adopted an ethos of open science/open research, ranging from open access to publishing code and analysis artifacts.  Among these are the following:

- _Public Library of Science_ (PLOS), open access

- _Open Science Journal_ (OSJ), open research

- _Journal of Open Source Software_ (JOSS)

- _Empirical Software Engineering Journal_ (ESEJ)

- _Open Library of Humanities_ (OLH)

- _Journal of Open Source Education_ (JOSE)

- _Journal of Computational Science Education_ (JOCSE)

    > The Journal of Computational Science Education is intended to provide an outlet for high quality papers describing successful computational science instructional materials and projects and research on the efficacy of instruction with computational science.

Preprint and e-print services, such as [arXiv](https://arxiv.org/), also provide a way to make your research available to all.

Preprint services do not provide peer review, only hosting and some nominal topical organization.  (This touches on an interesting question around the structure of modern capital-S Science, such as Grigori Perelman's 2002 work in geometrization which he never submitted for peer review.)

> A well-known example of the latter is an outline of a proof of Thurston's geometrization conjecture, including the Poincaré conjecture as a particular case, uploaded by Grigori Perelman in November 2002. Perelman appears content to forgo the traditional peer-reviewed journal process, stating: "If anybody is interested in my way of solving the problem, it's all there on the arXiv – let them go and read about it". Despite this non-traditional method of publication, other mathematicians recognized this work by offering the Fields Medal and Clay Mathematics Millennium Prizes to Perelman, both of which he refused.


## Penumbra

Preparing code for release can be time-consuming, but the adoption of an existing supported framework can give your code much broader access than it would otherwise have as a simple GitHub repo.

- The [Collective Knowledge Framework (CK)](https://ck.readthedocs.io/en/latest/src/introduction.html) seeks to produce a standard metadata-enabled format for sharing projects and components via a unified workflow interface.  CK currently focuses on machine learning-enabled research.

- [Figshare](https://figshare.com/) is an open access repository for figures, datasets, and other supporting materials.  See also [Dryad](https://datadryad.org/stash) and [ORCID](https://orcid.org/); these are independent but tightly coupled initiatives.

- The [Open Science Framework (OSF)](https://osf.io/) is an open-science platform for hosting primary and supporting materials, including graphics, data, slides, handouts, and other ephemera that often do not survive in a discoverable format.

- The [Whole Tale](https://wholetale.org/) project "[builds] a scalable, open source, web-based, multi-user platform for reproducible research enabling the creation, publication, and execution of _tales_—executable research objects that capture data, code, and the complete software environment used to produce research findings."

Some domains have arranged their own platforms:

- [nanoHUB](https://nanohub.org/) is a nanotechnology-oriented platform for modeling, teaching, developing software, and publishing results and materials.

Of course, the trick with each of these is that you have to use them for them to be effective!  That is, you have to do some planning up front on the structure of your code artifacts so that they are compatible with the platform's expectations.

Digital Object Identifiers (DOIs) can be used to uniquely locate an article or data online.  DOIs remain persistent even if the redirection changes.  At this point, most of the platforms we've mentioned above can help broker access to a DOI when you publish your research.

Related to DOI-enabled indexing, [DataCite](https://datacite.org/value.html) among others is working to promote the production and publication of research data as a citeable and promotion-legible accomplishment.

- [Webinar, "A Critical Analysis of the Scientific Reform Movement" (4/20)](https://cos-io.zoom.us/webinar/register/8516185066074/WN_jb5oZNFWTw-4i3ifNwCuMQ)

Questions to consider:

- What are the benefits of openness v. embargo v. closed processes?
  - GIS data usage, patentability, weapons/cryptography/national security, medical data, political implications


##  Build Management

At a minimum, your distributable product should include the data and code required to validate your results.  It is even better if all of your analysis is transparent enough that one can easily map tables and claims in your reports to particular data and calculations (_provenance_).

As a laudable stretch goal, your distribution may include everything necessary to reproduce the core documents and images as well.

Operating systems have significant mutual incompatibilities, such as the Windows' `.exe` binary executable files or `.bat` batch scripts versus Unix-style binaries or `.sh` shell scripts.  Or again, consider Windows backslash folder separaters `\` versus macOS/Linus forward slash folder separators `/`.  If you have worked carefully in a reasonably portable scripting language, then many or all issues can be avoided, but full portability is rarely achievable in practice.

For instance, in Python one can avoid Windows/macOS/Linux file path incompatibility by preferring to use the `os.path` library whenever dealing with files.

### Tools for Build Management

The most venerable build tool is Make, which builds targets based on a strictly formatted script linking inputs and outputs.  Make has been widely used in software development since the 1970s, but its shortcomings have led many developers to prefer other tools in recent years.

For instance, to produce a LaTeX PDF document from source `.tex` files, one could use the following Makefile:

```
filename=MAIN_LATEX_FILE_NAME_WITHOUT_.tex

pdf: ps
	ps2pdf ${filename}.ps

pdf-print: ps
	ps2pdf -dColorConversionStrategy=/LeaveColorUnchanged -dPDFSETTINGS=/printer ${filename}.ps

text: html
	html2text -width 100 -style pretty ${filename}/${filename}.html | sed -n '/./,$$p' | head -n-2 >${filename}.txt

html:
	@#latex2html -split +0 -info "" -no_navigation ${filename}
	htlatex ${filename}

ps:	dvi
	dvips -t letter ${filename}.dvi

dvi:
	latex ${filename}
	bibtex ${filename}||true
	latex ${filename}
	latex ${filename}

read:
	evince ${filename}.pdf &

aread:
	acroread ${filename}.pdf

clean:
    rm -f ${filename}.{ps,pdf,log,aux,out,dvi,bbl,blg}
```

and used as

```
make               # to compile to PDF
make && make read  # to compile and read
```

<!--  $$ stub to satisfy Overleaf Markdown -->

There are other Make-like tools as well, but these tend to target software developers rather than researchers.  These include Apache Maven, Nix, and CMake.

- [Eric Ma, “A Simple Makefile for LaTeX”](https://www.systutorials.com/a-simple-makefile-for-latex/)
- [Software Carpentry, “Automation and Make”](https://swcarpentry.github.io/make-novice/)

[Snakemake](https://snakemake.github.io/) is a Python-based tool focused on reproducible data analysis.

> The central idea of Snakemake is that workflows are specified through decomposition into steps represented as rules. Each rule describes how to obtain a set of output files from a set of input files.

- [Felix Mölder et al, “Sustainable data analysis with Snakemake”](https://f1000research.com/articles/10-33/v2)

A related effort focuses on making as much research software code as possible portable across projects.  Exemplars include:

- [CK Framework](https://ck.readthedocs.io/en/latest/src/introduction.html)
- [Haiyan Meng et al, “An Invariant Framework for Conducting Reproducible Computational Science”](https://www.sciencedirect.com/science/article/abs/pii/S1877750315000502)


##  Building a Reproducible Distributable Container

Whole Tale's model recognizes six components of reproducibility which must be coordinated across the published product:

1. Data
2. Metadata (OrcID, etc.)
3. Publications (DOI, document generation)
4. Provenance (e.g., which data set led to which result?)
5. Environment (mainly Docker container configuration)
6. Frontend (e.g., Jupyter notebook or R scripts)

### A Quick and Dirty Intro to Docker

Docker is a container service.  What that means is that it essentially provides sandboxes, or containers of code which can operate “on top of” the operating system but without affecting permanent state.  (You can think of this like incognito tabs for a browser.)  It's not the only solution, and likely not the simplest, but it is the most widespread.

While Docker is mainly used for cloud services and software development, research software engineers have begun to use it as a way of distributing code, data, and documentation packages in a reproducible way.  The most prominent project in this vein is [Whole Tale](https://wholetale.org/), which has been building infrastructure to support research publication using Docker.

A Docker _image_ is the Platonic archetype of the environment.  It is specified by a _Dockerfile_ which contains a set of instructions used to build the environment exactly.  A particular instance of the image which is actually running is known as a _container_.  Every container begins in the same state from the image definition; thus, Docker is a reproducible environment.

- [Carpentries Incubator, “Reproducible Computational Environments Using Containers: Introduction to Docker”](https://carpentries-incubator.github.io/docker-introduction/)

### Exploring Published Distributables

1. Navigate to [Whole Tale](https://wholetale.org/).
2. Click `Explore`.
3. Choose one of the Featured Tales such as the “LIGO Tutorial” or “Predicting the Properties of Inorganic Materials”.
4. Attempt to build and reproduce the results using the Whole Tale container.

### Exploring Infrastructure Setup (Optional)

1. From the main page of the Tale Dashboard you arrived at before, select the `Files` tab.
2. Examine the files such as `docker.bs` and the Jupyter `.ipynb` files.  (The Docker-related files are largely boilerplate which you as researcher won't need to work with too much.)

    Most of the Tales are based on the [`jupyter/all-spark-notebook`](https://hub.docker.com/r/jupyter/all-spark-notebook) Docker image.  You can see the base [`Dockerfile`](https://github.com/jupyter/docker-stacks/blob/master/all-spark-notebook/Dockerfile) online.

Whole Tale represents the current gold standard for reproducible research.  This or a similar hosted approach will make any research immediately accessible and transparent to your peers.

See also the Center for Open Science's [Open Science Framework](https://osf.io/), which is an all-in-one platform similar in some regards to Whole Tale.

The downside, of course, is the amount of work required to get everything coordinated and into the right format.  Alston & Rick cite complexity, technological change, human error, and intellectual property rights as barriers to full adoption of reproducible research methods.

### Exercise

- Walk through the "Informatics-aided bandgap engineering for solar materials" publication at WholeTale.
