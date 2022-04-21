#   Document Authoring

**Objectives**

- Compose a document using internal structural features, such as automatic labeling and numbering.
- Enumerate document composition best practices.
- Employ an automated citation management tool (such as BibTeX, Zotero, etc.).

##  Document Composition

You are likely to compose a research document using one of three modalities:

1. WYSIWYG (“what you see is what you get”) tools like Microsoft Word and Google Docs.
2. Composition tools with separate renderer such as LaTeX or XeTeX.
3. Plain text files (likely Markdown).

Each of these imposes different requirements on you to match capabilities.

Before we embark on a discussion of these tools, we need to separate two processes that are often entwined:

1. _Document composition_ refers to the production of the running copy, the text itself.  Formerly this was commonly done by hand or typewriter, then sent to a publisher to be typeset.
2. _Document layout_ refers to the consideration of page structure and aesthetics and features like page numbering.


### WYSIWYG Document Composition

You are probably most used to using what-you-see-is-what-you-get document editors like Microsoft Word and Google Docs.  These allow you to visualize exactly what your end product will look like as you compose it.

One of the most common mistake casual users of Word and Docs make is to simply use formatting to indicate document features.

You must logically separate _formatting_ from _role_.  For instance, when you select text and make it bold, you only change the formatting rather than designating it as a header or associating any metadata.  If you select a block of text and set it to be a header, even if that text looks no different than surrounding copy it is logically a header.

Only values which have been designated of a certain type (such as a heading, a figure caption, or a table caption) will be included in automatic document summarization tools like a table of contents or a table of figures.

- Demonstrate producing a heading (not a header).
- Demonstrate producing a footer.
- Demonstrate producing a table of contents.
- Demonstrate producing a figure.
- Demonstrate producing a table.

#### Strengths

When used properly, WYSIWYG editors afford a principled way to structure your document.  They can automatically produce tables of contents and figures, manage headers and footers, and manage equation numbering.  However, to get these features, you must use the internal tools to produce captions, styles, etc.

Publishers frequently produce a template `.docx` file for researchers to use, and this will not work correctly unless you use the styles.

You can also nail down table and figure placement very precisely.  One of the most frustrating experiences with WYSIWYG document composition can be the placement of figures and tables.  There are several text wrapping options available, but I have found that the best solution is to insert a one-column centering table where the figure should be and simply place the figure in that table.

#### Weaknesses

The chief weakness of WYSIWYG editors is that they foment distraction by their feature sets and in particular their formatting options.  You can spend far too many hours geeking out over fonts, placement, and feature application.  (“Ask me how I know!”)

