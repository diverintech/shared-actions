# Node.js CI Tests GitHub Action

This GitHub Action workflow is designed to automate the testing process for Node.js projects. It handles dependency caching, installation, and runs the test suite, uploading a test report in case of failure.

## Workflow Overview

This workflow performs the following steps:

1. **Checkout Code**: Fetches the latest code from the repository using `actions/checkout@v4`.
2. **Cache Dependencies**: Caches Node.js dependencies using `actions/cache@v4`, improving build times for subsequent runs.
3. **Install Node.js**: Sets up Node.js version 20 using `actions/setup-node@v4`.
4. **Install Dependencies**: Installs the required project dependencies by running `npm install`.
5. **Run Tests**: Executes the test suite using the `npm run test:ci` command.
6. **Upload Test Report**: If the tests fail, the workflow uploads the `test.json` file containing the test report using `actions/upload-artifact@v4`.

## How to Use

You can include this workflow in another repository by referencing it as follows:

```yaml
jobs:
  test:
    uses: diverintech/shared-actions/test-node-project/tests.yml@v1.0.0
```
