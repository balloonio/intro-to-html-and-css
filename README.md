Learning notes and hand-ons for Udacity course *Intro to HTML and CSS*

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

# Lesson 1: HTML, CSS, and Boxes

## The First Step

Conceptually, let's think of a website as a house:  
**HTML** - **stucture** of the house, which defines where the kitchen is, where the bedroom is etc.  
**CSS** - the **style** of the house, which defines what color the walls are, how big is the carpet, what decorations are there etc.  
**Javascript** - **interactive** components of the house, for example, a garage door opener or a TV remote controller, which would change some elements of the house

## Quiz: Exploring the Web

Observing Wikipedia page structure, which of the followings is/are true?

- [ ] all elements are visible
- [x] all elements are rectangular
- [x] you can read the same texts as on the page

Though some elements are invisible (like the 'head' element), all visible elements are rectangular. And, if you dig deep enough into the structure you can read all the text that shows up on the page.

## Quiz: Page Structure

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

## Summary of HTML

So far, we have learned how HTML classifies the page content, like where a image is or where a paragraph should be, but we haven't learn how the content is shown, like how big the font size or what image is shown. 

## Quiz: Visual Styling

You can find all the examples for this course [here](http://assignments.udacity-extras.appspot.com/courses/html-css/index.html). The second example which you are supposed to check for this quiz is [Same HTML 2](http://assignments.udacity-extras.appspot.com/courses/html-css/samples/style-2.html)! This page has the same HTML file as [Same HTML 1](http://assignments.udacity-extras.appspot.com/courses/html-css/samples/style-1.html), but the look is totally different.

Learn to use developer tools to identify the font size of `h1` and the border size of the image.

## HTML-CSS-DOM

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

## Quiz: Boxes Everywhere

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

## Boxes, Grids and Rules

The reason every element has a box layout is for simplicity. Think about boxes in a warehouse - the reason everything is stored in boxes is because they can stacked easily, and their location can be referred to easily. If all the warehouse storage units are of different shapes, they would be really difficult to arrange and categorize. Same thing here for web page layout.

## Quiz: Boxifying Design

Boxify a design:

- [x] drew boxes with a graphic program
- [x] doodled on a piece of paper
- [x] printed the page and drew on it
- [x] printed the page and cut with scissors

## Interview with Jacques

Jacques talked about how to boxify a design - from outer big boxes to inner small boxes.

## Boxes To HTML

Draw a pure box with `<div>`

```html
<div>title box</div>
<div>
    <div>image</div>
    <div>text</div>
</div>
```

A way to differentiate these boxes is to use the `class` attribute. (We want to be able to differentiate the boxes because, for example, we want to apply different style to each box.) If an element is imagined to be a real paperboard box, `class` is like the label on that box. One box can have any number of lables. 

```html
<div class="title">title box</div>
<div class="app">
    <div class="screenshot">image</div>
    <div class="description">text</div>
</div>
```

## Quiz: Creating the Files

### Create Folder and File Structure

- Create a folder for all your future web projects somewhere convenient, for example on your Desktop or in your Documents folder and call the folder “portfolio”.
- Create another folder inside it for this first page, call it “toplist”.
- Create 2 files there - index.html and style.css.

The structure should look like this:
```
.
└───portfolio
    └───toplist
        ├───index.html
        └───style.css
```

To keep things organized we highly recommend using the file structure described above. Since many of the HTML and CSS files you'll be creating in these lessons have similar names (like `index.html`), it is recommended that you create a separate folder/directory within `portfolio` for each mockup (the suggested name for this one is `toplist`) and save the related HTML and CSS files within it.

### Edit the HTML Document

Open the `index.html` file in your code editor, and write or copy/paste the following code and save the file:

```html
<div class="title">My App</div>
<div class="app">
    <div class="screenshot">image</div>
    <div class="description">text</div>
</div>
```

Note: For this quiz, you are not expected to add the image or the description text.

### Test the HTML File in a Browser

- Go to the folder, right click the file and choose “Open.. with Google Chrome”.
- Alternatively, in Chrome click "File -> Open File" and then browse to the `index.html` file and click "Open".