The defaults often underwhelm, not necessarily by poor design decisions (looking at _you_ Excel 2003) but because the viewer will have experienced visual saturation from prior exposure to documents composed with those defaults.  Never underestimate the premium gained by _not_ using the default settings:  if you turn in a document in Times New Roman or Calibri (and these weren't specified), it is a subtle visual signal that you didn't care.  Even switching to something similar can refresh the eye.  Consider these replacements:

For Times New Roman (serif fonts):

- [Tinos](https://fonts.adobe.com/fonts/tinos)
- [Linux Libertine](https://libertine-fonts.org/)

For Calibri and Arial (sans-serif fonts):

- Helvetica Neue (on macOS only, so be careful if not producing a PDF)
- [Open Sans](https://fonts.adobe.com/fonts/open-sans)

#### Collaboration

WYSIWYG document editors are common on the cloud:  Google Docs and Microsoft Office 365 are both commonly used and almost everyone has access to them.  However, the documents produced by these tools are not legible to version-control systems like Git, which must treat them as binary blobs and delete and re-upload the entire document for even a single line change.  


### TeX and Derivatives

TeX was invented by computer scientist Donald Knuth to author his own texts after the retirement of earlier [hot metal typesetting technology](https://www.thisiscolossal.com/2016/09/a-fascinating-film-about-the-last-day-of-hot-metal-typesetting-at-the-new-york-times/).

![](https://www.thisiscolossal.com/wp-content/uploads/2016/09/hotmetal-3.jpg)

Most users of TeX use the LaTeX macro toolset which introduces a number of helpful macros in a fully extensible system.

LaTeX is extremely powerful but not terribly user-friendly, and if you are trying to do something really specific you can struggle to get it done.  On the other hand, the document management tools (such as automatic tables of figures and internal cross-references) are second to none.

```
\documentclass{article} % Starts an article
\usepackage{amsmath} % Imports amsmath
\title{\LaTeX} % Title

\begin{document} % Begins a document
  \maketitle
  
  \section{\LaTeX}

  \LaTeX{} is a document preparation system for
  the \TeX{} typesetting program. It offers
  programmable desktop publishing features and
  extensive facilities for automating most
  aspects of typesetting and desktop publishing,
  including numbering and  cross-referencing,
  tables and figures, page layout,
  bibliographies, and much more. \LaTeX{} was
  originally written in 1984 by Leslie Lamport
  and has become the  dominant method for using
  \TeX; few people write in plain \TeX{} anymore.
  The current version is \LaTeXe.

  % This is a comment, not shown in final output.
  % The following shows typesetting power of LaTeX:
  \begin{align}
    E_0 &= mc^2 \\
    E &= \frac{mc^2}{\sqrt{1-\frac{v^2}{c^2}}}
  \end{align} 
\end{document}
```

Another example:  producing a histogram of 500 points loaded from a file `randn.dat`:

```
\begin{document}
\pagestyle{empty}

\newcommand{\mainline}{0.025in}
\begin{tikzpicture}[
declare function={
  gauss(\x)= 1/(sqrt(2*pi))*exp(-(\x^2)/2);
}
]
\begin{axis}[xmin=-4,xmax=4,ymin=0,samples=500,ybar interval,
  x tick label style={rotate=90,anchor=east},
  xticklabel=
    {$[\pgfmathprintnumber\tick,%
	   \pgfmathprintnumber\nexttick)$}]
  \addplot[yellow,ultra thick,hist={data=x}]
	file {randn.dat};
\end{axis}

\end{tikzpicture}
\end{document}
```

#### Strengths

If you are producing documents laden with mathematics, nothing can touch LaTeX for ease of expression and compatibility.

If you are managing a lot of references, including internal cross-references within a longer document, TeX shines at this.

Many publishers (such as Springer-Verlag) offer LaTeX templates for articles and books.

There are some good tools for scanning maths references and have the TeX generated. Other tools, like overleaf, can help make the process work smoother and offer collaboration.

It can provide a plain text accessible way to "write" complex maths via typing rather than by hand. 

While expansive in capability, the core set of syntax skills you need for general work is reasonable. 

#### Weaknesses

TeX and derivatives have a steep learning curve, although there is an ample user community dating back to the 1980s so you can find the answer to almost any question.

There is no good universal package management system so installing third-party packages can be a total pain.

TeX and LaTeX don't really know about Unicode so typesetting documents that use a lot of non-ASCII symbols can be more comfortably composed using the XeTeX distribution.

#### Collaboration

As plain text-based documents, `tex` files are perfectly compatible with version control tools.  Git and friends do not check for the validity of the file (as if you make a change that removes the `\\end{}` from a structure) but otherwise allow you to monitor per-line changes.

There haven't been a lot of cloud tools for direct collaboration in producing `tex` documents without leaning on version control.  The most important is [Overleaf](https://overleaf.com), which is also how we produced these documents originally.


### Plain-Text Authoring

Plain-text authoring is straightforward and particularly easy to manage with a version control system.  However, it frequently doesn't look much like an end product and internal cross-reference and citation management is _ad hoc_ and messy.

A Markdown file is formatted according to some basic conventions, such as `**bold**` for **bold** and `_italic_` for _italic_ text.  Bulleted and numbered lists, internal references, hyperlinks, and images are supported, but not much else.

Sometimes the `.md` file extension is used to denote a Markdown text file, particularly on GitHub.

The best introduction is still the original specification document.  Read the following two sections in full:

-   [Basics](https://daringfireball.net/projects/markdown/basics)
-   [Syntax](https://daringfireball.net/projects/markdown/syntax)

Use the ["Dingus" sandbox](https://daringfireball.net/projects/markdown/dingus) to test out text samples.

Note particularly that Markdown is a superset of HTML, and so you can use HTML inline when necessary to achieve a particular effect.

Markdown converts trivially to HTML.  The `markdown` tool converts `.md` to `.html` files, but we will prefer to use the even more flexible and powerful Pandoc.

[Pandoc](https://pandoc.org/) supports many specific dialects of markup languages, as well as PDF, EPUB, DOCX, and ODT output.

Pandoc can detect input formats automatically (and generally does a decent job).  Given a file [`example.md`](repo:./resources/example.md), one may convert it to a PDF thus:

```
pandoc example.md -o example.pdf
```

More sophisticated conversions can be specified, here for [`example-ghm.md`](repo:./resources/example-ghm.md), the GitHub Markdown dialect:

```
pandoc -f gfm example-ghm.md -o example-ghm.pdf
```

Pandoc supports citations via [Citation Style Language](https://citationstyles.org/), a resource with hundreds of citation styles.

#### Strengths

The composition syntax is trivial to learn and rather cosmopolitan in its adoption.

Markdown files can be converted into anything.

#### Weaknesses

Many advanced features necessary for articles and books are not supported.

The Markdown standard is often extended by particular platforms, such as to include LaTeX-style equations.  This means that one can quickly run into compatibility issues moving from Jupyter to GitHub to Pandoc etc.

#### Collaboration

Everyone can open a text file.  Not everyone will edit it perfectly, but it reads pretty smoothly even if it hasn't been converted into a fancier format.

Some text file formats and structures are a bit better for collaboration than others. For example, a markdown file or other file that keeps data entry points at a line level will be easier to handle in things like git (which is designed to act on files at the line level). Versus another structure, say json or xml without proper indents, where a single new "entry" can span multiple lines or mutate lines that are not directly relevant to the content being added. 

#### References

-   [Gruber, J.  "Markdown 1.0.1"](https://daringfireball.net/projects/markdown/)
-   ["Mastering Markdown"](https://guides.github.com/features/mastering-markdown/)


##  Managing References

### Tools

The University Library has some guidance: https://guides.library.illinois.edu/citationmanagers/help-and-training

The Savvy Researcher workshop series is something that runs all academic year and has 60+ different workshops about various research skills. They have a citation manager workshop as well as specific workshops and guides on using Zotero and Mendeley. Research groups, study groups, and classes can request to have a workshop run for their group. 

Things to think about: 

* how often will you need to collaborate with others on citations and co-authorship? (check with your partners to see what they use)
* Does your advisor or PI/supervisor/lab group use a specific one? (you may want to match the group as a starting place)
* do you want it to integrate with PDF annotation and reading? (some have better integrations than others)
* how well do the journal PDFs etc work with importing data? (there may be some domain differences in how the PDFs are parsed)
* do you need cloud storage of pdfs? (there may be paid tiers that you want to review in more detail)

Zotero

- Free and paid options
- Web, plugin, app, and desktop software options
- shared citation libraries with groups and projects

Mendeley

- BibTeX is the TeX-compatible citation manager tool.  (Indeed, several other tools can convert directly to BibTeX format.)

    BibTeX stores entries in a plain-text file.  A BibTeX entry looks like this:
    
    ```
    @Book{abramowitz+stegun,
     author    = "Milton {Abramowitz} and Irene A. {Stegun}",
     title     = "Handbook of Mathematical Functions with
                  Formulas, Graphs, and Mathematical Tables",
     publisher = "Dover",
     year      =  1964,
     address   = "New York City",
     edition   = "ninth Dover printing, tenth GPO printing"
    }
    ```

    BibTeX facilitates clean automatic conversion to virtually every citation format.

    BibTeX has the disadvantage of being very command-line-heavy to use properly.  The LaTeX source file must be compiled twice to resolve internal references, then `bibtex` is run to incorporate citations, then LaTeX is compiled again to resolve.

### Best Practices

1.  Bit rot is real.  Always archive any link and preferably include it in your citation manager.

    To archive a link, go to [`archive.is`](https://www.archive.is) and check whether the link has already been archived.  If it has not, archive it and store the archival link as well.
    
    Support for archival links is unfortunately rather rough.  For instance, in BibTeX [a new macro must be defined to support a new `archiveurl` field](https://tex.stackexchange.com/questions/302968/biblatex-add-a-second-url-where-content-is-archived).

2.  Track your research sessions because you will likely recall useful information days after you first encountered it.

    Tools such as [Vortimo](https://www.vortimo.com/) track your viewing history in great detail, allowing you to reconstruct Internet research-heavy sessions.
    
    Tree-style tab managers such as [Forest](https://gettreely.com/) allow you to reconstruct your logical path to information.
    
    Annotation tools like [Hypothes.is](https://web.hypothes.is/) help you collaboratively collect notes and observations.
