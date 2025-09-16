# Blood Bank Management System - Setup Instructions

## Issues Fixed

The authentication and role-based routing issues have been resolved. Here's what was fixed:

1. **Backend Authentication**: Added proper JWT-based authentication with registration and login endpoints
2. **Frontend Integration**: Connected registration and login forms to the backend API
3. **Role-based Routing**: Fixed AuthContext to properly handle user types and redirect to appropriate dashboards
4. **Admin Registration**: Added admin registration with access code validation
5. **API Integration**: Updated frontend to use proper API calls instead of mock data

## How to Run the Application

### Prerequisites
- Node.js (v14 or higher)
- npm

### Installation

1. **Install Frontend Dependencies**:
   ```bash
   npm install
   ```

2. **Install Backend Dependencies**:
   ```bash
   cd server
   npm install
   cd ..
   ```

### Running the Application

#### Option 1: Run Both Servers Together (Recommended)
```bash
npm run dev
```
This will start both the React frontend (port 3000) and the backend server (port 4000) simultaneously.

#### Option 2: Run Servers Separately

**Terminal 1 - Backend Server**:
```bash
npm run server
```

**Terminal 2 - Frontend Server**:
```bash
npm start
```

### Testing the Application

#### Sample Test Accounts

1. **Donor Account**:
   - Email: `donor@test.com`
   - Password: `password123`
   - User Type: Donor

2. **Hospital Account**:
   - Email: `hospital@test.com`
   - Password: `password123`
   - User Type: Hospital

3. **Admin Account**:
   - Email: `admin@test.com`
   - Password: `password123`
   - User Type: Admin

#### Admin Registration
- Use admin access code: `admin123`
- Select department from dropdown

### Features Working Now

✅ **Registration**: All user types (donor, hospital, admin) can register
✅ **Login**: Proper authentication with role-based redirection
✅ **Role-based Routing**: Users are redirected to their respective dashboards
✅ **Protected Routes**: Only authenticated users can access their dashboards
✅ **JWT Authentication**: Secure token-based authentication
✅ **Admin Access Control**: Admin registration requires access code

### API Endpoints

- `POST /api/register` - User registration
- `POST /api/login` - User login
- `GET /api/profile` - Get user profile (requires authentication)
- `GET /api/health` - Health check

### Troubleshooting

1. **CORS Issues**: The backend is configured to allow CORS from the frontend
2. **Port Conflicts**: Make sure ports 3000 and 4000 are available
3. **Authentication Issues**: Check browser console for error messages
4. **API Connection**: Ensure backend server is running on port 4000

### Next Steps for Production

1. **Database Integration**: Replace mock data with Firebase Firestore
2. **Password Hashing**: Implement proper password hashing (bcrypt)
3. **Environment Variables**: Use proper environment variables for secrets
4. **Input Validation**: Add comprehensive input validation
5. **Error Handling**: Improve error handling and user feedback
6. **Security**: Add rate limiting, input sanitization, etc.

## Testing the Complete Flow

1. Start the application: `npm run dev`
2. Open browser to `http://localhost:3000`
3. Try registering a new user or use the test accounts
4. Login with the registered/test credentials
5. Verify you're redirected to the correct dashboard based on user type
6. Test protected routes by trying to access other user type dashboards
