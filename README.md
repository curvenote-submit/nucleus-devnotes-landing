# Nucleus Developer Notes: landing site

The landing pages of [Nucleus Developer Notes](https://devnotes.nucleus.engineering/): the
home page, the collection listings, the contribute page and the DevNotes network. The
DevNotes themselves are submitted to the `bnext-devnotes` venue from their own repositories;
these pages list them.

On every push to `main`, [`landing.yml`](.github/workflows/landing.yml) builds the
[DevNotes network widget](widgets/devnotes-network/README.md), pushes this project to
Curvenote as a Work (`project.id` in `curvenote.yml`) and sets it as the site's landing
content. Run it by hand to refresh the notes cached into the widget.

## Working on it

```bash
(cd widgets/devnotes-network && bun install && bun run build)
curvenote start
```

The pages are listed in the `toc` of `curvenote.yml`.

## Contact

If you have problems, questions, ideas, or suggestions, please contact us at build@bnext.bio.
