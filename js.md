### [JavaScript](https://www.javascript.com/) code

#### Find element
- Find a element by id. Return a list of elements.
````bash
    document.getElementById(id)
````

- Find a element by name. Return a list of elements.
````bash
    document.getElementsByTagName(name)
````

- Find a element by class. Return a list of elements.
````bash
    document.getElementsByClassName(name)
````

#### Insert element
- Insert a element in the HTML document.
````bash
    document.createElement(element)
````

- Insert a element in the HTML document.
````bash
    document.appendChild(element)
````

- Insert a text for a element.
````bash
    document.createTextNode("text")
````

- Insert a element before another one
````bash
    element.insertBefore(element,elementChild)
````

#### Remove element
- Remove a element from a HTML document.
````bash
    document.removeChild(element)
````

#### Replace element
- Replace a element from a HTML document.
````bash
    document.replaceChild(element)
````

#### Get values
- Get a value from a element.
````bash
    element.value
````

- Get a value from a the first child element.
````bash
    element.firstChild.nodeValue
````

- Get a value from a child element in position 0.
````bash
    element.childNodes[0].nodeValue
````

- Get all from HTML document.
````bash
    document.documentElement.innerHTML
````

- Get all from body element.
````bash
    document.body.innerHTML
````

- Get all cookies. Return a list with key and value.
````bash
    document.cookie
````

- Get window's width. Not include toolbar and scrollbar. Return in pixels.
````bash
    window.innerWidth
    document.documentElement.clientWidth
    document.body.clientWidth
````

- Get window's height. Not include toolbar and scrollbar. Return in pixels.
````bash
    window.innerHeight
    document.documentElement.clientHeight
    document.body.clientHeight	
````

- Get screen's width. Return in pixels.
````bash
    screen.width
    screen.availWidth	
````

- Get screen's height. Return in pixels.
````bash
    screen.height
    screen.availHeight	
````

- Return the number of bits used to display a color on screen.
````bash
    screen.colorDepth	
````

- Return the deep of pixels on the screen.
````bash
    screen.pixelDepth
````

- Return URL from the current window.
````bash
    window.location.href 
````

- Return the host name from the current window.
````bash
    window.location.hostname
````

- Return the path name from the current window.
````bash
    window.location.pathname
````

- Return the protocol web (e.g., http, https) used by the current page.
````bash
    window.location.protocol
````

- Return the browser's name (e.g., IE11, Chrome, Firefox, and Safari 'Netscape').
````bash
    navigator.appName
````

- Return the browser's codename (e.g., IE11, Chrome, Firefox, and Safari 'Mozilla').
````bash
    navigator.appCodeName
````

- Return the SO used to run the current browser (e.g., Linux, Windows).
````bash
    navigator.platform
````

- Return the engine's name used on the browser.
````bash
    navigator.product
````

- Return the language set on the browser (e.g., pt-br, en-us).
````bash
    navigator.language
````

#### Replace values
- Replace a content's value from an element.
````bash
    element.innerHTML =  new html content
````

- Replace a content's value from an element specified by id.
````bash
    document.getElementById("id").innerHTML = "text"
````

- Replace a attribute's value from an element.
````bash
    element.attribute = new value	
````

- Replace a attribute's value from an element.
````bash
    element.setAttribute(attribute, value)	
````

- Replace element's style.
````bash
    element.style.property = new style
````

- Replace an attribute's value from an element specified by id.
````bash
    document.getElementById("id")."any attribute" = "text"
````

- Replace the HTML document.
````bash
    document.write(text)
````

#### Window manipulation
- Open a new window.
````bash
    window.open()
````

- Close the current window.
````bash
    window.close()	
````

- Move the current window.
````bash
    window.moveTo()
````

- Resize the current window.
````bash
    window.resizeTo()
````

- Load a new document.
````bash
    window.location.assign(URL)
````

- Display a popup.
````bash
    window.alert("text")
````

#### Console
- Display a onformation on browser's console.
````bash
    console.log(5 + 6)
````

#### Trigger
- Trigger a function after a specified time.
````bash
    window.setTimeout(function, milliseconds)
````

- Trigger a function over and over in a specified interval.
````bash
    window.setInterval(function, milliseconds)
````

- Trigger a function by a click event.
````bash
    <script>
    function myFunction()
    {	
        document.getElementById("id").innerHTML = "text";
    }
    </script>

    <tag onclick="myFunction()"> </tag>	
````

- Trigger a function to replace the HTML document by a click event.
````bash
    <tag onclick="document.write("text")">text</tag>
````

- Trigger a function to replace a content's value from an element by a click event.
````bash
    <tag onclick="this.innerHTML="text"">text</tag>
````

- Assign an event to a element through addEventListener().
````bash
    <script>
    element.addEventListener("click", displayDate);

    function displayDate() 
    {
        document.getElementById("demo").innerHTML = Date();
    }
    </script>
````
