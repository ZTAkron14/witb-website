# WITB Website

Minimum viable company website for WITB, LLC.

This site is intentionally simple:

- Static HTML, CSS, and vanilla JavaScript
- No framework
- No build process
- GitHub Pages compatible
- Custom domain prepared for `witbsports.com`

## Pages

- Home: `index.html`
- Products: `products.html`
- Contact: `contact.html`

## Company

WITB, LLC develops premium software focused on sports education and sports intelligence.

Products currently shown:

- WITB Sports Academy
- WITB Sports Intelligence

Both products are listed as currently in development.

## Contact Email

The public contact email is currently:

`winningsportsintel@gmail.com`

Update the email in `contact.html` if the final company address changes.

## GitHub Pages Deployment

1. Create a GitHub repository named `witb-website`.
2. Push this repository to GitHub.
3. In GitHub, open repository Settings.
4. Go to Pages.
5. Set the source to deploy from the main branch root.
6. Confirm GitHub Pages publishes the site.
7. Confirm the custom domain is set to `witbsports.com`.

The `CNAME` file is already included and contains:

`witbsports.com`

## Cloudflare DNS

In Cloudflare, configure DNS for `witbsports.com` to point to GitHub Pages.

Recommended records:

```text
Type    Name    Value
A       @       185.199.108.153
A       @       185.199.109.153
A       @       185.199.110.153
A       @       185.199.111.153
CNAME   www     <your-github-username>.github.io
```

Optional IPv6 records:

```text
Type    Name    Value
AAAA    @       2606:50c0:8000::153
AAAA    @       2606:50c0:8001::153
AAAA    @       2606:50c0:8002::153
AAAA    @       2606:50c0:8003::153
```

Cloudflare settings:

- SSL/TLS mode: Full
- Always Use HTTPS: On
- Proxy status: DNS only during initial GitHub Pages verification if needed

After GitHub verifies the domain, Cloudflare proxying can be reviewed.

Reference: GitHub's current Pages custom domain documentation lists these apex-domain `A` and optional `AAAA` records and recommends avoiding wildcard DNS records.

## Validation Checklist

- Open `index.html`
- Open `products.html`
- Open `contact.html`
- Confirm navigation works on desktop width
- Confirm menu toggle works on mobile width
- Confirm images load
- Confirm email link opens `mailto:winningsportsintel@gmail.com`
- Confirm `robots.txt` and `sitemap.xml` are present
