# pblx-npm-starter

Starter kit for creating NPM packages for PBLX.

## Variables to adjust

- public/index.html: PROJECT_TITLE
- package.json:
  - files - if any more files need to go in the NPM package add them here
- gitlab: Add `PRODUCTION__S3_BUCKET`, `PRODUCTION__S3_PATH`,

Also change this README.md.

## Testing the NPM package locally

To test the package locally you can run `yarn link`. In some cases the project
you're using to test the package will 'see' two versions of react. You can solve
this by temporarily linking react from the testing project in this package. More
information here: https://reactjs.org/warnings/invalid-hook-call-warning.html#duplicate-react

## Deploying

A gitlab pipeline is set up to deploy your app to an S3 bucket. This is to be used
for staging purposes. Make sure the env variables are set in gitlab.

## Publishing your module

Bump your package version:

```sh
npm version patch/minor/major
```

Push tags to gitlab:

```sh
git push --tags
```

Then run the publish pipeline in gitlab.
