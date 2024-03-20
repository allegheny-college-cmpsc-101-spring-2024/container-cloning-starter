
# Container Cloning Source Code Survey

[![build](../../actions/workflows/build.yml/badge.svg)](../../actions/)
![Platforms: Linux, MacOS, Windows](https://img.shields.io/badge/Platform-Linux%20%7C%20MacOS%20%7C%20Windows-blue.svg)
[![Language: Python](https://img.shields.io/badge/Language-Python-blue.svg)](https://www.python.org/)
[![Code Style: Black](https://img.shields.io/badge/Code%20Style-Black-blue.svg)](https://github.com/psf/black)
[![Commits: Conventional](https://img.shields.io/badge/Commits-Conventional-blue.svg)](https://www.conventionalcommits.org/en/v1.0.0/)
[![Discord](https://img.shields.io/discord/872320492936257537?logo=discord)](https://discord.gg/kjah8MFYbR)

## Introduction

- Due date: Check Discord or the
  [Course Materials Schedule](https://github.com/allegheny-college-cmpsc-101-spring-2024/course-materials/blob/main/Schedule.md)
- This assignment is graded on a checkmark basis (100 for gatorgrade reports of 100, 0 otherwise) as
  described in the syllabus section for
  [Assignment Evaluation](https://github.com/allegheny-college-cmpsc-101-spring-2024/course-materials?tab=readme-ov-file#assignment-evaluation)
- Submit this assignment on GitHub following the expectations in the syllabus on
  [Assignment Submission](https://github.com/allegheny-college-cmpsc-101-spring-2024/course-materials#assignment-submission).
- To begin, read this `README` based on the Proactive Programmers' project
  [instructions](https://proactiveprogrammers.com/data-abstraction/source-code-surveys/container-cloning/)
- This project has been adapted from Proactive Programmers' material, thus discrepancies are possible.
- Post to the #data-structures Discord channel for questions and clarifications.
- For reference, check the
  [starter repo](https://github.com/allegheny-college-cmpsc-101-spring-2024/container-cloning-starter)
- Modifications to the gatorgrade.yml file are not permitted without explicit instruction.

## Learning Objectives

The learning objectives of this assignment are to:

1. Identify costly python operations
2. Problem-solve effectively online
3. Fix errors due to aliasing
4. Write clearly about the programming concepts in this assignment.

## Seeking Assistance

Please review the course expectations on the syllabus about
[Seeking Assistance](https://github.com/allegheny-college-cmpsc-101-spring-2024/course-materials#seeking-assistance).
Students are reminded to uphold the Honor Code. Cloning the assignment repository is a
commitment to the latter.

For this assignment, you may use class materials, textbooks, notes, and the
internet. Ensure that your writing is original and based on your own understanding
of the concepts.

To claim that work is your own, it is essential to craft the logic and the
writing together without copying or using the logical structure of another
source. The honor code holds everyone to this standard.

If outside of lab you have questions, the #data-structures Discord channel,
TL office hours, instructor office hours, and GitHub Issues can be utilized.

## Project Details (Overview Below)

This assignment invites you to study, repair, and test a Python programs called
`perform-container-cloning`. Specifically, it affords you to opportunity to
continue to practice the task of debugging and testing a Python function that
has defects inside of it due to aliasing. After learning more about how containers
are cloned or not cloned in memory in a Python program
and why cloning is needed when a program iterates through a
collection while changing it at the same time, you will find and fix the fault in
the provided source code. Once you have fixed the defect, you will document a
provided test case that (i) creates an input for a function, (ii) passes that
input to the function under test, (iii) captures the output of the function
under test, and (iv) asserts that the captured function output equals the
expected output if the function was implemented correctly. Instead of using a
test automation framework to run the provided test you will run a function to
complete the aforementioned steps.

## Code Survey

If you change into the `source/` directory of your GitHub repository, you will
see one Python file called `perform-container-cloning.py`. The
`perform-container-cloning` module contains a defective function with the
signature `def remove_duplicates(list_one: List[Any], list_two: List[Any]) ->
Tuple[List[Any], List[Any]]`. Your task is to identify and fix the defects
inside of this function! To aid your debugging efforts, you should use and
extend the `def test_remove_duplicates() -> bool` function that should subject
the `remove_duplicates` function to several tests. Although it does not use
Pytest, it is possible to implement a test called `test_remove_duplicates` in
the following fashion:

```python linenums="1"
list_one = [1, 2, 3, 4]
list_two = [1, 2, 5, 6]
expected_list_one = [3, 4]
expected_list_two = [5, 6]
test_case_passed = True
(actual_list_one, actual_list_two) = remove_duplicates(list_one, list_two)
if expected_list_one == actual_list_one and expected_list_two == actual_list_two:
    print("Expected output correct for input lists: [1, 2, 3, 4] and [1, 2, 5, 6]")
else:
    print("Expected output not correct for input lists: [1, 2, 3, 4] and [1, 2, 5, 6]")
    print(f"   actual_list_one: {actual_list_one}")
    print(f"   actual_list_two: {actual_list_two}")
    test_case_passed = False
return test_case_passed
```

Lines `1` and `2` of this function create two lists, called `list_one` and
`list_two`, that have in common the values `1` and `2`. Lines `3` and `4` of
this function indicate that, if the `remove_duplicates` function worked
correctly, then its output should be a tuple container the lists `[3, 4]` and
`[5, 6]`. After making the assumption that the test case will pass on line `5`,
the function calls `remove_duplicates` and checks to see if the expected output
equals the actual output returned by the function. If the expected output is
correct, then line `8` displays a message indicating that is the case.
Otherwise, lines `10` through `13` signal that the test did not pass and display
diagnostic output to highlight this fact for the tester. Ultimately, if this
test case passes correctly it will help to establish a confidence in the
correctness of `remove_duplicates`. When the test case for the
`remove_duplicates` function passes, then it should produce the following
output:

``` text
Expected output correct for input lists: [1, 2, 3, 4] and [1, 2, 5, 6]
The test case passed!
```

## Running Checks

Since this project does not use [Poetry](https://python-poetry.org/) to manage
project dependencies and virtual environments, it does not support the use of
commands like `poetry run task test`. However, you can leverage the relevant
instructions in the [technical
skills](/proactive-skills/introduction-proactive-skills/) to run the command
`gatorgrade --config config/gatorgrade.yml` to check your work. If your work
meets the baseline requirements and adheres to the best practices that proactive
programmers adopt you will see that all the checks pass when you run
`gatorgrade`. You can study the `config/gatorgrade.yml` file in your repository
to learn how :material-github:
[GatorGrade](https://github.com/GatorEducator/gatorgrade) runs :material-github:
[GatorGrader](https://github.com/GatorEducator/gatorgrader) to automatically
check your program and technical writing.

## Project Reflection

Once you have finished all of the previous technical tasks, you can use a text
editor to answer all of the questions in the `writing/reflection.md` file.
Since this is a source code survey, you should provide output from running each
of the provided Python programs on your own laptop and then explain how the
program's source code produced that output. A specific goal for this project is
to ensure that you can explain the syntax and meaning of function signatures
like `def remove_duplicates(list_one: List[Any], list_two: List[Any]) ->
Tuple[List[Any], List[Any]]`. You should also be able to discuss what defect(s)
you found in the `remove_duplicates` function and how you fixed them.

## Project Assessment

Since this project is source code survey, it is aligned with the **remembering**
and **understanding** levels of [Bloom's
taxonomy](/proactive-learning/blooms-taxonomy/). You can learn more about how a
proactive programming expert will assess your work by examining the [assessment
strategy](/proactive-learning/assessment-strategy/). From the start to the end
of this project you may make an unlimited number of reattempts at submitting
source code and technical writing that meet the project's specification.

## Project Overview

After cloning this repository to your computer, please take the following
steps:

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
- Run the automated grading checks by typing
  `gatorgrade --config config/gatorgrade.yml`.  
- You may also review the output from running GatorGrader in GitHub Actions.
- Don't forget to provide all of the required responses to the technical writing
  prompts in the `writing/reflection.md` file.
- Please make sure that you completely delete the `TODO` markers and their
  labels from all of the provided source code.
- Please make sure that you also completely delete the `TODO` markers and their
  labels from every line of the `writing/reflection.md` file.
