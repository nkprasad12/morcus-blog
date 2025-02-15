# Updates [2024/02]

## Features

### No more auto-expansions

Previously, the dictionaries auto-expanded some abbreviations where we had a high confidence of the meaning of an expansion.
However, there have been a fair number of edge cases where the auto-expansions have resulted in misleading or just incorrect
replacements.

As a result, this release removes all auto-expansions. You can still see the possible expanded forms by clicking on
abbreviated text.

| Old | New |
| --- | --- |
| ![Old screenshot with expansions.](/images/2024-02/old-with-expansions.png) | ![New screenshow without expansions](/images/2024-02/new-without-expansions.png)    |

### Reader navigation

The `jump to section` search box has been moved into the top bar. You can quickly navigate to any section with an ID using this box.

Taking `De Bello Gallico`, which has `Book`, `Chapter`, and `Section` divisions:
- Searching `2.1` would take you to `Book 2`, `Chapter 1`.
- Searching `3.2.7` would take you to `Book 3`, `Chapter 2` and scroll down to `Section 7`.
- If you're already on `3.2`, searching `3.2.7` will just scroll down to `Section 7`, as expected.

![Screenshot showing the new search box](/images/2024-02/reader-search-box.png)

## Performance

### `brotli` compression

The main app bundle is now pre-compressed using `brotli` at the highest-level setting. The download size of the site is reduced by about 15% (`98 kB -> 84 kB`) for browsers that support `brotli`.

### Caching of dynamic data

Previously, dyanmically fetched data (such as dictionary entries or texts from the library) were not cached.

What this means is that previously if you opened a dictionary entry, pressed back, and then forward again, your browser would need
to fetch the entry from the server again. Similarly, if you opened a text in the library, and then came back later in the same day
to read some more, your browser would need to fetch the same work twice.

With the new cache settings, if you request the same resource within the same week, it will be cached.