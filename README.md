# Healthcare Management System

A full-stack web application for managing medical appointments, doctor-patient interactions, and healthcare facility administration. Built with Angular and Node.js/Express with TypeScript.

## Overview

This healthcare management system provides a comprehensive platform for three types of users:
- **Patients (Pacijenti)**: Schedule appointments, view medical history, search for doctors
- **Doctors (Lekari)**: Manage appointments, update patient records, create medical reports
- **Managers (Menadžeri)**: Administer system, manage users, oversee facility operations

##  Architecture

### Backend
- **Framework**: Express.js with TypeScript
- **Database**: MongoDB with Mongoose ODM
- **Port**: 4000
- **API**: RESTful architecture

### Frontend
- **Framework**: Angular 14
- **Language**: TypeScript
- **Styling**: CSS
- **Port**: 4200 (default Angular dev server)

## 🚀 Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- MongoDB (v4.0 or higher)
- Angular CLI

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd programming-internet-applications
   ```

2. **Install backend dependencies**
   ```bash
   cd backend
   npm install
   ```

3. **Install frontend dependencies**
   ```bash
   cd frontend
   npm install
   ```

4. **Set up MongoDB**
   - Ensure MongoDB is running on `mongodb://127.0.0.1:27017`
   - The application will create a database named `projectDB`

### Running the Application

#### Backend

```bash
cd backend

# Build TypeScript
npm tsx

# Start the server
npm run serve
```

The backend server will start on `http://localhost:4000`

#### Frontend

```bash
cd frontend

# Start the development server
npm start

# Or explicitly
ng serve
```

The frontend will be available at `http://localhost:4200`

## 🔑 Features

### Patient Features
- User registration and authentication
- Browse and search doctors by specialization
- Schedule medical appointments
- View appointment history
- Access medical records and reports
- Update profile information

### Doctor Features
- Manage appointment schedule
- View and update patient medical records
- Create medical examination reports
- Update availability
- Manage profile and specialization information

### Manager Features
- User management (approve/reject registrations)
- Add new doctors to the system
- View system statistics
- Manage facility branches
- Password reset functionality

### Authentication & Security
- Role-based access control
- Route guards for protected pages
- User authentication system
- Password management

## 🗄️ Database Models

- **Lekar (Doctor)**: Doctor profiles with specialization, license, contact info
- **Pacijent (Patient)**: Patient profiles and medical information
- **Menadžer (Manager)**: Administrative user accounts
- **Pregled (Examination)**: Medical examination types and details
- **ZakazaniPregled (Scheduled Examination)**: Appointment records
- **Izvestaj (Report)**: Medical examination reports
- **Specijalizacija (Specialization)**: Medical specializations

## 🛠️ Technology Stack

### Backend
- **Express.js**: Web framework
- **TypeScript**: Type-safe JavaScript
- **Mongoose**: MongoDB object modeling
- **CORS**: Cross-origin resource sharing
- **Multer**: File upload handling
- **Nodemon**: Development auto-reload

### Frontend
- **Angular 14**: Frontend framework
- **TypeScript**: Type-safe JavaScript
- **RxJS**: Reactive programming
- **Angular Router**: Navigation
- **Angular Forms**: Form handling
- **HttpClient**: HTTP communication

## 📝 API Endpoints

### Authentication
- `POST /authentication/login` - User login
- `POST /authentication/register` - User registration
- `POST /authentication/reset-password` - Password reset

### Patient Routes
- `GET /pacijent/profile` - Get patient profile
- `PUT /pacijent/profile` - Update patient profile
- `GET /pacijent/appointments` - Get appointments
- `POST /pacijent/appointments` - Schedule appointment

### Doctor Routes
- `GET /lekar/profile` - Get doctor profile
- `PUT /lekar/profile` - Update doctor profile
- `GET /lekar/appointments` - Get doctor's appointments
- `GET /lekar/patients` - Get doctor's patients

### Manager Routes
- `GET /menadzer/users` - Get all users
- `POST /menadzer/doctor` - Add new doctor
- `PUT /menadzer/user` - Update user information
- `GET /menadzer/statistics` - Get system statistics

## 📦 Building for Production

### Backend
```bash
cd backend
npm run build-ts
```

### Frontend
```bash
cd frontend
npm run build
```

## 📄 License

This project is for educational purposes as part of Programming Internet Applications course.
