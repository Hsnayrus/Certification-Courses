<link rel="stylesheet" type="text/css" href="../../../../SupportingFiles/content.css">
<h1 class="custom-header">HTML</h1>

# Introduction

* HTML is a markup language that was introduced in 1990.
* Its the most basic and fundamental language that helps build and display contents of a webpage.


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
* A list of all HTML tags and their documentation can be found [here](https://www.w3schools.com/tags/default.asp).
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
![alt text](/Coursera/Meta-Back-End-Developer/Meta-The-Full-Stack/Documents/Resources/HTML/basicHTMLPage.png)
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


# Best Practices

* When writing HTML, it is good practices to semantically describe the content. This allows search engines and accessibility software to understand the contents of a page.
    * This can be done using basic HTML tags. E.g. Using the `<h1>` heading tag describes that the content is a heading.
* It is standard practice for developers to specify their links as an unordered list `<ul>` inside the `<nav>` element.
