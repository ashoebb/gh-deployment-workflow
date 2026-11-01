# gh-deployment-workflow

A static site deployed to GitHub Pages by a GitHub Actions workflow. Built as a roadmap.sh DevOps project.

## Project page

https://roadmap.sh/projects/github-actions-deployment-workflow

## Live site

https://ashoebb.github.io/gh-deployment-workflow/

## How it works

- `index.html` is the site.
- `.github/workflows/deploy.yml` runs on every push to `main` that changes `index.html`, and can also be started by hand from the Actions tab.
- The workflow copies `index.html` into a `_site` folder, uploads it as a Pages artifact, and deploys it with `actions/deploy-pages`. Only the site file is published, not the repo.
- A push that changes only other files (such as this README) does not trigger a deployment.

## Setup

In the repository, open Settings, then Pages, and set Source to **GitHub Actions**.
