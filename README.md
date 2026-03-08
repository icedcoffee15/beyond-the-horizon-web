# Beyond The Horizon — Official Website

Landing page + signup/login + admin panel for user count tracking.

## Setup

1. **Create a GitHub repo:**
   ```bash
   git init
   git add .
   git commit -m "initial"
   git remote add origin https://github.com/YOUR_USERNAME/beyond-the-horizon-web.git
   git push -u origin main
   ```

2. **Deploy to Vercel:**
   - Go to [vercel.com](https://vercel.com)
   - Click "New Project"
   - Select "Import Git Repository"
   - Choose this repo
   - Framework: **Other** (static site)
   - Deploy

3. **After deploy:**
   - Copy the Vercel URL (e.g., `https://beyond-the-horizon.vercel.app`)
   - Update `BuildConfig.WEBSITE_URL` in `script/build_config.gd` with this URL

## Firebase Config

Make sure your Firebase config is in `public/index.html` (around line 357):

```javascript
const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_AUTH_DOMAIN",
    projectId: "YOUR_PROJECT_ID",
    // ... etc
};
```

## Admin Panel

Only emails listed in `ADMIN_EMAILS` inside `public/index.html` will see the admin panel (shows total user count).

Update the list with your email before deploying.
