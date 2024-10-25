# Remote Workflows Configuration Example

This repository provides examples for configuring remote workflows using GitHub Actions. It demonstrates how to set up various workflows for CI/CD, deployment, and other automation tasks.

## Workflows

### 1. CI Workflow
**File:** `.github/workflows/ci.yml`

**Description:** This workflow is triggered on a push to the `main` branch. It builds the service, logs the build process, generates a build number, and outputs the build number.

### 2. Deployment Workflow
**File:** `.github/workflows/deployment.yml`

**Description:** This workflow is triggered on the completion of a check suite, a workflow run, or a pull request merge to the `main` branch. It performs a multi-region deployment using a remote workflow.

### 3. Break Glass Workflow
**File:** `.github/workflows/break-glass.yml`

**Description:** This workflow is manually triggered using the `workflow_dispatch` event. It allows for a breakglass deployment to a specified region (US or EU).

### 4. DevX Deployment Workflow
**File:** `.github/workflows/devX-deployment.yml`

**Description:** This workflow is triggered when a pull request is labeled with a label starting with `DEV-`. It deploys to the specified development environment using a remote workflow.

## Usage

1. **CI Workflow:**
    - Push changes to the `main` branch to trigger the CI workflow.

2. **Deployment Workflow:**
    - Ensure that the CI workflow has completed successfully.
    - Merge a pull request to the `main` branch to trigger the deployment workflow.

3. **Break Glass Workflow:**
    - Manually trigger the workflow from the GitHub Actions tab.
    - Select the desired region (US or EU) for the


Test