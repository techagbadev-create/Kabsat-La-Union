# Kabsat La Union - Surf Resort Reservation System

<div align="center">
  
  **A surf resort reservation system for Kabsat La Union, Philippines**
  
  🌐 [kabsatlaunion.com](https://kabsatlaunion.com) | ✉️ Kabsatreservation@gmail.com
</div>

---

## Overview

A full-stack MERN reservation system featuring a premium surf resort booking experience with admin dashboard, PDF receipt generation, email confirmations, and live chat support.

## Live Demo

- **Website**: [kabsatlaunion.com](https://kabsatlaunion.com)
- **Frontend**: Hosted on Vercel
- **Backend API**: Hosted on Render

## Tech Stack

### Frontend

- **React 19** + **Vite** - Modern build tooling
- **Tailwind CSS** - Custom coastal theme
- **Zustand** - Lightweight state management
- **React Router v7** - Client-side routing
- **Radix UI** - Accessible UI primitives
- **jsPDF + html2canvas** - PDF receipt generation
- **Lucide React** - Icons
- **Sonner** - Toast notifications
- **date-fns** - Date handling

### Backend

- **Node.js + Express** - REST API server
- **MongoDB + Mongoose** - Database & ODM
- **JWT** - Admin authentication
- **Nodemailer** - Email service with PDF attachments
- **bcryptjs** - Password hashing
- **Helmet** - Security headers

## Features

### 🏄 Guest Features

- Browse surf resort rooms and bungalows with stunning imagery
- Real-time availability checking
- Interactive date picker with calendar
- Flexible guest count management
- Secure online booking
- Downloadable PDF receipts
- Email confirmation with receipt attachment
- Live chat support

### 👑 Admin Features

- Secure JWT-based authentication
- Dashboard with booking analytics
- Complete room management (CRUD)
- Seasonal discount configuration
- Booking management & status updates
- Payment confirmation workflow

## Project Structure

```
Kabsat-La-Union/
├── backend/
│   ├── config/           # Database & constants
│   ├── controllers/      # Route handlers
│   ├── middleware/       # Auth & validation
│   ├── models/           # Mongoose schemas
│   ├── routes/           # API endpoints
│   ├── utils/            # Email service, seeders
│   └── server.js
│
├── frontend/
│   ├── public/           # Static assets, SEO files
│   └── src/
│       ├── components/   # UI components & Receipt
│       ├── layouts/      # Header, Footer, AdminLayout
│       ├── lib/          # PDF generator, utilities
│       ├── pages/        # Route pages
│       ├── services/     # API service layer
│       └── store/        # Zustand stores
│
└── README.md
```

## Quick Start

### Prerequisites

- Node.js v18+
- MongoDB (local or Atlas)
- npm or yarn

### 1. Clone & Install

```bash
git clone https://github.com/RabbitDaCoder/Kabsat-La-Union.git
cd Kabsat-La-Union

# Backend
cd backend && npm install

# Frontend
cd ../frontend && npm install
```

### 2. Configure Environment

**Backend** (`backend/.env`):

```env
PORT=5000
NODE_ENV=development
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_secure_jwt_secret
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_gmail_app_password
EMAIL_FROM="Kabsat Reservation <reservation@kabsatlaunion.com>"
FRONTEND_URL=http://localhost:5173
```

**Frontend** (`frontend/.env`):

```env
VITE_API_URL=http://localhost:5000/api
```

### 3. Seed Database

```bash
cd backend
npm run seed:admin   # Creates admin user
npm run seed:rooms   # Seeds room data
```

### 4. Run Development Servers

```bash
# Terminal 1 - Backend (port 5000)
cd backend && npm run dev

# Terminal 2 - Frontend (port 5173)
cd frontend && npm run dev
```

## Deployment

| Service  | Platform | Root Directory |
| -------- | -------- | -------------- |
| Frontend | Vercel   | `frontend`     |
| Backend  | Render   | `backend`      |

## API Reference

### Public Endpoints

| Method | Endpoint                      | Description             |
| ------ | ----------------------------- | ----------------------- |
| GET    | `/api/rooms`                  | List available rooms    |
| GET    | `/api/rooms/:id`              | Get room details        |
| GET    | `/api/rooms/:id/availability` | Check room availability |
| POST   | `/api/bookings`               | Create booking          |
| GET    | `/api/bookings/:id`           | Get booking by ID       |
| GET    | `/api/health`                 | Health check            |

### Admin Endpoints (Protected)

| Method | Endpoint                  | Description     |
| ------ | ------------------------- | --------------- |
| POST   | `/api/auth/login`         | Admin login     |
| GET    | `/api/admin/dashboard`    | Dashboard stats |
| GET    | `/api/admin/rooms`        | List all rooms  |
| POST   | `/api/admin/rooms`        | Create room     |
| PUT    | `/api/admin/rooms/:id`    | Update room     |
| DELETE | `/api/admin/rooms/:id`    | Delete room     |
| GET    | `/api/admin/bookings`     | List bookings   |
| PATCH  | `/api/admin/bookings/:id` | Update booking  |

## Booking Flow

1. **Browse Rooms** → Guest explores available accommodations
2. **Select Dates** → Calendar picker with availability check
3. **Enter Details** → Guest information form
4. **Create Booking** → System generates booking confirmation
5. **Receive Receipt** → PDF generated & emailed

## SEO & Performance

- Optimized meta tags & Open Graph
- Sitemap & robots.txt
- PWA manifest
- Responsive images

## Contact

- **Website**: [kabsatlaunion.com](https://kabsatlaunion.com)
- **Email**: Kabsatreservation@gmail.com
- **Location**: La Union, Philippines

## License

ISC

---

<div align="center">
  Built with ❤️ by RabbitDaCoder
</div>
