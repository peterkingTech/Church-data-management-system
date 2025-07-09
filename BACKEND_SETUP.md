# 🚀 Complete Backend Setup Guide for Church Management System

## 📋 Overview
This guide will help you set up a complete backend for your Church Management System using Supabase, ensuring all data persists and files are properly stored.

## 🎯 What You'll Get
- **Persistent Data Storage**: No more data loss when refreshing
- **PDF File Management**: Upload, store, and manage PDF files
- **Real-time Sync**: Multiple users can collaborate in real-time
- **Secure Access**: Church-based data isolation and user permissions
- **Professional Hosting**: Deploy anywhere with confidence

## 🔧 Step 1: Create Supabase Account (5 minutes)

### 1.1 Sign Up for Supabase
1. Go to [supabase.com](https://supabase.com)
2. Click "Start your project"
3. Sign up with GitHub, Google, or email
4. **It's completely FREE** for small churches!

### 1.2 Create New Project
1. Click "New Project"
2. Choose your organization (or create one)
3. Fill in project details:
   - **Name**: `church-management-system`
   - **Database Password**: Generate a strong password (save it!)
   - **Region**: Choose closest to your location
4. Click "Create new project"
5. **Wait 2-3 minutes** for setup to complete

## 📊 Step 2: Set Up Database Schema (10 minutes)

### 2.1 Access SQL Editor
1. In your Supabase dashboard, click "SQL Editor" in the sidebar
2. Click "New query"

### 2.2 Run Migration Files
Copy and paste each migration file from the `supabase/migrations/` folder:

#### Migration 1: PDF Files Table
```sql
-- Copy content from: supabase/migrations/20250707075116_sweet_ocean.sql
-- Paste into SQL Editor and click "Run"
```

#### Migration 2: Core Tables (if needed)
```sql
-- Copy content from other migration files in the migrations folder
-- Run each one separately
```

### 2.3 Enable Storage
1. Go to "Storage" in the sidebar
2. Click "Create a new bucket"
3. Name: `pdf-files`
4. Set as **Public bucket**
5. Click "Create bucket"

## 🔑 Step 3: Get API Keys (2 minutes)

### 3.1 Find Your Keys
1. Go to "Settings" → "API" in your Supabase dashboard
2. Copy these values:
   - **Project URL** (starts with `https://`)
   - **Anon/Public Key** (starts with `eyJ`)

### 3.2 Create Environment File
Create a `.env` file in your project root:

```env
# Supabase Configuration
VITE_SUPABASE_URL=https://your-project-id.supabase.co

VITE_SUPABASE_ANON_KEY=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...your-anon-key-here

# App Configuration
VITE_APP_NAME=Church Management System
VITE_CHURCH_NAME=Your Church Name
VITE_SUPPORT_EMAIL=support@yourchurch.com
VITE_SUPPORT_PHONE=+1-555-123-4567
```

**⚠️ Important**: Replace the placeholder values with your actual Supabase URL and key!

## 🚀 Step 4: Deploy Your App (10 minutes)

### Option A: Netlify (Recommended - Free)

#### 4.1 Build Your App
```bash
npm run build
```

#### 4.2 Deploy to Netlify
1. Go to [netlify.com](https://netlify.com)
2. Sign up/login
3. Drag and drop your `dist` folder to the deploy area
4. Your app is live instantly!

#### 4.3 Add Environment Variables
1. Go to your site dashboard on Netlify
2. Click "Site settings" → "Environment variables"
3. Add each variable from your `.env` file:
   - `VITE_SUPABASE_URL`
   - `VITE_SUPABASE_ANON_KEY`
   - etc.
4. Redeploy your site

### Option B: Vercel (Alternative - Free)

#### 4.1 Install Vercel CLI
```bash
npm install -g vercel
```

#### 4.2 Deploy
```bash
vercel --prod
```

#### 4.3 Add Environment Variables
```bash
vercel env add VITE_SUPABASE_URL
vercel env add VITE_SUPABASE_ANON_KEY
# Add other variables...
```

### Option C: Traditional Hosting

#### 4.1 Build and Upload
```bash
npm run build
# Upload contents of 'dist' folder to your web host
```

#### 4.2 Configure Environment
- Add environment variables through your hosting provider's control panel
- Or create a `.env.production` file (not recommended for security)

## ✅ Step 5: Test Your Setup (5 minutes)

### 5.1 Test Database Connection
1. Open your deployed app
2. Try logging in with demo credentials
3. Create a test program or folder
4. Refresh the page - data should persist!

### 5.2 Test PDF Upload
1. Go to any module (Folders, Programs, etc.)
2. Try uploading a PDF file
3. Verify it appears in the file list
4. Test viewing and deleting files

### 5.3 Test Multi-User Access
1. Open your app in different browsers/devices
2. Log in with different user roles
3. Make changes in one browser
4. Refresh the other browser - changes should sync!

## 🔒 Step 6: Security & Production Setup

### 6.1 Row Level Security (Already Configured)
- Each church's data is isolated
- Users can only access their church's information
- Role-based permissions are enforced

### 6.2 Backup Strategy
1. **Automatic Backups**: Supabase provides automatic daily backups
2. **Manual Backup**: Go to "Settings" → "Database" → "Backups"
3. **Export Data**: Use the SQL Editor to export specific tables

### 6.3 Custom Domain (Optional)
1. **Netlify**: Go to "Domain settings" → "Add custom domain"
2. **Vercel**: Go to "Domains" → "Add domain"
3. **Traditional**: Point your domain to your hosting provider

## 📈 Step 7: Monitoring & Maintenance

### 7.1 Monitor Usage
- **Supabase Dashboard**: Check database usage, API calls
- **Storage Usage**: Monitor file storage limits
- **Performance**: Check query performance in SQL Editor

### 7.2 Scaling Options
- **Free Tier**: Up to 500MB database, 1GB storage
- **Pro Tier**: $25/month for larger churches
- **Team Tier**: $599/month for multiple churches

### 7.3 Regular Maintenance
- **Weekly**: Check error logs and performance
- **Monthly**: Review storage usage and cleanup old files
- **Quarterly**: Update dependencies and security patches

## 🆘 Troubleshooting

### Common Issues & Solutions

#### "Supabase not configured" Error
- **Cause**: Environment variables not set correctly
- **Solution**: Double-check your `.env` file and deployment environment variables

#### PDF Upload Fails
- **Cause**: Storage bucket not created or wrong permissions
- **Solution**: Recreate the `pdf-files` bucket and run storage policies

#### Data Not Syncing
- **Cause**: Database connection issues
- **Solution**: Check Supabase project status and API keys

#### Migration Errors
- **Cause**: Tables already exist or permission issues
- **Solution**: Use `IF NOT EXISTS` clauses and check user permissions

### Getting Help
1. **Supabase Docs**: [supabase.com/docs](https://supabase.com/docs)
2. **Community**: [github.com/supabase/supabase/discussions](https://github.com/supabase/supabase/discussions)
3. **Support**: Contact through Supabase dashboard

## 🎉 Success! Your Church Management System is Live

### What You've Accomplished:
- ✅ **Professional Backend**: Enterprise-grade database and storage
- ✅ **Persistent Data**: No more data loss or resets
- ✅ **File Management**: Upload and manage PDF documents
- ✅ **Multi-User Support**: Real-time collaboration
- ✅ **Secure Access**: Church-based data isolation
- ✅ **Production Ready**: Deployed and accessible worldwide

### Next Steps:
1. **Train Your Team**: Share the user manual with church staff
2. **Import Data**: Add your existing church members and programs
3. **Customize**: Update church information and branding
4. **Scale**: Invite more users and departments

### Cost Breakdown:
- **Supabase**: FREE for most churches (up to 500MB database)
- **Hosting**: FREE on Netlify/Vercel
- **Domain**: $10-15/year (optional)
- **Total**: $0-15/year for a professional church management system!

---

**🎯 Your Church Management System is now production-ready with persistent data storage, file management, and professional hosting!**

**Powered by AMEN TECH** - Building systems that serves God's kingdom (Matthew 6:33)

© 2025 AMEN TECH. All rights reserved.