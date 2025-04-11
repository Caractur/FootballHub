# ⚽ Football Stats Tracker

![image](https://github.com/user-attachments/assets/48a1f526-54c8-4fe1-a1de-ef9b9541d1f1)


A complete web application for tracking football team statistics with real-time Firebase integration.

## ✨ Features
- 📊 Track player goals and performance
- 📅 Record matches with dates and participants
- 🏆 Auto-generated top scorers rankings
- 🔒 Password-protected admin mode
- 🔄 Real-time sync across devices

## 🚀 Quick Setup
1. Create Firebase project at [firebase.google.com](https://firebase.google.com/)
2. Replace Firebase config in code:
   
javascript
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT.firebaseapp.com",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_BUCKET.appspot.com",
  messagingSenderId: "YOUR_SENDER_ID",
  appId: "YOUR_APP_ID"
};

3. Set Firestore rules:
   
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /footballData/stats {
      allow read, write;
    }
  }
}

🔑 Default Login

Admin password: admin123
Change in code: const ADMIN_PASSWORD = "your-new-password";

🎮 Basic Usage
Add Players:

  Name + initial goals
  Edit goals later

Record Matches:

  Select date
  Add players via search dropdown
  Enter goals per player

View Rankings:

  Automatically updates
  Shows top 5 performers


📜 License
MIT License - Free for personal and commercial use


To use:
1. Copy all text above
2. Paste into a new file named `README.md`
3. Replace `screenshot.png` with your actual screenshot
4. Update the Firebase config with your project details
5. Customize any other sections as needed

The formatting will render perfectly on GitHub/GitLab and most other markdown viewers.
