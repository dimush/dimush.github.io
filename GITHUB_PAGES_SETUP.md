# GitHub Pages Setup for app-ads.txt

## Why GitHub Pages?

Google Sites doesn't support uploading custom files like `app-ads.txt` to the root directory. 
GitHub Pages is a free, reliable solution that gives you full control over your files.

## Setup Instructions (5-10 minutes)

### Step 1: Push Your Code to GitHub (if not already done)

1. Go to [GitHub](https://github.com) and sign in (create account if needed)
2. Create a new repository named `CrushLabyrinth` (or similar)
3. In your local project, run these commands:

```bash
cd C:\Development\Android\CrushLabyrinth
git init
git add .
git commit -m "Initial commit with app-ads.txt"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/CrushLabyrinth.git
git push -u origin main
```

### Step 2: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (top menu)
3. Click **Pages** (left sidebar)
4. Under "Source":
   - Select branch: **main**
   - Select folder: **/docs**
   - Click **Save**
5. Wait 1-2 minutes for deployment

### Step 3: Verify Your Site

Your site will be available at:
```
https://YOUR_USERNAME.github.io/CrushLabyrinth/
```

Your app-ads.txt will be at:
```
https://YOUR_USERNAME.github.io/CrushLabyrinth/app-ads.txt
```

### Step 4: Update Google Play Console

1. Go to [Google Play Console](https://play.google.com/console/)
2. Select your app "Crush Labyrinth"
3. Go to **Store presence** → **Store settings**
4. Update the **Website** field with your GitHub Pages URL
5. Save changes

### Step 5: Update AdMob

1. Go to [AdMob Console](https://apps.admob.com/)
2. Select your app
3. Go to **App settings**
4. Update the **App URL** with your GitHub Pages URL
5. Save changes

## Alternative: Simple HTML Redirect

If you want to keep your Google Sites as the main site, the GitHub Pages site includes:
- A simple landing page that redirects visitors to your Google Sites
- The app-ads.txt file in the root for AdMob verification

Visitors will see a notice and can click through to your Google Sites page.

## Verification

After 24 hours, check that AdMob has verified your app-ads.txt:
1. Test the URL: `https://YOUR_USERNAME.github.io/CrushLabyrinth/app-ads.txt`
2. Check AdMob console for verification status

## Files Created

- `docs/index.html` - Landing page with redirect to Google Sites
- `docs/app-ads.txt` - Your app-ads.txt file for AdMob

## Troubleshooting

**Q: My GitHub Pages site isn't working**
- Wait 5-10 minutes after enabling Pages
- Check that you selected the `/docs` folder
- Verify files are in the `docs` folder in your repository

**Q: Can I use a custom domain?**
- Yes! GitHub Pages supports custom domains
- See: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site

**Q: Do I need to keep Google Sites?**
- No, but you can! The GitHub Pages site redirects to it
- Or migrate everything to GitHub Pages

## Next Steps

After setup:
- [ ] Push code to GitHub
- [ ] Enable GitHub Pages
- [ ] Verify app-ads.txt URL works
- [ ] Update Google Play Console with new URL
- [ ] Update AdMob with new URL
- [ ] Wait 24 hours for verification

