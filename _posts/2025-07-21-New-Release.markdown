---
layout: post
title: "Lots of new works and lots of new quality of life features and fixes!"
subtitle: "TODO: Summarize"
tags: release
---

See the updates [live](https://morcus.net),
browse the [code](https://github.com/nkprasad12/morcus-net/tree/668ccc601c3d5b32fa1212b0571908c8b9d4315f),
or get the [Docker image](https://github.com/nkprasad12/morcus-net/pkgs/container/morcus/466739681).

## General

### Swipe-to-Open Drawer

You can now swipe left from the right edge of the screen to open the navigation drawer on touch screen devices.
The drawer has also moved to the right side of the screen (because some browsers interpret "swipe right from the left edge" as a `Back` gesture).

## Dictionary

### Dismissible Bottom Drawer

Similar to the reader, the bottom drawer of the dictionary view is now dismissible.

## Reader

### Toggleable Section Numbers

Section numbers can now be hidden (and re-enabled) by pressing the `1.2` icon in the top bar. This can be useful on small screens.

| Section Numbers On | Section Numbers Off |
| ------------------ | ------------------- |
| <img src="/images/2025-07-R3/sections-on.png" width="200"> | <img src="/images/2025-07-R3/sections-off.png" width="200"> |

### Reader Tabs

When switching from a sidebar tab and back (for example `Translation` -> `Dictionary` -> `Translation`), the original scroll position of the
first tab is restored (so you can freely switch tabs without losing your place).

### Wake Lock

The wake lock (preventing the screen from turning off on mobile devices) previously had a bug when switching windows; this is now fixed.

## Library

### More Hypotactic Works

Several works of `Horace` are now available in the library. This includes:

- `Sermones`
- `Odes` (or `Carmina`)
- `Epistulae`

Also, the following by `Statius` are available:

- `Achilleid`
- `Silvae`
- `Thebaid`

Finally, `Bellum Civile` (or `Pharsalia`) of `Lucan` has been added.

### Works List

The list of works has been slightly revamped in appearance and now shows which works have
translations and which are macronized.

<img src="/images/2025-07-R3/library-listing.png" width="300" aria-label="Example showing the new library listing."> 

## Internal

A few technical items:

- `nginx` has been updated to the latest stable release (the version previously used was deprecated)
- Various `Javascript` packages were updated to avoid potential security issues.
- `nginx` access logs now show the origin IP rather than the Proxy's IP.
- API call logging has been updated try to avoid logging requests from crawlers.
