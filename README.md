# JOBS-APP | Full-Stack Job Tracking Platform

A comprehensive job application tracking system built with the MERN stack, featuring user authentication, job management, and analytics dashboard.

## Tech Stack

**Backend:**
- Node.js & Express.js
- MongoDB with Mongoose ODM
- JWT Authentication
- Express middleware for error handling

**Frontend:**
- React 18 with Redux Toolkit
- Chart.js for analytics visualization
- Responsive CSS design

## Features

- **User Authentication:** Register, login with JWT tokens
- **Job Management:** Create, read, update, delete job applications
- **Search & Filter:** Advanced job filtering and pagination
- **Analytics Dashboard:** Visual charts and statistics
- **Responsive Design:** Mobile-friendly interface

## Project Structure

```
├── app.js                 # Express server entry point
├── controllers/           # Route handlers
│   ├── auth.js           # Authentication logic
│   └── jobs.js           # Job operations
├── models/               # MongoDB schemas
│   ├── User.js           # User model
│   └── Job.js            # Job model
├── middleware/           # Express middleware
│   ├── authentication.js # JWT verification
│   └── error-handler.js  # Error handling
├── routes/               # API routes
│   ├── auth.js           # Authentication routes
│   └── jobs.js           # Job routes
├── client/               # React frontend
│   ├── src/              # React source code
│   └── build/            # Production build
└── db/                   # Database configuration
    └── connect.js        # MongoDB connection
```

## Installation

```bash
# Clone repository
git clone <repository-url>
cd JOBS-APP

# Install backend dependencies
npm install

# Install frontend dependencies
cd client
npm install
cd ..

# Create .env file
echo "MONGO_URI=your_mongodb_connection_string" > .env
echo "JWT_SECRET=your_jwt_secret" >> .env
echo "JWT_LIFETIME=30d" >> .env
```

## Development

```bash
# Start backend server (port 5000)
npm run dev

# Start frontend development server (port 3000)
cd client
npm start
```

## Production Build

```bash
# Build React client
cd client
npm run build
cd ..

# Start production server
npm start
```

## API Endpoints

### Authentication
- `POST /api/v1/auth/register` - User registration
- `POST /api/v1/auth/login` - User login

### Jobs
- `GET /api/v1/jobs` - Get all jobs (with pagination/filtering)
- `POST /api/v1/jobs` - Create new job
- `GET /api/v1/jobs/:id` - Get single job
- `PATCH /api/v1/jobs/:id` - Update job
- `DELETE /api/v1/jobs/:id` - Delete job
- `GET /api/v1/jobs/stats` - Get job statistics

## Environment Variables

```
MONGO_URI=mongodb://localhost:27017/jobs-app
JWT_SECRET=your-secret-key
JWT_LIFETIME=30d
```

## Deployment

The application includes a `Procfile` for Heroku deployment and serves the React build from the Express server in production.

## License

Private project - All rights reserved.

---

Built with ❤️ by Ivan Duarte | ByteUp LLC