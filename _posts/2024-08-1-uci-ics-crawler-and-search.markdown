---
layout: post
title: "Web Crawler and Search Engine (Project)"
categories: project
---

## About:

This is a web crawler, indexer, and search engine for the uci.ics domain. 

The web crawler scans through sites on the uci.ics domain, scanning each page for links to other pages, and outputs a list of unique urls. It also filters out crawler traps, such as dynamicly generated websites and infinite loops. A total of 35,589 unique urls were found.

The indexer uses the list of urls as input. It scans through the contents of each of them, breaking each website into a list of individual tokens. It does this in order to create an inverted index, where each token is mapped to a list of websites containing that token. The indexer also calculates statistics for each token, such as document and term frequency. After filtering out common "stop" tokens, the total number of tokens found is 72,835.

The search engine uses the inverted index as input. It then lets users search for multi-word queries. To find the top results, uses the [vector space model](https://en.wikipedia.org/wiki/Vector_space_model), where each website and the query are represented as vectors in an n-dimensional space, where n is the number of tokens, and [tf-idf](https://en.wikipedia.org/wiki/Tf%E2%80%93idf) scores are used as weights for each dimension. It then finds the websites with the smallest angle difference between the website vector and query vector. Websites which contain the searched token(s) in a heading or title also get an extra boost in the ranking process. This is presented to the user in a simple GUI, with the resulting urls are ordered by relevance and listed in pages that can be flipped through.

Made for CS 121 with a team of 2 other students.

## Languages, Frameworks, Tools

- Python
- Github
- BeautifulSoup (HTML Parser)
- Tkinter (GUI)
- Numpy


