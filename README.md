# Eveneum Solutions — Static Website

This repository contains a static, production-ready website for Eveneum Solutions.

## Files included
- index.html
- about.html
- services.html
- candidates.html
- companies.html
- contact.html
- style.css
- README.md

## Purpose
A clean, responsive, accessibility-minded static site for recruitment services (BPO/KPO, accounting, operations). Ready to push to GitHub and deploy with Azure Static Web Apps.

## Deploy steps (GitHub → Azure Static Web Apps)
1. push all files to your `eveneum-website` GitHub repository (root).
   - Ensure `index.html` is at repo root.
   - Commit message example: "Add production website files (static HTML/CSS)"
2. In Azure portal:
   - Create a new resource > Static Web App (Free or paid tier)
   - Authenticate with GitHub and select the `eveneum-website` repo and branch (main/master)
   - For app location, enter `/` (root). For API location leave blank.
   - Review and create.
3. Azure will create a GitHub Action workflow in your repo. Every commit to the selected branch will trigger a new deployment.
4. Configure custom domain (optional) and SSL in Azure Static Web Apps portal.

## Notes
- Contact forms use `mailto:` for simple submission. For production forms consider adding a lightweight form endpoint (Formspree, Netlify Forms, Azure Function).
- Images and assets can be added to an `assets/` folder and referenced from HTML.
- SEO: meta tags and JSON-LD included on index. Add page-specific structured data as needed.

If you want, I can:
- create a `workflow` file tuned for Azure Static Web Apps (CI) in `.github/workflows` (optional)
- add a small `robots.txt` and `sitemap.xml` (recommended)
