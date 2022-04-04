## Modelling with Document Object Model

Document object model is the representation of all the objects of the HTML page as a tree structure. There is no specification on the documents be implemented as tree or collection of trees. It is an abstract interface which created by the browser when the page is loaded.

It helps the javascript to access the elements of the HTML page, which are called to be the objects, whose attributes are called to be the properties. Any changes to these elements can be made by calling the methods. The elements can be accessed by their id, classname or tagname.

With the help of DOM, the structure of the web page and how each elements are connected and can be traversed from one element to another is provided to the scripting lanaguage. Some browsers are providing addons under the name of DOM which when added helps to inspect the DOM of a web page in the browser. With the information obtained from the DOM, javascript can access the elements, modify the elements of the web page including the CSS style options of the elements. We can add or delete elements to the HTML page, with the knowledge of the connection between the elements. For example a tree structure define the root element, parent and child elements. Based on that we could determine which elements could be the parent, and which elements should form part of the child nodes.

DOM generate events which are activities of the browser or the browser user that are detected and computation is provided in response to those activities by the java script, being a event driven programming language. The event is the specific activity taking place, whereas event handlers is the script that is executed in response to those activities.

Some of the example of events can be click, mousemove, key press, key down. The difference between key press and key down is- when the key is pressed, the key press event occurs, whereas when the key is pressed and released the key down event has taken place. These events fire the event handler. There occurs a confusion when the parent and child node both have event handlers. When the child node event has been triggered which event handler should be fired. The elements need not be parent and child, they can be nested elements as well.  
element1  
———element2  
element 2 event handler is fired first and then element 1 event handler is triggered. This approach is known as event bubbling, the reverse triggering that is first element 1 event handler is triggered and then element 2 event handler is triggered it is known as event capturing.

In some of the situation we desire the event handling not to take place, in such cases preventDefault method could be used to prevent the action of the handler. In event bubbling, to stop the event from further propagation stopPropagation method is used on the event object.

This post realizes the importance of DOM and more details can be found at [http://www.w3schools.com/js/js\_htmldom.asp](http://www.w3schools.com/js/js_htmldom.asp "http://www.w3schools.com/js/js_htmldom.asp").