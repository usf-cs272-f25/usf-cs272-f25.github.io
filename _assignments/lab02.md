---
layout: assignment
due: 2025-08-26 23:59:59
github_url: https://classroom.github.com/a/LXNls3-9
published: true
---

## Background

For this assignment you will use the first chapter of _The Call of the Wild_ by Jack London as a data set to work with text processing in Go. 

## Given

1. The text of the book is provided in the repo you will clone from GitHub. 
1. We will discuss using Go to program files I/O, strings, and data structures such as slices

## Requirements

1. You will read the file, dividing the text up into a slice of words
1. Each word must be normalized: lower-case, no white space (spaces, tabs, or newlines), and no punctuation
1. You will accumulate a slice of words, including its frequency (i.e. how many times that word appears in the text)
1. You will output (to stdout) the most frequently occurring word and its count

## Rubric

1. 100 pts using autograder tests which will be provided shortly