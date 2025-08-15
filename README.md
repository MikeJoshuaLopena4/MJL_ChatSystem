# MJL_ChatSystem

## Overview
Brief description of your project

## Prerequisites
- Docker
- Docker Compose
- Git

## Quick Start

1. Clone the repository:
```bash
git clone https://github.com/yourusername/yourproject.git
cd yourproject
```

2. Create necessary environment files:

For client (.env.local):
```bash
SERVER_IP=https://localhost
HOSTNAME=localhost
PORT=3000
NEXT_PUBLIC_API_BASE_URL=https://localhost:5000
NEXT_PUBLIC_SOCKET_SERVER_URL=https://localhost:5000
NEXT_PUBLIC_PORT=3000
```

For server (.env):
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

3. Generate SSL certificates:
```bash
mkcert localhost
```
Move the generated certificates to `server/ssl/`

4. Start the application:
```bash
docker-compose up -d
```

5. Access the application:
- Frontend: https://localhost:3000
- Backend: https://localhost:5000

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

## Directory Structure
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
- Feature 1
- Feature 2
- Feature 3

## Technologies
- Next.js
- Express
- MongoDB
- Socket.IO
- Docker
- Nginx

## Contributing
Instructions for contributing to your project

## License
MIT License or your chosen license
