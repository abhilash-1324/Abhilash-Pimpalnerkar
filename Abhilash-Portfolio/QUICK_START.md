# 🚀 Quick Start - Deploy in 5 Minutes

## Your portfolio is ready! Follow these simple steps:

### Step 1: Check Your Files ✅
Make sure you have:
- ✅ `assets/profile.jpg` - Your professional photo
- ✅ `assets/resume.pdf` - Your latest resume
- ✅ All other files are ready

### Step 2: Update Your Information 📝

**In `index.html`, find and replace:**
1. LinkedIn URL: Search for `linkedin.com/in/abhilash-pimpalnerkar`
2. GitHub URL: Search for `github.com/abhilash-pimpalnerkar`
3. Email: Verify `pimpalnerkarabhilash@gmail.com`
4. Phone: Verify `+91 93569 55721`

### Step 3: Deploy to GitHub Pages 🌐

**Option A: Via GitHub Website (Easiest)**

1. Go to [github.com](https://github.com)
2. Click **"New repository"**
3. Name: `yourusername.github.io` OR `Abhilash-Portfolio`
4. Select **Public**
5. Click **"Create repository"**
6. Click **"Upload files"**
7. Drag ALL your portfolio files
8. Click **"Commit changes"**
9. Go to **Settings** → **Pages**
10. Source: Select **main** branch
11. Click **Save**
12. ✨ Your site is live at: `https://yourusername.github.io`

**Option B: Via Git Command Line**

```bash
cd "path/to/Abhilash-Portfolio"
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/yourusername/Abhilash-Portfolio.git
git branch -M main
git push -u origin main
```

Then enable GitHub Pages in Settings → Pages

### Step 4: Test Your Site 🧪

Visit your URL and check:
- ✅ Navigation works
- ✅ Profile image displays
- ✅ Resume downloads
- ✅ Social links work
- ✅ Mobile responsive (resize browser)

### Step 5: Share Your Portfolio 🎉

Add your portfolio URL to:
- LinkedIn profile
- Resume
- Email signature
- GitHub profile README
- Twitter/X bio

---

## Need More Details?

- **Full Deployment Guide**: See [DEPLOYMENT_GUIDE.md](DEPLOYMENT_GUIDE.md)
- **Customization Help**: See [README.md](README.md)
- **Troubleshooting**: See [DEPLOYMENT_GUIDE.md](DEPLOYMENT_GUIDE.md) → Troubleshooting section

---

## Common First Steps

### Change Colors
Edit `style.css` line 8-15:
```css
:root {
    --primary-color: #3b82f6;  /* Change this! */
}
```

### Update Content
Edit `index.html`:
- Search for sections you want to change
- Update text directly
- Save and push changes

### Add Projects
Edit `index.html` → Find `<section id="projects">`
- Copy a project card
- Paste and modify for your project

---

**That's it! Your portfolio is ready to deploy! 🚀**

Any issues? Check [DEPLOYMENT_GUIDE.md](DEPLOYMENT_GUIDE.md) for detailed troubleshooting.
