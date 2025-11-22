# Screenshots Guide for Portfolio

## Purpose
Capture real production screenshots from your do-vps-prod infrastructure to prove reliability and show actual working systems.

---

## Screenshots Needed (Priority Order)

### 1. Monitoring Dashboard ⭐ HIGHEST PRIORITY

**What to capture**: Digital Ocean monitoring or Uptime Kuma dashboard showing uptime

**How to take it**:
```bash
# Option A: Digital Ocean Monitoring
1. Log in to cloud.digitalocean.com
2. Navigate to your droplet
3. Click "Monitoring" tab
4. Set time range to "Last 30 days" or "Last 90 days"
5. Capture screenshot showing:
   - Uptime percentage (should show 99%+)
   - CPU/Memory graphs (stable performance)
   - Bandwidth usage

# Option B: Uptime Kuma (if installed)
1. Access your Uptime Kuma instance
2. Capture dashboard showing all services "UP" (green)
3. Show response times and uptime percentages
```

**File name**: `monitoring-dashboard.png`

**Caption for Upwork**: "99.5% uptime over 3 months - Production infrastructure monitoring"

---

### 2. Nextcloud Interface ⭐ HIGH PRIORITY

**What to capture**: Clean file sync interface showing professional setup

**How to take it**:
```bash
1. Log in to your Nextcloud instance
2. Navigate to Files view
3. Create a clean, organized folder structure if needed
4. Take screenshot showing:
   - Left sidebar (Files, Photos, etc.)
   - Main file listing area
   - File sync status icons
   - Clean, professional appearance

# Bonus: Mobile App
5. Take screenshot of Nextcloud mobile app on your phone
6. Show file sync in action
```

**Files**:
- `nextcloud-web-interface.png`
- `nextcloud-mobile-app.png` (bonus)

**Caption**: "Nextcloud file sync interface - Google Drive alternative with complete data ownership"

---

### 3. n8n Workflow Example ⭐ MEDIUM PRIORITY

**What to capture**: Sample automation workflow

**How to take it**:
```bash
1. Log in to your n8n instance
2. Create a simple demo workflow if you don't have one:
   - Trigger: Webhook or Schedule
   - Actions: HTTP Request → Send Email → Log to database
3. Make it visually clean and professional
4. Take screenshot showing:
   - Workflow canvas with connected nodes
   - Clear labeling of what it does
   - Successful execution indicator

# Sample workflow ideas:
- "Invoice generation automation"
- "Daily backup notification"
- "New customer onboarding flow"
```

**File name**: `n8n-workflow-automation.png`

**Caption**: "n8n workflow automation - Zapier alternative for business process automation"

---

### 4. CI/CD Pipeline Success ⭐ MEDIUM PRIORITY

**What to capture**: GitHub Actions successful deployment

**How to take it**:
```bash
1. Go to one of your GitHub repos (business-cloud-template, arcforge-website)
2. Navigate to "Actions" tab
3. Find a successful workflow run
4. Take screenshot showing:
   - Green checkmarks for all steps
   - Build/deploy time
   - Automated deployment success

# If no workflows yet:
5. Create a simple GitHub Action for arcforge-website
6. Push a commit to trigger it
7. Capture the success screen
```

**File name**: `cicd-pipeline-success.png`

**Caption**: "Automated CI/CD deployment with GitHub Actions - Zero-downtime deployments"

---

### 5. SSL Certificate Rating (BONUS)

**What to capture**: SSL Labs A+ rating

**How to take it**:
```bash
1. Go to: https://www.ssllabs.com/ssltest/
2. Enter your domain (arcforge.au or your VPS domain)
3. Wait for scan to complete
4. Take screenshot of A+ rating (or highest you have)
5. Show:
   - Overall rating
   - Security score
   - Certificate details
```

**File name**: `ssl-labs-rating.png`

**Caption**: "A+ SSL security rating - Professional security configuration"

---

## Screenshot Best Practices

### Technical Settings:
- **Resolution**: 1920x1080 minimum (Retina/HiDPI preferred)
- **Format**: PNG (better quality than JPG)
- **Crop**: Remove unnecessary browser chrome, focus on content
- **Redact**: Blur/redact any sensitive information:
  - Personal email addresses
  - API keys or tokens
  - Internal IP addresses
  - Real client names (use "Demo Client" or "Example Corp")

### Visual Quality:
- Clean, uncluttered interface
- Good color contrast
- No dark mode (unless very professional looking)
- Consistent styling across screenshots
- Professional folder/file names (no "test123" or "asdf")

### Linux Screenshot Tools:
```bash
# Built-in tools
gnome-screenshot        # GNOME desktop
spectacle               # KDE desktop
flameshot              # Best cross-platform option

# Install flameshot (recommended)
sudo apt install flameshot

# Usage
flameshot gui          # Interactive screenshot with annotation
```

---

## Organizing Screenshots

```bash
portfolio/screenshots/
├── monitoring-dashboard.png          # MUST HAVE
├── nextcloud-web-interface.png       # MUST HAVE
├── n8n-workflow-automation.png       # SHOULD HAVE
├── cicd-pipeline-success.png         # SHOULD HAVE
├── ssl-labs-rating.png               # NICE TO HAVE
├── nextcloud-mobile-app.png          # NICE TO HAVE
└── docker-health-checks.png          # NICE TO HAVE
```

---

## Quick Checklist

**Before taking screenshots:**
- [ ] Log in to all services (Nextcloud, n8n, DO dashboard)
- [ ] Create demo/example data if needed
- [ ] Clean up any messy interfaces
- [ ] Ensure good uptime data is visible
- [ ] Check browser is full-screen (F11)

**After taking screenshots:**
- [ ] Verify no sensitive info is visible
- [ ] Crop to focus on important content
- [ ] Check file size (<5MB per image for Upwork)
- [ ] Rename with descriptive names
- [ ] Save to portfolio/screenshots/
- [ ] Add to Upwork gallery with captions

---

## Alternative: Stock Screenshots

If you don't have access to do-vps-prod right now, you can:

1. **Create demo screenshots**:
   - Install Nextcloud locally (Docker)
   - Set up demo data
   - Take clean screenshots
   - Label as "Demo environment"

2. **Use official product screenshots**:
   - Nextcloud official demo: https://try.nextcloud.com
   - n8n demo workflows: https://n8n.io/workflows
   - Add caption: "Example deployment - actual implementation customized for client needs"

**Important**: Always disclose if using demo/stock screenshots

---

## Next Steps

1. Take monitoring dashboard screenshot FIRST (blocks Upwork upload)
2. Take Nextcloud interface screenshot
3. Upload both to Upwork gallery
4. Add remaining screenshots as time permits
5. Total time needed: 15-30 minutes

---

**Created**: 2025-11-22
**Priority**: Complete monitoring + Nextcloud screenshots TODAY
