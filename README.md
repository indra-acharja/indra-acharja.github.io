# Indra Prasad Acharja — Personal Website
### Built with [Quarto](https://quarto.org) · Hosted on GitHub Pages (free)

---

## 🚀 Quick Start — Launch your site in ~1 hour

### Step 1: Install the tools (one time only)

1. **Install R** — https://cran.r-project.org  
2. **Install RStudio** — https://posit.co/downloads  
3. **Install Quarto** — https://quarto.org/docs/get-started  
4. **Install Git** — https://git-scm.com/downloads  
5. **Create a free GitHub account** — https://github.com (if you don't have one)

---

### Step 2: Preview the site on your computer

Open RStudio (or any terminal), navigate to this folder, and run:

```bash
quarto preview
```

Your site will open in a browser at `http://localhost:4321`. Any changes you save will update live.

---

### Step 3: Add your photo

1. Place your photo file (e.g. `photo.jpg`) in the root folder of this project  
2. Open `index.qmd` and find this line:
   ```html
   <!-- Replace the line below with: <img src="photo.jpg" alt="Indra Prasad Acharja"> -->
   🦢
   ```
3. Replace those two lines with:
   ```html
   <img src="photo.jpg" alt="Indra Prasad Acharja">
   ```

---

### Step 4: Build the site

```bash
quarto render
```

This creates a `docs/` folder containing your complete website as HTML files.

---

### Step 5: Publish to GitHub Pages (free hosting)

1. **Create a new GitHub repository** named `indraacharja.github.io`  
   - Go to github.com → New repository  
   - Name it exactly: `indraacharja.github.io`  
   - Make it **Public**  
   - Do NOT initialize with README

2. **Connect your local folder to GitHub:**
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/indraacharja/indraacharja.github.io.git
   git push -u origin main
   ```

3. **Enable GitHub Pages:**
   - On GitHub, go to your repo → Settings → Pages  
   - Under "Source", select **Deploy from a branch**  
   - Branch: `main` · Folder: `/docs`  
   - Click Save

4. **Your site is live at:** `https://indraacharja.github.io` (takes ~2 minutes)

---

### Step 6: Point a custom domain (optional, also free)

If you want `www.indraacharja.com` instead of `indraacharja.github.io`:

1. Buy a domain at Namecheap (~$12/year) or Google Domains  
2. In your domain's DNS settings, add a CNAME record:  
   - Name: `www` → Value: `indraacharja.github.io`  
3. In GitHub Pages settings, enter your custom domain  
4. Tick "Enforce HTTPS"

---

## 📁 Project Structure

```
indra-quarto-site/
├── _quarto.yml          ← Site config: navbar, theme, footer
├── styles.css           ← All visual styling
├── index.qmd            ← Home page
├── research.qmd         ← Research page
├── publications.qmd     ← Publications page
├── blog.qmd             ← Blog listing page (auto-generates from posts/)
├── posts/               ← One folder per blog post
│   ├── 2024-03-winter-survey/index.qmd
│   ├── 2024-01-ex-situ-lessons/index.qmd
│   ├── 2023-10-ai-monitoring/index.qmd
│   └── 2023-09-why-phd/index.qmd
└── docs/                ← Generated site (created by `quarto render`)
```

---

## ✏️ Updating your site

### Add a new blog post:
1. Create a new folder in `posts/` (e.g. `posts/2025-05-new-paper/`)
2. Add an `index.qmd` file with YAML header:
   ```yaml
   ---
   title: "Your post title"
   description: "One sentence summary"
   author: "Indra Prasad Acharja"
   date: "2025-05-01"
   categories: [Research, White-bellied Heron]
   ---
   Your post content here...
   ```
3. Run `quarto render` and push to GitHub — it appears on the blog automatically.

### Update publications:
- Open `publications.qmd` and add a new `<div class="pub-item">` block following the existing pattern.

### Update research themes or funding:
- Open `research.qmd` and edit the relevant section.

### Push any update live:
```bash
quarto render
git add .
git commit -m "Update: description of what changed"
git push
```
Your live site updates within ~1 minute.

---

## 🎨 Customisation

All colours are in `styles.css` under `:root`:
```css
:root {
  --ip-accent: #1e4d20;   /* forest green — change for a different accent */
  --ip-bg:     #f9f7f3;   /* warm off-white background */
  --ip-text:   #1a1814;   /* near-black body text */
}
```

To change the navbar title, edit `_quarto.yml`:
```yaml
website:
  title: "Your Name Here"
```

---

## ❓ Need help?

- Quarto documentation: https://quarto.org/docs/websites  
- Quarto blog tutorial: https://quarto.org/docs/websites/website-blog.html  
- GitHub Pages docs: https://docs.github.com/en/pages  
