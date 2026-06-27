# 🎡 Amusement Park Manager

<p align="center">
  <img src="https://img.shields.io/badge/version-2.0.0-blue?style=for-the-badge&labelColor=1a1a2e" alt="Version">
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge&labelColor=1a1a2e" alt="License">
  <img src="https://img.shields.io/badge/Node.js-v18+-339933?style=for-the-badge&logo=node.js&logoColor=white&labelColor=1a1a2e" alt="Node.js">
  <img src="https://img.shields.io/badge/Express-5.2-000000?style=for-the-badge&logo=express&logoColor=white&labelColor=1a1a2e" alt="Express">
  <img src="https://img.shields.io/badge/MongoDB-8.9-47A248?style=for-the-badge&logo=mongodb&logoColor=white&labelColor=1a1a2e" alt="MongoDB">
  <img src="https://img.shields.io/badge/EJS-Template-8A2BE2?style=for-the-badge&labelColor=1a1a2e" alt="EJS">
  <img src="https://img.shields.io/badge/Tailwind_CSS-3.4-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white&labelColor=1a1a2e" alt="Tailwind">
</p>

<p align="center">
  <b>🏆 A professional, multi-language, full-featured web application for managing amusement park games, attractions, transactions, and staff — with real-time stats, role-based access, coupon engine, shift tracking, and PDF report exports.</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Status-Production%20Ready-success?style=flat-square">
  <img src="https://img.shields.io/badge/PRs-Welcome-brightgreen?style=flat-square">
  <img src="https://img.shields.io/badge/Maintained-Yes-green?style=flat-square">
  <img src="https://img.shields.io/badge/Docker-Ready-2496ED?style=flat-square&logo=docker">
  <img src="https://img.shields.io/badge/Test_Coverage-Jest-C21325?style=flat-square&logo=jest">
</p>

---

## 📋 Table of Contents

