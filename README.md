Football Stats Tracker
![image](https://github.com/user-attachments/assets/cc79badc-5b5e-4d71-93ee-a85786425259)

Overview

A comprehensive football statistics tracking web application with Firebase backend integration. This tool allows coaches, team managers, or fans to track player performance, match results, and team rankings.

Features
Player Management: Add, edit, and track player statistics

Match Tracking: Record matches with dates and player participation

Rankings System: View top scorers from recent matches

Password Protection: Secure admin mode for editing data

Real-time Updates: Changes sync instantly across all devices

Responsive Design: Works on desktop and mobile devices

Technologies Used
Frontend: HTML5, CSS3, JavaScript

Backend: Firebase Firestore (NoSQL database)

Authentication: Client-side password protection

Deployment: Compatible with GitHub Pages, Firebase Hosting, etc.

Setup Instructions
Prerequisites
Firebase project with Firestore database

Web hosting (GitHub Pages, Firebase Hosting, etc.)

Installation
Set up Firebase:

Create a Firebase project at firebase.google.com

Enable Firestore database

Update the Firebase configuration in the code with your project's details

Configure Security Rules:

javascript
Copy
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /footballData/stats {
      allow read, write: if true; // For testing - tighten for production
    }
  }
}
Deploy the Application:

Upload all files to your web hosting provider

For GitHub Pages, simply push to your repository's gh-pages branch

Set Admin Password:

The default password is "admin123"

Change it by modifying the ADMIN_PASSWORD constant in the JavaScript code

Usage Guide
Basic Navigation
Players Tab: View and manage player roster

Matches Tab: Record and view match history

Rankings Tab: See top performers

Admin Features
Click "Enter Edit Mode" and enter the admin password

In edit mode you can:

Add new players

Edit player goals

Delete players

Add matches

Add players to matches

Delete matches

Adding Players to Matches
Navigate to Matches tab

Click "Add Player" on a match

Start typing a player's name to see matching options

Select a player and enter goals scored

Click "Add Player" to confirm

Customization Options
Team Name: Change the title in the sidebar

Password: Modify the ADMIN_PASSWORD constant

Color Scheme: Edit the CSS variables

Data Fields: Add additional statistics by modifying the player/match objects

Troubleshooting
Issue: Changes not saving

Verify your Firebase configuration is correct

Check browser console for errors

Ensure Firestore security rules allow writes

Issue: Autocomplete not working

Verify players exist in the database

Check for JavaScript errors in console

License
This project is open source and available under the MIT License.

Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your improvements.

Contact
For questions or support, please contact [Your Email/Contact Info]
