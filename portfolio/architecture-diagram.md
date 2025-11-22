# Business Cloud Infrastructure - Architecture Diagram

**Purpose**: Visual architecture diagram for Upwork portfolio showing the business-cloud-template system

**Tools to use**: Excalidraw (excalidraw.com) or Figma

---

## Diagram Layout (Text Description)

```
┌─────────────────────────────────────────────────────────────────────┐
│                                                                     │
│               SELF-HOSTED BUSINESS CLOUD                            │
│          Professional Infrastructure for Small Business             │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘
                                 │
                                 │
                                 ▼
                        ┌────────────────┐
                        │   INTERNET     │
                        │  (Public Web)  │
                        └────────┬───────┘
                                 │
                                 │ HTTPS (Port 443)
                                 │
                                 ▼
        ┌────────────────────────────────────────────────────┐
        │                                                    │
        │          CADDY REVERSE PROXY                       │
        │     Automatic HTTPS + SSL Certificates             │
        │                                                    │
        │  ✓ Auto-renewing Let's Encrypt SSL                │
        │  ✓ Rate limiting & security headers               │
        │  ✓ Automatic HTTP → HTTPS redirect                │
        │                                                    │
        └───┬────────┬────────────┬────────────┬─────────────┘
            │        │            │            │
            │        │            │            │
    ┌───────▼──┐ ┌──▼──────┐ ┌──▼──────┐ ┌──▼──────────┐
    │          │ │         │ │         │ │             │
    │NEXTCLOUD │ │VAULTWDN │ │   n8n   │ │  HEADSCALE  │
    │          │ │         │ │         │ │             │
    └──────────┘ └─────────┘ └─────────┘ └─────────────┘
         │            │           │             │
         │            │           │             │
    File Sync    Password    Workflow      VPN Mesh
    Calendar     Manager     Automation    Network
    Contacts                 (Zapier Alt)
    Tasks
         │            │           │
         │            │           │
         └────────────┴───────────┘
                      │
                      ▼
              ┌──────────────┐
              │              │
              │ POSTGRESQL   │
              │  Database    │
              │              │
              └──────┬───────┘
                     │
                     ▼
          ┌─────────────────────┐
          │                     │
          │  AUTOMATED BACKUPS  │
          │                     │
          │  Daily → DO Spaces  │
          │  7-day retention    │
          │                     │
          └─────────────────────┘


┌─────────────────────────────────────────────────────────────────┐
│                         TECH STACK                              │
├─────────────────────────────────────────────────────────────────┤
│  • Server: Digital Ocean Droplet (Sydney, 4GB RAM)             │
│  • OS: Ubuntu 24.04 LTS                                        │
│  • Container Platform: Docker + Docker Compose                 │
│  • Reverse Proxy: Caddy 2.x (automatic HTTPS)                 │
│  • Infrastructure as Code: Terraform                           │
│  • CI/CD: GitHub Actions                                       │
│  • Monitoring: Docker health checks + DO monitoring            │
│  • Backups: Digital Ocean Spaces (S3-compatible)               │
└─────────────────────────────────────────────────────────────────┘


┌─────────────────────────────────────────────────────────────────┐
│                      COST COMPARISON                            │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  TRADITIONAL SAAS STACK:          SELF-HOSTED SOLUTION:        │
│                                                                 │
│  Google Workspace    $240/mo      DO Droplet       $43/mo     │
│  1Password Business   $96/mo      Backblaze B2      $5/mo     │
│  Zapier Professional $200/mo      Domain            $1/mo     │
│  VPN Service          $48/mo                                   │
│  ────────────────────────         ──────────────────────      │
│  TOTAL:             $584/mo       TOTAL:           $49/mo     │
│                                                                 │
│  Annual: $7,008/year              Annual: $588/year            │
│                                                                 │
│              💰 SAVINGS: $6,420/year (91%)                     │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘


┌─────────────────────────────────────────────────────────────────┐
│                         FEATURES                                │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  ✓ Complete data sovereignty (your server, your data)          │
│  ✓ No per-user fees (unlimited users on flat $43/mo)          │
│  ✓ 99.5%+ uptime (production-proven)                          │
│  ✓ Mobile apps (iOS + Android)                                │
│  ✓ Desktop sync clients (Windows, Mac, Linux)                 │
│  ✓ Automated daily backups with 7-day retention               │
│  ✓ Secure remote access via VPN mesh network                  │
│  ✓ Reproducible infrastructure (Terraform)                    │
│  ✓ Auto-deploy on git push (CI/CD pipeline)                   │
│  ✓ Professional monitoring and alerting                       │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘


┌─────────────────────────────────────────────────────────────────┐
│                    DEPLOYMENT TIMELINE                          │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  Week 1: Infrastructure provisioning + base services           │
│  Week 2: Client device setup + training + handover             │
│                                                                 │
│  Total: 10-14 days to production                               │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

---

## Visual Design Instructions (for Excalidraw/Figma)

### Color Scheme:
- **Background**: White or light gray (#F8F9FA)
- **Containers**: Light blue (#E3F2FD) with darker blue borders (#1976D2)
- **Arrows**: Dark gray (#424242)
- **Text**: Dark gray (#212121)
- **Highlights**: Green for cost savings (#4CAF50)
- **Security icons**: Orange/amber for SSL (#FF9800)

### Layout:
1. **Top section**: Title banner with project name
2. **Main flow**: Vertical flow from Internet → Caddy → Services
3. **Services row**: Horizontal arrangement of 4 service boxes
4. **Database**: Centered below services
5. **Backups**: Below database with arrow connection
6. **Right sidebar**: Cost comparison box (highlighted)
7. **Bottom sections**: Tech stack + Features in two columns

### Typography:
- **Title**: 24pt bold, sans-serif
- **Service names**: 16pt bold
- **Descriptions**: 12pt regular
- **Tech stack**: 11pt monospace for tech terms

### Icons (optional):
- 🔒 SSL/HTTPS security
- 📁 File storage (Nextcloud)
- 🔑 Password vault (Vaultwarden)
- ⚙️ Automation (n8n)
- 🔐 VPN network (Headscale)
- 💾 Database (PostgreSQL)
- 💰 Cost savings callout

---

## Excalidraw Quick Start

1. Go to excalidraw.com
2. Create rectangles for each service
3. Use arrows to show data flow
4. Add text labels and descriptions
5. Group related elements
6. Add color coding (blue for services, green for cost savings)
7. Export as PNG (2x resolution for clarity)
8. Save to `/portfolio/architecture-diagram.png`

---

## Alternative: ASCII Art Version (for GitHub README)

The text diagram above can be used directly in GitHub README.md files or documentation.

---

**Created**: 2025-11-22
**Project**: arcforge-revenue-sprint
**Portfolio Asset #1**
