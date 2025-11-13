# Cron Jobs Repository

Centralized GitHub Actions workflows for scheduled tasks across multiple projects.

## Why This Repo?

- **Free Unlimited Minutes**: Public repos get unlimited GitHub Actions minutes
- **Centralized Management**: All scheduled jobs in one place
- **Keep Services Alive**: Prevent free-tier services from spinning down
- **Scheduled Tasks**: Run periodic maintenance, scraping, and monitoring

## Current Jobs

### Irish Mortgage API

- **Keep-Alive**: Pings API every 5 minutes (24/7) to prevent Render free tier spin-down
- **Daily Scrape**: Triggers fresh mortgage rate scraping at 2 AM UTC daily

**API URL**: https://irish-mortgage-api.onrender.com

## Setup

### Required Secrets

Configure these in **Settings → Secrets and variables → Actions**:

| Secret Name | Description | Example |
|------------|-------------|---------|
| `MORTGAGE_API_KEY` | Irish Mortgage API authentication key | `sk_live_xxxxx...` |

### Adding Secrets

1. Go to this repo's Settings
2. Navigate to **Secrets and variables → Actions**
3. Click **New repository secret**
4. Add each secret from the table above

## Usage

The workflows run automatically on schedule. You can also trigger them manually:

1. Go to **Actions** tab
2. Select the workflow
3. Click **Run workflow**

## Monitoring

Check the **Actions** tab to see:
- Workflow run history
- Success/failure status
- Execution logs

## Adding More Projects

To add scheduled jobs for other projects:

1. Create a new workflow file in `.github/workflows/`
2. Define the schedule and tasks
3. Add any required secrets
4. Commit and push

## Cost

**$0/month** - Public repositories get unlimited GitHub Actions minutes.
