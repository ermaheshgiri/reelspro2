# 🎥 ReelsPro - Video Sharing Platform

A modern video sharing platform built with Next.js 15, featuring video uploads, user authentication, and a TikTok-like video feed interface. Upload, share, and discover amazing video content in a sleek, responsive design.

## ✨ Features

- � **Modern Video Feed** - TikTok-style vertical video scrolling experience
- �🔐 **User Authentication** - Secure registration and login with NextAuth.js
- � **Video Upload** - Drag-and-drop video uploads with thumbnails using ImageKit
- 🎬 **Video Management** - Create, view, and manage your video content
- 📊 **Responsive Design** - Mobile-first design optimized for all devices
- �️ **Database Integration** - MongoDB with Mongoose for data persistence
- 🔒 **Security** - JWT authentication with password hashing
- � **Performance** - Optimized video loading and CDN delivery

## 🛠️ Tech Stack

- **Frontend**: Next.js 15, React 19, TypeScript
- **Styling**: Tailwind CSS, DaisyUI
- **Authentication**: NextAuth.js, JWT, bcryptjs
- **Database**: MongoDB, Mongoose
- **File Storage**: ImageKit (Video & Image CDN)
- **Form Handling**: React Hook Form
- **Icons**: Lucide React
- **Email**: Nodemailer

## 🚀 Quick Start

### Prerequisites

- Node.js 18+ installed
- MongoDB database (Atlas or local instance)
- ImageKit account for video/image storage

### Installation

1. **Clone and navigate to the project**
   ```bash
   git clone <repository-url>
   cd reelspro22
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Configuration**
   
   Create a `.env.local` file with these variables:
   
   ```env
   # Database
   MONGODB_URI=your_mongodb_connection_string
   
   # Authentication
   NEXTAUTH_SECRET=your_secret_key
   NEXTAUTH_URL=http://localhost:3000
   
   # ImageKit Configuration
   NEXT_PUBLIC_PUBLIC_KEY=your_imagekit_public_key
   IMAGEKIT_PRIVATE_KEY=your_imagekit_private_key
   NEXT_PUBLIC_URL_ENDPOINT=your_imagekit_url_endpoint
   ```

4. **Start development server**
   ```bash
   npm run dev
   ```

5. **Open in browser**
   
   Visit [http://localhost:3000](http://localhost:3000) to see your app

## 📁 Project Structure

```
reelspro22/
├── app/                    # Next.js App Router
│   ├── api/               # API Routes
│   │   ├── auth/          # Authentication endpoints
│   │   │   ├── [...nextauth]/  # NextAuth.js dynamic route
│   │   │   └── register/       # User registration
│   │   ├── imagekit-auth/ # ImageKit upload authentication
│   │   └── videos/        # Video CRUD operations
│   ├── components/        # React Components
│   │   ├── FileUpload.tsx      # Drag-drop file upload
│   │   ├── Header.tsx          # Navigation component
│   │   ├── Notification.tsx    # Toast notifications
│   │   ├── VideoFeed.tsx       # Main video feed
│   │   └── VideoUploadForm.tsx # Video upload form
│   ├── login/            # Login page
│   ├── register/         # User registration page
│   ├── upload/           # Video upload page
│   ├── layout.tsx        # Root layout
│   └── page.tsx          # Home page
├── lib/                  # Utility Libraries
│   ├── api-client.ts     # API client functions
│   ├── auth.ts           # NextAuth configuration
│   └── db.ts             # MongoDB connection
├── models/               # Database Models
│   ├── User.ts           # User schema
│   └── Video.ts          # Video schema
├── middleware.ts         # Next.js middleware
└── public/               # Static assets
```

## 🔧 Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run lint` - Run ESLint
- `npm run seed` - Seed database with sample data
- `npm run mailtrap` - Test email functionality

## 🎯 Key Features Overview

### 🔐 Authentication System
- User registration with email validation
- Secure login with JWT tokens
- Protected routes and API endpoints
- Password hashing with bcryptjs
- Session management with NextAuth.js

### 📹 Video Management
- Drag-and-drop video upload interface
- Real-time upload progress tracking
- Automatic thumbnail generation
- Video metadata management (title, description)
- ImageKit integration for optimized delivery

### 📱 Video Feed
- Infinite scroll video feed
- Mobile-responsive video player
- Touch-friendly interface
- Optimized video loading
- Social media-like interactions

### 🔒 Security Features
- Environment variable protection
- JWT token-based authentication
- Password encryption
- CORS protection
- Input validation and sanitization

## 🌐 API Endpoints

### Authentication
- `POST /api/auth/register` - Create new user account
- `GET /api/auth/[...nextauth]` - NextAuth.js authentication

### Videos
- `GET /api/videos` - Fetch all videos
- `POST /api/videos` - Upload new video
- `PUT /api/videos/:id` - Update video details
- `DELETE /api/videos/:id` - Delete video

### File Upload
- `GET /api/imagekit-auth` - Get upload authentication token

## 🎨 UI Components

- **VideoFeed**: Main component displaying video feed
- **VideoUploadForm**: Complete video upload interface
- **FileUpload**: Reusable drag-and-drop component
- **Header**: Navigation with user authentication
- **Notification**: Toast notification system
- **Providers**: Context providers for app state

## 🚀 Deployment Guide

### Build for Production
```bash
npm run build
npm start
```

### Deploy to Vercel (Recommended)
1. Connect repository to Vercel
2. Configure environment variables
3. Deploy automatically on push

### Other Deployment Options
- **Netlify**: Static site deployment
- **Railway**: Full-stack deployment
- **DigitalOcean**: App platform deployment
- **Heroku**: Container deployment

## 🔧 Development Tips

1. **Database Seeding**: Use `npm run seed` to populate with sample data
2. **Email Testing**: Use `npm run mailtrap` for email functionality testing  
3. **Environment**: Ensure all environment variables are properly configured
4. **ImageKit**: Set up ImageKit account for video storage
5. **MongoDB**: Use MongoDB Atlas for cloud database

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes
4. Commit changes (`git commit -m 'Add amazing feature'`)
5. Push to branch (`git push origin feature/amazing-feature`)
6. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - feel free to use it for your projects!

## 🆘 Support & Help

- **Issues**: Report bugs or request features via GitHub Issues
- **Documentation**: Check this README for setup instructions
- **Community**: Join discussions in the repository discussions section

## 🙏 Acknowledgments

- **Next.js** - Amazing React framework
- **ImageKit** - Powerful media processing and delivery
- **MongoDB** - Flexible NoSQL database
- **Tailwind CSS** - Utility-first CSS framework
- **DaisyUI** - Beautiful component library

---

**🚀 Built with modern web technologies for the best video sharing experience!**