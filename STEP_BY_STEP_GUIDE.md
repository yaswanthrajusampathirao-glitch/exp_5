# Experiment 5 Step-by-Step Execution Guide

### Step 1: Initialize Git and Create Feature Branch
```bash
git init
git checkout -b main
# (If using remote): git pull origin main
git checkout -b feature/add-calculator
```

### Step 2: Add Code and Tests
- `src/calc.py` created
- `tests/test_calc.py` created

### Step 3 & Step 9: Configure GitHub Actions Workflow (Testing + Linting)
- `.github/workflows/ci.yml` created with Python 3.11, flake8 linting, and pytest execution.

### Step 4: Commit and Push Feature Branch
```bash
git add .
git commit -m "Add calculator with CI workflow"
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin feature/add-calculator
```

### Step 5: Open a Pull Request
- Navigate to your repository on GitHub.
- Open a PR from `feature/add-calculator` into `main`.
- Observe the automated check run under the PR's **Checks** tab.

### Step 6: Configure Branch Protection Rules for `main`
- Go to repository **Settings** -> **Branches**.
- Click **Add branch ruleset** or **Add rule**.
- Set branch pattern to `main`.
- Check **Require a pull request before merging** (Require approvals: 1).
- Check **Require status checks to pass before merging** and search/select `test`.

### Step 7: Review and Merge
- Request review from a collaborator.
- Ensure the CI check turns green.
- Merge the Pull Request into `main`.

### Step 8: Add Status Badge to README
- In `README.md`, update the badge URL with your actual username and repository name:
  `![CI](https://github.com/<username>/<repo>/actions/workflows/ci.yml/badge.svg)`

### Step 10: Clean up Feature Branch
```bash
git checkout main
git pull origin main
git branch -d feature/add-calculator
git push origin --delete feature/add-calculator
```
