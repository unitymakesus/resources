---
title: View files
weight: 5
---

# Resources: View files
The starter template comes with the following directory structure and files for the templates. The markup is based on [HTML5 Boilerplate](http://html5boilerplate.com/) with ARIA roles for accessibility and the hNews micro format for posts.

```
|-- resources/            # -> Theme assets and templates
|   |-- views/            # -> Theme templates
|   |   |-- layouts/      # -> Base templates
|   |   |-- partials/     # -> Partial templates
|   |   |-- *.php         # -> WP blade template files
|   |-- functions.php     # -> Composer autoloader, theme includes
|   |-- index.php         # -> Never manually edit
|   |-- screenshot.png    # -> Theme screenshot for WP admin
|   |-- style.css         # -> Theme meta information
```

## Required WordPress files
There are four files required by WordPress for any theme. These are all present in the `resources/` directory and should never be moved. 

1. Theme stylesheet: `style.css`
This file contains the theme metadata, which is generated when installing the starter template.

2. Functions file: `functions.php`
This file controls theme functionality. Only thing you’ll need to be editing here is to include new files in the `app/` directory it the array of required files on line 61.

3. Default template: `index.php`
This file is deliberately blank. Never edit this.

4. Theme screenshot: `screenshot.png`
This screenshot should show the home page of the theme and may be taken from the design mockup. The recommended image size is 1200px wide by 900px tall and it should be saved in PNG format.

## Layout files
```
|-- resources/
|   |-- views/
|   |   |-- layouts/
|   |   |   |-- app.blade.php
```

We strive to keep our code DRY. To this end, we use a theme wrapper to remove all the standard repeated markup from individual templates. The default theme wrapper is `resources/views/layouts/app.blade.php`.

A theme rarely needs more than one theme wrapper. But if there are dramatic differences between templates, you can certainly create another layout file as a different theme wrapper.

## Template files
The ones that come with the starter template may not be the ones that are needed by your project. But that’s why it’s called a starter template! You get to mold it into what you need.

```
|-- resources/
|   |-- views/
|   |   |-- partials/                 # -> Template partials
|   |   |-- 404.blade.php             # -> 404 error page
|   |   |-- index.blade.php           # -> Archive page (used by blog page, category archives, author archives and more)
|   |   |-- page.blade.php            # -> Single page
|   |   |-- search.blade.php          # -> Search results page
|   |   |-- single.blade.php          # -> Single post page
|   |   |-- template-custom.blade.php # -> An example single page template
```

All the files in the `resources/views/` directory can be further extended with the [WordPress Template Hierarchy](http://codex.wordpress.org/Template_Hierarchy) — except the starter template has the extra super-powers provided by [Laravel Blade Templates](https://laravel.com/docs/5.5/blade) too! Here are some examples:

* Copy `index.blade.php` to `author.blade.php` for customizing author archives
* Copy `index.blade.php` to `home.blade.php` for customizing the Home page if you’re showing the latest posts (under Reading Settings) instead of a static front page
* Copy `index.blade.php` to `archive-gallery.blade.php` for customizing the archive page for a custom post type registered as gallery
* Copy `page.blade.php` to `front-page.blade.php` for customizing the static front page
* Copy `page.blade.php` to `page-about.blade.php` for customizing a page called About

## Template partials
The partials included in the `templates/partials/` directory are snippets of code that may be repeated across multiple templates. So in order to keep things as DRY as possible, they’re created as partials that are then included in multiple templates.

You’ll be making lots of customizations here.

```
|-- resources/
|   |-- views/
|   |   |-- partials/	
|   |   |   |-- comments.blade.php        # -> Markup for comments
|   |   |   |-- content-page.blade.php    # -> Page content markup
|   |   |   |-- content-search.blade.php  # -> Search results content markup
|   |   |   |-- content-single.blade.php  # -> Single post content markup
|   |   |   |-- content.blade.php         # -> Single post excerpt markup
|   |   |   |-- entry-meta.blade.php      # -> Single post meta markup
|   |   |   |-- footer.blade.php          # -> Footer markup
|   |   |   |-- head.blade.php            # -> <head> markup
|   |   |   |-- header.blade.php          # -> Header markup
|   |   |   |-- page-header.blade.php     # -> Page title markup
|   |   |   |-- sidebar.blade.php         # -> Sidebar markup
```

### TODO: Write Unity coding standards
