# jdesap.github.io

personal website, hosted on github pages. has a math section and a blog.

live at [jdesap.github.io](https://jdesap.github.io)

---

## structure

```
index.html          ← homepage
math/
  index.html        ← list of math articles
  *.html            ← individual articles
blog/
  index.html        ← list of blog posts
  *.html            ← individual posts
assets/
  css/style.css     ← all the styling, including dark mode
```

---

## if you want to use this for yourself

feel free to fork it. here's what you need to change:

**1. find and replace `jdesap` with your name/handle** in these files:
- `index.html` (appears in the nav, the h1, and the footer)
- `math/index.html`
- `blog/index.html`
- any article files you keep

**2. edit your homepage** — open `index.html` and change the intro paragraph and the email/linkedin links near the top of the `<main>` section.

**3. delete my articles** (actually, if you need it, keep one as one example, but don't index it pls, i worked hard on them ;).

---

## adding a new post

1. copy an existing article file (e.g. `math/bigezioni.html`) and rename it
2. edit the title, date, and content inside
3. add a line to the relevant index (`math/index.html` or `blog/index.html`):

```html
<li class="post-item">
  <a href="your-file.html">Your Title</a>
  <span class="post-date">2026-06-03</span>
</li>
```

4. upload both files to github and you're done

---

## latex / math

math articles use [MathJax](https://www.mathjax.org/). wrap inline math in `$...$` and display math in `$$...$$`. make sure this line is in the `<head>` of your article:

```html
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>
```

---

## themes

there's a toggle in the nav. preference is saved in localStorage so it persists across pages.
