# Chi Wan Homepage

This repository contains Chi Wan's personal academic homepage, built with
[Hugo](https://gohugo.io/) and the [barks](https://github.com/timothygebhard/barks)
theme.

## Local Preview

```bash
hugo server --bind 127.0.0.1 --port 1313 --disableFastRender
```

Then open:

```text
http://localhost:1313/
```

## Content

- Main homepage content: `content/_index.md`
- Custom styles: `static/css/custom.css`
- Static assets: `static/assets/`
- Publication images: `static/publication/`
- Theme: `themes/barks/`

## Build

```bash
hugo
```

The generated site is written to `public/`, which is ignored by git.
