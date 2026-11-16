# Doyeon Yoo – Portfolio (Astro)

Your portfolio rebuilt with Astro. The page markup and all of your CSS are the same as the HTML version.
Astro turns it into plain HTML files, so there is no JavaScript framework running on your site.

## Run it

```bash
npm install
npm run dev        # live preview at http://localhost:4321
npm run build      # writes the finished site into /dist
npm run preview    # look at the /dist build locally
```

You need Node.js 18.20 or newer (Node 20+ recommended).

## Where things are

```
public/
  css/                  your CSS files (style.css, about.css, resume.css, hm.css, ...)
  images/               your images
src/
  layouts/Layout.astro  <head>, nav and footer – every page uses this
  components/Nav.astro  the top menu (edit once, every page changes)
  components/Footer.astro
  pages/                one file per page; the file name is the URL
  data/artworks.js      every piece on the Design page
```

## Common edits

- **Change the menu or footer:** edit `Nav.astro` or `Footer.astro`.
- **Add a Design piece:** add an entry to `src/data/artworks.js`
  (category: `photography`, `fine-art`, `illustration` or `multimedia`).
- **Add a page:** create `src/pages/my-page.astro` (it becomes `/my-page`):

  ```astro
  ---
  import Layout from '../layouts/Layout.astro';
  ---
  <Layout title="Doyeon Yoo | My Page" styles={['/css/style.css']} current="projects">
    <section> ...your HTML... </section>
  </Layout>
  ```

  `styles` lists the CSS files from `public/css` the page uses, in order, like the `<link>` tags in the old `<head>`.
  `current` highlights a menu item (`projects`, `resume`, `about`, `design`).

## URLs

| Old file | New URL |
|---|---|
| index.html | / |
| projects.html | /projects |
| resume.html | /resume |
| about.html | /about |
| design.html | /design |
| lennoxGotLunch.html | /lennox-got-lunch |
| kimsDragon.html | /kims-dragon |
| chessRookie.html | /chess-rookie |
| chubb.html | /chubb |
| PaFDC.html | /pa-fdc |
| YarnDatabase.html | /yarn-database |
| dream_job.html | /dream-job |
| personalbranding.html | /personal-branding |
| creative.html / testindex.html | /creative, /test |

## Hosting

`npm run build` gives static files in `dist/`. Netlify, Vercel, Cloudflare Pages and GitHub Pages all work
with no special settings.
# portfolio-astro
