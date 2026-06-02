# Portfolio Website — Setup & Usage Guide

---

## PART 1: Setting up GitHub Pages (one-time, ~15 minutes)

### Step 1 — Create a GitHub account
Go to https://github.com and sign up if you don't have an account.

### Step 2 — Create a new repository
1. Click the **+** icon (top right) → **New repository**
2. Name it exactly: `yourusername.github.io`
   (replace `yourusername` with your actual GitHub username, lowercase)
3. Set it to **Public**
4. Click **Create repository**

### Step 3 — Upload your files
1. On the repository page, click **uploading an existing file**
2. Drag and drop ALL the files you downloaded, keeping the folder structure:
   - `index.html`
   - `assets/css/style.css`
   - `math/index.html`
   - `math/basel-problem.html`  ← example, you can delete this later
   - `blog/index.html`
   - `blog/reading-slowly.html` ← example, you can delete this later
3. Scroll down and click **Commit changes**

### Step 4 — Enable GitHub Pages
1. Go to your repository → **Settings** tab
2. Click **Pages** in the left sidebar
3. Under "Branch", select **main** and click **Save**
4. Wait 1–2 minutes, then visit: `https://yourusername.github.io`

Your site is live! 🎉

---

## PART 2: Personalizing your homepage

Open `index.html` in any text editor (Notepad works, but VS Code is nicer — it's free at https://code.visualstudio.com).

Find the sections marked `✏️ EDIT THIS` and change:

```html
<!-- Your name (appears in 3 places — search "Your Name") -->

<!-- Your intro paragraph -->
<p class="intro-text">
  Hi! I'm a mathematician / student / curious person based in [City].
  ...
</p>

<!-- Your contact links -->
<a href="mailto:you@email.com" ...> you@email.com </a>
<a href="https://linkedin.com/in/yourprofile" ...> LinkedIn </a>
```

After editing, re-upload the file to GitHub (same drag-and-drop process, GitHub will replace the old version).

---

## PART 3: Writing a new Math article

### Step A — Create the HTML file
Copy the file `math/basel-problem.html`, rename it to something like `math/my-topic.html`.

The filename becomes the URL: `yourusername.github.io/math/my-topic.html`
Use lowercase letters and hyphens, no spaces.

### Step B — Edit the article content

Change the title, date, and body:

```html
<title>Your Article Title — Your Name</title>
...
<h1>Your Article Title</h1>
<div class="article-meta">June 15, 2025</div>
...
<article class="prose">
  Your content here
</article>
```

### Step C — Writing LaTeX

Inline math (inside a sentence): wrap with single dollar signs
  → `The series $\sum_{n=1}^{\infty} \frac{1}{n}$ diverges.`

Display math (centered on its own line): wrap with double dollar signs
  → `$$\int_0^\infty e^{-x^2} dx = \frac{\sqrt{\pi}}{2}$$`

### Step D — Adding images

1. Put your image file (e.g. `diagram.png`) in the `math/` folder
2. In your article, add:
   ```html
   <img src="diagram.png" alt="Description of the image" />
   ```

### Step E — Register the article on the index page

Open `math/index.html`. Find the `<ul class="post-list">` section and add a line:

```html
<li class="post-item">
  <a href="my-topic.html">Your Article Title</a>
  <span class="post-date">2025-06-15</span>
</li>
```

Also **delete** (or keep) the example `<li class="empty-state">` line.

### Step F — Upload to GitHub

Drag and drop your new `.html` file (and any images) onto your GitHub repository.

---

## PART 4: Writing a new Blog post

Same process as Math, but:
- Copy `blog/reading-slowly.html` instead
- No LaTeX needed (but it works if you want it — just add the MathJax script tags from the math template)
- Add the listing entry to `blog/index.html`

---

## PART 5: Quick reference

| Task | File to edit |
|------|-------------|
| Change your name/intro/links | `index.html` |
| Add a math article to the list | `math/index.html` |
| Add a blog post to the list | `blog/index.html` |
| Change site colors or fonts | `assets/css/style.css` |

### Color customization (optional)

Open `assets/css/style.css`. At the top you'll see:

```css
:root {
  --bg:       #f5f1eb;   /* page background */
  --ink:      #1a1208;   /* main text color */
  --accent:   #8b3a1a;   /* rust/red highlight color */
  --border:   #c9c0b0;   /* lines and borders */
}
```

Change any hex color code to customize the palette. 
Use https://coolors.co to pick colors.

---

## Tips

- **Committing on GitHub** = saving/publishing. Every time you upload a changed file, the site updates within ~30 seconds.
- **Test locally** by just double-clicking `index.html` — it opens in your browser without internet.
- LaTeX won't render locally (it needs the CDN), but everything else will.
- Keep article filenames short and URL-friendly: `riemann-hypothesis.html` not `My Article About The Riemann Hypothesis!!.html`
