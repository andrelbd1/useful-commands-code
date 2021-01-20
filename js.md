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
screen.pixelDepth					//Retorna a profundidade de pixels da tela.
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

#### Replace values
- Replace a content value from a element.
````bash
element.innerHTML =  new html content
````

- Replace a attribute value from a element.
````bash
element.attribute = new value	
````

- Replace a attribute value from a element.
````bash
element.setAttribute(attribute, value)	
````

- Replace element's style.
````bash
element.style.property = new style
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

