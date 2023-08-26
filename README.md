# Shell Shockers Mods
This repository features shellshock.io mods that I chose to release publicly.

## Legacy Mode
```js
// ==UserScript==
// @name         Legacy Mode | Shell Shockers
// @version      3.0
// @author       Infinite Smasher
// @description  Old in-game sound effects and legacy default gun skins!
// @icon         https://raw.githubusercontent.com//InfiniteSmasher/Shell-Shockers-Mods/main/ico_egg.png
// @match        https://shellshock.io
// ==/UserScript==

(function() {
    let interval = setInterval(() => {
        if (typeof(BAWK) === "undefined" || !BAWK.sounds || !Object.keys(BAWK.sounds)) return;
        clearInterval(interval);
        BAWK.load("https://raw.githubusercontent.com//InfiniteSmasher/Shell-Shockers-Mods/main/legacy/sounds.json");
        extern.catalog.findItemsByIds([3000, 3100, 3400, 3600, 3800, 4000, 4200]).forEach(item => {
            item.item_data.meshName += "_Legacy";
        });
    }, 200);
})();
```

## Better Inventory
```js
// ==UserScript==
// @name         Better Inventory | Shell Shockers
// @version      4.0
// @author       Infinite Smasher
// @description  Inventory Upgrades - item search bar, new item themes, item randomizer, misc UI tweaks, and MOAR!
// @icon         https://raw.githubusercontent.com/InfiniteSmasher/Shell-Shockers-Mods/main/ico_egg.png
// @require      https://raw.githubusercontent.com/InfiniteSmasher/Shell-Shockers-Mods/main/inventory/htmlEdits.js
// @match        https://shellshock.io
// @run-at       document-end
// ==/UserScript==

(function() {
    let script = document.createElement('script');
    script.src = 'https://raw.githubusercontent.com/InfiniteSmasher/Shell-Shockers-Mods/main/inventory/inventory.js';
    document.head.appendChild(script);

    let style = document.createElement('link');
    Object.assign(style, {
        rel: 'stylesheet',
        href: 'https://raw.githubusercontent.com/InfiniteSmasher/Shell-Shockers-Mods/main/inventory/inventory.css'
    });
    document.head.appendChild(style);
})();
```
