# Kinectify Central Workflows

This repository contains centralized GitHub Actions workflows for use across all Kinectify repositories.

## How to use these workflows in other repositories?

Add the following file to the `.github/workflows` directory of your target repository:

```yaml
name: Use Kinectify Central .NET Auto Approve & Merge

on:
  pull_request:
    types: [opened, synchronize, reopened]

jobs:
  auto-merge-dotnet:
    uses: kinectify/.github/.github/workflows/auto-approve-merge-dotnet.yml@main
```

With this configuration, your repository will always use the latest version of the base workflow from this central repo.

## Benefits

- **Consistency:** All projects follow the same automation standards.
- **Maintainability:** Update workflows centrally, and all projects benefit immediately.
- **Simplicity:** Easy integration for new and existing repositories.
