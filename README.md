# Event Management System

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.11%2B-blue.svg)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-%3E=2.0-green.svg)](https://flask.palletsprojects.com/)
[![MySQL](https://img.shields.io/badge/Database-MySQL-blue.svg)](https://www.mysql.com/)
[![Bootstrap](https://img.shields.io/badge/UI-Bootstrap-purple.svg)](https://getbootstrap.com/)
[![Code Quality](https://img.shields.io/badge/Code%20Quality-Polished-brightgreen.svg)]()
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-orange.svg)](CONTRIBUTING.md)

> A full-stack web application for creating, managing, and attending events with integrated user roles, ticket booking, and real-time event tracking.

---

## 🌟 Project Overview

The Event Management System is a comprehensive platform for both event organizers and attendees. Organizers can create events, manage bookings, and track statistics, while attendees can browse events, book tickets, and manage their registrations. The system features:
- Fully role-based user authentication (organizer, attendee, optional admin)
- Event creation, editing, and deletion
- Real-time ticket booking and availability tracking
- Dashboards and analytics for event performance
- Secure payment and registration flows
- Modern and responsive user interface

### Architecture & Key Components

- **Frontend**: HTML, CSS, JavaScript, Bootstrap for fast, responsive UI
- **Backend**: Python (Flask), with Flask-Login and Flask-WTF for security and forms
- **Database**: MySQL, managed via SQLAlchemy ORM
- **Authentication**: Role-based access, password hashing, session management
- **Dashboards**: Chart.js for real-time stats and analytics
- **Modular Structure**:
  ```
  EventManagementSystem/
  ├── app/
  │   ├── models.py            # ORM models for users, events, tickets, bookings
  │   ├── routes/
  │   │   ├── auth_routes.py
  │   │   ├── attendee_routes.py
  │   │   ├── organizer_routes.py
  │   │   ├── event_routes.py
  │   ├── templates/
  │   │   ├── base.html
  │   │   ├── auth/
  │   │   ├── attendee/
  │   │   ├── organizer/
  │   │   ├── admin/ (optional)
  │   ├── static/
  │       ├── css/
  │       ├── js/
  ├── migrations/
  ├── tests/
  ├── run.py
  ├── requirements.txt
  ├── README.md
  └── LICENSE
  ```

### Major Functions & Flow

**Authentication System**
- Secure registration and login for organizers/attendees
- Password hashing and session-based login with Flask-Login

**Role-Based Access**
- Decorators restrict dashboard/event management to organizers
- Attendees can register and manage their own bookings

**Event Management**
- CRUD operations for events (title, details, date/time, location, capacity, price)
- Image upload for event banners

**Ticket Booking**
- Attendees book tickets (capacity limits enforced)
- Dashboard to view/manage tickets; cancellation supported

**Dashboards**
- Organizers: track event stats, registrations, sales
- Attendees: view booked events, tickets

**Dashboard and Analytics**
- Visualize event statistics
- Track attendance and registrations
- Monitor popular event categories

**Event Listing & Filtering**
- Public event list, search, and category/date/location filters

**Optional Features**
- Downloadable tickets (PDF)
- QR code for event check-in
- Sales analytics

---

## 🚀 Installation

### Prerequisites
- Python 3.11 or higher
- MySQL (recommended: XAMPP or a standalone MySQL server)
- Modern web browser (Chrome, Firefox, Edge, etc.)

### Quick Setup

> **For detailed setup, see the [XAMPP Setup Guide for Beginners](XAMPP_SETUP_GUIDE.md).**

1. **Start MySQL database service** (via XAMPP or your preferred method)
2. **Create a database** named `event_management`
3. **Install Python dependencies**:
    ```bash
    pip install flask flask-login flask-sqlalchemy flask-wtf email-validator gunicorn mysql-connector-python werkzeug
    ```
4. **Configure the database connection** in `app.py` or `main.py`
5. **Run the application**:
    ```bash
    python main.py
    ```
6. **Open your browser** and navigate to [http://localhost:5000](http://localhost:5000)

---

## 💡 Usage Example

### Registration & Login

1. Click 'Register' on the homepage
2. Choose your user type (Organizer or Attendee)
3. Fill in the required details
4. Login using your registered email and password

### Creating Events (Organizers Only)

1. Log in as an organizer
2. Navigate to 'Create Event'
3. Enter event details (title, description, date/time, location, etc.)
4. Set event capacity and pricing
5. Submit to create your event

### Managing Events

- View all your events under 'My Events'
- Edit, delete, and track registration statistics

### Browsing & Booking (Attendees)

1. Click 'Explore Events' to view all events
2. Apply filters or search for specific events
3. Click on an event to see details
4. Register by clicking 'Get Tickets'

### Managing Tickets

- View registered events under 'My Tickets'
- See event details, ticket status
- Cancel tickets for events you cannot attend

---

## Quick Start Guide

For first-time users, we've provided a comprehensive guide to set up the application using XAMPP. Please see the [XAMPP Setup Guide for Beginners](XAMPP_SETUP_GUIDE.md) for detailed instructions.

### Prerequisites

- Python 3.11 or higher
- XAMPP (for beginners) or equivalent (MySQL, Apache)
- Modern web browser

### Running the Application

1. Start MySQL database service
2. Create a database named 'event_management'
3. Install Python dependencies:
   ```
   pip install flask flask-login flask-sqlalchemy flask-wtf email-validator gunicorn mysql-connector-python werkzeug
   ```
4. Configure the database connection in app.py
5. Run the application:
   ```
   python main.py
   ```
6. Open your browser and navigate to http://localhost:5000

## Using the Application

### Registration & Login

1. Create an account by clicking 'Register'
2. Choose your user type (Organizer or Attendee)
3. Fill in your details and submit
4. Login using your email and password

### Creating Events (Organizers Only)

Only organizers have permission to create events:

1. Click on 'Create Event' in the navigation bar
2. Fill in the event details (title, description, date/time, location, etc.)
3. Set capacity and pricing options
4. Submit the form to create your event

### Managing Events (Organizers)

1. Go to 'My Events' to see all your created events
2. Edit or delete events as needed
3. View registration statistics

### Browsing and Registering for Events (Attendees)

1. Click on 'Explore Events' to browse all available events
2. Use filters to find specific events
3. Click on an event to view details
4. Register for the event by clicking 'Get Tickets'

### Managing Tickets

1. Go to 'My Tickets' to view all your registered events
2. See event details and ticket information
3. Cancel tickets for events you can no longer attend

## 🛠 Technology Stack

- **Frontend**: HTML, CSS, JavaScript, Bootstrap
- **Backend**: Python, Flask
- **Database**: MySQL (SQLAlchemy ORM)
- **Authentication**: Flask-Login
- **Forms & Validation**: Flask-WTF, Email-Validator
- **Visualization**: Chart.js

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- FontAwesome for icons
- Bootstrap for UI components
- Chart.js for data visualization

---

## 📚 Further Help

If you're a beginner, check out the [XAMPP Setup Guide for Beginners](XAMPP_SETUP_GUIDE.md) for a step-by-step walkthrough.
