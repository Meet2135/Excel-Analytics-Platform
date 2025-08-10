# 📊 Excel Analytics Platform - MERN Stack

A comprehensive full-stack web application for uploading Excel files, analyzing data, and creating interactive visualizations with advanced chart customization capabilities. Built with the MERN stack (MongoDB, Express.js, React, Node.js) featuring secure authentication, role-based access control, and powerful data export functionality.

![Excel Analytics Platform](https://img.shields.io/badge/React-19.1.0-blue?style=for-the-badge&logo=react)
![Node.js](https://img.shields.io/badge/Node.js-18+-green?style=for-the-badge&logo=node.js)
![MongoDB](https://img.shields.io/badge/MongoDB-8.15.2-green?style=for-the-badge&logo=mongodb)
![TypeScript](https://img.shields.io/badge/TypeScript-5.8.3-blue?style=for-the-badge&logo=typescript)

---

## ✨ Key Features

### 🔐 Authentication & Security
- **JWT-based Authentication** with bcrypt password hashing
- **Role-based Access Control** (Admin/User dashboards)
- **Secure Password Reset** via modal interface
- **Session Management** with localStorage

### 📊 Data Visualization
- **Multiple Chart Types**: Bar, Line, and Pie charts using Chart.js
- **Interactive Color Customization** with real-time preview
- **Column Filtering** and Y-axis selection for targeted analysis
- **Responsive Chart Rendering** with smooth animations

### 📁 File Management
- **Excel File Upload** (.xls/.xlsx) with data preview
- **Data Parsing** using SheetJS library
- **Upload Statistics** tracking per user
- **File Validation** and error handling

### 🎨 User Experience
- **Modern Responsive UI** built with CSS3
- **Intuitive Dashboard** for both admin and regular users
- **Real-time Updates** without page refresh
- **Toast Notifications** for user feedback

### 📤 Export Capabilities
- **PNG Export** using html2canvas
- **PDF Generation** with jsPDF
- **CSV Download** with custom formatting
- **Chart Sharing** functionality

### 👨‍💼 Admin Panel
- **User Management** with CRUD operations
- **Activity Monitoring** with login timestamps
- **Upload Analytics** across all users
- **User Status Tracking** (Active/Inactive)
- **CSV Export** of user data

---

## 🛠️ Technology Stack

### Frontend
- **React 19.1.0** - UI Framework
- **TypeScript** - Type Safety
- **Vite** - Build Tool & Dev Server
- **Chart.js + react-chartjs-2** - Data Visualization
- **React Router DOM** - Navigation
- **React Toastify** - Notifications
- **Axios** - HTTP Client

### Backend
- **Node.js** - Runtime Environment
- **Express.js** - Web Framework
- **TypeScript** - Type Safety
- **MongoDB + Mongoose** - Database & ODM
- **JWT** - Authentication
- **bcryptjs** - Password Hashing
- **CORS** - Cross-Origin Resource Sharing

### Libraries & Tools
- **SheetJS (xlsx)** - Excel file parsing
- **html2canvas** - Chart to image conversion
- **jsPDF** - PDF generation
- **file-saver** - File download handling
- **react-color** - Color picker component

---

## 📋 Prerequisites

Before running this project, make sure you have the following installed:

- **Node.js** (v18 or higher)
- **npm** or **yarn** package manager
- **MongoDB** (local installation or MongoDB Atlas account)
- **Git** (for cloning the repository)

---

## 🚀 Quick Start

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/Excel-Analytics-Platform-Mern-.git
cd Excel-Analytics-Platform-Mern-
```

### 2. Backend Setup
```bash
# Navigate to backend directory
cd mern-auth-secure

# Install dependencies
npm install

# Create environment file (if .env.example exists)
# cp .env.example .env
```

### 3. Configure Environment Variables
Create a `.env` file in the `mern-auth-secure` directory:
```env
PORT=5000
MONGO_URI=mongodb://localhost:27017/excel-analytics
JWT_SECRET=your-super-secret-jwt-key-here
NODE_ENV=development
```

### 4. Start Backend Server
```bash
npm run dev
```
Backend will run on: `http://localhost:5000`

### 5. Frontend Setup
```bash
# Open new terminal and navigate to project root
cd ..

# Install frontend dependencies
npm install

# Start frontend development server
npm run dev
```
Frontend will run on: `http://localhost:5173`

---

## 📁 Project Structure

```
Excel-Analytics-Platform-Mern-/
├── src/                          # Frontend React application
│   ├── components/               # React components
│   │   ├── adminpannel/         # Admin dashboard components
│   │   ├── user-dashboard/      # User dashboard components
│   │   ├── Login.tsx           # Authentication components
│   │   └── Register.tsx
│   ├── api/                     # API integration
│   ├── context/                 # React context providers
│   └── main.tsx                # Application entry point
├── mern-auth-secure/            # Main Backend (Express + MongoDB + JWT)
│   ├── controllers/             # Route controllers
│   ├── middleware/              # Custom middleware
│   ├── models/                  # MongoDB schemas
│   ├── routes/                  # API routes
│   └── index.ts                # Server entry point
├── express-backend-jwt/         # Alternative Backend (Express + JWT only)
├── public/                      # Static assets
├── package.json                # Frontend dependencies (React + Vite)
├── vite.config.ts              # Vite configuration
└── index.html                  # HTML entry point
```

---

## 🔐 Authentication Flow

1. **Registration**: Users sign up with email and password
2. **Login**: JWT token generated and stored in localStorage
3. **Role-based Routing**: 
   - Admin users → `/adminpannel1`
   - Regular users → `/user-dashboard`
4. **Password Reset**: Modal-based reset functionality
5. **Session Management**: Automatic token validation

---

## 📊 Data Visualization Workflow

1. **File Upload**: User uploads Excel file (.xls/.xlsx)
2. **Data Parsing**: SheetJS extracts and validates data
3. **Column Selection**: User chooses relevant columns for visualization
4. **Chart Generation**: Chart.js creates interactive visualizations
5. **Customization**: Real-time color and style adjustments
6. **Export**: Download as PNG, PDF, or CSV

---

## 🧪 Testing the Application

### Default Admin Account
```
Email: admin@example.com
Password: admin123
```

### Regular User Registration
- Navigate to `/register`
- Create a new account
- Login to access user dashboard

### Alternative Backend (Optional)
If you want to use the alternative backend:
```bash
cd express-backend-jwt
npm install
npm run dev
```

---

## 📤 API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/reset-password` - Password reset

### File Management
- `POST /api/upload` - Upload Excel file
- `GET /api/upload/:userId` - Get user uploads

### User Management (Admin)
- `GET /api/users` - Get all users
- `DELETE /api/users/:id` - Delete user
- `GET /api/users/stats` - Get user statistics

---

## 🚀 Deployment

### Backend Deployment (Render/Heroku)
```bash
# Navigate to backend directory
cd mern-auth-secure

# Set environment variables in deployment platform
MONGO_URI=your-mongodb-atlas-uri
JWT_SECRET=your-jwt-secret
NODE_ENV=production
```

### Frontend Deployment (Vercel/Netlify)
```bash
# From project root directory
npm run build

# Deploy the dist folder
```

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**Rishav Kumar Singh**  
MERN Stack Developer

- 📧 Email: `rishavse06@gmail.com`
- 🔗 LinkedIn: [Your LinkedIn Profile]
- 🌐 Portfolio: [Your Portfolio Website]

---

## 🙏 Acknowledgments

- [Chart.js](https://www.chartjs.org/) for powerful charting capabilities
- [SheetJS](https://sheetjs.com/) for Excel file processing
- [React](https://reactjs.org/) for the amazing frontend framework
- [Express.js](https://expressjs.com/) for the robust backend framework

---

## 📈 Future Roadmap

- [ ] **AI-Powered Insights** - Integrate OpenAI/Gemini for chart analysis
- [ ] **Real-time Collaboration** - Multi-user chart editing
- [ ] **Advanced Analytics** - Statistical analysis and predictions
- [ ] **Mobile App** - React Native version
- [ ] **Cloud Storage** - Google Drive/Dropbox integration
- [ ] **Chart Templates** - Pre-built chart designs
- [ ] **Data Validation** - Enhanced error checking
- [ ] **Performance Optimization** - Lazy loading and caching

---

⭐ **Star this repository if you find it helpful!**

=======

