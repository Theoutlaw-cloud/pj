# Setup Guide

## Prerequisites

- Node.js 18+ and npm
- PostgreSQL 12+
- Git

## Installation

### 1. Clone the repository
```bash
git clone https://github.com/Theoutlaw-cloud/pj.git
cd pj
```

### 2. Install dependencies
```bash
npm install
```

### 3. Setup environment variables

#### Backend
```bash
cp backend/.env.example backend/.env
# Edit backend/.env with your database credentials
```

#### Database
```bash
# Create database
createdb financial_app

# Run migrations
psql -U postgres -d financial_app -f backend/src/schemas/init.sql
```

### 4. Start development servers

```bash
npm run dev
```

This will start:
- Frontend: http://localhost:3000
- Backend: http://localhost:5000

## Project Structure

- **frontend/** - React application with TypeScript and Tailwind CSS
- **backend/** - Express.js API server
- **database/** - Database schemas and migrations
- **docs/** - Documentation

## Available Scripts

- `npm run dev` - Start both frontend and backend in development mode
- `npm run build` - Build both frontend and backend
- `npm run test` - Run tests for both projects
- `npm run lint` - Lint both projects

## Features to Implement

- [ ] User Authentication (JWT)
- [ ] Transaction Management API
- [ ] Budget Management API
- [ ] Reports and Analytics
- [ ] User Dashboard
- [ ] Data Visualization
- [ ] Export Reports (PDF, CSV)
