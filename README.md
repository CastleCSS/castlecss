# CastleCSS (Full package)
A modular, updatable, easy to use SCSS Framework

![CastleCSS logo @CastleCss.com](https://www.doordarius.nl/castlecss-logo-250.png)

## What's included?
Included in this package:
- Example project setup
- Gruntfile and task
- [castlecss-core](https://github.com/CastleCSS/castlecss-core)
- [castlecss-buttons](https://github.com/CastleCSS/castlecss-buttons)
- [castlecss-notifications](https://github.com/CastleCSS/castlecss-notifications)

## How to install
CastleCSS is built with easy updating in mind.
You can download the Full package and make adjustments as long as you don't update the dependencies (core, buttons, notifications, etc).

When you dó adjust the dependencies, you will lose all adjustments with an update.

There are a few ways to install:

- Download or clone the package (easiest way for the full package)
- Install via [NPM](https://www.npmjs.com/): ```npm install castlecss```
- Require it in your own NPMJS package

## Updating files

NOTE: Only update the dependencies so you don't overwrite your own SCSS files. If you do update the Full package you'll overwrite everything. 

We recommend downloading the full package and updating the dependencies like:
```
npm update castlecss-core
npm update castlecss-buttons
npm update castlecss-notifications
```

## Documentation
We're currently writing the documentation. Hang on tight!

## Setup
Your project should have a setup similair to this (included in the Full package):
With this you make sure your own variables overwrite the castle-core variables and your setup is still updatable.

```
| Your project/
|
|-- scss/ 
| |-- /* Custom project specific scss files here */
| |-- Main.scss
| |
|-- node_modules/
| | 
| | /*	CastleCSS files included automatically here */
| | castlecss-core/
| | castlecss-buttons/
| | castlecss-etc ;)/
```

### Main.scss
Your main.scss should have a setup similair to this (included in the [Full CastleCSS Package](https://github.com/CastleCSS/castlecss)):

```
/*  castlecss variable files */
@import "path/to/castlecss-core/sass/variables";


/*  Your own variables so they overwrite the core */
@import "variables";
/*  rest of castle files */
@import "path/to/castlecss-core/sass/main";
@import "path/to/castlecss-buttons/sass/variables";
@import "path/to/castlecss-notifications/sass/variables";
 
/*  Include your own files below this line
    --------------------------------------
*/
```
