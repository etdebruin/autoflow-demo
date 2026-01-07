# AutoFlow Demo

A demonstration of voice-powered development using Claude Code on mobile devices with automatic deployment via GitHub Actions.

## What This Demo Shows

1. **Voice Commands on Mobile**: Use Claude Code on your phone to make changes to the app by speaking
2. **Automatic Deployment**: Changes are committed and automatically deployed to GitHub Pages
3. **Live Updates**: See your changes live within seconds

## Setup Instructions

### 1. Enable GitHub Pages

1. Go to your repository settings on GitHub
2. Navigate to **Pages** (under "Code and automation")
3. Under "Build and deployment":
   - **Source**: Select "GitHub Actions"
4. Save the settings

### 2. Push Your Code

```bash
git add .
git commit -m "Initial demo setup"
git push origin main
```

The GitHub Action will automatically deploy your site to: `https://[your-username].github.io/autoflow-demo/`

## Using Claude Code on Mobile

### Important: Direct Commits (Not PRs)

For this demo to work smoothly, you want Claude Code to commit directly to `main` and push (not create a PR).

**How to do this:**
- Be explicit in your voice commands that you want to commit and push
- Stay on the `main` branch
- Don't mention "PR" or "pull request"

### Example Voice Commands

Try these commands with Claude Code on your phone:

- "Change the background gradient to ocean blue and teal, then commit and push it"
- "Add a random quote button and push the change to main"
- "Change the emoji to a rocket and deploy it"
- "Make the counter start at 100, commit it"
- "Add a confetti effect when clicking increment and push it"
- "Change the heading color to gold and commit the change"

**Pro tip**: End your requests with "and push it" or "and commit it" to avoid being asked about creating a PR.

## How It Works

1. Speak to Claude Code on your mobile device
2. Claude Code makes the requested changes to `index.html`
3. Changes are committed to the repository
4. GitHub Actions automatically deploys to GitHub Pages
5. Refresh the page to see your changes live

## Project Structure

```
.
├── index.html              # Main page with HTML, CSS, and JavaScript
├── .github/
│   └── workflows/
│       └── deploy.yml      # GitHub Actions deployment workflow
└── README.md               # This file
```

## Local Development

Simply open `index.html` in your browser. No build step required!
