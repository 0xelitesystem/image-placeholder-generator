# Image Placeholder Generator

Generate lightweight placeholder images as inline SVG data URIs. No raster encoding, no network request. Set the size, colors, label, and style, then copy the output in the format you need.

## Live demo

https://0xelitesystem.github.io/image-placeholder-generator/

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

Everything is generated in your browser. Your inputs and the generated markup never leave your machine. There are no external requests, no analytics, and no tracking.

## License

MIT. Copyright 0xelitesystem 2026.
