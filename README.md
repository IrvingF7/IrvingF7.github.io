# Irving Fang — personal research website

The site is static: open `index.html` locally or serve the repository with any
HTTP server.

## Regenerating the social preview

Run:

```bash
python3 scripts/generate_social_preview.py
```

This writes both `images/social-preview.svg` and the 1200×630
`images/social-preview.png` referenced by the page metadata. The generator uses:

- `social-preview.config.json` for the portrait and text;
- the light or dark color tokens in `stylesheet.css`; and
- `scripts/social-preview.template.svg` for layout, decoration, and the robot glyph.

For a one-off photo or palette override:

```bash
python3 scripts/generate_social_preview.py --photo images/new-photo.jpg --palette light
```

Chrome or Chromium is required for deterministic SVG-to-PNG rendering. Use
`--browser /path/to/chrome` if it is not on `PATH`.

## Attribution

The original site foundation is based on
[Jon Barron's academic website](https://jonbarron.info/) and its
[source code](https://github.com/jonbarron/jonbarron_website).
