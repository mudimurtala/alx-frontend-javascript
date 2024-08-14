# ES6 Data Manipulation

## Table of Contents
1. [Resources](#resources)
2. [Learning Objectives](#learning-objectives)
3. [Requirements](#requirements)
4. [Setup](#setup)
5. [Configuration Files](#configuration-files)
6. [Tasks](#tasks)

## Resources
Read or watch:
- [Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
- [Typed Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Typed_arrays)
- [Set Data Structure](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set)
- [Map Data Structure](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)
- [WeakMap](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakMap)

## Learning Objectives
By the end of this project, you should be able to explain the following concepts:
- How to use `map`, `filter`, and `reduce` on arrays.
- Typed arrays.
- The Set, Map, and WeakMap data structures.

## Requirements
- Your files will be executed on Ubuntu 18.04 LTS using NodeJS 12.11.x.
- Allowed editors: `vi`, `vim`, `emacs`, `Visual Studio Code`.
- All your files should end with a new line.
- A `README.md` file at the root of the project folder is mandatory.
- Your code should use the `.js` extension.
- Your code will be tested using Jest and the command `npm run test`.
- Your code will be verified against lint using ESLint.
- Your code needs to pass all tests and lint. You can verify the entire project by running `npm run full-test`.
- All your functions must be exported.

## Setup
### Install NodeJS 12.11.x
```bash
curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
sudo bash nodesource_setup.sh
sudo apt install nodejs -y
```

## Verify Installation
```bash
nodejs -v
# v12.11.1

npm -v
# 6.11.3
```
## Install Jest, Babel, and ESLint
In your project directory, install Jest, Babel, and ESLint using the provided `package.json` and run `npm install`.

## Configuration Files
### package.json

```json
{
  "scripts": {
    "lint": "./node_modules/.bin/eslint",
    "check-lint": "lint [0-9]*.js",
    "dev": "npx babel-node",
    "test": "jest",
    "full-test": "./node_modules/.bin/eslint [0-9]*.js && jest"
  },
  "devDependencies": {
    "@babel/core": "^7.6.0",
    "@babel/node": "^7.8.0",
    "@babel/preset-env": "^7.6.0",
    "eslint": "^6.4.0",
    "eslint-config-airbnb-base": "^14.0.0",
    "eslint-plugin-import": "^2.18.2",
    "eslint-plugin-jest": "^22.17.0",
    "jest": "^24.9.0"
  }
}
```
