# CloudOpex Project - Quick Command Reference

## 📂 Project Location
```
C:\Users\bkann\Desktop\CloudOpex_Project
```

## 🧪 Step 1: Test Locally
```
1. Open File Explorer
2. Navigate to: C:\Users\bkann\Desktop\CloudOpex_Project
3. Right-click index.html → Open with Browser
4. Test calculator by moving sliders
5. Form should be visible below results
```

## 🐙 Step 2: Push to GitHub

**Create repo on GitHub first:**
1. Go to https://github.com/new
2. Repo name: `cloudopex-site`
3. Make **Public**
4. Click "Create repository"

**Then run these commands in PowerShell:**

```powershell
cd C:\Users\bkann\Desktop\CloudOpex_Project

git init
git add .
git commit -m "Initial CloudOpexAdvisor landing page"

# Replace YOUR-USERNAME with your actual GitHub username
git remote add origin https://github.com/YOUR-USERNAME/cloudopex-site.git
git branch -M main
git push -u origin main

# You'll be prompted to enter your GitHub credentials
```

## 🚀 Step 3: Deploy to Netlify

**In browser:**
1. Go to https://netlify.com
2. Sign up with GitHub
3. Click "Add new site"
4. Select "Import an existing project"
5. Choose GitHub
6. Find & select `cloudopex-site`
7. Click "Deploy site"
8. Wait for green checkmark ✓

## 🌐 Step 4: Connect Custom Domain

**In Netlify:**
1. Go to: Site settings → Domain management
2. Click "Add custom domain"
3. Enter: `cloudopexadvisor.com`
4. Copy the 4 **nameservers** that appear

**In GoDaddy:**
1. Log in to godaddy.com
2. My Products → cloudopexadvisor.com
3. DNS/Manage DNS
4. Find Nameservers section
5. Replace all 4 nameservers with Netlify's
6. Save

**Verify DNS propagated:**
```powershell
ping cloudopexadvisor.com
nslookup cloudopexadvisor.com
```

Wait 5-30 minutes, then visit: https://cloudopexadvisor.com

## 📧 Step 5: Set Up Email Notifications

**In Netlify Dashboard:**
1. Your site → Forms
2. Click "lead-capture" form
3. Settings → Add notification
4. Email notification
5. Enter: `contact@cloudopexadvisor.com`
6. Save

## 🔄 Update After Deployment

After you make changes locally:

```powershell
cd C:\Users\bkann\Desktop\CloudOpex_Project

git add .
git commit -m "Your change description"
git push origin main

# Netlify auto-deploys within 30 seconds
```

## 📋 Files Included

```
CloudOpex_Project/
├── index.html          ← Complete website (HTML + CSS + JS)
├── framework.txt       ← Downloadable optimization framework
├── DEPLOYMENT.md       ← Full deployment guide
├── README.md           ← Project overview
└── COMMANDS.md         ← This file
```

## ✅ Verification Checklist

After deployment:
- [ ] https://cloudopexadvisor.com loads
- [ ] Calculator works (sliders update results)
- [ ] Form is visible
- [ ] HTTPS shows 🔒 padlock
- [ ] Mobile responsive (test on phone)
- [ ] Framework downloads when clicked

## 🆘 Troubleshooting Commands

**Check git status:**
```powershell
git status
```

**View commit history:**
```powershell
git log --oneline
```

**See current branch:**
```powershell
git branch
```

**Check if DNS is ready:**
```powershell
ping cloudopexadvisor.com
nslookup cloudopexadvisor.com
```

## 🎯 What Happens Next

1. **Visitors arrive at your site**
2. **They use the calculator** to estimate savings
3. **They enter their name + email** in the form
4. **Netlify captures the data** automatically
5. **You get an email** notifying you of the new lead
6. **You follow up manually** with personalized outreach

## 📞 Support Links

- Netlify Docs: https://docs.netlify.com/
- GitHub Help: https://docs.github.com/
- GoDaddy DNS: https://support.godaddy.com/

---

**Total time:** ~30-45 minutes from local test to live deployment
**Ready?** Start with "Test Locally" above ⬆️
