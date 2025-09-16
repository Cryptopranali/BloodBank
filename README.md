# Blood Bank Management System Frontend

A responsive, modern ReactJS frontend for a Blood Bank Management System web application. This interface serves three types of users: Donors, Hospitals, and Administrators.

## 🌐 Tech Stack

- ReactJS (v18+)
- TypeScript
- Axios for REST API calls
- React Router for routing
- React Bootstrap for styling
- React Icons for UI icons

## 🧑‍💼 User Roles & Features

### 1. Donor Interface
- Home page with donor registration/login
- Dashboard: View profile, donation history, next eligible donation date
- Donate Now: Submit donation form (units, blood group)
- Donation History: Track past donations
- Get Certificate: Download PDF certificates for donations

### 2. Hospital Interface
- Login/Register
- Dashboard: View statistics and blood availability
- Request Blood: Form to request blood units (blood group, quantity)
- View Status of Requests: Track and manage blood requests

### 3. Admin Interface
- Login page
- Admin Dashboard with comprehensive statistics
- View/Add/Update Blood Stock
- View All Donors and Donations
- View and Approve/Reject Hospital Requests
- Send Reminders to Eligible Donors

## 🎨 UI/UX Features

- Color theme: Red + White + Soft Gray (blood-related theme)
- Sidebar navigation for each user role
- Responsive components: Alerts, cards, tables, modals
- Mobile-responsive layout
- Blood type badges and status indicators

## 🚀 Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn

### Installation

1. Clone the repository
   ```
   git clone https://github.com/yourusername/blood-bank-management.git
   cd blood-bank-management
   ```

2. Install dependencies
   ```
   npm install
   # or
   yarn install
   ```

3. Start the development server
   ```
   npm start
   # or
   yarn start
   ```

4. Open [http://localhost:3000](http://localhost:3000) to view it in the browser

## 📁 Project Structure

```
src/
├── components/       # Reusable UI components
├── layouts/          # Layout components for different user roles
├── pages/            # Page components organized by user role
│   ├── admin/        # Admin pages
│   ├── donor/        # Donor pages
│   ├── hospital/     # Hospital pages
│   └── public/       # Public pages (home, login, register)
├── services/         # API services and utilities
├── App.tsx           # Main application component with routing
└── index.tsx         # Entry point
```

## 🔗 API Integration

The frontend connects to the following REST API endpoints:

- `/api/donors` - Donor management
- `/api/hospitals` - Hospital management
- `/api/requests` - Blood request management
- `/api/admin` - Admin operations
- `/api/stocks` - Blood stock management

## 📱 Responsive Design

The application is fully responsive and works on devices of all sizes:

- Desktop: Full feature set with optimal layout
- Tablet: Adapted layout with all features
- Mobile: Streamlined interface with essential features

## 🔒 Authentication

The application implements role-based authentication:

- JWT-based authentication
- Protected routes based on user roles
- Persistent login with token storage

## 🛠️ Future Enhancements

- Implement Redux for state management
- Add dark mode theme
- Integrate real-time notifications
- Add multi-language support
- Implement advanced analytics dashboard

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.