# Shell Shockers Mods
This repository features some mods that I made for [Shell Shockers](https://shellshock.io). Enjoy!\
(You'll need to install the [Tampermonkey](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo) extension to use these scripts)

## Better Inventory
```js
// ==UserScript==
// @name         Better Inventory | Shell Shockers
// @version      4.0
// @author       Infinite Smasher
// @description  Inventory Upgrades - new item themes, skin randomizer, UI improvements, and MOAR!
// @icon         https://raw.githubusercontent.com/InfiniteSmasher/Better-Inventory/main/ico_egg.png
// @require      https://raw.githubusercontent.com/InfiniteSmasher/Better-Inventory/main/htmlEdits.js
// @match        *://shellshock.io/*
// @run-at       document-end
// ==/UserScript==

(function() {
    let script = document.createElement('script');
    script.src = 'https://cdn.jsdelivr.net/gh/InfiniteSmasher/Better-Inventory@latest/inventory.js';
    document.head.appendChild(script);

    let style = document.createElement('link');
    Object.assign(style, {
        rel: 'stylesheet',
        href: 'https://cdn.jsdelivr.net/gh/InfiniteSmasher/Better-Inventory@latest/inventory.css'
    });
    document.head.appendChild(style);
})();
```

## Legacy Mode (Basic)
```js
// ==UserScript==
// @name         Legacy Mode | Shell Shockers
// @version      3.0
// @author       Infinite Smasher
// @description  Go back in time with the old in-game sound effects (2018/2019) and legacy default gun skins!
// @icon         https://raw.githubusercontent.com/InfiniteSmasher/Legacy-Mode/main/ico_egg.png
// @match        *://shellshock.io/*
// ==/UserScript==

(function() {
    let script = document.createElement('script');
    script.src = 'https://cdn.jsdelivr.net/gh/InfiniteSmasher/Legacy-Mode@latest/legacy1.js';
    document.head.appendChild(script);
})();
```

## Legacy Mode (w/ SFX Settings Toggle)
```js
// ==UserScript==
// @name         Legacy Mode (w/ SFX Toggle in Settings) | Shell Shockers
// @version      4.0
// @author       Infinite Smasher
// @description  Go back in time with a settings toggle for the old in-game sound effects (2018/2019) and legacy default gun skins!
// @icon         https://raw.githubusercontent.com/InfiniteSmasher/Legacy-Mode/main/ico_egg.png
// @match        *://shellshock.io/*
// ==/UserScript==

(function() {
    let script = document.createElement('script');
    script.src = 'https://cdn.jsdelivr.net/gh/InfiniteSmasher/Legacy-Mode@latest/legacy2.js';
    document.head.appendChild(script);
})();
```

## VIP Color Slider
```js
(Coming Soon!)
```

## Hide HUD
```js
// ==UserScript==
// @name         Hide HUD | Shell Shockers
// @version      1.0
// @author       Infinite Smasher
// @description  Adds a toggle to hide the HUD elements (in-game/spectate UI)
// @icon         https://raw.githubusercontent.com/InfiniteSmasher/Hide-HUD/main/ico_egg.png
// @match        *://*shellshock.io/*
// @run-at       document-end
// ==/UserScript==

(function() {
    let script = document.createElement('script');
    script.src = 'https://cdn.jsdelivr.net/gh/InfiniteSmasher/Hide-HUD@latest/hideHud.js';
    document.head.appendChild(script);
})();
```
