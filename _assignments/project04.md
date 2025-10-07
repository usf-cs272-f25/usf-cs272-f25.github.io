---
layout: assignment
due: 2025-10-21 23:59:59
github_url: https://classroom.github.com/a/IbcMHpFN
published: true
---

## Requirements

1. Features
    1. For this project, you will crawl `www.usfca.edu` and produce a searchable index
    1. Your web server will produce clickable search results by generating `<a>` tags using the `<title>` of each web page
1. Ethical crawling
    1. You will use a `Crawl-delay` of 100 milliseconds
    1. You will honor the `Disallow` rules in USF's `robots.txt`
    1. Hopefully we won't get rate-limited!
1. Go concurrency
    1. You will adapt the components of your project03 `sqlite` (not `inmem`) crawler to run concurrently
    1. You will use at least two goroutines and communicate between them using Go channels

## Given

1. We will discuss potential approaches in lecture
1. I strongly recommend watching [Rob Pike's talk](https://www.youtube.com/watch?v=f6kdp27TYZs) on Go's concurrency features

## Rubric (draft)

1. 40 pts. TestTfIdf with a concurrent test case
1. 30 pts. [LLM implementation](https://classroom.github.com/a/5blT18pa) including prompt conversation as we did for project03
1. Code review (30 pts)
    1. Explain your design and implementation for concurrency (10 pts)
    1. Plan to demonstrate your solution including clickable search results (10 pts)
    1. Please turn in your best work for the code review, including fixes from your previous pull request. We're not going to file issues on messy code this time. (10 pts)
