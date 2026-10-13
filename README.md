# Ahmed Aly - Senior Mobile Developer Portfolio

A responsive personal portfolio showcasing Native Android and Flutter experience, production mobility applications, technical expertise, and professional experience.

## Project structure

```text
.
├── .github/
│   └── workflows/
│       └── deploy-pages.yml
├── assets/
│   ├── docs/
│   │   └── Ahmed_Aly_Senior_Mobile_Developer.pdf
│   └── images/
│       ├── shift-app-promo.png
│       └── shift-driver-promo.png
├── .gitignore
├── .nojekyll
├── index.html
└── README.md
```

## Preview locally

No package installation or build step is required.

```bash
python3 -m http.server 4173
```

Then open `http://localhost:4173`.

## Deploy to GitHub Pages

### 1. Create a repository

Create a new empty repository on GitHub. A name such as `portfolio` or `ahmed-aly-portfolio` works well.

### 2. Push this project

Run these commands from this directory, replacing the repository URL with your own:

```bash
git init
git add .
git commit -m "Launch portfolio"
git branch -M master
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin master
```

### 3. Enable GitHub Pages

1. Open the repository on GitHub.
2. Go to **Settings > Pages**.
3. Under **Build and deployment**, choose **GitHub Actions** as the source.
4. If the first deployment already failed with `Get Pages site failed: Not Found`, open the failed run and choose **Re-run all jobs**.
5. Open the **Actions** tab and wait for the `Deploy portfolio to GitHub Pages` workflow to finish.

The published URL will appear in the completed workflow and in **Settings > Pages**.

> GitHub Pages must be enabled once in the repository settings before the deployment action can publish the site. The standard workflow token cannot safely perform this first-time enablement on its own.

## Updating the portfolio

Edit `index.html` or replace files inside `assets`, then commit and push:

```bash
git add .
git commit -m "Update portfolio"
git push
```

Every push to `master` automatically deploys the latest version.

## Troubleshooting

### `Get Pages site failed: Not Found`

This means GitHub Pages is not enabled for the repository yet. Open **Settings > Pages**, select **GitHub Actions** under **Build and deployment**, save the setting, and re-run the failed workflow.

### Node.js 20 deprecation warning

The workflow uses `actions/configure-pages@v6` and `actions/deploy-pages@v5`, which run on Node.js 24. `actions/upload-pages-artifact@v4` remains the current upload action.

### `ubuntu-latest` migration warning

The workflow is pinned to `ubuntu-24.04`, so changes to the `ubuntu-latest` label will not alter this deployment unexpectedly.

