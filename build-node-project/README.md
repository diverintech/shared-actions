# Node.js Build GitHub Action

This GitHub Action workflow is designed to automate the build process for Node.js projects. It checks out the code, caches dependencies, installs the required Node.js version and dependencies, and then builds the project.

## Workflow Overview

The workflow performs the following steps:

1. **Checkout Code**: Fetches the latest code from the repository using `actions/checkout@v4`.
2. **Cache Dependencies**: Caches Node.js dependencies using `actions/cache@v4`, speeding up the installation process on subsequent runs.
3. **Install Node.js**: Sets up the required Node.js version (version 20) using `actions/setup-node@v4`.
4. **Install Dependencies**: Runs `npm ci` to install project dependencies in a clean state.
5. **Build Project**: Runs the `npm run build` command to build the project.

## How to Use

To use this workflow in another repository, you can reference it like this:

```yaml
jobs:
  test:
    uses: diverintech/shared-actions/build-project/build.yml@v1.0.0
```
