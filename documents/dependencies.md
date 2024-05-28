# Application Dependencies

This document provides a concise overview of the dependencies required for the front-end and backend applications.

## General Requirements

- **Node.js**: v14.15.1 (LTS) or more recent.
- **npm**: v6.14.8 (LTS) or more recent.
- **RDS Database**: Running PostgreSQL.
- **S3 Bucket**: For hosting uploaded pictures.
- **Elastic Beanstalk**: For hosting the Node.js backend.
- **AWS CLI**: v2 (recommended).
- **EB CLI**

## Front-End Dependencies

### Core Libraries

- **@angular/common**: ^8.2.14
- **@angular/core**: ^8.2.14
- **@angular/forms**: ^8.2.14
- **@angular/platform-browser**: ^8.2.14
- **@angular/platform-browser-dynamic**: ^8.2.14
- **@angular/router**: ^8.2.14
- **@ionic/angular**: ^4.1.0

### Utilities

- **rxjs**: ~6.5.4
- **zone.js**: ~0.9.1
- **core-js**: ^2.5.4

## Backend Dependencies

### Core Libraries

- **aws-sdk**: ^2.429.0
- **bcryptjs**: 2.4.3
- **body-parser**: ^1.18.3
- **cors**: ^2.8.5
- **dotenv**: ^8.2.0
- **email-validator**: ^2.0.4
- **express**: ^4.16.4
- **jsonwebtoken**: ^8.5.1
- **pg**: ^8.7.1
- **reflect-metadata**: ^0.1.13
- **sequelize**: ^6.26.0
- **sequelize-typescript**: ^2.1.5

### Development Dependencies

- **@types/bcryptjs**: 2.4.2
- **@types/jsonwebtoken**: ^8.3.2
- **@types/bluebird**: ^3.5.26
- **@types/cors**: ^2.8.6
- **@types/express**: ^4.16.1
- **@types/node**: ^11.11.6
- **@types/sequelize**: ^4.28.14
- **@types/validator**: ^13.7.10
- **@typescript-eslint/eslint-plugin**: ^2.19.2
- **@typescript-eslint/parser**: ^2.19.2
- **chai**: ^4.2.0
- **chai-http**: ^4.2.1
- **eslint**: ^6.8.0
- **eslint-config-google**: ^0.14.0
- **mocha**: ^6.1.4
- **ts-node-dev**: ^1.0.0-pre.32
- **typescript**: ^4.2.3

## Additional Notes

- **Database and Storage**: Ensure you have access to an RDS instance running PostgreSQL and an S3 bucket for handling file uploads.
- **Deployment**: Use AWS Elastic Beanstalk for deploying the Node.js backend.
