![Proactive Programmers](.github/images/Square-Proactive-Programmers-Logo.svg)

# Container Cloning Source Code Survey

[![build](../../actions/workflows/build.yml/badge.svg)](../../actions/)
![Platforms: Linux, MacOS, Windows](https://img.shields.io/badge/Platform-Linux%20%7C%20MacOS%20%7C%20Windows-blue.svg)
[![Language: Python](https://img.shields.io/badge/Language-Python-blue.svg)](https://www.python.org/)
[![Code Style: Black](https://img.shields.io/badge/Code%20Style-Black-blue.svg)](https://github.com/psf/black)
[![Commits: Conventional](https://img.shields.io/badge/Commits-Conventional-blue.svg)](https://www.conventionalcommits.org/en/v1.0.0/)
[![Discord](https://img.shields.io/discord/872320492936257537?logo=discord)](https://discord.gg/kjah8MFYbR)

## Introduction

- Due date: Check the [Proactive Programmers Discord
server](https://discord.gg/kjah8MFYbR).
- This assignment will be submitted on GitHub following
the expectations in the syllabus on
[Assignment Submission](https://github.com/allegheny-college-cmpsc-101-fall-2023/course-materials#assignment-submission).
- To begin, read this `README` and the Proactive Programmers' project
description for
[Container Cloning](https://proactiveprogrammers.com/data-abstraction/source-code-surveys/container-cloning/)
- Modifications to the gatorgrade.yml file are not permitted without explicit instruction.
- This assignment is an Source Code Survey and will be evaluated as
described in the
[Assessment Strategies for Source Code Surveys](https://proactiveprogrammers.com/proactive-learning/assessment-strategy/#source-code-surveys).
- You can check the
[container-cloning-starter repository](https://github.com/allegheny-college-cmpsc-101-fall-2023/container-cloning-starter)
for any updates to this project's documentation or
source code.

## Learning Objectives

The learning objectives of this assignment are to:

1. Explore complexity of python operations
2. Identify costly operations
3. Problem-solve effectively online
4. Write clearly about the programming concepts in this assignment.

## Seeking Assistance

Please review the course expectations on the syllabus about
[Seeking Assistance](https://github.com/allegheny-college-cmpsc-101-fall-2023/course-materials#seeking-assistance).
Students are reminded to uphold the Honor Code. Cloning the assignment
repository is a commitment to the latter.

For this assignment, you may use class materials, textbooks, notes,
and the internet. However, you must use _your own_ answers, in
_you own_ words. Using ChatGTP or other AI-based language models
to generate reflection responses is not permitted. Asking questions and
learning the necessary concepts to complete the reflection is required.

Post questions to the
[Proactive Programmers Discord server](https://discord.gg/kjah8MFYbR)
or create an issue in your individual copy of the repository
describing your question 24 hours before the deadline.
Be sure to @-tag emgraber in the issue.

## Project Overview

After cloning this repository to your computer, please take the following
steps:

- Make sure that you have already installed and know how to use all of the
  programming tools that are mentioned in the description of the [Proactive
  Skills](https://proactiveprogrammers.com/proactive-skills/technical-skills/introduction-technical-skills/).
- Follow the instructions on the Proactive Programmers web site for this project
  to take all of the needed steps and to complete all of the required
  deliverables.
- Use the `cd` command to change into the directory for this repository.
- Change into the program source code directory by typing `cd source`.
- Run the provided Python script by typing the following:
  - `python perform-container-cloning.py`: perform duplicate removal with container cloning
- The program should initially produce the following output:

```text
Expected output not correct for input lists: [1, 2, 3, 4] and [1, 2, 5, 6]
  actual_list_one: [2, 3, 4]
  actual_list_two: [2, 5, 6]
At least one test case did not pass!
```

- You need to fix the defects in the program so that it produces the correct output:

```text
Expected output correct for input lists: [1, 2, 3, 4] and [1, 2, 5, 6]
All of the test cases passed!
```

- Again, please make sure that you fix the defects inside of these programs!
- Finally, please confirm that the programs are producing the expected output.
- Make sure that you can explain why the programs produce the output that they do.
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
  deleting the `TODO` marker from the code you should instead delete the `TODO`
  marker and the entire prompt and then add your own comments to demonstrate
  that you understand all of the source code in this project.
- Please make sure that you also completely delete the `TODO` markers and their
  labels from every line of the `writing/reflection.md` file. This means that
  you should not simply delete the `TODO` marker but instead delete the entire
  prompt so that your reflection is a document that contains polished technical
  writing that is suitable for publication on your professional web site.
