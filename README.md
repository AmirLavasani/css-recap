# css-recap

A cheat-sheet for CSS with tips and tricks gathered from different sources. 

I was going through some of my old drives and stumbled upon this complete notes for when I was learning CSS.

## Table of Contents

1. [CSS Selectors](#css-selectors)
    - [Simple Selectors](#1-simple-selectors)
    - [Combinator Selectors](#2-combinator-selectors)
    - [Pseudo-class Selectors](#3-pseudo-class-selectors)
    - [Pseudo-element Selectors](#4-pseudo-element-selectors)
    - [Attribute Selectors](#5-attribute-selectors)
2. [Cascading Order](#cascading-order)
3. [Colors](#colors)
4. [Background Properties](#background)
5. [Borders](#border)
6. [Margins](#margins)
7. [Paddings](#paddings)
8. [Height and Width](#height-and-width)
9. [Box Model](#box-model)
10. [Outline](#outline)
11. [Text](#text)
12. [Fonts](#fonts)
13. [Icons](#icons)
14. [Links](#links)
15. [Tables](#tables)
16. [`display` Property](#display-property)
17. [`position` Property](#position-property)
18. [Overflow](#overflow)
19. [`float` and `clear` Property](#float-and-clear-property)
20. [Horizontal and Vertical Align](#horizontal-and-vertical-align)
21. [Combinators](#combinators)
22. [Pseudo-classes](#pseudo-classes)
23. [Pseudo-elements](#pseudo-elements)
24. [Transparency](#transparency)
25. [Navigation Bar](#navigation-bar)
26. [Attribute Selectors](#attribute-selectors)
27. [Counters](#counters)

## CSS Selectors

CSS selectors are an essential part of styling web pages. They allow us to target specific elements for styling based on various criteria. CSS selectors can be classified into five main categories:

### 1. Simple Selectors

Simple selectors enable us to target elements based on their attributes such as name, ID, or class.

- **Element Name Selector**: Targets elements by their HTML tag name.
- **ID Selector**: Targets an element by its unique ID attribute.
- **Class Selector**: Targets elements with a specific class attribute.

### 2. Combinator Selectors

Combinator selectors allow us to target elements based on their relationship with other elements.

- **Descendant Selector**: Targets elements that are descendants of a specific element.
- **Child Selector**: Targets elements that are direct children of a specific parent element.
- **Adjacent Sibling Selector**: Targets an element that directly follows another element.
- **General Sibling Selector**: Targets elements that share the same parent and are on the same level in the hierarchy.

### 3. Pseudo-class Selectors

Pseudo-class selectors target elements based on specific states or interactions. They are often used to apply styles in response to user actions.

- **:hover**: Targets an element when the mouse pointer is over it.
- **:active**: Targets an element when it's being clicked.
- **:focus**: Targets an element when it gains focus (e.g., through keyboard navigation).

### 4. Pseudo-element Selectors

Pseudo-element selectors allow us to style specific parts of an element's content. This provides finer control over styling. Some examples of pseudo-elements are:
- **::before**: Inserts content before the element's content.
- **::after**: Inserts content after the element's content.
- **::first-line**: Styles the first line of text within an element.
- **::first-letter**: Styles the first letter of text within an element.

### 5. Attribute Selectors

Attribute selectors enable us to target elements based on their attribute values. This is particularly useful for targeting elements with specific attributes. Examples include:
- **[attribute]**: Targets elements with a specific attribute.
- **[attribute=value]**: Targets elements with a specific attribute and value.

## Cascading Order

When multiple styles are defined for the same element, the cascading order determines which style takes precedence. The following order is followed:
1. **Inline Style**: Styles applied directly within the HTML element using the `style` attribute.
2. **External and Internal Style Sheets**: Styles defined in external CSS files or within the `<style>` tags in the `<head>` section of the HTML document.
3. **Browser Default Styles**: The default styles applied by the browser to elements when no specific styles are provided.

## Colors

When working with shades of gray, it's common to define them using equal values for all three light sources.

- **RGB Format**:
    - `rgb(60, 60, 60)`
    - `rgb(180, 180, 180)`

- **Hexadecimal Format**:
    - `#787878`
    - `#b4b4b4`
    - `#f0f0f0`

## Background Properties

In CSS, you can control the background of elements using various properties. Some of the essential CSS background properties include:

- **Background Color (`background-color`)**: This property sets the background color of an element. You can specify colors using color names, RGB values, or hexadecimal codes.

- **Background Image (`background-image`)**: This property allows you to set an image as the background of an element. You can use URLs to reference the image file.

- **Background Repeat (`background-repeat`)**: With this property, you can control how the background image is repeated both horizontally and vertically. Options include `repeat`, `repeat-x`, `repeat-y`, and `no-repeat`.

- **Background Attachment (`background-attachment`)**: This property determines whether the background image scrolls with the content or remains fixed within the viewport as the content scrolls. Options are `scroll` and `fixed`.

- **Background Position (`background-position`)**: Use this property to set the initial position of the background image. You can specify positions using keywords like `top`, `center`, and `bottom`, as well as using specific coordinates.

These background properties provide you with powerful tools to customize the visual appearance of elements on your web page.


## Border

**CSS Border Properties**

The CSS border properties allow you to specify the style, width, and color of an element's border.

- If the `border-style` property has four values:
  ```css
    border-style: dotted solid double dashed;
    /*
    top border is dotted

    right border is solid

    bottom border is double

    left border is dashed
    */
  ```

- If the border-style property has three values:
  ```css
    border-style: dotted solid double;
    /*
    top border is dotted

    right border is solid

    bottom border is double
    */
  ```

- If the border-style property has two values:
  ```css
    border-style: dotted solid;
    /*
    top and bottom borders are dotted

    right and left borders are solid
    */
  ```

- If the border-style property has one value:

  ```css
    border-style: dotted;
    /*
    all four borders are dotted
    */
  ```

## Margins

The CSS margin properties are used to create space around elements, outside of any defined borders.

> Note: Negative values are allowed.

All the margin properties can have the following values:
- `auto` - the browser calculates the margin
- `length` - specifies a margin in px, pt, cm, etc.
- `%` - specifies a margin in % of the width of the containing element
- `inherit` - specifies that the margin should be inherited from the parent element

**The `auto` Value**

You can set the margin property to `auto` to horizontally center the element within its container.

**Margin Collapse**

Top and bottom margins of elements are sometimes collapsed into a single margin that is equal to the largest of the two margins.
This does not happen on left and right margins! Only top and bottom margins!

## Paddings

The CSS padding properties are used to generate space around an element's content, inside of any defined borders.

> Note: Negative values are not allowed.

All the padding properties can have the following values:
- `length` - specifies a padding in px, pt, cm, etc.
- `%` - specifies a padding in % of the width of the containing element
- `inherit` - specifies that the padding should be inherited from the parent element

**Padding and Element Width**

The CSS `width` property specifies the width of the element's content area. The content area is the portion inside the padding, border, and margin of an element (the box model).

To keep the width at 300px, no matter the amount of padding, you can use the `box-sizing` property. This causes the element to maintain its width; if you increase the padding, the available content space will decrease.
```css
{ box-sizing: border-box; }
```

## Height and Width

The `height` and `width` properties are used to set the height and width of an element.

The `height` and `width` properties **do not** include padding, borders, or margins. They set the height/width of the area inside the padding, border, and margin of the element.

The `height` and `width` properties may have the following values:
- `auto` - This is default. The browser calculates the height and width
- `length` - Defines the height/width in px, cm etc.
- `%` - Defines the height/width in percent of the containing block
- `initial` - Sets the height/width to its default value
- `inherit` - The height/width will be inherited from its parent value

**Setting Max-Width**

The `max-width` property is used to set the maximum width of an element.

The `max-width` can be specified in length values, like px, cm, etc., or in percent (%) of the containing block, or set to `none` (this is default, meaning that there is no maximum width).

> Note: The value of the `max-width` property overrides `width`.

## Box Model

Explanation of the different parts:
- **Content** - The content of the box, where text and images appear
- **Padding** - Clears an area around the content. The padding is transparent
- **Border** - A border that goes around the padding and content
- **Margin** - Clears an area outside the border. The margin is transparent

## Outline

An outline is a line that is drawn around elements, OUTSIDE the borders, to make the element "stand out".

```css
.dotted {
  outline-style: dotted;
}

/* Available values:
  dotted
  dashed
  solid
  double
  groove
  ridge
  inset
  outset
*/

```

## Text

**Text Alignment**

The `text-align` property is used to set the horizontal alignment of text. Text can be left or right aligned, centered, or justified.

**Text Transformation**

The `text-transform` property is used to specify uppercase and lowercase letters in text.

```css
{
  text-transform: uppercase;
  /* Available values:
    uppercase
    lowercase
    capitalize
  */ 
}
```

**Text Indentation**

The `text-indent` property is used to specify the indentation of the first line of a text.

**Letter Spacing**

The `letter-spacing` property is used to specify the space between the characters in a text.

**Line Height**

The `line-height` property is used to specify the space between lines.

**Text Direction**

The `direction` property is used to change the text direction of an element.

**Word Spacing**

The `word-spacing` property is used to specify the space between the words in a text.

**Text Shadow**

The `text-shadow` property adds shadow to text.


## Fonts

The CSS font properties define the font family, boldness, size, and the style of a text.

In CSS, there are two types of font family names:

- **Generic family** - a group of font families with a similar look (like "Serif" or "Monospace")
- **Font family** - a specific font family (like "Times New Roman" or "Arial")

**Serif** - Serif fonts have small lines at the ends on some characters

**Sans-serif** - "Sans" means without - these fonts do not have the lines at the ends of characters

**Monospace** - All monospace characters have the same width

> Note: On computer screens, sans-serif fonts are considered easier to read than serif fonts.

**Font Family**

The font family of text is set with the `font-family` property.
The `font-family` property should hold several font names as a "fallback" system. Start with the font you want, and end with a generic family.

**Font Size**

The `font-size` property sets the size of the text.

**Set Font Size With Em**

To allow users to resize the text (in the browser menu), many developers use `em` instead of pixels.
The `em` size unit is recommended by the W3C. Default: 1em = 16px.

**Use a Combination of Percent and Em**

The solution that works in all browsers is to set a default font-size in percent for the `<body>` element:

```css
body {
  font-size: 100%;
}
h1 {
  font-size: 2.5em;
}
```

**Font Weight**

The `font-weight` property specifies the weight and boldness of a font.

**Responsive Font Size**

The text size can be set with a `vw` unit, which means the "viewport width".

Viewport is the browser window size. `1vw = 1%` of viewport width.

**Font Variant**

The `font-variant` property specifies whether or not text should be displayed in a small-caps font.
In a small-caps font, all lowercase letters are converted to uppercase letters. However, the converted uppercase letters appear in a smaller font size than the original uppercase letters in the text.

## Icons


Add the name of the specified icon class to any inline HTML element (like `<i>` or `<span>`).

Three Icon Library:

  - **Font Awesome Icons**
  - **Bootstrap Icons**
  - **Google Icons**


```html

<head>
  <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
</head>

<body>

<i class="fas fa-cloud"></i>

</body>

```



## Links

The four links states are:
- `a:link` - a normal, unvisited link
- `a:visited` - a link the user has visited
- `a:hover` - a link when the user mouses over it
- `a:active` - a link the moment it is clicked

> `a:hover` MUST come after `a:link` and `a:visited`

> `a:active` MUST come after `a:hover`

## Tables

**Collapse Table Borders**

The `border-collapse` property sets whether the table borders should be collapsed into a single border.

**Striped Tables**

For zebra-striped tables, use the `nth-child()` selector and add a `background-color` to all even (or odd) table rows.

**Responsive Table**

Add a container element (like `<div>`) with `overflow-x:auto` around the `<table>` element to make it responsive.

## `display` Property

The `display` property specifies if/how an element is displayed.

**Block-level Elements**

A block-level element always starts on a new line and takes up the full width available.

**Inline Elements**

An inline element does not start on a new line and only takes up as much width as necessary.

**`display: none;`**

`display: none;` is commonly used with JavaScript to hide and show elements without deleting and recreating them.
The `<script>` element uses `display: none;` as default.

**Hide an Element - `display:none` or `visibility:hidden`?**

`display: none;` - The element will be hidden, and the page will be displayed as if the element is not there.

`visibility: hidden;` - However, the element will still take up the same space as before. The element will be hidden but still affect the layout.

### The `display: inline-block` Value

**Compared to `display: inline`:**

The major difference is that `display: inline-block` allows you to set a width and height on the element.
Also, with `display: inline-block`, the top and bottom margins/paddings are respected, but with `display: inline`, they are not.

**Compared to `display: block`:**

The major difference is that `display: inline-block` does not add a line-break after the element, so the element can sit next to other elements.

**Using `inline-block` to Create Navigation Links:**

One common use for `display: inline-block` is to display list items horizontally instead of vertically.

## The `position` Property

The `position` property specifies the type of positioning method used for an element.

There are five different position values:
- `static`
- `relative`
- `fixed`
- `absolute`
- `sticky`

**`position: static;`**

- HTML elements are positioned static by default.

- Static positioned elements are not affected by the `top`, `bottom`, `left`, and `right` properties.
- An element with `position: static;` is not positioned in any special way; it is always positioned according to the normal flow of the page.

**`position: relative;`**

- An element with `position: relative;` is positioned relative to its normal position.
- Setting the `top`, `right`, `bottom`, and `left` properties of a relatively-positioned element will cause it to be adjusted away from its normal position.

**`position: fixed;`**

- An element with `position: fixed;` is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled. 
- The `top`, `right`, `bottom`, and `left` properties are used to position the element.

**`position: absolute;`**

- An element with `position: absolute;` is positioned relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like fixed).

**`position: sticky;`**

- An element with `position: sticky;` is positioned based on the user's scroll position.
- A sticky element toggles between relative and fixed, depending on the scroll position. It is positioned relative until a given offset position is met in the viewport - then it "sticks" in place (like `position: fixed`).

```css
div.sticky {
  position: -webkit-sticky; /* Safari */
  position: sticky;
  top: 0;
  background-color: green;
  border: 2px solid #4CAF50;
}
```

**Overlapping Elements**

The `z-index` property specifies the stack order of an element (which element should be placed in front of, or behind, the others).


## Overflow

The CSS `overflow` property controls what happens to content that is too big to fit into an area.

The `overflow` property has the following values:
- `visible` - Default. The overflow is not clipped. The content renders outside the element's box.
- `hidden` - The overflow is clipped, and the rest of the content will be invisible.
- `scroll` - The overflow is clipped, and a scrollbar is added to see the rest of the content.
- `auto` - Similar to scroll, but it adds scrollbars only when necessary.

>Note: The overflow property only works for block elements with a specified height.

**`overflow-x` and `overflow-y`**

- `overflow-x` specifies what to do with the left/right edges of the content.
- `overflow-y` specifies what to do with the top/bottom edges of the content.

## `float` and `clear` Property

The CSS `float` property specifies how an element should float.
The `float` property can have one of the following values:
- `left` - The element floats to the left of its container
- `right` - The element floats to the right of its container
- `none` - The element does not float (will be displayed just where it occurs in the text). This is default
- `inherit` - The element inherits the float value of its parent

The CSS `clear` property specifies what elements can float beside the cleared element and on which side.
The `clear` property can have one of the following values:
- `none` - Allows floating elements on both sides. This is default
- `left` - No floating elements allowed on the left side
- `right` - No floating elements allowed on the right side
- `both` - No floating elements allowed on either the left or the right side
- `inherit` - The element inherits the clear value of its parent

### The clearfix Hack

If an element is taller than the element containing it, and it is floated, it will "overflow" outside of its container. To fix this problem, you can add `overflow: auto;` to the containing element.

```css
.clearfix {
  overflow: auto;
}
```

The new, modern clearfix hack however, is safer to use, and the following code is used for most webpages:

```css
.clearfix::after {
  content: "";
  clear: both;
  display: table;
}
```

**Equal Height Boxes**

This is where **CSS3 Flexbox** comes in handy - as it can automatically stretch boxes to be as long as the longest box

```css
.flex-container {
  display: flex;
  flex-wrap: nowrap;
}
```

## Horizontal and Vertical Align

### Center Align Elements

To horizontally center a block element (like `<div>`), use `margin: auto;`.

**Center Align Text**

To just center the text inside an element, use `text-align: center;`.

**Center an Image**

To center an image, set left and right margin to auto and make it into a block element.

```css
img {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 40%;
}
```

### Left and Right Align

**Using `position`**

One method for aligning elements is to use `position: absolute;`.

```css
.right {
  position: absolute;
  right: 0px;
  width: 300px;
  border: 3px solid #73AD21;
}
```

>Note: Absolute positioned elements are removed from the normal flow and can overlap elements.

**Using `float`**

Another method for aligning elements is to use the `float` property.

```css
.right {
  float: right;
  width: 300px;
  border: 3px solid #73AD21;
  padding: 10px;
}
```

> Note: If an element is taller than the element containing it and it is floated, it will overflow outside of its container. You can use the **clearfix hack** to fix this.

```css
.clearfix {
  overflow: auto;
}
```

### Center Vertically

**Using `padding`**

There are many ways to center an element vertically in CSS. A simple solution is to use top and bottom padding.

```css
.center {
  padding: 70px 0;
}
```

To center both vertically and horizontally, use padding and `text-align: center`.

```css
.center {
  padding: 70px 0;
  text-align: center;
}
```

**Using `line-height`**

Another trick is to use the `line-height` property with a value that is equal to the height property.

```css
.center {
  line-height: 200px;
  height: 200px;
  text-align: center;
}

/* If the text has multiple lines, add the following: */
.center p {
  line-height: 1.5;
  display: inline-block;
  vertical-align: middle;
}
```

**Using `position` & `transform`**

If `padding` and `line-height` are not options, a third solution is to use positioning and the transform property.

```css
.center { 
  height: 200px;
  position: relative;
}

.center p {
  margin: 0;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```

## Combinators

A combinator is something that explains the relationship between the selectors. There are four different combinators in CSS:

- **Descendant Selector (space)**: The descendant selector matches all elements that are descendants of a specified element.

```css
/* Selects all <p> elements that are descendants of <div> elements */
div p {
    color: blue;
}
```

- **Child Selector (>)**: The child selector selects all elements that are the direct children of a specified element.

```css
/* Selects all <li> elements that are direct children of <ul> elements */
ul > li {
    list-style-type: square;
}
```

- **Adjacent Sibling Selector (+)**: The adjacent sibling selector selects all elements that are the adjacent siblings of a specified element. Sibling elements must have the same parent element, and "adjacent" means "immediately following."

```css
/* Selects the <h2> element that is an immediate sibling of a <p> element */
p + h2 {
    font-weight: bold;
}
```

- **General Sibling Selector (~)**: The general sibling selector selects all elements that are siblings of a specified element.

```css
/* Selects all <p> elements that are siblings of a <h2> element within the same parent */
h2 ~ p {
    font-style: italic;
}
```

## Pseudo-classes

A pseudo-class is used to define a special state of an element.

```css
selector:pseudo-class {
  property: value;
}
```

**`:first-child` Pseudo-class**

The `:first-child` pseudo-class matches a specified element that is the first child of another element.

```css
/* Selects the first <li> element within an <ul> */
ul li:first-child {
    font-weight
    : bold;
}
```
In this example, the first `<li>` element within a `<ul>` will have its text displayed in bold.



**`:lang` Pseudo-class**

The `:lang` pseudo-class allows you to define special rules for different languages.

```css
/* Selects paragraphs in English language */
p:lang(en) {
    color: blue;
}

/* Selects paragraphs in French language */
p:lang(fr) {
    color: red;
}
```

In this example, paragraphs with the **English (en)** language attribute will have blue text, while paragraphs with the **French (fr)** language attribute will have red text.

### Common CSS Pseudo-classes

1. `:hover`: Selects an element when the mouse pointer is over it.
2. `:active`: Selects an element when it is being clicked or activated.
3. `:focus`: Selects an element when it has keyboard input focus.
4. `:first-child`: Selects the first child of a parent element.
5. `:last-child`: Selects the last child of a parent element.
6. `:nth-child()`: Selects elements based on their position within a parent element using a formula.
7. `:not()`: Selects elements that do not match a given selector.
8. `:checked`: Selects input elements (e.g., checkboxes and radio buttons) that are checked.
9. `:disabled`: Selects form elements that are disabled.
10. `:enabled`: Selects form elements that are enabled.
11. `:required`: Selects form elements that are required to be filled out.
12. `:empty`: Selects elements that have no children.
13. `:target`: Selects the target element of an anchor link (e.g., `#example` in `<a href="#example">`).
14. `:nth-of-type()`: Selects elements based on their position among elements of the same type within a parent element.
15. `:first-of-type`: Selects the first occurrence of an element type within a parent element.
16. `:last-of-type`: Selects the last occurrence of an element type within a parent element.
17. `:only-child`: Selects elements that are the only child of their parent element.
18. `:only-of-type`: Selects elements that are the only occurrence of their type within a parent element.
19. `:placeholder`: Selects input elements with placeholder text.
20. `:valid`: Selects form elements that are considered valid based on their input.
21. `:invalid`: Selects form elements that are considered invalid based on their input.
22. `:required`: Selects form elements that are required to be filled out.
23. `:optional`: Selects form elements that are optional and not required.

## Pseudo-elements

A CSS pseudo-element is used to style specified parts of an element.

```css
selector::pseudo-element {
  property: value;
}
```

**`::first-line` Pseudo-element**

The `::first-line` pseudo-element is used to add a special style to the first line of a text.

**`::before` Pseudo-element**

The `::before` pseudo-element can be used to insert some content before the content of an element.

**`::after` Pseudo-element**

The `::after` pseudo-element can be used to insert some content after the content of an element.

**`::selection` Pseudo-element**

The `::selection` pseudo-element matches the portion of an element that is selected by a user.

## Transparency

The `opacity` property can take a value from 0.0 to 1.0. The lower value, the more transparent

```css
img {
  opacity: 0.5;
  filter: alpha(opacity=50); /* For IE8 and earlier */
}
```

**Transparent Hover Effect**

The `opacity` property is often used together with the `:hover` selector to change the opacity on *mouse-over*

**Transparency using RGBA**

If you do not want to apply opacity to child elements, use RGBA color values.


## Navigation Bar

A Navigation Bar is essentially a list of links.

- **display: block**: Displaying the links as block elements makes the whole link area clickable (not just the text), and it allows us to specify the width (and padding, margin, height, etc. if you want).

- **Active/Current Navigation Link**: Add an `active` class to the current link to let the user know which page he/she is on.

### Horizontal Navigation Bar

- **Inline List Items**: One way to build a horizontal navigation bar is to specify the `<li>` elements as inline.

- **Floating List Items**: Another way of creating a horizontal navigation bar is to float the `<li>` elements and specify a layout for the navigation links.

- **Border Dividers**: Add the `border-right` property to `<li>` to create link dividers.

### Fixed Navigation Bar

> Note: Fixed position might not work properly on mobile devices.

- **Fixed Top**
  ```css
  ul {
    position: fixed;
    top: 0;
    width: 100%;
  }
  ```

- **Fixed Bottom**
  ```css
  ul {
    position: fixed;
    bottom: 0;
    width: 100%;
  }
  ```

## Attribute Selectors

Attribute selectors in CSS allow you to style HTML elements based on specific attributes or attribute values.

### [attribute] Selector

The `[attribute]` selector is used to select elements with a specified attribute.

### [attribute="value"] Selector

The `[attribute="value"]` selector is used to select elements with a specified attribute and value.

### [attribute~="value"] Selector

The `[attribute~="value"]` selector is used to select elements with an attribute value containing a specified word.

### [attribute|="value"] Selector

The `[attribute|="value"]` selector is used to select elements with the specified attribute starting with the specified value.

### [attribute^="value"] Selector

The `[attribute^="value"]` selector is used to select elements whose attribute value begins with a specified value.

### [attribute$="value"] Selector

The `[attribute$="value"]` selector is used to select elements whose attribute value ends with a specified value.

### [attribute*="value"] Selector

The `[attribute*="value"]` selector is used to select elements whose attribute value contains a specified value.

### Styling Forms

Attribute selectors can be useful for styling forms without class or ID:

```css
input[type="text"] {
  width: 150px;
  display: block;
  margin-bottom: 10px;
  background-color: yellow;
}

input[type="button"] {
  width: 120px;
  margin-left: 35px;
  display: block;
}
```

These selectors provide a powerful way to target specific elements in your HTML based on their attributes, allowing for fine-grained styling control.


## Counters

CSS counters function like "variables" that can be incremented by CSS rules, tracking how many times they are used. To work with CSS counters, you can utilize the following properties:

- **counter-reset**: This property creates or resets a counter.

- **counter-increment**: It increments a counter value.

- **content**: The `content` property is used to insert generated content.

- **counter() or counters() function**: These functions are used to add the value of a counter to an element.
