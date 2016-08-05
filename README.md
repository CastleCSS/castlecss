# CastleCSS Core Files
![CastleCSS logo @CastleCss.com](https://www.doordarius.nl/castlecss-logo-250.png)

## What is CastleCSS?
CastleCSS a mobile first SCSS framework with modular building blocks for the web. It's also fully **updateable**! Now longer worrying if your base files are still correct. We do this for you ;)

## What is different between CastleCSS and other frameworks?
Unlike other Frameworks we don't include *everything*,  but only what you need. You don't need and want everything :):. 
You pick what you want to use. The core is a way to kickstart your website with the basic files and philosophy we believe in.

Our philosophy is mobile first, self explanatory code code and breakpoints. On the other hand we want to be able to keep you up to date with the latest version of CastleCSS, this is possible if you overwrite the defaults the way you're supposed to.

### Breakpoint CSS
We don't believe in classes like *laptop* or *small* and other device-classes that change throughout time but we define everything with **b{breakpoint}** this makes everything readable and since we use this throughout the whole framework everything feels familiar when you use it for a while. Whether it's for grid, utility classes, hiding, showing. It all starts with **b{breakpoint}**

You can overwrite these breakpoins in your own variable file.

### Breakpoints
Mobile first breakpoints (defined in variables.scss)

    .b0: 0px; (smartwatch and higher)
    .b1: 320px; (phone portait and higher)
    .b2: 480px; (phone landscape and higher)
    .b3: 768px; (tablet portait and higher)
    .b4: 1024px; (tablet landscape/desktop and higher)
    .b5: 1280px; (desktop large and higher)
    .b6: 1600px; (desktop huge and higher)

As your base you can always just use b0, only use b1 if you have a totally different markup <320px



## Included files and structure
CastleCSS Core has the following basic files to kickstart your website:

### SCSS folder structure and overwriting the CastleCSS defaults
The ideal structure of your SASS folder should be the following:

    | Your project/
    |-- sass/ 
    |  |-- Custom project specific files here
    |  |-- Main.scss //include castlecss main.scss files here first, your project specific files after that
    |  |
    |  |-- node_modules/ //CastleCSS files are automatically installed here
    |  |  |
    |  |  | castlecss-core/
    |  |  |  |
    |  |  |  |-- sass/
    |  |  |  |  |-- main.scss - include all your other SCSS files
    |  |  |  |
    |  |  |  |-- base/
    |  |  |  |  |-- reset.scss - set browser defaults to zero/none so nothing weird happends in different browsers
    |  |  |  |  |-- variables.scss - Variables for the grid, fonts, utility, etc
    |  |  |  |  |-- defaults.scss - Set default web settings
    |  |  |  |  |-- mixins.scss - Small but handy collection of mixins to use
    |  |  |  |  |-- utility.scss - Utility classes
    |  |  |  |  |-- utility_spacers.scss - Utility padding / margin classes
    |  |  |  |
    |  |  |  |-- layout/
    |  |  |  |  |--  grid.scss - *Flexbox scss grid with floating fallback*
    |  |  |  |  |--  static_files.scss - *Static files like containers*

### Main.scss
You should make your own main.scss which includes castlecss. Your main.scss could/should look similar to this if you want to use your own variables:

```
    @import 'node_modules/castlecss-core/sass/variables'; core variables
    @import 'base/variables';  // own variables
    @import '/node_modules/castlecss-core/sass/main'; //rest of core files
    // now import the rest of your scss files
```

### Overwrite CastleCSS
Of course you want to be able to set your own variables and other classes. To do this: make your own custom folder outside of node modules folder and include the files in your main.scss.

## How to install
You can install castle css with [NPM](https://nodejs.org) in your sass folder:

    npm i castlecss-core
    
### How to update
Type the following to check for updates in your sass folder:
    
    npm outdated
    

Nothing? Good! Then you're up to date
In any other case you'll get something that looks like this:

    Package         Current   Wanted   Latest   Location
    castlecss-core  1.0.0     1.1.0    1.1.0    castlecss-core

So type the following to update:

    npm update

If you didn't alter the core files it will now update.
If the updated did succeed you shouldn't get anything back from your terminal if you use *npm outdated* again

