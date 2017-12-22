# App: Theme Setup Files

The starter template comes with the following files. You should add theme add-on configurations like *custom post types*, *custom taxonomies*, and *custom shortcodes* to this directory too. 

```
|-- app/                # -> Theme PHP
|   |-- controllers/    # -> Laravel Controllers
|   |-- admin.php       # -> Theme customizer setup
|   |-- filters.php     # -> Theme filters
|   |-- helpers.php     # -> Helper functions
|   |-- setup.php       # -> Theme setup
```

## app/setup.php
Important things in this file:
* Enqueue theme scripts and styles
* Configure Soil functions
* Register navigation menus
* Enable post thumbnails
* Enable HTML5 markup for built-in WordPress features (image captions, comments, photo galleries, and search form)
* Configure custom image sizes
* Register sidebars

## Customizations
### Post Types
Add file to `app` directory
```
|-- app/
|   |-- custom-post-types.php
```

#### Related resources:
* register_post_type() function reference: [Function Reference/register post type « WordPress Codex](https://codex.wordpress.org/Function_Reference/register_post_type)
* WordPress Post Types documentation: [Post Types « WordPress Codex](https://codex.wordpress.org/Post_Types)

### Shortcodes
Add file to `app` directory
```
|— app/
|   |— shortcodes.php
```

#### Related resources:
* add_shortcode() function reference: [Function Reference/add shortcode « WordPress Codex](https://codex.wordpress.org/Function_Reference/add_shortcode)
* WordPress Shortcodes API: [Shortcode API « WordPress Codex](https://codex.wordpress.org/Shortcode_API)
 
