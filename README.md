# intro-to-html-and-css

Learning notes and hand-ons for Udacity course Intro to HTML and CSS

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
