---
layout: assignment
due: 2025-09-09 23:59:59
github_url: https://classroom.github.com/a/SCehnva4
published: true
---

## Requirements
1. You will build a web crawler which incorporates the elements of the prior lab assignments, including their test cases: 
    1. Download from a URL
    1. Extract non-markup text using Go's `html.Parser`
    1. Extract `href` attributes from `<a>` tags
1. Lab03 adds the following new features, which must include new test cases
    1. An in-memory inverted index based on Go's `map`
    1. [Snowball stemmer](https://github.com/kljensen/snowball)
1. Your solution will crawl the text of [Romeo and Juliet](/test-data/rnj/), which I got from [Project Gutenberg](https://www.gutenberg.org/) and divided
into an HTML document per scene.
1. You will write a `TestSearch` function which tests these three cases for the inverted index, returning the term frequency for each one (i.e. the map of string to frequency)
    1. Search `https://usf-cs272-f25.github.io/test-data/rnj/sceneI_30.0.html` for `Verona` should find one hit:
        ```
        "https://usf-cs272-f25.github.io/test-data/rnj/sceneI_30.0.html": 1
        ```
    1. Search `https://usf-cs272-f25.github.io/test-data/rnj/sceneI_30.1.html` for `Benvolio` should return 26 hits:
        ```
        "https://usf-cs272-f25.github.io/test-data/rnj/sceneI_30.1.html": 26
        ```
    1. Search `https://usf-cs272-f25.github.io/test-data/rnj/` for `Romeo` should return these hits:
        ```
        "https://usf-cs272-f25.github.io/test-data/rnj/sceneI_30.0.html":  2,
        "https://usf-cs272-f25.github.io/test-data/rnj/sceneI_30.1.html":  22,
        "https://usf-cs272-f25.github.io/test-data/rnj/sceneI_30.3.html":  2,
        "https://usf-cs272-f25.github.io/test-data/rnj/sceneI_30.4.html":  17,
        "https://usf-cs272-f25.github.io/test-data/rnj/sceneI_30.5.html":  15,
        "https://usf-cs272-f25.github.io/test-data/rnj/sceneII_30.2.html": 42,
        "https://usf-cs272-f25.github.io/test-data/rnj/":                  200,
        "https://usf-cs272-f25.github.io/test-data/rnj/sceneI_30.2.html":  15,
        "https://usf-cs272-f25.github.io/test-data/rnj/sceneII_30.0.html": 3,
        "https://usf-cs272-f25.github.io/test-data/rnj/sceneII_30.1.html": 10,
        "https://usf-cs272-f25.github.io/test-data/rnj/sceneII_30.3.html": 13,
        ```
1. You can use `reflect.DeepEqual()` to test the equivalence of your `got` map and your `want` map

## Given

In lecture meetings we will discuss and provide sample code for:
1. Hash tables, the underlying technology for go `map`
1. Inverted indexes, which can be used to facilitate searching a corpus of documents
1. Word stemming

## Rubric
Your lab will receive the score indicated by the autograder using this rubric:
1. 10 pts: `TestExtract()`
1. 10 pts: `TestCleanHref()`
1. 10 pts: `TestDownload()` (do you download the correct content)
1. 10 pts: `TestCrawl()` (can you crawl a given seed url and download it along with all of the links embedded within)
1. 60 pts: `TestSearch()` (can you find a search term and return the number of hits)