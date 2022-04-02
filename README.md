Този скрипт не рисува за вас той само дава инструкции къде да поставите скрипта.
За да set up-нете (чрез Chrome само!):
1. Свалете това: https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo?hl=en
2. Натисни върху extension-а
3. "Create new script"
4. Копи-пейст този код (върху целия файл): 

 ```javascript
// ==UserScript==
// @name         r/poland Pope drawing
// @namespace    http://tampermonkey.net/
// @version      1.0
// @description  try to take over the canvas!
// @author       wokstym - repurposed from other subreddits
// @match        https://hot-potato.reddit.com/embed*
// @icon         https://www.google.com/s2/favicons?sz=64&domain=reddit.com
// @grant        none
// ==/UserScript==
if (window.top !== window.self) {
    window.addEventListener('load', () => {
            document.getElementsByTagName("mona-lisa-embed")[0].shadowRoot.children[0].getElementsByTagName("mona-lisa-canvas")[0].shadowRoot.children[0].appendChild(
        (function () {
            const i = document.createElement("img");
            i.src = "https://raw.githubusercontent.com/wokstym/place/master/map.png";
            i.style = "position: absolute;left: 0;top: 0;image-rendering: pixelated;width: 1000px;height: 1000px;";
            console.log(i);
            return i;
        })())

    }, false);

}
```

6. После save: ctrl + s
8. Накрая refresh reddit
