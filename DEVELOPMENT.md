# Development Guide

**Purpose**: Tools setup and sales toolkit
**Lifecycle**: Stable
**Last Updated**: 2025-11-20

---

## Overview

This project is primarily a **sales and execution sprint**, not software development. The "development" here refers to:
- Setting up sales/outreach tools
- Creating website and marketing materials
- Building the sales toolkit
- Tracking and optimization

---

## Tools Setup

### Essential Tools (Week 1)

**1. arcforge.au Website**

**Option A: Cloudflare Pages (Recommended - Free)**
```bash
# Create simple HTML site
mkdir arcforge-website
cd arcforge-website

# Create index.html (see templates/ directory)
# Single-page design with services, pricing, contact form

# Deploy to Cloudflare Pages
# - Go to pages.cloudflare.com
# - Connect GitHub repo or upload directly
# - Point arcforge.au domain
# - Free SSL included
```

**Option B: GitHub Pages (Alternative - Free)**
```bash
# Use existing GitHub account
# Create repo: arcforge-website
# Enable GitHub Pages in settings
# Point arcforge.au via CNAME
```

**Option C: Host on do-vps-prod (Existing infrastructure)**
```bash
# Use existing Caddy reverse proxy
# Create static site directory
# Configure Caddy for arcforge.au
# Already have SSL setup
```

---

**2. Upwork Profile**

**Setup steps:**
1. Go to upwork.com/signup
2. Create freelancer account
3. Complete profile:
   - Professional photo
   - Headline: "DevOps & Business Automation Specialist | Sydney, Australia"
   - Overview: 300+ words (see templates/)
   - Portfolio: Link GitHub projects
   - Skills: Add 10-15 relevant skills
   - Rate: $80-100/hour

**Profile approval**: 24-48 hours typical
**Backup**: Freelancer.com if Upwork delayed

---

**3. Lead Tracking System**

**Google Sheets Template:**

Create spreadsheet: "Arc Forge - Revenue Sprint Leads"

**Sheet 1: Leads**
```
A: Company
B: Contact Name
C: Industry
D: Phone
E: Email
F: Status (dropdown: Lead/Contacted/Engaged/Proposal/Closed/Lost)
G: Source (dropdown: Upwork/Google/LinkedIn/Referral)
H: Value ($)
I: Last Contact (date)
J: Next Action
K: Notes
```

**Sheet 2: Metrics**
```
Week 1, Week 2, Week 3, Week 4 columns
Rows: Upwork bids, Conversations, Proposals, Revenue, etc.
Auto-calculate conversion rates
```

**Alternative**: Streak CRM (Gmail plugin, free tier)

---

**4. Communication Tools**

**Email:**
- Use existing professional email
- Or set up [email protected]
- Email signature template (see templates/)

**Phone:**
- Use existing mobile
- Consider Google Voice for separate business line
- Voicemail: Professional greeting

**Calendar:**
- Google Calendar or equivalent
- Booking link: Calendly free tier (optional)
- Time blocking for outreach (Tue-Thu mornings)

---

**5. Analytics & Tracking**

**Website analytics:**
- Cloudflare Analytics (free, built-in)
- Or Google Analytics (free, privacy concerns)

**Link tracking:**
- Bitly (free tier) for tracking click rates on outreach

**Time tracking:**
- Toggl Track (free tier)
- Track time per track (Freelance/B2B/Productized)

---

## Website Templates

### index.html Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arc Forge - Business Systems Automation | Sydney, Australia</title>
    <!-- Tailwind CSS CDN or custom CSS -->
