---
layout: post
title: "New Morcus Update"
---

See the updates [live](https://morcus.net), browse the [code](https://github.com/nkprasad12/morcus-net/commit/TODO) or get the [Docker image](https://github.com/nkprasad12/morcus-net/pkgs/container/morcus/TODO).

## Performance

# Page Loads

We migrated to a lighter framework for the site (from `React` to `preact`). 
This lowers the base download (bundle) size of the site by around `40%` (to less than `54 kB`) 
and should speed up page loads on slower connections. In additional, we made some performance optimzations that
should speed up page loads on the largest sites by an average of `30%`.

# Less Memory

We optimized memory usage across the board in a variety of ways, 
and various pages should use `5-20%` less memory than before.

