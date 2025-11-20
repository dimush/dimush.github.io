# Quick Start: Host app-ads.txt on GitHub Pages

## Problem
Google Sites doesn't support uploading `app-ads.txt` to the root directory.

## Solution
Use GitHub Pages (FREE) to host your `app-ads.txt` file.

## ⚡ Quick Setup (10 minutes)

### Step 1: Create GitHub Account & Repository
1. Go to [github.com](https://github.com) and sign up (if needed)
2. Click the **+** icon → **New repository**
3. Name it: `CrushLabyrinth` (or any name)
4. Make it **Public**
5. Click **Create repository**
6. **Leave the page open** - you'll need the URL

### Step 2: Push Your Code to GitHub

**Option A: Use the automated script**
```cmd
cd C:\Development\Android\CrushLabyrinth
setup_github_pages.bat
```
Follow the prompts and enter your GitHub username and repository name.

**Option B: Manual commands**
```cmd
cd C:\Development\Android\CrushLabyrinth
git init
git add docs/ app-ads.txt *.md .gitignore
git commit -m "Add app-ads.txt and GitHub Pages setup"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/CrushLabyrinth.git
git push -u origin main
```
Replace `YOUR_USERNAME` with your GitHub username.

### Step 3: Enable GitHub Pages

1. On GitHub, go to your repository
2. Click **Settings** (top right)
3. Click **Pages** (left sidebar, under "Code and automation")
4. Under **"Build and deployment"**:
   - Source: **Deploy from a branch**
   - Branch: **main**
   - Folder: **/docs**
   - Click **Save**

### Step 4: Wait & Verify (2-5 minutes)

Your site will deploy automatically. After a few minutes:

✅ Your website: `https://YOUR_USERNAME.github.io/CrushLabyrinth/`
✅ Your app-ads.txt: `https://YOUR_USERNAME.github.io/CrushLabyrinth/app-ads.txt`

Test the URL in your browser to make sure it works!

### Step 5: Update Google Play Console

1. Go to [Google Play Console](https://play.google.com/console/)
2. Select "Crush Labyrinth"
3. **Store presence** → **Store settings**
4. Update **Website** field with your GitHub Pages URL
5. Save

### Step 6: Update AdMob

1. Go to [AdMob Console](https://apps.admob.com/)
2. Select your app
3. **App settings**
4. Update **App URL** with your GitHub Pages URL
5. Save

## ✅ Done!

AdMob will verify your `app-ads.txt` file within 24 hours.

---

## What About My Google Sites?

**You can keep it!** The GitHub Pages site includes:
- A simple landing page that links to your Google Sites
- The app-ads.txt file for AdMob verification

Most visitors can still go to your Google Sites page. GitHub Pages is just for the app-ads.txt file.

---

## Troubleshooting

**"Git is not recognized"**
- Install Git: [git-scm.com/download/win](https://git-scm.com/download/win)
- Restart your terminal after installation

**"GitHub Pages not working"**
- Wait 5-10 minutes (first deployment takes time)
- Check Settings → Pages shows a green checkmark
- Verify you selected `/docs` folder

**"Authentication failed"**
- You may need to create a Personal Access Token
- Go to GitHub → Settings → Developer settings → Personal access tokens
- Create a token with "repo" permissions
- Use the token as your password when pushing

---

## Files Created for You

✅ `docs/app-ads.txt` - Your AdMob verification file
✅ `docs/index.html` - Landing page with redirect
✅ `docs/README.md` - Documentation
✅ `setup_github_pages.bat` - Automated setup script
✅ `GITHUB_PAGES_SETUP.md` - Detailed instructions
✅ `HOSTING_OPTIONS_FOR_APP_ADS_TXT.md` - Alternative solutions

---

## Need Help?

See `GITHUB_PAGES_SETUP.md` for detailed instructions and alternatives.

