# ReelsPro Deployment Guide

This repository contains the ReelsPro video sharing platform. The main application is located in the `reelspro22` directory.

## Repository Structure

```
reelspro2/
├── reelspro22/          # Main Next.js application
│   ├── package.json     # App dependencies
│   ├── next.config.ts   # Next.js configuration
│   └── ...              # Application code
├── package.json         # Root package.json for deployment
├── render.yaml          # Render.com deployment config
└── README.md           # This file
```

## Deployment Instructions

### Render.com Deployment

1. **Connect Repository**: Connect this GitHub repository to Render.com

2. **Service Configuration**:
   - **Build Command**: `cd reelspro22 && npm install && npm run build`
   - **Start Command**: `cd reelspro22 && npm start`
   - **Root Directory**: Leave as default (root)
   - **Node.js Version**: 18.17.0

3. **Environment Variables** (Required):
   ```
   MONGODB_URI=your_mongodb_connection_string
   NEXTAUTH_SECRET=your_secret_key
   NEXTAUTH_URL=https://your-app-name.onrender.com
   NEXT_PUBLIC_PUBLIC_KEY=your_imagekit_public_key
   IMAGEKIT_PRIVATE_KEY=your_imagekit_private_key
   NEXT_PUBLIC_URL_ENDPOINT=your_imagekit_url_endpoint
   ```

### Alternative Deployment Options

#### Vercel (Recommended)
1. Set **Root Directory** to `reelspro22`
2. Framework preset will auto-detect Next.js
3. Add environment variables in Vercel dashboard

#### Netlify
1. Set **Build command**: `cd reelspro22 && npm run build`
2. Set **Publish directory**: `reelspro22/.next`
3. Add environment variables in Netlify dashboard

#### Railway
1. Set **Root Directory** to `reelspro22`
2. Railway will auto-detect Next.js configuration
3. Add environment variables in Railway dashboard

## Local Development

To run locally:

```bash
# Clone repository
git clone https://github.com/ermaheshgiri/reelspro2.git
cd reelspro2

# Navigate to app directory
cd reelspro22

# Install dependencies
npm install

# Start development server
npm run dev
```

## Environment Variables Template

Create a `.env.local` file in the `reelspro22` directory:

```env
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/database
NEXTAUTH_SECRET=your-super-secret-key-here
NEXTAUTH_URL=http://localhost:3000
NEXT_PUBLIC_PUBLIC_KEY=your_imagekit_public_key
IMAGEKIT_PRIVATE_KEY=your_imagekit_private_key
NEXT_PUBLIC_URL_ENDPOINT=https://ik.imagekit.io/your-endpoint/
```

## Troubleshooting

### Common Deployment Issues

1. **Package.json not found**: Ensure build commands include `cd reelspro22`
2. **Environment variables**: Verify all required env vars are set
3. **Build failures**: Check Node.js version compatibility (use 18.x)
4. **Database connection**: Ensure MongoDB URI is accessible from deployment platform

### Build Command Examples

- **Render**: `cd reelspro22 && npm install && npm run build`
- **Vercel**: Auto-detected (set root directory to `reelspro22`)
- **Netlify**: `cd reelspro22 && npm run build`

### Start Command Examples

- **Render**: `cd reelspro22 && npm start`
- **Railway**: `npm start` (with root directory set)