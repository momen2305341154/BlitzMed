# BlitzMed - Emergency Medical Transport Application

## Overview

BlitzMed is a web-based emergency medical transport booking platform that connects users with ambulance services. The application provides a modern, responsive interface for booking emergency medical transport, user authentication, and administrative management of bookings. It combines a Firebase-powered frontend with a Flask backend for comprehensive service delivery.

## System Architecture

### Frontend Architecture
- **Technology Stack**: Vanilla JavaScript, HTML5, CSS3
- **UI Framework**: Custom CSS with modern design patterns
- **Authentication**: Firebase Authentication
- **Database**: Firebase Realtime Database
- **Styling**: Modern glassmorphism design with CSS custom properties
- **Icons**: Font Awesome 6.0
- **Fonts**: Google Fonts (Inter family)

### Backend Architecture
- **Framework**: Flask (Python 3.11)
- **Database**: PostgreSQL (prepared for future implementation)
- **ORM**: Flask-SQLAlchemy
- **Server**: Gunicorn WSGI server
- **Email Validation**: Email-validator library
- **Deployment**: Autoscale deployment target

## Key Components

### Frontend Components
1. **Navigation System**: Responsive navbar with hamburger menu for mobile
2. **Authentication Modal**: Login/register forms with Firebase integration
3. **Booking System**: Multi-step booking form for ambulance services
4. **Dashboard**: User and admin dashboard for managing bookings
5. **Real-time Updates**: Firebase Realtime Database integration

### Backend Components
1. **Flask Application**: Main server application (`main.py` expected)
2. **Database Models**: User and booking management (SQLAlchemy)
3. **Authentication**: Integration with Firebase Auth
4. **API Endpoints**: RESTful API for booking management

### Security Features
1. **Firebase Security Rules**: Role-based access control
2. **Admin System**: Email-based admin access control
3. **Data Validation**: Client and server-side validation
4. **HTTPS**: Secure communication protocols

## Data Flow

### User Authentication Flow
1. User registers/logs in through Firebase Auth
2. User data stored in Firebase Realtime Database
3. Admin status determined by email address matching
4. Session management handled by Firebase SDK

### Booking Flow
1. Authenticated user fills multi-step booking form
2. Booking data validated on client-side
3. Data submitted to Firebase Realtime Database
4. Real-time updates for booking status
5. Admin can manage booking status through dashboard

### Admin Dashboard Flow
1. Admin authentication verified by email
2. Access to all bookings and user data
3. Ability to update booking status
4. Analytics data access for reporting

## External Dependencies

### Frontend Dependencies
- Firebase SDK (Authentication, Realtime Database)
- Font Awesome 6.0 (Icons)
- Google Fonts (Typography)

### Backend Dependencies
- Flask 3.1.1 (Web framework)
- Flask-SQLAlchemy 3.1.1 (ORM)
- Gunicorn 23.0.0 (WSGI server)
- psycopg2-binary 2.9.10 (PostgreSQL adapter)
- email-validator 2.2.0 (Email validation)

### Infrastructure Dependencies
- Firebase (Authentication and Database)
- PostgreSQL (Database server)
- OpenSSL (Security)

## Deployment Strategy

### Development Environment
- **Platform**: Replit with Nix package management
- **Runtime**: Python 3.11 and Node.js 20
- **Database**: PostgreSQL with OpenSSL
- **Hot Reload**: Gunicorn with reload flag

### Production Deployment
- **Target**: Autoscale deployment
- **Server**: Gunicorn bound to 0.0.0.0:5000
- **Process Management**: Parallel workflow execution
- **Port Configuration**: Default port 5000 with reuse-port option

### Configuration Management
- **Environment**: Stable Nix channel (24_05)
- **Modules**: Python 3.11 and Node.js 20 modules
- **Packages**: OpenSSL and PostgreSQL system packages

## User Preferences

Preferred communication style: Simple, everyday language.

## Changelog

Changelog:
- June 25, 2025. Initial setup
- Sepetmber 20, 2025. updated
