<link rel="stylesheet" type="text/css" href="../assets/css/content.css">
<h1 class="custom-header">CSS</h1>

# Introduction

* Cascading Style Sheets or _CSS_, as it is most commonly referred to, is a set of rules that enhance the appearance of web pages.
* Allows better visual design and more creativity.
* Layouts is one of the most important components of designing a web page, since layouts help divide a page into different sections, thus making the page more presentable.

# CSS Web Layouts

* CSS can be used to enhance a web page by modifying __fonts, colors, layouts, size__ and other style formatting options that make the web page more presentable.
* The browser window that is visible to the user is called the __viewport__.
* The idea behind any CSS web layout is to create an optimally designed web page that has a good view port at any given point. In other words, CSS layouts are all about having the content of your webpages organized.
* When it comes to creating layouts using CSS, an important property is the __display__ property.

## Display property

* The display property specifies the type of box one would want to use for a given HTML element.

| ![alt text](./Resources/CSS/display-property.png) |
|:--:|
| _Display property's boxes_ | 

* The following class's display property would convert the displayed box to a block type.
```
#sample{
	display: block;
}
```
* There are two more types of boxes: _flexbox_ and _grid_.

## Flexbox

* Stands for flexible box
* Allows an elements block to flex into shrinking or expanding, allowing flexibility

## Grid

* Just like flex box but for two dimensions
* Used for large scale designs

# CSS Selectors

* Correspond to specific elements or element groups in an HTML document.
* There are different types of selectors, some of them being: 
	* Element or type selectors
	* ID selectors
	* Class selectors
	* Attribute selectors

## Element or Type Selectors

* Element selector allows developers to select elements based on their element type

__index.html__:

```
<p>Once upon a time...</p>
<p>In a hidden land...</p>
```
__styles.css__:

```
p{
	color: blue;
}
```

## ID selectors

* ID selectors use the _id_ attribute of the html element
* Since the id is unique within a webpage, it allows the developer to select a specific element for styling
__index.html__:
```
<span id="latest">New!</span>
```
__styles.css__:
```
#latest{
	color: white;
	background-color: blue;
}
```

## Class Selectors

* Class selectors allow you to select elements based on the class attribute applied to them
* With class selectors, you can apply rules to elements with the specified class name

__index.html__:
```
<a class="navigation">Go Back</a>
<p class="navigation">Go Forward
```
__styles.css__:
```
.navigation{
	margin: 20px;
}
```

## Attribute selectors:

* Has a few syntax variations. 
```
[attr=value]{}
[attr~=value]{}
[attr$=value]{}
[attr*=value]{}
```
among others..
* Matches the attribute or value for a given element
	* ### Attributes and values
		`<img src="first.jpg" alt="first image">`
		* _img_ is the name of the tag
		* _src_ and _alt_ are the names of its attributes
		* The actual name of the file, _first.jpg_ is the value
* With attribute selectors, one can target different attributes of the HTML document. 
* These [html](../examples/attribute-selectors.html) and [css](../assets/css/attribute-styles.css) files contain examples how one can use attribute selectors.
* Whenever there is an attribute on a webpage, one can use some sort of attribute selector to modify it.
* This makes attribute selectors a very flexible styling tool

## Nth-of-type and Nth-child selectors

* The syntax of these two selectors is very similar
* As their names suggest, these selectors target the _nth-child_ or the _nth-type_ of a specified _parent_ element
	* ### Nth-child
		* #### Syntax:
			```
			element:nth-child(n){
				property: value;
			}
			```
	* ### Nth-type
		* #### Syntax:
			```
			element:nth-of-type(n){
				property: value;
			}
			```
	* ### Parent
		* Let's say you have an unordered list element with 3 list item tags.
		```
		<ul>
			<li>One</li>
			<li>Two</li>
			<li>Three</li>
		</ul>
		``` 
		* The unordered list tag, `<ul>` is the parent tag in this case and the three `<li>` tags are the children.
* If I wanted the second list item to have a certain styling, I could use
```
li:nth-of-type(2){
	color: aqua;
}
```
__OR__
```
li:nth-child(2){
	color: aqua;
}
```

## Star(*) selector

* Just like other programming languages, `*` is used to select all the elements of the web page
* It will affect all the elements of the HTML file.
```
* {
	color: blue;
}
```
* It is especially helpful when you want to reset the default settings and styles that browsers use before applying my styling to the web page

## Group selectors

* If you want to apply the same styling to the same type of element, for example only the `h1` and `p` elements one can use group selectors
* Instead of using:
```
h1{
	color: blue;
	text-align: center;
}
p{
	color: blue;
	text-align: center
}
```
* One can use:
```
h1, p{
	color: blue;
	text-align: center;
}
```
* This is also called selector stacking
