# Memory Allocation

[![build](../../actions/workflows/build.yml/badge.svg)](../../actions/)
[![Language: C](https://img.shields.io/badge/Language-C-blue.svg)](https://gcc.gnu.org/)
[![Language: Go](https://img.shields.io/badge/Language-Go-blue.svg)](https://go.dev/)
[![Commits: Conventional](https://img.shields.io/badge/Commits-Conventional-blue.svg)](https://www.conventionalcommits.org/en/v1.0.0/)
[![Discord](https://img.shields.io/discord/1013818801281839184?logo=discord)](https://discord.gg/9VfCdqffu6)

## Introduction

This project introduces the steps that you must take to implement, build, and
run programs in the C and Go programming languages. You will learn how to use
Makefiles to automatically build programs and copy their binaries to a suitable
directory. The programs that you implement will demonstrate the execution of
constructs that help you to detect details about the computer that runs the
programs and the size of the data that the programs allocate to memory.

## Seeking Assistance

Even though the course instructor will have covered all of the concepts central
to this project before you start to work on it, please note that not every
detail needed to successfully complete the assignment will have been covered
during prior classroom sessions. This is by design as an important skill that
you must practice as you explore the depth and breadth in the field of operating
systems. If you have questions about this project, please schedule a meeting
with the course instructor during office hours.

## Project Overview

After cloning this repository to your computer, please take the following steps:

### Program Setup

Along with studying the references provided as comments in the C and Go source
code files, please make sure that you refer to the chapter and to the slides on
the course web site for more information about this project's context.

- Make sure that you have installed the following programs on your laptop:
  - Gcc toolchain
  - Go programming language
  - C programming language
- Use the `cd` command to change into the directory for this repository.
- Review the `Makefile` in the `project/clang/` directory to see the targets for
  the version of this project implemented in the C programming language.
- Review the `Makefile` in the `project/golang/` directory to see the targets
  for the version of this project implemented in the Go programming language .
- Both of these `Makefile`s will work on the Linux and MacOS operating systems
  and, additionally, on GitHub Actions, and inside of the OS-Sketch Docker
  container. You may need to revise portions of these `Makefile`s so that they
  work correctly on the Windows operating system.
- To build the C and Go programs you need to run the following commands from the
  respective `clang/` and `golang/` directories:
  - `make run-sizeof` to build the `bin/run-sizeof` binary
- Note that the `make` commands are the same regardless of whether you are in
  the `clang/` or the `golang/` directories! With that said, it is important to
  note that the `Makefile` in `golang/` does something different than the one in
  `clang`. Make sure that you understand how these `Makefile`s work!

### Program Use

The `run-sizeof` program that you implement should output the following
information when run in your terminal window. All of this information should be
detected through functions calls that access operating system information and
not output in a hard-coded fashion. This means that, for instance, the
`run-sizeof` program will output different information when it runs on your
computer than when it is run in GitHub Actions or on the instructor's computer!
Please note that you may decide that your implementation of `run-sizeof` may
output more information that what is required by the following list; with that
said, you must at least provide the following information and be able to label
and interpret all of the output that the program creates.

- The technical name of the operating system on which the program was run
- The technical name of the computer architecture on which the program was run
- The size of the following data types for each programming language:
  - `char`: single-character value
  - `int`: single- and/or double-precision integer value
  - `float`: single-precision floating-point value
  - `double`: double-precision floating-point value

When a specific programming language does not, in your judgement, provide a
direct counterpart to the four aforementioned data types, you should qualify
your program's output and/or provide additional output for the most similar data
types. Ultimately, you should be able to use the output of the two `run-sizeof`
programs to reach a principled conclusion about the size of data in each
language. It is important that your C and Go programs both run on Windows,
Linux, and MacOS and automatically report data type sizes that are not
hard-coded for a specific architecture platform or operating system. Your
programs should also feature an automated approach, that is as general-purpose
and platform-independent as is possible, for detecting the operating system and
computer architecture on which the program is run and then display that in the
terminal window and/or in GitHub Actions. Finally, whenever it is appropriate to
do so, your C and Go programs should include references to the online technical
resources that you consulted and a statement about how they influenced your
approach to implementing the programs and collecting the required data.

### Project Reflection

As you work on this project, you should regularly take time to reflect on the
steps that you are taking and why you are taking them. Each time you run a
program you should think about the inputs, outputs, and behavior of that
program, jotting down notes to help you remember these insights. When you are
writing C and Go programs, please reserve time to reflect on the features of the
language that you are learning and how the languages are similar to and
different from each other. Make sure that you also reflect on your own strengths
and weaknesses, how you can improve in advance of the next project, and the
online technical resources that you consulted when completing the project. You
should also ensure that you provide sufficient justification for the source code
of the C and Go programs and sufficient commentary on their output.

### Automated Assessment

Please review the following notes about the way in which your project will be
automatically assess in GitHub Actions:

- If you have already installed the
  [GatorGrade](https://github.com/GatorEducator/gatorgrade) program that runs
  the automated grading checks provided by
  [GatorGrader](https://github.com/GatorEducator/gatorgrader) you can, from the
  repository's base directory, run the automated grading checks by typing
  `gatorgrade --config config/gatorgrade.yml`.
- You may also review the output from running GatorGrader in GitHub Actions.
- Don't forget to provide all of the required responses to the technical writing
  prompts in the `writing/reflection.md` file.
- Please make sure that you completely delete the `TODO` markers and their
  labels from all of the provided source code. This means that instead of only
  deleting the `TODO` marker from the code you should delete the `TODO`
  marker and the entire prompt and then add your own comments to demonstrate
  that you understand all of the source code in this project.
- Please make sure that you also completely delete the `TODO` markers and their
  labels from every line of the `writing/reflection.md` file. This means that
  you should not simply delete the `TODO` marker but instead delete the entire
  prompt so that your reflection is a document that contains polished technical
  writing that is suitable for publication on your professional web site.
