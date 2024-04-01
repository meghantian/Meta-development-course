In this module you will learn how to construct HTML documents and add basic styling and layout using CSS.
# HTML 
- structure
- common HTML tags 
    - Headings: h1, h2, ...h6
    - Paragraphs: p
    - Line breaks: br
    - Lists: ul, ol
    - Texts: strong, b, em, i
    - Content divison: div
    - Link documents: a
    - Images: img
    - Tables: table, tr,td
    - Forms: form
- What is DOM?
- Web accessiblity

## structure
HTML stands for Hypertext Markup Language, which defines the basic frame of a webpage.Hypertext is text which contains links to other text,Markup refers to tags and elements used within a document.

Each HTML element consists of an opening tag enclosed in angle brackets.Most elements are paired with a closing tag. Elements can also be empty or self-closing tag, meaning they don't have a closing HTML tag.At the end of a self-closing tag, you simply add a right angle bracket or type a forward slash right before it.
<br>
`<p> This is a paragraph </p>`
<br>
`<p> This is a <br/> paragraph </p>`
<br>The rules and structure for elements and tags are known as the HTML specification. The HTML spec is maintained by the World Wide Web, or W3C.  Whenever the HTML spec changes, a new version of HTML is standardized, the current version is HTML5.


In the head element, you add information or metadata about the HTML documents. 
<br>
In the body element, you add content you want to display on the webpage.
Let me give a HTML example.
```
<!DOCTYPE html>
<html>
    <head>
        <title>Little Lemon</title>
    </head>
    <body>
        <h1>Our Menu</h1>
        <h2>Falafel</h2>
        <h2>Pasta Salad</h2>
    </body>
</html>
```

**Please attention**, **nothing** inside the head element is displayed on the webpage in the web browser. For example, inside the head tag, you always create the title elements. This is the title that is displayed in the web browser tab.

# CSS
- structure
- common selector format
- common properties
- Box model
- Document flow: block vs inline

## structure
CSS refers to Cascading Style Sheet. CSS rule includes selctor and declaration block which is made up of properties and their values.

## common selector format
When styling a web page, there are many types of selectors available that allow developers to be as broad or as specific as they need to be when selecting HTML elements to apply CSS rules to.<br> Let me list some of them. Please combine the example of source code in the *example* folder.
1. Element selctors. The element selector allows developers to select HTML elements based on their element type. **Like "h1" selector in the above example.**
2. ID selectors. The ID selector uses the id attribute of an HTML element. Since the id is unique within a webpage, it allows the developer to select a specific element for styling. ID selectors are prefixed with a # character. **Like "#header1" selector.**
3. Class selectors. Elements can also be selected based on the class attribute applied to them. The CSS rule has been applied to all elements with the specified class name. The class selector is prefixed with a . character.
4. Element with Class Selector. A more specific method for selecting HTML elements is by first selecting the HTML element, then selecting the CSS class or ID. **Like "p.navigation" selector.**
5. Descendant Selectors. Descendant selectors are useful if you need to select HTML elements that are contained within another selector. **Like "#blog h1" and "#blog div h1" selector.**
6. Child Selectors.Child selectors are more specific than descendant selectors. They only select elements that are immediate descendants (children) of a selector (the parent).**Like "#blog > h1" selector.**
7. :hover Pseudo-Class. A special keyword called a pseudo-class allows developers to select elements based on their state. **Like "a:hover" selector.**
8. Other Selectors

## common properities
About common properities like text color and alignment.

## Box model
When an HTML document and CSS style sheet are downloaded, the web browser needs to know how to display the elements on the screen. To do this, it allocates a rectangle or box to each element. CSS rules are applied to the boxes of the elments. This is known as the box model.
![alt text](https://github.com/HannahTin/Front-end-Series/blob/main/pcs/boxmodel.jpg)
Each box consists of 4 parts: the content, the padding, the border and the margin. The content is actually the content of the element.Its size is known as content width and content height. By default, browsers are clever and will calculate the width and height based on the content itself. We can also control the size to manipulate the layout by using the following css rules.
```
width:1px;
min-width:1px;
max-width:2px;
height:1px;
min-height:1px;
max-height:2px;
```
The padding extends the content size.<br>
The border goes around the padding and content. An HTML element is equal to the size of the border box. <br>
The margin is the empty space keeping elements apart. <br>
## Document flow: block vs inline
How does the web browser know where to place the elements on the screen? The web browser normal way of calculating the position of html elements on the screen is called document flow. By default, nearly all html elements are organized into one of two catergories namely in block and inline elements.

A block level element will occupy the full horizontal width of its parent element and the vertical height of its content. Each block level element will have a new line before and after. Therefore, multiple block level element will stack on top of each other like a stack of boxes. Examples include div, form and headings.

Inline elements only occupy the width and height of their content. They don't appear on a new line.Examples include a, img, input, label, b, i, em, span.

We can change the *display* property to switch the block or inline elements.