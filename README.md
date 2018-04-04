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
