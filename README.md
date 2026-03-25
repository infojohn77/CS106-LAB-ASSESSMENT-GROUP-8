# The 8th Wardrobe — GitHub Pages Deployment Guide

## Project Structure

```
your-repo/
├── index.html          ← Main website (put this at the ROOT)
└── trustees/
    ├── shegun.jpg
    ├── john.jpg
    ├── adewumi.jpg
    ├── david.jpg
    ├── chisom.jpg
    ├── Adewale.jpg
    ├── Devine.jpg
    ├── purpose.jpg
    ├── michael.jpg
    ├── joshua.jpg
    ├── gbolahan.jpg
    ├── Hafsat.jpg
    └── faith2.jpg

(Product images go in the ROOT alongside index.html)
  clothe1.jpg, clothe3.jpg, clothe5.jpg, clothe7.jpg
  shoe1.jpg, shoe2.jpg
  wo1.jpg, wo4.jpg, wo5.jpg
```

## Deployment Steps

### 1. Create a GitHub Repository
1. Go to [github.com](https://github.com) → click **New repository**
2. Name it anything (e.g. `the8thwardrobe`)
3. Set it to **Public**
4. Click **Create repository**

### 2. Upload your files
**Option A — GitHub web interface (easiest):**
1. Open your new repo
2. Click **Add file → Upload files**
3. Drag and drop `index.html` and all image files
4. For trustee images: create the `trustees/` folder by uploading a file named `trustees/shegun.jpg` (GitHub creates the folder automatically)
5. Click **Commit changes**

**Option B — Git command line:**
```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/YOUR_USERNAME/the8thwardrobe.git
git branch -M main
git push -u origin main
```

### 3. Enable GitHub Pages
1. In your repo, go to **Settings → Pages**
2. Under **Source**, select **Deploy from a branch**
3. Choose branch: `main`, folder: `/ (root)`
4. Click **Save**
5. Wait ~1 minute — your site will be live at:
   `https://YOUR_USERNAME.github.io/the8thwardrobe/`

---

## Setting Up the AI Chatbox

GitHub Pages is static-only, so the API key **cannot** be hidden on a server. Instead, the site has a built-in key input field — whoever uses the chatbox enters their own Anthropic API key, which is stored only in their browser's localStorage and sent directly to Anthropic.

**To get an API key:**
1. Go to [console.anthropic.com](https://console.anthropic.com)
2. Sign in → API Keys → **Create Key**
3. Copy the key (starts with `sk-ant-`)
4. Paste it into the 🔑 field on the website and click **Save**

> The key is stored in the visitor's browser only. It is never sent to GitHub or any other server — only to Anthropic directly.
