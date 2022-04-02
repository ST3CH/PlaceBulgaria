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

![unknown](https://user-images.githubusercontent.com/44115112/161381116-e1268f8e-0fe5-415d-8621-7f7ff0d010b0.png)

## Update changelog - to update replace your script with the one above

### Update 0.3
Pierog has been added ;]

![unknown (2)](https://user-images.githubusercontent.com/44115112/161382401-0603fb0b-68b7-43ec-80ad-bcba3ed27158.png)

### Update 0.3.1

Pope has been moved to right to accomodate flood of pierogies

### Update 0.3.2

Fixed some pope colors

### Update 1.0

Now your link doesn't have to change - so no more need to update script just refresh to get latest guide 
