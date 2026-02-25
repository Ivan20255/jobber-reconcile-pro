# Jobber Reconcile Pro - Setup Instructions

## Features
- ✅ Google Sign-In
- ✅ Phone Number Sign-In  
- ✅ User accounts with cloud data storage
- ✅ Data persists across devices
- ✅ Works on GitHub Pages and Replit

## Firebase Setup (REQUIRED)

1. Go to https://console.firebase.google.com/
2. Create a new project
3. Enable Authentication:
   - Go to Authentication → Sign-in method
   - Enable "Google" provider
   - Enable "Phone" provider
4. Get your config:
   - Go to Project Settings → General
   - Click "Add app" → Web
   - Copy the firebaseConfig object
5. Replace the config in index.html:
   ```javascript
   const firebaseConfig = {
       apiKey: "YOUR_ACTUAL_API_KEY",
       authDomain: "your-project.firebaseapp.com",
       projectId: "your-project",
       storageBucket: "your-project.appspot.com",
       messagingSenderId: "123456789",
       appId: "1:123456789:web:abc123"
   };
   ```

## Deploy to GitHub Pages

1. Fork/clone this repo
2. Replace Firebase config in index.html
3. Push to GitHub
4. Enable GitHub Pages in repo settings

## Deploy to Replit

1. Import from GitHub
2. Replace Firebase config
3. Click Run

## Files
- index.html - Main app with authentication
- background.jpg - Background image

## Security Note
The Firebase config is public (required for client-side apps). Make sure to:
- Set up Firebase Security Rules
- Restrict API key to your domains only

## Free Tier Limits
- Firebase Auth: 50,000 users/month (free)
- Firestore: 50,000 reads/day (free)
