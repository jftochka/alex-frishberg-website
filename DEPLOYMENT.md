# Alex Frishberg Website - Deployment Guide

## Overview

This is a static multipage website ready for deployment on any static hosting platform with custom domain support.

## Files Structure

```
alex-frishberg-site/
├── index.html          # Homepage
├── books.html          # Publications page
├── photography.html    # Photography gallery
├── art.html            # Art gallery
├── press.html          # Press & media coverage
├── about.html          # About the author
├── contact.html        # Contact page
├── styles.css          # Main stylesheet (fully responsive)
├── script.js           # JavaScript functionality
├── images/             # All website images
├── robots.txt          # SEO robots file
├── sitemap.xml         # SEO sitemap
├── netlify.toml        # Netlify configuration
├── vercel.json         # Vercel configuration
├── _headers            # Netlify/Cloudflare headers
└── _redirects          # Netlify redirects
```

## Deployment Options

### Option 1: Netlify (Recommended)

1. Go to [netlify.com](https://netlify.com) and sign up/login
2. Click "Add new site" → "Deploy manually"
3. Drag and drop the entire `alex-frishberg-site` folder
4. Once deployed, go to "Domain settings"
5. Click "Add custom domain" and enter your domain
6. Follow DNS configuration instructions

**DNS Configuration for Netlify:**
- Add a CNAME record pointing to your Netlify subdomain
- Or use Netlify DNS for automatic SSL

### Option 2: Vercel

1. Go to [vercel.com](https://vercel.com) and sign up/login
2. Click "Add New..." → "Project"
3. Upload the folder or connect to a Git repository
4. Go to "Settings" → "Domains"
5. Add your custom domain

**DNS Configuration for Vercel:**
- Add an A record: `76.76.21.21`
- Or add a CNAME record pointing to `cname.vercel-dns.com`

### Option 3: Cloudflare Pages

1. Go to [pages.cloudflare.com](https://pages.cloudflare.com)
2. Create a new project
3. Upload the folder directly
4. Add custom domain in project settings

### Option 4: GitHub Pages

1. Create a new GitHub repository
2. Upload all files to the repository
3. Go to Settings → Pages
4. Select source branch (main)
5. Add custom domain in the custom domain field

**DNS Configuration for GitHub Pages:**
- Add A records: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
- Or add a CNAME record pointing to `<username>.github.io`

## Custom Domain Setup

### General DNS Configuration

For most providers, you'll need to:

1. **For apex domain (alexfrishberg.com):**
   - Add A record(s) pointing to your hosting provider's IP
   - Or use ALIAS/ANAME if supported

2. **For www subdomain:**
   - Add CNAME record pointing to your hosting provider

### SSL/HTTPS

All recommended platforms provide free SSL certificates via Let's Encrypt. SSL is typically provisioned automatically after DNS propagation (can take up to 48 hours).

## Post-Deployment Checklist

- [ ] Verify all pages load correctly
- [ ] Test responsive design on mobile devices
- [ ] Check all images load properly
- [ ] Verify navigation works on all pages
- [ ] Test contact form functionality (if applicable)
- [ ] Submit sitemap to Google Search Console
- [ ] Set up Google Analytics (optional)

## Updating the Site

To update content:
1. Modify the HTML files locally
2. Re-upload to your hosting platform
3. Changes typically go live within minutes

## Support

For technical issues with hosting platforms, refer to their documentation:
- [Netlify Docs](https://docs.netlify.com)
- [Vercel Docs](https://vercel.com/docs)
- [Cloudflare Pages Docs](https://developers.cloudflare.com/pages)
- [GitHub Pages Docs](https://docs.github.com/pages)
