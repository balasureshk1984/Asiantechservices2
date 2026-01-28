<!-- 
DEPLOYMENT GUIDE - Asiantechservices Job Portal
================================================

This file contains instructions for deploying your website to various platforms.
-->

# Deployment Guide

## Quick Start Options

### 1. LOCAL DEPLOYMENT (Fastest)
Simply open `index.html` in your browser - that's it!

**Pros**: No setup needed, works offline
**Cons**: Only accessible on your computer

---

## 2. GitHub Pages (Recommended - Free)

### Steps:
1. Create a GitHub account (https://github.com)
2. Create a new repository named `asiantechservices`
3. Click "Upload files" and upload:
   - index.html
   - styles.css
   - script.js

4. Go to Settings → Pages
5. Select "Deploy from a branch"
6. Choose "main" branch
7. Click Save

**Your site will be live at**: `https://username.github.io/asiantechservices`

---

## 3. Netlify (Free - Recommended)

### Steps:
1. Go to https://netlify.com
2. Sign up with GitHub/Google
3. Click "Add new site" → "Deploy manually"
4. Drag and drop your files
5. Wait for deployment

**Pros**: Easy setup, auto-HTTPS, form handling available
**Your site will be live in**: 30 seconds!

---

## 4. Vercel (Free)

### Steps:
1. Go to https://vercel.com
2. Sign up with GitHub
3. Import project
4. Click Deploy
5. Done!

---

## 5. Traditional Web Hosting

### Using FTP:
1. Buy hosting (GoDaddy, Bluehost, Hostinger, etc.)
2. Get FTP credentials
3. Use FileZilla or similar FTP client
4. Upload files to `public_html` folder
5. Access via your domain

### Popular Hosting Providers:
- **Hostinger** - $2.99/month
- **Bluehost** - $2.95/month
- **SiteGround** - $2.99/month
- **Namecheap** - $2.88/month

---

## 6. AWS (S3 + CloudFront)

### Steps:
1. Create AWS account
2. Create S3 bucket
3. Enable static website hosting
4. Upload files
5. Create CloudFront distribution
6. Configure domain

**Best for**: Large-scale deployments

---

## Domain Configuration

### How to Use Your Domain:

1. **Buy a domain**: GoDaddy, Namecheap, Route53
2. **Point to GitHub Pages**:
   - Add DNS records:
     - A: 185.199.108.153
     - A: 185.199.109.153
     - A: 185.199.110.153
     - A: 185.199.111.153

3. **Point to Netlify**:
   - Change nameservers to Netlify
   - Or add CNAME to your DNS

---

## Email Setup for Contact Form

### Option 1: FormSubmit.co (Free)

Update your form in index.html:
```html
<form class="contact-form" action="https://formsubmit.co/YOUR_EMAIL@example.com" method="POST">
    <input type="text" name="name" required>
    <input type="email" name="email" required>
    <textarea name="message" required></textarea>
    <button type="submit">Send</button>
</form>
```

### Option 2: Netlify Forms (Free with Netlify)

Just add `netlify` attribute:
```html
<form class="contact-form" netlify>
    ...
</form>
```

Forms will appear in Netlify dashboard!

### Option 3: Backend Email

Create a simple PHP backend:
```php
<?php
$name = $_POST['name'];
$email = $_POST['email'];
$message = $_POST['message'];

mail("info@asiantechservices.com", "New Inquiry from $name", $message);
?>
```

---

## SSL Certificate (HTTPS)

- **GitHub Pages**: Automatic ✅
- **Netlify**: Automatic ✅
- **Vercel**: Automatic ✅
- **Traditional Hosting**: Usually free with hosting

---

## Performance Optimization

1. **Compress Images**:
   - Use TinyPNG or ImageOptim
   - Save as WebP format

2. **Minify CSS/JS**:
   - Use CSS Minifier
   - Use JavaScript Minifier

3. **Enable Caching**:
   - Set browser cache headers
   - Use CDN for images

4. **Test Performance**:
   - Google PageSpeed Insights
   - GTmetrix
   - WebPageTest

---

## SEO Optimization

1. **Google Search Console**: https://search.google.com/search-console
2. **Google Analytics**: https://analytics.google.com
3. **Sitemap**: Add sitemap.xml
4. **Robots.txt**: Add robots.txt

---

## Monitoring & Maintenance

1. **Uptime Monitoring**: UptimeRobot (free)
2. **Analytics**: Google Analytics or Hotjar
3. **Backups**: Regular backups of files
4. **Updates**: Keep content current

---

## Troubleshooting

**Issue**: Images not loading
**Solution**: Check image URLs, use full HTTPS URLs

**Issue**: Form not working
**Solution**: Check email service configuration

**Issue**: Website slow
**Solution**: Compress images, enable caching

**Issue**: Mobile menu not working
**Solution**: Check JavaScript is loading

---

## Next Steps

1. Choose a deployment platform
2. Upload your files
3. Test on multiple devices
4. Set up analytics
5. Monitor and maintain

**Questions?** Email: info@asiantechservices.com
