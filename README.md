# VUEStarterkit

## Overview
vueJS components and widgets develop using html5, css flexbox.

Building [vue.js](https://vuejs.org/) components and widgets based on html5 and css flexbox.

This repository is a __work in progress__. When it's finished, you'll be able to build websites using this framework with zero effort.

The end goal is to build up a library of reusable components and widgets that are used to build a website easily.

## Requirements

* nodejs
* `sudo npm install -g gulp`

## Getting Started

Install the package via npm, all dependencies will be in the `dist` folder.

```shell
$ npm install VUEStarterkit --save
```

Or download and add the dependencies. (again all dependencies will be in the `dist` folder)

```html
<script src='vue.js'></script>
<script src='lodash-compat.js'></script>
```

Example use of components:
```html
--- will be here soon ---
```

## Get Involved

Clone the repo, then from the root folder:

1. `npm start`
1. Open [http://localhost:9080/](http://localhost:9080/) in your browser

## Creating a new component
--- will be here soon ---


## Everything in public folder is temporary!

**Important note:** Any file in public folder is copied there as part of the gulp build process.

See `src` folder for original files to edit.

## Static and Dynamic components

--- will be here soon ---

## Accessibility (a11y)

VUEStarterkit uses [a11y](http://addyosmani.github.io/a11y/) with gulp for automated accessibility testing.

Example uses:

```
# Build and audit entire component list
gulp a11y

# Skip the build process, just audit
gulp a11y-only

# Single component with all its use cases
gulp a11y --component=ux-button
gulp a11y -c ux-button
gulp a11y-only --component=ux-button

# Run only a single use case
gulp a11y --component ux-button --usecase ClickMe
gulp a11y -c ux-button -u ClickMe
gulp a11y-only --component=ux-button --usecase=ClickMe
```

Example usage (failure):

```
$ gulp a11y-only -c ux-button -u BuyNow
[17:59:54] Using gulpfile ~/dev/projects/ractive-foundation/gulpfile.js
[17:59:54] Starting 'a11y-connect'...
[17:59:55] Finished 'a11y-connect' after 139 ms
[17:59:55] Starting 'a11y-only'...
[17:59:55] Server started http://localhost:8089
[17:59:56] a11y FAIL http://localhost:8089/testRunner.html#!/component/ux-button/use-case/BuyNow

*** Begin accessibility audit results ***
An accessibility audit found
Warnings:
Warning: AX_COLOR_01 (Text elements should have a reasonable contrast ratio) failed on the following element:
#childComponent > .button
See https://github.com/GoogleChrome/accessibility-developer-tools/wiki/Audit-Rules#ax_color_01 for more information.

Warning: AX_FOCUS_03 (Avoid positive integer values for tabIndex) failed on the following element:
#childComponent > .button
See https://github.com/GoogleChrome/accessibility-developer-tools/wiki/Audit-Rules#ax_focus_03 for more information.

*** End accessibility audit results ***

[17:59:56] 'a11y-only' errored after 1.37 s One or more a11y tests failed, see log.
```

## Run on Device

### Prerequisities

You need the SDK installed for each platform you wish to target.

### Building the App

To create a Cordova app within your project:

`gulp cordova-build --android`

This will also install the Android platform if the Android SDK is installed on your machine.
The cordova project will be saved in the `/.cordova` directory.

### Run the App

To then run:

`gulp cordova-run --android`