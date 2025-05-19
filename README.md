# NFC Relay

A tiny, static HTML “relay” page that forwards NFC tag scans to your Google Apps Script web app for inventory logging.

## 📦 What it Does

When someone scans an NFC tag programmed with a URL like:
https://<your-github-pages>.github.io/nfc-relay/?key=Second%20Skin
this page immediately grabs the `key` parameter and redirects the browser to your Apps Script:
https://script.google.com/macros/s/AKfycbx..../exec?key=Second%20Skin
That way, any staffer can tap with their phone and log the item—no special app required.

## 🚀 Quick Start

1. **Clone or create** this repo on GitHub, enable **GitHub Pages** (source = `main` branch, root).
2. **Edit** `index.html`:
   - Find the `const SCRIPT_URL = '…';` line.
   - Paste in your Apps Script “Web app” URL (the one you get after **Deploy → Manage deployments**).
3. **Publish** to GitHub Pages.  
4. **Program** your NFC tags with:
https://<your-user>.github.io/nfc-relay/?key=<Tag%20Key>
5. **Scan** with any smartphone—logs will flow into your sheet via Apps Script.

## 🛠️ File Overview

- **index.html**  
Contains the tiny JS redirector. No build tools or frameworks needed—just plain HTML/JS.

- **README.md**  
This file.

- **LICENSE**  
MIT — feel free to tweak however you like.

## ⚙️ Customization

- If you want a “tap acknowledgment” UI instead of a bare redirect, you can drop in some HTML in the `<body>` before the script runs.
- To change how long the page shows feedback before redirecting, edit the `setTimeout` in the JS.

## 🔒 License

Released under the MIT License. See [LICENSE](LICENSE) for details.

