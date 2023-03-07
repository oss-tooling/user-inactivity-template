# user-inactivity-template

This template repository is a reference implementation for GitHub Enterprise Administrators looking to use [user-inactivity](https://github.com/oss-tooling/user-inactivity) to monitor and remove inactive users from a GitHub organization.

## Installation

1. Create a [GitHub App](#create-a-github-app)
1. Copy this repository into your organization.
1. Update [the audit workflow](./.github/workflows/audit.yml) with your organization name.
1. Update [the report workflow](./.github/workflows/report.yml) with your organization name and the repository in which notification issues will be created.
1. Update [the kick workflow](./.github/workflows/kick.yml) with your organization name and the repository in which notification issues are created.

## Create a GitHub App

This automation runs as a GitHub App.  Follow [these instructions](https://docs.github.com/en/apps/creating-github-apps/creating-github-apps/creating-a-github-app) to create an app and set the following secrets in your GitHub repository:

* `APP_ID`: The ID of the GitHub App
* `APP_PRIVATE_KEY`: The private key of the GitHub App
* `APP_INSTALLATION_ID`: The installation ID of the GitHub App installed in the target organization.