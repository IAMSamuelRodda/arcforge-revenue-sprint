# Portfolio Assets - Quick Start Guide

## Creating Image Files for Upwork

### Option 1: Screenshot the HTML File (FASTEST)

**For cost-comparison.html:**
```bash
# Open the HTML file in your browser
firefox portfolio/cost-comparison.html
# or
google-chrome portfolio/cost-comparison.html

# Take a screenshot:
# - Linux: Use Screenshot tool or press PrtScn
# - Press F11 for fullscreen mode first (cleaner image)
# - Save as: portfolio/cost-comparison.png
```

### Option 2: Use Browser DevTools (Higher Quality)

1. Open `cost-comparison.html` in Chrome/Firefox
2. Right-click → "Inspect Element"
3. Click the device toolbar icon (mobile view toggle)
4. Set dimensions: 1200px x 800px
5. Right-click on page → "Capture screenshot"
6. Save to `portfolio/cost-comparison.png`

### Option 3: Command Line (requires wkhtmltoimage)

```bash
# Install tool
sudo apt install wkhtmltopdf

# Convert HTML to image
wkhtmltoimage --width 1200 --height 900 \
  portfolio/cost-comparison.html \
  portfolio/cost-comparison.png
```

---

## Quick Upload to Upwork

1. Go to your Upwork project setup
2. Navigate to "Gallery" section
3. Click "Upload Media"
4. Select `portfolio/cost-comparison.png`
5. Set as cover image
6. Add caption: "Self-hosted infrastructure cost savings for small business"

---

## Files Ready for Portfolio

- ✅ `architecture-diagram.md` - Architecture documentation (convert to image with Excalidraw)
- ✅ `cost-comparison.html` - Beautiful cost comparison (screenshot this!)
- 🔄 Screenshots folder - Pending: Add your do-vps-prod screenshots
- 🔄 Docker Compose gist - Pending: Create GitHub Gist
- 🔄 Case study - Pending: Create 1-page case study

---

**Priority**: Screenshot `cost-comparison.html` NOW to unblock your Upwork project!
