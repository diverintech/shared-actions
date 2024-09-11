# CI Build Workflow

This repository contains a CI build workflow designed for continuous integration, testing, and building of Node.js projects using GitHub Actions.

## Workflow Overview

The workflow is triggered on two events:

push: Every time code is pushed to the repository.
workflow_dispatch: Manually triggered workflow from the GitHub interface.
The workflow consists of two jobs:

Test: Runs tests and caches dependencies to speed up future builds.
Build: Builds the project after the testing steps have passed.
Workflow Structure
Environment Variables
NODE_VERSION: Specifies the version of Node.js used in the workflow. The default is set to 20.
Jobs

## 1. Test

This job handles testing the codebase:

Checks out the repository code.
Caches dependencies using actions/cache@v4.
Installs Node.js version specified in the environment variable.
Installs dependencies using npm install.
Runs tests using npm run test:ci.
Uploads test reports only if the tests fail.

## 2. Build

This job handles building the project after successful testing:

Checks out the repository code.
Caches dependencies using actions/cache@v4.
Installs Node.js version specified in the environment variable.
Installs dependencies using npm ci.
Builds the project using npm run build.

# Customization

Node.js version: Update the NODE_VERSION environment variable to use a different version of Node.js.
Test command: Customize the test step by modifying the npm run test:ci command to match your project's test scripts.
