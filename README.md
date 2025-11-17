# PolkaSEC Frontend

Modern React + TypeScript frontend for Polkadot Security Operations Center.

## Quick Start

### Prerequisites
- Node.js 18+ and npm
- Backend server running on http://localhost:8000

### Installation

1. **Install dependencies:**
   ```powershell
   npm install
   ```

2. **Start development server:**
   ```powershell
   npm run dev
   ```

3. **Open browser:**
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:8000

## Features

- 🔴 Real-time security alerts via WebSocket
- 📊 Threat analytics dashboard with charts
- ⛓️ Chain status monitoring
- 🎯 MITRE ATT&CK technique mapping
- 🎨 Modern dark theme UI

## Project Structure

```
polkasec-frontend/
├── src/
│   ├── components/      # React components
│   │   ├── Dashboard.tsx
│   │   ├── AlertFeed.tsx
│   │   ├── ChainStatus.tsx
│   │   ├── AlertStats.tsx
│   │   └── DemoButton.tsx
│   ├── lib/            # API and WebSocket clients
│   │   ├── api.ts
│   │   └── websocket.ts
│   ├── types/           # TypeScript definitions
│   │   └── index.ts
│   ├── App.tsx
│   ├── main.tsx
│   └── index.css
├── package.json
└── vite.config.ts
```

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build

## API Integration

The frontend uses Vite's proxy to connect to the backend:
- API requests: `/api/*` → `http://localhost:8000/api/*`
- WebSocket: `/ws/*` → `ws://localhost:8000/ws/*`

## Tech Stack

- **React 18** - UI framework
- **TypeScript** - Type safety
- **Vite** - Build tool
- **Tailwind CSS** - Styling
- **Recharts** - Data visualization
- **Lucide React** - Icons

