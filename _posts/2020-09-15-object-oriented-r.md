---
title: "Resources for object-oriented programming in R"
excerpt: "Overview of object-oriented programming systems in R"
date: 2020-09-15
toc: true
categories:
  - Developer Resources
tags:
  - developer resources
  - R
  - software
---



## What is object and object-oriented programming (OOP)?


From J.Niño and F.Hosch (2008):
An object is "a software abstraction representing some data component to be manipulated by the system".
OOP refers to "a method of software development in which the system is organized around data objects".
Using OOP, we can use modular pieces of code to build complex models or large systems.


## OOP systems in R


Based on H.Wickham (2019):
R supports OOP. S3, S4, and Reference classes (RC) are the three main OOP systems in R. An object from these systems contains both classes and methods. Classes include the type and data fields of an object. Methods are implemented in a class and define the behavior of the class.

S3 is from base R and was the first OOP system available in R. It's a functional OOP, where objects contain data while methods are defined separately from an associated class. It is the most commonly used OO system and is flexible and friendly to use.

S4 from base R is a more formal and rigorous system. It's still a functional OOP, but requires more careful program design.

RC is available in base R as well, and builds off of S4. RC implements encapsulated OOP and is mutable (not usual copy-on-modify semantics found in R).

There are multiple CRAN packages that provides OOP for R. For example, R6 is one package that is similar to RC from base R but more lightweight. R6 has comprehensive online documentation and shows promising performance in comparison tests.


## OOP applications in marine science field


- [Fishery Library in R (S4 Classes)](https://flr-project.org/)
- [Data-Limited Methods Toolkit (S4 Classes)](https://dlmtool.github.io/DLMtool/userguide/introduction.html)
- [Objected-oriented Simulator of Marine Ecosystem (Java objects)](http://www.osmose-model.org/object-oriented-simulator-marine-ecosystems)


## Resource links

- [H.Wickham's book (Advanced R)](https://adv-r.hadley.nz/oo.html)
- [R6 package](https://r6.r-lib.org/)
- [J.Niño and F.Hosch's book (Introduction to programming and object oriented design using Java)](http://www.cs.uno.edu/~fred/nhText/index.html)
- [Bioconductor](https://www.bioconductor.org/)
