# Udagram

The udagram application is application based on Instagram. Front-end is deployed in S3 bucket and the Back-end is deployed in Elastic Beanstalk

### How to run in your local

1. **Back-end**

```
    source set_env.sh
    cd udagram-api/
    rm -rf node_modules/
    rm -rf package-lock.json

    # Install the package dependencies
    npm install .

    # Build application
    npx tsc

    # Run the application locally
    npm run start:dev
```

2. **Front-end**

```
    source set_env.sh
    cd udagram-frontend/
    rm -rf node_modules/
    rm -rf package-lock.json

    # Install the package dependencies
    npm install -f

    # Build application
    npm run build

    # Run the application locally
    npm run start
```

## Testing

This project contains two different test suite: unit tests and End-To-End tests(e2e). Follow these steps to run the tests.

1. `cd starter/udagram-frontend`
1. `npm run test`
1. `npm run e2e`

There are no Unit test on the back-end

### Unit Tests:

Unit tests are using the Jasmine Framework.

### End to End Tests:

The e2e tests are using Protractor and Jasmine.

## Built With

- [Angular](https://angular.io/) - Single Page Application Framework
- [Node](https://nodejs.org) - Javascript Runtime
- [Express](https://expressjs.com/) - Javascript API Framework

## Hosting

The Front-end is deployed at: [http://tuanla122.s3-website-us-east-1.amazonaws.com](http://tuanla122.s3-website-us-east-1.amazonaws.com)

## License

[License](LICENSE.txt)
