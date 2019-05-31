---
title: Other files
weight: 15
---

# Other files
There are a bunch of files that power the theme. These are rarely edited and should only be touched if you know what you’re doing.

```
|-- config/         # -> Sage configuration 
|-- dist/           # -> Compiled theme assets (never edit)
|-- node_modules/   # -> Node.js packages (never edit)
|-- resources/
|   |-- assets/
|   |   |-- build/  # -> Webpack config
|-- vendor/         # -> Composer packages (never edit)
```

The `dist` directory contains all the built theme assets that are compiled when running yarn. These should never be edited directly, as they are deleted and recreated anytime yarn is run.

The `node_modules` directory contains packages that are managed by yarn:

```bash
# @ themes/your-theme-name/
$ yarn add <package name>
```

The `vendor` directory contains packages that are managed by Composer.
