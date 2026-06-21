# HI-Tech Village - Form Deployment Guide

## ✅ Local Testing

```bash
npm install
npm start
```
Visit: http://localhost:3000

---

## 🚀 Deploy to Railway.app (Recommended - Free & 24/7)

### Step 1: Prepare Your Code
```bash
git init
git add .
git commit -m "Initial commit"
```

### Step 2: Create Railway Account
1. Go to https://railway.app
2. Sign up with GitHub
3. Click "New Project"

### Step 3: Deploy from GitHub
1. Select "Deploy from GitHub"
2. Connect your GitHub repository
3. Railway will auto-detect the Node.js app
4. Click "Deploy"

### Step 4: Set Environment Variables
1. In Railway Dashboard, go to Variables
2. Add:
   ```
   PORT=3000
   NODE_ENV=production
   ADMIN_PHONE=919310575003
   ```
3. Click "Redeploy"

### Step 5: Get Your Live URL
- Once deployed, Railway provides a public URL (e.g., `https://form-production-xxxx.railway.app`)
- Share this link - it works 24/7

---

## 📱 Form Validation Rules (Updated)

✅ **Full Name**: Text only (letters & spaces)
✅ **Mobile**: Integers only (10 digits, 6-9 start)
✅ **Address**: Text with min 10 characters
✅ **Plot No.**: Integers only
✅ **Plot Area**: Numbers (decimals allowed)
✅ **Property Rate**: Integers (₹)
✅ **Advance Amount**: Integers (₹)
✅ **Payment Schedule**: Dropdown selection
✅ **Reference**: Text/numbers/hyphens

---

## 💬 WhatsApp Messages Sent

✅ **To Receiver (Admin)**: Complete registration details
✅ **To Sender (Customer)**: Confirmation receipt with transaction summary

---

## 🔒 Security Notes

- WhatsApp session is stored locally on server (persistent)
- Mobile numbers are validated server-side
- All fields are sanitized before sending
- CORS enabled for cross-origin requests

---

## 📝 Alternative Deployment Options

### Option 2: Render.com
1. Go to https://render.com
2. Create account → New → Web Service
3. Connect GitHub repo
4. Set Environment: Node
5. Build: `npm install`
6. Start: `npm start`

### Option 3: Heroku
1. Go to https://heroku.com
2. Create app
3. Connect GitHub repository
4. Enable auto-deploy

---

## ✨ Form Messaging Flow

```
User fills form → Server validates → 
→ Sends to Admin (WhatsApp) 
→ Sends to Customer (WhatsApp) 
→ Shows success message
```

---

**Questions?** Check the form validation in `index.html` and server logic in `server.js`
