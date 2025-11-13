# Mileage Tracker - React Version

**Live Demo:** [https://a4-aarogyarijal-a25.onrender.com](https://a4-aarogyarijal-a25.onrender.com)

## Project Description

Mileage Tracker is a full-stack web application that helps users track their vehicle fuel purchases and calculate fuel efficiency metrics. Users can securely log in with their GitHub account, add fuel purchase records (date, cost, gallons, and odometer reading), and view all their mileage data in an organized table format. The application automatically calculates the cost per gallon for each fuel purchase, making it easy to monitor fuel expenses over time.

This application was converted from a vanilla JavaScript implementation to a modern React-based single-page application with TypeScript, providing better code organization, type safety, and maintainability.

## Features

- **Secure Authentication**: GitHub OAuth integration using Passport.js for secure user authentication
- **Add Mileage Records**: Create new fuel purchase entries with date, cost, gallons, and total mileage
- **Edit Records**: Update existing mileage entries with new information
- **Delete Records**: Remove unwanted mileage records with confirmation
- **Automatic Calculations**: Calculates cost per gallon (CPG) automatically for each entry
- **Persistent Storage**: All data is stored in MongoDB and associated with the authenticated user
- **Responsive Design**: Clean, mobile-friendly interface using Bootstrap 5
- **Session Management**: Secure session handling with 24-hour cookie expiration

## Technology Stack

### Frontend
- **React 18.2.0**: Modern JavaScript library for building user interfaces
- **TypeScript 5.2.2**: Static typing for enhanced code quality and developer experience
- **Vite 7.1.7**: Fast build tool and development server with hot module replacement
- **Bootstrap 5.3.8**: CSS framework for responsive and modern UI design
- **React Hooks**: useState and useEffect for state management and side effects

### Backend
- **Node.js**: JavaScript runtime for server-side execution
- **Express.js 5.1.0**: Web application framework for Node.js
- **MongoDB 6.20.0**: NoSQL database for storing user mileage data
- **Passport.js 0.7.0**: Authentication middleware for Node.js
- **Passport-GitHub 1.1.0**: GitHub OAuth 2.0 authentication strategy
- **express-session 1.18.2**: Session middleware for Express
- **CORS 2.8.5**: Cross-Origin Resource Sharing middleware
- **dotenv 17.2.2**: Environment variable management

### DevOps & Tools
- **Concurrently 8.2.2**: Run multiple npm scripts simultaneously during development
- **Render**: Cloud platform for production deployment

## What Has Been Achieved

### Core Functionality
✅ **Full CRUD Operations**: Complete Create, Read, Update, Delete functionality for mileage records  
✅ **GitHub OAuth Authentication**: Secure login system using GitHub credentials  
✅ **User-specific Data**: Each user's mileage data is isolated and persistent  
✅ **Responsive UI**: Mobile-friendly interface that works on all screen sizes  
✅ **Type Safety**: TypeScript implementation for catching errors at compile time  
✅ **Production Deployment**: Live application deployed on Render platform

### Migration from Vanilla JS to React
✅ **Component Architecture**: Converted multiple HTML pages into a single, cohesive React component  
✅ **State Management**: Implemented React hooks (useState, useEffect) for managing application state  
✅ **Modern Build System**: Integrated Vite for fast development and optimized production builds  
✅ **TypeScript Integration**: Added type definitions for better code quality and IntelliSense support  
✅ **Maintained Functionality**: Preserved all original features while improving code structure

### Development Experience Improvements
✅ **Single Page Application**: Eliminated page reloads for smoother user experience  
✅ **Hot Module Replacement**: Instant feedback during development with Vite  
✅ **Better Code Organization**: Separation of concerns with modular component structure  
✅ **Type Safety**: TypeScript caught potential runtime errors during development  
✅ **Maintainability**: Cleaner, more readable codebase that's easier to extend

## Setup Instructions

### Prerequisites
- Node.js (v14 or higher)
- MongoDB database (local or cloud instance)
- GitHub OAuth App credentials

### Environment Variables
Create a `.env` file in the `/server` directory with the following:
```
GITHUB_CLIENT_ID=your_github_client_id
GITHUB_CLIENT_SECRET=your_github_client_secret
GITHUB_CALLBACK_URL=http://localhost:3000/auth/github/callback
MONGODB_URI=your_mongodb_connection_string
NODE_ENV=development
```

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/aarogyarijal/a4-AarogyaRijal-a25.git
   cd a4-AarogyaRijal-a25
   ```

2. **Install dependencies**
   ```bash
   npm run install-deps
   ```
   This installs dependencies for the root, server, and client directories.

3. **Run in development mode**
   ```bash
   npm run dev
   ```
   This runs both the Express server (port 3000) and Vite dev server (port 5173) concurrently.

4. **Build for production**
   ```bash
   npm run build
   ```
   This builds the React frontend into the `/client/dist` folder.

5. **Start production server**
   ```bash
   npm start
   ```
   Serves the built React app and API from the Express server on port 3000.

## Project Structure

```
a4-AarogyaRijal-a25/
├── client/               # React frontend application
│   ├── src/
│   │   ├── App.tsx      # Main React component
│   │   ├── App.css      # Component styles
│   │   ├── main.tsx     # React entry point
│   │   └── index.css    # Global styles
│   ├── index.html       # HTML template
│   ├── package.json     # Frontend dependencies
│   └── vite.config.ts   # Vite configuration
├── server/              # Express backend application
│   ├── routes/
│   │   ├── auth.js      # GitHub OAuth routes
│   │   └── index.js     # API routes for mileage data
│   ├── server.js        # Express server setup
│   ├── db.js            # MongoDB connection
│   └── package.json     # Backend dependencies
├── package.json         # Root package with dev scripts
└── README.md           # Project documentation
```

## API Endpoints

- `GET /api/user` - Get authenticated user information
- `GET /api/mileage` - Retrieve user's mileage records
- `POST /api/mileage` - Save/update mileage records
- `POST /api/logout` - Log out current user
- `GET /auth/github` - Initiate GitHub OAuth flow
- `GET /auth/github/callback` - GitHub OAuth callback

## Reflection: Did React Improve the Development Experience?

Converting the existing vanilla JavaScript application to React was more **tedious** than expected. Starting from scratch with React would have been significantly easier. However, the final result demonstrates several benefits:

**Pros:**
- Cleaner, more maintainable code structure
- TypeScript caught several potential bugs during development
- Better separation of concerns with component-based architecture
- Easier to extend with new features

**Cons:**
- Conversion process required significant refactoring effort
- Had to maintain exact same functionality, limiting design improvements
- More complex build setup compared to vanilla JS

**Conclusion:** While the conversion process was more work than the immediate benefits justified, the long-term maintainability and scalability improvements make React a better choice for this application.
