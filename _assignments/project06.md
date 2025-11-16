---
layout: assignment
due: 2025-11-18 23:59:59
github_url: https://classroom.github.com/a/JW4iaFcy
published: true
---

## Requirements

In this project, you will
1. Extend your lab07 solution to include "agentic" behavior
1. As in lab07, write the code yourself without using an LLM coding assistant
1. You may reuse or modify the `sqlite-vec` code you wrote for project05, but continue to use `sqlite-vec`
1. Enhance your tool-calling lab to run in a loop, accumulating a slice of
`openai.ChatCompletionMessage` which provides a running session (or "context") for your questions. Example output:

    ```text
    Q. Who is teaching CS 272?

    A. Philip Peterson is teaching CS 272

    Q. What's his email address?

    A. Philip Peterson's email address is phpeterson@usfca.edu
    ```
1. Handle multiple argument and multiple tools, e.g.:

    ```text
    Q. What are Phil Peterson and Greg Benson teaching?

    Q. Which courses is Phil Peterson teaching in HR 148?

    Q. Which department's courses are most frequently scheduled in Kalmanovitz (KA) Hall?
    ```

## Given

1. We will discuss design strategies for utilizing the LLM's context window
1. You will need to reuse your code from project05 and lab07

## Rubric

1. 48 pts - Passes test cases, including reasonable import time
1. 52 pts - Code review
    1. Peer review
    1. Review my code
    1. Competition for least token use
