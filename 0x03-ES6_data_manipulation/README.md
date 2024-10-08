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
### babel.config.js

```js
module.exports = {
  presets: [
    [
      '@babel/preset-env',
      {
        targets: {
          node: 'current',
        },
      },
    ],
  ],
};
```

### .eslintrc.js

```js
module.exports = {
  env: {
    browser: false,
    es6: true,
    jest: true,
  },
  extends: [
    'airbnb-base',
    'plugin:jest/all',
  ],
  globals: {
    Atomics: 'readonly',
    SharedArrayBuffer: 'readonly',
  },
  parserOptions: {
    ecmaVersion: 2018,
    sourceType: 'module',
  },
  plugins: ['jest'],
  rules: {
    'max-classes-per-file': 'off',
    'no-underscore-dangle': 'off',
    'no-console': 'off',
    'no-shadow': 'off',
    'no-restricted-syntax': [
      'error',
      'LabeledStatement',
      'WithStatement',
    ],
  },
  overrides:[
    {
      files: ['*.js'],
      excludedFiles: 'babel.config.js',
    }
  ]
};
```

### Run npm install
Don't forget to run the command below to install all dependencies:
```bash
npm install
```
## Tasks
### 0. Basic list of objects

- **File**: `0-get_list_students.js`.
- **Description**: Create a function named `getListStudents` that returns an array of objects. Each object should have three attributes: `id` (Number), `firstName` (String), and `location` (String).

### 1. More mapping
- **File**: `1-get_list_student_ids.js`.
- **Description**: Create a function `getListStudentIds` that returns an array of ids from a list of objects. If the argument is not an array, the function returns an empty array.

### 2. Filter
- **File**: `2-get_students_by_loc.js`.
- **Description**: Create a function `getStudentsByLocation` that returns an array of objects who are located in a specific city. It accepts a list of students and a city as parameters.

### 3. Reduce
- **File**: `3-get_ids_sum.js`.
- **Description**: Create a function `getStudentIdsSum` that returns the sum of all the student ids. It accepts a list of students as a parameter.

### 4. Combine
- **File**: `4-update_grade_by_city.js`.
- **Description**: Create a function `updateStudentGradeByCity` that returns an array of students for a specific city with their new grade. If a student doesn’t have a grade, the final grade should be `N/A`.

### 5. Typed Arrays
- **File**: `5-typed_arrays.js`.
- **Description**: Create a function `createInt8TypedArray` that returns a new ArrayBuffer with an Int8 value at a specific position. If the position is outside range, throw an error Position outside range.

### 6. Set data structure
- **File**: `6-set.js`.
- **Description**: Create a function `setFromArray` that returns a Set from an array. It accepts an argument (Array, of any kind of element).

### 7. More set data structure
- **File**: `7-has_array_values.js`.
- **Description**: Create a function `hasValuesFromArray` that returns a boolean if all the elements in the array exist within the set.

### 8. Clean set
- **File**: `8-clean_set.js`.
- **Description**: Create a function `cleanSet` that returns a string of all the set values that start with a specific string. The string contains all the values of the set separated by `-`.

### 9. Map data structure
- **File**: `9-map.js`.
- **Description**: Create a function `groceriesList` that returns a Map of groceries with the following items (name, quantity):
- - Apples, 10
- - Tomatoes, 10
- - Pasta, 1
- - Rice, 1
- - Bananas, 5

### 10. More map data structure
- **File**: `10-update_uniq_items.js`.
- **Description**: Create a function `updateUniqueItems` that returns an updated map for all items with initial quantity of 1. Replace the quantity with 100.

### 11. Weak link data structure
- **File**: `100-weak.js`.
- **Description**: Write a class `WeakMap` that is weakly referenced. The class should have methods to add, delete, and check existence of keys.

## Author
- **Mudi Murtala**
- **GitHub**: https://github.com/mudimurtala
