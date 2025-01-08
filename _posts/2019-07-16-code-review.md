---
title: "Code Review"
excerpt: "Introduction to code review and how to do it"
date: 2019-07-16
toc: true
categories:
  - Developer Resources
tags:
  - code review
  - software
  - developer resources
---



## What is code review and why should I do it?

The point of code review is to improve code quality. By drawing on the
expertise of reviewers in addition to code authors, code quality can be
enhanced and both authors and reviewers will improve their coding
skills. Automated testing is a subset of procedures undertaken in a code
review, but the most thorough review and feedback comes from other
people.

If code review is done correctly, it saves author time. Other developers
who review your code must understand why the change has been made and
how it works, so if a bug is detected they are able to debug and/or fix
it. Reviewing code before it is merged upstream increases the chances
that bugs are caught before propogating to the main branch. Reviews
should be done often on small chunks of code, therefore each review
should not take a substantial amount of time.

Code review checklist
---------------------

Mozilla science has an excellent
[checklist](https://mozillascience.github.io/codeReview/review.html) for
scientific code review.  Here are some additional suggestions.

### Intrinsic issues

-   Argument handling - are there too many arguments, or conversely are
    global variables assumed? Could redundant argument passing be
    simplified? Should we be dragging along objects with inputs and
    outputs. Input arguments and initializing to null?
-   Function location, structure, and size
-   Efficiency - reducing duplication and using mapping if possible
-   Consistent and meaningful name standards
-   Documentation
-   Error handling - are inputs checked?
-   Are unit tests performed?

### Extrinsic issues

-   Is there functionality in the new code that is duplicated elsewhere
    in the package?
-   Does the new code follow the project standard?
-   Are the user guides/tutorials updated?