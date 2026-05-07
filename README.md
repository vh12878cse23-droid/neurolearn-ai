# NeuroLearn AI - Smart AI Study Companion 🧠

A production-ready AI-powered EdTech platform combining modern frontend, scalable backend, real-time features, and intelligent AI integrations.

## 🎯 Features

### Core Features
- **AI Video Teacher**: AI-generated explanations with visual diagrams
- **Voice & Visual Explanations**: Speech recognition + text-to-speech responses
- **Emotion Detection**: Real-time emotion recognition via webcam
- **Pomodoro Study Timer**: Customizable focus sessions with analytics
- **AI Quiz Generator**: Dynamic quiz creation from topics/PDFs
- **Gamification System**: Streaks, XP, badges, leaderboards
- **Smart Analytics Dashboard**: Real-time study metrics and insights
- **Real-time Chat**: Live AI tutor with streaming responses

### Advanced Features
- AI Notes Summarizer
- PDF Question Answering
- Smart Revision Planner
- Study Calendar
- AI Flashcards
- Multi-language Support
- Voice-controlled Navigation
- AI Motivation Quotes
- Focus Music Integration
- Career Guidance

## 🛠 Tech Stack

### Frontend
- **Framework**: Next.js 15
- **Language**: TypeScript
- **Styling**: Tailwind CSS + Framer Motion
- **UI Components**: ShadCN UI
- **State Management**: Zustand + React Query
- **Real-time**: Socket.io Client
- **Charts**: Recharts
- **AI/ML**: TensorFlow.js, face-api.js, MediaPipe

### Backend
- **Runtime**: Node.js
- **Framework**: Express.js
- **Language**: TypeScript
- **Database**: MongoDB Atlas
- **ORM**: Mongoose
- **Auth**: JWT + OAuth 2.0
- **Real-time**: Socket.io
- **API Security**: Helmet, CORS, Rate Limiting

### AI & Integrations
- **LLM**: OpenAI API / Google Gemini
- **Voice**: ElevenLabs Text-to-Speech
- **Speech Recognition**: Web Speech API / Whisper API
- **Emotion Detection**: face-api.js + TensorFlow.js
- **Image Processing**: MediaPipe
- **Cloud Storage**: Cloudinary
- **OAuth**: Google
- **Payments**: Stripe (optional)

### Deployment
- **Frontend**: Vercel
- **Backend**: Render / Railway
- **Database**: MongoDB Atlas
- **CI/CD**: GitHub Actions

## 📁 Project Structure

```
neurolearn-ai/
├── frontend/                 # Next.js application
│   ├── app/                 # App router pages
│   ├── components/          # Reusable components
│   ├── hooks/              # Custom React hooks
│   ├── lib/                # Utilities and helpers
│   ├── public/             # Static assets
│   ├── store/              # Zustand state management
│   ├── services/           # API service layer
│   ├── styles/             # Global styles
│   └── package.json
│
├── backend/                 # Express.js API
│   ├── src/
│   │   ├── controllers/    # Request handlers
│   │   ├── routes/         # API routes
│   │   ├── models/         # Mongoose schemas
│   │   ├── middleware/     # Express middleware
│   │   ├── services/       # Business logic
│   │   ├── sockets/        # Socket.io handlers
│   │   ├── config/         # Configuration
│   │   ├── utils/          # Utility functions
│   │   └── server.ts       # Entry point
│   ├── .env.example
│   └── package.json
│
├── docs/                    # Documentation
├── .github/                 # GitHub Actions
└── README.md
```

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- npm or yarn
- MongoDB Atlas account
- OpenAI API key
- ElevenLabs API key

### Frontend Setup
```bash
cd frontend
npm install
cp .env.example .env.local
npm run dev
```

Access at: http://localhost:3000

### Backend Setup
```bash
cd backend
npm install
cp .env.example .env
npm run dev
```

API running at: http://localhost:5000

## 📝 Environment Variables

See `.env.example` files in both frontend and backend directories.

### Key Variables
```
MONGODB_URI=your_mongodb_atlas_uri
JWT_SECRET=your_jwt_secret
OPENAI_API_KEY=your_openai_key
ELEVENLABS_API_KEY=your_elevenlabs_key
GOOGLE_OAUTH_ID=your_google_oauth_id
GOOGLE_OAUTH_SECRET=your_google_oauth_secret
CLOUDINARY_API_KEY=your_cloudinary_key
```

## 📊 Database Models

- **User**: Student profiles, settings, authentication
- **Quiz**: AI-generated and custom quizzes
- **StudySession**: Pomodoro sessions and focus metrics
- **EmotionLog**: Real-time emotion detection data
- **PomodoroSession**: Timer sessions with analytics
- **Achievement**: Badges and milestones
- **Leaderboard**: Global rankings
- **AIConversation**: Chat history with AI tutor
- **Notes**: User study notes and summaries
- **Recommendations**: AI-powered suggestions

## 🔐 Authentication

- JWT-based authentication
- Refresh token rotation
- Password hashing with bcrypt
- Google OAuth 2.0
- Protected API routes
- Email verification
- Rate limiting

## 🎨 UI Features

- Modern glassmorphism design
- Animated neural network background
- Dark/Light mode support
- Smooth page transitions
- Loading skeletons
- Interactive hover effects
- Responsive design (mobile-first)
- Accessible components
- Beautiful typography

## 📱 Main Pages

1. **Landing Page** - Hero, features, testimonials, pricing
2. **Authentication** - Login, signup, OAuth, password recovery
3. **Dashboard** - Analytics, streaks, recommendations
4. **AI Teacher** - Chat interface, explanations, voice
5. **Emotion Detection** - Real-time mood analysis
6. **Pomodoro Timer** - Study sessions, history
7. **Quiz System** - AI-generated quizzes, leaderboards
8. **Profile** - Settings, achievements, certificates

## ⚡ Real-time Features

- Live AI chat streaming
- Real-time quiz updates
- Live leaderboard updates
- Study session notifications
- Emotion detection live feed

## 🧪 Testing

```bash
# Frontend tests
cd frontend
npm run test

# Backend tests
cd backend
npm run test
```

## 📦 Deployment

### Frontend (Vercel)
```bash
cd frontend
vercel deploy
```

### Backend (Render/Railway)
```bash
cd backend
# Push to your platform
```

### Environment Setup
- Add environment variables to platform dashboards
- Configure MongoDB Atlas IP whitelist
- Setup CI/CD pipelines

## 🤝 Contributing

1. Create a feature branch
2. Commit your changes
3. Push to branch
4. Create Pull Request

## 📄 License

MIT License - see LICENSE file

## 📧 Support

For issues and questions, create an issue in the GitHub repository.

## 🎯 Roadmap

- [ ] Mobile app (React Native)
- [ ] Advanced AI tutoring
- [ ] Group study sessions
- [ ] Institution dashboard
- [ ] Advanced analytics
- [ ] API marketplace

---

**Built with ❤️ for students worldwide**