</head>
<body>
    <!-- Header -->
    <header>
        <h1>Arc Forge</h1>
        <p>Business Systems Automation | Sydney, Australia</p>
    </header>

    <!-- Hero -->
    <section id="hero">
        <h2>Automate Your Business. Increase Productivity.</h2>
        <p>We build custom software and infrastructure for Australian businesses.</p>
        <a href="#contact">Get Started</a>
    </section>

    <!-- Services -->
    <section id="services">
        <h2>Services</h2>

        <div class="service">
            <h3>Infrastructure Setup - $1,500</h3>
            <p>VPS provisioning, Docker, CI/CD, monitoring, 1 month support</p>
        </div>

        <div class="service">
            <h3>Custom Business Apps - $3,000-8,000</h3>
            <p>Quoting systems, job management, process automation</p>
        </div>

        <div class="service">
            <h3>Self-Hosted Business Cloud - $1,800 + $150/mo</h3>
            <p>Complete Google Workspace alternative with data ownership</p>
        </div>

        <div class="service">
            <h3>Automation Consulting - $150/hour</h3>
            <p>Process optimization, integrations, custom scripts</p>
        </div>
    </section>

    <!-- Portfolio -->
    <section id="portfolio">
        <h2>Portfolio</h2>

        <div class="project">
            <h3>Production VPS Infrastructure</h3>
            <p>Self-hosted cloud saving $500/month vs SaaS</p>
            <a href="https://github.com/IAMSamuelRodda/do-vps-prod">View on GitHub</a>
        </div>

        <div class="project">
            <h3>Offline-First Quoting System</h3>
            <p>PWA for field services, works without internet</p>
            <a href="https://github.com/IAMSamuelRodda/embark-quoting-system">View on GitHub</a>
        </div>

        <div class="project">
            <h3>AI-Powered Business Assistant</h3>
            <p>Xero integration with natural language interface</p>
            <a href="https://github.com/IAMSamuelRodda/zero-agent">View on GitHub</a>
        </div>
    </section>

    <!-- Contact -->
    <section id="contact">
        <h2>Get Started</h2>
        <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
            <input type="text" name="name" placeholder="Your Name" required>
            <input type="email" name="email" placeholder="Your Email" required>
            <input type="tel" name="phone" placeholder="Your Phone">
            <textarea name="message" placeholder="Tell us about your project"></textarea>
            <button type="submit">Send Message</button>
        </form>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2025 Arc Forge. ABN: [Your ABN]</p>
        <p>Sydney, Australia | [email protected]</p>
    </footer>
</body>
</html>
```

**Form backend**: Formspree.io (free tier, 50 submissions/month)

---

## Email Signature Template

```
---
Samuel Rodda
Founder | Arc Forge

Business Systems Automation
Sydney, Australia

W: arcforge.au
E: [email protected]
P: [phone]
GitHub: github.com/IAMSamuelRodda

Specialists in: Custom Business Applications | Self-Hosted Infrastructure | Workflow Automation
```

---

## Upwork Profile Template

**Headline** (max 80 chars):
```
DevOps & Business Automation Specialist | Sydney, Australia
```

**Overview** (300-500 words):
```
I help Australian businesses automate workflows, build custom applications,
and deploy secure self-hosted infrastructure.

WHAT I DO:

✓ Infrastructure Setup & DevOps
  - VPS provisioning (Digital Ocean, AWS)
  - Docker containerization
  - CI/CD pipelines (GitHub Actions)
  - Monitoring and alerting

✓ Custom Business Applications
  - Quoting and invoicing systems
  - Job management tools
  - Offline-first PWAs for field services
  - API integrations

✓ Self-Hosted Cloud Infrastructure
  - Nextcloud, Vaultwarden, n8n
  - VPN mesh networks
  - Cost-effective alternatives to Google Workspace

✓ Automation & Scripting
  - Python, Bash, JavaScript
  - Workflow automation (n8n, Zapier alternatives)
  - Data processing and reporting

TECH STACK:

- Infrastructure: Terraform, Docker, Kubernetes
- Backend: Node.js, Python, PostgreSQL
- Frontend: React, TypeScript, Tailwind CSS
- Cloud: AWS, Digital Ocean, Firebase
- Automation: n8n, GitHub Actions, custom scripts

RECENT PROJECTS:

• Built production VPS infrastructure serving 5-20 users, saving $500/month
  vs cloud alternatives (Nextcloud, Vaultwarden, VPN, automation)

• Developed offline-first PWA quoting system for landscaping company,
  reducing quote turnaround from 2 days to 20 minutes

• Created AI-powered accounting assistant with Xero API integration
  using Claude Agent SDK

WHY WORK WITH ME:

✓ Based in Sydney (AEST timezone) - excellent for Australian businesses
✓ Production experience, not just tutorials
✓ Clear communication and realistic timelines
✓ Documentation and knowledge transfer included
✓ Support after delivery

I'm particularly interested in helping trades and field service businesses
leverage technology to save time and win more business.

Let's chat about how I can help automate your workflows or build the
custom tool your business needs.
```

**Portfolio items:**
1. do-vps-prod (screenshot + description)
2. embark-quoting-system (screenshot + description)
3. zero-agent (screenshot + description)

---

## Call Script Template

**Opening:**
```
Hi [Name], this is Samuel from Arc Forge.

[If cold call]:
I specialize in building custom software for [industry] businesses here
in Australia. Do you have a quick minute?

