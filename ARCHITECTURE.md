# Arc Forge Revenue Sprint - Architecture

**Purpose**: Service offerings, pricing strategy, sales processes
**Lifecycle**: Living (update as strategy evolves)
**Last Updated**: 2025-11-20

---

## Service Architecture

### Three-Track Revenue Model

```
┌─────────────────────────────────────────────────────────┐
│                   REVENUE GENERATION                     │
├─────────────────────────────────────────────────────────┤
│                                                          │
│  Track 1: Freelance Platforms (Days → Weeks)            │
│  ┌──────────────────────────────────────────┐           │
│  │ Upwork/Freelancer.com                    │           │
│  │ - DevOps jobs                            │           │
│  │ - Python automation                      │           │
│  │ - Infrastructure setup                   │           │
│  │ Rate: $80-100/hour                       │           │
│  │ Target: $500-1000/gig                    │           │
│  └──────────────────────────────────────────┘           │
│                                                          │
│  Track 2: Local B2B (1-4 Weeks)                         │
│  ┌──────────────────────────────────────────┐           │
│  │ Direct outreach to trades businesses     │           │
│  │ - Custom quoting systems                 │           │
│  │ - Job management apps                    │           │
│  │ - Process automation                     │           │
│  │ Price: $2,500-5,000/project              │           │
│  │ Target: 1 client/month                   │           │
│  └──────────────────────────────────────────┘           │
│                                                          │
│  Track 3: Productized Service (2-4 Weeks)               │
│  ┌──────────────────────────────────────────┐           │
│  │ Self-Hosted Business Cloud in a Box      │           │
│  │ - Nextcloud, Vaultwarden, n8n, VPN       │           │
│  │ - Setup: $1,800                          │           │
│  │ - Support: $150/month                    │           │
│  │ Target: 2-3 clients/month                │           │
│  └──────────────────────────────────────────┘           │
│                                                          │
└─────────────────────────────────────────────────────────┘
```

---

## Service Offerings (Detailed)

### 1. Infrastructure Setup - $1,500

**What's included:**
- VPS provisioning (Digital Ocean or AWS)
- Server hardening and security setup
- Docker containerization for services
- Reverse proxy configuration (Caddy/Nginx)
- SSL/TLS certificates (automatic renewal)
- Basic monitoring and alerting
- CI/CD pipeline setup (GitHub Actions)
- 1 month support (email + async chat)

**Timeline**: 1-2 weeks
**Support**: 4 hours/month included (email response <24h)

**Tech stack delivered:**
- Ubuntu 24.04 LTS server
- Docker + Docker Compose
- Caddy reverse proxy
- Monitoring (built-in or external)

---

### 2. Custom Business Applications - $3,000-8,000

**Scope tiers:**

**Tier 1 - Simple ($3,000-4,000):**
- Single-purpose app (quoting, invoicing, inventory)
- Mobile-responsive web interface
- Offline-first PWA capability
- Basic reporting
- 2-3 weeks delivery

**Tier 2 - Standard ($4,000-6,000):**
- Multi-module application
- User authentication and roles
- API integrations (1-2 services)
- Advanced reporting
- 3-4 weeks delivery

**Tier 3 - Complex ($6,000-8,000):**
- Full business management system
- Multiple user roles and permissions
- Complex workflows and automation
- API integrations (3+ services)
- Custom reporting dashboards
- 4-6 weeks delivery

**What's included (all tiers):**
- Requirements gathering (2-3 meetings)
- Full-stack development
- Testing and QA
- Deployment to production
- User training (2 hours)
- Documentation
- 2 months support

**Tech stack:**
- Frontend: React + TypeScript + Tailwind CSS
- Backend: Node.js/Python + PostgreSQL/SQLite
- Hosting: Customer's infrastructure or managed hosting (+$50-150/month)

---

### 3. Self-Hosted Business Cloud - $1,800 + $150/month

**The "Google Workspace Alternative" package**

