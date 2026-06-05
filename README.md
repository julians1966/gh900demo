# GH-900 Demo

GH-900 Training — Sample code and processes for GitHub Issues, Pull Requests, and Actions.

This is a change in VS Code

## Overview

This repository demonstrates common GitHub workflows including:

- **Issues** — Using issue templates to report bugs and request features
- **Pull Requests** — Following a consistent PR process with a template
- **Actions** — Automated CI pipelines that lint and test code on every push and pull request

## Repository Structure

```
gh900demo/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.md        # Template for bug reports
│   │   └── feature_request.md  # Template for feature requests
│   ├── workflows/
│   │   └── ci.yml               # GitHub Actions CI workflow
│   └── pull_request_template.md # PR checklist template
├── src/
│   └── calculator.py            # Sample Python module
├── tests/
│   └── test_calculator.py       # Unit tests for the sample module
└── README.md
```

## Sample Application

The `src/calculator.py` module provides basic arithmetic operations and serves as a minimal example to exercise the CI pipeline.

## Getting Started

### Prerequisites

- Python 3.9+

### Install dependencies

```bash
pip install pytest
```

### Run tests

```bash
pytest tests/
```

## GitHub Processes

### Reporting an Issue

Use one of the issue templates available when creating a new issue:

- **Bug Report** — Describe a defect, including steps to reproduce and expected vs actual behavior.
- **Feature Request** — Describe a new capability you would like to see.

### Opening a Pull Request

When opening a PR, the pull request template will guide you through describing your changes and confirming you have completed the standard checks.

### Continuous Integration

Every push and pull request triggers the `ci.yml` workflow, which:

1. Checks out the code
2. Sets up Python
3. Runs `pytest` against the test suite

A green check mark on your PR means all tests passed.
