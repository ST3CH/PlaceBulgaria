This script doesn't draw for you, it only shows guides where to draw what color.
New version 1.0 - now you won't need to update your script, latest guide will be on your screen after you refesh reddit page :D

To setup the script follow steps bellow:

1. Download TamperMonkey extension
https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo?hl=en

2. Then click on the extension the top right of Chrome (please use chrome, might not work on other browsers)

3. "Create new script" 

4. Copy this script there:

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

5. Then save by using "ctrl+s" or "command+s"

After refreshing reddit page you should see something like this:
<img width="1114" alt="image" src="https://user-images.githubusercontent.com/44115112/161381088-0804c3b3-7664-4a9e-bf2f-ed3f5d7240b2.png">
Smaller dots represent what color should be at this place. 
Happy drawing ;)
