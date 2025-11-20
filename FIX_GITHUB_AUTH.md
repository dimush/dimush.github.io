# 🔑 QUICK FIX: GitHub Authentication Error

## The Problem
```
Password authentication is not supported for Git operations.
fatal: Authentication failed
```

## ✅ The Solution (5 minutes)

### Option 1: Create Personal Access Token (Recommended)

**Step 1: Create Token**
- Run: `create_github_token.bat` (this opens GitHub for you)
- OR manually go to: https://github.com/settings/tokens/new
- Configure:
  - Note: `CrushLabyrinth`
  - Expiration: `90 days`
  - Scopes: ✅ Check `repo`
- Click **Generate token**
- **COPY THE TOKEN** (starts with `ghp_...`)

**Step 2: Configure Git to Save Token**
```cmd
git config --global credential.helper wincred
```

**Step 3: Push Again**
```cmd
cd C:\Development\Android\CrushLabyrinth
git push -u origin main
```

**Step 4: Enter Credentials**
- Username: `dimush`
- Password: **Paste your token** (right-click to paste in cmd)

**Done!** Windows will save your token for future use.

---

### Option 2: Use Token in URL (Quick One-Time Push)

```cmd
cd C:\Development\Android\CrushLabyrinth
git remote remove origin
git remote add origin https://dimush:YOUR_TOKEN@github.com/dimush/WebPages.git
git push -u origin main
```

Replace `YOUR_TOKEN` with your actual token.

---

## 📋 Quick Commands Summary

```cmd
:: 1. Create token at: https://github.com/settings/tokens/new
:: 2. Configure Git to remember credentials
git config --global credential.helper wincred

:: 3. Push (you'll be prompted for username and token)
cd C:\Development\Android\CrushLabyrinth
git push -u origin main

:: When prompted:
:: Username: dimush
:: Password: [paste your token]
```

---

## 🆘 Troubleshooting

**Can't paste in Command Prompt?**
- Right-click in the cmd window to paste
- Or enable Ctrl+V: Right-click title bar → Properties → Enable Ctrl key shortcuts

**Token not working?**
- Make sure you checked the `repo` scope
- Copy the entire token (no spaces)
- Token is used as PASSWORD, not username

**Want to reset?**
- Clear saved credentials: Control Panel → Credential Manager → Windows Credentials
- Remove any GitHub entries
- Try again with a fresh token

---

## 📚 Full Guide

For detailed instructions with screenshots, see: `GITHUB_TOKEN_SETUP.md`

---

## ⚡ Fastest Path Right Now

1. **Run:** `create_github_token.bat` 
2. **Copy** the token GitHub generates
3. **Run:** `git config --global credential.helper wincred`
4. **Run:** `git push -u origin main`
5. **Paste** token when prompted for password

**That's it!** 🚀

