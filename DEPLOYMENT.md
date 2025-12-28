# CloudOpex_Project Deployment Guide

## ✅ What's Ready
- `index.html` - Fully functional landing page with calculator
- `framework.txt` - 5-Step optimization framework
- All styling, JavaScript, and Netlify form integration included

## 📋 Steps to Launch (You Must Do These)

### Step 1: Test Locally (1 min)
```
1. Open File Explorer
2. Navigate to: C:\Users\bkann\Desktop\CloudOpex_Project
3. Right-click index.html → "Open with" → Browser
4. Move the sliders to verify calculations update
5. Try submitting the form (won't work yet - that's normal)
```

### Step 2: Create GitHub Repository (10 min)

**What you need:**
- GitHub account (free at github.com)

**Steps:**
1. Go to: https://github.com/new
2. Repository name: `cloudopex-site`
3. Description: "CloudOpexAdvisor landing page and lead capture"
4. Make it **Public** (required for Netlify)
5. Click "Create repository"
6. GitHub shows you commands to run

**In PowerShell:**
```powershell
cd C:\Users\bkann\Desktop\CloudOpex_Project

git init
git add .
git commit -m "Initial CloudOpexAdvisor landing page"

# Copy the commands from GitHub (they'll look like:)
git remote add origin https://github.com/YOUR-USERNAME/cloudopex-site.git
git branch -M main
git push -u origin main

# Enter your GitHub username and password when prompted
```

### Step 3: Deploy to Netlify (10 min)

**What you need:**
- GitHub account (from Step 2)

**Steps:**
1. Go to: https://netlify.com
2. Click "Sign up"
3. Click "GitHub" to sign up with GitHub
4. Authorize Netlify to access your GitHub repos
5. Click "Add new site"
6. Select "Import an existing project"
7. Choose GitHub
8. Find and select `cloudopex-site`
9. Click "Deploy site"

**Netlify will:**
- Deploy automatically
- Assign you a temporary URL (e.g., `xyz.netlify.app`)
- Show "Publish log" - wait for green checkmark

### Step 4: Connect Custom Domain (10 min)

**What you need:**
- GoDaddy account (you own cloudopexadvisor.com)
- Access to domain settings

**Steps in Netlify:**
1. Go to: Netlify Dashboard → Your Site → Domain Settings
2. Click "Add custom domain"
3. Enter: `cloudopexadvisor.com`
4. Click "Verify"
5. Netlify shows 4 **Nameservers**
6. Copy all 4 nameservers

**Steps in GoDaddy:**
1. Log in to GoDaddy.com
2. Go to "My Products"
3. Find "cloudopexadvisor.com" → Click it
4. Click "DNS" or "Manage DNS"
5. Find "Nameservers" section
6. Change from GoDaddy nameservers to Netlify's
7. Paste the 4 nameservers Netlify gave you
8. Save changes

**Wait:** 5-30 minutes for DNS to propagate
- Test with: `ping cloudopexadvisor.com` in PowerShell
- Then visit: https://cloudopexadvisor.com

### Step 5: Set Up Email Notifications (5 min)

**In Netlify Dashboard:**
1. Go to your site → Forms
2. Click "lead-capture" form
3. Click "Settings"
4. Click "Add notification"
5. Select "Email notification"
6. Enter: `contact@cloudopexadvisor.com`
7. Save

**Result:** You'll get an email every time someone fills out the form

### Step 6: Enable SSL/HTTPS (Automatic)

Netlify automatically:
- Issues free SSL certificate
- Forces HTTPS on your domain
- No action needed

---

## 🎯 Verification Checklist

After deployment, verify:
- [ ] Visit https://cloudopexadvisor.com (loads without errors)
- [ ] Calculator sliders work and update results
- [ ] Form is visible below calculator
- [ ] Submit button is clickable
- [ ] Browser shows 🔒 padlock (HTTPS enabled)
- [ ] Mobile view is responsive (open DevTools, toggle mobile)

---

## 📧 Lead Capture Workflow

**When someone submits the form:**

1. Netlify captures the data
2. You receive email notification
3. You see the lead in Netlify Forms dashboard
4. You can export all leads as CSV

**To view leads in Netlify:**
- Go to: Dashboard → Site → Forms → lead-capture
- See all submissions with timestamps and data

---

## 🔧 Customizations

If you want to make changes:

1. Edit `index.html` locally
2. Save the file
3. In PowerShell:
   ```powershell
   cd C:\Users\bkann\Desktop\CloudOpex_Project
   git add .
   git commit -m "Your change description"
   git push origin main
   ```
4. Netlify automatically redeploys (takes ~30 seconds)

**Common edits:**
- Change email: Find `contact@cloudopexadvisor.com` and replace
- Change colors: Find `:root {` in CSS and edit color hex codes
- Change calculator ranges: Find `min="1000" max="100000"` and adjust
- Change text: Search for the text you want to change

---

## ⚠️ Troubleshooting

**Domain not showing up?**
- Wait 10-30 minutes for DNS propagation
- Clear browser cache (Ctrl+Shift+Delete)
- Try incognito window

**Form not submitting?**
- Check browser DevTools (F12) for errors
- Verify `data-netlify="true"` is in the form tag
- Try submitting again

**Netlify deploy failed?**
- Check "Deploys" tab in Netlify dashboard
- Click failed deploy to see error log
- Common issue: Files not in the root directory

**Calculator not working?**
- Open DevTools (F12)
- Check Console tab for JavaScript errors
- Make sure framework.txt is in same folder as index.html

---

## 🚀 You're Ready!

**Time estimate:** 30-45 minutes total for full deployment

Next step: **Follow Step 1 above** - Test locally first!

Questions? Check the Netlify docs: https://docs.netlify.com/
