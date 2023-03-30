name: Setup node.js
on: workflow_dispatch
jobs:
print:
runs-on: ubuntu-latest
steps: - uses: actions/checkout@v3 - uses: actions/setup-node@v3
with:
node-version: 16
cache: 'npm' - run: npm ci - run: npm test
