# Pipeline Process Documentation

This document outlines the pipeline process as defined in the `config.yml` file.

## Version

- **Version**: 2.1

## Orbs

Orbs are reusable packages of CircleCI configuration that help automate repetitive tasks. The following orbs are used:

- **Node**: `circleci/node@5.0.2`
- **AWS Elastic Beanstalk**: `circleci/aws-elastic-beanstalk@2.0.1`
- **AWS CLI**: `circleci/aws-cli@3.1.1`

## Jobs

### Build

The build job is responsible for setting up the environment, installing dependencies, linting, and building both the frontend and backend applications.

- **Docker Image**: `cimg/node:14.15`
- **Steps**:
  1. **Install Node**: Installs Node.js version 14.15.
  2. **Checkout**: Checks out the code from the repository.
  3. **Install Front-End Dependencies**: Runs `npm run frontend:install` to install frontend dependencies.
  4. **Install API Dependencies**: Runs `npm run api:install` to install backend dependencies.
  5. **Front-End Lint**: Runs `npm run frontend:lint` to lint the frontend code.
  6. **Front-End Build**: Runs `npm run frontend:build` to build the frontend application.
  7. **API Build**: Runs `npm run api:build` to build the backend API.

### Deploy

The deploy job is responsible for deploying the application after manual approval.

- **Docker Image**: `cimg/base:stable`
- **Steps**:
  1. **Install Node**: Installs Node.js version 14.15.
  2. **Setup Elastic Beanstalk**: Sets up AWS Elastic Beanstalk.
  3. **Setup AWS CLI**: Sets up the AWS CLI.
  4. **Checkout**: Checks out the code from the repository.
  5. **Deploy App**: Runs `npm run deploy` to install, build, and deploy both the frontend and backend applications.

## Workflows

### Udagram

The workflow `udagram` orchestrates the execution of jobs.

- **Jobs**:
  1. **Build**: Runs the build job.
  2. **Hold**: Requires manual approval to proceed.
     - **Filters**:
       - **Branches**: Only runs on the `master` branch.
  3. **Deploy**: Runs the deploy job after manual approval.

This pipeline ensures that the application is built and tested before deployment, with a manual approval step to ensure control over the deployment process.
