# GitHub Authentication Fix - Personal Access Token Required

## ❌ The Error You're Seeing

```
Password authentication is not supported for Git operations.
fatal: Authentication failed
```

## ✅ Solution: Use Personal Access Token (PAT)

GitHub no longer accepts passwords for Git operations. You must create and use a Personal Access Token.

---

## 🔑 Step-by-Step: Create Personal Access Token

### Step 1: Create the Token (2 minutes)

1. **Go to GitHub** and log in
2. Click your **profile picture** (top right) → **Settings**
3. Scroll down the left sidebar → Click **Developer settings** (at the bottom)
4. Click **Personal access tokens** → **Tokens (classic)**
5. Click **Generate new token** → **Generate new token (classic)**
6. You may be asked to enter your password or 2FA code

### Step 2: Configure the Token

Fill in the form:

- **Note:** `CrushLabyrinth GitHub Pages` (or any name you'll remember)
- **Expiration:** `90 days` (or choose your preference)
- **Select scopes:** Check **`repo`** (this gives full control of private repositories)
  - This will automatically check all sub-options under `repo`

### Step 3: Generate and Copy

1. Scroll down and click **Generate token** (green button at bottom)
2. **IMPORTANT:** Copy the token immediately! It looks like: `ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx`
3. **Save it somewhere safe** - you won't be able to see it again!

---

## 🚀 Push to GitHub Using the Token

Now use the token as your password:

```cmd
cd C:\Development\Android\CrushLabyrinth
git push -u origin main
```

When prompted:
- **Username:** `dimush`
- **Password:** Paste your Personal Access Token (the `ghp_xxxxx...` string)

---

## 💾 Option: Save Credentials (Recommended)

To avoid entering the token every time, use Git Credential Manager:

### Windows (Recommended):

```cmd
git config --global credential.helper wincred
```

Then push once with your token - Windows will save it for future use:

```cmd
git push -u origin main
```

### Or Use HTTPS with Token in URL (One-Time):

```cmd
git remote remove origin
git remote add origin https://dimush:YOUR_TOKEN_HERE@github.com/dimush/WebPages.git
git push -u origin main
```

Replace `YOUR_TOKEN_HERE` with your actual token.

---

## 🔐 Alternative: Use SSH (More Secure)

If you prefer SSH keys over tokens:

### Step 1: Generate SSH Key

```cmd
ssh-keygen -t ed25519 -C "your_email@example.com"
```

Press Enter 3 times (default location, no passphrase).

### Step 2: Copy Your Public Key

```cmd
type %USERPROFILE%\.ssh\id_ed25519.pub
```

Copy the entire output (starts with `ssh-ed25519`).

### Step 3: Add to GitHub

1. Go to GitHub → Settings → **SSH and GPG keys**
2. Click **New SSH key**
3. Title: `My Computer`
4. Paste the public key
5. Click **Add SSH key**

### Step 4: Change Remote URL to SSH

```cmd
git remote remove origin
git remote add origin git@github.com:dimush/WebPages.git
git push -u origin main
```

---

## 🎯 Quick Fix - Just Push Now!

**Easiest way right now:**

1. **Create token** (instructions above - takes 2 min)
2. **Copy the token**
3. **Run these commands:**

```cmd
cd C:\Development\Android\CrushLabyrinth

:: Save credentials so you only need to enter once
git config --global credential.helper wincred

:: Push (enter 'dimush' for username, paste TOKEN for password)
git push -u origin main
```

4. When prompted:
   - Username: `dimush`
   - Password: Paste your token (right-click to paste in cmd)

---

## ✅ Verification

After successful push:

1. Go to: `https://github.com/dimush/WebPages`
2. You should see your files there!
3. Now enable GitHub Pages (Settings → Pages → Select `/docs` folder)

---

## 🆘 Troubleshooting

**"Token not working"**
- Make sure you selected `repo` scope when creating
- Token must be copied exactly (no extra spaces)
- Use token as PASSWORD, not username

**"Permission denied"**
- Verify the repository exists: `https://github.com/dimush/WebPages`
- Check repository name matches exactly

**"Still asking for password"**
- Clear saved credentials: `git credential-manager-core erase`
- Try again with fresh token

---

## 📝 Token Best Practices

✅ **Do:**
- Save your token in a password manager
- Set expiration (90 days recommended)
- Create new tokens when old ones expire
- Use minimal scopes needed

❌ **Don't:**
- Share your token with anyone
- Commit tokens to your code
- Use the same token everywhere
- Leave tokens without expiration

---

**Ready?** Create your token and push again! 🚀

