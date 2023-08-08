---
title: "Reproducible Code"
excerpt: "Writing and using reproducible code"
date: 2019-08-16
toc: true
categories:
  - Developer Resources
tags:
  - reproducible
  - developer resources
  - software
  - software user resources
  - R
---



## What is reproducibility?

"An article about computational results is advertising, not scholarship.
The actual scholarship is the full software environment, code, and data,
that produced the result." - Claerbout and Karrenbach, 1992

Reproducibility in software or science refers to the ability of others to
repeat your analyses and come up with the same result. Traditionally,
the way scientists work is not amenable to reproducibility - code is
scattered and highly customized, the steps taken to perform an analysis
are not documented or shared, and the data for the analyses are kept
private. Although there are cases where data must be
protected, we encourage striving for reproducibility when possible. While any
scholars have thought and written much about reproducibility,a good starting 
place is rOpenSci's
[reproducibility
handbook](https://ropensci-archive.github.io/reproducibility-guide/).

The NOAA Fisheries Toolbox is an example of a storage repository for
common software tools, tools which encourage reproducibility by making
shared software accessible to and tested by other researchers. However,
common software tools are only one component of making research
reproducible. A large part of reproducibility is ensuring others can
follow the steps and set up the same data and environment as you did to
complete a task. Tools to enable and simplify this include:

1. literate programming tools (i.e. `Rmarkdown`,
`knitr`, Doxygen)
2. provenance-tracking tools, in other words, tools to
track to origin and chronology of data, code, figures, and results (i.e.
`drake`, Kepler)
3. interactive notebooks
4. tools to capture or emulate a specific software environment

## Literate programming

The concept of literate programming was introduced by Donald Knuth. It
is a programming paradigm by which code is interspersed with text, with the goal
 of making computer code more readable rather than adhering to a structure imposed
by the computer. Although literate programming approaches have been
criticized for being less efficient, when attempting to create a
reproducible tool, example, or user manual, it is usually more important
to clearly convey what the software is doing than to express it in the fewest
lines of code. The most effective examples combine text and code, and we
recommend doing this in markdown when possible. [Markdown](https://www.markdownguide.org/) is a framework
for converting text to HTML and has several benefits: 

- it allows for seamless integration of code, rich text, and equations
- it can quickly generate web content (i.e. HTML pages) that can be quickly and
easily styled without the manual formatting and repositioning required
by LaTeX, for example.

Markdown can be [extended](https://www.markdownguide.org/extended-syntax/), so 
you may encounter different "flavors" of markdown. For example, when writing on
GitHub, [GitHub Flavored Markdown](https://github.github.com/gfm/) is used.

R users are likely familiar with [R markdown](https://rmarkdown.rstudio.com/) 
and [Quarto](https://quarto.org/), which are literate programming formats that use Markdown. 

## Provenance tracking

[Provenance tracking](https://rrcns.readthedocs.io/en/latest/provenance_tracking.html) 
refers to tracking the knowledge needed to recreate a scientific result, from 
raw data, to filtered data, to the code used to run the analysis, to the code 
used to create the result. This can be thought of the software analog to the 
lab notebook. Provenance tracking tools can include things
like programming notebooks and markdown. They
can also include workflow tools, which track the steps in your workflow
and which inputs and outputs were used and produced at each time. Workflow 
management tools include [Kepler](https://kepler-project.org/) and 
[targets](https://docs.ropensci.org/targets/).

## Notebooks

Interactive notebooks capture the benefits of literate programming approaches, by
incorporating descriptive text with code, as well as allowing real-time editing 
and re-running of the code. Some commonly used notebook formats are [R
notebooks](https://bookdown.org/yihui/rmarkdown/notebook.html), [Jupyter
notebooks](https://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/what_is_jupyter.html)

## Capturing/emulating software environments

Finally, an important aspect of reproducibility is perhaps so simple
it is often overlooked. If a different version of software is used, or
if paths are set to be specific to the original author, it can create a
barrier to reproducible results. This might seem like a small issue, but
it often doesn't take much to dissuade someone from creating custom code
rather than reusing a published, reproducible example. Jenny Bryan expresses why
 this  matters and what to do instead in a 
[blog post on project-oriented workflows](https://www.tidyverse.org/articles/2017/12/workflow-vs-script/).

Luckily, there are a number of tools you can use to capture software
environments, emulate them in remote instances or on different
computers, or simply clearly document the dependencies and versions
required to run your software. 

One way to do this is to use virtual instances, such as virtual machines. You can use desktop
applications, such as VMware or VirtualBox, or remote instances using
virtual machines on cloud instances like Amazon Web Services (AWS) or
Microsoft Azure. Such instances can be helpful to test out
software to work on multiple environments; for example, if you are
programming on a Mac but would like to ensure Windows users can run your
code. More lightweight options for reproducing a work environment are web-based 
remote containers for software environments, such as [conda](https://docs.conda.io/en/latest/) and
[Docker](https://www.docker.com/) (however, Docker is no longer free for government use). 
Other options include:

- [Binder](https://mybinder.org/)
- [Holepunch](https://github.com/karthik/holepunch)
- [Jupyter and conda for R](https://anaconda.org/chdoig/jupyter-and-conda-for-r/notebook)
