---
layout: post
title: "Morcus Release (Fall / Winter 2025)"
subtitle: "Corpus search tool, many new works, and more!"
tags: release
---

See the updates [live](https://morcus.net),
browse the [code](https://github.com/nkprasad12/morcus-net/tree/f56db8e6580a18a341d5fb4d485d5676fc26e879),
or get the [Docker image](https://github.com/nkprasad12/morcus-net/pkgs/container/morcus/613744875).

## Corpus Search Tool

The [corpus search tool](https://morcus.net/corpus) is now available, 
and allows making complex queries across the entire library (currently 
1.5 million words, or about 25% of the classical corpus).

You can construct queries:

- On the whole library, or filtered to one author
- For exact sequences 
  - For example, `dedit oscula nato` would find all instaces of `dedit oscula nato`
- Involving lemma or case
  - For example, `@lemma:do oscula @case:dative` would find all instances of any conjugation
    of the lemma `do`, followed by the word `oscula`, followed by any word that could be dative.
- With words close to other words
  - For example, `@lemma:do ~> oscula ~10 @case:dative` would find all instances of any conjugation
    of the lemma `do`, within a few words before (`~>`) the word `oscula`, within 10 words of (`~10`)
    a word that could be dative.

## Library

### New texts

Many more texts (totaling about 500k new words) from the Perseus library and Hypotactic are now available:

- 29 new works by `Cicero`
- 16 new vitae of `Nepos`
- 5 new works (macronized) by `Ovid`
- `De Spectaculis` (macronized) by `Martial`
- The `Metamorphoses` of `Apuleius`
- `Ars Poetica` and `Epodes` (both macronized) by `Horace`
- `Bellum Civile` (macronized) and `Satyricon` by `Petronius`
- `De Vita Caesarum` by `Seutonius`

### Open-in-new-tab

In the library page, clicking on a work with the middle button now opens that
work in a new tab.

## Macronizer

The macronizer (currently hidden because it is still under some development, but available via [direct link](https://morcus.net/macronizer)) 
now has a `Copy Text` button that automatically unicode normalizes and copies all macronized text to the clipboard.

## Typo and Bug Fixes

### Typos

About 10 user suggested typos were fixed (including fixes to various library works, Smith and Hall, and Lewis and Short).
Thanks for reporting!

### Bundle Cache Fix

Fixed a typo that was accidentally setting a max valid age of 1000 years on the app bundle. Some browsers (such as Chrome) seem to have
clamped this to the maximum valid time, but this fix makes caching work properly on all browsers.

## Development

The old `first_time_setup.sh` script is now `set_up_or_update.sh`.

As the name implies, this helps developers set up a development environment the first time, 
but on subsequent runs it will also handle downloading additional data repositories that were
added since the last time the setup script was run, updating all existing data repositores, and
updating dependencies.
