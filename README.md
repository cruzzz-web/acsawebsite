# ACSA Studios - Roblox Group Website

A modern, multi-purpose website for tracking and managing the ACSA Studios Roblox group with dark/light theme support, user authentication, and real-time game statistics.

## Features

- 🌓 **Dark/Light Theme Toggle** - Beautiful theme switching with smooth transitions
- 🔐 **Roblox Account Authentication** - Secure login system with role-based access
- 👥 **User Role Management** - Special access for Owner and Manager roles
- 🎮 **Game Tracking** - Real-time display of active players and visits
- 📊 **Group Statistics** - View group members, total games, and player counts
- 🎯 **Game Details** - Detailed information pages for each game
- 💾 **Local Data Storage** - Login credentials stored securely on your system

## Special Users

- **SILVERWOODGAMERZ_YT** - Owner (full access)
- **blcruz2m** - Manager (full access)

## Installation

1. Install dependencies:
```bash
npm install
```

2. Create a `.env` file in the root directory (optional, for production):
```
JWT_SECRET=your-secret-key-here
PORT=5000
```

3. Ensure the login data directory exists:
   - The directory `C:\Users\Somegh\OneDrive\Documents\Desktop\acsa website login data\` will be created automatically
   - Login credentials are stored as JSON files in this directory

## Running the Application

Start both the frontend and backend servers:
```bash
npm run dev
```

This will start:
- Frontend (React + Vite) on `http://localhost:3000`
- Backend (Express) on `http://localhost:5000`

## Project Structure

```
├── server/              # Backend Express server
│   ├── routes/         # API routes
│   │   ├── auth.js     # Authentication endpoints
│   │   ├── roblox.js   # Roblox API integration
│   │   └── games.js    # Game data endpoints
│   └── index.js        # Server entry point
├── src/                # Frontend React application
│   ├── components/     # React components
│   ├── context/        # React context providers
│   └── App.jsx         # Main app component
└── package.json        # Dependencies and scripts
```

## API Endpoints

### Authentication
- `POST /api/auth/login` - Login with username and password
- `GET /api/auth/verify` - Verify JWT token

### Roblox Data
- `GET /api/roblox/group` - Get group information
- `GET /api/roblox/group/games` - Get all games in the group
- `GET /api/roblox/game/:gameId` - Get detailed game information

### Games
- `GET /api/games/active` - Get all games with active player counts

## Usage

1. Navigate to `http://localhost:3000`
2. Login with your Roblox username and password
3. View the dashboard with all active games
4. Click on any game to see detailed information
5. Toggle between dark and light themes using the button in the top-right corner

## Notes

- Login data is stored locally in JSON format
- The website automatically refreshes game data every 30 seconds
- Game details refresh every 10 seconds
- Special users (Owner/Manager) have elevated permissions (currently displayed as badges)

## Technologies Used

- **Frontend**: React, Vite, React Router
- **Backend**: Node.js, Express
- **Styling**: CSS with CSS Variables for theming
- **Authentication**: JWT (JSON Web Tokens)
- **API**: Roblox Public APIs

