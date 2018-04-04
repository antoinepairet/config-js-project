# config-js-project

````
npm i --save-dev eslint eslint-config-prettier eslint-plugin-mocha husky lint-staged
````

Package.json scripts:
````
"eslint": "eslint \"./**/*.js\"",
"precommit": "lint-staged",
````

Package.json lint-staged:
````
    "lint-staged": {
        "*.js": [
            "prettier --write",
            "eslint",
            "git add"
        ]
    }
````

.prettierc
```
{
    "singleQuote": true,
    "trailingComma": "es5",
    "write": true,
    "tabWidth": 4,
    "bracketSpacing": true
}
````

.eslintrc.js
````
module.exports = {
    env: {
        es6: true,
        node: true,
        //browser: true,
    },
    globals: {
        //_: true,
        //angular: true,
        //moment: true,
    },
    extends: ['prettier', 'eslint:recommended'],
    rules: {
        noConsole: false,
        noIgnoredWarnings: true,
    },
};
````
