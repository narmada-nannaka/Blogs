## How to override a CSS style from another style

When multiple CSS rules reference the same HTML element, the browser needs a rule of thumb to predict which styling instruction should take precedence. This is known as the CSS override. Depending on which selector type is used to style an element, there are certain rules that determine which style overrides another.

Let’s take a small example to understand how this is done.

HTML

```
<html>
  <head>
  </head>
  <body>
   <div>
    <p>Hello World!</p>
   </div>
  </body>
</html>
```

CSS

```
p {
color: Red;
}
```

### Class CSS Override element

The above example displays the hello world text in red color. The paragraph element specifies the styling in an external CSS. This applies to any paragraph element not just the “Hello World!” paragraph text. Now, I want to display the hello world text differently from all paragraphs. For this, I am adding a blue class as shown below:

```
<html>
  <head>
  </head>
  <body>
   <div>
    <p class="blue-class">Hello World!</p>
   </div>
  </body>
</html>
```

```
p {
color: Red;
}
.blue-class {
  color: blue;
}
```

Now, the text color changes from Red to blue confirming that a class has higher specificity compared to an element tag.

### Class Overrides Class

It is common knowledge that a class style overrides a general element style. But, do you know how one class style overrides another. This little tip will come in handy when you have multiple classes competing with each other to specify the styling for a specific element.

```
<html>
  <head>
  </head>
  <body>
   <div>
    <p class="blue-class orange-class">Hello World!</p>
   </div>
  </body>
</html>
```

```
p {
color: Red;
}
.blue-class {
  color: blue;
}
.orange-class {
  color: orange;
}
```

With the above changes, the hello world text color changes from blue to orange. **Note:** You can specify the class name in any order in the p tag but the CSS override rules suggest that the order of preference is given to the class that is defined last in [CSS](https://narmadanannaka.com/category/web-development/css/).

### Id Overrides Class

A class selector is re-usable. In other words, multiple elements can have the same class name and so the same styling. Contrarily, HTML does not let you reuse an ID. If the element you are styling has both class and id attributes, in that case, ID styling takes precedence over the class. Because other elements cannot refer to the same ID, ID selector styling is more specific compared to a class.

```
<html>
  <head>
  </head>
  <body>
   <div>
    <p id="purple-id" class="blue-class orange-class">Hello World!</p>
   </div>
  </body>
</html>
```

```
p {
color: Red;
}
.blue-class {
  color: blue;
}
.orange-class {
  color: orange;
}
#purple-id {
  color : purple;
}
```

As expected the hello world text color changes from orange to purple.

### Inline Style Overrides Id

CSS can be added to HTML as inline tags and when done the styling specified inline will take precedence over other styling instructions noted above. Now, let’s rewrite our current example by adding an inline style to the paragraph element in HTML.

```
<html>
  <head>
  </head>
  <body>
   <div>
    <p style="color:green;" id="purple-id" class="blue-class orange-class">Hello World!</p>
   </div>
  </body>
</html>
```

With the addition of an inline style, the hello world text color changes from purple to green.

### !Important CSS Override All

!Important is an important attribute that can be added to CSS styling. As the name implies, it indicates the styling it accompanies is important and can override the inline styling. !important is added at the end of the styling instruction line as done with our example below.

```
p {
  color: Red !important;
}
.blue-class {
  color: blue;
}
.orange-class {
  color: orange;
}
#purple-id {
  color : purple;
}
```

The hello world text is now displayed in red color because !important added to the p element tag styling overrides all other selector types.

You can access the code mentioned in this post from [here](https://codepen.io/narmada-nannaka/pen/oNzgWmE).