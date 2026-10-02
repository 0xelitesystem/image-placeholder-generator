# Image Placeholder Generator

Generate lightweight placeholder images as inline SVG data URIs. No raster encoding, no network request. Set the size, colors, label, and style, then copy the output in the format you need.

**Live demo:** https://0xelitesystem.github.io/image-placeholder-generator/

## Use

1. Set the width and height.
2. Pick background and text colours, a label, a font size (zero auto-sizes), and the solid or cross style.
3. Check the live preview.
4. Click **Copy** next to the format you need: raw SVG, data URI, `<img>` tag, or CSS background-image.

## Why this exists

Mockups and layouts need placeholder images, and pulling them from a remote placeholder service adds a network dependency. This tool generates tiny inline SVG placeholders locally. It is one HTML file with inline CSS and JavaScript: no account, no tracking, no analytics, no external scripts or fonts, and it works offline. MIT licensed, so you can fork it, self-host it, or read every line.

## Features

- Controls for width, height, background color, text color, a custom label (defaults to WxH), and font size (auto-sizes when left at zero).
- Solid or diagonal-cross style.
- Live preview on a checkerboard so transparency and edges are visible.
- Four outputs, each with a copy button: the raw SVG, a `data:` URI, an `<img>` tag, and a CSS `background-image`.
- Dark mode toggle, keyboard and screen-reader friendly (the SVG carries an aria-label).
- One file, no external dependencies, works offline.

## How it works

The tool assembles a small SVG string from your inputs: a `<rect>` for the background, optional cross lines, and centered `<text>` for the label. That SVG is URL-encoded into a `data:image/svg+xml` URI, which is used for the live preview and the four copyable outputs. Because it is vector SVG, the output stays tiny and scales cleanly at any resolution, and no image is ever fetched or rasterized.

## Privacy

Everything is generated in your browser. Your inputs and the generated markup never leave your machine. There are no external requests, no analytics, and no tracking. The only thing written to storage is your light or dark theme choice, saved in localStorage under the key `theme`.

## Run locally

```bash
git clone https://github.com/0xelitesystem/image-placeholder-generator
cd image-placeholder-generator
```

Then open `index.html` in any modern browser. Or serve the folder with `python -m http.server 8000` and visit http://localhost:8000.

## Build

No build step. The whole tool is one `index.html` with no dependencies, so there is nothing to install or compile.

## More

Part of a catalog of single-file browser tools and plain-language references, all MIT licensed and dependency-free: [0xelitesystem.github.io](https://0xelitesystem.github.io/). Built by [elitesystem.ai](https://elitesystem.ai).

## License

MIT. Copyright 0xelitesystem 2026.
