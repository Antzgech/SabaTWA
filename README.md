# 🎮 Telegram Rewards App

A complete, production-ready gamified reward system for Telegram Web App. Users earn points through gaming, social media engagement, and referrals, with automated bi-weekly cash rewards for top performers.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Node](https://img.shields.io/badge/node-%3E%3D18.0.0-brightgreen.svg)
![React](https://img.shields.io/badge/react-18.2.0-blue.svg)

## ✨ Key Features

- 🎯 **Daily HTML5 Game** - 10-minute engaging gameplay with point rewards
- 📱 **Telegram Integration** - Seamless authentication via Telegram Web App
- 🎁 **Automated Rewards** - $3-$18 prizes distributed every 15 days
- 📊 **Real-time Leaderboard** - Live updates via WebSocket
- 🔗 **Referral System** - Earn 500 points per referred friend
- 📲 **Social Tasks** - YouTube, TikTok, Facebook, Telegram verification
- 🎚️ **3-Level System** - Progressive challenges with cumulative rewards
- 👨‍💼 **Admin Dashboard** - Complete management interface
- 🔒 **Enterprise Security** - JWT auth, rate limiting, input validation

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- PostgreSQL 14+
- Telegram Bot Token (from @BotFather)

### Installation

1. **Clone repository**
```bash
git clone https://github.com/yourusername/telegram-rewards-app.git
cd telegram-rewards-app
```

2. **Backend setup**
```bash
cd backend
npm install
cp .env.example .env
# Edit .env with your credentials
npm run migrate
npm run dev
```

3. **Frontend setup**
```bash
cd ../frontend
npm install
npm run dev
```

4. **Access the app**
- Backend: http://localhost:5000
- Frontend: http://localhost:3000

📖 **Full instructions**: See [Quick Start Guide](docs/QUICKSTART.md)

## 📚 Documentation

- **[Complete Documentation](docs/README.md)** - Architecture, API, deployment
- **[Quick Start Guide](docs/QUICKSTART.md)** - Get running in 5 minutes
- **[API Reference](docs/README.md#api-documentation)** - All endpoints documented

## 🏗️ Tech Stack

**Backend**
- Node.js + Express
- PostgreSQL + Sequelize ORM
- JWT Authentication
- Socket.IO (real-time)
- Node-cron (automated rewards)

**Frontend**
- React 18 + Vite
- Tailwind CSS
- Zustand (state management)
- React Router
- Framer Motion

## 📁 Project Structure

```
telegram-rewards-app/
├── backend/           # Node.js API server
│   ├── controllers/   # Business logic
│   ├── models/        # Database models
│   ├── routes/        # API routes
│   ├── middleware/    # Auth & validation
│   └── scripts/       # Cron jobs & utilities
├── frontend/          # React application
│   └── src/
│       ├── components/
│       ├── pages/
│       ├── services/  # API client
│       └── store/     # State management
└── docs/              # Documentation
```

## 🎮 How It Works

### For Users

1. **Sign In** - Open Telegram bot → Web app launches → Auto-login
2. **Play Daily** - Complete 10-minute game to earn points
3. **Complete Tasks** - Subscribe to social channels for bonus points
4. **Invite Friends** - Share referral link for 500 points each
5. **Compete** - Climb the leaderboard in your level
6. **Win Prizes** - Top 10 users per level get cash every 15 days

### Reward Distribution

- **Level 1** (0-999 points): Top 10 get $3
- **Level 2** (1000-4999 points): Top 10 get $8 total
- **Level 3** (5000+ points): Top 10 get $18 total

Rewards are cumulative and distributed automatically via cron job.

## 🔧 Configuration

### Essential Environment Variables

**Backend (.env)**
```env
TELEGRAM_BOT_TOKEN=your_bot_token
DB_PASSWORD=your_postgres_password
JWT_SECRET=your_secret_key
```

**Frontend (.env)**
```env
VITE_API_URL=http://localhost:5000/api
```

See [.env.example](backend/.env.example) for all options.

## 🚢 Deployment

### Backend
```bash
# Production build
npm install --production
pm2 start server.js --name telegram-rewards

# Or use Docker
docker build -t telegram-rewards .
docker run -p 5000:5000 telegram-rewards
```

### Frontend
```bash
npm run build
# Deploy dist/ folder to Vercel, Netlify, or any static host
```

Full deployment guide in [documentation](docs/README.md#deployment).

## 🔐 Security

- ✅ JWT authentication with token expiration
- ✅ Telegram Web App data validation
- ✅ Rate limiting (100 req/15min)
- ✅ Input validation with Joi
- ✅ SQL injection protection (Sequelize ORM)
- ✅ XSS protection (React escaping)
- ✅ CORS configuration
- ✅ Helmet security headers

## 🧪 Testing

```bash
# Backend tests (coming soon)
cd backend && npm test

# Frontend tests (coming soon)
cd frontend && npm test
```

## 🗺️ Roadmap

- [x] Core gaming system
- [x] Social media integration
- [x] Referral system
- [x] Automated rewards
- [x] Admin panel
- [ ] Mobile apps (React Native)
- [ ] Payment automation
- [ ] Advanced analytics
- [ ] Multi-language support
- [ ] NFT rewards

## 🤝 Contributing

Contributions are welcome! Please read our contributing guidelines and submit pull requests.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

- 📧 Email: support@example.com
- 💬 Telegram: @YourSupportBot
- 🐛 Issues: [GitHub Issues](https://github.com/yourusername/telegram-rewards-app/issues)

## 🙏 Acknowledgments

- Inspired by Hamster Kombat
- Built for the Telegram community
- Powered by open-source technologies

---

**Made with ❤️ for gamers and entrepreneurs**

[⭐ Star this repo](https://github.com/yourusername/telegram-rewards-app) if you find it useful!
