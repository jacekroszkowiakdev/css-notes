## CSS Basics

### 1. Selectors:

CSS selectors are patterns used to select the elements you want to style in a web page. They allow you to target HTML elements and apply styles to them. Here are the main types of CSS selectors:

#### Type Selector

Selects all elements of a given type.

```css
p {
    color: blue;
}
```

This will apply the style to all `<p>` elements.

#### Class Selector

Selects all elements with a specific class attribute. Prefixed with a dot `.`.

```css
.className {
    color: red;
}
```

This will apply the style to all elements with class="classname".

#### ID Selector

Selects a single element with a specific id attribute. Prefixed with a hash `#`.

```css
#idName {
    color: green;
}
```

This will apply the style to the element with id="idname".

#### Universal Selector

Selects all elements on the page. Denoted by an asterisk `*`.

```css
* {
    color: black;
}
```

This will apply the style to all elements.

#### Attribute Selector

Selects elements based on the presence or value of a given attribute. The list of attributes can be found [here](https://www.w3schools.com/cssref/index.php).

```css
[type="text"] {
    border: 1px solid black;
}
```

This will apply the style to all elements with type="text".

#### Pseudo-class Selector

Selects elements based on their state or position. The list of pseudo-classes can be found [here](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes).

```css
a:hover {
    color: orange;
}
```

This will apply the style to links when they are hovered over.

#### Pseudo-element Selector

Selects and styles a part of an element. For example, it can be used to:

    Style the first letter, or line, of an element
    Insert content before, or after, the content of an element

    Note: The ::first-line pseudo-element can only be applied to block-level elements.

The following properties apply to the ::first-line pseudo-element:

    font properties
    color properties
    background properties
    word-spacing
    letter-spacing
    text-decoration
    vertical-align
    text-transform
    line-height
    clear

```css
p::first-line {
    font-weight: bold;
}
```

This will apply the style to the first line of all `<p>` elements.

#### Descendant Selector

Selects elements that are descendants of a specified element.

```css
div p {
    color: purple;
}
```

This will apply the style to all `<p>` elements inside `<div>` elements.

#### Child Selector

Selects elements that are direct children of a specified element.

```css
ul > li {
    color: blue;
}
```

This will apply the style to all `<li>` elements that are direct children of `<ul>` elements.

#### Adjacent Sibling Selector

Selects an element that is immediately preceded by a specified element.

```css
h1 + p {
    color: brown;
}
```

This will apply the style to the <p> element that immediately follows an `<h1>` element.

#### General Sibling Selector

Selects all elements that are siblings of a specified element.

```css
h1 ~ p {
    color: pink;
}
```

This will apply the style to all `<p>` elements that are siblings of an `<h1>` element.

CSS selectors are powerful tools that enable you to target specific HTML elements precisely and apply styles accordingly.

#### Selector list

A selector list is a comma-separated list of simple, compound, and/or complex selectors. A given element is said to match a selector list when the element matches any (at least one) of the selectors in that selector list.

```css
#main,
article.heading {
}
```

### 2. Specificity
