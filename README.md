# Portfolio

An interactive, design-file-style portfolio. Plain HTML/CSS/JS, no build step, hosted on GitHub Pages.

## Editing content

- **Home page** ([`index.html`](index.html)): the `window.CONTENT` block at the top of the script holds the name, intro, About tabs, experience, contact links, CV path and the four project cards.
- **Case studies** ([`project.html`](project.html)): the `window.CASES` list holds one entry per project, built from sections and blocks (facts, images, galleries, before/after sliders, quotes, results…). The comment above it lists every block type. Each case study is linked by its `slug`, e.g. `project.html?p=checkout-redesign`, which must match the card’s `slug` on the home page.
- **Screenshots:** put them in `assets/projects/<slug>/`, then use them as the card `cover` on the home page and in `image`, `gallery` or `compare` blocks in the case study:
  ```js
  { type:'image', label:'Home screen', src:'assets/projects/checkout-redesign/home.png', caption:'Saved methods come first' }
  ```
- **CV:** `assets/Noha-Ghoweil-CV.pdf`, linked from the contact card.
- Remove `sample:true` from a case study once its content is real; it hides the “sample content” tag.

## Preview locally

```bash
npx http-server -p 5173
```

## Publish

Push to a GitHub repo, then go to **Settings → Pages → Source: Deploy from a branch → `main` / root**.
Name the repo `<username>.github.io` to host it at `https://<username>.github.io`.
