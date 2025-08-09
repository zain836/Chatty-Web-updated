# 🤖 Chatty Web - Advanced AI Chatbot Platform

A modern, full-stack AI chatbot platform built with React, Node.js, and multiple AI integrations. Features real-time chat, multiple AI personalities, advanced tools, and a sleek dark UI.

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![Node](https://img.shields.io/badge/node-%3E%3D16.0.0-green.svg)
![React](https://img.shields.io/badge/react-18.3.1-blue.svg)
![TypeScript](https://img.shields.io/badge/typescript-5.5.3-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## 🌟 Features

### 🤖 AI Chatbot
- **Multiple AI Personalities**: Mentor, Hacker, CEO, Therapist, Comedian
- **Google Gemini Integration**: Advanced AI responses
- **OpenAI Support**: GPT-4 integration ready
- **Demo Mode**: Works without API keys for testing

### 💬 Chat System
- **Real-time Messaging**: WebSocket-powered live chat
- **Conversation History**: Persistent chat sessions
- **Message Threading**: Organized conversation management
- **Voice Input**: Speech-to-text support

### 🛠️ Advanced Tools
- **Business Planner**: AI-powered business strategy generator
- **Script Writer**: Code generation utility
- **Payload Generator**: Security testing tools
- **PDF Generator**: Document creation

### 🔐 Security & Auth
- **JWT Authentication**: Secure token-based auth
- **User Management**: Registration, login, profiles
- **Rate Limiting**: API abuse protection
- **Stealth Mode**: Privacy disguise interface

### 🎨 Modern UI/UX
- **Dark Theme**: Cyberpunk aesthetic with neon accents
- **Responsive Design**: Mobile-first approach
- **PWA Support**: Progressive Web App features
- **Voice Interface**: Audio interactions

### 💰 Subscription System
- **Free Tier**: 15 messages per day
- **Premium Plans**: Unlimited usage
- **Payment Integration**: Razorpay/Stripe ready

---

## 📋 Prerequisites

Before running the application, ensure you have:

- **Node.js** (v16.0.0 or higher) - [Download here](https://nodejs.org/)
- **npm** (comes with Node.js)
- **Git** (optional, for cloning)

### Check your versions:
```bash
node --version    # Should be v16+
npm --version     # Should be v7+
```

---

## 🚀 Quick Start

### Option 1: One-Click Launch (Windows)
```batch
# Simply double-click or run:
start-app.bat
```

### Option 2: Manual Setup
```bash
# 1. Install frontend dependencies
npm install

# 2. Install backend dependencies
cd backend
npm install
cd ..

# 3. Start backend server (Terminal 1)
cd backend
npm run dev

# 4. Start frontend server (Terminal 2)
npm run dev
```

### 🌐 Access Your Application
- **Frontend**: http://localhost:5173
- **Backend API**: http://localhost:3001
- **API Documentation**: http://localhost:3001/api/docs
- **Health Check**: http://localhost:3001/health

---

## 📁 Project Structure

```
Chatty-Web-main/
├── 📁 backend/                     # Node.js Backend Server
│   ├── 📁 data/                    # SQLite Database Files
│   │   └── chatty_web_architect.db # Main Database
│   ├── 📁 src/                     # Backend Source Code
│   │   ├── 📁 config/              # Configuration Files
│   │   │   └── sqlite-database.js  # Database Setup & Queries
│   │   ├── 📁 middleware/          # Express Middleware
│   │   │   ├── authMiddleware.js   # JWT Authentication
│   │   │   └── errorMiddleware.js  # Error Handling
│   │   ├── 📁 routes/              # API Route Handlers
│   │   │   ├── authRoutes.js       # Authentication Endpoints
│   │   │   ├── chatRoutes.js       # Chat & AI Endpoints
│   │   │   ├── userRoutes.js       # User Management
│   │   │   ├── subscriptionRoutes.js # Subscription Management
│   │   │   ├── paymentRoutes.js    # Payment Processing
│   │   │   └── toolsRoutes.js      # Advanced Tools
│   │   ├── 📁 websocket/           # WebSocket Handlers
│   │   │   └── handler.js          # Real-time Communication
│   │   └── server.js               # Main Server Entry Point
│   ├── .env                        # Backend Configuration
│   ├── .env.example               # Environment Template
│   ├── package.json               # Backend Dependencies
│   └── swagger.yaml               # API Documentation
├── 📁 src/                        # React Frontend Source
│   ├── 📁 components/             # React Components
│   │   ├── 📁 ui/                 # Reusable UI Components
│   │   │   ├── button.tsx         # Custom Button Component
│   │   │   ├── card.tsx           # Card Component
│   │   │   ├── input.tsx          # Input Component
│   │   │   └── ...                # Other UI Components
│   │   ├── 📁 chatbot/            # Chatbot-Specific Components
│   │   │   ├── BusinessPlanner.tsx # Business Planning Tool
│   │   │   ├── ScriptWriter.tsx   # Code Generator
│   │   │   ├── StealthMode.tsx    # Privacy Mode
│   │   │   ├── VoiceInterface.tsx # Voice Input
│   │   │   └── SubscriptionModal.tsx # Subscription UI
│   │   ├── AuthProvider.tsx       # Authentication Context
│   │   ├── ChatWidget.tsx         # Main Chat Interface
│   │   ├── Navigation.tsx         # App Navigation
│   │   ├── HeroSection.tsx        # Landing Page Hero
│   │   ├── FeaturesSection.tsx    # Features Showcase
│   │   ├── PricingSection.tsx     # Pricing Plans
│   │   └── ...                    # Other Components
│   ├── 📁 pages/                  # Page Components
│   │   ├── Index.tsx              # Landing Page
│   │   ├── ChatbotPage.tsx        # Main Chat Interface
│   │   ├── AuthPage.tsx           # Login/Register
│   │   ├── PricingPage.tsx        # Pricing Plans
│   │   └── NotFound.tsx           # 404 Page
│   ├── 📁 services/               # API & Service Layers
│   │   ├── api.ts                 # API Client & Base Methods
│   │   ├── auth.ts                # Authentication Services
│   │   └── websocket.ts           # WebSocket Management
│   ├── 📁 integrations/           # External Integrations
│   │   └── 📁 auth/               # Auth Integration
│   │       ├── client.ts          # Auth Client
│   │       └── types.ts           # Auth Type Definitions
│   ├── 📁 lib/                    # Utility Libraries
│   │   └── utils.ts               # Helper Functions
│   ├── 📁 hooks/                  # Custom React Hooks
│   │   ├── use-mobile.tsx         # Mobile Detection
│   │   └── use-toast.ts           # Toast Notifications
│   ├── App.tsx                    # Main App Component
│   ├── main.tsx                   # Application Entry Point
│   ├── index.css                  # Global Styles & CSS Variables
│   └── vite-env.d.ts             # Vite Type Definitions
├── 📁 public/                     # Static Assets
│   ├── favicon.svg                # App Icon
│   ├── manifest.json              # PWA Manifest
│   └── ...                        # Images & Assets
├── 📁 dist/                       # Built Production Files
├── 📄 Configuration Files
│   ├── package.json               # Frontend Dependencies
│   ├── tsconfig.json              # TypeScript Configuration
│   ├── vite.config.ts             # Vite Build Configuration
│   ├── tailwind.config.ts         # Tailwind CSS Configuration
│   ├── postcss.config.js          # PostCSS Configuration
│   ├── eslint.config.js           # ESLint Configuration
│   ├── components.json            # Shadcn/UI Configuration
│   └── .env.local                 # Frontend Environment Variables
├── 📄 Startup Scripts
│   ├── start-app.bat              # One-click Windows Startup
│   ├── start-servers.bat          # Alternative Startup Script
│   ├── quick-start.bat            # Quick Development Start
│   └── start-development.ps1      # PowerShell Startup Script
├── 📄 Documentation
│   ├── README.md                  # This File
│   ├── COMPREHENSIVE_ANALYSIS_REPORT.md # Technical Analysis
│   ├── APPLICATION_STATUS.md      # Current Status Report
│   ├── SETUP_GUIDE.md             # Detailed Setup Guide
│   ├── TESTING_GUIDE.md           # Testing Instructions
│   ├── BACKEND_SETUP.md           # Backend-Specific Setup
│   └── FRONTEND_BACKEND_LINKING_ANALYSIS.md # Integration Guide
└── 📄 Other Files
    ├── docker-compose.yml         # Docker Configuration
    ├── .gitignore                 # Git Ignore Rules
    └── bun.lockb                  # Package Lock File
```

---

## ⚙️ Configuration

### Frontend Configuration (`.env.local`)
```env
# Backend API URL
VITE_BACKEND_URL=http://localhost:3001

# JWT Configuration
VITE_JWT_EXPIRY=3600

# Application Environment
VITE_APP_ENV=development
```

### Backend Configuration (`backend/.env`)
```env
# Server Configuration
PORT=3001
NODE_ENV=development

# Database Configuration (SQLite)
DB_HOST=localhost
DB_PORT=5432
DB_NAME=chatty_web_architect
DB_USER=postgres
DB_PASSWORD=password
DB_SSL=false

# AI API Keys (Optional - for full AI features)
OPENAI_API_KEY=sk-your-openai-api-key-here
GEMINI_API_KEY=your-gemini-api-key-here

# JWT Security
JWT_SECRET=your-super-secret-jwt-key-change-this-in-production
JWT_EXPIRES_IN=7d

# Rate Limiting
RATE_LIMIT_WINDOW=15
RATE_LIMIT_MAX_REQUESTS=100

# CORS Configuration
CORS_ORIGIN=http://localhost:5173,http://localhost:8080

# File Upload
MAX_FILE_SIZE=10485760
UPLOAD_PATH=./uploads

# Payment Integration (Optional)
RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_key_secret
STRIPE_SECRET_KEY=your_stripe_secret_key
```

---

## 🔑 Getting API Keys (Optional)

### For Full AI Chat Features:

#### Option 1: Google Gemini (Recommended)
1. Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Sign in with your Google account
3. Create a new API key
4. Add to `backend/.env`: `GEMINI_API_KEY=your-key-here`

#### Option 2: OpenAI GPT-4
1. Visit [OpenAI API Keys](https://platform.openai.com/api-keys)
2. Sign in and create a new API key
3. Add to `backend/.env`: `OPENAI_API_KEY=your-key-here`

**Note**: The application works in demo mode without API keys!

---

## 🖥️ Available Scripts

### Frontend Scripts
```bash
# Development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview

# Lint code
npm run lint

# Electron development
npm run electron:dev

# Build Electron app
npm run electron:build
```

### Backend Scripts
```bash
# Development server with hot reload
npm run dev

# Start production server
npm start

# Database setup
npm run setup-db

# Run tests
npm test

# Database migration
npm run migrate
```

---

## 🎮 Usage Guide

### 1. First Launch
1. Run the application using `start-app.bat`
2. Navigate to http://localhost:5173
3. Register a new account or use the demo account:
   - **Email**: developer@localhost
   - **Password**: password

### 2. Chat Features
- **Select AI Personality**: Choose from 5 different AI personalities
- **Send Messages**: Type and send messages to the AI
- **Voice Input**: Click microphone icon for voice input
- **Conversation History**: Access previous chat sessions

### 3. Advanced Tools
- **Business Planner**: Generate comprehensive business plans
- **Script Writer**: Create code snippets and scripts
- **Stealth Mode**: Enable privacy mode (Ctrl+Shift+S)
- **Voice Interface**: Use voice commands and responses

### 4. Account Management
- **Profile Settings**: Update your personal information
- **Subscription**: Upgrade to premium for unlimited usage
- **Chat History**: View and manage conversation history

---

## 🔧 Troubleshooting

### Common Issues & Solutions

#### Backend Won't Start
```bash
# Check if port 3001 is available
netstat -ano | findstr :3001

# Install dependencies
cd backend && npm install

# Check Node.js version
node --version  # Should be v16+
```

#### Frontend Won't Start
```bash
# Check if port 5173 is available
netstat -ano | findstr :5173

# Install dependencies
npm install

# Clear cache and reinstall
rm -rf node_modules package-lock.json
npm install
```

#### Database Issues
```bash
# Reset database (will lose data)
rm backend/data/chatty_web_architect.db

# Database will be recreated on next startup
```

#### Build Errors
```bash
# Clean build
npm run build -- --clean-cache

# Update dependencies
npm update
```

### Error Messages

| Error | Solution |
|-------|---------|
| `EADDRINUSE: port 3001` | Change PORT in `backend/.env` or stop other services |
| `Module not found` | Run `npm install` in the appropriate directory |
| `Database connection failed` | Check database configuration in `backend/.env` |
| `API key invalid` | Verify your API key in `backend/.env` |
| `Build failed` | Check TypeScript errors and run `npm run lint` |

---

## 🧪 Testing

### Manual Testing
1. **Registration**: Create a new user account
2. **Login**: Sign in with credentials
3. **Chat**: Send messages to different AI personalities
4. **Tools**: Test business planner and script writer
5. **Voice**: Try voice input functionality
6. **Mobile**: Test responsive design on mobile devices

### API Testing
```bash
# Health check
curl http://localhost:3001/health

# Test authentication
curl -X POST http://localhost:3001/api/auth/login \
  -H "Content-Type: application/json" \
  -d '{"email":"developer@localhost","password":"password"}'
```

---

## 🚀 Deployment

### Development Deployment
- Frontend runs on port 5173
- Backend runs on port 3001
- Database: SQLite (local file)

### Production Deployment
1. **Update Environment Variables**
   ```env
   NODE_ENV=production
   VITE_BACKEND_URL=https://your-domain.com
   ```

2. **Build Applications**
   ```bash
   # Build frontend
   npm run build
   
   # Backend is ready to run
   cd backend && npm start
   ```

3. **Database Migration**
   ```bash
   # For production, consider PostgreSQL
   npm run migrate
   ```

4. **Domain & SSL**
   - Configure your domain to point to the server
   - Set up SSL certificates (Let's Encrypt recommended)
   - Update CORS settings for production domain

---

## 🤝 Contributing

We welcome contributions! Here's how to get started:

1. **Fork the Repository**
2. **Create a Feature Branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. **Make Your Changes**
4. **Test Thoroughly**
5. **Submit a Pull Request**

### Development Guidelines
- Follow existing code style
- Add TypeScript types for new features
- Update documentation for new features
- Test on both mobile and desktop

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🆘 Support

### Getting Help
- **Issues**: Open an issue on GitHub
- **Documentation**: Check the `docs/` folder
- **Community**: Join our Discord server

### Contact
- **Email**: support@chatty-web.com
- **Website**: https://chatty-web.com
- **GitHub**: https://github.com/your-username/chatty-web

---

## 📊 Performance & Analytics

### Performance Metrics
- **Build Time**: ~5 seconds
- **Bundle Size**: 489KB (gzipped: 150KB)
- **First Load**: <2 seconds
- **API Response**: <100ms average

### Browser Support
- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+
- Mobile browsers (iOS Safari, Chrome Mobile)

---

## 🔮 Roadmap

### Upcoming Features
- [ ] Multi-language support
- [ ] Plugin system for custom tools
- [ ] Team collaboration features
- [ ] Advanced analytics dashboard
- [ ] Mobile app (React Native)
- [ ] Desktop app improvements
- [ ] Custom AI model training

---

## 🎉 Acknowledgments

### Built With Love Using:
- **React** - UI library
- **TypeScript** - Type safety
- **Node.js** - Backend runtime
- **Express** - Web framework
- **SQLite** - Database
- **Socket.io** - Real-time communication
- **Tailwind CSS** - Styling framework
- **Vite** - Build tool
- **Shadcn/UI** - Component library

### Special Thanks
- OpenAI for GPT-4 API
- Google for Gemini API
- All open-source contributors

---

**🚀 Ready to start chatting with AI? Launch your application now!**

```bash
# One command to rule them all
start-app.bat
```

**Happy Coding! 🎉**
#   C h a t t y - W e b - u p d a t e d  
 