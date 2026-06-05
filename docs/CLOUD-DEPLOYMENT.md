# 🚀 Cloud Deployment Guide - Step by Step

## Prerequisites
- GitHub account (you have this ✅)
- 10 minutes
- Free accounts on: Vercel, Railway, MongoDB Atlas

---

## 📋 **Part 1: Create Free Accounts**

### **1A. Vercel Account (Frontend Hosting)**
1. Go to https://vercel.com/signup
2. Click "Continue with GitHub"
3. Authorize Vercel
4. Done! ✅

### **1B. Railway Account (Backend Hosting)**
1. Go to https://railway.app
2. Click "Login"
3. Click "Login with GitHub"
4. Authorize Railway
5. Done! ✅

### **1C. MongoDB Atlas (Free Database)**
1. Go to https://www.mongodb.com/cloud/atlas/register
2. Sign up with email or GitHub
3. Create free account
4. Done! ✅

---

## 🔗 **Part 2: Deploy Frontend (Vercel)**

### **Step 1: Connect GitHub Repo**
1. Go to https://vercel.com/new
2. Click "Continue with GitHub"
3. Find and select `arch-ai` repository
4. Click "Import"

### **Step 2: Configure Project**
- **Framework Preset:** Next.js ✅ (auto-detected)
- **Root Directory:** `frontend` ← **IMPORTANT: Change this**
- **Environment Variables:** (keep empty for now)

### **Step 3: Deploy**
- Click "Deploy"
- Wait 3-5 minutes
- You'll see: **"Congratulations! Your site is live"**

### **Step 4: Get Your Frontend URL**
- Copy the URL (looks like: `https://arch-ai-beta.vercel.app`)
- Save it for later ⭐

---

## 🔗 **Part 3: Create MongoDB Database**

### **Step 1: Create Cluster**
1. Go to https://www.mongodb.com/cloud/atlas
2. Click "Create a Deployment"
3. Choose **Free Tier** (M0 Sandbox)
4. Select your region (closest to you)
5. Click "Create Deployment"

### **Step 2: Create User**
1. In "Security" → "Database Access"
2. Click "Add New Database User"
3. **Username:** `admin`
4. **Password:** (create strong password) → **SAVE THIS** ⭐
5. Click "Add User"

### **Step 3: Allow Network Access**
1. Go to "Security" → "Network Access"
2. Click "Add IP Address"
3. Click "Allow Access from Anywhere"
4. Click "Confirm"

### **Step 4: Get Connection String**
1. Go back to "Databases"
2. Click your cluster → "Connect"
3. Choose "Drivers"
4. Copy connection string (looks like):
   ```
   mongodb+srv://admin:PASSWORD@cluster.mongodb.net/?retryWrites=true&w=majority
   ```
5. **Replace `PASSWORD` with your password** ⭐

---

## 🔗 **Part 4: Deploy Backend (Railway)**

### **Step 1: Create New Project**
1. Go to https://railway.app/dashboard
2. Click "New Project"
3. Click "Deploy from GitHub repo"
4. Select `arch-ai` repository

### **Step 2: Configure Backend**
1. After importing, Railway auto-detects the repo
2. Set **Root Directory:** `backend` ← **IMPORTANT**
3. Click "Deploy"

### **Step 3: Add Environment Variables**
1. In Railway dashboard, click your project
2. Click "backend" service
3. Go to "Variables" tab
4. Add these variables:

```
NODE_ENV=production
PORT=5000
MONGODB_URI=mongodb+srv://admin:YOUR_PASSWORD@YOUR_CLUSTER.mongodb.net/arch-ai?retryWrites=true&w=majority
HUGGING_FACE_API_KEY=hf_xxxxxxxxxxxx
FRONTEND_URL=https://your-vercel-url.vercel.app
```

*Replace with your actual values from previous steps*

### **Step 4: Get Backend URL**
1. In Railway, click "backend" service
2. Look for "Domain" section
3. Copy the URL (looks like: `https://arch-ai-backend.up.railway.app`)
4. Save it ⭐

### **Step 5: Deploy**
1. Click "Deploy" button
2. Wait for green checkmark
3. Takes 5-10 minutes

---

## 🔗 **Part 5: Update Frontend Environment Variables**

### **Step 1: Go to Vercel Dashboard**
1. Go to https://vercel.com/dashboard
2. Select `arch-ai` project

### **Step 2: Add Environment Variable**
1. Click "Settings"
2. Go to "Environment Variables"
3. Add new variable:
   - **Name:** `NEXT_PUBLIC_API_URL`
   - **Value:** `https://your-railway-backend-url.up.railway.app`
   - Click "Add"

### **Step 3: Redeploy Frontend**
1. Go to "Deployments"
2. Find latest deployment
3. Click "..." → "Redeploy"
4. Click "Redeploy" again
5. Wait 2-3 minutes

---

## ✅ **Final Step: Test Your Live App**

### **Open in Safari:**
```
https://your-vercel-url.vercel.app/generate
```

You should see:
- ✅ Homepage loads
- ✅ "Start Designing" button works
- ✅ Can enter prompts
- ✅ Can generate designs

### **Troubleshooting Live App:**
1. **Frontend loads but API fails:** Check `NEXT_PUBLIC_API_URL` in Vercel
2. **Backend not responding:** Check Railway environment variables
3. **Database errors:** Verify MongoDB connection string

---

## 📝 **Quick Reference**

| Service | URL | Purpose |
|---------|-----|---------|
| Vercel | https://vercel.com | Frontend hosting |
| Railway | https://railway.app | Backend hosting |
| MongoDB | https://www.mongodb.com/cloud/atlas | Database |
| Your App | `https://YOUR-VERCEL-URL/generate` | **Use this in Safari!** |

---

## 🎉 **You're Done!**

Your app is now live! Share the Vercel URL with anyone:

```
https://your-vercel-url.vercel.app/generate
```

They can use it in Safari (or any browser) without any setup! 🚀

---

## 💡 **Pro Tips**

- **Auto-deploy:** Every push to `main` automatically deploys
- **View logs:** Check Railway/Vercel dashboards for errors
- **Free tier limits:**
  - Vercel: 100 deployments/month (plenty)
  - Railway: $5 free credit/month (more than enough)
  - MongoDB: 512MB storage (enough for testing)

---

**Questions? Let me know!** 💪
