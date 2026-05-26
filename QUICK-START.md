# ⚡ Quick Start — Upload to GitHub in 5 Minutes

**For shop owners who've never used GitHub before.** No coding required!

---

## 🎯 What You'll Achieve

By the end of this guide, you'll have:
- ✅ A live website (like `https://yourname.github.io/mobile-shop`)
- ✅ Auto-updates from your Google Sheet
- ✅ Free hosting forever
- ✅ Easy editing via GitHub web interface

---

## 📋 Step-by-Step

### 1️⃣ Sign Up for GitHub (2 min)

1. Go to **[github.com](https://github.com)**
2. Click **"Sign up"** (top right)
3. Choose a username (this will appear in your URL!) — e.g., `apexmobile`
4. Verify your email
5. Choose the **FREE plan**

> 💡 **Tip**: Pick a clean username — it becomes part of your shop URL. Good: `apexmobile`, `mumbaiphones`. Avoid: `john_doe_1992`.

---

### 2️⃣ Create a New Repository (1 min)

1. Click the **➕** icon at top-right → **"New repository"**
2. Fill in:
   - **Repository name**: `mobile-shop` (or any name — this also appears in URL)
   - **Description**: `My phone shop live stock catalog` (optional)
   - **Visibility**: ✅ **Public** (required for free hosting)
   - ❌ **DO NOT** check "Add a README file"
   - ❌ **DO NOT** add .gitignore or license
3. Click the green **"Create repository"** button

You'll see an empty repository page.

---

### 3️⃣ Upload All Files (2 min)

1. On the empty repo page, look for this text:
   > "...or **uploading an existing file**"
   
   Click **"uploading an existing file"** (blue link)

2. **Open the folder** containing all your project files on your computer

3. **Select all files** in the folder:
   - Windows: Click first file → press `Ctrl+A`
   - Mac: Click first file → press `Cmd+A`

4. **Drag and drop** the selected files into the GitHub upload area

5. **Important**: Make sure these files/folders are uploaded:
   ```
   ✅ index.html
   ✅ stock_template.csv
   ✅ README.md
   ✅ LICENSE
   ✅ .gitignore
   ✅ CHANGELOG.md
   ✅ CONTRIBUTING.md
   ✅ QUICK-START.md
   ✅ .github/ (folder)
   ✅ assets/ (folder)
   ✅ docs/ (folder)
   ```

6. Scroll down → click **"Commit changes"** button

⏳ Wait a few seconds for upload to complete.

---

### 4️⃣ Enable GitHub Pages (1 min)

1. In your repo, click the **"Settings"** tab (top menu, far right)
2. In the left sidebar, scroll down and click **"Pages"**
3. Under **"Build and deployment"**:
   - **Source**: Choose **"Deploy from a branch"**
   - **Branch**: Select `main` → Folder: `/ (root)` → click **"Save"**
4. Wait 1-2 minutes for the green message:
   > ✅ **Your site is live at https://YOUR-USERNAME.github.io/mobile-shop/**

---

### 5️⃣ Configure Your Shop Details

Now edit `index.html` to add your info:

**On GitHub directly (no software needed!):**

1. Go to your repo → click **`index.html`**
2. Click the **✏️ pencil icon** (top-right of the file)
3. Press **`Ctrl+F`** (or `Cmd+F` on Mac) → search for: `CONFIG = {`
4. You'll find this block:
   ```js
   const CONFIG = {
     SHOP_NAME:    "Mobile Hub",
     SHOP_TAGLINE: "Premium Phones at Best Prices",
     SHOP_PHONE:   "919999999999",
     SHOP_LOCATION:"Your City, India",
     GOOGLE_SHEET_CSV_URL: "",
     AUTO_REFRESH_MINUTES: 10
   };
   ```
5. **Edit each line** (keep quotes!):
   - `SHOP_NAME`: Your shop name
   - `SHOP_TAGLINE`: Your tagline
   - `SHOP_PHONE`: Your WhatsApp (e.g., `"919876543210"` for India)
   - `SHOP_LOCATION`: Your city
   - `GOOGLE_SHEET_CSV_URL`: Paste your Google Sheets CSV URL (from `docs/SETUP.md`)

6. Scroll to the bottom → click **"Commit changes"** → click **"Commit changes"** again

**🎉 Done!** Your website auto-redeploys in 30-60 seconds with your new settings.

---

## 🔁 How to Update Anything Later

Want to change shop name, fix a typo, update colors, or anything else?

1. Go to your repo on GitHub
2. Click the file you want to edit
3. Click the ✏️ pencil icon
4. Make changes
5. Click **"Commit changes"**
6. Wait 30 seconds — site auto-updates ✅

**That's it!** No need to re-upload, re-deploy, or do anything manual.

---

## 📱 Share Your Website

Your shop is now live at:
```
https://YOUR-USERNAME.github.io/mobile-shop/
```

**Share via:**
- WhatsApp status
- Instagram bio link
- Facebook page
- Google My Business
- Printed QR code in your physical shop
- Email signature

---

## ❓ Common Questions

**Q: Can I use a custom domain like `mystore.com`?**
A: Yes! GitHub Pages supports custom domains for free. See [GitHub's guide](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

**Q: Will GitHub charge me?**
A: No. Public repositories + GitHub Pages = 100% free, forever.

**Q: How do I see my changes immediately?**
A: After committing, wait 30-60 seconds, then **hard refresh** your browser:
- Windows: `Ctrl + Shift + R`
- Mac: `Cmd + Shift + R`

**Q: I made a mistake. Can I undo?**
A: Yes! GitHub keeps full version history.
- Go to the file → click **"History"** → revert to a previous version

**Q: Is my code/data secret?**
A: No — public repos are visible to everyone. BUT:
- ✅ Your Google Sheet **data** is fetched live (not stored in code)
- ✅ Pricing/stock is in Google Sheets, not the repo
- ❌ Don't put passwords or secrets in the code

**Q: Can multiple people manage the shop?**
A: Yes! Add collaborators: Settings → Collaborators → Add people

---

## 🆘 Stuck?

- Read [docs/TROUBLESHOOTING.md](docs/TROUBLESHOOTING.md) for common issues
- Open an [Issue](../../issues) on GitHub
- Watch a GitHub tutorial on YouTube: search "GitHub Pages tutorial"

---

**Congratulations! You now have a professional, auto-updating e-commerce website. 🎊**
