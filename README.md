# Template Aries Bootstrap HTML

[Live Demo](https://wowthemesnet.github.io/template-aries-bootstrap-html/)

Aries is a [Bootstrap](https://getbootstrap.com/) 4.0 template designed and developed by [WowThemesNet](https://www.wowthemes.net/) and distributed by [Bootstrap Starter](https://bootstrapstarter.com/). The theme is built with Sass, concatenation, minification, autoprefixer, Browsersync, hot reloading and sourcemaps all runned by [Gulp](https://gulpjs.com/). A great Bootstrap starter template for both, beginnners and developers.

![aries theme](assets/img/screenshot.jpg)

## Beginners

- [Download](https://github.com/wowthemesnet/template-aries-bootstrap-html/archive/master.zip)
- Extract and copy "docs" folder, this is the only one you'll need.
- Get Started:
 - open index.html in your browser to visit the homepage
 - assets/css/theme.css - add/edit your custom CSS
 - assets/js/theme.js - add/edit your custom JS

## Developers

- Clone this repo: `git clone https://github.com/wowthemesnet/template-aries-bootstrap-html.git`
- Navigate into the repo directory: `cd template-aries-bootstrap-html`
- Install all node packages: `npm install`
- Get started:
    - `gulp serve` - starts localhost server with browser-sync, watches html sass js with hot reloading
    - `gulp` - minify css/js and builds your app into the docs directory, ready for production
    - `header` and `footer` are edited via `partials` folder ONLY. Any change you make here will automatically update all your files, so you don not have to manually modify them each time edit your menu (as an example). The output in the main files will be wrapped between:
    ~~~javascript
    <!-- inject:partials/header.html -->
    <!-- endinject -->
    ~~~
    ~~~javascript
    <!-- inject:partials/footer.html -->
    <!-- endinject -->
    ~~~
    So, make sure you do not touch anything between these tags in the main files. Just edit your header in footer in `partials` and simply watch the changes.

## Requirements

This project requires you to have a installation of [nodejs](https://nodejs.org/en/) with [npm](https://www.npmjs.com/get-npm)
This project also requires you to have global installations of [gulp](http://gulpjs.com/).

Install gulp globally:

`npm install -g gulp`

## Gulp commands

**gulp serve**

The gulp serve command starts a local Browsersync server that serves your files in the browser.
It automatically reload the current page when changing html, sass and js files.
The output of all sass files go to main.css.
All js files are concatenated into main.js.
You can access the project live in development with other devices on the same network. Go to the "External" address specified by Browsersync in the terminal in the browser of your device.

`gulp serve`

**gulp (build)**

The default gulp command is set to creating a "docs" directory with a production version of the project, ready to be deployed.
It minifies and renames js/css assets as well as cleaning the old "docs" directory. CSS is autoprefixed for the latest two browser versions.

`gulp`

**gulp concatScripts**

The gulp concatScripts command combines the specified js ressources into main.js.
You can add new js files to this command on line 16 in gulpfile.js
You might want to run concatScripts once seperately after adding new js files.

`gulp concatScripts`

## Overwriting Bootstrap sass variables

You can overwrite specific bootstrap sass variables by uncommenting lines in `assets/css/1-frameworks/bootstrap/bootstrap-user-variables.scss`