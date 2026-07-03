# CNAME File - Custom Domain Configuration

⚠️ **IMPORTANT**: This file is currently EMPTY and should stay empty unless you have a custom domain.

## When to Use This File

The CNAME file is **ONLY** needed if you want to use a custom domain (like `yourname.com` instead of `username.github.io`).

### If Using Default GitHub Pages URL
- **Keep this file EMPTY** (current state ✅)
- Your site will be: `https://username.github.io/Abhilash-Portfolio`
- No action needed!

### If Using a Custom Domain

1. **Add your domain to CNAME file**:
   - Open the `CNAME` file
   - Add ONLY your domain name (no http://, no www, no comments)
   - Examples of VALID content:
     ```
     example.com
     ```
     OR
     ```
     www.example.com
     ```

2. **Configure DNS Settings** with your domain provider:
   
   **Option A - Using www subdomain:**
   ```
   Type: CNAME
   Name: www
   Value: yourusername.github.io
   TTL: 3600
   ```
   
   **Option B - Using apex/root domain:**
   ```
   Type: A
   Name: @ (or leave blank)
   Value: 185.199.108.153
   
   Type: A
   Name: @ (or leave blank)
   Value: 185.199.109.153
   
   Type: A
   Name: @ (or leave blank)
   Value: 185.199.110.153
   
   Type: A
   Name: @ (or leave blank)
   Value: 185.199.111.153
   ```

3. **Enable HTTPS** in GitHub Pages settings (after DNS propagation)

## Common Mistakes

❌ **WRONG** - Don't include:
```
# This is my domain
https://example.com
www.example.com/portfolio
```

✅ **CORRECT** - Only the domain:
```
example.com
```
OR
```
www.example.com
```

## Troubleshooting

**Error: "Custom domain is not properly formatted"**
- Solution: Ensure CNAME file contains ONLY the domain name
- No comments (#), no protocols (http://), no paths (/page)
- One domain per file, no extra lines or spaces

**Domain not working?**
- Wait 24-48 hours for DNS propagation
- Verify DNS settings with `nslookup yourdomain.com`
- Check GitHub Pages settings shows your domain

## Resources

- [GitHub Custom Domains Documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)
- [Troubleshooting Custom Domains](https://docs.github.com/articles/troubleshooting-custom-domains)
- DNS Checker: https://dnschecker.org

---

**Current Status**: CNAME file is empty ✅  
**Using**: Default GitHub Pages URL  
**No custom domain configured**
