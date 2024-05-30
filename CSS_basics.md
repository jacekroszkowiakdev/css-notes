## CSS Basics

1. Selectors:
   CSS selectors are patterns used to select the elements you want to style in a web page. They allow you to target HTML elements and apply styles to them. Here are the main types of CSS selectors:

## Type Selector

Selects all elements of a given type.

```css
p {
    color: blue;
}
```

This will apply the style to all `<p>` elements.

## Class Selector

Selects all elements with a specific class attribute. Prefixed with a dot `.`.

```css
.classname {
    color: red;
}
```

This will apply the style to all elements with class="classname".

## ID Selector

Selects a single element with a specific id attribute. Prefixed with a hash `#`.

```css
#idname {
    color: green;
}
```

This will apply the style to the element with id="idname".

## Universal Selector

Selects all elements on the page. Denoted by an asterisk `*`.

```css
* {
    color: black;
}
```

This will apply the style to all elements.

## Attribute Selector

Selects elements based on the presence or value of a given attribute.

```css
[type="text"] {
    border: 1px solid black;
}
```

This will apply the style to all elements with type="text".

## Pseudo-class Selector

Selects elements based on their state or position.

```css
a:hover {
    color: orange;
}
```

This will apply the style to links when they are hovered over.

## Pseudo-element Selector

Selects and styles a part of an element.

```css
p::first-line {
    font-weight: bold;
}
```

This will apply the style to the first line of all `<p>` elements.

## Descendant Selector

Selects elements that are descendants of a specified element.

```css
div p {
    color: purple;
}
```

This will apply the style to all `<p>` elements inside `<div>` elements.

## Child Selector

Selects elements that are direct children of a specified element.

```css
ul > li {
    color: blue;
}
```

This will apply the style to all `<li>` elements that are direct children of `<ul>` elements.

## Adjacent Sibling Selector

Selects an element that is immediately preceded by a specified element.

```css
h1 + p {
    color: brown;
}
```

This will apply the style to the <p> element that immediately follows an `<h1>` element.

## General Sibling Selector

Selects all elements that are siblings of a specified element.

```css
h1 ~ p {
    color: pink;
}
```

This will apply the style to all `<p>` elements that are siblings of an `<h1>` element.

CSS selectors are powerful tools that enable you to target specific HTML elements precisely and apply styles accordingly.