[If follow-up]:
Following up on the email I sent about [topic]. Did you get a chance
to take a look?
```

**Discovery questions:**
```
1. How do you currently handle [quotes/invoices/job management]?
2. What's the most time-consuming part of that process?
3. Have you looked at software solutions before? What stopped you?
4. If you could wave a magic wand, what would the ideal solution look like?
5. What's your timeline for making a change?
6. What's your rough budget for solving this problem?
```

**Closing:**
```
Based on what you've shared, I think I can help. I've built similar
solutions for [similar industry] that [specific result].

Would it make sense to schedule 30 minutes next week to discuss a
specific solution for you? I can show you some examples and give you
a rough ballpark on cost and timeline.

[If yes]: Great! How's [day/time]?
[If no]: No problem. Can I send you some information and follow up
in a few weeks when timing is better?
```

---

## Git Workflow

**Initial setup:**
```bash
cd /home/x-forge/repos/arcforge-revenue-sprint
git add .
git commit -m "docs: initial project setup with 4-week revenue strategy"
git branch -m main
```

**Daily updates:**
```bash
# Update STATUS.md after completing tasks
git add STATUS.md
git commit -m "status: update Week 1 Day X progress"

# Add new leads
git add leads.md
git commit -m "leads: add 5 new prospects from research"
```

**Weekly updates:**
```bash
# End of week
git add STATUS.md CHANGELOG.md
git commit -m "status: complete Week 1 review"
git tag week-1-complete
```

**No branches needed** - this is a documentation/tracking project, not software.

---

## Automation Scripts (Optional)

### Lead Research Automation

**Google Maps scraper** (for local businesses):
```python
# pip install playwright beautifulsoup4
# Simple script to extract business listings from Google Maps
# Use ethically - respect rate limits

# See scripts/research_businesses.py (when created)
```

**LinkedIn search automation:**
```python
# Use LinkedIn Sales Navigator filters
# Export to CSV
# Import to Google Sheets lead tracker

# Manual process preferred (more authentic)
```

---

## Metrics Dashboard (Optional)

**Google Data Studio** (free):
- Connect to Google Sheets (lead tracker)
- Auto-refresh metrics dashboard
- Track conversion funnel visually
- Share-able link for accountability

**Simple alternative:**
- Google Sheets with pivot tables
- Manual update weekly
- Formulas for conversion rates

---

## Testing Checklist

### Website Pre-Launch

- [ ] All links work (no 404s)
- [ ] Contact form submits successfully
- [ ] Mobile-responsive (test on phone)
- [ ] Fast load time (<3 seconds)
- [ ] SSL certificate active (https://)
- [ ] Meta tags present (title, description)
- [ ] No typos or grammatical errors
- [ ] Portfolio links work
- [ ] Professional appearance

### Upwork Profile Pre-Submission

- [ ] No grammatical errors
- [ ] Professional photo uploaded
- [ ] All sections complete
- [ ] Portfolio items added (3+)
- [ ] Skills match job targets
- [ ] Rate is competitive ($80-100/hour)
- [ ] Overview addresses client needs (not just about you)

### Before Sending Outreach Email

- [ ] Personalized (not template obvious)
- [ ] Spell-checked
- [ ] No broken links
- [ ] Professional signature
- [ ] Clear call-to-action
- [ ] Sent from professional email
- [ ] Follow-up scheduled

---

## Troubleshooting

### Website not loading
- Check DNS propagation (can take 24-48 hours)
- Verify Cloudflare settings
- Test with different DNS (8.8.8.8)
- Check browser cache (hard refresh)

### Upwork profile rejected
- Review Upwork guidelines
- Ensure no prohibited claims
- Professional photo required
- Try Freelancer.com as backup

### No response to outreach
- Give it 3-5 days before follow-up
- Test different subject lines
- Try different time of day (Tue-Thu 9-11am best)
- Shorten message (people are busy)

### Not getting Upwork interviews
- Apply faster (within 1 hour of posting)
- Target jobs with <5 proposals
- Customize each proposal (no templates)
- Lower rate temporarily to build reviews

---

## Resources

**Website builders (if no HTML skills):**
- Carrd.co (simple one-page sites, $19/year)
- Webflow (more complex, free tier available)
- WordPress (overkill for this, but familiar)

**Form backends:**
- Formspree.io (50 submissions/month free)
- Netlify Forms (100 submissions/month free)
- Google Forms (free, less professional)

**Image assets:**
- Unsplash.com (free stock photos)
- Canva.com (design tool, free tier)
- Favicon.io (generate favicons)

**Learning resources:**
- Upwork success tips: /r/Upwork
- Cold email templates: Close.com blog
- Sales process: Predictable Revenue book

---

**Last Updated**: November 20, 2025
