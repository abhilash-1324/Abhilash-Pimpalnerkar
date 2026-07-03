# 🚀 Deployment Guide for GitHub Pages

This guide will walk you through deploying your portfolio to GitHub Pages step by step.

## Prerequisites

- [ ] GitHub account (create one at [github.com](https://github.com))
- [ ] Portfolio files ready in the folder
- [ ] Profile photo at `assets/profile.jpg`
- [ ] Resume PDF at `assets/resume.pdf`

## Quick Start (5 Minutes)

### Step 1: Create GitHub Repository

1. Go to [GitHub](https://github.com)
2. Click the **"+"** icon (top right) → **"New repository"**
3. Repository name: Choose one of these options:
   - **Option A** (Recommended): `yourusername.github.io` 
     - Example: `abhilash-pimpalnerkar.github.io`
     - Site will be: `https://yourusername.github.io`
   - **Option B**: `Abhilash-Portfolio`
     - Site will be: `https://yourusername.github.io/Abhilash-Portfolio`
4. Description: "Professional DevOps Engineer Portfolio"
5. Select **Public** (required for free GitHub Pages)
6. ✅ Check "Add a README file" (or skip if uploading existing files)
7. Click **"Create repository"**

### Step 2: Upload Your Portfolio Files

#### Method A: Web Upload (Easiest)

1. In your new repository, click **"Add file"** → **"Upload files"**
2. Drag all these files into the upload area:
   ```
   index.html
   style.css
   script.js
   README.md
   LICENSE
   .gitignore
   robots.txt
   CNAME (only if using custom domain)
   assets/ (folder with profile.jpg and resume.pdf)
   ```
3. Commit message: "Add portfolio files"
4. Click **"Commit changes"**

#### Method B: Using Git (For Developers)

```bash
# Navigate to your portfolio folder
cd "C:\Users\SM25CR\OneDrive - ING\Documents\Personal\Abhilash_Professional_Portfolio\Abhilash-Portfolio"

# Initialize Git
git init

# Add all files
git add .

# Commit
git commit -m "Initial portfolio commit"

# Add remote (replace 'yourusername' with your GitHub username)
git remote add origin https://github.com/yourusername/Abhilash-Portfolio.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. In your repository, go to **Settings** (top menu)
2. Scroll down to **"Pages"** (left sidebar)
3. Under **"Source"**:
   - Branch: Select **main** (or **master**)
   - Folder: Select **/ (root)**
4. Click **"Save"**
5. Wait 2-3 minutes for deployment
6. Refresh the page - you'll see: **"Your site is live at..."**

🎉 **Done!** Your portfolio is now live!

## Post-Deployment Checklist

After deployment, verify everything works:

- [ ] Visit your GitHub Pages URL
- [ ] Test all navigation links
- [ ] Check mobile responsiveness (use browser DevTools)
- [ ] Verify profile image loads
- [ ] Test resume download
- [ ] Check all social media links
- [ ] Test on different browsers

## Customization Before Deployment

### 1. Update Social Links

Edit `index.html` and replace:

```html
<!-- Replace these URLs -->
<a href="https://linkedin.com/in/abhilash-pimpalnerkar" target="_blank">
<a href="https://github.com/abhilash-pimpalnerkar" target="_blank">
```

With your actual profile URLs:
```html
<a href="https://linkedin.com/in/YOUR-LINKEDIN-USERNAME" target="_blank">
<a href="https://github.com/YOUR-GITHUB-USERNAME" target="_blank">
```

### 2. Update Contact Information

In `index.html`, verify your contact details:
- Email address
- Phone number
- Location

### 3. Customize Content

Update these sections:
- About Me description
- Skills and proficiency levels
- Work experience details
- Project descriptions

### 4. Replace Assets

Ensure you have:
- `assets/profile.jpg` - Your professional photo (square, at least 400x400px)
- `assets/resume.pdf` - Your latest resume

## Using a Custom Domain (Optional)

If you want to use your own domain (e.g., `abhilash.dev`):

### Step 1: Configure CNAME File

1. Edit the `CNAME` file in your repository
2. Remove the `#` and replace with your domain:
   ```
   yourdomain.com
   ```
3. Save and commit

### Step 2: Configure DNS Settings

Go to your domain provider's DNS settings and add:

**Option A: Using CNAME (Subdomain)**
```
Type: CNAME
Name: www
Value: yourusername.github.io
```

**Option B: Using A Records (Root Domain)**
```
Type: A
Name: @
Value: 185.199.108.153

Type: A
Name: @
Value: 185.199.109.153

Type: A
Name: @
Value: 185.199.110.153

Type: A
Name: @
Value: 185.199.111.153
```

### Step 3: Enable HTTPS

1. Go to repository **Settings** → **Pages**
2. Check **"Enforce HTTPS"** (may take 24 hours to enable)

## Updating Your Portfolio

To make changes after deployment:

### Using GitHub Web Interface

1. Navigate to the file in your repository
2. Click the **pencil icon** (Edit)
3. Make changes
4. Click **"Commit changes"**
5. Changes appear live in 1-2 minutes

### Using Git

```bash
# Make your changes to files

# Stage changes
git add .

# Commit with descriptive message
git commit -m "Update skills section"

# Push to GitHub
git push origin main

# Changes will be live in 1-2 minutes
```

## Troubleshooting

### ❌ Site Not Loading

**Problem**: Getting 404 error

**Solutions**:
- Check that `index.html` is in the root directory
- Verify GitHub Pages is enabled in Settings → Pages
- Wait 3-5 minutes after first deployment
- Check branch name is correct (main vs master)

### ❌ Images Not Loading

**Problem**: Profile photo or assets not showing

**Solutions**:
- Verify files are in `assets/` folder
- Check file names match exactly (case-sensitive)
- Ensure images were uploaded to repository
- Clear browser cache (Ctrl+F5)

### ❌ Styling Issues

**Problem**: Page has no styling

**Solutions**:
- Verify `style.css` is in root directory
- Check link tag in index.html: `<link rel="stylesheet" href="style.css">`
- Clear browser cache
- Check browser console for errors (F12)

### ❌ Custom Domain Not Working

**Problem**: Custom domain shows error

**Solutions**:
- Verify DNS propagation (can take 24-48 hours)
- Check CNAME file contains only domain name (no http://)
- Verify DNS settings with your domain provider
- Wait before enabling HTTPS (needs DNS first)

## Performance Optimization

### Optimize Images

Before uploading, optimize images:
- Profile photo: Max 500KB, 400x400px recommended
- Use JPG for photos (better compression)
- Use PNG only if transparency needed

Tools:
- [TinyPNG](https://tinypng.com/) - Online compression
- [ImageOptim](https://imageoptim.com/) - Desktop app

### Test Performance

After deployment, test your site:
- [Google PageSpeed Insights](https://pagespeed.web.dev/)
- [GTmetrix](https://gtmetrix.com/)
- Target: 90+ score

## SEO Optimization

### Google Search Console

1. Go to [Google Search Console](https://search.google.com/search-console)
2. Add your property (your GitHub Pages URL)
3. Verify ownership
4. Submit sitemap (optional)

### Update Meta Tags

In `index.html`, ensure these are filled:
```html
<meta name="description" content="Your description">
<meta name="keywords" content="Your, Keywords">
<meta name="author" content="Your Name">
```

## Security Best Practices

- ✅ Never commit sensitive data (API keys, passwords)
- ✅ Use HTTPS (automatic with GitHub Pages)
- ✅ Keep contact info professional
- ✅ Review code before committing
- ✅ Don't include personal documents beyond resume

## Monitoring & Analytics (Optional)

### Add Google Analytics

1. Create account at [analytics.google.com](https://analytics.google.com)
2. Get tracking code
3. Add before `</head>` in index.html:
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

## Backup Strategy

Always keep backups:
1. **GitHub** - Your primary backup (version controlled)
2. **Local copy** - Keep original files on your computer
3. **Cloud storage** - Optional: OneDrive, Google Drive, Dropbox

## Next Steps After Deployment

1. ✅ Share your portfolio URL on LinkedIn
2. ✅ Add link to your resume
3. ✅ Include in email signatures
4. ✅ Share in developer communities
5. ✅ Update regularly with new projects
6. ✅ Monitor visitor analytics

## Getting Help

If you encounter issues:

1. **GitHub Pages Docs**: [docs.github.com/pages](https://docs.github.com/en/pages)
2. **GitHub Community**: [github.community](https://github.community)
3. **Stack Overflow**: Tag your question with `github-pages`

## Maintenance Schedule

Keep your portfolio fresh:

- **Weekly**: Check for broken links
- **Monthly**: Update project descriptions
- **Quarterly**: Review and update skills
- **Yearly**: Refresh design and content

---

## Quick Reference Commands

```bash
# Check Git status
git status

# Pull latest changes
git pull origin main

# Add all changes
git add .

# Commit changes
git commit -m "Your message"

# Push to GitHub
git push origin main

# View remote URL
git remote -v

# Clone repository
git clone https://github.com/yourusername/repository.git
```

---

🎉 **Congratulations on deploying your portfolio!**

Need help? Check the [README.md](README.md) for more details.
