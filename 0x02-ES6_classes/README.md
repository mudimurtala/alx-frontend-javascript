# 0x02. ES6 Classes

## Overview
This project focuses on Object-Oriented Programming (OOP) in JavaScript, specifically using ES6 classes. By the end of this project, you will understand how to define and work with classes, methods, inheritance, and more advanced topics such as metaprogramming and symbols.

## Learning Objectives
By the end of this project, you should be able to explain the following concepts without the help of Google:
- How to define a Class
- How to add methods to a class
- Why and how to add a static method to a class
- How to extend a class from another
- Metaprogramming and symbols

## Resources
Read or watch:
- [Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
- [Metaprogramming](https://en.wikipedia.org/wiki/Metaprogramming)

## Requirements
- All files will be executed on Ubuntu 18.04 LTS using NodeJS 12.11.x
- Allowed editors: vi, vim, emacs, Visual Studio Code
- All files should end with a new line
- A `README.md` file, at the root of the folder of the project, is mandatory
- Your code should use the `.js` extension
- Your code will be tested using Jest and the command `npm run test`
- Your code will be verified against lint using ESLint
- Your code needs to pass all the tests and lint. You can verify the entire project running `npm run full-test`

## Setup
### Install NodeJS 12.11.x
In your home directory, run the following commands:
```bash
curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
sudo bash nodesource_setup.sh
sudo apt install nodejs -y
```
### Verify the installation:
```
nodejs -v
# v12.11.1
npm -v
# 6.11.3
```
### Install Jest, Babel, and ESLint
In your project directory, install Jest, Babel, and ESLint by using the supplied package.json and running:
```
npm install
```
### Configuration Files
Make sure to include the following configuration files in your project directory:

package.json
babel.config.js
.eslintrc.js
## Tasks
### 0. You used to attend a place like this at some point
File: 0-classroom.js
Description: Implement a class named ClassRoom that accepts one attribute named maxStudentsSize (Number) and assigns it to _maxStudentsSize.
### 1. Let's make some classrooms
File: 1-make_classrooms.js
Description: Import the ClassRoom class from 0-classroom.js and implement a function named initializeRooms that returns an array of 3 ClassRoom objects with the sizes 19, 20, and 34.
### 2. A Course, Getters, and Setters
File: 2-hbtn_course.js
Description: Implement a class named HolbertonCourse with attributes name, length, and students. Implement getters and setters for each attribute.
### 3. Methods, static methods, computed methods names..... MONEY
File: 3-currency.js
Description: Implement a class named Currency with attributes code and name. Implement getters and setters for each attribute, and a method named displayFullCurrency that returns the attributes in the format name (code).
### 4. Pricing
File: 4-pricing.js
Description: Implement a class named Pricing that imports Currency from 3-currency.js. The class should have attributes amount and currency, with getters and setters for each. Implement a method named displayFullPrice and a static method convertPrice.
### 5. A Building
File: 5-building.js
Description: Implement a class named Building with an attribute sqft. This class is abstract, and any class extending from it must implement a method named evacuationWarningMessage.
### 6. Inheritance
File: 6-sky_high.js
Description: Implement a class named SkyHighBuilding that extends from Building. The class should have attributes sqft and floors, with getters for each. Override the method evacuationWarningMessage to return the string Evacuate slowly the NUMBER_OF_FLOORS floors.
### 7. Airport
File: 7-airport.js
Description: Implement a class named Airport with attributes name and code. The default string description of the class should return the airport code.
### 8. Primitive - Holberton Class
File: 8-hbtn_class.js
Description: Implement a class named HolbertonClass with attributes size and location. When the class is cast into a Number, it should return the size, and when cast into a String, it should return the location.
### 9. Hoisting
File: 9-main.js
Description: Fix the given code to make it work correctly by rearranging the class definitions and using the correct order.
# Repository
GitHub repository: alx-frontend-javascript
Directory: 0x02-ES6_classes