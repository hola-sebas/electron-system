# HOW TO CREATE APP?
first you need to create index.js & icon file.

example: 
```
.
|
| - images
|       |- icon.png
| - views
|       |- index.html
| - main.js
```

then you need to modifed the installed apps file

example:
```json
{
    "apps": [
        {
            "name": "File Explorer",
            "icon_route": "/apps/FileExplorer/images/icon-file-explorer.png",
            "main_route": "/apps/FileExplorer/index.js",
            "id": "001"
        },
        {
            "name": "Internet",
            "icon_route": "/apps/navegador/images/icon-explorer.png",
            "main_route": "/apps/navegador/main.js",
            "id": "002"
        },
        {
            "name": "new app",
            "icon_route": "/apps/newApp/images/icon.png",
            "main_route": "/apps/newApp/main.js",
            "id": "003"
        }
    ]
}
```

then you need exports class with static method main

example:

```js
// file name = main.js
module.exports = class app {
    static main(){
        // the code of the app
    }
}
/**
 * IMPORTANT 
 * if you need to create a window please use the function loadWindow()
 * the html file doesn't need a full html to be declared
 * @example loadWindow('/apps/newApp/views/index.html', 200, 300, 'new app');
 */
```