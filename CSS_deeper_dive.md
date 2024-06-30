## CSS Box Model

The CSS Box Model is a fundamental concept in web design and layout, describing how elements are rendered on the page. It consists of four main parts:

-   Content: The innermost part of the box where the text and images are displayed.
-   Padding: The space between the content and the border. It clears an area around the content inside the element, making the content appear with some spacing from the border.
-   Border: A line surrounding the padding (if any) and content. The border can be styled with different widths, colors, and styles (solid, dashed, dotted, etc.).
-   Margin: The outermost layer, which clears an area outside the border. It creates space between the element and its neighboring elements.

Visual Representation

```css
+---------------------------+
|        Margin             |
|  +---------------------+  |
|  |      Border         |  |
|  |  +---------------+  |  |
|  |  |   Padding     |  |  |
|  |  |  +---------+  |  |  |
|  |  |  | Content |  |  |  |
|  |  |  +---------+  |  |  |
|  |  +---------------+  |  |
|  +---------------------+  |
+---------------------------+
```

**Example**:

```css
div {
    width: 200px;
    height: 100px;
    padding: 10px;
    border: 5px solid black;
    margin: 20px;
    box-sizing: border-box; /* Optional: includes padding and border in the width and height */
}
```

### CSS Margin Collapsing

Margin collapsing is a behavior in CSS where vertical margins between adjacent block-level elements are combined (collapsed) into a single margin that is **equal to the largest of the adjoining margins**. This can happen in several scenarios:

-   Adjacent Sibling Elements: When two block-level elements are next to each other, their vertical margins collapse.

-   Parent and First/Last Child: If a parent and its first or last child element have vertical margins, those margins will collapse.

-   Empty Elements: If an element has no border, padding, or content, its top and bottom margins collapse.

### CSS Shorthand Properties

CSS shorthands are a convenient way to set multiple CSS properties in a single declaration, simplifying your code and making it more readable. Here are some commonly used CSS shorthand properties:

1. Margin and Padding

Margin:

```css

/_ Separate properties _/
margin-top: 10px;
margin-right: 20px;
margin-bottom: 30px;
margin-left: 40px;

/_ Shorthand _/
margin: 10px 20px 30px 40px; /_ top right bottom left _/
```

Padding:

```css

/_ Separate properties _/
padding-top: 5px;
padding-right: 10px;
padding-bottom: 15px;
padding-left: 20px;

/_ Shorthand _/
padding: 5px 10px 15px 20px; /_ top right bottom left _/
```

2. Border

```css

/_ Separate properties _/
border-width: 1px;
border-style: solid;
border-color: #000;

/_ Shorthand _/
border: 1px solid #000;
```

3. Font

```css

/_ Separate properties _/
font-style: italic;
font-variant: small-caps;
font-weight: bold;
font-size: 16px;
line-height: 1.5;
font-family: Arial, sans-serif;

/_ Shorthand _/
font: italic small-caps bold 16px/1.5 Arial, sans-serif;
```

4. Background

```css

/_ Separate properties _/
background-color: #ff0;
background-image: url('image.jpg');
background-repeat: no-repeat;
background-position: center;
background-size: cover;

/_ Shorthand _/
background: #ff0 url('image.jpg') no-repeat center/cover;
```

5. List Style

```css

/_ Separate properties _/
list-style-type: disc;
list-style-position: inside;
list-style-image: url('image.png');

/_ Shorthand _/
list-style: disc inside url('image.png');
```

6. Animation

```css

/_ Separate properties _/
animation-name: slidein;
animation-duration: 3s;
animation-timing-function: ease-in-out;
animation-delay: 1s;
animation-iteration-count: infinite;
animation-direction: alternate;

/_ Shorthand _/
animation: slidein 3s ease-in-out 1s infinite alternate;
```

7. Transition

```css

/_ Separate properties _/
transition-property: opacity;
transition-duration: 2s;
transition-timing-function: linear;
transition-delay: 0.5s;

/_ Shorthand _/
transition: opacity 2s linear 0.5s;
```

8. Flex

```css

/_ Separate properties _/
flex-grow: 1;
flex-shrink: 1;
flex-basis: 0;

/_ Shorthand _/
flex: 1 1 0;
```

9. Grid

```css

/_ Separate properties _/
grid-template-columns: 100px 1fr;
grid-template-rows: auto;
grid-template-areas: "header header"
"sidebar main";
grid-gap: 10px;

/_ Shorthand _/
grid:
"header header"
"sidebar main"
/ 100px 1fr;
gap: 10px;
```

