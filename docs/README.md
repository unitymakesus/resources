# Site Template for Riverscapes Docs folders

This is the main template for `/docs` folders in Riverscapes. Think of it as the central theme repository where bugs get fixed. 

## Where to find things

### Site templates and HTML

* The default template that controls the large-scale page layout is:  `src/_layouts/default.html`. There can be more than one but we like to keep it simple
* The footer, sidenav and navigation stuff is in `src/_includes`. We build a lot of stuff using javascript so `src/_includes/navigation.html` is going to not be very useful.

### Editing CSS:

* `/assets/css/custom.css` for custom hackery and small changes
* `/src/scss/app.scss` for site-wide changes. These must be compiled using sass (and grunt)

### Editing Javascript

Javascript is compiled using grunt. Find the source in the `src/js` folder

## Recompiling SASS and JS

The following files are compiled and should not be tampered with:

* `assets/css/app.css`
* `assets/css/app.css.map`
* `assets/js/dist.js`
* `assets/fonts/*`

to compile them simply run `grunt` in the `src/` folder

## Creating a new site:

Copy the following files to your docs folder:

* `/assets/` This contains all your JS and css
* `/src/` (_layouts and _includes are mandatory. Everything else is optional)
* `_config.yaml` Your site settings go here
* `.gitignore` This will make sure you don't add files you shouldn't to your git repo
* `index.md` (optional)

## Updating your theme

Sometimes we may make changes to the theme. These could be cosmetic or functional. If you've customized your CSS or Javascript then you are repsonsible for merging changes yourself. These instructions only apply to a fresh site or one where the CSS, Javascript and Jekyll tempaltes haven't been customized. 

Copy the following files from this repo into your repo/docs folder

* `assets/css/app.css`
* `assets/css/app.css.map`
* `assets/js/dist.js`
* `assets/fonts/*`
* `src/_includes`
* `src/_layouts/default.html`


## Updating your favicon

Favicons used to be simple. Now, with the range of resolutions they have to support things have gotten more complicated. Here's how you generate your own

1. Find a nice sized copy of your logo that is square.
2. Go to a service like http://www.favicon-generator.org/ and upload it. It will give you the following files in a zip: `android-icon-144x144.png`, `apple-icon-114x114.png`, `apple-icon-60x60.png`, `favicon-16x16.png`, `ms-icon-150x150.png`, `android-icon-192x192.png`, `apple-icon-120x120.png`, `apple-icon-72x72.png`, `favicon-32x32.png`, `ms-icon-310x310.png`, `android-icon-36x36.png`, `apple-icon-144x144.png`, `apple-icon-76x76.png`, `favicon-96x96.png`, `ms-icon-70x70.png`, `android-icon-48x48.png`, `apple-icon-152x152.png`, `apple-icon-precomposed.png`, `favicon.ico`, `android-icon-72x72.png`, `apple-icon-180x180.png`, `apple-icon.png`, `manifest.json`, `android-icon-96x96.png`, `apple-icon-57x57.png`, `browserconfig.xml`, `ms-icon-144x144.png`
3. put these files in the folder `assets/images/favicons`

Now you're ready to link them up. Open `src/_layouts/default.html` and add the following lines:

```html
      <link rel="apple-touch-icon" sizes="57x57" href="{{ site.baseurl }}/assets/images/favicons/apple-icon-57x57.png">
      <link rel="apple-touch-icon" sizes="60x60" href="{{ site.baseurl }}/assets/images/favicons/apple-icon-60x60.png">
      <link rel="apple-touch-icon" sizes="72x72" href="{{ site.baseurl }}/assets/images/favicons/apple-icon-72x72.png">
      <link rel="apple-touch-icon" sizes="76x76" href="{{ site.baseurl }}/assets/images/favicons/apple-icon-76x76.png">
      <link rel="apple-touch-icon" sizes="114x114" href="{{ site.baseurl }}/assets/images/favicons/apple-icon-114x114.png">
      <link rel="apple-touch-icon" sizes="120x120" href="{{ site.baseurl }}/assets/images/favicons/apple-icon-120x120.png">
      <link rel="apple-touch-icon" sizes="144x144" href="{{ site.baseurl }}/assets/images/favicons/apple-icon-144x144.png">
      <link rel="apple-touch-icon" sizes="152x152" href="{{ site.baseurl }}/assets/images/favicons/apple-icon-152x152.png">
      <link rel="apple-touch-icon" sizes="180x180" href="{{ site.baseurl }}/assets/images/favicons/apple-icon-180x180.png">
      <link rel="icon" type="image/png" sizes="192x192"  href="{{ site.baseurl }}/assets/images/favicons/android-icon-192x192.png">
      <link rel="icon" type="image/png" sizes="32x32" href="{{ site.baseurl }}/assets/images/favicons/favicon-32x32.png">
      <link rel="icon" type="image/png" sizes="96x96" href="{{ site.baseurl }}/assets/images/favicons/favicon-96x96.png">
      <link rel="icon" type="image/png" sizes="16x16" href="{{ site.baseurl }}/assets/images/favicons/favicon-16x16.png">
      <link rel="manifest" href="{{ site.baseurl }}/assets/images/favicons/manifest.json">
      <meta name="msapplication-TileColor" content="#ffffff">
      <meta name="msapplication-TileImage" content="{{ site.baseurl }}/assets/images/favicons/ms-icon-144x144.png">
      <meta name="theme-color" content="#ffffff">

```

be really careful about the paths here. Too many broken links and it starts to affect your google ranking. 