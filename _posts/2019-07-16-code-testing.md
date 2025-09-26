---
title: "Code Testing"
excerpt: "Guidance on how to test your code"
date: 2019-07-16
toc: true
categories:
  - Developer Resources
tags:
  - testing
  - developer resources
  - software
  - R
---


## Introduction

We recommend tool developers create *unit tests* and *integrated tests*
to to validate their
software. Once these test cases are created, they may be added to a
continuous integration tool (such as [GitHub Actions](https://docs.github.com/en/actions/quickstart)) so that every time a pull
request is merged in on Github, this suite of tests is run.

For R packages, we recommend trying out the FIT-maintained 
[ghactions4r package](https://nmfs-fish-tools.github.io/ghactions4r/). `{ghactions4r}` 
reduces the GitHub actions learning curve by providing reusable workflows and helper 
functions for common R package development workflows (such as `devtools::check()`).

## Unit tests

Unit tests check that a singular piece of code (i.e. a function or
method) does what it is intended to. The benefit of this type of test is
that it is relatively straightforward to create and it can catch many
problems in software. The downside is unit tests are simplistic and
therefore somewhat tedious to create. Most software platforms or IDEs
have a way to auto-generate a skeleton of the unit test methods a user
might require. In the Eclipse IDE, for example, generating unit tests is
done via the pull down menu. Selecting "create unit tests" will generate
a skeleton test class for each of the classes/functions in your
software. These are usually stored in some kind of created "Tests"
folder.

### An R example of how to create tests

In `R`, the [`testthat` package](https://testthat.r-lib.org/index.html) is the most widely used unit testing framework. It works best on R packages
rather than scripts. Get started with `testthat` using the [Testing basics chapter of R packages](https://r-pkgs.org/testing-basics.html).

## Integrated tests

There may be isolated cases where your package consists only of a number
of independent functions that are not expected to be called in sequence.
In this situation, unit tests alone may be sufficient. However, most
tools require integrated tests in addition to unit tests. Integrated
tests check the functionality of a suite of functions that work
together. For example, if you have a tool that fits a population model,
you might have unit tests for the functions that process the data, fit
the model, and plot the outputs, but an integrated test that runs a
whole example from start to finish. These types of test can help
identify software problems that occur when outputs of one function are
passed as inputs to the next function.

A clear place to source integrated tests is from your user manual,
vignette, or examples directory. If you are providing these examples for
users to work off of, they should always work, and they should be able
to run with only data, functions, and dependencies loaded with the
package. Therefore, we recommend at minimum including a full example as
one of your integrated tests.

If your software relies on a workflow with many different options, each
set of options should have its own integrated test. This could be as
simple as checking that your software returns an error when two
incompatible options are specified, or might mean you need many
different integrated test cases. If you do not find the errors across
multiple cases in an integrated tests, your users will, leading to much
more debugging to find the error than if your code was adequately tested
in the first place.

If you are using `R`, you can include integrated tests in another
`test-*.R` file within the `testing` directory so they are run whenever
the `testthat::test_check()` function is called.

## Code coverage

Once a suite of tests is created, there are
many automated tools you can use to see how much of your code is covered
by automated tests. If you'd like to track this, you can even create a
badge for your repository (and your toolbox landing page) that
highlights how well-covered your code is by test cases. We recommend
tracking this metric so that you can observe how your test coverage
changes over time - it may not be feasible to achieve 100% code
coverage, but at least strive for keeping the same level of code
coverage over time. This will indicate that you are introducing test
cases to cover new functionality at the same rate that you add new
features to your software.

For R packages, a workflow to [create a coverage badge](https://nmfs-ost.github.io/ghactions4r/reference/use_create_cov_badge.html) can be set up entirely on GitHub (to avoid pushing to an unapproved third party cloud). Additionally, a workflow to [calculate a summary and post it on pull requests](https://nmfs-ost.github.io/ghactions4r/reference/use_calc_cov_summaries.html) can also be set up on GitHub.