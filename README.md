# ✅ Steps to Publish GitHub Pages using MkDocs

> ⚠️ **Prerequisites**
- GitHub Pages is always **public**. Even if your repo is private, the site **won’t render** until the repo is made public.
- Ensure you have **Git** and **MkDocs** installed locally.

---

## 🛠️ Step 1: Clone the Repository

```bash
git clone https://github.com/GamyaInc/docs.git 
cd docs
```

Create a new Markdown page:

```bash
echo "# Welcome to My Docs" > docs/<new_page>.md
```

Add and push your changes:

```bash
git add docs/
git commit -m "Add new doc"
git push
```

---

## 📦 Step 2: Install MkDocs Locally

MkDocs builds your `.md` files into a clean, static site.

```bash
pip install mkdocs mkdocs-material
```

---

## ⚙️ Step 3: Create or Update `mkdocs.yml`

In the repo root, edit `mkdocs.yml`:

```yaml
site_name: My GitDoc
nav:
  - Home: index.md
  - Guide: guide.md
theme:
  name: material
```

---

## 👀 Step 4: Preview the Site Locally (Optional)

```bash
mkdocs serve
```

Visit the local site in your browser:  
[http://127.0.0.1:8000](http://127.0.0.1:8000)

---

## 🚀 Step 5: Deploy to GitHub Pages

```bash
mkdocs gh-deploy --clean
```

This will:
- Build your site
- Push it to the `gh-pages` branch
- Enable GitHub Pages

---

## 🌐 View Your Live Site

Example:
```
https://gamyainc.github.io/docs/
```

---
