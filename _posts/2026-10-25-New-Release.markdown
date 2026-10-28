---
layout: post
title: "Morcus Release (October 2026)"
description: "A redesigned site that's easier to use, faster, and lighter (and can work without JavaScript!)"
tags: release
---

See the updates [live](https://morcus.net), or
browse the [code](https://github.com/nkprasad12/morcus-net/tree/2836f39fd9702acfd8d536f70fd452d375c27991).

Long time, no Morcus update! I've rebuilt the site from the ground up, a large undertaking (and it opens the door to some projects that have been on hold!). Thanks to Andras, Chumpius, Quillful, and many others for their feedback and testing along the way!

## New Look

The whole site has been redesigned, with every page and control reconsidered to make it clearer and easier to use (and a cleaner, more polished look along the way). For example, in the reader, clicking a word now shows the definition right away, instead of below a pile of menus and headers. Lookups are also much faster (0.4s vs 1.5s for a long entry like _cum_).

<video src="/images/2026-10/caesar_1_8_before_after.mp4" autoplay loop muted playsinline controls style="max-width: 100%; border-radius: 6px;"></video>

### Lighter Pages

Across the site, pages load faster and fetch smaller chunks of data on demand. In the reader, books now load one chapter at a time instead of all at once, using much less data and memory:

- Opening Pliny's _Naturalis Historia_ used to download up to 3.2 MB; now each chapter is a few dozen KB.
- Reading Livy uses 21 MB of memory, down from 55 MB.

## Works Without JavaScript

You can now use Morcus with JavaScript turned off: dictionary search, browsing the library, reading texts, and corpus search all work.

This also helps on slow connections, since you can start reading or searching as soon as the page appears, without waiting for it to finish loading.

## Other Notable Changes

- Display settings (theme, font, text size, and line spacing) now live in a single _Appearance_ menu that applies across the site, and on a computer you can drag the edges of the page to make it wider or narrower.
- The `§` button at the top of the reader now opens a searchable table of contents.
- The library shows where you left off in each work, and can be filtered to works with macrons, works with translations, or works you've been reading.
- To report a typo, click a section number in the reader or a sense number in a dictionary entry and choose `Suggest correction`. This now opens a text box with _Submit_ and _Cancel_ buttons, so it's harder to send a report by accident.

## Fixes

- Many user-reported typos were fixed in the dictionaries and library - thank you!
- Raw Beta Code Greek in several library texts has been converted to Unicode.
- Double punctuation in Smith and Hall has been fixed.
