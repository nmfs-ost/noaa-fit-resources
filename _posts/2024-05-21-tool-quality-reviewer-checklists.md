---
title: "FIT Tool Quality Standards: Reviewer Checklists"
excerpt: "Checklists for reviewers for the FIT tool quality standards"
date: 2024-5-21
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

## Basics 

For the FIT coordinator to fill out. These must be met for inclusion; no badge assigned for basic check.

- [ ] Metadata complete, as determined by running against the json schema
- [ ] Links in metadata work
- [ ] A license is included (Where appropriate, [an open source license](https://opensource.org/licenses/)).
- [ ] For NOAA developed products where the source code is linked, there is a [NOAA disclaimer](https://github.com/nmfs-fish-tools/resources?tab=readme-ov-file#noaa-license) on the readme.
- [ ] After review: Add FIT badges to metadata based on reviewer's work.

# Checklist for reviewers

Thanks for reviewing this tool! Please use the information submitted by the tool authors to fill out the checklist.

If you have any questions, you can ask them directly on this thread by using the `@` in front of their github username in a comment.

## Documentation

Check off all that are complete. A badge will be assigned based upon how many are checked off:

- 0-2 checked = red
- 3-6 checked = orange
- All 7 checked = green

- [ ] Background text includes a description of the tool and Motivation and/or scope of tool. If appropriate, it also includes link to examples where the tool has informed science-based decision making.
- [ ] Installation instructions that the reviewer can run. If this is a web app, check this off (Reviewer, please try installing and only check off if install is verified)
- [ ] A getting started example that the reviewer can run (e.g. R vignette; reviewer, please try running this example and only check off if it verified that it can run)
- [ ] How to cite the tool 
- [ ] Documentation of how to use the tool in an appropriate form (e.g., a user manual, function reference: R oxygen, doxygen, Sphinx).
- [ ] Example demonstrating advanced features or functions
- [ ] Web-hosted documentation (e.g., pkgdown site, doxygen site, readthedocs)

## Tests

Check off all that are complete. A badge will be assigned based upon how many are checked off

- 0-1 checked = red
- 2-4 checked = orange
- All 5 checked = green

- [ ] [Integrated tests](https://en.wikipedia.org/wiki/Integration_testing) have been done (manually or within a testing framework)
- [ ] Unit testing framework used (e.g., testthat, googletest, unittest) that allows running tests with a single command
- [ ] Test coverage acceptable (>40%)
- [ ] Test coverage excellent (>70%)
- [ ] Tests set up on a continuous integration service to run automatically on code changes or on a schedule (e.g., on GitHub Actions, Travis, Jenkins)
- [ ] For web apps: manual user testing has been done. If not a web app, check this off.