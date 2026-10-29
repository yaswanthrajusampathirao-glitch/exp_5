# Experiment 5: Advanced GitHub Workflows

![CI](https://github.com/username/repo/actions/workflows/ci.yml/badge.svg)

## Overview
Demonstrating advanced GitHub workflows:
- GitHub Flow branching strategy
- Protected branches & required code reviews
- Continuous Integration (CI) and linting using GitHub Actions

## Directory Structure
```
.
├── .github/
│   └── workflows/
│       └── ci.yml
├── src/
│   └── calc.py
├── tests/
│   └── test_calc.py
└── README.md
```

## Running Locally
```bash
pip install pytest flake8
flake8 src/ --max-line-length=100
pytest -q
```
