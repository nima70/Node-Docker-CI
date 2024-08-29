
# Docker-Compose GitHub Action for Testing and Deploying NPM Packages

This repository provides a template for setting up a CI/CD pipeline using GitHub Actions and Docker Compose. The primary purpose is to automate the testing and deployment of npm packages, utilizing Docker Compose to manage the necessary services during the testing phase.

## Overview

This template leverages Docker Compose to spin up services required for testing npm packages in a consistent environment. The GitHub Action workflow included in this repository is designed to install dependencies, run tests, build the project, and publish the npm package upon a successful push to the specified branch.

## Key Features

- **Automated Testing**: The GitHub Action automatically runs your tests within a Docker-managed environment, ensuring consistent results across different environments.
- **Docker Compose Integration**: Easily define and manage services required for your tests using Docker Compose.
- **NPM Publishing**: Automatically publish your npm package after passing tests and building the project.
- **Customizable Workflow**: The provided GitHub Action can be easily customized to suit the specific needs of your project.

## Usage

### Prerequisites

- A GitHub repository.
- Docker and Docker Compose installed locally for testing the setup.
- An npm account with an authentication token stored as a secret in your GitHub repository.

### Setting Up

1. **Fork or Clone this Repository:**

   ```bash
   git clone https://github.com/your-username/docker-compose-github-action.git
   cd docker-compose-github-action
   ```
2. **Modify the docker-compose.yml File:**

Update the docker-compose.yml file to define the services required for your project’s tests.

3. **Update the GitHub Actions Workflow:**

The .github/workflows/publish-to-npm.yml file contains the CI/CD pipeline. Customize this file to fit your project's requirements, such as modifying the services or npm scripts.

4. **Set Up NPM Authentication:**

Store your npm authentication token in your GitHub repository’s secrets:

Go to your repository on GitHub.
Navigate to Settings > Secrets and variables > Actions > New repository secret.
Create a secret named NPM_TOKEN with your npm token as the value.
Running the Workflow
The GitHub Action will trigger automatically on a push to the master branch (or any branch you specify). It will:

# License
This project is licensed under the MIT License.
