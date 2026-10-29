# Experiment 5 - Viva Questions & Answers

1. **Compare Git Flow and GitHub Flow.**
   - *Git Flow*: Features long-lived branches (`main`, `develop`, `release`, `hotfix`). Suitable for scheduled release cycles.
   - *GitHub Flow*: Lightweight, branch-based workflow where short-lived feature branches branch off and merge directly back into `main` via Pull Requests. Designed for continuous deployment.

2. **What are branch protection rules and why are they used?**
   - Quality gates enforced on a remote branch (like `main`) to prevent direct pushes, require code reviews from peers, and block merges until automated status checks (CI tests/linters) pass.

3. **What triggers a GitHub Actions workflow?**
   - GitHub webhook events configured in the `on:` block of the workflow YAML, such as `push`, `pull_request`, scheduled triggers (`schedule`), or manual triggers (`workflow_dispatch`).

4. **What is Continuous Integration and what problem does it solve?**
   - The practice of automatically building and testing code every time a team member pushes changes. It solves merge conflicts, integration drift, and undetected bugs by catching issues early.

5. **What is the role of a hosted runner in GitHub Actions?**
   - A virtual machine managed by GitHub (e.g., `ubuntu-latest`) that executes the workflow steps and jobs in a clean, isolated environment without requiring local server setup.
