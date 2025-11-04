---
layout: assignment
due: 2025-11-11 23:59:59
github_url: https://classroom.github.com/a/r9wXeBtH
published: true
---

## Requirements

For this lab, you will evolve your project05 solution as follows:

1. For Named Entity Recognition, you will adopt "structured output" using a JSON schema
1. You will remove the hints in the prompt you send to the ChatCompletion API
1. Rather, you will passing the user's question directly to the LLM and provide hints in the style of "tool/function calling"
1. You will add `tools` to the ChatCompletion request
1. Your tool implementation will query ChromaDB and provide structured query results to the LLM
1. The LLM will use the results of the tool call to answer the user's question
1. Include the token usage in your output, as with project05

## Given

1. We will discuss the fundamentals of JSON schema and tool calling in lecture

## Rubric

Same test cases as project05, except the guitar one is optional

1. 100 pts. - correctness including required test cases
    1. `Lab07/TestPhil` to prompt the LLM to correctly answer the question, "What courses is Phil Peterson teaching this semester?"
    1. `Lab07/TestPHIL` to prompt the LLM to correctly answer the question, "Which philosophy courses are offered this semester?"
    1. `Lab07/TestBio` to prompt the LLM to correctly answer the question, "Where does Bioinformatics meet?"
    1. `Lab07/TestGuitar` to prompt the LLM to correctly answer the question, "Can I learn guitar this semester?"
    1. `Lab07/TestMultiple` to prompt the LLM to correctly answer the question, "I would like to take a Rhetoric course from Phil Choong. What can I take?"
