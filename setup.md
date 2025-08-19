# Quick Setup Guide

## 🚨 Environment Variable Issue Resolved

The error you encountered was because the `vercel.json` file was referencing non-existent secrets. This has been fixed.

## ✅ Correct Setup Steps

### 1. Local Development
```bash
# Install dependencies
npm install

# Copy environment template
cp .env.local.example .env.local

# Edit .env.local with your Supabase credentials
# NEXT_PUBLIC_SUPABASE_URL=https://your-project.supabase.co
# NEXT_PUBLIC_SUPABASE_ANON_KEY=your-anon-key

# Start development server
npm run dev
```

### 2. Vercel Deployment
1. **Push to Git** (GitHub, GitLab, etc.)
2. **Import to Vercel** - Connect your repository
3. **Add Environment Variables** in Vercel project settings:
   - `NEXT_PUBLIC_SUPABASE_URL` = Your Supabase project URL
   - `NEXT_PUBLIC_SUPABASE_ANON_KEY` = Your Supabase anon key
4. **Select all environments** (Production, Preview, Development)
5. **Deploy!**

## 🔧 What Was Fixed

- Removed incorrect secret references from `vercel.json`
- Environment variables are now set directly in Vercel project settings
- No need to create Vercel secrets

## 📍 Supabase Setup

1. Go to [supabase.com](https://supabase.com) and create a project
2. Run the SQL from `supabase-schema.sql` in the SQL Editor
3. Get your credentials from Settings → API
4. Copy the URL and anon key to your environment variables

## 🚀 Ready to Deploy!

Your application is now properly configured for both local development and Vercel deployment.