**Setup ($1,800 one-time):**
- Digital Ocean droplet provisioning (Sydney region)
- Nextcloud 31+ (file sync, calendar, contacts, tasks)
- Vaultwarden (Bitwarden-compatible password manager)
- n8n (workflow automation - Zapier alternative)
- Headscale (VPN mesh network)
- Automatic HTTPS + monitoring
- Desktop client setup (Windows/Mac/Linux)
- Mobile app configuration (Android/iOS)
- 2 hours training
- Full documentation

**Monthly support ($150/month):**
- Software updates and security patches
- Monitoring and uptime (99% target)
- Backup verification (weekly)
- Priority support (email response <4 hours business days)
- 1 hour/month consulting for automation workflows

**Timeline**: 1-2 weeks setup
**Target customers**: 5-20 employee businesses wanting data sovereignty

**Infrastructure:**
- VPS: $24-48/month (4-8GB RAM depending on users)
- Backups: $5-10/month (DigitalOcean Spaces or Backblaze B2)
- Domain: Customer provides or $15/year

---

### 4. Automation Consulting - $150/hour

**Scope:**
- Process analysis and bottleneck identification
- Automation opportunity mapping
- Custom script development (Python, Bash, JavaScript)
- API integration development
- n8n workflow creation
- Documentation and handover

**Minimum engagement:** 4 hours ($600)
**Typical projects:** 8-20 hours ($1,200-3,000)

**Common use cases:**
- Automate data entry from emails/PDFs
- Sync data between multiple systems
- Generate reports from multiple sources
- Automate invoice generation and sending
- Social media posting automation
- Document generation workflows

---

## Pricing Strategy

### Rationale

**Infrastructure Setup ($1,500):**
- Market rate: $2,000-3,000
- Positioning: Entry-level to build trust
- Upsell path: Monthly support or custom apps

**Custom Apps ($3,000-8,000):**
- Market rate: $5,000-15,000
- Positioning: Mid-market, quality over cheap
- 2-4 week delivery = $750-2,000/week effective rate

**Cloud in a Box ($1,800 + $150/mo):**
- Competitor: Google Workspace $12/user/month (5 users = $60/month)
- Value prop: Data ownership, no per-user fees, more features
- ROI: 12-month payback, then $150/month pure profit

**Consulting ($150/hour):**
- Market rate: $100-250/hour for DevOps/automation
- Positioning: Premium but accessible

---

## Sales Process

### Track 1: Freelance Platforms

**Profile optimization:**
- Title: "DevOps & Business Automation Specialist | Sydney, Australia"
- Rate: $80-100/hour (competitive for AU market)
- Portfolio: Link to GitHub projects (do-vps-prod, embark-quoting-system)

**Bidding strategy:**
- Volume: 10 bids/week minimum
- Target jobs: <5 proposals (less competition)
- Response time: <2 hours (shows urgency)
- Proposal template: Problem → Solution → Timeline → Price

**Job types to target:**
- VPS/server setup and migration
- Docker containerization
- CI/CD pipeline setup
- Python automation scripts
- API integration development
- Infrastructure as Code (Terraform)

**Conversion goal:** 10% bid-to-conversation, 30% conversation-to-hire

---

### Track 2: Local B2B Outreach

**Target industries:**
1. Landscaping & earthworks (proven with Embark)
2. Plumbing & electrical
3. Construction & trades
4. Field service businesses (HVAC, pest control)
5. Professional services (accounting, legal - later)

**Prospecting sources:**
- Google Maps: "landscaping [suburb]", "plumber [suburb]"
- LinkedIn: Business owners in target industries
- Industry associations: MBA, HIA
- Local business directories
- Facebook groups: Australian small business

**Outreach script (email):**

```
Subject: Custom quoting system for [Industry] businesses

Hi [Name],

I'm Samuel from Arc Forge. I build custom software for Australian
trades businesses.

Recently built an offline-first quoting system for a landscaping
company that lets them quote jobs on-site without internet connection.
Cut their quote turnaround from 2 days to 20 minutes.

Quick question: Are you currently using paper quotes, Excel spreadsheets,
or generic tools that don't quite fit your workflow?

I'd love to show you how custom software could save 5-10 hours/week
and improve your quote-to-close rate.

Would you have 15 minutes this week for a quick call?

Cheers,
Samuel
Arc Forge
arcforge.au
```

