# 🚀 PolkaSEC Frontend - Quick Start

## ✅ What's Already Created

All frontend files have been created! The complete React + TypeScript application is ready.

## 📋 Setup Steps

### Step 1: Install Dependencies

**Option A: Use the setup script**
```powershell
cd "C:\Users\hanah\Polkadot Project\polkasec-frontend"
.\setup.ps1
```

**Option B: Manual installation**
```powershell
cd "C:\Users\hanah\Polkadot Project\polkasec-frontend"
npm install
```

### Step 2: Make Sure Backend is Running

**In a separate terminal:**
```powershell
cd "C:\Users\hanah\Polkadot Project\polkasec-backend"
venv\Scripts\activate
python main.py
```

The backend should be running on **http://localhost:8000**

### Step 3: Start Frontend Development Server

```powershell
cd "C:\Users\hanah\Polkadot Project\polkasec-frontend"
npm run dev
```

You should see:
```
VITE v5.x.x  ready in xxx ms

➜  Local:   http://localhost:3000/
```

### Step 4: Open in Browser

Open **http://localhost:3000** in your browser.

## 🎯 What You'll See

- **Dashboard** with real-time security alerts
- **Chain Status** panel showing monitored chains
- **Threat Analytics** with charts and statistics
- **Alert Feed** with live WebSocket updates
- **Demo Button** to simulate attacks

## 🔧 Troubleshooting

### "Cannot connect to backend"

**Check:**
1. Backend is running on port 8000
2. No firewall blocking connections
3. Check browser console for errors

**Test backend:**
```powershell
Invoke-RestMethod -Uri "http://localhost:8000/health" -Method Get
```

### "Module not found" errors

**Fix:**
```powershell
npm install
```

### Port 3000 already in use

**Fix:** Change port in `vite.config.ts`:
```typescript
server: {
  port: 3001,  // Change to different port
  // ...
}
```

### WebSocket connection failed

**Check:**
1. Backend WebSocket endpoint is working
2. Vite proxy is configured correctly
3. Check browser console for WebSocket errors

## 📁 Project Structure

```
polkasec-frontend/
├── src/
│   ├── components/
│   │   ├── Dashboard.tsx      # Main dashboard
│   │   ├── AlertFeed.tsx      # Alert list
│   │   ├── ChainStatus.tsx    # Chain monitoring
│   │   ├── AlertStats.tsx     # Statistics & charts
│   │   └── DemoButton.tsx      # Demo attack button
│   ├── lib/
│   │   ├── api.ts             # REST API client
│   │   └── websocket.ts        # WebSocket client
│   ├── types/
│   │   └── index.ts            # TypeScript types
│   ├── App.tsx
│   ├── main.tsx
│   └── index.css               # Tailwind styles
├── package.json
├── vite.config.ts              # Vite configuration
└── tailwind.config.js          # Tailwind configuration
```

## 🎨 Features

- ✅ Real-time alerts via WebSocket
- ✅ Responsive dark theme UI
- ✅ Interactive charts with Recharts
- ✅ Chain status monitoring
- ✅ MITRE ATT&CK technique display
- ✅ Demo attack simulation

## 🚀 Next Steps

1. ✅ Install dependencies: `npm install`
2. ✅ Start backend: `python main.py` (in backend folder)
3. ✅ Start frontend: `npm run dev` (in frontend folder)
4. ✅ Open browser: http://localhost:3000
5. ✅ Click "⚡ Demo Attack" to test!

Enjoy your PolkaSEC Security Operations Center! 🔐

