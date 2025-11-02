---
layout: assignment
due: 2025-11-04 23:59:59 -0700
github_url: https://classroom.github.com/a/FV5tLqLA
published: true
---

## Requirements

For this project you will evolve your lab06 solution by adding:

1. A vector database for `courses.csv` which allows semantic similarity
1. A feature to ask questions of an LLM using command-line input
1. A solution for the "PHILosophy" problem
1. A prompting strategy which answers questions about courses by department, course name, instructor, times, and location
1. Use the `Usage.TotalTokens` field of the LLM response to output the number of tokens used. The exact number will not be graded since it varies with the prompts you design

## Original Code Only

1. In response to feedback about critiquing an LLM-generated solution. We're going to skip 
that for at least this assignment. Therefore, you must hand in only original code. If you
turn in LLM-generated code, you will receive a zero.

## Given

In lecture, we will discuss:

1. How to use Go to read input from the command line
1. The problems of relying on vector similarity to build prompts
1. Opportunities to improve the database implementation 
1. Opportunities to improve the prompts and leverage the capabilities of the LLM

## Rubric

1. 50 pts. - correctness including required test cases
    1. `TestPhil` to prompt the LLM to correctly answer the question, "What courses is Phil Peterson teaching in Fall 2024?"
    1. `TestPHIL` to prompt the LLM to correctly answer the question, "Which philosophy courses are offered this semester?"
    1. `TestBio` to prompt the LLM to correctly answer the question, "Where does Bioinformatics meet?"
    1. `TestGuitar` to prompt the LLM to correctly answer the question, "Can I learn guitar this semester?"
    1. `TestMultiple` to prompt the LLM to correctly answer the question, "I would like to take a Rhetoric course from Phil Choong. What can I take?"
1. 50 pts. - code review
    1. You must build an abstraction around the chat completion API so you can reuse it
    1. You must build the prompt in a general way, without hard-coding the desired LLM output in the prompt
    1. You must use object-oriented structs and methods to build the components required for your database, chatbot, etc. No long main programs. 
    1. You must use the techniques discussed in lecture. If you think of a shortcut, you may implement that in addition to the approach we discussed.