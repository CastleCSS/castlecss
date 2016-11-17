# CastleCSS (Full package)
A modular, updatable, easy to use HTML and SCSS framework.

![CastleCSS logo @CastleCss.com](https://www.doordarius.nl/castlecss-logo-250.png)

## What's included?
Included in this package:
- Example project setup
- Gruntfile.js and tasks
- [castlecss-core](https://github.com/CastleCSS/castlecss-core)
- [castlecss-buttons](https://github.com/CastleCSS/castlecss-buttons)
- [castlecss-notifications](https://github.com/CastleCSS/castlecss-notifications)
- [castlecss-docs (documentation)](https://github.com/CastleCSS/castlecss-docs)

## How to install
CastleCSS is built with easy updating in mind.
You can download the full package and make adjustments as long as you don't update the dependencies (core, buttons, notifications and docs). When you decide to adjust the dependencies, you will lose them with the next update.

There are a few ways to install:

- [Download the latest release](https://github.com/CastleCSS/castlecss/archive/master.zip)
- Clone the package ```git clone https://github.com/CastleCSS/castlecss.git```
- Install via [npm](https://www.npmjs.com/): ```npm install castlecss```
- Add it to your package.json in your own npm package

When downloading or cloning CastleCSS, you have to run ```npm install``` from the directory to get the full package (core, buttons, notifications and docs). 

## Updating files

NOTE: Only update the dependencies so that you don't overwrite your own SCSS files. If you do update the full package you'll overwrite everything.

We recommend downloading the full package and updating the dependencies like:
```
npm update castlecss-core
npm update castlecss-buttons
npm update castlecss-notifications
npm update castlecss-docs
```

## Documentation and examples
You can find the documentation and examples at http://www.castlecss.com and included in this package (castlecss-docs)


## Basic structure
The basis structure for your website should look similar like this:

```
| Project directory/
|
|-- node_modules/
| | -- castlecss-core/
| | --castlecss-buttons/
| | --castlecss-notifications/
| |
|-- scss/
| |-- main.scss
| |-- variables.scss
| |
|-- img/
|-- dist/
| |-- styles.min.css
| |-- styles.min.map
| |
|-- index.html
|-- Gruntfile.js
|-- package.json
```

### main.scss
Your main.scss should have the following set-up:

```
/* 	CastleCSS Core variables */
@import "node_modules/castlecss-core/sass/variables";

/* 	Your variables */
@import "variables";

/* 	Remaining Core files and other CastleCSS modules */
@import "node_modules/castlecss-core/sass/main";
@import "node_modules/castlecss-buttons/sass/main";
@import "node_modules/castlecss-notifications/sass/main";

/* Include your own files below this line
   -------------------------------------- */



/* --------------------------------------
   Include your own files above this line */

@import "node_modules/castlecss-core/sass/base/utility";
@import "node_modules/castlecss-core/sass/base/utility_spacers";
```
