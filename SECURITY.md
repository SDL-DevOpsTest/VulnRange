# Security Policy

## Supported Versions

Use this section to tell people about which versions of your project are
currently being supported with security updates.

| Version | Supported          |
| ------- | ------------------ |
| 5.1.x   | :white_check_mark: |
| 5.0.x   | :x:                |
| 4.0.x   | :white_check_mark: |
| < 4.0   | :x:                |

## Reporting a Vulnerability

Use this section to tell people how to report a vulnerability.

Tell them where to go, how often they can expect to get an update on a
reported vulnerability, what to expect if the vulnerability is accepted or
declined, etc.


name: autofix.ci  # needed to securely identify the workflow

on:
  pull_request:
  push:
    branches: [ "main" ]
permissions:
  contents: read

jobs:
  autofix:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      # TODO: add all code-fixing here.

      - uses: autofix-ci/action@dd55f44df8f7cdb7a6bf74c78677eb8acd40cd0a
