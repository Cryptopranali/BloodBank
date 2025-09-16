# Blood Bank Management System - Setup Guide

## Quick Setup

### 1. Firebase Configuration
1. Go to [Firebase Console](https://console.firebase.google.com/)
2. Select your project: `bloodbank-5752e`
3. Go to **Firestore Database** → **Rules**
4. Replace the rules with the content from `firestore.rules` file
5. Click **Publish**

### 2. Start the Application
```bash
# Install dependencies
npm install
cd server && npm install

# Start both frontend and backend
npm run dev
```

### 3. Test Registration
1. Go to `http://localhost:3000/register`
2. Select "Admin" user type
3. Fill in the form with your details:
   - Name: Prathmesh Dayanand Dongale
   - Email: prathmeshdongale04@gmail.com
   - Password: your password
   - Phone: 08329835054
   - Address: ghotWDAE
   - Admin Code: admin123
   - Department: Blood Bank Management
4. Click Register

### 4. Verify Data in Firestore
1. Go to Firebase Console → Firestore Database
2. You should see a `users` collection
3. Your registration data will be stored there

## Features
- ✅ All data stored in Firestore
- ✅ No service account required
- ✅ Client-side authentication
- ✅ Role-based access (Donor, Hospital, Admin)
- ✅ Clean interface without dummy data

## Troubleshooting
- If registration fails, check browser console for errors
- Make sure Firestore rules allow read/write operations
- Verify Firebase project ID matches in `src/firebase.js`
