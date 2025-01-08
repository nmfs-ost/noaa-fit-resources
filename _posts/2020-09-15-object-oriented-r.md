---
title: "Object-oriented programming in R"
excerpt: "Learn about what object-oriented programming systems are and how they are implemented in R"
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

>From J.Niño and F.Hosch (2008):
>
>An **object** is "a software abstraction representing some data component to be manipulated by the system".
>
>**Object-oriented programming** (OOP) refers to "a method of software development in which the system is organized around data objects".


Using OOP, we can use modular pieces of code to build complex models or large systems.

## OOP systems in R

Based on H.Wickham (2019):

R supports OOP. S3, S4, Reference classes (RC), and [R6](https://r6.r-lib.org/) are the main OOP systems in R. An object from these systems contains both classes and methods. Classes include the type and data fields of an object. Methods are implemented in a class and define the behavior of the class.

Learn more about object oriented programming in [H.Wickham's book (Advanced R)](https://adv-r.hadley.nz/oo.html).

## OOP in marine science applications

- [Fishery Library in R](https://flr-project.org/)(S4 Classes)
- [Data-Limited Methods Toolkit](https://dlmtool.github.io/DLMtool/userguide/introduction.html)(S4 Classes)
- [Objected-oriented Simulator of Marine Ecosystem](https://osmose-model.org/)(Java objects)

## Resource links

- [Presentation on Object Oriented Programming in R](https://docs.google.com/presentation/d/1twfJtgg6pq9Obur-lBDvOBO7CA2nQdzutsWusV4OhI0/edit?usp=sharing) (NOAA Internal only)
- [J.Niño and F.Hosch's book (Introduction to programming and object oriented design using Java)](http://www.cs.uno.edu/~fred/nhText/index.html)
- [Bioconductor](https://www.bioconductor.org/)
