# CastleCSS
CastleCSS is a modular, updatable, easy-to-use HTML5 and SCSS framework. It includes a flexible grid system, buttons, notifications, utility classes, icons and a set of Sass mixins to make a quick start for your site or app.

![CastleCSS logo @CastleCss.com](https://www.doordarius.nl/castlecss-logo-250.png)

## What's Included?
This is a meta package with all available packages for CastleCSS:

- [castlecss-core](https://github.com/CastleCSS/castlecss-core)
- [castlecss-buttons](https://github.com/CastleCSS/castlecss-buttons)
- [castlecss-notifications](https://github.com/CastleCSS/castlecss-notifications)
- [castlecss-icons](https://github.c
om/CastleCSS/castlecss-icons)

## Getting Started
There are a few ways to get started with CastleCSS. If you're setting things up all by yourself, the easiest way to install is through the npm package manager or to clone the package in your project directory.

- Download the [CastleCSS Boilerplate](https://www.github.com/CastleCSS/castlecss-boilerplate). All Packages are included + examples and project setup
- Install with [npm](https://www.npmjs.com/): ```npm install castlecss -S```
- Clone the package ```git clone https://github.com/CastleCSS/castlecss.git```

Make sure to run ```npm install``` from your directory to install the dependencies and start using CastleCSS.

### Adjusting the variables
Because of the unique update-able setup of CastleCSS you need a seperate variable file to overwrite the default CastleCSS variables. There are a few ways to do this: 

- Download the [CastleCSS Boilerplate](https://www.github.com/CastleCSS/castlecss-boilerplate). All Packages are included + examples and project setup
- Copy variables.scss from /node_modules/castlecss-core/sass/variables.scss into your own scss folder and include it into your main.scss
- Copy the example from the [documentation](http://castlecss.com/variables.html) into your own variables.scss and include it into your main.scss

## Boilerplate
If you're looking for a ready-to-go project setup, check out [CastleCSS Boilerplate](https://github.com/CastleCSS/castlecss-boilerplate/) and simply download the .ZIP. This download is extended with a basic HTML5-template and a configuration for Grunt to easily compile and minify your Sass files.

## Updating files
This front-end framework is easy updatable. This has the advantage that new features can easily be included in your project, but that your adjustments made to the dependencies itself will be overwritten with your next update, so we won't recommend doing that.

We recommend updating the dependencies as follows:
```
npm update
```

## Documentation and examples
You can find the documentation and examples at http://www.castlecss.com or [Download the boilerplate](https://github.com/CastleCSS/castlecss-boilerplate/archive/master.zip) with a ready-to-go setup.

## Setup
Your project should have a setup similar to this:

```
| Project directory/
|
|-- node_modules/
| | -- castlecss-core/
| | -- castlecss-buttons/
| | -- castlecss-notifications/
| | -- castlecss-icons/
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
|-- Gruntfile.js (or gulp, or whatever you want to use)
|-- package.json
```

With this setup you make sure that your own variables overwrite the castlecss-core variables, and that your setup is still updatable without overwriting your own modifications.

### main.scss
Your main.scss should have the following setup:

```
/* 	CastleCSS Core variables */
@import "path/to/castlecss-core/sass/variables";

/* 	Your variables */
@import "variables";

/* 	Remaining Core files and other CastleCSS modules */
@import "path/to/castlecss-core/sass/main";
@import "path/to/castlecss-buttons/sass/main";
@import "path/to/castlecss-notifications/sass/main";
@import "path/to/castlecss-icons/sass/main";

/* Include your own files below this line
   -------------------------------------- */



/* --------------------------------------
   Include your own files above this line */

@import "path/to/castlecss-core/sass/base/utility";
@import "path/to/castlecss-core/sass/base/utility_spacers";
```


## Roadmap
We're currently working hard on making the CastleCSS expansions and improvements. CastleCSS is made to serve as lightweight basis for tailor made software but we do want to give you the option to install a few modules to make your life easier.

Please see the [ROADMAP.MD](https://github.com/CastleCSS/castlecss/blob/master/ROADMAP.md) for our current plans for the future.

## Contributing
Want to contribute? We'd love your help, please take a look at the roadmap or submit new suggestions.