# MJL Chat System

## Quick Installation

```bash
curl -fsSL https://raw.githubusercontent.com/MikeJoshuaLopena4/MJL_ChatSystem/main/install.sh | sudo bash
```

## Manual Installation

### Prerequisites
- Docker
- Docker Compose
- Git
- Node.js 18+

### Steps

1. Clone the repository:
```bash
git clone https://github.com/MikeJoshuaLopena4/MJL_ChatSystem.git
cd MJL_ChatSystem
```

2. Set up environment files:

Client (.env.local):
```bash
SERVER_IP=https://localhost
HOSTNAME=localhost
PORT=3000
NEXT_PUBLIC_API_BASE_URL=https://localhost:5000
NEXT_PUBLIC_SOCKET_SERVER_URL=https://localhost:5000
NEXT_PUBLIC_PORT=3000
```

Server (.env):
```bash
ALLOWED_ORIGINS=https://localhost,https://localhost:5000,http://localhost:3000
PORT=5000
SSL_KEY_PATH=./ssl/localhost-key.pem
SSL_CERT_PATH=./ssl/localhost.pem
NEXT_PUBLIC_SOCKET_SERVER_URL=https://localhost:5000
FRONTEND_URL=http://localhost:3000
MONGO_CHAT_URI=mongodb://mongodb:27017/chatDB
MONGO_SYSTEM_URI=mongodb://mongodb:27017/systemDB
MONGO_AUTH_URI=mongodb://mongodb:27017/authDB
JWT_SECRET=your_secret_here
JWT_EXPIRES_IN=7d
```

3. Start with Docker:
```bash
docker-compose up -d
```

## Development

### Client
```bash
cd client
npm install
npm run dev
```

### Server
```bash
cd server
npm install
npm run dev
```

## Structure
```
.
├── client/                   # Next.js frontend
├── server/                   # Express backend
│   ├── nginx/               # Nginx configuration
│   └── ssl/                 # SSL certificates
├── mongodb/                 # MongoDB configuration
├── docker-compose.yml       # Docker compose configuration
└── README.md               # Project documentation
```

## Features
- Real-time chat
- User authentication
- Dark/Light mode
- Weather integration
- Attendance tracking

## Technologies
- Next.js
- Express
- MongoDB
- Socket.IO
- Docker
- Nginx

## License
MIT License
