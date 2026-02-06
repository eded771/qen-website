# QEN Website - Setup Guide

## 🚀 Quick Start

### Step 1: Firebase Setup
1. Go to https://console.firebase.google.com
2. Click "Add Project"
3. Name: "QEN-Network" (or anything)
4. Enable Google Analytics (optional)
5. Create project

### Step 2: Enable Authentication
1. In Firebase Console → Build → Authentication
2. Click "Get Started"
3. Enable "Google" provider
4. Add your email as authorized domain

### Step 3: Get Firebase Config
1. Go to Project Settings (gear icon)
2. Scroll down to "Your apps"
3. Click "Web" (</> icon)
4. Register app: "QEN Website"
5. Copy the `firebaseConfig` object

### Step 4: Update index.html
Open `index.html` and replace:
```javascript
const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    // ... paste your config here
};
```

### Step 5: Deploy to GitHub Pages
1. Create GitHub account (if needed)
2. Create new repository: "qen-website"
3. Upload all files from `qen-website` folder
4. Go to Settings → Pages
5. Source: Deploy from branch `main`
6. Wait 1-2 minutes

### Step 6: Connect QEN.US Domain
1. In GitHub repo Settings → Pages
2. Custom domain: `qen.us`
3. In your domain registrar (Namecheap/GoDaddy):
   - Add DNS record:
     - Type: `CNAME`
     - Name: `@` or `www`
     - Value: `YOUR-USERNAME.github.io`

### Step 7: Verify Token Domain
Once the website is live, run this Python script to connect the domain to Wallet 3:
```bash
python set_domain_wallet3.py
```

## 📂 File Structure
```
qen-website/
├── index.html (homepage with auth)
├── .well-known/
│   └── xrpl.toml (token verification)
└── README.md (this file)
```

## ✅ Checklist
- [ ] Firebase project created
- [ ] Authentication enabled
- [ ] Config updated in index.html
- [ ] GitHub repo created
- [ ] Files uploaded
- [ ] GitHub Pages enabled
- [ ] Domain connected to GitHub
- [ ] Website accessible at qen.us
- [ ] Domain set on Wallet 3

## 🆘 Need Help?
Ask me any questions!
