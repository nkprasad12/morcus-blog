# Running Jekyll Locally

To start the Jekyll server locally run the following from the root directory:

```bash
bundle exec jekyll serve
```

This command builds the site and starts a local web server. The server will automatically regenerate the site when you make changes to most files.

## Viewing Drafts and Future Posts

To include posts marked as drafts (located in the `_drafts` folder) or posts with a future date, use the following flags:

- **Include drafts:** Add the `--drafts` flag.
    ```bash
    bundle exec jekyll serve --drafts
    ```

- **Include future posts:** Add the `--future` flag.
    ```bash
    bundle exec jekyll serve --future
    ```