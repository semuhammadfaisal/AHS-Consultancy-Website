# Vercel Deployment Guide

## Quick Deploy Steps:

### 1. Install Vercel CLI (if not installed)
```bash
npm i -g vercel
```

### 2. Deploy from Project Directory
```bash
cd AHS-Consultancy&Training-Website
vercel --prod
```

### 3. Follow Prompts:
- Set up and deploy? **Y**
- Which scope? **Select your account**
- Link to existing project? **N**
- Project name? **ahs-consultancy** (or your choice)
- Directory? **./** (current directory)
- Override settings? **N**

### Alternative: GitHub Deploy
1. Push code to GitHub repository
2. Go to https://vercel.com
3. Click "New Project"
4. Import your GitHub repository
5. Deploy automatically

## Test Email After Deployment:
1. Visit your live Vercel URL
2. Fill out the contact form
3. Submit and check faisalsb0348@gmail.com
4. Verify email delivery works on live site

## Current Configuration:
- EmailJS Public Key: `C0s6AJJhqkEqzPfti`
- Service ID: `service_wo3b3um`
- Template ID: `template_2d3l98h`
- Target Email: `faisalsb0348@gmail.com`

## Push Updates:

### Method 1: Vercel CLI (Recommended)
```bash
vercel --prod
```

### Method 2: GitHub Auto-Deploy
```bash
git add .
git commit -m "Update website"
git push origin main
```
*Auto-deploys if connected to GitHub*

### Method 3: Drag & Drop
1. Go to vercel.com dashboard
2. Click your project
3. Drag updated folder to redeploy

## Troubleshooting:
- If emails don't work on live site, check browser console for errors
- Verify EmailJS domain restrictions in dashboard
- Test form submission and check network tab for failed requests