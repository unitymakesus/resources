---
title: Asset files
weight: 10
---

# Resources: Asset files
The starter template comes with the following directory structure and files for the front-end development. Any theme assets, such as images, fonts, CSS, and JS should be contained within the `resources/assets/` directory.

```
|-- resources/            # -> Theme assets and templates
|   |-- assets/           # -> Front-end assets
|   |   |-- build/        # -> Webpack config
|   |   |-- fonts/        # -> Theme fonts
|   |   |-- images/       # -> Theme images
|   |   |-- scripts/      # -> Theme JS
|   |   |-- styles/       # -> Theme stylesheets (SCSS)
|   |   |-- config.json   # -> Settings for compiled assets
|-- package.json          # -> Node.js dependencies and scripts, plus ESLint and StyleLint config
```

## package.json
```
|-- package.json
```

Generally, this file doesn’t need to be edited. It contains the Node.js dependencies ([which can be managed through Yarn](https://yarnpkg.com/lang/en/docs/managing-dependencies/)).

This file also manages the rules/configuration for [ESLint](https://eslint.org/docs/user-guide/configuring) and [StyleLint](https://stylelint.io/user-guide/configuration/). These will be standardized across all our projects, so don’t edit this just to suit your whims. If you would like a change to be made to the Linter configurations, it will need to be approved by the whole dev team.

### TODO: About the rules we follow

## resources/assets/config.json
```
|-- resources/
|   |-- assets/
|   |   |-- config.json
```

This file controls the different theme assets that get built. There are settings for each of:

* File locations for the main JS and CSS files
* File locations for the customizer JS file (for the [WordPress Customizer](https://developer.wordpress.org/themes/customize-api/))
* The path to the theme directory
* The local development URL. *Important: This MUST be the same as the domain name configured in your Local by Flywheel installation for this site.*
* The proxy URL that will be used by BrowserSync to automatically show file changes while developing.
* Cachebusting filename suffix formula.
* Which files BrowserSync should watch for changes in.

By default, Sage builds two JS files and one CSS file. To create additional CSS or JS files, you'll need to:

1. Create the files within the `resources/assets/scripts/` or `resources/assets/styles/` directories
2. Open `resources/assets/config.json` and add the new files to entry in a new array.

## resources/assets/fonts/
```
|-- resources/
|   |-- assets/
|   |   |-- fonts/
```
Before you go and add font files here, make sure they’re not available via [Google Fonts](https://fonts.google.com/). Any Google Fonts should be loaded with the Web Font Loader script.

This directory may contain licensed web fonts in .eot, .otf, .svg, .ttf, and .woff formats. Including as many file types as possible will help ensure cross-browser compatibility. 

### TODO: About @font-face

## resources/assets/images/
```
|-- resources/
|   |-- assets/
|   |   |-- images/
```
This directory should only contain images that are used within the theme files. Before adding images to this directory, make sure they are appropriately sized and compressed with image compression tools like [TinyPNG](https://tinypng.com/) or [SVG Minifier](http://www.svgminify.com/).

### Images in template files
Use the @asset directive to call images from template files:

```html
<img src="@asset('images/example.jpg')">
```

### Images in CSS
CSS files and images are sibling folders, so you can reference images in CSS:

```css
.background {
  background-image: url('../images/image.jpg');
}
```


### TODO: About appropriately sized images

## resources/assets/scripts/
```
|-- resources/
|   |-- assets/
|   |   |-- scripts/
|   |   |   |-- routes/			# -> Route files
|   |   |   |-- util/				# -> Utilities for DOM-based routing
|   |   |   |-- customizer.js		# -> Theme customizer JS, used only in the Customizer
|   |   |   |-- main.js			# -> Primary theme JS
```

All of the JavaScript for our projects must be written in ES6. The magic that allows for only the relevant JS to be loaded on certain pages is called DOM-based routing ([here’s an interesting article on how it works by Paul Irish](https://www.paulirish.com/2009/markup-based-unobtrusive-comprehensive-dom-ready-execution/)). The important thing to know is that each file within the `resources/assets/scripts/routes` directory contains the JS that will load on each of the configured pages.

### TODO: More on DOM-based routing, specific to our purposes

## resources/assets/styles/
```
|-- resources/
|   |-- assets/
|   |   |-- styles/
|   |   |   |-- autoload/		# -> Any files to autoload into main.scss
|   |   |   |-- common/		# -> Global style partials
|   |   |   |-- components/	# -> Component style partials
|   |   |   |-- layouts/		# -> Specific layout style partials
|   |   |   |-- main.scss		# -> Primary theme CSS, barebones partials are imported to help get your styling started
```

### TODO: SCSS standards
