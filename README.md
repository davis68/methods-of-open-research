#   Interdisciplinary Methods in Research Computing
##  ENG 498IM/IS 497/CSE 498 · Spring 2O22
##  Elizabeth Wickes (IS) · Neal Davis (CS)

#   Methods in Open Research
##  CS 498MOR/IS 497MOR

Instructors:
- Elizabeth Wickes (IS)
- Neal Davis (CS)

Advisors:
- André Schleife (MatSE)
- Richard Sowers (Math+ISE)
- Jake Bowers (Poli Sci)
- Matt West, 2020–21 (AE3)
- Marcia Pool, 2021–22 (AE3)

##  Course-Level Learning Objectives

At the conclusion of this course, students should be able to

1. Conduct research using best practices of open science and open research communities.
2. Reason critically about data and using data.
3. Compose the pieces of a functional workflow as a competent member of a research group and/or in the context of a research application.

##  Lessons

- [Spring 2021 Moodle site](https://learn.illinois.edu/course/view.php?id=55405)
- [Spring 2022 Canvas site](https://canvas.illinois.edu/courses/16488/)

### Data Management

1. Project Organization & Management [1 lesson]
  - Objectives:
    - Think about and understand the types of metadata an experiment will generate.
    - Understand the importance of metadata and potential metadata standards.
    - Employ the ETL (Extract/Transform/Load) process to and summarize statistics of a previously-unfamiliar data set.
    - Make decisions about how data and code will be stored, archived, and shared.
    - Distinguish between quantitative and qualitative categorizations of data.
  - Software:
    - Any modern text editor ([Sublime Text](https://www.sublimetext.com/), [Atom](https://atom.io/), [VS Code](https://code.visualstudio.com/), [Notepad++](https://notepad-plus-plus.org/))
  - Readings:
    - [“Managing Research Software Projects: Introduction”](https://swcarpentry.github.io/managing-research-software-projects/01-intro/)
    - [“The Reinhart-Rogoff error—or how not to Excel at economics”](https://theconversation.com/the-reinhart-rogoff-error-or-how-not-to-excel-at-economics-13646)
    - [“Managing Research Data”](https://www.ideals.illinois.edu/bitstream/handle/2142/88861/ManagingResearchDataCompSocSci2016.pdf?sequence=2&isAllowed=y)
    - [“Evidence of Fraud in an Influential Field Experiment About Dishonesty”](http://datacolada.org/98)
    - [“Time to assume that health research is fraudulent until proven otherwise?”](https://blogs.bmj.com/bmj/2021/07/05/time-to-assume-that-health-research-is-fraudulent-until-proved-otherwise/)
    - [Noble, “A quick guide to organizing computational biology projects”](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1000424)
    - [Data Carpentry, “Spreadsheets for Social Science”](https://datacarpentry.org/spreadsheets-socialsci/)
  - Data files:
  - Assignments:
    - Quiz
2. Data Organization in Spreadsheets [1 lesson]
  - Objectives:
    - Enumerate principles of good data entry and structure.
    - Formulate an argument for using CSV as the standard spreadsheet file type.
    - Avoid common formatting problems with spreadsheets.
  - Software:
    - Any spreadsheet program:  [Microsoft Excel]() or [LibreOffice](), for instance.
  - Readings:
    - [“Data Organization in Spreadsheets for Ecologists”](https://datacarpentry.org/spreadsheet-ecology-lesson/)
  - Data files:
    - `Towed Vehicles (messy data).xlsx`
    - `Tidy Data`
    - `GDP/Debt by Countries.xlsx`
`
  - Assignments:
    - Quiz
3. Data Cleaning with OpenRefine [1 lesson]
  - Objectives:
    - Explain the ETL (extract–transform–load) process for data sets.
    - Create an OpenRefine project from a CSV file.
    - Identify data facets.
    - Use clustering to clean data.
    - Filter and refine data.
    - Clean a data source in a reproducible and repeatable manner.
  - Software:
    - [OpenRefine](https://docs.openrefine.org/manual/installing)
  - Readings:
    - [“About OpenRefine”](https://guides.library.illinois.edu/openrefine)
    - [“Data Cleaning with OpenRefine for Ecologists”](https://datacarpentry.org/OpenRefine-ecology-lesson/)
    - [“OpenRefine:  Clean Your Data”](https://uidaholib.github.io/clean-your-data/5-resources.html)
  - Data files:
  - Assignments:
    - Quiz

### Process Management

4. Scripting for Automation at the Command Line [2 lessons]
  - Objectives:
    - Navigate files and directories using the shell.
    - Carry out basic file operations using the shell.
    - Employ pipes and filters to control the flow of data at the shell.
    * Build loops to repeat iterated operations.
    * Compose a short shell script.
  - Software:
    - Mac:  [Terminal](https://support.apple.com/guide/terminal/welcome/mac) (already installed)
    - Windows:  [Git for Windows/Git Bash](https://gitforwindows.org/)
  - Readings:
    - [The Unix Shell](https://swcarpentry.github.io/shell-novice/)
  - Data files:
  - Assignments:
    - Quiz

5. Managing Project History and Changes with Git [2 lessons]
  - Objectives:
    - Use a graphical user interface to set up a local repository.
    - Place documents under version control.
    - Track and revert changes using version control.
    * Utilize GitHub as a remote repository.
    * Collaborate using a common remote repository.
    * Resolve conflicts resulting from a merge.
  - Software:
    - Mac:  [Git](https://git-scm.com/download/mac)
    - Windows:  [Git for Windows/Git Bash](https://gitforwindows.org/)
  - Readings:
    - [“Version Control with Git”](http://swcarpentry.github.io/git-novice/)
    - [Wickes, “Version Control Tutorial”](https://uofi.box.com/s/ytww3uqwwxmk9per2vy15mfpnebna8ov)
    - Optional: [Chacon & Straub, _Pro Git_](https://git-scm.com/book/en/v2)
    - Optional: [GitHub, “Git Commit Message Standard”](https://gist.github.com/turbo/efb8d57c145e00dc38907f9526b60f17)
    - [Wickes, “Getting started with GitHub (for text documents)”](https://github.com/elliewix/github-training-brain-dumps/blob/master/github_directions_text_only.md)
    - [Wilson et al., “Keeping Track of Changes”](https://uofi.box.com/s/mqzpmx563ewf2yph89w1cubw65659ltx) (from [“Good enough practices in scientific computing”](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005510))
    - [Wilson et al., “Manuscript Versioning Control”](https://uofi.app.box.com/s/fqvazy0ugxr0xb0uj5u87u7b2e9czpvn) (from [“Good enough practices in scientific computing”](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005510))
  - Data files:
  - Assignments:
    - Quiz
6. Scripting for Reproducibility
    1. Python track (simultaneous with R) [5 lessons]
      - Objectives:
        * Write programs that assign scalar values to variables and perform calculations with those values.
        * Distinguish basic data types.
        - Write programs that import and use libraries from Python’s standard library.
        - Use a library function to get a list of filenames that match a wildcard pattern.
        - Write a for loop to process multiple files.
        * Enumerate ways of working with Python code (scripts, Jupyter notebooks).
        * Define a function that takes parameters.
        * Explain why we should divide programs into small, single-purpose functions.
        * Identify the points of cleavage in a process which yield logical modular functions.
        * Test and debug a function.
        * Explain what software libraries are and why programmers create and use them.
        * Compose an importable library in a standalone file.
        - Provide sound justifications for basic rules of coding style.
        - Refactor one-page programs to make them more readable and justify the changes.
        - Adhere to Python community coding standards ([PEP-8](https://www.python.org/dev/peps/pep-0008/), [Flake8](https://flake8.pycqa.org/en/latest/), [_Black_](https://pypi.org/project/black/)).
        - Explain what test-driven development is, and use it when creating new functions.
        - Operate a code review.
        * Load and process tabular data using Pandas.
        * Apply operations to and across data fields in Pandas data frames.
        * Reason about data transformations in data frames.
    - Software:
      - Mac:  [Anaconda Python](https://docs.anaconda.com/anaconda/install/mac-os/)
      - Windows:  [Anaconda Python](https://docs.anaconda.com/anaconda/install/windows/)
    - Readings:
      - [Programming with Python](http://swcarpentry.github.io/python-novice-inflammation/)
      - [Plotting and Programming in Python](http://swcarpentry.github.io/python-novice-gapminder/)
    - Lesson:
    - Data files:
    - Assignments:
      - Quiz
    2. R track (simultaneous with Python) [5 lessons]
      - Objectives:
         * Write programs that assign scalar values to variables and perform calculations with those values.
         * Distinguish basic data types.
         - Write programs that import and use common libraries.
         - Use a function to get a list of filenames that match a wildcard pattern.
         - Write a for loop to process multiple files.
         * Enumerate ways of working with R code (plain text in simple editors and RStudio, R+Markdown, and Jupyter notebooks).
         * Define a function that takes parameters.
         * Explain why we should divide programs into small, single-purpose functions.
         * Test and debug a function.
         * Explain what software libraries are and why programmers create and use them.
         * Compose an importable R package.
         - Provide sound justifications for basic rules of coding style.
         - Refactor one-page programs to make them more readable and justify the changes.
         - Use R community coding standards (try styler and lintr and formatR).
         - Explain what test-driven development is, and use it when creating new functions.
         - Operate a code review.
         * Load and process tabular data using base R, tidyverse, and `data.table`.
         * Apply operations to and across data fields in data frames using base R, tidy, and data.table approaches
         * Reason about data transformations in data frames.
      - Software:
        - [RStudio](https://www.rstudio.com/)
      - Readings:
        - [Programming with R](http://swcarpentry.github.io/r-novice-inflammation/)
        - [R for Reproducible Scientific Analysis](http://swcarpentry.github.io/r-novice-gapminder/)
      - Lesson:
      - Data files:
      - Assignments:
        - Quiz
7. Visualizing Data [1 lesson]
  - Objectives:
    - Articulate a model of building effective plots.
    - Distinguish types of plots and their utility (particularly print v. web products).
    - Visualize unstructured and discrete data.
  - Software:
  - Readings:
    - [Jean-Luc Doumont, _Trees, maps, and theorems_](https://www.principiae.be/book/)
    - [Edward Tufte, _The Visual Display of Quantitative Information_](https://www.edwardtufte.com/tufte/books_vdqi)
    - [Leland Wilkinson, _The Grammar of Graphics_](https://link.springer.com/book/10.1007%2F0-387-28695-0)
  - Lesson:
    - Assess examples of visuals.
  - Data files:
  - Assignments:
    - Quiz
8. Visualizing Data using a Scripting Language [1 lesson]
    1. Python track (simultaneous with R) [1 lesson]
      - Objectives:
        - Produce publication-quality plots using `matplotlib`.
        - Compose a script to produce publication-quality plots in a repeatable manner.
      - Software:
        - Python
      - Readings:
      - Lesson:
      - Data files:
      - Assignments:
        - Quiz
    2. R track (simultaneous with Python) [1 lesson]
      - Objectives:
        - Produce publication-quality plots using `ggplot`.
        - Compose a script to produce publication-quality plots in a repeatable manner.
      - Software:
        - RStudio
      - Readings:
      - Lesson:
      - Data files:
      - Assignments:
        - Quiz
9. Interacting with Data (Widgets) [1 lesson]
  - Objectives:
    - Use notebook widgets to visualize system behavior.
    - Create a basic widget to examine the behavior of a function or equation.

### Project Management

10. Workflows & Lifecycles [1 lesson]
  - Objectives:
    - Employ a framework for embarking on a research program (such as the Heilmeier Catechism).
    - Build automatic tools to manage portions of your data analysis.
    - Explain the standard project lifecycle, from conceptualization to termination.
    - Consider what the standard project lifecycle looks like in practical research software and research program efforts.
11. Task Management [1 lesson]
  - Objectives:
    - Enumerate models of basic project management (such as waterfall, Agile, etc.) and explain objectives and rationales of each.
    - Relate project management to a research program.
    - Employ an issue-tracking system such as kanban to organize project tasks and deliverables.
    - Create a suitable metadata and tagging system for your research project (_à la_ Zettelkasten).
12. Testing & Continuous Integration [1 lesson]
  - Objectives:
    - Identify the role of testing in a production workflow.
    - Enumerate several forms of testing.
    - Build a set of basic tests for your project.
    - Implement a continuous integration server.
  - Readings
    - [Scopatz & Huff, _Effective Computation in Physics_](http://physics.codes/)
    - [Introduction to Testing (and Continuous Integration)](https://people.bath.ac.uk/rjg20/training/intro-testing/)
    - [Python Testing and Continuous Integration](https://carpentries-incubator.github.io/python-testing/) (TravisCI material slightly out-of-date)
13. Data Entry & Storage with SQL [2 lessons]
  - Objectives:
    - Identify and distinguish a table, a record, and a field.
    - Explain the difference between a database and a database manager.
    - Compose queries to select and filter basic data.
    * Define aggregation and give examples of its use.
    * Write queries that compute aggregated values and trace their execution.
    * Distinguish between atomic and non-atomic values.
    * Explain why every value in a database should be atomic.
    * Explain what a primary key is and why every record should have one.
    * Identify primary keys in database tables.
  - Readings
    - [Using Databases and SQL](http://swcarpentry.github.io/sql-novice-survey)
14. Working with Databases using a Scripting Language [1 lesson]
  1. Python track (simultaneous with R) [1 lesson]
    - Objectives:
      - Set up a new database from scratch for a research project.
      - Populate a database automatically using a script, API, or database UI tool.
      - Explain why database entries should not contain redundant information.
  2. R track (simultaneous with Python) [1 lesson]
    - Objectives:
      - Set up a new database from scratch for a research project.
      - Populate a database automatically using a script, API, or database UI tool.
      - Explain why database entries should not contain redundant information.

### Productive Collaboration

15. Document Authoring [1 lesson]
  - Objectives:
    - Compose a document using internal structural features, such as automatic labeling and numbering.
    - Enumerate document composition best practices.
    - Employ an automated citation management tool (such as BibTeX, Zotero, etc.).

16. Collaboration, Licensing & Legal [1 lesson]
  - Objectives:
    - Examine coordination strategies for distributed online projects.
    - Articulate a rationale for a strategy you would select if your research project involved multiple collaborators.
    - Learn how to share datasets and papers online using services like ArXiv.org and OrcID.
    - Explain why including licensing information with a project is important.
    - Choose a proper license for a particular intent.
    - Explain differences in licensing and social expectations.
    - Make your work easy to cite.

17. Reproducibility [1 lesson]
  - Objectives:
    - Describe best practices for creating reproducible products and explain the justification for each.
    - Produce and document a project (script plus data files) capable of recreating an entire final product.
    - Distinguish strengths and weaknesses of various build management systems.
    * Access a Docker image containing scripts and data.
    * Reproduce a pre-packaged pipeline to reproduce published results.
    * Construct a simple container containing data and scripts for reproducibility.
    https://carpentries-incubator.github.io/docker-introduction/

---

Total lessons:  ~23

##  Assessment

### Grading

| Component | Number | Value per Assignment | Notes |
| --------- | ------ | -------------------- | ----- |
| Homework  | 
| Project   | | | Variable points per milestone and final |
| Quiz      |

### Long-Term Assessment

- Beginning of course assessment (comfort with tasks)
- End of course assessment (comfort with tasks, largely identical)
- Consent to follow-up survey
