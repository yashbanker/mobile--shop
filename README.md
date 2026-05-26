# 📱 Mobile Shop Live Stock Catalog

A beautiful, professional, **auto-updating** mobile phone stock catalog website that syncs with Google Sheets in real-time. Built for mobile shop owners who want to share their live stock with customers via WhatsApp.

![Status](https://img.shields.io/badge/status-active-success)
![License](https://img.shields.io/badge/license-MIT-blue)
![No Backend](https://img.shields.io/badge/backend-none-orange)
![Hosting](https://img.shields.io/badge/hosting-GitHub_Pages-black)

---

## ✨ Features

- 🔄 **Auto-updates from Google Sheets** — edit your sheet, website refreshes automatically
- 🖼️ **Real phone images** — automatically matched for iPhone, Samsung, Google Pixel, Apple Watch, AirPods
- 🔍 **Smart search & filters** — by brand, color, storage, price range
- 📂 **Category tabs** — iPhone, Samsung, Pixel, Apple Watch, AirPods, iPad, MacBook
- 💬 **WhatsApp integration** — every "Buy" button opens pre-filled WhatsApp message
- ❤️ **Wishlist** — customers save phones and send all at once via WhatsApp
- 📱 **Fully responsive** — perfect on mobile, tablet, desktop
- 🎨 **Premium dark UI** — purple-pink gradient design, smooth animations
- ⚡ **Zero backend** — pure HTML/JS, hosted free on GitHub Pages
- 🚀 **Auto-deployment** — push to GitHub, site updates automatically

---

## 🚀 Quick Start (15 minutes)

### Step 1 — Create Your Google Sheet

1. Go to [sheets.google.com](https://sheets.google.com) → click **Blank**
2. Name it **"Mobile Stock"**
3. Rename Sheet1 → **STOCK** (right-click tab → Rename)
4. Open the included [`stock_template.csv`](stock_template.csv) file
5. In Google Sheets: **File → Import → Upload** → drop the CSV → **"Replace current sheet"** → Import
6. Your stock is now in Google Sheets ✅

### Step 2 — Publish Sheet as CSV

1. Click **Share** (top-right) → **"Anyone with the link" → Viewer** → **Done**
2. **File → Share → Publish to web**
3. Choose **STOCK** sheet + **Comma-separated values (.csv)**
4. Click **Publish** → copy the URL (ends with `/pub?output=csv`)

**Alternative URL format (always works):**
```
https://docs.google.com/spreadsheets/d/YOUR_SHEET_ID/export?format=csv&gid=0
```
Replace `YOUR_SHEET_ID` with the long ID between `/d/` and `/edit` in your sheet URL.

### Step 3 — Configure Your Shop Info

Open `index.html` in any text editor. Near line 430, find this block:

```js
const CONFIG = {
  SHOP_NAME:    "Mobile Hub",                       // Your shop name
  SHOP_TAGLINE: "Premium Phones at Best Prices",    // Tagline
  SHOP_PHONE:   "919999999999",                     // WhatsApp (country code + number, no +)
  SHOP_LOCATION:"Your City, India",                 // Location
  GOOGLE_SHEET_CSV_URL: "",                         // ← PASTE YOUR CSV URL HERE
  AUTO_REFRESH_MINUTES: 10                          // Auto-refresh interval
};
```

Update all 5 values, then save the file.

### Step 4 — Deploy to GitHub Pages (Free Forever)

1. **Create a GitHub account** at [github.com](https://github.com) (if you don't have one)
2. **Create a new repository**:
   - Click **➕** (top right) → **New repository**
   - Repository name: `mobile-shop` (or anything you like)
   - ✅ Public
   - ❌ Don't initialize with README
   - Click **Create repository**
3. **Upload these files**:
   - On the new repo page → click **"uploading an existing file"**
   - Drag ALL files from this folder into the upload area
   - Click **Commit changes**
4. **Enable GitHub Pages**:
   - Go to **Settings** tab → **Pages** (left sidebar)
   - Source: **Deploy from a branch**
   - Branch: **main** → Folder: **/ (root)** → **Save**
   - Wait 1-2 minutes
5. Your live URL appears: **`https://YOUR-USERNAME.github.io/mobile-shop/`** 🎉

### Step 5 — Share With Customers!

Send the URL via WhatsApp to your customers:
> *"Check our live stock here: https://yourusername.github.io/mobile-shop/"*

---

## 📋 Daily Workflow

Every day, you just do **ONE thing**:

1. Open your **Google Sheet** (phone or laptop)
2. Add new phones / update prices / remove sold ones
3. ✅ Done! Your website auto-updates within 10 minutes

**No re-uploading. No code changes. No re-deployment.**

---

## 🔄 How to Update the Website Code

When you want to change the design, add features, or fix bugs:

### Option A — Edit directly on GitHub (Easiest)
1. Open your repo on GitHub
2. Click `index.html` → click **✏️ pencil icon** (top right)
3. Make your changes → scroll down → **Commit changes**
4. GitHub Pages **auto-deploys** within 30 seconds! 🚀

### Option B — Clone and edit locally
```bash
git clone https://github.com/YOUR-USERNAME/mobile-shop.git
cd mobile-shop
# Edit files in any code editor (VS Code recommended)
git add .
git commit -m "Updated design"
git push
```

Auto-deployment via GitHub Actions handles the rest!

---

## 📁 Project Structure

```
mobile-shop/
├── index.html                  # Main website (all-in-one file)
├── stock_template.csv          # Pre-filled sample stock data
├── README.md                   # This file
├── LICENSE                     # MIT License
├── .gitignore                  # Git ignore rules
├── .github/
│   └── workflows/
│       └── deploy.yml          # Auto-deployment to GitHub Pages
├── assets/
│   └── README.md               # How to add logo/images
└── docs/
    ├── SETUP.md                # Detailed setup guide
    ├── CUSTOMIZATION.md        # How to customize design
    ├── TROUBLESHOOTING.md      # Common issues & fixes
    └── WHATSAPP-AUTOMATION.md  # Future WhatsApp Business setup
```

---

## ➕ Adding New Phones to Your Stock

Just add a row to your Google Sheet under the right section:

| S NO. | BRAND | MODEL | COLOUR | GB | CONDITION | BATTREY | CYCLE | WARRANTY | PRICE |
|-------|-------|-------|--------|----|-----------|---------|-------|----------|-------|
| O-501 | APPLE | 17PRO MAX SIM+ESIM | BLACK | 256 | 1 | 1 | 5 | 1 YEAR | 130000 |

- **To remove a sold phone**: delete that row
- **To change a price**: edit the PRICE cell
- **To add a new section** (iPad, MacBook): add a row with just the section name, then a header row, then your products

---

## 🎨 Customization

See **[docs/CUSTOMIZATION.md](docs/CUSTOMIZATION.md)** for:
- Changing colors and theme
- Adding your shop logo
- Modifying fonts
- Adding new product categories
- Customizing WhatsApp message templates

---

## 🐛 Troubleshooting

See **[docs/TROUBLESHOOTING.md](docs/TROUBLESHOOTING.md)** for common issues like:
- "Couldn't load stock" error
- Phone images not showing
- Google Sheet URL not working
- Filters not working correctly

---

## 🤖 WhatsApp Business Automation (Future)

For full chatbot automation (auto-reply, payment links, order tracking), see **[docs/WHATSAPP-AUTOMATION.md](docs/WHATSAPP-AUTOMATION.md)**.

Recommended providers:
- **AiSensy** (₹999/month) — Indian, easy setup
- **Wati** (~$49/month) — Global, popular
- **Interakt** (₹999/month) — Indian, Shopify-style

---

## 📜 License

MIT License — free to use, modify, and distribute. See [LICENSE](LICENSE) for details.

---

## 🙏 Credits

- Built with vanilla HTML/CSS/JS (no frameworks needed)
- Icons: [Font Awesome](https://fontawesome.com/)
- CSV parsing: [PapaParse](https://www.papaparse.com/)
- Fonts: [Inter](https://fonts.google.com/specimen/Inter) & [Plus Jakarta Sans](https://fonts.google.com/specimen/Plus+Jakarta+Sans)
- Hosted on: [GitHub Pages](https://pages.github.com/)

---

## 💡 Support

Found a bug or need a feature? Open an **[Issue](../../issues)** on GitHub.

**Happy selling! 📱✨**
