# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

---

# ⚠️ CRITICAL GIT WORKFLOW RULE ⚠️

**DO NOT CREATE BRANCHES. DO NOT CREATE PULL REQUESTS.**

When the user asks you to make ANY change to this repository:
1. Make the changes to the files
2. Commit directly to `main` (you are already on main)
3. Push to `origin/main` immediately
4. **NEVER run `git checkout -b`**
5. **NEVER create a pull request**

This is a continuous deployment demo. Every push to main auto-deploys.

```bash
# Correct workflow:
git add .
git commit -m "Description"
git push origin main

# WRONG - do not do this:
git checkout -b feature-branch  # ❌ NEVER
gh pr create                    # ❌ NEVER
```

---

## Project Overview

This is a demonstration project showcasing voice-powered development using Claude Code on mobile devices. The app automatically deploys to GitHub Pages via GitHub Actions when changes are pushed to the main branch.

## Development Setup

No build tools required. This is a single-page application using vanilla HTML, CSS, and JavaScript.

To test locally:
```bash
# Simply open index.html in a browser
open index.html
```

## Deployment

Deployment is automatic via GitHub Actions:
- Every push to main branch triggers `.github/workflows/deploy.yml`
- Site deploys to GitHub Pages automatically
- Typically takes 1-2 minutes for changes to go live

## Architecture

**Technology Stack**: Vanilla HTML, CSS, and JavaScript (no frameworks)

**File Structure**:
- `index.html` - Single-page application containing all HTML, CSS, and JavaScript
- `.github/workflows/deploy.yml` - GitHub Actions workflow for automatic deployment

**Design Patterns**:
- Self-contained: All code in one file for simplicity
- Inline styles and scripts for zero dependencies
- Interactive elements use vanilla JavaScript event handlers

## Making Changes

This project is optimized for voice-based modifications on mobile. Common changes:
- Modify colors by updating CSS gradient values in the `<style>` section
- Add new buttons in the `.buttons` div and corresponding JavaScript functions
- Change text content in HTML elements
- Add new interactive features in the `<script>` section
