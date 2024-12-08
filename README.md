# Hosting Playwright Reports on GitHub Pages

This README explains how to host Playwright reports on GitHub Pages, enabling you to share your test results publicly or within your team. Follow these steps to set up automatic deployment of Playwright reports to GitHub Pages using GitHub Actions.

## Prerequisites

- A GitHub repository with Playwright tests configured.
- GitHub Actions enabled for your repository.
- A basic understanding of Playwright and GitHub Pages.

## Steps to Host Reports

### 1. Generate Playwright Reports

Ensure your Playwright tests are configured to generate an HTML report. Update the `playwright.config.ts` file if needed:

```javascript
import { defineConfig } from '@playwright/test';

export default defineConfig({
  reporter: 'html',
});
```

### 2. Set Up GitHub Pages

1. Navigate to your repository on GitHub.
2. Go to **Settings > Pages**.
3. Under "Source," select the branch and folder where the reports will be deployed (e.g., `gh-pages` branch or `/root` folder).
4. Click **Save**.

### 3. ...

WIP
