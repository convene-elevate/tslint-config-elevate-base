# tslint-config-elevate-base

Elevate's base TypeScript TSLint config.

## How to configure

1) npm install https://github.com/convene-elevate/tslint-config-elevate-base.git#actual_version --save-dev
2) npm install tslint@5.9.1 --save-dev
2) npm install typescript@2.6.2 --save-dev
3) In you project root you need to add tslint.json file with a default configuration.
```
{
    "extends": "tslint-config-elevate-base"
}

Read more about the tslint configuration [here](https://palantir.github.io/tslint/usage/tslint-json/).

## How to use

1) tslint --config tslint.json ./app_directory --exclude './**/node_modules/**'

Read more about the CLI [here](https://palantir.github.io/tslint/usage/cli/)

## How to automate linting

1) npm install husky --save-dev
2) Add the next lines in a scripts section in your package.json
```
"tslint": "tslint --config tslint.json ./app_directory --exclude './**/node_modules/**'",
"precommit": "npm run tslint"
```
