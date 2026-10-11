# OpenCanvas

A free, open-source design editor that runs entirely in your browser. No account, no login, no tracking, no installation.

**Live app:** `https://radebekhethelo55-dot.github.io/opencanvas/` 

## What you can do

- Add shapes (rectangle, circle, triangle, star, heart, arrow, line) and text
- Upload images (PNG, JPG, WebP, GIF) by button, drag-and-drop or paste
- Drag, resize, rotate, recolor, change opacity, reorder layers, duplicate
- Select several items at once (drag a box, or Shift-click), then move, align, space evenly, recolor, duplicate or delete them together
- Gradients on shapes, text and the page background
- Smart snapping to the page centre and edges
- Start from templates or standard sizes (Instagram, Story, YouTube, A4, business card, and more)
- Undo and redo
- Export to PNG, JPG, PDF or SVG
- Save a design as a `.json` file and open it later
- Optional: describe a design in plain words and let Claude build or edit it

## Use it

1. Open the live link above in any modern browser (Chrome, Edge, Firefox, Safari), on phone or computer.
1. That’s it. Nothing to sign up for.

Run it on your own computer: download `index.html` and double-click it. It is a single file with no dependencies.

## Claude integration (optional)

Open the **Claude** tab, paste your own Anthropic API key, and type what you want (“make a bake sale poster”, “make the title bigger”). Claude replies with simple commands that the editor applies to your page.

- The editor works fully without this feature and without any login.
- Your key stays in the page and is sent only to `api.anthropic.com`. It is only saved in the browser if you tick “Remember”.
- Claude receives the layout of your page (text, sizes, colors). Uploaded pictures are never sent.
- API usage is billed to the key owner by Anthropic.

Developers can also drive the editor from the browser console or another script:

```js
OpenCanvas.getDesign();                       // current design as JSON
OpenCanvas.run([{op:"add_text",text:"Hi",fontSize:80}]);
```

Supported commands: `set_canvas`, `add_text`, `add_shape`, `update`, `delete`, `reorder`, `clear`.

## Privacy and security

- One HTML file, zero third-party libraries, zero network calls except the optional Claude request.
- A strict Content-Security-Policy in `index.html` blocks any other outside connection.
- Designs and images never leave your device.
- Uploaded SVG files are rejected, and opened design files are validated before use.
- Please read the source before you trust it: it is about 700 readable lines.

## Publish on GitHub Pages

1. Create a new public repository named `opencanvas`.
1. Upload `index.html`, `README.md` and `LICENSE` to the root of the repo.
1. Go to **Settings → Pages**, set **Source** to “Deploy from a branch”, choose branch `main` and folder `/ (root)`, then Save.
1. Wait a minute or two. Your app is live at `https://YOUR-USERNAME.github.io/opencanvas/`.

## Contributing

Pull requests are welcome. Ideas: grouping, more shapes, image filters, Google-Fonts-free font packs, multi-page designs, a translations file.

Please keep the project dependency-free and login-free.

## License

MIT. See <LICENSE>.

OpenCanvas is an independent project and is not affiliated with Canva.
