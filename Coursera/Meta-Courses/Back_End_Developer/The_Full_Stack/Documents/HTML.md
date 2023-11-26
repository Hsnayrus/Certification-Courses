<link rel="stylesheet" type="text/css" href="../../../../SupportingFiles/content.css">
<h1 class="custom-header">HTML</h1>

<h1 class="toc-header">Table of Contents</h1>
<ul>
    <li><a href="#introduction">Introduction</a></li>
    <li>
    <a href="#basic-html-page-structure">Basic HTML page Structure</a>
        <ul>
            <li><a href="#header-header">Header Tag</a></li>
            <li><a href="#main-content-main">Main Content</a>
                <ul>
                    <li><a href="#article-element-article">Article Tag</a></li>
                    <li><a href="#section-element-section">Section Element</a></li>
                </ul>
            </li>
            <li><a href="#footer-element-footer">Footer Tag</a></li>
        </ul>
    </li>
    <li><a href="#best-practices">Best Practices for writing HTML Documents</a></li>
</ul>



# Introduction

* HTML is a markup language that was introduced in 1990.
* Its the most basic and fundamental language that helps build and display contents of a webpage.
* A list of all HTML tags and their documentation can be found [here](https://www.w3schools.com/tags/default.asp).
* Another HTML tag cheatsheet can be found [here](https://www.coursera.org/learn/the-full-stack/supplement/guED4/semantic-html-cheat-sheet).
* An HTML Page is a basic structure which consists of different components such as tags and elements.

## HTML:

* Stands for Hypertext Markup Language
    * Hypertext: Text which contains links to other elements.
    * Markup: Refers to tags and elements used within a document.
* Simply a text file with a specific structure. 
* This structure consists of differnet components such as tags and elements.
* Have the `.html` suffix.
* Whenever you go to a website, the first page that often gets returned is called _index.html_.
* If you want to learn how to tell the browser to show the webpage content, learn ___CSS___.

# Basic HTML Page Structure

```
<!DOCTYPE html>
<html>
    <head>
    </head>
    <body>
    </body>
</html>
```

* Other tags such as `<main></main>, <footer></footer>` etc. can be used to describe a typical HTML page.
* A normal website can look something like this:
```
<!DOCTYPE html>
    <head>
    </head>
    <body>
        <header>
        <!-- Contains the header of a page, e.g. Your company name: Apple -->
        </header>
        <main>
        <!-- Main content of the web page -->
        </main>
        <footer>
        <!-- Social media links, contact us, etc.  -->
        </footer>
    </body>
</html>
```
* As can be seen above, the `<body>` element has 3 main elements, `<header>`, `<main>`  and `<footer>`, as shown in <a href="#basic-html-page-structure"></a>.
* It is important to note that semantic elements are not limited to this structure. Elements can be nested inside each other if it accurately describes the content. 

## Header `<header>`

* Usually contains thing such as company logos and navigation links. 
* The main navigation section of a webpage can also be defined semantically, using `<nav>` tags.

| ![alt text](/Coursera/Meta-Back-End-Developer/Meta-The-Full-Stack/Documents/Resources/HTML/basicHTMLPage.png) |
|:--:|
| *Webpage with `<header>`, `<main>` and `<footer` tags*| 
* The `<nav>` element is used after the `<header>` element(which is used for logos).
* An example for this:
```
<!DOCTYPE html>
    <head>
    </head>
    <body>
        <header>
            <nav>
                <ul>
                    <li><a href="#home">Home</a</li>
                    <li><a href="#about">About</a</li>
                    <li><a href="#contact">Contact</a</li>
                </ul>
            </nav>
        </header>
    </body>
</html>
```


## Main Content `<main>`

* The two key semantic elements for your main content are the following elements:
    * Article
    * Section

### Article Element `<article>`

* The HTML specification states that "According to the World Wide Web Consortium's website, the `<article>` element indicates content which represents a _complete_ or _self-contained_ composition in a document page application or site that is _independently distributable_. 
    * Imagine articles in a newspaper. There are many articles on a page and you can cut out the individual articles with scissors if you want to. The `<article>` element can be thought of in this way. Examples would be:
        * Forum Post
        * User Comment
        * Article
        * Blog post
        * Interactive widget
        * Or any other independent item of content
* You should place your `<article>` within your `<main>` element.
* Example of how an `<article>` element can be used:
    * Say you are developing a blog about some holiday. Its good practice to contain the blog content inside the `<article>` element since it's a complete self-contained composition on a web-page.
    ```
    <body>
        <header>
        </header>
        <main>
            <article>
                <h2>This is my heading</h2>
                <p>My paragraph is gonna start like this</p>
            </article>
        </main>
        <footer>
        </footer>
    </body>
    ```
    * The reason for doing it this way is that the `<main>` element semantically represents the main content of a page. Inside there can be multiple `<article>` elements for things such as blog post lists.

### Section Element `<section>`

* You can add `<section>` elements to individually define sections of the article.
    * Should contain heading elements, e.g. `<h1>`, `<h2>`, etc. to semantically describe the section. 
* Doesn't require the `<article>` element. It all depends on how you want to semantically describe the page.

## Footer Element `<footer>`

* The footer element contains additional links or other content.
* Its usually at the end of the document.



# Tags and Elements:

* Each HTML element, consists of an opening tag enclosed in angle brackets. 
    * To create a paragraph, you type `<p>`.
* Most elements are paired with a closing tag, which has a `/` after the left angle bracket.
    * The closing tag for paragraphs would be, `</p`.
* HTML tags usually have some content inside them. Example:
    ```
    <p>This is a paragraph</p>
    ```
    Would generate something like this:

    <p>This is a paragraph</p>
* HTML elements can also contain other elements.
    ```
    <p>This is a <i>paragraph</i></p>
    ```
    _index.html_:
    <p>This is a <i>paragraph</i></p>

    * `<i>` is the italics element.
* Elements can also be self-closing, where the do not require the closing tag. 
    ```
    <p>This is a <br>paragraph</p>
    ```
    _index.html_:
    <p>This is a <br>paragraph</p>
    
    * Another way to 'close' the self-closing tag is to type a `/` before the right-angled bracket. `<br/>`.
* The rules and structure for elements and tags are known as the HTML specifiction. The HTML specification is managed by the world wide web consortium or __w3c__. 
* Whenever the HTML specification changes, a new version of HTML is standardized.
* The current version is HTML5.


# Best Practices

* When writing HTML, it is good practices to semantically describe the content. This allows search engines and accessibility software to understand the contents of a page.
    * This can be done using basic HTML tags. E.g. Using the `<h1>` heading tag describes that the content is a heading.
* It is standard practice for developers to specify their links as an unordered list `<ul>` inside the `<nav>` element.