- [✨ Features](#-features)
- [🖼️ Screenshots](#%EF%B8%8F-screenshots)
- [🏗️ Architecture](#%EF%B8%8F-architecture)
- [🛠️ Technology Stack](#%EF%B8%8F-technology-stack)
- [🚀 Quick Start](#-quick-start)
- [📖 Detailed Setup](#-detailed-setup)
- [👥 User Roles](#-user-roles)
- [📁 Project Structure](#-project-structure)
- [🌐 Multi-Language System](#-multi-language-system)
- [🎮 Game Management](#-game-management)
- [💳 Transaction System](#-transaction-system)
- [🏷️ Coupon Engine](#%EF%B8%8F-coupon-engine)
- [📊 Reports & Analytics](#-reports--analytics)
- [👤 Profile & Preferences](#-profile--preferences)
- [🔐 Admin Panel](#-admin-panel)
- [🌙 Dark Mode](#-dark-mode)
- [🐳 Docker Deployment](#-docker-deployment)
- [🧪 Testing](#-testing)
- [📚 API Reference](#-api-reference)
- [🔒 Security](#-security)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)
- [👨‍💻 Author](#%EF%B8%8F-author)

---

## ✨ Features

### 🔐 Authentication & Authorization
| Feature | Description |
|---------|-------------|
| **JWT-based Auth** | Secure JSON Web Token authentication with 24h expiry |
| **Role-Based Access** | Admin / Operator roles with granular route protection |
| **Session Management** | MongoDB-backed session store with auto-cleanup |
| **Login/Register** | Full register and login with bcrypt password hashing |

### 🎮 Game Management
| Feature | Description |
|---------|-------------|
| **CRUD Operations** | Full Create, Read, Update, Delete for games |
| **Image Uploads** | Secure multer upload (5MB limit, images only) with auto-cleanup |
| **Multi-Language Names** | Name and description in English, Arabic, and French |
| **Status System** | Active / Static / Closed states with visual badges |
| **Pricing Engine** | Per-player pricing with MAD currency formatting |
| **Categorization** | Custom categories for filtering (thrill, family, kids, water, etc.) |
| **Pagination** | 12 games per page with search and status filtering |

### 💰 Transaction Processing
| Feature | Description |
|---------|-------------|
| **Quick Add** | One-click transaction from game detail page |
| **Auto Revenue Calc** | Automatic total = price × players count |
| **Discount Engine** | Coupon code support with percentage discounts |
| **Refund System** | One-click refunds with audit logging |
| **Filtering** | Filter by game, status, date range, player name |
| **Operator Tracking** | Every transaction linked to the operator |

### 🏷️ Coupon Engine
| Feature | Description |
|---------|-------------|
| **Percentage Discounts** | Configurable 0–100% discount codes |
| **Usage Limits** | Max uses counter with auto-expiry |
| **Expiry Dates** | Set expiration dates for time-limited promotions |
| **Auto-Validation** | `isValid()` method checks active, max uses, and expiry |

### 📊 Reports & Analytics
| Feature | Description |
|---------|-------------|
| **Date Range** | Custom from/to date filtering |
| **Per-Game Reports** | Filter reports by specific game |
| **PDF Export** | Generate professional PDF reports via PDFKit |
| **Stats Summary** | Total revenue, transactions, players, average per day |
| **Admin Dashboard** | Overview cards with key metrics |

### 👥 User Management
| Feature | Description |
|---------|-------------|
| **User CRUD** | Admin can create/edit users with role assignment |
| **Toggle Active** | Enable/disable user accounts instantly |
| **Role Labels** | Visual role badges (Admin purple, Operator blue) |

### 📜 Activity Logging (Audit Trail)
| Feature | Description |
|---------|-------------|
| **Full Audit** | Every create/update/delete/refund logged |
| **Old/New Diffs** | `oldValues` / `newValues` stored for changes |
| **Pagination** | 30 logs per page chronologically |
| **Clear Logs** | Admin can purge the log |

### 👤 Profile Management
| Feature | Description |
|---------|-------------|
| **Edit Name** | Update display name |
| **Language Preference** | Switch between English, Arabic, French |
| **Theme Toggle** | Light/Dark mode with server-side persistence |
| **Password Change** | Secure password update with current password verification |

### 👷 Shift Management
| Feature | Description |
|---------|-------------|
| **Start/End Shifts** | Track operator working hours |
| **Status Tracking** | Active / Completed / Cancelled states |
| **History View** | Chronological shift history with user attribution |

### 🌐 Internationalization (i18n)
| Feature | Description |
|---------|-------------|
| **3 Languages** | English, Arabic (العربية), French (Français) |
| **RTL Support** | Full right-to-left layout for Arabic |
| **Locale Files** | JSON-based translation files, easy to extend |
| **User Preference** | Language saved per user, persists across sessions |

### 🎨 UI/UX
| Feature | Description |
|---------|-------------|
| **Responsive Design** | Mobile-first with Tailwind CSS |
| **Dark Mode** | Full dark theme with system-class toggle |
| **Smooth Animations** | Fade-in transitions, hover effects |
| **Toast Notifications** | Success/error flash messages |
| **Modal Dialogs** | Create modals for transactions, users, coupons |
| **SVG Icons** | Heroicons throughout the interface |

---

## 🖼️ Screenshots

```
  ┌─────────────────────────────────────────────────────┐
  │                    🎡 LOGIN PAGE                     │
  ├─────────────────────────────────────────────────────┤
  │                                                     │
  │                 🎡                                  │
  │           Amusement Park Manager                    │
  │     Manage your park games with ease               │
  │                                                     │
  │  ┌─────────────────────────────────────────────────┐│
  │  │  Email:    admin@park.com                       ││
  │  │  Password: •••••••••                            ││
  │  │                                                 ││
  │  │  ┌─────────────────────────────────────────────┐ ││
  │  │  │                  Login                      │ ││
  │  │  └─────────────────────────────────────────────┘ ││
  │  └─────────────────────────────────────────────────┘│
  │                                                     │
  │       Don't have an account? Register               │
  └─────────────────────────────────────────────────────┘

  ┌─────────────────────────────────────────────────────┐
  │  🎡 Amusement Park    [🏠  🎮  💰  📊  ⚙️  🌙]     │
  ├─────────────────────────────────────────────────────┤
  │  Welcome, Admin!                    June 27, 2026   │
  │                                                     │
  │  ┌──────┐ ┌────────┐ ┌──────┐ ┌──────────┐        │
  │  │  47  │ │ 12,450 │ │  89  │ │ 342,800  │        │
  │  │ Txns │ │Revenue │ │Players│ │Total Rev │        │
  │  └──────┘ └────────┘ └──────┘ └──────────┘        │
  │                                                     │
  │  ┌──────────── Recent Transactions ──────────────┐  │
  │  │ Game        │ Players │ Amount │ Date         │  │
  │  ├───────────────────────────────────────────────┤  │
  │  │ Ferris Wheel│   2     │ 60 MAD │ Jun 27      │  │
  │  └───────────────────────────────────────────────┘  │
  └─────────────────────────────────────────────────────┘

  ┌─────────────────────────────────────────────────────┐
  │  🎮 Games                    [+ New Game]           │
  ├─────────────────────────────────────────────────────┤
  │                                                     │
  │  ┌──────┐ ┌──────┐ ┌──────┐ ┌──────┐              │
  │  │  🎡  │ │  🎢  │ │  🚗  │ │  🎠  │              │
  │  │Ferris│ │Coastr│ │Bumper│ │Crsell│              │
  │  │30 MAD│ │50 MAD│ │25 MAD│ │15 MAD│              │
  │  └──────┘ └──────┘ └──────┘ └──────┘              │
  └─────────────────────────────────────────────────────┘
```

> *For live screenshots, deploy and visit `http://localhost:3000`*

---

## 🏗️ Architecture

```
                           ┌─────────────────────┐
                           │    Client Browser    │
                           │   (Tailwind + EJS)   │
                           └──────────┬──────────┘
                                      │ HTTP/HTTPS
                                      ▼
                     ┌─────────────────────────────┐
                     │      Express.js Server       │
                     │         (server.js)          │
                     │                              │
                     │  ┌──────┐ ┌──────┐ ┌──────┐ │
                     │  │Auth  │ │Rate  │ │Sess. │ │
                     │  │Mid.  │ │Limit │ │Store │ │
                     │  └──┬───┘ └──────┘ └──┬───┘ │
                     │     │                  │     │
                     │     ▼                  ▼     │
                     │  ┌───────────────────────┐  │
                     │  │    Express Routes      │  │
                     │  │ ┌───┐ ┌───┐ ┌───┐     │  │
                     │  │ │Gme│ │Trx│ │Adm│ ... │  │
                     │  │ └───┘ └───┘ └───┘     │  │
                     │  └───────────┬───────────┘  │
                     │              │              │
                     │              ▼              │
                     │  ┌───────────────────────┐  │
                     │  │     Controllers        │  │
                     │  │    (Business Logic)    │  │
                     │  └───────────┬───────────┘  │
                     │              │              │
                     │              ▼              │
                     │  ┌───────────────────────┐  │
                     │  │   Mongoose Models     │  │
                     │  │  (ODM / Data Layer)   │  │
                     │  └───────────┬───────────┘  │
                     └──────────────┼──────────────┘
                                    │
                                    ▼
                     ┌─────────────────────────────┐
                     │        MongoDB               │
                     │  ┌──┐ ┌──┐ ┌──┐ ┌──┐ ┌──┐  │
                     │  │Usr│ │Gme│ │Trx│ │Log│ │...│
                     │  └──┘ └──┘ └──┘ └──┘ └──┘  │
                     └─────────────────────────────┘
```

### Request Lifecycle

```
  Request  →  Rate Limiter  →  Session Load  →  i18n Middleware
     ↓
  Load User (JWT verify)  →  Set locals  →  Flash Messages
     ↓
  Route Match → Auth Check → Controller → Model Query
     ↓
  Render EJS → Express Layouts → HTML Response
```

---

## 🛠️ Technology Stack

### Backend
| Technology | Version | Purpose |
|------------|---------|---------|
| ![Node.js](https://img.shields.io/badge/-Node.js-339933?logo=node.js) | **18+** | JavaScript runtime |
| ![Express](https://img.shields.io/badge/-Express-000000?logo=express) | **5.2** | Web framework & routing |
| ![MongoDB](https://img.shields.io/badge/-MongoDB-47A248?logo=mongodb) | **8.9** | NoSQL database |
| ![Mongoose](https://img.shields.io/badge/-Mongoose-880000) | **8.9** | MongoDB ODM |
| ![JWT](https://img.shields.io/badge/-JWT-000000?logo=jsonwebtokens) | **9.0** | Authentication tokens |
| ![bcrypt](https://img.shields.io/badge/-bcrypt-003545) | **2.4** | Password hashing |
| ![Multer](https://img.shields.io/badge/-Multer-FF6C37) | **1.4** | File upload handling |
| ![PDFKit](https://img.shields.io/badge/-PDFKit-EC1C24) | **0.15** | PDF report generation |

### Frontend
| Technology | Version | Purpose |
|------------|---------|---------|
| ![EJS](https://img.shields.io/badge/-EJS-8A2BE2) | **3.1** | Template engine |
| ![Tailwind CSS](https://img.shields.io/badge/-Tailwind-06B6D4?logo=tailwindcss) | **3.4** | Utility-first CSS |
| ![Chart.js](https://img.shields.io/badge/-Chart.js-FF6384?logo=chartdotjs) | **4.4** | Data visualization |
| ![Heroicons](https://img.shields.io/badge/-Heroicons-8A2BE2) | — | SVG icon library |

### Infrastructure
| Technology | Purpose |
|------------|---------|
| ![Docker](https://img.shields.io/badge/-Docker-2496ED?logo=docker) | Containerization |
| ![Jest](https://img.shields.io/badge/-Jest-C21325?logo=jest) | Testing framework |
| ![Supertest](https://img.shields.io/badge/-Supertest-00D8AE) | HTTP assertion testing |

---

## 🚀 Quick Start

```bash
# 1. Clone
git clone https://github.com/wickmrakchi/Park-Project
cd "Park System"

# 2. Install
npm install

# 3. Configure
cp .env.example .env
# Edit .env with your MongoDB URI and secret

# 4. Seed database
npm run seed

# 5. Start development server
npm run dev

# 6. Open in browser
open http://localhost:3000
```

---

## 📖 Detailed Setup

### Prerequisites
- [Node.js](https://nodejs.org/) v18 or higher
- [MongoDB](https://www.mongodb.com/) v7 or higher (local or Atlas)
- [npm](https://www.npmjs.com/) v9+ (ships with Node)

### Environment Configuration

Create a `.env` file in the project root:

```env
# ─── MongoDB ──────────────────────────────────────────
MONGO_URI=mongodb://localhost:27017/amusement-park

# ─── Session ──────────────────────────────────────────
SESSION_SECRET=your-super-secret-key-change-in-production

# ─── Server ───────────────────────────────────────────
PORT=3000

# ─── Environment ──────────────────────────────────────
NODE_ENV=development
```

| Variable | Required | Default | Description |
|----------|----------|---------|-------------|
| `MONGO_URI` | ✅ | — | MongoDB connection string |
| `SESSION_SECRET` | ✅ | — | Session encryption key (min 32 chars) |
| `PORT` | ❌ | `3000` | Server listening port |
| `NODE_ENV` | ❌ | `development` | Environment mode |

### Seeding the Database

The seed script populates your database with demo data:

```bash
npm run seed
```

**Seed Data:**
| Entity | Count | Details |
|--------|-------|---------|
| 👤 **Users** | 2 | Admin (`admin@park.com` / `admin123`), Operator (`operator@park.com` / `operator123`) |
| 🎮 **Games** | 6 | Ferris Wheel (30 MAD), Roller Coaster (50 MAD), Bumper Cars (25 MAD), Carousel (15 MAD), Haunted House (35 MAD), Water Slide (40 MAD) |
| 💰 **Transactions** | 3 | Sample entries with different operators |
| 🏷️ **Coupons** | 3 | WELCOME10 (10%), SUMMER20 (20%), VIP50 (50%) |

### Running the Application

```bash
# Production
npm start

# Development (with auto-restart)
npm run dev
```

Visit **[http://localhost:3000](http://localhost:3000)** 🚀

---

## 👥 User Roles

### 🛡️ Admin
- **Full system access**
- Manage users (create, activate/deactivate)
- View activity logs with full audit trail
- Manage coupons (create, expiry, usage limits)
- View all reports
- Access admin dashboard with system-wide stats
- Manage shifts
- All Operator permissions

### 🎮 Operator
- **Game operations**
- View games list and details
- Record transactions (player entries)
- Process refunds
- View personal profile and edit settings
- View reports
- Start/end shifts

### Route Protection Matrix

| Route | Admin | Operator | Public |
|-------|:-----:|:--------:|:------:|
| `/auth/login` | ❌ | ❌ | ✅ |
| `/auth/register` | ❌ | ❌ | ✅ |
| `/` Dashboard | ✅ | ✅ | ❌ |
| `/games` | ✅ | ✅ | ❌ |
| `/games/new` | ✅ | ❌ | ❌ |
| `/games/:id/edit` | ✅ | ❌ | ❌ |
| `/games/:id/delete` | ✅ | ❌ | ❌ |
| `/transactions` | ✅ | ✅ | ❌ |
| `/reports` | ✅ | ❌ | ❌ |
| `/admin` | ✅ | ❌ | ❌ |
| `/admin/users` | ✅ | ❌ | ❌ |
| `/admin/logs` | ✅ | ❌ | ❌ |
| `/admin/coupons` | ✅ | ❌ | ❌ |
| `/admin/shifts` | ✅ | ✅ | ❌ |
| `/profile` | ✅ | ✅ | ❌ |

---

## 📁 Project Structure

```
Park System/
│
├── 📁 src/                          # Source code root
│   │
│   ├── 📁 config/                   # Configuration files
│   │   ├── 📄 db.js                 # MongoDB connection
│   │   └── 📄 i18n.js               # Internationalization engine
│   │
│   ├── 📁 controllers/              # Business logic layer
│   │   ├── 📄 authController.js     # Login/register/logout
│   │   ├── 📄 dashboardController.js# Dashboard stats & data
│   │   ├── 📄 gameController.js     # Game CRUD operations
│   │   ├── 📄 transactionController.js # Transaction processing
│   │   ├── 📄 adminController.js    # Admin panel logic
│   │   ├── 📄 profileController.js  # User profile management
│   │   └── 📄 reportController.js   # Report generation & PDF
│   │
│   ├── 📁 locales/                  # Translation files
│   │   ├── 📄 en.json               # English (UK/US)
│   │   ├── 📄 ar.json               # العربية (Arabic)
│   │   └── 📄 fr.json               # Français (French)
│   │
│   ├── 📁 middleware/               # Express middleware
│   │   ├── 📄 auth.js               # JWT auth & role guard
│   │   ├── 📄 i18n.js               # Language detection
│   │   ├── 📄 upload.js             # Multer file upload config
│   │   └── 📄 stats.js              # Dashboard statistics
│   │
│   ├── 📁 models/                   # Mongoose schemas
│   │   ├── 📄 User.js               # User model (bcrypt hashing)
│   │   ├── 📄 Game.js               # Game model (multi-lang)
│   │   ├── 📄 Transaction.js        # Transaction model
│   │   ├── 📄 Log.js                # Audit log model
│   │   ├── 📄 Coupon.js             # Coupon model (validation)
│   │   └── 📄 Shift.js              # Shift model
│   │
│   ├── 📁 public/                   # Static assets
│   │   ├── 📁 css/
│   │   │   └── 📄 style.css         # Custom styles & animations
│   │   ├── 📁 js/
│   │   │   └── 📄 main.js           # Client-side JavaScript
│   │   ├── 📁 images/
│   │   │   └── 📄 placeholder.svg   # Default game image
│   │   └── 📁 uploads/              # Game image uploads
│   │
│   ├── 📁 routes/                   # Express route definitions
│   │   ├── 📄 auth.js               # /auth/* routes
│   │   ├── 📄 dashboard.js          # / (root) routes
│   │   ├── 📄 games.js              # /games/* routes
│   │   ├── 📄 transactions.js       # /transactions/* routes
│   │   ├── 📄 admin.js              # /admin/* routes
│   │   ├── 📄 profile.js            # /profile/* routes
│   │   └── 📄 reports.js            # /reports/* routes
│   │
│   ├── 📁 views/                    # EJS templates
│   │   ├── 📁 layouts/
│   │   │   └── 📄 main.ejs          # Main layout shell
│   │   ├── 📁 partials/
│   │   │   ├── 📄 navbar.ejs        # Navigation bar
│   │   │   └── 📄 footer.ejs        # Page footer
│   │   ├── 📁 auth/
│   │   │   ├── 📄 login.ejs         # Login page
│   │   │   └── 📄 register.ejs      # Registration page
│   │   ├── 📁 dashboard/
│   │   │   └── 📄 index.ejs         # Dashboard view
│   │   ├── 📁 games/
│   │   │   ├── 📄 index.ejs         # Games grid with filters
│   │   │   ├── 📄 show.ejs          # Game detail + transactions
│   │   │   ├── 📄 new.ejs           # Create game form
│   │   │   └── 📄 edit.ejs          # Edit game form
│   │   ├── 📁 transactions/
│   │   │   └── 📄 index.ejs         # Transaction list + modal
│   │   ├── 📁 admin/
│   │   │   ├── 📄 index.ejs         # Admin dashboard
│   │   │   ├── 📄 users.ejs         # User management
│   │   │   ├── 📄 logs.ejs          # Audit log viewer
│   │   │   ├── 📄 coupons.ejs       # Coupon management
│   │   │   └── 📄 shifts.ejs        # Shift management
│   │   ├── 📁 profile/
│   │   │   ├── 📄 show.ejs          # Profile display
│   │   │   └── 📄 edit.ejs          # Profile editor
│   │   └── 📁 reports/
│   │       └── 📄 index.ejs         # Report generator + results
│   │
│   └── 📄 seed.js                   # Database seeder
│
├── 📁 tests/                        # Test files
│   └── 📄 auth.test.js              # Authentication tests
│
├── 📄 server.js                     # Application entry point
├── 📄 package.json                  # Dependencies & scripts
├── 📄 .env                          # Environment variables
├── 📄 .gitignore                    # Git ignore rules
├── 📄 Dockerfile                    # Docker build spec
├── 📄 docker-compose.yml            # Docker Compose config
└── 📄 README.md                     # This file (you are here)
```

---

## 🌐 Multi-Language System

### Architecture
The i18n system uses a custom engine (`src/config/i18n.js`) with JSON locale files:

```
Request → Cookie/Session/User lang → Load locale JSON → t('key')
```

### Adding a New Language

1. Create `src/locales/de.json` (or any language code)
2. Copy structure from `en.json` and translate values
3. That's it! The system auto-detects new files

### Translation Key Pattern

Keys use dot notation: `games.createSuccess`, `admin.users`, `common.save`

Supports variable interpolation:
```json
{
  "dashboard": {
    "welcome": "Welcome, {name}!"
  }
}
```
```javascript
t('dashboard.welcome', { name: 'Admin' })
// → "Welcome, Admin!"
```

### Language Detection Priority
1. User's saved preference (`req.user.lang`)
2. Session language (`req.session.lang`)
3. Cookie (`req.cookies.lang`)
4. Default: `'en'`

---

## 🎮 Game Management

### Game States

```
┌────────────┐
│   Active   │ ← Currently operational, can accept transactions
├────────────┤
│   Static   │ ← Displayed but not taking new players
├────────────┤
│   Closed   │ ← Hidden from active views, no transactions
└────────────┘
```

### Game CRUD

| Action | Route | Method | Auth |
|--------|-------|--------|------|
| **List** | `/games` | GET | User |
| **View** | `/games/:id` | GET | User |
| **Create** | `/games/new` | GET | Admin |
| **Create** | `/games` | POST | Admin |
| **Edit** | `/games/:id/edit` | GET | Admin |
| **Update** | `/games/:id` | POST | Admin |
| **Delete** | `/games/:id/delete` | POST | Admin |

---

## 💳 Transaction System

### Transaction Flow

```
  Operator clicks "Add Transaction"
         │
         ▼
  Select Game → Enter Player Name → Players Count
         │
         ▼
  Optional: Apply Coupon Code
         │
         ▼
  System calculates: totalAmount = price × playersCount
         │
         ▼
  If coupon: totalAmount = totalAmount - (totalAmount × discount%)
         │
         ▼
  Transaction saved → Revenue updated → Log created
```

### Transaction States

| State | Description |
|-------|-------------|
| `completed` | Standard transaction, revenue counted |
| `refunded` | Money returned, excluded from revenue |
| `cancelled` | Cancelled, excluded from revenue |

---

## 🏷️ Coupon Engine

### Coupon Validation Logic

```javascript
isValid() {
  if (!this.active) return false;             // Must be active
  if (this.maxUses > 0 &&                     // If has limit
      this.usedCount >= this.maxUses)          // Check usage
    return false;
  if (this.expiresAt &&                        // If has expiry
      this.expiresAt < new Date())             // Check date
    return false;
  return true;                                 // Valid!
}
```

---

## 📊 Reports & Analytics

### Report Features
- **Date Range**: Custom `from` / `to` date selection
- **Game Filter**: Filter by specific game or all games
- **Summary Cards**: Total revenue, transactions, players, daily average
- **Transaction Table**: Detailed chronologically sorted list
- **PDF Export**: Professional PDF with company header, summary stats, and full transaction list

### PDF Report Sample

```
╔══════════════════════════════════════════╗
║        Amusement Park Report              ║
║                                           ║
║  Period: 2026-01-01 → 2026-06-27         ║
║                                           ║
║  Total Revenue:    342,800 MAD           ║
║  Total Transactions: 1,247               ║
║  Total Players:    4,892                 ║
║                                           ║
║  ─── Transactions ───                     ║
║  06/27 | Ferris Wheel | 2 | 60 MAD       ║
║  06/27 | Roller Coaster | 1 | 50 MAD     ║
║  ...                                      ║
╚══════════════════════════════════════════╝
```

---

## 👤 Profile & Preferences

Users can manage their profile settings:

```
Profile
├── Name (editable)
├── Email (read-only)
├── Role (read-only)
├── Language: English / العربية / Français
├── Theme: Light / Dark
└── Password (change with current password verification)
```

---

## 🔐 Admin Panel

### Admin Dashboard Metrics
| Card | Description |
|------|-------------|
| 👥 **Users** | Total registered users |
| 🎮 **Games** | Total games in system |
| 💰 **Transactions** | Total transaction count |
| 📈 **Total Revenue** | Sum of all completed transactions |

### Activity Logs (Audit Trail)

Every operation is logged with:
- **User**: Who performed the action
- **Action**: `create`, `update`, `delete`, `refund`, `activate`, `deactivate`
- **Resource**: Affected entity type (Game, User, Transaction, Profile)
- **Details**: Human-readable description
- **Old Values**: Snapshot before change
- **New Values**: Snapshot after change
- **Timestamp**: When it happened

---

## 🌙 Dark Mode

### Implementation
- **CSS Class Strategy**: Tailwind's `dark:` variant with `class` mode
- **Persistence**: Theme preference saved to user profile in database
- **Toggle**: Instant switch via JavaScript, persisted via `POST /lang/theme/:theme`

### Color Palette

| Element | Light | Dark |
|---------|-------|------|
| Background | `bg-gray-50` | `bg-gray-900` |
| Cards | `bg-white` | `bg-gray-800` |
| Text | `text-gray-900` | `text-gray-100` |
| Borders | `border-gray-300` | `border-gray-600` |
| Primary | `primary-600` | `primary-400` |

---

## 🐳 Docker Deployment

### Using Docker Compose (Recommended)

```bash
# Build & start
docker-compose up -d

# View logs
docker-compose logs -f

# Stop
docker-compose down
```

### Docker Architecture

```
  ┌──────────────────────────────────────────┐
  │         docker-compose.yml                │
  ├──────────────────────────────────────────┤
  │                                          │
  │  ┌──────────────────┐  ┌──────────────┐  │
  │  │   app:3000        │  │   mongo:27017 │  │
  │  │   (Node.js)       │◄─┤   (MongoDB)   │  │
  │  └──────────────────┘  └──────────────┘  │
  │                       │                  │
  │  ┌──────────────────┐  ┌──────────────┐  │
  │  │   volumes:        │  │   volumes:    │  │
  │  │   uploads_data    │  │   mongo_data  │  │
  │  └──────────────────┘  └──────────────┘  │
  └──────────────────────────────────────────┘
```

### Manual Docker Build

```bash
# Build image
docker build -t amusement-park-manager .

# Run container
docker run -p 3000:3000 \
  -e MONGO_URI=mongodb://host.docker.internal:27017/amusement-park \
  -e SESSION_SECRET=your-secret \
  amusement-park-manager
```

---

## 🧪 Testing

### Test Suite

```bash
# Run all tests
npm test

# Watch mode
npm run test:watch
```

### Test Coverage

```
auth.test.js
├── GET  /auth/login     → 200 (login page renders)
├── GET  /auth/register  → 200 (register page renders)
├── POST /auth/register  → 302 (user created)
├── POST /auth/login     → 302 (valid credentials)
└── POST /auth/login     → 200 (invalid credentials → error shown)
```

### Writing Tests

Tests use **Jest** + **Supertest** with **MongoDB Memory Server** for isolated database testing:

```javascript
const request = require('supertest');
const mongoose = require('mongoose');
const { MongoMemoryServer } = require('mongodb-memory-server');

let mongoServer;
let app;

beforeAll(async () => {
  mongoServer = await MongoMemoryServer.create();
  process.env.MONGO_URI = mongoServer.getUri();
  app = require('../server');
});

afterAll(async () => {
  await mongoose.disconnect();
  await mongoServer.stop();
});
```

---

## 📚 API Reference

### Authentication

| Endpoint | Method | Description | Auth |
|----------|--------|-------------|------|
| `/auth/login` | GET | Login page | — |
| `/auth/login` | POST | Authenticate user | — |
| `/auth/register` | GET | Register page | — |
| `/auth/register` | POST | Create account | — |
| `/auth/logout` | GET | Logout | Session |

### Games

| Endpoint | Method | Description | Auth |
|----------|--------|-------------|------|
| `/games` | GET | List games (paginated) | User |
| `/games/new` | GET | New game form | Admin |
| `/games` | POST | Create game | Admin |
| `/games/:id` | GET | Game detail + transactions | User |
| `/games/:id/edit` | GET | Edit game form | Admin |
| `/games/:id` | POST | Update game | Admin |
| `/games/:id/delete` | POST | Delete game | Admin |

### Transactions

| Endpoint | Method | Description | Auth |
|----------|--------|-------------|------|
| `/transactions` | GET | List transactions | User |
| `/transactions` | POST | Create transaction | User |
| `/transactions/:id/refund` | POST | Refund transaction | User |

### Admin

| Endpoint | Method | Description | Auth |
|----------|--------|-------------|------|
| `/admin` | GET | Admin dashboard | Admin |
| `/admin/users` | GET | User management | Admin |
| `/admin/users` | POST | Create user | Admin |
| `/admin/users/:id/toggle` | POST | Activate/deactivate user | Admin |
| `/admin/logs` | GET | Activity logs | Admin |
| `/admin/logs/clear` | POST | Clear all logs | Admin |
| `/admin/coupons` | GET | Coupon management | Admin |
| `/admin/coupons` | POST | Create coupon | Admin |
| `/admin/shifts` | GET | Shift management | User |
| `/admin/shifts/start` | POST | Start shift | User |
| `/admin/shifts/end` | POST | End shift | User |

### Profile

| Endpoint | Method | Description | Auth |
|----------|--------|-------------|------|
| `/profile` | GET | View profile | User |
| `/profile/edit` | GET | Edit profile form | User |
| `/profile/edit` | POST | Update profile | User |
| `/profile/change-password` | POST | Change password | User |

### Reports

| Endpoint | Method | Description | Auth |
|----------|--------|-------------|------|
| `/reports` | GET | Report page | Admin |
| `/reports/generate` | POST | Generate report | Admin |
| `/reports/export/pdf` | GET | Export PDF | Admin |

### System

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/lang/:lang` | GET | Switch language (en/ar/fr) |
| `/lang/theme/:theme` | POST | Toggle theme (light/dark) |

---

## 🔒 Security

### Implemented Measures

| Measure | Implementation |
|---------|---------------|
| **Password Hashing** | bcryptjs with 12 salt rounds |
| **JWT Authentication** | 24-hour tokens with secret signing |
| **Rate Limiting** | 200 req/15min global, 20 req/15min on auth |
| **Session Security** | MongoDB-backed store, HTTP-only cookies |
| **File Upload Validation** | Image-only filter + 5MB size limit |
| **Input Validation** | express-validator ready (extensible) |
| **XSS Protection** | EJS auto-escapes output (`<%= %>`) |
| **CSRF Readiness** | Session-based, ready for csurf integration |
| **Role Authorization** | Route-level guards with role verification |
| **Error Handling** | Centralized error middleware, no stack leaks |
| **Dependency Audit** | Regular `npm audit` maintenance |

### Security Checklist for Production
- [ ] Change `SESSION_SECRET` to a strong random value
- [ ] Set `NODE_ENV=production`
- [ ] Enable HTTPS with a valid certificate
- [ ] Set up MongoDB authentication
- [ ] Configure firewall rules
- [ ] Run `npm audit` and fix vulnerabilities
- [ ] Set up regular database backups
- [ ] Use environment-specific `.env` files

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

### Bug Reports & Feature Requests
- Use the [GitHub Issues](https://github.com/wickmrakchi/Park-Project/issues) tab
- Provide clear reproduction steps for bugs
- Describe the expected vs actual behavior

### Pull Request Process
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines
- Follow existing code style and conventions
- Add tests for new features
- Update documentation when changing functionality
- Keep PRs focused on a single concern

---

## 📄 License

This project is licensed under the **MIT License**.

```
MIT License

Copyright (c) 2026 Hamza Mrakchi

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 👨‍💻 Author

<p align="center">
  <img src="https://img.shields.io/badge/حَمْزَة_الْمُرَاكْشِي-000000?style=for-the-badge" alt="Hamza Mrakchi">
</p>

<p align="center">
  <b>Hamza Mrakchi</b> — Full-Stack Developer & System Architect
</p>

<p align="center">
  <a href="https://github.com/wickmrakchi">
    <img src="https://img.shields.io/badge/GitHub-wickmrakchi-181717?style=for-the-badge&logo=github" alt="GitHub">
  </a>
  <a href="https://www.instagram.com/mrakchi_5/">
    <img src="https://img.shields.io/badge/Instagram-@mrakchi__5-E4405F?style=for-the-badge&logo=instagram" alt="Instagram">
  </a>
  <a href="mailto:hessamgrati@gmail.com">
    <img src="https://img.shields.io/badge/Email-hessamgrati@gmail.com-D14836?style=for-the-badge&logo=gmail" alt="Email">
  </a>
</p>

---

<p align="center">
  <img src="https://img.shields.io/badge/⭐_Star_this_repo_if_you_found_it_useful!-FFD700?style=for-the-badge" alt="Star">
</p>

<p align="center">
  <sub>Built with ❤️ using Node.js, Express, MongoDB, and Tailwind CSS</sub>
</p>
