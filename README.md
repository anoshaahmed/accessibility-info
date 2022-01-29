# Accessibility Info
_List of simple accessibility practices to know and other common mistakes to avoid while writing your code._
<hr>

__HTML Language__

```html
<html lang="en">
```
##
__Title__

```html
<head>
<title>Some title</title>
</head>
```
##
__Semantic tags__

The direct children of the body must be wrapped in semantic tags to indicate the users what purpose that part of the webpage is for.

For example,
```html
<body>
  <header>
    ...header of the webpage...
  </header>
  <main>
    ...main content of the webpage...
  </main>
  <footer>
    ...footer of the webpage...
  </footer>
</body>
```
_Read more [here](https://www.w3.org/TR/wai-aria-practices/examples/landmarks/main.html)_
##
__Heading__

- First level headings indicate what the webpage is about and it is a must that every page has one.
- Headings must start with `<h1>`, and move up by one level each time. This makes it easier for a screen reader to navigate a page.
##
__Image__

Image tags (`<img>`) must contain alternative text (`alt=" "`) for a screen reader to read out loud to the user.

For example,
```html
<img src="images/flower.jpg" alt="Pink flower">
```
##
__UL and OL__

`<ul>` or `<ol>` must contain `<li>`. If images need to be put in a list, the images must go inside of `<li>` tags.

##
__ID vs. Class__

IDs must only be used *once*. Use classes instead of IDs if they're required for styling on more than one element.

##
__Link__

`<a>` should have an `aria-label` _Read more [here](https://dequeuniversity.com/rules/axe/3.5/link-name)_

For example,
```html
<ul class="social-media">
  <li>
    <a aria-label="Facebook">
      <img src="images/icon-facebook.svg" alt="facebook">
    </a>
  </li>
  
  <li>
    <a aria-label="Twitter"><img src="images/icon-twitter.svg" alt="twitter">
    </a>
  </li>
  
  <li>
    <a aria-label="Instagram"><img src="images/icon-instagram.svg" alt="instagram">
    </a>
  </li>
</ul>
```
##
__Button__

Like `<a>` tags, `<button>`s must also contain an `aria-label=" "`

##
__Link vs. Button__

In simple words, use `<a>` if it needs to take the use to a different page, whereas use a button if it needs to fulfill a small purpose on the same page, for example, a button to make text green.
_Read more [here](https://ux.iu.edu/writings/buttons-vs-links-basic/#:~:text=There%20are%20differences%20as%20to,affect%20the%20website%20at%20all.)

Don't use a `<button>` with an `<a>` inside of it. Instead, use `<a>` and style it like a button.

##
__Form__

An `<input>` must have a corresponding `<label>`

##
__Section__
A `<section>` needs a heading; if you don't need a heading in it, use some other element such as `<div>`

##
__Article__

An `<article>` usually needs a heading; if you don't need a heading in it, use some other element such as `<div>`

<hr>

I hope this helps you :)