### CSS Height and Width

The **height** and **width** properties are used to set the height and width of an element.

The height and width properties do not include padding, borders, or margins. It sets the height/width of the area inside the padding, border, and margin of the element.

```css
div {
    width: 200px;
    height: 100px;
    padding: 10px;
    border: 5px solid #000;
    margin: 20px;
}
```

In this example:

-   The content area is 200px wide and 100px high.
-   Padding adds 20px to both the width (10px on the left and right) and the height (10px on the top and bottom).
-   Borders add 10px to both the width (5px on the left and right) and the height (5px on the top and bottom).

So, the total width and height, including padding and borders, are:

-   Total width: 200px (content) + 20px (padding) + 10px (border) = 230px
-   Total height: 100px (content) + 20px (padding) + 10px (border) = 130px

Margins add space outside the element and do not affect the element's dimensions but influence the spacing between elements.

**Using box-sizing**

The **box-sizing** property allows you to change the default CSS box model used to calculate widths and heights of elements.

Values of box-sizing:

    **content-box** (default):
    -   Width and height only include the content. Padding and border are added outside these dimensions.

```css
div {
    box-sizing: content-box;
}
```

**border-box**:

-   Width and height include content, padding, and border. This makes it easier to control the size of elements, especially for layouts.

```css
div {
    box-sizing: border-box;
}
```

**Example**: Setting box-sizing: border-box

```css
/_ Apply border-box to all elements _/ _,
_::before,
\*::after {
    box-sizing: border-box;
}

div {
    width: 200px;
    height: 100px;
    padding: 10px;
    border: 5px solid #000;
    margin: 20px;
}
```

With box-sizing: border-box, the total width and height remain:

-   Total width: 200px
-   Total height: 100px

Padding and border are included within the specified width and height, so you do not need to manually subtract padding and border from the dimensions you want.
Practical Use of box-sizing

**Global Box-Sizing Reset**:

To make layouts easier to manage, many developers apply box-sizing: border-box globally using a universal selector or a more targeted approach. This helps avoid unexpected size calculations when adding padding or borders to elements.

```css
/* Universal box-sizing reset */
*,
*::before,
*::after {
    box-sizing: border-box;
}
```

Specific Element Box-Sizing:

In some cases, you might want to apply box-sizing to specific elements only.

```css
/* Specific element */
.container {
    box-sizing: border-box;
}
```

### The CSS display property

It specifies the type of rendering box used for an element and can influence how an element interacts with other elements on the page.

Common **display** Values

1. **block**:

-   The element is rendered as a block-level element.
-   Takes up the full width available, with line breaks before and after.
-   Examples: `<div>`,` <p>`,` <h1>`.

```css
.block {
    display: block;
}
```

2. **inline**:

-   The element is rendered as an inline element.
-   Takes up only as much width as necessary, no line breaks before or after.
-   Examples: <span>, <a>, <strong>.

```css
.inline {
    display: inline;
}
```

3. **inline-block**:

-   The element is rendered as an inline-level block container.
-   Flows with inline content but allows setting width and height.
-   Examples: Custom buttons, badges.

```css
.inline-block {
    display: inline-block;
}
```

4. **flex**::

-   The element becomes a flex container.
-   Enables flexbox layout model for flexible and responsive layouts.
-   Examples: Navigation bars, card layouts.

```css
.flex {
    display: flex;
}
```

5. **inline-flex**:

-   The element behaves like an inline-level flex container.
-   Combines features of flex and inline.

```css
.inline-flex {
    display: inline-flex;
}
```

6. **grid**:

-   The element becomes a grid container.
-   Enables grid layout model for complex, two-dimensional layouts.

```css
.grid {
    display: grid;
}
```

7. **inline-grid**:

-   The element behaves like an inline-level grid container.

```css
.inline-grid {
    display: inline-grid;
}
```

8. **none**:

-   The element is not displayed at all (no rendering box).
-   Does not take up any space in the layout.

```css
.none {
    display: none;
}
```

**Other Values and Concepts**

    **table**:

-   The element behaves like a <table>.

```css
.table {
    display: table;
}
```

**table-row, table-cell, etc**.:

-   Elements behave like rows and cells of a table.

```css
.table-row {
    display: table-row;
}
.table-cell {
    display: table-cell;
}
```

**contents**:

-   The element disappears, but its child elements remain and are rendered as if they were direct children of the parent element.

```css
.contents {
    display: contents;
}
```

**list-item**:

-   The element behaves like a list item.

```css
.list-item {
    display: list-item;
}
```
