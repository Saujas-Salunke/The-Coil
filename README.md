# The Coil

A fictional/parody news website built as a college assignment demonstrating
technical SEO and Google Search Console concepts. Static HTML/CSS/JS only —
no backend, no build step, no framework.

> **Mock disclaimer:** The Coil is a fictional parody publication. All
> stories, quotes, and people are invented for demonstration purposes.

## 1. Upload the project to GitHub

1. Create a new, empty repository on GitHub (for example, named `the-coil`).
2. From inside this project's folder, run:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: The Coil"
   git branch -M main
   git remote add origin https://github.com/Saujas-Salunke/the-coil.git
   git push -u origin main
   ```
3. Confirm the files appear in the repository on GitHub, including the
   `css/`, `js/`, and `images/` folders.

## 2. Enable GitHub Pages

1. In your repository, go to **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Choose the **main** branch and the **/(root)** folder, then **Save**.
4. Wait a minute or two, then GitHub will show your live URL, typically:
   ```
   https://Saujas-Salunke.github.io/the-coil/
   ```

## 3. Where to replace `Saujas-Salunke`

Search the project for `Saujas-Salunke` and replace it with your actual
GitHub username in these files:

- `index.html`, `about.html`, `contact.html`, `privacy.html`,
  `article-ai-campus.html`, `article-coffee.html`,
  `article-smartphone.html`, `article-student.html`
  (canonical URLs, Open Graph URLs, Twitter Card image URLs, and JSON-LD)
- `sitemap.xml` (every `<loc>` entry)
- `robots.txt` (the `Sitemap:` line)

Tip: most code editors let you find-and-replace `Saujas-Salunke` across the
whole project in one step.

## 4. Submit the sitemap to Google Search Console

1. Go to [Google Search Console](https://search.google.com/search-console).
2. Add your site as a property using your GitHub Pages URL
   (`https://Saujas-Salunke.github.io/the-coil/`).
3. Verify ownership (see the next section for verification options).
4. Once verified, open **Sitemaps** in the left-hand menu.
5. Enter `sitemap.xml` and click **Submit**.
6. Google will periodically re-crawl the sitemap; you can check indexing
   status under the **Pages** report.

## 5. Where to add Google's verification meta tag

Google Search Console offers a few verification methods; the simplest for
a static GitHub Pages site is the **HTML tag** method:

1. In Search Console, choose the **HTML tag** verification method.
2. Copy the `<meta name="google-site-verification" content="...">` tag
   Google gives you.
3. Open `index.html` and paste it where the following comment is located,
   in the `<head>`:
   ```html
   <!-- Google Search Console verification meta tag goes here if Google provides one -->
   ```
4. Commit and push the change, then click **Verify** in Search Console.

Alternatively, GitHub Pages also supports the **HTML file upload** method
(add the file Google gives you to the repository root) or a **DNS TXT
record** method if you're using a custom domain. This project does not
invent or include a verification code — add your own once Google issues it.

## 6. Demonstrating the SEO elements for your assignment

Each file contains SEO-related comments to help you point these out live:

- **Unique titles & meta descriptions** — open any two pages side by side
  and show the `<title>` and `<meta name="description">` differ.
- **Canonical URLs** — show the `<link rel="canonical">` tag in the page
  source.
- **Structured data** — paste any page's JSON-LD block into Google's
  [Rich Results Test](https://search.google.com/test/rich-results) to show
  it validates.
- **Sitemap & robots.txt** — open `sitemap.xml` and `robots.txt` directly
  in the browser at your live URL to show they're reachable and correctly
  linked together.
- **Semantic HTML** — open dev tools and show the `<header>`, `<nav>`,
  `<main>`, `<article>`, `<section>`, `<aside>`, and `<footer>` elements.
- **Internal linking** — click through from the homepage into an article,
  then into its related articles, to show the link graph.
- **Accessibility & responsiveness** — resize the browser window to show
  the mobile hamburger menu, and tab through the page with the keyboard to
  show visible focus states and the skip-to-content link.

## Project structure

```
the-coil/
├── index.html
├── about.html
├── contact.html
├── privacy.html
├── 404.html
├── sitemap.xml
├── robots.txt
├── manifest.json
├── css/style.css
├── js/main.js
├── images/ (local .jpg files, one per article, plus a README)
└── articles/
    ├── article-ai-campus.html
    ├── article-coffee.html
    ├── article-smartphone.html
    ├── article-student.html
    ├── article-tea.html
    ├── article-almond.html
    ├── article-attendance.html
    ├── article-calculator.html
    ├── article-charger.html
    └── article-playlist.html
```

All ten article pages live together under `articles/`, which keeps the
site's URL structure tidy (`/articles/article-name.html`) and makes it
easy to add new stories in one place. Every article links back to the
homepage, to related articles in the same folder, and to About/Contact/
Privacy at the site root — update `sitemap.xml` with the same `articles/`
path whenever you add a new one.
