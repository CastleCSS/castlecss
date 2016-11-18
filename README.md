# [castlecss-core](https://www.castlecss.com)
CastleCSS is a modular, updatable, easy-to-use HTML5 and SCSS framework. It includes a flexible grid system, buttons, notifications, utility classes and a set of Sass mixins to make a quick start for your site or app.

## What's Included?
- [castlecss-core](https://github.com/CastleCSS/castlecss-core)
- [castlecss-buttons](https://github.com/CastleCSS/castlecss-buttons)
- [castlecss-notifications](https://github.com/CastleCSS/castlecss-notifications)
- [castlecss-docs (documentation)](https://github.com/CastleCSS/castlecss-docs)

## Getting Started
There are a few ways to get started with CastleCSS. If you're setting things up all by yourself, the easiest way to install is through the npm package manager or to clone the package in your project directory.

- Install with [npm](https://www.npmjs.com/): ```npm install castlecss```
- Clone the package ```git clone https://github.com/CastleCSS/castlecss.git```

Make sure to run ```npm install``` from your directory to install the dependencies and start using CastleCSS.

If you're looking for a ready-to-go project setup, checkout [CastleCSS Boilerplate](https://github.com/CastleCSS/castlecss-boilerplate/) and simply download the .ZIP. This download is extended with a basic HTML5-template and a configuration for Grunt to easily compile and minify your Sass files.

## Updating files
This front-end framework is easy updatable. This has the advantage that new features can quickly be included in your project, but that your adjustments made to the dependencies will be overwritten with your next update.

This is an easy updatable framework. This means that adjustments you made to the dependencies will be overwritten with your next update.
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

## Setup
Your project should have a setup similar to this:

```
| Your project/
|
|-- scss/
| |-- /* Custom project specific scss files here */
| |-- main.scss
| |
|-- node_modules/
| |
| | /*	CastleCSS files included automatically here */
| | castlecss-core/
| | castlecss-buttons/
| | castlecss-etc ;)/
```

With this you make sure your own variables overwrite the castle-core variables and your setup is still updatable.

### main.scss
Your main.scss should have a setup similar to this (included in the [CastleCSS (Full package)](https://github.com/CastleCSS/castlecss)):

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
