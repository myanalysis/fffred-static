# fffred.info Static Site

Simple "Coming Soon" static site for fffred.info domain.

## Deployment to DigitalOcean App Platform

### Step 1: Add Domain to DigitalOcean DNS

1. Go to DigitalOcean Console → Networking → Domains
2. Click "Add Domain"
3. Enter: `fffred.info`
4. DigitalOcean will create default DNS records

### Step 2: Create App on App Platform

1. Go to DigitalOcean Console → Apps
2. Click "Create App"
3. Choose "GitHub" as source (or upload files)
4. Select this directory: `fffred-static/`
5. DigitalOcean will auto-detect it as a static site

### Step 3: Configure App

- **Name**: fffred-static
- **Region**: Singapore (SGP1) - same as your droplet
- **Plan**: Free tier (Starter - $0/month for static sites)

### Step 4: Add Custom Domain

After app is deployed:
1. Go to Settings → Domains
2. Add domain: `fffred.info`
3. DigitalOcean will provide DNS records to add

### Step 5: Update DNS Records

In DigitalOcean DNS for fffred.info:
1. Add CNAME record: `@` → `<your-app>.ondigitalocean.app`
2. Add CNAME record: `www` → `<your-app>.ondigitalocean.app`

DNS propagation can take up to 48 hours, but usually happens within 1-2 hours.

## Local Testing

Open `index.html` in a browser to preview the site.

## Files

- `index.html` - Single page static site with gradient background and "Coming Soon" message
