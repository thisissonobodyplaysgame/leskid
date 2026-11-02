# Flux Mini

A small copy of Flux: games, a web proxy and wallpapers.

- The root link (`https://<you>.github.io/<repo>/`) opens the browser directly, always through Scramjet.
- `https://<you>.github.io/<repo>/?url=example.com` opens a site straight in the proxy, full window, with no browser bar.
- `extra.svg?f3` opens the same site inside one SVG page.
- `extra.svg` on its own just shows a picture.
- `calculator.html` is a calculator.

## Put it online

You need [git](https://git-scm.com), Python and the [GitHub CLI](https://cli.github.com).

```bash
gh auth login
python upload.py
```

It makes a public repo called `flux-mini`, turns on GitHub Pages and prints your link. For a different name, run `python upload.py my-repo-name`. Run it again after any change.

## Try it on your computer

```bash
python -m http.server 8000
```

Then open `http://localhost:8000/`.

## Change things

- **The page:** edit `src/page.html`, then run `python build_svg.py` (it writes `index.html` and `extra.svg`).
- **Games:** add a folder to `edutools/` and a line to `edulist.txt`, with its cover in `visuals/`.
- **The picture:** replace `src/decoy.svg`.
