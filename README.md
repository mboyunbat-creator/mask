# SOOUL — mask.mn

Static Mongolian skincare shop MVP. No build step is required.

## Publish with GitHub Pages

1. Create a **public** GitHub repository named `mask-mn` (or another name you prefer).
2. Upload all files in this directory to the repository root.
3. In **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
4. In Pages custom domain, enter `mask.mn` and save. The root `CNAME` file is included.
5. At the `mask.mn` registrar, set these apex DNS records for GitHub Pages:

   ```text
   A     @     185.199.108.153
   A     @     185.199.109.153
   A     @     185.199.110.153
   A     @     185.199.111.153
   CNAME www   <YOUR-GITHUB-USERNAME>.github.io
   ```

   Replace `<YOUR-GITHUB-USERNAME>` with the account that owns the repository. Remove conflicting A/AAAA records, wait for DNS to propagate, then enable **Enforce HTTPS** in Pages settings.

## Before accepting real orders

This is a browser-only demo: product edits, cart, and orders are stored in that browser's local storage. Orders are not sent to a server and the demo admin password is visible in the client code. Do not accept real payments or rely on it for fulfillment until server-side authentication, a shared database/API, validated checkout, and a real payment provider are connected. The visible QPay option is a placeholder.

Product photos are loaded from Unsplash at runtime and Google Fonts are loaded remotely.
