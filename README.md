# Leap JS

This is the js framework for working with the Leap.

## Installation

Either grab the js file in the root of the project. There is a minified version there too.

If you're using npm, you can use `npm install leapjs`.

## Usage

### Using the javascript event loop

```javascript
Leap.loop(function(frame) {
  // ... your code here
})
```

### Do-it-yourself loop

To use the leap motion api do the following...

```javascript
var controller = new Leap.Controller();
controller.onFrame(function() {
  console.log("hello")
  console.log(controller.frame().id)
  console.log(controller.frame().fingers.length)
  console.log(controller.frame().finger(0))
})
controller.connect()
```

## Examples

Inside the examples directory are a few great examples. To get them running, do the following:

* Run `npm install`
* Run `./node_modules/.bin/static .`
* Point your browser at http://localhost:8080/examples and enjoy

## Tests

There are currently rudamentary tests. To get them running, do the following:

* Run `npm install`
* Run `rake test`
