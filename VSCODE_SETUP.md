# 🚀 VSCode Complete Setup & Running Guide for NeuroLearn AI

## 📋 Prerequisites

Before starting, ensure you have installed:

1. **Node.js** (v18 or higher)
   - Download: https://nodejs.org/
   - Verify: `node --version` (should be v18+)

2. **npm** (comes with Node.js)
   - Verify: `npm --version`

3. **Git**
   - Download: https://git-scm.com/
   - Verify: `git --version`

4. **VSCode**
   - Download: https://code.visualstudio.com/

---

## 🔧 VSCode Extensions (Recommended)

Install these extensions for better development experience:

1. **ES7+ React/Redux/React-Native snippets**
   - Search: `ES7+ React/Redux`
   - By: dsznajder.es7-react-js-snippets

2. **Prettier - Code formatter**
   - Search: `Prettier`
   - By: esbenp.prettier-vscode

3. **ESLint**
   - Search: `ESLint`
   - By: dbaeumer.vscode-eslint

4. **Thunder Client** (API testing)
   - Search: `Thunder Client`
   - By: rangav.vscode-thunder-client

5. **MongoDB for VS Code**
   - Search: `MongoDB`
   - By: mongodb.mongodb-vscode

6. **REST Client**
   - Search: `REST Client`
   - By: humao.rest-client

7. **TypeScript Vue Plugin**
   - Search: `TypeScript Vue`
   - By: Vue.volar

8. **Error Lens**
   - Search: `Error Lens`
   - By: usernamehw.errorlens

---

## 📂 Step 1: Clone the Repository

### Option A: Using VSCode Terminal

1. Open VSCode
2. Press `Ctrl + ~` (or `Cmd + ~` on Mac) to open terminal
3. Navigate to where you want the project:
   ```bash
   cd Desktop
   # or
   cd Documents
   ```

4. Clone the repository:
   ```bash
   git clone https://github.com/vh12878cse23-droid/neurolearn-ai.git
   cd neurolearn-ai
   ```

### Option B: Using VSCode UI

1. Open VSCode
2. Click `File` → `Open Folder`
3. Navigate to your desired location
4. Open VSCode terminal: `Ctrl + ~`
5. Run:
   ```bash
   git clone https://github.com/vh12878cse23-droid/neurolearn-ai.git
   cd neurolearn-ai
   code .
   ```

---

## 🔐 Step 2: Get API Keys

Before running, you need these API keys:

