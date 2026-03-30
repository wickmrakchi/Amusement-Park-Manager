# Amusement Park Manager

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node.js](https://img.shields.io/badge/Node.js-v18-green.svg)](https://nodejs.org/)
[![Express](https://img.shields.io/badge/Express-5.2-blue.svg)](https://expressjs.com/)

A professional web application for managing amusement park games and attractions. Track player transactions, monitor real-time revenue and stats, manage game statuses, and handle user roles with secure authentication.

## ✨ Features (v1.1.0)

- **User Authentication**: Secure login/register with role-based access (Admin, Game operators)
- **Game Management**: Admin dashboard to **upload/edit game images**, pricing, status (static/active/closed) – auto default placeholder
- **Activity Logs**: Full audit trail (/admin/logs) with old/new diffs for games/users updates
- **Profile Management**: Users edit name/password (email/roles read-only)

- **Transaction Tracking**: Record player entries with automatic revenue calculation (MAD currency)
- **Real-time Stats**: Live polling for daily players and revenue per game
- **Game Pages**: Detailed views with history tables, live metrics, and quick-add transactions
- **Dashboard Overview**: Centralized stats and navigation
- **Profile Management**: User settings and role info
- **Image Uploads**: Secure multer uploads for game images (5MB limit, images only)
- **Responsive UI**: Tailwind CSS with modern, mobile-friendly design
- **Rate Limiting & Validation**: Production-ready security

## 🛠️ Technologies Used

| Frontend | Backend | Database | Other |
|----------|---------|----------|--------|
| EJS Templates | Node.js / Express 5 | MongoDB / Mongoose | Tailwind CSS |
| | Multer (uploads) | | bcryptjs / JWT |
| | express-session | | express-validator |
| | connect-mongo | | dotenv |

## 📁 Project Structure

```
Park Project/
├── models/     # Mongoose schemas (Game, Transaction, User, Log)
├── routes/     # Express routes (auth, dashboard, games, admin, profile)
├── views/      # EJS templates (dashboard, game, admin, etc.)
├── public/     # Static assets (CSS, JS, images)
├── middleware/ # Auth, stats middleware
├── server.js   # Main Express app
├── package.json
└── .env        # Environment variables
```

## 🚀 Installation

1. **Clone & Install Dependencies**
   ```bash
   git clone https://github.com/wickmrakchi/Park-Project
   cd "Park Project"
   npm install
   ```

2. **Environment Setup**
   Create `.env` file:
   ```
   MONGO_URI=mongodb://localhost:27017/amusement-park
   SESSION_SECRET=your-super-secret-key-here
   PORT=3000
   ```

3. **Run the Application**
   ```bash
   npm run dev
   ```
   Open [http://localhost:3000](http://localhost:3000)

## ⚙️ Configuration

| Variable | Description | Example |
|----------|-------------|---------|
| `MONGO_URI` | MongoDB connection string | `mongodb://localhost:27017/amusement-park` |
| `SESSION_SECRET` | Session encryption key | `your-super-secret-key-here` |
| `PORT` | Server port | `3000` |

## 📱 Screenshots

<!-- Add screenshots here -->
*![Login Preview](https://cdn.discordapp.com/attachments/1476763298325201037/1487474932894928916/image.png?ex=69c9467b&is=69c7f4fb&hm=77a0a79b1de1e7e2f290db17faeb5f6ae8852da87dfe4a0793b858e95726669d&)*
*![Dashboard Preview](https://cdn.discordapp.com/attachments/1476763298325201037/1487474425229213957/image.png?ex=69c94602&is=69c7f482&hm=0b6323747ed6173e7051678428ec8f30c2bbca47326cc131b595e2ddcb91e157&)*
*![Game Management](https://cdn.discordapp.com/attachments/1476763298325201037/1487474564022796318/image.png?ex=69c94624&is=69c7f4a4&hm=0d3f4d8936536bf28265a6243bb4ab5b5d4b16b4a42ce5782951e999ef4a3a5b&)*
*![Admin Panel](https://cdn.discordapp.com/attachments/1476763298325201037/1487474409164898364/image.png?ex=69c945ff&is=69c7f47f&hm=7357653f41d1f2b6ca656ffe649851af46d7d0a2a13d7292f509cead2aba0db8&)*

> **Note**: Screenshots placeholders. Add actual images to `public/images/` and update paths.

## 👨‍💼 Author

**Hamza Mrakchi**

- GitHub: [@wickmrakchi](https://github.com/wickmrakchi)
- Email: hessmgrati@gmail.com

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

⭐ **Star this repo if you found it useful!** ⭐

