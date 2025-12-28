# CloudOpexAdvisor Landing Page

Professional B2B SaaS landing page for cloud cost optimization consultation.

## 📁 Files

- **index.html** - Complete single-page website (HTML + CSS + JavaScript)
- **framework.txt** - 5-Step OPEX Optimization Framework
- **DEPLOYMENT.md** - Step-by-step deployment instructions

## 🎯 Features

✅ Interactive Cloud Savings Calculator
- Input: Monthly cloud spend ($1k - $100k slider)
- Input: Compute percentage (0-100% slider)
- Output: Annual savings range with conservative & aggressive estimates
- Live calculations update as sliders move

✅ Lead Capture Form
- Collects: Name + Work Email
- Netlify form integration (auto-captures submissions)
- Success message with CTA buttons

✅ Responsive Design
- Mobile, tablet, and desktop optimized
- Professional B2B aesthetic
- Deep blue (#1a4d8c) + Action green (#4caf50) color scheme

✅ Production Ready
- SSL/HTTPS support
- Netlify forms integration
- PDF framework download
- Call-to-action buttons

## 🚀 Quick Start

1. **Test locally:**
   ```
   Right-click index.html → Open with Browser
   ```

2. **Deploy to web:**
   - Follow `DEPLOYMENT.md` instructions
   - Takes 30-45 minutes end-to-end

3. **Launch at:**
   - cloudopexadvisor.com (your custom domain)

## 📊 Calculator Logic

```
1. Get monthly cloud spend and compute percentage from sliders
2. Compute spend = (Monthly Spend × Compute % ÷ 100)
3. Conservative savings = (Compute Spend × 0.15 × 12 months)
4. Aggressive savings = (Compute Spend × 0.30 × 12 months)
5. Display range to user
```

Example:
- Monthly spend: $10,000
- Compute %: 50%
- Compute spend: $5,000
- Conservative: $5,000 × 0.15 × 12 = $9,000/year
- Aggressive: $5,000 × 0.30 × 12 = $18,000/year

## 🔧 Customization

Edit these sections in `index.html`:

**Colors:**
```css
:root {
    --primary-blue: #1a4d8c;
    --action-green: #4caf50;
}
```

**Contact email:**
Search for `contact@cloudopexadvisor.com` and replace

**Hero text:**
Search for "Stop Overpaying for Cloud" and update

**Calculator ranges:**
Find `min="1000" max="100000"` and adjust values

## 📧 Lead Management

Leads are automatically captured via Netlify Forms:
1. User fills form → Data sent to Netlify
2. You receive email notification
3. View all leads in Netlify dashboard
4. Export as CSV for follow-up

## ✨ Design Highlights

- Clean, modern aesthetic
- High contrast for readability
- Smooth animations and transitions
- Mobile-first responsive design
- Accessibility-friendly (proper semantic HTML)
- Fast load times (single HTML file, no dependencies)

## 🌐 Deployment Platforms

Recommended: **Netlify** (easiest)
- Automatic deploys from GitHub
- Free SSL certificates
- Form submissions captured
- Custom domain support
- Fast CDN

Alternative: Vercel, GitHub Pages, or any static host

## 📞 Support

For questions about deployment, see `DEPLOYMENT.md`

---

**Created for:** CloudOpexAdvisor - Cloud Cost Optimization Consulting
**License:** © 2025 CloudOpexAdvisor. All rights reserved.
