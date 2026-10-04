# Custom Domain Setup — GitHub Pages

Use this after the GitHub Pages site is already live on the default `github.io` URL.

## Recommended naming approach

For a personal executive portfolio, a short name-based domain is preferable.

Examples:

- `tamtran.me`
- `tamtran.co`
- `phoebietran.com`
- `tranngocnhantam.com`

Check availability before deciding.

## Recommended setup

Use both:

- apex domain: `example.com`
- `www` subdomain: `www.example.com`

GitHub recommends configuring the `www` variant alongside the apex domain.

## Step 1 — Verify your domain in GitHub

In GitHub account settings, verify the domain before attaching it to the Pages site when possible.

This reduces the risk of domain takeover.

## Step 2 — Add the custom domain to GitHub Pages

Repository:

**Settings → Pages → Custom domain**

Enter the domain and save it.

When publishing from a branch, GitHub normally creates a `CNAME` file in the repository source automatically.

## Step 3 — DNS records

### If using an apex domain

Create A records for `@` pointing to:

```text
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

Optional IPv6 AAAA records:

```text
2606:50c0:8000::153
2606:50c0:8001::153
2606:50c0:8002::153
2606:50c0:8003::153
```

### If using `www`

Create a CNAME:

```text
Host/Name: www
Target: YOUR-GITHUB-USERNAME.github.io
```

Do **not** append the repository name to the CNAME target.

## Step 4 — HTTPS

After DNS is recognized, enable:

**Settings → Pages → Enforce HTTPS**

DNS propagation can take time.

## Step 5 — Put the final URL in the CV

Preferred CV format:

```text
Portfolio: https://www.example.com
```

Use the same URL on LinkedIn and in the email signature for consistent personal branding.
