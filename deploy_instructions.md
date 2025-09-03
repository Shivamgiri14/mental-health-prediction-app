# 🚀 RENDER DEPLOYMENT GUIDE

## Step-by-Step Deployment Instructions

### STEP 1: Create GitHub Repository
1. Go to https://github.com/new
2. Repository name: `mental-health-prediction-app`
3. Description: `Mental Health Prediction using Machine Learning - Flask Web App`
4. Set to **PUBLIC** (required for free Render tier)
5. **DO NOT** check "Add a README file" (we already have one)
6. Click "Create repository"

### STEP 2: Push Code to GitHub
After creating the repo, GitHub will show you these commands. Run them in PowerShell:

```powershell
# Set the remote repository (replace YOUR_USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR_USERNAME/mental-health-prediction-app.git

# Push the code
git push -u origin main
```

### STEP 3: Deploy on Render
1. **Go to**: https://render.com
2. **Sign up/Login** (you can use your GitHub account)
3. **Click**: "New +" button → "Web Service"
4. **Connect GitHub**: Authorize Render to access your repositories
5. **Select Repository**: `mental-health-prediction-app`

### STEP 4: Configure the Web Service
Render should automatically detect our configuration, but verify these settings:

- **Name**: `mental-health-prediction` (or your choice)
- **Environment**: `Python 3`
- **Region**: Choose the closest to your users
- **Branch**: `main`
- **Build Command**: `pip install -r requirements.txt`
- **Start Command**: `gunicorn --bind 0.0.0.0:$PORT app:app`
- **Instance Type**: `Free` (for testing)

### STEP 5: Environment Variables (Optional)
No special environment variables needed for this app.

### STEP 6: Deploy!
1. Click **"Create Web Service"**
2. Render will start building your app (takes 3-5 minutes)
3. Watch the build logs for any issues
4. Once deployed, you'll get a URL like: `https://mental-health-prediction-xyz.onrender.com`

## 🎉 Your App Features

Once deployed, your app will have:
- **Home Page**: `/` or `/first`
- **Mental Health Prediction**: `/predict` (main feature)
- **Data Upload**: `/upload`
- **Data Visualization**: `/chart`
- **User Authentication**: `/login`

## 📱 Testing Your Deployment

Visit these URLs after deployment:
- Main app: `https://your-app-name.onrender.com/`
- Prediction form: `https://your-app-name.onrender.com/prediction1`

## 🔧 Troubleshooting

If you see any issues:
1. Check Render build logs
2. Ensure all files were pushed to GitHub
3. Verify requirements.txt includes all dependencies
4. Check that render.yaml is properly formatted

## 💡 Pro Tips

1. **Free Tier**: Apps sleep after 15 minutes of inactivity
2. **Custom Domain**: Available on paid plans
3. **Auto-Deploy**: Enabled by default - pushes to main branch auto-deploy
4. **Scaling**: Can upgrade instance type anytime

## 📞 Need Help?

If you encounter any issues:
1. Check the Render dashboard logs
2. Ensure your GitHub repo is public
3. Verify all required files are present:
   - app.py
   - requirements.txt
   - render.yaml
   - model.pkl
   - templates/ folder
   - static/ folder

---
**Ready to deploy? Follow the steps above and your app will be live in minutes!**