**Call script:**

```
Hi [Name], Samuel from Arc Forge calling about business automation.

[If receptionist]: I sent [Name] an email about custom quoting systems
for [industry] businesses. Is [he/she] available?

[When connected]:
Thanks for taking my call. I'll be quick - I build custom software
for trades businesses. Recently built a quoting system for a landscaping
company that cut their quote turnaround from 2 days to 20 minutes.

Quick question: How are you currently handling quotes? Excel? Paper?
Some generic tool?

[Listen for pain points]

[If interested]: Great! I'd love to show you what's possible. Can we
schedule 30 minutes this week to discuss your workflow?

[If not now]: No worries! Can I send you some info and follow up in
a month when you're less busy?
```

**Conversion funnel:**
- 20 outreach → 5 responses (25%)
- 5 responses → 2 meetings (40%)
- 2 meetings → 1 proposal (50%)
- 1 proposal → 0.5 closed (50%)
- **Net: 40 outreach → 1 client**

---

### Track 3: Productized Service

**Marketing channels:**

**arcforge.au website:**
- Landing page with service description
- Case study: "How we saved $500/month vs Google Workspace"
- Pricing calculator (# of users → recommended plan)
- Book consultation form

**Reddit (r/selfhosted):**
- Post case study: "Self-hosted business cloud setup guide"
- Offer paid setup service in comments
- Build credibility through helpful responses

**LinkedIn:**
- Weekly posts about data sovereignty, cloud costs, automation
- Target: Australian business owners, CTOs
- Content themes: Cost savings, privacy, customization

**Australian business forums:**
- Whirlpool business forums
- Small business subreddits (r/smallbusiness, r/entrepreneur)
- Industry-specific Facebook groups

**SEO keywords:**
- "self-hosted cloud Australia"
- "Google Workspace alternative"
- "business cloud setup Sydney"
- "nextcloud setup service"

---

## Tech Stack (Proven Capabilities)

### Infrastructure
- **Cloud providers**: Digital Ocean, AWS
- **IaC**: Terraform
- **Containers**: Docker, Docker Compose
- **Reverse proxy**: Caddy, Nginx
- **VPN**: Headscale, Tailscale
- **Monitoring**: Built-in DO monitoring, Uptime Kuma

### Development
- **Frontend**: React, TypeScript, Tailwind CSS
- **Backend**: Node.js, Python (FastAPI/Flask)
- **Database**: PostgreSQL, SQLite
- **APIs**: RESTful, GraphQL
- **Real-time**: WebSockets, Server-Sent Events

### Automation
- **Workflow engines**: n8n (self-hosted Zapier)
- **Scripting**: Python, Bash, JavaScript
- **CI/CD**: GitHub Actions
- **Integrations**: Xero API, Firebase, various webhooks

### AI/LLM
- **Frameworks**: Claude Agent SDK
- **Protocols**: MCP (Model Context Protocol)
- **Use cases**: Conversational interfaces, document processing

---

## Portfolio Projects (Reference)

### 1. Production VPS Infrastructure (do-vps-prod)
- **What**: Self-hosted cloud infrastructure
- **Tech**: Terraform, Docker, Caddy, Nextcloud, Vaultwarden, n8n, Headscale
- **Cost**: $43/month (vs $200+ for equivalent SaaS)
- **Uptime**: 99.5%+ (real production use)
- **Use case**: Demonstrates "Cloud in a Box" offering

### 2. Embark Quoting System
- **What**: Offline-first PWA for landscaping quotes
- **Tech**: React, TypeScript, Firebase, Terraform
- **Features**: Offline operation, real-time sync, mobile-optimized
- **Status**: 60-70% complete (can demo core functionality)
- **Use case**: Example custom business application

### 3. Xero Agent (zero-agent)
- **What**: AI-powered accounting assistant
- **Tech**: Claude Agent SDK, MCP, Firebase, React PWA
- **Features**: Natural language Xero interaction, invoice management
- **Status**: Architecture complete, needs deployment
- **Use case**: Demonstrates AI integration capabilities

---

## ADR (Architecture Decision Records)

### ADR-001: Services-First Revenue Model
**Date**: 2025-11-20
**Status**: Accepted

**Context**:
Need $250/week profit within 4 weeks. Current strategy (building products)
has 3-6 month timeline to revenue. Must pivot to immediate cash generation.

**Decision**:
Pause all product development. Sell services using existing proven skills:
- DevOps/infrastructure setup
- Custom business application development
- Productized self-hosted cloud offering
- Automation consulting

**Consequences:**
✅ Faster time to revenue (weeks vs months)
✅ Validates market demand with real customers
✅ Builds cash reserves to fund future product development
✅ Creates portfolio of completed work
✅ Recurring revenue potential (support contracts)

❌ Lower margins than successful products (services cap at hourly rate)
❌ Time-for-money model (limited scalability initially)
❌ Must delay product vision (design-forge, agents)

**Alternatives Considered:**
- Continue product development → Rejected (too slow, no revenue guarantee)
- Seek employment → Rejected (defeats business purpose, option if sprint fails)
- Raise funding → Rejected (no traction to pitch, dilutive)

---

### ADR-002: Three-Track Parallel Execution
**Date**: 2025-11-20
**Status**: Accepted

**Context**:
Single-track approach risks 4-week timeline if that channel fails. Need
multiple simultaneous paths to revenue to maximize success probability.

**Decision**:
Execute three revenue tracks in parallel:
1. Freelance platforms (fastest, lowest ticket)
2. Local B2B outreach (medium speed, medium ticket)
3. Productized service (slower, recurring revenue)

**Consequences:**
✅ Multiple chances to hit revenue target
✅ Diversified risk across channels
✅ Learn which channel works best for scaling
✅ Some channels feed others (freelance → portfolio → B2B)

❌ Divided attention across three efforts
❌ Potential context switching overhead
❌ Need to track multiple metrics

**Alternatives Considered:**
- Focus only on freelance → Rejected (low ticket size, competitive)
- Focus only on B2B → Rejected (longer sales cycle risk)
- Focus only on productized → Rejected (unproven offer, slow ramp)

---

### ADR-003: arcforge.au Single-Page Launch
**Date**: 2025-11-20
**Status**: Accepted

**Context**:
Need web presence but can't spend week building elaborate site. Must
balance speed (launch this week) with credibility (professional appearance).

**Decision**:
Launch single-page arcforge.au site on Cloudflare Pages (free):
- Services list with pricing
- Portfolio section (3 projects)
- Contact form
- Deploy in <4 hours

**Consequences:**
✅ Web presence THIS WEEK (critical for credibility)
✅ Zero hosting cost (free Cloudflare Pages)
✅ Professional domain (arcforge.au already owned)
✅ Can iterate and improve while live

❌ Basic design (not elaborate)
❌ Limited SEO (single page)
❌ No blog/content marketing initially

**Alternatives Considered:**
- Full multi-page site → Rejected (takes days, not critical for sprint)
- No website → Rejected (unprofessional, kills B2B credibility)
- WordPress → Rejected (overkill, maintenance overhead)

---

## What Worked (Living Section)

*This section will be updated as we learn what drives revenue*

### Successful Tactics
- TBD (update after Week 1)

### Failed Experiments
- TBD (update after Week 1)

### Key Learnings
- TBD (update weekly)

---

## Scaling Strategy (Post-Sprint)

**Once $250/week is stable for 4 weeks:**

1. **Hire VA/contractor** for outreach (Upwork/Fiverr, $10-20/hour)
2. **Systemize sales** (templates, CRM, automated follow-ups)
3. **Increase pricing** (10-20% once portfolio grows)
4. **Add team member** (junior dev, split revenue)
5. **Resume product development** (with cash reserves)

**Revenue targets:**
- Month 2: $500/week
- Month 3: $1,000/week
- Month 6: $2,000/week
- Month 12: $4,000/week + launch first product

---

**Last Updated**: November 20, 2025
