---
title: "FIT Tool Quality Standards: Reviewer Checklists"
excerpt: "Checklists for reviewers for the FIT tool quality standards"
date: 2026-5-28
toc: true
categories:
  - NOAA FIT
tags:
  - NOAA resources
  - GitHub
  - developer resources
  - software
  - code review
---

# Checklists for FIT tool quality standards

The below are checklists for reviewers assessing the FIT tool quality standards

## Basics \- for the FIT coordinator to fill out

### Mandatory items

- [ ] Confirm that tool is in scope per the [FIT scope statement](https://noaa-fisheries-integrated-toolbox.github.io/resources/about/)  
- [ ] Metadata is complete, as determined by running against the [json schema](https://github.com/nmfs-ost/FIT_web_templating/blob/main/schema_model_list.json)
- [ ] Links in metadata work
- [ ] A license is included (where appropriate, [an open source license](https://opensource.org/licenses/)).
- [ ] Software version is included
- [ ] Source code is linked (note: check this off if source code is not provided and there is a valid reason for source code to be kept private)  
- [ ] For NOAA-developed products where the source code is linked, there is a [NOAA disclaimer](https://github.com/nmfs-ost/FIT-resource-files?tab=readme-ov-file#noaa-license) on the readme of the source code.  
- [ ] For Web apps and other apps that use web technologies: All errors flagged by [ANDI](https://www.ssa.gov/accessibility/andi/help/install.html) are resolved   
- [ ] For other GUIs that do not use web technologies: *need more info on how to test these for accessibility. Some tools available for Windows: Accessibility Insights for Windows, AccEvent, NVDA; and for MacOS: Accessibility Inspector in Xcode*

## Checklist for reviewers

Thanks for reviewing this tool! Please use the information submitted by the tool authors to complete the checklist.

If you have any questions, you can ask the tool author directly on this thread by using the \`@\` in front of their github username in a comment.

Check off all items that are complete.

### Reviewer Basics

- [ ] Reviewer has no known [Conflicts of Interest](https://github.com/nmfs-ost/FIT-test-quality-checks/blob/main/reviewer-guide.md#reviewer-conflict-of-interest). If the reviewer has a potential conflict of interest, it should be brought up with the FIT coordinator.

### Mandatory items

#### Documentation

- [ ] Background text includes a description of the tool and its motivation and/or scope. If appropriate, it also includes links to examples where the tool has informed science-based decision making.
- [ ] Installation instructions are provided that the reviewer can run. Reviewer, please attempt installation and only check this off if install is verified. If this is a web app or other software type that does not require installation, check this off.
- [ ] A getting started example (e.g., R vignette) is provided that the reviewer can run. Reviewer, attempt to run this example and only check this off if verified to run.
- [ ] Instructions on how to cite the tool are included.
- [ ] Documentation on how to use the tool is provided in an appropriate form (e.g., a user manual, or function reference: roxygen, doxygen, Sphinx).

#### Tests

- [ ] [Integrated tests](https://en.wikipedia.org/wiki/Integration_testing) have been conducted (manually or within a testing framework).
- [ ] A unit testing framework (e.g., testthat, googletest, unittest) is used that allows running tests with a single command.
- [ ] [Code coverage](https://www.atlassian.com/continuous-delivery/software-testing/code-coverage) is acceptable (\>40% line coverage).
- [ ] Sample data provided to validate functionality.
- [ ] [Usability tests](https://digital.gov/topics/usability) have been conducted and results are sufficiently described (can be qualitative).

#### Good practices items (not mandatory)

- [ ] An example demonstrating advanced features or functions is included.
- [ ] Web-hosted documentation is available (e.g., pkgdown site, doxygen site).
- [ ] [Code coverage](https://www.atlassian.com/continuous-delivery/software-testing/code-coverage) is excellent (\>70% line coverage).
- [ ] Tests set up on a continuous integration service to run automatically on code changes or on a schedule (e.g., on GitHub Actions, Travis, Jenkins).
