# 🚀 Deployment Guide

## Quick Deployment to GitHub Pages

Follow these steps to host the ULI Validator on GitHub Pages.

---

## Prerequisites

- GitHub account
- Git installed on your computer
- Basic familiarity with command line

---

## Step-by-Step Instructions

### 1. Create GitHub Repository

1. Go to https://github.com/new
2. Repository name: `uli-validator` (or your preferred name)
3. Description: `ULI Security Document Validator for IP/URL Whitelisting`
4. Set to **Public** (required for GitHub Pages free tier)
5. **Do NOT** initialize with README (we already have one)
6. Click "Create repository"

### 2. Push Code to GitHub

Open terminal/command prompt in the `uli-validator-git` folder and run:

```bash
# Add all files
git add .

# Commit files
git commit -m "Initial commit: ULI Security Document Validator v1.0"

# Rename branch to main (if needed)
git branch -M main

# Add your GitHub repository as remote
git remote add origin https://github.com/YOUR_USERNAME/uli-validator.git

# Push to GitHub
git push -u origin main
```

**Replace `YOUR_USERNAME` with your actual GitHub username!**

### 3. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (top menu)
3. Click **Pages** (left sidebar)
4. Under "Source":
   - Select **GitHub Actions** (recommended)
   - OR select **Deploy from a branch** → choose `main` branch → `/ (root)`
5. Click **Save**

### 4. Wait for Deployment

- GitHub will automatically build and deploy your site
- Check the **Actions** tab to see progress
- Deployment usually takes 1-2 minutes

### 5. Access Your Site

Your validator will be available at:

```
https://YOUR_USERNAME.github.io/uli-validator/
```

---

## Custom Domain (Optional)

### If RBIH wants to use a custom domain:

1. **Settings** → **Pages**
2. Under "Custom domain", enter: `validator.uli.rbih.in`
3. Add DNS records at your domain registrar:
   ```
   Type: CNAME
   Name: validator.uli.rbih.in
   Value: YOUR_USERNAME.github.io
   ```

---

## Updating the Validator

When you make changes:

```bash
# Make your changes to index.html or other files

# Stage changes
git add .

# Commit with descriptive message
git commit -m "Fix: Improved LOW+HIGH detection logic"

# Push to GitHub
git push

# GitHub Actions will automatically redeploy
```

---

## Sharing with RBIH Team

### For Pilot Testing:

1. **Share the URL:**
   ```
   https://YOUR_USERNAME.github.io/uli-validator/
   ```

2. **Create a short link (optional):**
   - Use https://bit.ly or https://tinyurl.com
   - Example: `bit.ly/uli-validator-pilot`

3. **Email Template:**
   ```
   Subject: ULI Security Document Validator - Pilot Access

   Hi Team,

   The ULI Security Document Validator is now live for pilot testing:

   🔗 https://YOUR_USERNAME.github.io/uli-validator/

   Features:
   - Validates all 3 mandatory documents (Anti-Malware, Architecture, VAPT)
   - 20+ automated checks
   - OCR support for scanned PDFs
   - 100% private (no data uploaded)

   Please test and provide feedback on:
   - Accuracy of validation checks
   - Ease of use
   - Any issues or bugs

   Feedback: Create issue at GitHub or email support@uli.rbih.in

   Thanks!
   ```

---

## Troubleshooting

### Issue: Page shows 404

**Solution:**
1. Check Settings → Pages → ensure GitHub Pages is enabled
2. Verify file name is `index.html` (lowercase)
3. Wait 5 minutes and hard refresh (Ctrl+Shift+R)

### Issue: Changes not showing

**Solution:**
1. Check Actions tab for deployment status
2. Hard refresh browser (Ctrl+Shift+R)
3. Clear browser cache

### Issue: GitHub Actions fails

**Solution:**
1. Go to Settings → Pages
2. Switch to "Deploy from a branch"
3. Select `main` branch, `/ (root)`

---

## Security Considerations

### For Production Deployment:

1. **Enable HTTPS** (automatically enabled on GitHub Pages)
2. **Review logs** regularly in Settings → Insights → Traffic
3. **Monitor issues** on GitHub Issues tab
4. **Keep dependencies updated** (PDF.js, Tesseract.js)

### What's Safe:

✅ All processing happens client-side  
✅ No server uploads  
✅ No logging or analytics  
✅ No cookies or tracking  

---

## Alternative Hosting Options

### If GitHub Pages doesn't work:

1. **Netlify** (Free tier)
   - Drag & drop `uli-validator-git` folder
   - Auto-deploy on git push
   - URL: `uli-validator.netlify.app`

2. **Vercel** (Free tier)
   - Connect GitHub repository
   - Auto-deploy on push
   - URL: `uli-validator.vercel.app`

3. **CloudFlare Pages** (Free tier)
   - Connect GitHub repository
   - Fast global CDN
   - URL: `uli-validator.pages.dev`

---

## Monitoring Usage (Optional)

### If you want to track usage:

1. Add Google Analytics (optional)
2. Add privacy-friendly analytics:
   - Plausible Analytics
   - Simple Analytics
   - Fathom Analytics

**Note:** For pilot, recommend NO analytics to maintain privacy.

---

## Support

If you encounter issues during deployment:

1. **GitHub Pages Documentation:**
   https://docs.github.com/en/pages

2. **Git Help:**
   https://git-scm.com/doc

3. **Contact:**
   Create an issue on GitHub repository

---

## Checklist

Before sharing with RBIH team:

- [ ] Repository created on GitHub
- [ ] Code pushed to GitHub
- [ ] GitHub Pages enabled
- [ ] Site accessible at URL
- [ ] Test all 3 document types
- [ ] Test on mobile devices
- [ ] Update README with actual URL
- [ ] Share URL with team

---

**You're all set! 🎉**

The validator is now live and ready for pilot testing with the RBIH team.