### 1. OpenAI API Key
- Go to: https://platform.openai.com/api-keys
- Create new secret key
- Copy the key (you won't see it again!)
- Keep it safe

### 2. MongoDB Atlas
- Go to: https://www.mongodb.com/cloud/atlas
- Create free account
- Create cluster
- Get connection string:
  - Clusters → Connect → Drivers → MongoDB URI
  - Copy the URI
  - Replace `<password>` with your password

### 3. ElevenLabs API Key (Optional)
- Go to: https://elevenlabs.io
- Sign up
- Get API key from Profile → API Key

### 4. Google OAuth (Optional for now)
- Go to: https://console.cloud.google.com
- Create new project
- Enable Google+ API
- Create OAuth credentials
- Get Client ID and Secret

---

## 🏗️ Step 3: Setup Backend

### 3.1 Open Backend Folder in Terminal

In VSCode terminal, navigate to backend:

```bash
cd backend
```

### 3.2 Install Dependencies

```bash
npm install
```

**Wait for installation to complete** (takes 2-3 minutes)

### 3.3 Create Environment File

```bash
# Copy example env file
cp .env.example .env
```

Or manually:
1. Right-click in `/backend` folder
2. Create new file: `.env`
3. Copy content from `.env.example`
4. Paste into `.env`

### 3.4 Edit `.env` File

Click on `.env` in VSCode and fill in your values:

```env
# Database
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/neurolearn

# JWT Secrets
JWT_SECRET=your-super-secret-key-min-32-chars-long!@#$
JWT_EXPIRE=7d
REFRESH_TOKEN_EXPIRE=30d

# OpenAI
OPENAI_API_KEY=sk-your-actual-key-here

# ElevenLabs (optional)
ELEVENLABS_API_KEY=your-key-here
ELEVENLABS_VOICE_ID=21m00Tcm4TlvDq8ikWAM

# Google OAuth (optional)
GOOGLE_OAUTH_ID=your-id-here
GOOGLE_OAUTH_SECRET=your-secret-here

# Server
NODE_ENV=development
PORT=5000
FRONTEND_URL=http://localhost:3000
```

### 3.5 Run Backend Server

In VSCode terminal (in backend folder):

```bash
npm run dev
```

You should see:
```
✓ Server running on http://localhost:5000
✓ Connected to MongoDB
✓ Socket.io initialized
```

**Leave this running! Don't close the terminal.**

---

## 💻 Step 4: Setup Frontend

### 4.1 Open New Terminal

In VSCode:
- Click `Terminal` → `New Terminal`
- Or press `Ctrl + Shift + ~`

### 4.2 Navigate to Frontend

```bash
cd frontend
```

### 4.3 Install Dependencies

```bash
npm install
```

**Wait for installation** (takes 2-3 minutes)

### 4.4 Create Environment File

```bash
cp .env.example .env.local
```

Or manually create `.env.local` in `/frontend` folder

### 4.5 Edit `.env.local`

```env
NEXT_PUBLIC_API_URL=http://localhost:5000
NEXT_PUBLIC_WS_URL=http://localhost:5000
NEXT_PUBLIC_APP_NAME=NeuroLearn AI
```

### 4.6 Run Frontend Server

In your frontend terminal:

```bash
npm run dev
```

You should see:
```
▲ Next.js 15.0.0
- ready started server on 0.0.0.0:3000, url: http://localhost:3000
```

---

## ✅ Step 5: Access the Application

Open your browser and go to:

```
http://localhost:3000
```

You should see the **NeuroLearn AI Landing Page** with:
- Beautiful hero section
- Features showcase
- Navigation bar
- CTA buttons

---

## 📱 Full Terminal Setup (Copy-Paste Ready)

### Terminal 1 - Backend:
```bash
cd backend
npm install
cp .env.example .env
# Edit .env with your API keys
npm run dev
```

### Terminal 2 - Frontend:
```bash
cd frontend
npm install
cp .env.example .env.local
npm run dev
```

Then open: `http://localhost:3000`

---

## 🧪 Testing the Application

### Test Landing Page
- ✅ Visit `http://localhost:3000`
- ✅ Scroll through features
- ✅ Check responsive design (F12 → toggle device toolbar)

### Test Signup
- ✅ Click "Sign Up" button
- ✅ Fill form with:
  - Email: `test@example.com`
  - First Name: `Test`
  - Last Name: `User`
  - Password: `Test@1234`
- ✅ Click Submit
- ✅ Should redirect to login or dashboard

### Test Login
- ✅ Click "Login"
- ✅ Use credentials from signup
- ✅ Should show dashboard

### Test Dashboard
- ✅ View analytics charts
- ✅ Check study hours graph
- ✅ View achievements

---

## 🐛 Troubleshooting

### Problem: `npm install` fails

**Solution:**
```bash
# Clear cache
npm cache clean --force

# Delete node_modules and package-lock.json
rm -rf node_modules
rm package-lock.json

# Reinstall
npm install
```

### Problem: Port 5000 already in use

**Solution:**
```bash
# On Windows
netstat -ano | findstr :5000
taskkill /PID <PID> /F

# On Mac/Linux
lsof -i :5000
kill -9 <PID>
```

### Problem: Port 3000 already in use

**Solution:**
```bash
# On Windows
netstat -ano | findstr :3000
taskkill /PID <PID> /F

# On Mac/Linux
lsof -i :3000
kill -9 <PID>
```

### Problem: MongoDB connection fails

**Solution:**
1. Check `MONGODB_URI` in `.env`
2. Verify MongoDB cluster IP whitelist:
   - Go to MongoDB Atlas
   - Network Access
   - Add your IP (0.0.0.0/0 for development)

### Problem: "Cannot find module" errors

**Solution:**
```bash
# Clear node_modules
rm -rf node_modules
npm install

# Type check
npm run type-check
```

### Problem: TypeScript errors

**Solution:**
```bash
npm run type-check
```

---

## 📊 VSCode Debugging

### Setup Debugger for Backend

Create `.vscode/launch.json`:

```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Attach to Backend",
      "type": "node",
      "request": "attach",
      "port": 9229,
      "skipFiles": ["<node_internals>/**"],
      "outFiles": ["${workspaceFolder}/backend/dist/**/*.js"]
    },
    {
      "name": "Launch Backend",
      "type": "node",
      "request": "launch",
      "program": "${workspaceFolder}/backend/src/server.ts",
      "restart": true,
      "runtimeArgs": [
        "--loader",
        "ts-node/esm"
      ],
      "env": {
        "NODE_ENV": "development"
      }
    }
  ]
}
```

To use:
1. Click Debug icon (Ctrl + Shift + D)
2. Select "Launch Backend"
3. Click green play button

---

## 🔍 VSCode Useful Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl + ~` | Toggle terminal |
| `Ctrl + Shift + ~` | New terminal |
| `Ctrl + P` | Quick file open |
| `Ctrl + Shift + F` | Search in files |
| `Ctrl + /` | Comment/uncomment |
| `Alt + Up/Down` | Move line up/down |
| `Shift + Alt + Up/Down` | Duplicate line |
| `F12` | Go to definition |
| `Ctrl + Shift + D` | Open Debugger |

---

## 📝 Common Commands Reference

```bash
# Frontend
npm run dev              # Start development server
npm run build            # Build for production
npm run start            # Start production server
npm run lint             # Run ESLint
npm run type-check       # Type check TypeScript
npm test                 # Run tests

# Backend
npm run dev              # Start with hot reload
npm run build            # Build TypeScript
npm start                # Run production build
npm run type-check       # Type check
npm test                 # Run tests
```

---

## 🚀 Development Workflow

1. **Start Both Servers:**
   ```bash
   # Terminal 1
   cd backend && npm run dev
   
   # Terminal 2
   cd frontend && npm run dev
   ```

2. **Make Changes:**
   - Edit files in VSCode
   - Both servers auto-reload
   - Check terminal for errors

3. **Test in Browser:**
   - Open `http://localhost:3000`
   - DevTools: F12

4. **View API Logs:**
   - Check backend terminal for requests
   - Look for errors in console

5. **Debug Issues:**
   - Check browser console (F12)
   - Check VSCode terminal output
   - Check `.env` configuration

---

## 📚 Useful Resources

- **Next.js Docs**: https://nextjs.org/docs
- **Express.js Docs**: https://expressjs.com/
- **MongoDB Docs**: https://docs.mongodb.com/
- **TypeScript Docs**: https://www.typescriptlang.org/docs/
- **Tailwind CSS**: https://tailwindcss.com/docs
- **OpenAI API**: https://platform.openai.com/docs

---

## ✨ Next Steps After Setup

1. ✅ Test the landing page
2. ✅ Create a test account
3. ✅ Explore the dashboard
4. ✅ Check browser DevTools for API calls
5. ✅ Review code structure
6. ✅ Start implementing features

---

## 🎯 You're All Set! 🎉

Your NeuroLearn AI development environment is ready!

**Quick Summary:**
- ✅ Backend running on `http://localhost:5000`
- ✅ Frontend running on `http://localhost:3000`
- ✅ MongoDB connected
- ✅ Hot reload enabled
- ✅ Ready for development!

**Happy Coding!** 🚀
