Organization-Wide GitHub Workflows This repository contains reusable GitHub Actions workflows for [Your Organization Name]. These workflows are designed to streamline and standardize automation processes across multiple repositories within the organization. By centralizing workflow configurations, we ensure consistency, reduce duplication, and simplify maintenance.

Available Workflows Auto Pull Changes (All Branches) Path: .github/workflows/auto-pull-changes.yml Description: This workflow triggers on any branch push event across organization repositories. It automates code pull operations on all designated servers and keeps the branches synchronized. Usage Instructions To use these workflows in other repositories:

Reference the workflow in the repository’s .github/workflows/ folder, using the workflow_call event. Add necessary secrets and permissions to each repository that requires access to these workflows. Example of calling a reusable workflow in another repository:
```
name: Call Reusable Auto-Pull Workflow

on:
  push:
    branches:
      - "*"

jobs:
  auto-pull:
    uses: Learnovia-egy/org-workflows/.github/workflows/auto-pull.yml@main
    secrets:
      SSH_PRIVATE_KEY: ${{ secrets.SSH_PRIVATE_KEY }}
    with:
      commands: |
        <FRAMEWORK COMMANDS>

```
