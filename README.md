# shared-actions

This repository includes GitHub Actions that are shared among multiple repositories.

## Available Actions

### 1. Node.js CI Tests
- **Path**: `/test-node-project/node-ci-tests.yml`
- **Description**: This action automates the testing process for Node.js projects. It caches dependencies, installs the necessary packages, and runs tests. If the tests fail, it uploads the test report for further investigation.

### 2. Node.js Build
- **Path**: `/build-project/build.yml`
- **Description**: This action automates the build process for Node.js projects. It installs dependencies, builds the project, and caches the results to speed up subsequent builds.
