## Scripting with javascripts

This post explains how to embed scripting languages into the web pages and mainly it narrows down to the java script scripting language.

At the start web sites are used to display general information. Later on it became a media to collect information and this information is mainly from customers and information from customers. This required more logic, to be performed by the web sites, which is not just possible with HTML. To provide more features not only for information collection, but also to validate information and display information, scripting languages are used at the client (browser) side and server side. The scripting languages are like programming languages executed by the browser during the loading of web page. These scripts can be either part of the HTML or linked to the web page externally just like the cascading style sheets as discussed in the previous post.

In this post we will mainly focus on explaining how the scripts can be included using the java script.

Scripts included internally and externally into the html pages are enclosed within the &lt;script&gt; and &lt;/script&gt; tags. Wherever the logic is required at that position the scripts can be embedded in the html page. For example  
&lt;html&gt;  
&lt;body&gt;  
&lt;script&gt;  
document.write(“&lt;h1&gt;Welcome to my page&lt;/h1  
&lt;/script&gt;  
&lt;/body&gt;  
&lt;/html&gt;

The same above content can be included externally to the html page by saving the line or the content between the scripts tags in a file as filename.js

&lt;html&gt;  
&lt;body&gt;  
&lt;script src=”filename.js”&gt;&lt;/script&gt;  
&lt;/body&gt;  
&lt;/html&gt;  
The script can be placed in the head or the body section, it functions at the place where it is placed.

Just like any programming language, javascript is a lightweighted language which supports the display of outputs as shown above to the web page and processes the input, supports comparison operators, if condition statement and loops as well.

Generally in any programming language, the most common used operators are:

- <span style="font-style: inherit; line-height: 1.625;">==</span>
- <span style="font-style: inherit; line-height: 1.625;">!=</span>
- <span style="font-style: inherit; line-height: 1.625;">&lt; </span>
- <span style="font-style: inherit; line-height: 1.625;">&gt;</span>
- <span style="font-style: inherit; line-height: 1.625;">&lt;=</span>
- <span style="font-style: inherit; line-height: 1.625;"> &gt;=</span>

Apart from these operators, java script also supports operators ===, which means it checks not only for the value but also for the type. When both are same, then only it passes as true, same goes with !== means it not equal to value and type as well.

The conditional statements that are supported include:  
**if..statement:**  
use this statement when there is only a condition to be checked under which specific code has to be implemented.  
**if… else.. statement:**  
use this statement when there is a statement to be executed when the condition is true and another statement when the condition is false.  
**if.. else if.. else.. statement:**  
use this statement to select one of many statements to be executed when the specified condition is true.  
**switch.. statement:**  
this statement is used to select a block of statements to be executed from many.

Iteration statements have their own place in any programming languages, similarly in java script we have:  
**for loop:**  
Example:  
for(var i=0;i&lt;arrayname.length;i++)  
{  
document.write(arrayname\[i\]);  
}  
**while loop**  
while(condition)  
{  
block of statements to be executed  
}

We divide the program into a block of statements and call it wherever necessary any number of times, without repeating the lines of code at each place with the help of functions. The syntax for the usage of functions in java script is:  
function functionname(argument1, argument2,..)  
{  
block of statements to be executed;  
return value;  
}  
This function can be called included in the rest of the script where it needs to be called and so in the html page as well. The return value, arguments of the function are optional, which can be used as per the logic. However when calling the function the number of arguments and the order of arguments should be correct. The return statement return the value to the place where the function is called.

This is a very brief summary of the concepts of javascript, it has a vast list of features it could provide with its usage which can be explored more at your interest.