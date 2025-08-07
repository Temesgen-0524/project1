# DBU Student Union - Full Stack Application

A comprehensive student union management system for Debre Berhan University built with React frontend and Node.js/Express backend.

## Features

- **Student Authentication**: Login system with admin and student roles
- **Elections Management**: Create and manage student elections with voting functionality
- **Clubs & Associations**: Club registration, management, and member tracking
- **Complaints System**: Submit and track complaints with admin response system
- **News & Events**: Post and manage campus news, events, and announcements
- **Contact System**: Contact form with branch-specific routing
- **Admin Dashboard**: Comprehensive admin panel with role-based permissions

## Tech Stack

### Frontend
- React 18 with Vite
- Tailwind CSS for styling
- Framer Motion for animations
- React Router for navigation
- React Hot Toast for notifications
- Lucide React for icons

### Backend
- Node.js with Express
- MongoDB with Mongoose
- CORS enabled
- RESTful API architecture

## Getting Started

### Prerequisites
- Node.js (v16 or higher)
- MongoDB (local or cloud instance)
- npm or yarn

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd dbu-student-union
   ```

2. **Backend Setup**
   ```bash
   cd backend
   npm install
   
   # Create environment file
   cp .env.example .env
   # Edit .env with your MongoDB connection string
   
   # Start the backend server
   npm run dev
   ```

3. **Frontend Setup**
   ```bash
   cd project
   npm install
   
   # Start the frontend development server
   npm run dev
   ```

### Environment Variables

Create a `.env` file in the backend directory:

```env
MONGODB_URI=mongodb://localhost:27017/dbu_student_union
PORT=5000
JWT_SECRET=your_jwt_secret_key_here
NODE_ENV=development
```

## API Endpoints

### Users
- `GET /users` - Get all users
- `POST /users` - Create new user

### Complaints
- `GET /complaints` - Get all complaints
- `POST /complaints` - Submit new complaint

### Clubs
- `GET /clubs` - Get all clubs
- `POST /clubs` - Create new club

### Posts
- `GET /api/posts` - Get all posts
- `POST /api/posts` - Create new post

### Elections
- `GET /api/elections` - Get all elections
- `POST /api/elections` - Create new election
- `POST /api/elections/:id/vote` - Vote in election

### Contact
- `POST /api/contact` - Submit contact message

## Admin Credentials

For testing admin functionality, use these demo credentials:

- **President**: president@dbu.edu.et / admin123
- **Student Din**: studentdin@dbu.edu.et / admin123
- **Academic Affairs**: academic@dbu.edu.et / admin123
- **Clubs & Associations**: clubs@dbu.edu.et / admin123

## Project Structure

```
├── backend/
│   ├── models/          # MongoDB schemas
│   ├── routes/          # API routes
│   ├── config/          # Database configuration
│   └── server.js        # Main server file
├── project/
│   ├── src/
│   │   ├── components/  # React components
│   │   ├── contexts/    # React contexts
│   │   ├── data/        # Static data and mock data
│   │   ├── hooks/       # Custom React hooks
│   │   └── services/    # API service layer
│   └── public/          # Static assets
```

## Development

### Running in Development Mode

1. Start MongoDB service
2. Run backend: `cd backend && npm run dev`
3. Run frontend: `cd project && npm run dev`

The frontend will be available at `http://localhost:5173` and the backend API at `http://localhost:5000`.

### Building for Production

```bash
# Build frontend
cd project
npm run build

# Start backend in production
cd backend
npm start
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is licensed under the ISC License.