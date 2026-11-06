# Kubernautic Website

Marketing website for **Kubernautic — Agentic AI for Kubernetes Operations**, part of the OpenKubes ecosystem.

## Run locally

```bash
npm install
npm run dev
```

Open http://localhost:4321. Create a production build with `npm run build`.

## GitHub Pages

Repository target: `openkubes/kubernautic-website` (public). The `main` branch builds with GitHub Actions and publishes `dist/` via Pages. In GitHub Settings → Pages, choose **GitHub Actions** as build/deployment source. Configure custom domain `kubernautic.com` and DNS according to GitHub's official documentation; enable **Enforce HTTPS** once certificate provisioning completes. `public/CNAME` is included.

**Do not point wildcard `*.kubernautic.com` DNS to GitHub Pages.** Future console and identity subdomains must point at independently hosted services.

## Launch status

- Static responsive marketing website with multiple pages.
- Console is **not yet deployed**. `/console/` is an honest coming-soon page, not a signup form or authentication service.
- Contact page links to the OpenKubes ecosystem until an approved contact address/form is available.
- Example Console content on the homepage is **illustrative**, not live telemetry.
- No analytics or tracking scripts are installed.
- Replace placeholder brand language with approved product claims and add legal/privacy pages before public launch.
- External Google Fonts are used; consider self-hosting fonts and reviewing privacy/legal requirements before launch.

## Planned next phase

Provide a separately hosted, audited read-only Console experience behind identity verification. Namespace-scoped Kubernetes RBAC alone is not a complete multi-tenant security boundary; review API proxy design, agent privileges, object visibility, logs, network access, quotas, authentication, and authorization before giving users access.
