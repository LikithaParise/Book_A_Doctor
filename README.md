# 📅 Book A Doctor - Healthcare Appointment Management System

![Project Status](https://img.shields.io/badge/Status-Completed-success)
![Tech Stack](https://img.shields.io/badge/Stack-MEAN-blue)
![License](https://img.shields.io/badge/License-MIT-green)

## 📋 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [System Architecture](#system-architecture)
- [Installation & Setup](#installation--setup)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [API Endpoints](#api-endpoints)
- [Database Schema](#database-schema)
- [Screenshots](#screenshots)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## 🌟 Overview

**Book A Doctor** is a comprehensive healthcare appointment management system that revolutionizes the way patients connect with medical services. Built using the MEAN stack (MongoDB, Express.js, Angular, Node.js), this application provides a seamless, user-friendly platform for scheduling medical appointments, managing patient records, and facilitating doctor-patient communication.

### 🎯 Problem Statement
Traditional appointment booking systems are often time-consuming, inefficient, and prone to errors. Patients face long wait times, phone call hassles, and lack of real-time appointment availability information.

### 💡 Solution
A modern web application that enables:
- **Instant appointment booking** with real-time availability
- **Seamless integration** with existing healthcare systems
- **Enhanced communication** between patients and healthcare providers
- **Efficient workflow management** for medical staff

---

## ✨ Features

### For Patients 👥
- ✅ **User Registration & Authentication** - Secure login/signup system
- 📅 **Easy Appointment Booking** - Book appointments with preferred doctors
- 🕒 **View Appointment History** - Track all past and upcoming appointments
- ❌ **Cancel Appointments** - Flexible cancellation options
- 💊 **Doctor Prescriptions** - Access and download medical prescriptions
- 🔔 **Real-time Notifications** - Get updates on appointment status
- 👨‍⚕️ **Doctor Profiles** - View doctor specializations and availability

### For Administrators 🔐
- 📊 **Admin Dashboard** - Comprehensive overview of system activities
- ✅ **Approve/Reject Appointments** - Manage appointment requests
- 👨‍⚕️ **Doctor Management** - Add, update, or remove doctor profiles
- 📈 **Analytics & Reports** - Track system usage and performance
- 👥 **User Management** - Manage patient accounts
- ⚙️ **System Configuration** - Customize settings and preferences

### For Doctors 🩺
- 📋 **View Assigned Appointments** - See all scheduled appointments
- 📝 **Create Prescriptions** - Generate digital prescriptions for patients
- 👤 **Patient History** - Access patient medical records
- ⏰ **Manage Availability** - Set working hours and schedule

---

## 🛠️ Technology Stack

### Frontend
- **Angular** (v12+) - Dynamic single-page application framework
- **TypeScript** - Type-safe JavaScript
- **HTML5 & CSS3** - Modern markup and styling
- **Bootstrap** - Responsive UI components
- **RxJS** - Reactive programming library

### Backend
- **Node.js** (v14+) - JavaScript runtime environment
- **Express.js** (v4+) - Web application framework
- **JWT** - JSON Web Tokens for authentication
- **Bcrypt** - Password hashing and security

### Database
- **MongoDB** (v4+) - NoSQL document database
- **Mongoose** - ODM (Object Data Modeling) library

### Development Tools
- **npm** - Package manager
- **Nodemon** - Auto-restart development server
- **Git** - Version control system

---

## 🏗️ System Architecture

```
┌─────────────────────────────────────────────────────────┐
│                     Client (Browser)                     │
│                    Angular Frontend                      │
└──────────────────────┬──────────────────────────────────┘
                       │ HTTP/HTTPS
                       ▼
┌─────────────────────────────────────────────────────────┐
│                   Express.js Server                      │
│                   RESTful API Layer                      │
│  ┌─────────────────────────────────────────────────┐   │
│  │  • Authentication Middleware                     │   │
│  │  • Route Handlers                               │   │
│  │  • Business Logic                               │   │
│  │  • Error Handling                               │   │
│  └─────────────────────────────────────────────────┘   │
└──────────────────────┬──────────────────────────────────┘
                       │ Mongoose ODM
                       ▼
┌─────────────────────────────────────────────────────────┐
│                    MongoDB Database                      │
│  ┌─────────────────────────────────────────────────┐   │
│  │  Collections:                                    │   │
│  │  • Users (Patients, Doctors, Admins)           │   │
│  │  • Appointments                                 │   │
│  │  • Prescriptions                                │   │
│  │  • Medical Records                              │   │
│  └─────────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────┘
```

---

## 📦 Installation & Setup

### Prerequisites
Ensure you have the following installed:
- Node.js (v14 or higher)
- npm (v6 or higher)
- MongoDB (v4 or higher)
- Angular CLI (v12 or higher)

### Step 1: Clone the Repository
```bash
git clone https://github.com/yourusername/book-a-doctor.git
cd book-a-doctor
```

### Step 2: Setup Backend (Server)
```bash
# Navigate to server directory
cd server

# Install dependencies
npm install

# Create .env file
touch .env

# Add environment variables to .env
# PORT=5000
# MONGODB_URI=mongodb://localhost:27017/book-a-doctor
# JWT_SECRET=your_secret_key_here
# JWT_EXPIRE=7d

# Start the server
npm run dev
```

The server will run on `http://localhost:5000`

### Step 3: Setup Frontend (Client)
```bash
# Open new terminal and navigate to client directory
cd client

# Install dependencies (use --force if there are peer dependency conflicts)
npm install --force

# Start the Angular development server
npm start
```

The client will run on `http://localhost:4200`

### Step 4: Setup Database
```bash
# Start MongoDB service
mongod

# The application will automatically create necessary collections
```

---

## 🚀 Usage

### For Patients

1. **Register/Login**
   - Navigate to `http://localhost:4200`
   - Click "Register" and create a new account
   - Login with your credentials

2. **Book an Appointment**
   - Browse available doctors
   - Select preferred date and time
   - Submit appointment request
   - Wait for admin approval

3. **View Appointments**
   - Check appointment status (Pending/Approved/Rejected)
   - View appointment history
   - Access doctor prescriptions

4. **Cancel Appointments**
   - Navigate to appointment history
   - Click "Cancel" on desired appointment

### For Administrators

1. **Login as Admin**
   - Use admin credentials to access admin panel
   - View dashboard with system statistics

2. **Manage Appointments**
   - Review pending appointment requests
   - Approve or reject appointments with reasons
   - View all appointments across the system

3. **Manage Doctors**
   - Add new doctor profiles
   - Update doctor information
   - Set doctor availability schedules

### For Doctors

1. **Login as Doctor**
   - Access doctor dashboard
   - View assigned appointments

2. **Manage Patients**
   - View patient details and history
   - Create and upload prescriptions
   - Update appointment status

---

## 📁 Project Structure

```
book-a-doctor/
│
├── client/                          # Angular Frontend
│   ├── src/
│   │   ├── app/
│   │   │   ├── components/         # Angular components
│   │   │   │   ├── home/
│   │   │   │   ├── login/
│   │   │   │   ├── register/
│   │   │   │   ├── appointments/
│   │   │   │   ├── admin-dashboard/
│   │   │   │   └── doctor-dashboard/
│   │   │   ├── services/           # API services
│   │   │   │   ├── auth.service.ts
│   │   │   │   ├── appointment.service.ts
│   │   │   │   └── doctor.service.ts
│   │   │   ├── guards/             # Route guards
│   │   │   ├── models/             # TypeScript interfaces
│   │   │   └── app.module.ts
│   │   ├── assets/                 # Images, styles
│   │   └── environments/           # Environment configs
│   ├── package.json
│   └── angular.json
│
├── server/                          # Node.js Backend
│   ├── config/
│   │   └── db.js                   # Database configuration
│   ├── controllers/                # Request handlers
│   │   ├── authController.js
│   │   ├── appointmentController.js
│   │   ├── doctorController.js
│   │   └── prescriptionController.js
│   ├── models/                     # Mongoose schemas
│   │   ├── User.js
│   │   ├── Appointment.js
│   │   ├── Doctor.js
│   │   └── Prescription.js
│   ├── routes/                     # API routes
│   │   ├── authRoutes.js
│   │   ├── appointmentRoutes.js
│   │   ├── doctorRoutes.js
│   │   └── prescriptionRoutes.js
│   ├── middleware/                 # Custom middleware
│   │   ├── auth.js
│   │   └── errorHandler.js
│   ├── utils/                      # Helper functions
│   ├── server.js                   # Entry point
│   ├── package.json
│   └── .env
│
├── docs/                           # Documentation
│   ├── API.md
│   ├── DEPLOYMENT.md
│   └── CONTRIBUTING.md
│
├── .gitignore
├── README.md
└── LICENSE
```

---

## 🔌 API Endpoints

### Authentication
```
POST   /api/auth/register          # Register new user
POST   /api/auth/login             # User login
GET    /api/auth/profile           # Get user profile
PUT    /api/auth/update-profile    # Update profile
```

### Appointments
```
POST   /api/appointments/book      # Book new appointment
GET    /api/appointments/user/:id  # Get user appointments
GET    /api/appointments/all       # Get all appointments (admin)
PUT    /api/appointments/:id       # Update appointment status
DELETE /api/appointments/:id       # Cancel appointment
```

### Doctors
```
POST   /api/doctors/add            # Add new doctor (admin)
GET    /api/doctors/all            # Get all doctors
GET    /api/doctors/:id            # Get doctor by ID
PUT    /api/doctors/:id            # Update doctor info
DELETE /api/doctors/:id            # Remove doctor (admin)
```

### Prescriptions
```
POST   /api/prescriptions/create   # Create prescription
GET    /api/prescriptions/:id      # Get prescription
GET    /api/prescriptions/patient/:id  # Get patient prescriptions
PUT    /api/prescriptions/:id      # Update prescription
```

---

## 🗄️ Database Schema

### User Schema
```javascript
{
  _id: ObjectId,
  name: String,
  email: String (unique),
  password: String (hashed),
  role: String (enum: ['patient', 'doctor', 'admin']),
  phone: String,
  address: String,
  dateOfBirth: Date,
  gender: String,
  createdAt: Date,
  updatedAt: Date
}
```

### Appointment Schema
```javascript
{
  _id: ObjectId,
  patientId: ObjectId (ref: 'User'),
  doctorId: ObjectId (ref: 'Doctor'),
  appointmentDate: Date,
  appointmentTime: String,
  status: String (enum: ['pending', 'approved', 'rejected', 'completed', 'cancelled']),
  reason: String,
  notes: String,
  rejectionReason: String,
  createdAt: Date,
  updatedAt: Date
}
```

### Doctor Schema
```javascript
{
  _id: ObjectId,
  userId: ObjectId (ref: 'User'),
  specialization: String,
  qualification: String,
  experience: Number,
  consultationFee: Number,
  availability: [{
    day: String,
    slots: [String]
  }],
  rating: Number,
  totalAppointments: Number,
  createdAt: Date,
  updatedAt: Date
}
```

### Prescription Schema
```javascript
{
  _id: ObjectId,
  appointmentId: ObjectId (ref: 'Appointment'),
  patientId: ObjectId (ref: 'User'),
  doctorId: ObjectId (ref: 'Doctor'),
  medicines: [{
    name: String,
    dosage: String,
    duration: String,
    instructions: String
  }],
  diagnosis: String,
  additionalNotes: String,
  createdAt: Date
}
```

---

## 📸 Screenshots

### Home Page
- User-friendly landing page with system overview
- Quick access to login/register

### Patient Dashboard
- View upcoming appointments
- Quick book appointment button
- Recent prescriptions

### Admin Dashboard
- System statistics
- Pending appointments queue
- Doctor management panel

### Appointment Booking
- Doctor selection with filters
- Interactive calendar for date selection
- Available time slots display

### Prescription View
- Detailed prescription information
- Download/Print options
- Medicine details with dosage

---

## 🚀 Future Enhancements

### Planned Features
- [ ] **Video Consultation** - Integrate video calling for remote consultations
- [ ] **Payment Integration** - Add payment gateway for consultation fees
- [ ] **SMS/Email Notifications** - Automated reminders for appointments
- [ ] **Medical Reports Upload** - Allow patients to upload test reports
- [ ] **Multi-language Support** - Add localization for different languages
- [ ] **Mobile Application** - Develop React Native mobile app
- [ ] **AI Chatbot** - Implement chatbot for basic queries
- [ ] **Insurance Integration** - Connect with insurance providers
- [ ] **Review & Rating System** - Allow patients to rate doctors
- [ ] **Emergency Booking** - Priority booking for emergencies

### Technical Improvements
- [ ] Implement Redis for caching
- [ ] Add comprehensive unit and integration tests
- [ ] Set up CI/CD pipeline
- [ ] Implement WebSocket for real-time updates
- [ ] Add API rate limiting
- [ ] Implement advanced security features (2FA)
- [ ] Optimize database queries with indexing
- [ ] Add logging and monitoring (Winston, Morgan)


Please ensure:
- Code follows existing style guidelines
- All tests pass
- Documentation is updated
- Commit messages are clear and descriptive



## 👤 Contact

**Your Name** - Likitha Parise

- Email: pariselikitha@gmail.com
- LinkedIn: [linkedin.com/in/likitha-parise-258b5b244](https://www.linkedin.com/in/likitha-parise-258b5b244/)
- GitHub: [@yourusername](https://github.com/LikithaParise)

**Project Link:** [https://github.com/yourusername/book-a-doctor](https://github.com/LikithaParise/book-a-doctor)

