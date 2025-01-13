# Wheel of balance [![npm][npm]][npm-url]

<img src="https://raw.githubusercontent.com/okolobaxa/wheel-of-balance/master/img/wheel-of-balance.jpg"  alt="Demo" width="300" height="300">

A small lib for drawing configurable [wheel of balance](https://medium.com/thrive-global/how-does-one-become-centered-and-balanced-bb28627a4461). 

## Usage

```js
var config = {};

config.segments = [
    { color: "#97CC64", text: "Section 1", level: 5 },
    { color: "#4569BC", text: "Section 2" }, // level is optional, 0 by default
    { color: "#2A8341", text: "Section 3" },
    { color: "#F68D38", text: "Section 4" },
    { color: "#EA527F", text: "Section 5" },
    { color: "#77B6E7", text: "Section 6" },
    { color: "#FFD963", text: "Section 7" },
    { color: "#A955B8", text: "Section 8" }
];

config.radius = 200; // optional. Default calculated based on canvas dimensions
config.levels = 10; // optional. Default 10
config.fontSize = 15; // optional. Default 15px

let canvas = document.getElementById("canvas");

const wheel = new Wheel(canvas, config);
wheel.draw();

const clearButton = document.getElementById("clear");
clearButton.addEventListener('click', function (e) {
    wheel.clear();
});

const downloadButton = document.getElementById("download");
downloadButton.addEventListener('click', function (e) {
    wheel.download();
});
```
