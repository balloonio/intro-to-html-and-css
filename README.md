# Intro to HTML and CSS

Learning notes and hand-ons for Udacity course [Intro to HTML and CSS](https://www.udacity.com/course/intro-to-html-and-css--ud001)

>*Throughout this course, you'll learn about the underlying structure of the web - HTML. You'll learn how to use this tree-like structure to create websites. You'll also learn how to apply styling to a website through CSS. You'll learn about CSS syntax, selectors, and units. Along the way, you'll also learn about code editors and a browser's Developer Tools.*

<table>
    <tr>
        <th>Course type</th>
        <td>Free</td>
    </tr>
    <tr>
        <th>Timeline</th>
        <td>Approx. 3 Weeks</td>
    </tr>
    <tr>
        <th>Skill level</th>
        <td>Beginner</td>
    </tr>
</table>

- [Lesson 1: HTML, CSS, and Boxes](#lesson-1-html-css-and-boxes)
  - [The First Step](#the-first-step)
  - [Quiz: Exploring the Web](#quiz-exploring-the-web)
  - [Quiz: Page Structure](#quiz-page-structure)
  - [Summary of HTML](#summary-of-html)
  - [Quiz: Visual Styling](#quiz-visual-styling)
  - [HTML-CSS-DOM](#html-css-dom)
  - [Quiz: Boxes Everywhere](#quiz-boxes-everywhere)
  - [Boxes, Grids and Rules](#boxes-grids-and-rules)
  - [Quiz: Boxifying Design](#quiz-boxifying-design)
  - [Interview with Jacques](#interview-with-jacques)
  - [Boxes To HTML](#boxes-to-html)
  - [Quiz: Creating the Files](#quiz-creating-the-files)
    - [Create Folder and File Structure](#create-folder-and-file-structure)
    - [Edit the HTML Document](#edit-the-html-document)
    - [Test the HTML File in a Browser](#test-the-html-file-in-a-browser)
  - [Quiz: Adding Style](#quiz-adding-style)
  - [Understanding CSS](#understanding-css)
    - [Search and Replace](#search-and-replace)
    - [Order Matters](#order-matters)
    - [Specifics Matter](#specifics-matter)
  - [Styling Up](#styling-up)
  - [Quiz: Using Semantic Tags](#quiz-using-semantic-tags)

## Lesson 1: HTML, CSS, and Boxes

### The First Step

Conceptually, let's think of a website as a house:  
**HTML** - **stucture** of the house, which defines where the kitchen is, where the bedroom is etc.  
**CSS** - the **style** of the house, which defines what color the walls are, how big is the carpet, what decorations are there etc.  
**Javascript** - **interactive** components of the house, for example, a garage door opener or a TV remote controller, which would change some elements of the house

### Quiz: Exploring the Web

Observing Wikipedia page structure, which of the followings is/are true?

- [ ] all elements are visible
- [x] all elements are rectangular
- [x] you can read the same texts as on the page

Though some elements are invisible (like the `<head>` element), all visible elements are rectangular. And, if you dig deep enough into the structure you can read all the text that shows up on the page.

### Quiz: Page Structure

Explain the tree structure for the html file below:

```html
<!doctype html>
<html>
    <head></head>
    <body>
        <h1>Hello, <em>Udacity student!</em></h1>
        <div>
            <img src="app.png" alt="sample image">
            <p>This is a very simple page for you to explore.</p>
        </div>
    </body>
</html>
```

### Summary of HTML

So far, we have learned how HTML classifies the page content, like where a image is or where a paragraph should be, but we haven't learn how the content is shown, like how big the font size or what image is shown, because those are not HTML's jobs.

### Quiz: Visual Styling

You can find all the examples for this course [here](http://assignments.udacity-extras.appspot.com/courses/html-css/index.html). The second example which you are supposed to check for this quiz is [Same HTML 2](http://assignments.udacity-extras.appspot.com/courses/html-css/samples/style-2.html)! This page has the same HTML file as [Same HTML 1](http://assignments.udacity-extras.appspot.com/courses/html-css/samples/style-1.html), but the look is totally different.

Learn to use developer tools to identify the font size of `h1` and the border size of the image.

### HTML-CSS-DOM

**HTML** - HyperText Markup Language - the standard markup language used to create web pages.

**CSS** - Cascading Style Sheets - style sheet language used for describing the look and formatting of a document written in a markup language.

**DOM** - Document Object Model - a cross-platform and language-independent convention for representing and interacting with objects in HTML (and other markup languages). The nodes of every document are organized in a tree structure, called the **DOM tree**.

HTML files are nothing but text files whose format follows the specific HTML syntax. The basic unit in HTML syntax is a **tag**. The browsers turn HTML tags into elements to form a tree, using DOM. HTML defines the **structure** and the **content** of a web page. Below is a typical HTML tag syntax:

```html
<!-- starting tag with attribute-->
<tag attribute-var1="attribute-value1" attribute-var2="attribute-value2">
    content (which can be empty, text, or other elements...)
<!-- ending tag -->
</tag>
```

CSS, on the other hand, is used to define the styles. For example, by using a CSS file, we can specify all the paragraph elements with attribute `class="news-body"` to use the style where font color is navy blue. We will learn how to do it later this course.

### Quiz: Boxes Everywhere

In this [page](http://assignments.udacity-extras.appspot.com/courses/html-css/samples/shapes.html), what happens when `border-radius` is unchecked?

- [ ] the circle disappeared
- [x] the circle became a square
- [ ] the circle shrank
- [ ] nothing changed

```css
.surprise, .surprise2 {
border-radius: 50%; /* try 20% also, you might find the result interesting */
display: inline-block;
}
```

### Boxes, Grids and Rules

The reason every element has a box layout is for simplicity. Think about boxes in a warehouse - the reason everything is stored in boxes is because they can stacked easily, and their location can be referred to easily. If all the warehouse storage units are of different shapes, they would be really difficult to arrange and categorize. Same thing here for web page layout.

### Quiz: Boxifying Design

Boxify a design:

- [x] drew boxes with a graphic program
- [x] doodled on a piece of paper
- [x] printed the page and drew on it
- [x] printed the page and cut with scissors

### Interview with Jacques

Jacques talked about how to boxify a design - from outer big boxes to inner small boxes.

### Boxes To HTML

Draw a pure box with `<div>`

```html
<div>My title box</div>
<div>
    <div>My image box</div>
    <div>My text box</div>
</div>
```

A way to differentiate these boxes is to use the `class` attribute. (We want to be able to differentiate the boxes because, for example, we want to apply different style to each box.) If an element is imagined to be a real paperboard box, `class` is like the label on that box. One box can have any number of lables.

```html
<div class="title">My title box</div>
<div class="app">
    <div class="screenshot">My image box</div>
    <div class="description">My text box</div>
</div>
```

### Quiz: Creating the Files

#### Create Folder and File Structure

- Create a folder for all your future web projects somewhere convenient, for example on your Desktop or in your Documents folder and call the folder “portfolio”.
- Create another folder inside it for this first page, call it “toplist”.
- Create 2 files there - index.html and style.css.

The structure should look like this:

```text
.
└───portfolio
    └───toplist
        ├───index.html
        └───style.css
```

To keep things organized we highly recommend using the file structure described above. Since many of the HTML and CSS files you'll be creating in these lessons have similar names (like `index.html`), it is recommended that you create a separate folder/directory within `portfolio` for each mockup (the suggested name for this one is `toplist`) and save the related HTML and CSS files within it.

#### Edit the HTML Document

Open the `index.html` file in your code editor, and write or copy/paste the following code and save the file:

```html
<div class="title">My title box</div>
<div class="app">
    <div class="screenshot">My image box</div>
    <div class="description">My text box</div>
</div>
```

Note: For this quiz, you are not expected to add the image or the description text.

#### Test the HTML File in a Browser

- Go to the folder, right click the file and choose “Open.. with Google Chrome”.
- Alternatively, in Chrome click "File -> Open File" and then browse to the `index.html` file and click "Open".

### Quiz: Adding Style

An HTML file needs to tell the browser where to look for the style files. Otherwise, the browser will just render with its default styles. That is exactly why we need a more complete HTML format, compared to what we've seen earlier. The `<head>` tag is used to specify some meta-data about the HTML file, in this case, the CSS style file.

```html
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" href="style.css"/>
    </head>
    <body>
        <div class="title">My title box</div>
        <div class="app">
            <div class="screenshot">My image box</div>
            <div class="description">In ac ipsum quis turpis...</div>
        </div>
    </body>
</html>
```

`style.css` looks like this:

```css
.description {
    color: red
}
```

### Understanding CSS

#### Search and Replace

You can also think about CSS as a search and replace tool: you identify a class or a tag of the element you want to find (or match, in CSS terminology), and then what you want to do with it, or what property values to replace with different ones.

#### Order Matters

It also matters where you define the rules and in what order they are applied. Styles can be defined in different places and are applied in the following order, with definitions further down the list overwriting previous definitions:

- the default style of a browser (different browsers have slightly different styles)
- stylesheet in a separate file (this is what you will be mostly using)
- stylesheet inside HTML (this can be done for small projects but is not ideal)
- inline style in an element (this can also be done but should be avoided)

#### Specifics Matter

**"Cascading"** means that rules are applied **not only** to the elements they directly match, but also to **all of those elements' child elements**. However, if a child element has multiple, overlapping rules defined for it, the **more specific rule takes effect**.

### Styling Up

The biggest key to understanding CSS is understanding **selectors**. Selectors are what allows you to target specific HTML elements and apply style to them. The best way to learn CSS is to get comfortable with the **documentations**.

[How CSS Selectors Work](https://css-tricks.com/how-css-selectors-work/)  
[MDN CSS Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)

Use the documentations above to answer the following questions:

1. Which of the following are possible values for the `font-style` property?
    - [x] italic
    - [x] normal
    - [ ] bold
    - [ ] standard

2. What property would you use to make the text look **bold**?  
    A: `font-weight` property.

### Quiz: Using Semantic Tags

[Content sectioning elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element#Content_sectioning) allow you to organize the document content into logical pieces. Use the sectioning elements to create a broad outline for your page content, including header and footer navigation, and heading elements to identify sections of content.

[Sections and Outlines of an HTML5 Document - The HTML5 Outline Algorithm](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Using_HTML_sections_and_outlines#The_HTML5_outline_algorithm)

Browsers use default stylesheets to determine how to display HTML elements. You can view the default style rules for `h1` and other elements for the following browsers:

- [WebKit (Chrome and Safari)](https://trac.webkit.org/browser/trunk/Source/WebCore/css/html.css)
- [Firefox](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)
- [Internet Explorer](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/ms757841(v=vs.85))

Because these rules differ sometimes between browsers, there are efforts to promote consistency in styles across browsers. One popular solution to this issue is using what is referred to as a CSS reset such as [`normalize.css`](http://necolas.github.io/normalize.css/).