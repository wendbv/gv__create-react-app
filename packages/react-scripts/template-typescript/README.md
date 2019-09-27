# pblx-npm-starter

Starter kit for creating NPM packages for PBLX.

## Variables to adjust
- config/webpack.config.js: LIBRARY_NAME
- public/index.html: PROJECT_TITLE
- src/index.tsx: ModuleName
- package.json:
    - adjust "name"
    - files - if any more files need to go in the NPM package add them here
- gitlab: Add PRODUCTION__S3_BUCKET, PRODUCTION__S3_PATH, 

Also change this README.md.

## Testing the NPM package locally
To test the package locally you can run `yarn link`. In some cases the project 
you're using to test the package will 'see' two versions of react. You can solve
this by temporarily linking react from the testing project in this package. More
information here: https://reactjs.org/warnings/invalid-hook-call-warning.html#duplicate-react
