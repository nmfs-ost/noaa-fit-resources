---
title: "Installing Windows Subsystem for Linux (WSL) on NOAA Computers"
excerpt: "A guide to setting up WSL2 and Docker on NOAA-issued computers with IT assistance"
date: 2026-06-22
toc: true
categories:
  - Developer Resources
tags:
  - developer resources
  - NOAA resources
  - software
---

[Windows Subsystem for Linux (WSL)](https://learn.microsoft.com/en-us/windows/wsl/about) allows developers to run a Linux environment on Windows computers without having to use a dual-boot setup. There are several blog posts on the Internet that outline how to install WSL2 (e.g., [instructions from Microsoft](https://learn.microsoft.com/en-us/windows/wsl/install)) but, if you are working on a NOAA-issued computer, the installation requires some assistance from the IT department.

## Why WSL

First, why would you even want to experiment with WSL on a Windows computer? There are several Linux-specific tools, bash scripts, and Docker containers that just work better or only work on Linux. And, running a dual-boot system, i.e., having both Linux and Windows on the same machine, can be a headache. Specifically, for the [Fisheries Integrated Modeling System (FIMS)](https://github.com/NOAA-FIMS/FIMS), we use WSL to facilitate debugging C++ code using [gdb](https://sourceware.org/gdb/). In theory, you can use gdb on Windows but it does not integrate well with compiled code because the `-d` flag is a Unix-only feature in R. I am sure there are other examples out there as well of reasons that WSL can help fisheries scientists.

Second, we found a huge cost saving by installing WSL because we were able to limit our use of codespaces (which is a Linux environment) once we were able to mimic the process on our own computer. Not only is WSL helpful for using gdb but it is also helpful for debugging failed GitHub workflows that are often running on Linux environments. As we are pushed to do more and more in the cloud, learning how to navigate Linux systems using WSL will pay off more and more.

Third, many projects provide a `devcontainer.json` file in the `.devcontainer` directory that facilitates launching a fully configured environment inside of VS Code without needing to manually install project dependencies, compilers, or other system tools on your local machine. In fact, these configuration files are becoming more prevalent as the use of [GitHub codespaces](https://github.com/features/codespaces) increases and as more people use [{renv}](https://rstudio.github.io/renv/articles/renv.html) for package management.

We decided to write this blog post because installing WSL2 on a NOAA Windows computer takes a bit more work than the instructions that are readily available and we wanted to limit the barrier to entry. Especially because we noticed that not many people ask IT to install WSL2, even though both WSL2 and Docker Engine are on the [approved software list](https://docs.google.com/spreadsheets/d/1oPaTegdBGEmkjrmkbOVjGAJpPFg755p3Wws50ddLwCI/edit?usp=sharing), so your local IT might not know all the tips and tricks for a seamless process.

## Install WSL2 and Docker Engine

**Steps:**

1. Contact IT to install WSL2 and Docker Engine on your Windows machine
2. For detailed technical information, refer to:
   - [Official WSL documentation](https://learn.microsoft.com/en-us/windows/wsl/install)
   - [Docker installation documentation](https://docs.docker.com/engine/install/)
3. **Important:** Have IT "Turn Windows features on or off" for WSL on Windows in addition to installing the software. Here are [similar instructions](https://www.tenforums.com/tutorials/46769-enable-disable-windows-subsystem-linux-wsl-windows-10-a.html) to guide them through this step.

## Install VS Code and Extensions

Once WSL is installed, you'll need to set up Visual Studio Code to work with your new Linux environment.

1. Open Visual Studio Code
2. Open the Extensions view with `Ctrl + Shift + X`
3. Install the following extensions:
   - **WSL extension** (ID: `ms-vscode-remote.remote-wsl`) — allows VS Code to connect to the WSL environment
   - **Dev Containers extension** (ID: `ms-vscode-remote.remote-containers`) — builds and manages development containers from the `.devcontainers/devcontainer.json` file

## Install a Distribution

The final step is to set up a distribution of Linux as your WSL distribution. We chose to highlight the installation of Ubuntu, but you can install any distribution that you like. To see all of the distributions that are available run `wsl --list --online` once WSL is installed and in your path. I also like Debian and have it installed on my personal machine.

1. Open a Windows Command Prompt and check if `Ubuntu` is already listed as a WSL distribution:

```bash
wsl --list --verbose
```

2. If `Ubuntu` is not listed under the `NAME` column, run the following command to install it:

```bash
wsl --install -d Ubuntu
```

## Using WSL

This blog post is about installing WSL for NOAA computers that use Windows and not about how to use it. But, there are many other posts about using WSL on the internet, e.g., [Microsoft's Get started using VS Code with WSL](https://learn.microsoft.com/en-us/windows/wsl/tutorials/wsl-vscode). Additionally, there are instructions in the [FIMS repository](https://github.com/NOAA-FIMS/FIMS/tree/main/.devcontainer#-wsl2) on how to use WSL with FIMS.

Best of luck. And, feel free to reach out to the [FIMS developers](https://noaa-fims.github.io/contact/) if you have questions.
