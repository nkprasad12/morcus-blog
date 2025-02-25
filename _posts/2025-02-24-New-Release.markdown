---
layout: post
title: "Morcus Release (February 2025 #2)"
subtitle: "Better Gaffiot support, more performance improvements, and lots of little UI fixes."
---

See the updates [live](https://morcus.net), 
browse the [code](https://github.com/nkprasad12/morcus-net/commit/a2fd2f4c868e883a6aec5bf79816d1d91ba3ab75), 
or get the [Docker image](https://github.com/nkprasad12/morcus-net/pkgs/container/morcus/361680911?tag=a2fd2f4c868e883a6aec5bf79816d1d91ba3ab75).

# Features

## Gaffiot

### Outlines and Indentation

Gaffiot now has an outline and indentations for detailed senses of a word.

![Gaffiot outlines and indentation](/images/2025-02-R2/gaffiot-outline.png)

### Inflections

Gaffiot now handles inflections, with some caveats. It will produce too many results in cases like `occido` where
there are multiple lemmata that differ only on vowel lengths, but other words should work correctly.

![Gaffiot with inflection handling](/images/2025-02-R2/gaffiot-inflections.png)

# Misc

## Landing page

In a (probably vain) attempt to alleviate user confusion, the landing page has
now been updated to nudge users towards the search settings if they don't see
useful results.

![Updated landing page](/images/2025-02-R2/landing-page.png)

## Other

This release fixes several scroll bugs and several small UI bugs related to poor spacing and layout.

# Performance

## Page Loads

We migrated to a lighter framework for the site (from `React` to `preact`).
This lowers the base download (bundle) size of the site by around `40%` (to less than `54 kB`)
and should speed up page loads on slower connections. In additional, we made some performance optimzations that
should speed up page loads on the largest sites by an average of `30%`.

## Less Memory

We optimized memory usage across the board in a variety of ways,
and various pages should use `5-20%` less memory than before.

# Play Store

The app is no longer available on the Play Store due to compliance issues, and the site `About`
page has been updated to reflect this. It is unclear if or when we will be able to the our Play Store listing.
