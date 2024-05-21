# Troll your friends

Troll your friends is a jscript that you put on tampermonkey, and what does it do?

The script changes the stuff position on screen when hover the mouse over, making impossible to click on it, its good to have some fun of your friends.


```js
// ==UserScript==
// @name         Troll your friends!
// @namespace    http://tampermonkey.net/
// @version      0.1
// @description  Troll your friends with this script that change the position of stuff in screen when they hover the mouse over!
// @author       to do
// @match        https://*/
// @grant        none
// ==/UserScript==

(function() {
    'use strict';

    // Your code here...
    const randomizer = (event) => {
        const a = Math.floor(Math.random() * -1000)
        const b = Math.floor(Math.random() * 100)
        const c = document.querySelectorAll('a')
        event.target.setAttribute('style',`
        position: relative;
        margin-left: ${a}%;
        margin-right: ${a}%;
        margin-top: ${b}vh;
        `)
    }
    const c = document.querySelectorAll('a')
    c.forEach( (d) => { d.addEventListener('mouseover', randomizer) } )
})();
```
