# Shell Shockers Mods
This repository features some mods that I made for [Shell Shockers](https://shellshock.io). Enjoy!\
(You'll need to install the [Tampermonkey](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo) extension to use these mods)

<details open>
<summary>Better Inventory</summary>

```js
// ==UserScript==
// @name         Better Inventory | Shell Shockers
// @version      4.0
// @author       Infinite Smasher
// @description  Inventory Upgrades - new item themes, skin randomizer, UI improvements, and MOAR!
// @icon         https://raw.githubusercontent.com/InfiniteSmasher/Better-Inventory/main/ico_egg.png
// @require      https://raw.githubusercontent.com/InfiniteSmasher/Better-Inventory/main/htmlEdits.js
// @match        *://*shellshock.io/*
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
</details>

<details>
<summary>Legacy Mode</summary>

### Legacy Mode (w/ SFX Settings Toggle)
> Legacy default weapon skins with a toggle for sound effects in the settings menu
```js
// ==UserScript==
// @name         Legacy Mode (w/ SFX Toggle in Settings) | Shell Shockers
// @version      4.0
// @author       Infinite Smasher
// @description  Go back in time with a settings toggle for the old in-game sound effects (2018/2019) and legacy default gun skins!
// @icon         https://raw.githubusercontent.com/InfiniteSmasher/Legacy-Mode/main/ico_egg.png
// @match        *://*shellshock.io/*
// @run-at       document-body
// ==/UserScript==

(function() {
    let script = document.createElement('script');
    script.src = 'https://cdn.jsdelivr.net/gh/InfiniteSmasher/Legacy-Mode@latest/legacy2.js';
    document.head.appendChild(script);
})();
```
    
### Legacy Mode (Basic)
> Legacy default weapon skins and sound effects - always on!
```js
// ==UserScript==
// @name         Legacy Mode | Shell Shockers
// @version      3.0
// @author       Infinite Smasher
// @description  Go back in time with the old in-game sound effects (2018/2019) and legacy default gun skins!
// @icon         https://raw.githubusercontent.com/InfiniteSmasher/Legacy-Mode/main/ico_egg.png
// @match        *://*shellshock.io/*
// @run-at       document-end
// ==/UserScript==

(function() {
    let script = document.createElement('script');
    script.src = 'https://cdn.jsdelivr.net/gh/InfiniteSmasher/Legacy-Mode@latest/legacy1.js';
    document.head.appendChild(script);
})();
```

</details>

<details>
<summary>Egg Color Slider</summary>

### Egg Color Slider (VIP-Exclusive)
> Egg color slider in inventory (locked for non-VIPs)
```js
Coming Soon!
```

### Egg Color Slider (Unlocked)
> Egg color slider in inventory (always unlocked!)
```js
Coming Soon!
```
</details>

<details>
<summary>Hide HUD</summary>

```js
// ==UserScript==
// @name         Hide HUD | Shell Shockers
// @version      1.0
// @author       Infinite Smasher
// @description  Adds a toggle in the settings menu to hide the HUD elements (in-game/spectate UI)
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

</details>

<details>
<summary>Speedrun Timer</summary>

```js
// ==UserScript==
// @name         Speedrun Timer | Shell Shockers
// @version      1.0
// @author       Infinite Smasher
// @description  Adds a visible speedrun timer to the readouts while spawned - useful for speedruns ofc!
// @icon         https://raw.githubusercontent.com/InfiniteSmasher/Speedrun-Timer/main/ico_egg.png
// @match        *://*shellshock.io/
// @match        *://*shellshock.io?*
// @run-at       document-end
// ==/UserScript==

(function() {
    let script = document.createElement('script');
    script.src = `https://cdn.jsdelivr.net/gh/InfiniteSmasher/Speedrun-Timer@latest/timer.js?ts=${new Date().getTime()}`;
    document.head.appendChild(script);
})();
```
</details>
