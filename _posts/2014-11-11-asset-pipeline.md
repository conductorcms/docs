---
layout: page
title: "Asset Pipeline"
category: dive
date: 2014-11-11 16:47:48
---

Conductor uses Bower and Gulp to manage assets and depdendencies. It also allows modules and themes to register their own assets that will be included 
in build scripts.

<br />
####How it works####

The Conductor source contains a core.json file which lists all assets and dependencies it needs to function in a similar way that they are listed in 
module and theme json files. 

The source also contains an asset_manifest.json file which lists all assets and dependencies from the core, the active theme, and all modules registered. This
is the file that Gulp will read from to compile the minified asset files. This file is built with the ``` php artisan module:scan ``` command. 

From there, Gulp reads all sources, backend and frontend, assets and dependencies, and builds the necessary files. 

<br />
####Asset registry examples####
<br />
#####module.json#####

```
    "assets": {
        "backend": {
            "js": [
                "resources/admin/js/**/*.js"
            ],
            "sass": [
                "resources/admin/sass/**/*.scss"
            ],
            "views": [
                "resources/admin/views/**/*.html"
            ]
        }
    }
```

#####theme.json#####

```
    "assets": {
        "sass": [
            "resources/sass/**/*.sass"
        ],
        "js": [
            "resources/js/**/*.js"
        ]
    },
    "dependencies": {
        "bower": {
            "angular": "latest"
        },
        "files": {
            "source": "./resources/vendor",
            "js": [
                "angular/angular.js"
            ],
            "css": [

            ]
        }
    }
```