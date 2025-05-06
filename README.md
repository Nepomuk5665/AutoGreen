# AutoGreen

A simple repository that automatically makes GitHub contributions to keep your graph green.

## What it does

- Makes 69 initial commits to populate your contribution graph
- Sets up a GitHub Action to automatically commit daily
- Uses the commit message: "A commit a day keeps the Girlfriend away"

## Setup Instructions

1. Clone this repository or create a new one with these files
2. Run the setup script:
   ```
   ./one-time-setup.sh
   ```
3. Create a new repository on GitHub
4. Connect and push your repository:
   ```
   git remote add origin https://github.com/YOUR-USERNAME/autogreen.git
   git branch -M main
   git push -u origin main
   ```

## How it works

- The GitHub Actions workflow (`.github/workflows/autogreen.yml`) runs automatically every day at 08:00 UTC
- It creates a new commit with a timestamp in the contributions.txt file
- The GitHub contribution graph counts these commits as activity

## Customization

- To change the schedule, edit the cron expression in `.github/workflows/autogreen.yml`
- The default is `0 8 * * *` which runs at 08:00 UTC daily