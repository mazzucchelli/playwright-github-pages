# Hosting Playwright Reports on GitHub Pages

This README explains how to host Playwright reports on GitHub Pages, enabling you to share your test results publicly or within your team. The following workflow will:

 - Generate the reports and host them in GitHub Pages every time a new PR is created or updated
 - Automatically comment the PR with the report URL
 - Delete the report once the branch is deleted

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

1. Create a new orphan branch 

  ```
    git checkout --orphan gh-pages
    git rm -rf .
    git commit --allow-empty -m "setup empty branch for GitHub Pages"
    git push --set-upstream origin gh-pages
  ```

2. Navigate to your repository on GitHub.
3. Go to **Settings > Pages**.
4. Select `Deploy from a branch` and set `gh-pages` as branch

### 3. Update the test job with a publish step

1. See `.github/workflows/playwright-pull-request.yml` file as reference (remember to update the report URL defined in the last 3 steps with your `owner` and `repo`)

### 3. Create a new action

1. See `.github/workflows/playwright-delete-reports.yml` file as reference
