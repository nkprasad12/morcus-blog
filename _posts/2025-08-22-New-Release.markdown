---
layout: post
title: "Morcus Release (August 2025)"
description: "A few dictionary fixes, and more works from Hypotactic."
tags: release
---

See the updates [live](https://morcus.net),
browse the [code](https://github.com/nkprasad12/morcus-net/tree/7d5b3ba9cf60e8a86bcb4dd09a5478ebf4b3569a),
or get the [Docker image](https://github.com/nkprasad12/morcus-net/pkgs/container/morcus/494467307).

## Dictionary

### Crashes on long inputs

Due to a bug in the dictionary page, attempting to find autocomplete results for very long inputs (for example, 
if someone accidentally copy-pasted a passage instead of a word) would crash the page. This is now fixed.

### More flexible input parsing

For convenience, the input box will ignore clusters of whitespace and punctuation at the beginning and end of
search queries. For example, before this the query `. unda, ` would not return any results, but it does now.

### Typos

Around 10 user-reported typos were fixed in the underlying sources and should reflect in the dictionary soon.
Thanks for your reports!

## Library

### More Hypotactic Works

Several more macronized works are now available in the library, courtesy of Hypotactic.

- By `Calpurnius Siculus`, `Eclogues`
- By `Germanicus`, `Aratea`
- By `Grattius`, `Cynegetica`
- By `Cicero`, `Aratea`
- By `Persius`, `Satires`
