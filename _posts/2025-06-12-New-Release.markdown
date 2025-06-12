---
layout: post
title: "Morcus Release (June 2025)"
subtitle: "Now available: Pozo (Spanish to Greek / Latin dictionary); Roman numerals; more Cicero; PDF links for library works."
tags: release
---

See the updates [live](https://morcus.net),
browse the [code](https://github.com/nkprasad12/morcus-net/commit/31d995dc213263e159e0183a72e96ba653ecb967),
or get the [Docker image](https://github.com/nkprasad12/morcus-net/pkgs/container/morcus/436994398).

# Features

## Dictionary

### Pozo (Early Preview)

A Spanish to Greek / Latin dictionary is now available. Due to a significant number of typos in the digitization, this is disabled by default (as we fix the issues) but can be turned in on the settings.
 
Thanks to Nikita Murzintcev of [latin-dict.github.io](https://latin-dict.github.io/dictionaries/LopezPozo1997.html) for making source data available.

![Example showing the entry for cómo in Pozo.`](/images/2025-06-R1/pozo-como.png)

### Roman Numerals

The numeric information table now shows the Roman numeral representation for an Indo-Arabic numeral.

![Example showing the entry for the number 49.`](/images/2025-06-R1/roman-numerals.png)

## Reader

A bug with incorrect handling of HTML entites in scraped URL texts is now fixed, and should now display correctly.

## Library

### More Cicero

The following are newly available on the [library](https://morcus.net/library):

- `De Lege Agraria` (Cicero) and an English transation
- `Pro Rabirio Perduellonis Reo` (Cicero) and an English translation

### Source Scan Links

Where available, the links to original scans for Library works are now surfaced in the info tab.

![Example showing the source scan link.`](/images/2025-06-R1/source-scan-link.png)
