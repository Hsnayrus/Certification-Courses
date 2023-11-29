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

# Units of Measurement

* A web page, as you know it, is two-dimensional.
* That means it has width and height. Multiple other ways to express this are: x and y axes, length and breadth, vertical and horizontal, etc.
* Another variable of a web page is its size, which can either be static or dynamic.
* CSS units of measurement are used to account for the dynamism and dimensionality of a web page.
* Units of measurement in CSS can be classified into two types, absolute and relative

## Absolute Units

* Are fixed across different devices and have a fixed size
* Useful for activities like printing a page
* Not so useful today for different devices since different devices have different viewport sizes
* Thus, absolute units are used when the size of the web page is known and will remain constant


| Unit | Name                | Comparison               |
|:----:|:-------------------:|:------------------------:|
|  Q   | Quarter-millimeters | 1Q = 1/40th of 1cm       |
|  mm  | Millimeters         | 1mm = 1/10th of 1cm      |
|  cm  | Centimeters         | 1cm = 37.8px = 25.2/64in |
|  in  | Inches              | 1in = 2.54cm = 96px      |
|  pc  | Picas               | 1pc = 1/6th of 1in       |
|  pt  | Points              | 1pt = 1/72nd of 1in      |
|  px  | Pixels              | 1px = 1/96th of 1in      |

* Of these, the pixels and centimeters are most frequently used for defining properties

## Relative Values

* When you create a web page, you will almost never have only a single element present inside it.
* Even in case of containers such as flexboxes and grids, there's ususally more than one element present that rules are applied to.
* Relative values are defined 'in relation' to the other elements preent inside the parent element.
* Additionally, they are defined 'in relation' to the viewport or the size of the visible web page.
* Given the dynamic nature of web pages today and the variable size of devies in use, relative unites are the go-to option in many cases.
* Below is a list of some of the important relative units

| Unit     | Description and relativity |
|:--------:|:--------------------------:|
| __em__   | Font size of the parent while present |
| __ex__   | x-co-ordinate or height of the font element | 
| __ch__   | Width of the font character | 
| __rem__  | Font size of the root element | 
| __lh__   | Value computed for line height of a parent element | 
| __rlh__  | Value computed for line height of root element which is `<html>`   | 
| __vw__   | 1% of the viewport width | 
| __vh__   | 1% of the viewport height | 
| __vmin__ | 1% of the smaller dimension of viewport | 
| __vmax__ | 1% of the larger dimension of viewport | 
| __%__    | Denotes a percentage value in relation to it's parent element | 

* Many of these units are used in terms of the relative size of fonts.
* Some Units are more suitable depending on the relative context. Like when the dimensions of the viewport are important, it's more appropriate to use __vw__ and __vh__. In a broader context, the relative units you will see most frequently used are percentage, __em, vh, vw__ and __rem__.  
* Much like the absolute and relative units discussed above, certain properties have their own set of acceptable values that need to be taken into account. For example, color-based properties such as backgroundcolor will have values such as hexadecimal, __rgb(), rgba(), hsl(), hsla()__ and so on. Each property should be explored on an individual basis and practicing with the code will help you to decide which of these units of measurement are the most suitable choice. 