## How to use the accessibility feature in browsers to apply your own style sheet.

# What are style sheets?

CSS (Cascading Style Sheets) defines the style on how different elements of HTML should get displayed. We could define various style properties to an HTML page such as bold headings, color-coded hyperlinks, text alignments each time we felt necessary for an element. However, we could find some patterns of elements or the same elements used more than once in the website sharing the same style. Selecting these patterns by defining some identifiers or class names or the elements by itself and applying the style only once would eliminate repetition of code and also makes it easy to perform any changes to them.

## Style applied at element level - Inline Style

```
<html>
<head>
</head>
<body>
<h1 style="color:yellow;">This is a heading</h1>
<p style="color:yellow;">This is a paragraph</p>
</body>
</html>
``` 

## Internal style sheet

```
<html>
<head>
<style>
h1, p {color: yellow;}
</style>
<body>
<h1>This is a heading</h1>
<p>This is a paragraph</p>
</body>
</html>
``` 

From this it is clear that the styles applied can be easily identified for any future updates when CSS is applied, moreover, these styles can be separated and placed in another file with an extension .css and linked to the main file. This keeps the code very clean by separating the document layout from its style. This kind of styling is called **external style sheets**.  

The external style sheets can be included in the HTML pages by using the following code: mystyle.css is the name of the Cascading style sheet file, which will contain the styling information - h1,p {color: yellow;}

The external style sheets are advantageous in many ways, say a website is being designed by two designers each had their own CSS files, which can later be composed to be one. They help to manage work and also make work easier when any changes are necessary.

## Accessibility

Accessibility means enabling the websites so they are easily accessible by people with disabilities. This is a very important design feature that must be considered when designing websites. Sadly, many websites nowadays are designed with accessibility barriers making them hard to use for some people. 

The following technique helps to access some of those sites by enabling the accessibility feature now directly available on a browser. Also, users can apply their own style sheet for any web page so the styling follows their accessibility needs. 

 Steps to follow are:

### Internet Explorer 

1. Go to Tools -&gt; Internet Options.
2. Click on the Accessibility button on the General tab.

![untitled-1.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1613592233605/EnyCRrZ6P.jpeg)

3\. Check the option Format documents using my style sheet, browse to the location where your style sheet is saved and click ok.

With this option saved in the browser, all the web pages will get displayed using the selected style sheet.

### Firefox

The Firefox browser supports the alternate style sheets as well, by mentioning in the web page for example:  
 &lt;link href=”default.css” rel=”stylesheet” type=”text/css” title=”Default Style”&gt;  
&lt;link href=”fancy.css” rel=”alternate stylesheet” type=”text/css” title=”Fancy”&gt;  
&lt;link href=”basic.css” rel=”alternate stylesheet” type=”text/css” title=”Basic”&gt;

The user can select the desired style by clicking the View tab in the menu of the browser and then clicking the style sub-menu provides the different alternate styles being provided by the web page. Based on the user selection, the web page will be rendered.