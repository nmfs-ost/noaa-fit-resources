---
title: "Dependency Management"
excerpt: "How to declare and manage software dependencies, and maintain backwards compatibility where appropriate"
date: 2019-07-16
toc: true
categories:
  - Developer Resources
tags:
  - backwards compatibility
  - software
  - developer resources
  - R

---


## Introduction

Most tools have dependencies on other software packages. For example, if
you write code in `R` you likely depend on both the version of the `R`
language and other `R` packages, while if you write in `C++` you may need to use
specific compilers. Most software will be supported differently by different operating systems.

This guide aims to clarify how to declare and manage software dependencies, as well as how to deal
with backwards compatibility.

## Declaring/listing dependencies

A first and necessary step is to make it **very clear** to the user what 
dependencies your software needs to run. This
sounds simple, but very few tools actually do this adequately. Different languages 
have different places for this (e.g., For R packages, it is standard to list the 
dependencies in the DESCRIPTION file). If there is no other guidance, one of the 
best places to declare dependencies is on your Github repository's README page.
You can simply create a "Dependencies" header in the README and list 
the dependencies out. 

### The DESCRIPTION file in R packages

In `R`, dependencies are listed within the package directory in a file
named "DESCRIPTION" (note, there is no file extension). You
should include which `R` version is needed to run your package under
"Depends:". There are two ways to include package dependencies - `R`
packages that are required for your software to run should be declared
under the "Imports:" section of your DESCRIPTION file, while packages
that are helpful (i.e. to run examples or the user manual) can be
listed under "Suggests:". Ideally, you can also specify which version of
each package your package depends upon in parentheses following the
package name.

A best practice is to try to limit dependencies where possible some strategies 
include:
- If a package is only used in one or two "optional" functions, you can list it under "suggests."
- Limit use of R packages that have a lot of dependencies themselves

More details are covered in the [The R packages book](http://r-pkgs.had.co.nz/description.html#dependencies).

## Backwards compatibility

It is admirable to want to make software work with older software
versions of dependent packages. However, to ensure backwards compatibility, the
software should be explicitly tested with multiple versions. This can create headaches as the number
of situations to test balloons quickly. For this reason, we think
it is important to maintain backwards compatibility only when previous
versions of software have a legitimate reason for use and continue to be
used by a large variety of users. If it is expected that users continue
to move forward (for example, updating their `R` version), there is no
need to support backwards compatibility.

If backward compatibility is maintained, we recommend using [GitHub
Releases](https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository) or [tags](https://git-scm.com/book/en/v2/Git-Basics-Tagging)
to release older, backwards compatible software. This way,
newer software can continue to be released while a stable build that
supports older software versions is maintained. More information is available in
the [GitHub best practices post](https://noaa-fisheries-integrated-toolbox.github.io/resources/developer%20resources/best-practices-version-control/#software-versioning-and-github-releases).
