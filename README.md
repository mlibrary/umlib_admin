# umlib_admin

## This is the admin drupal theme for U-M Library sites built off of Claro. 

**Please add this theme to your Drupal full stack project using composer:**

### Setup

```
vi composer.json
```

and add the following below your drupal line in repositories

```
    "repositories": {
        "drupal": {
            "type": "composer",
            "url": "https://packages.drupal.org/8"
        },
         "umlib_admin-theme": {
             "type": "package",
             "package": {
                 "name": "mlibrary/umlib_admin",
                 "version": "1.0",
                 "type": "drupal-theme",
                 "dist": {
                     "type": "zip",
                     "url": "https://github.com/mlibrary/umlib_admin/archive/refs/heads/main.zip",
                     "reference": "main"
                 }
             }
         },
```

You may also wish to alter what directory the theme is installed in

```
    "extra": {
        "enable-patching": true,
        "patchLevel": {
            "drupal/core": "-p2"
        },
        "installer-paths": {
            "core": [
                "type:drupal-core"
            ],
            "libraries/{$name}": [
                "type:drupal-library"
            ],
            "modules/contrib/{$name}": [
                "type:drupal-module"
            ],
             "themes/contrib/{$name}": [
             "themes/{$name}": [
                 "type:drupal-theme"
             ],
```

### Install

You can now run the following to get the latest version of the umlib_base theme

```
composer require mlibrary/umlib_admin
```

### Update

To get the lastest version in an existing project, you unfortunately cannot simply run composer update. Instead run

```
composer clear-cache
composer reinstall mlibrary/umlib_admin
```
