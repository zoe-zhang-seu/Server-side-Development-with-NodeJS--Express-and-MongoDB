```
```
## 1. Node modules
Related material
- [CommonJS modules](https://nodejs.org/api/modules.html)

**module**
Each file in Node is its own module. 
**Load the other module** -- `require(./xxx.js)`
```
const circle = require('./circle.js');
```
**export the constant** -- `exports.functionName`
```
const { PI } = Math;
exports.area = (r) => PI * r ** 2;
exports.circumference = (r) => 2 * PI * r;
```
**define a module** --`module.exports = class A { return xxx;};`
```
module.exports = class Square {
  constructor(width) {
    this.width = width;
  }

  area() {
    return this.width ** 2;
  }
};
```
#### how to write a simple Node application in js
```
npm init
```
add `start` to prepare for the `npm start` to open the local host 3000 web
```
{
  "name": "node-examples",
  "version": "1.0.0",
  "description": "Simple Node Examples",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "node index"
  },
  "author": "Jogesh Muppala",
  "license": "ISC"
}
```
Javascript Grammar
- [console.log()](https://www.w3schools.com/jsref/met_console_log.asp)
- [javascript function](https://www.w3schools.com/js/js_functions.asp)
- [js arrow function](https://www.w3schools.com/js/js_arrow_function.asp)
- [difference between regular and arrow function](https://www.geeksforgeeks.org/difference-between-regular-functions-and-arrow-functions/)

## 2. Node.js Event loop
related material
- [Event loop](https://nodejs.org/en/docs/guides/event-loop-timers-and-nexttick/) difficult to understand can read for more times
- [exteranl about module](https://www.freecodecamp.org/news/require-module-in-node-js-everything-about-module-require-ccccd3ad383/) read if have time
- [commonJS](http://www.commonjs.org/) not that necessary
- [commonJS format](http://wiki.commonjs.org/wiki/Modules/1.1.1) pay attention to the sample code
- [RequireJS](https://requirejs.org/) emmm...if needed 

Practice time
Read material first
- [what is callback function](https://www.freecodecamp.org/news/javascript-callback-functions-what-are-callbacks-in-js-and-how-to-use-them/)
- [synchronous vs asynchronous callback](https://www.javascripttutorial.net/javascript-callback/) this one is better
- [error handling](https://www.w3schools.com/js/js_errors.asp)
- [node.js error handling](https://www.joyent.com/node-js/production/design/errors) pay attention to the sample code
```
callback(new Error('something bad happened'));
```
- [Node.js error handling](https://nodejs.dev/learn/error-handling-in-nodejs) this one is the best

#### setTimeout()
- [setTimeout()](https://nodejs.dev/learn/discover-javascript-timers)
```
setTimeout(() => { // runs after 2 seconds
}, 2000)

setTimeout(() => { // runs after 50 milliseconds
}, 50)
```
#### nextTick()
the engine to invoke this function at the end of the current operation, before the next event loop tick starts:
```
process.nextTick(() => { //do something})
```
#### Js reponse
- [reponse object](https://www.tutorialspoint.com/nodejs/nodejs_response_object.htm)











