---
layout: post
title: "Morcus Release (November 2026 #2)"
description: "Wildcards and work filters in corpus search, smarter dictionary ranking, and many fixes."
tags: release
---

See the updates [live](https://morcus.net), or
browse the [code](https://github.com/nkprasad12/morcus-net/tree/d1d763a76316c0c94bce230667446bcfea4e1df9).

## Corpus Search

### Wildcards

You can now use `*` in a search word to match the start or end of words:

- `con*` finds words starting with _con_
- `*que` finds words ending in _que_
- `in*bilis` finds words starting with _in_ and ending in _bilis_

Wildcards also work alongside `and`, `or`, `@lemma:`, and grammatical filters.

### Searching by Work

You can now limit a search to a single work with `#Author/Work`. For example, `#Caesar/DeBelloGallico omnis` only searches the _De Bello Gallico_.

You can also search several authors or works at once by putting more than one filter at the start of a query, such as `#Caesar #Cicero @lemma:res`. Autocomplete suggests the available works once you've typed an author.

### Reference Page

The new [reference page](https://morcus.net/corpus/reference) explains how to write queries and lists the codes for every author and work.

### Fixes

- Search results are more accurate for words with ligatures, Roman numerals, or editorial brackets.
- Fixed corrupted characters in Gaius, Justin, and the _Declamationes Maiores_.
- Fixed a bug where author-filtered searches could show an empty second page of results.
- Fixed errors in proximity searches (such as `~10`) limited to an author or work.

## Dictionary

### Better Result Ordering

Dictionary results now put the most common reading first. For example, `illum` shows _ille_ before _illic_, and `moris` shows _mora_ and _mos_ before _moveo_. Rarer readings (contracted, archaic, poetic, or late forms) now appear further down.

The inflections listed within an entry are ordered the same way.

### Macronized Searches

When you search with macrons, results no longer include forms with different vowel lengths. For example, searching `quīs` no longer shows `quĭs`.

### More Recognized Forms

Morcus now recognizes more inflected forms and spellings, such as _admorunt_, _Aristides_, _inberbis_, and _attramentum_.

### Fixes

- Many user-reported typos were fixed in Lewis and Short and Smith and Hall - thank you!
- Some entries no longer show the same inflection twice.
- Updated the license attribution for the Gesner dictionary.

## Texts

### Shorter Links

Author links are now shorter and easier to recognize (for example, `cornelius_nepos` is now `nepos`, and `pliny_the_elder` is now `pliny_elder`). Old links still work.

### Fixes

- Several collections from _The Latin Library_ (including works by Erasmus, Dante, and Luther) are now split into individual works.
- Fixed user-reported typos and numbering errors in Cicero's _In C. Verrem_ - thank you!
- Fixed a small visual gap above the top bar in the reader on Firefox.
