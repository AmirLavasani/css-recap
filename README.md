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
28. [CSS Units](#css-units)
29. [Specificity](#specificity)
30. [Image Background](#image-background)
31. [Gradients](#gradients)
32. [Shadow Effects](#shadow-effects)
33. [Text Effects](#text-effects)
34. [Web Fonts](#web-fonts)
35. [2D Transforms](#2d-transforms)
36. [3D Transforms](#3d-transforms)
37. [Transitions](#transitions)
38. [Animations](#animations)
39. [Tooltip](#tooltip)
40. [Styling Images](#styling-images)
41. [`object-fit` Property](#object-fit-property)
42. [Button Styling](#button-styling)
43. [Multiple Columns](#multiple-columns)

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


## CSS Units

CSS offers various units for expressing lengths, which can be categorized into two types: absolute and relative.

### Absolute Lengths

Absolute length units are fixed, and a length expressed in any of these will appear as exactly that size:

- **cm**: Centimeters
- **mm**: Millimeters
- **in**: Inches (1in = 96px = 2.54cm)
- **px**: Pixels (1px = 1/96th of 1in) *
- **pt**: Points (1pt = 1/72 of 1in)
- **pc**: Picas (1pc = 12pt)

> Pixels (px) are relative to the viewing device. For low-dpi devices, 1px equals one device pixel (dot) of the display. For printers and high-resolution screens, 1px implies multiple device pixels.

### Relative Lengths

Relative length units specify a length relative to another length property, making them more adaptable across different rendering mediums:

- **em**: Relative to the font-size of the element (e.g., 2em means 2 times the size of the current font)
- **ex**: Relative to the x-height of the current font (rarely used)
- **ch**: Relative to the width of the "0" (zero)
- **rem**: Relative to the font-size of the root element
- **vw**: Relative to 1% of the width of the viewport *
- **vh**: Relative to 1% of the height of the viewport *
- **vmin**: Relative to 1% of the viewport's* smaller dimension
- **vmax**: Relative to 1% of the viewport's* larger dimension
- **%**: Relative to the parent element

> Viewport refers to the browser window size. For example, if the viewport is 50cm wide, 1vw equals 0.5cm.

> **Tip**: The `em` and `rem` units are practical for creating perfectly scalable layouts.


## Specificity

Think of specificity as a score or rank that determines which style declarations are ultimately applied to an element.

### Specificity Hierarchy

1. **Inline styles**: Attached directly to the element to be styled. Example: `<h1 style="color: #ffffff;">`.
2. **IDs**: Unique identifiers for page elements, such as `#navbar`.
3. **Classes, attributes, and pseudo-classes**: This category includes `.classes`, `[attributes]`, and pseudo-classes like `:hover`, `:focus`, etc.
4. **Elements and pseudo-elements**: This category includes element names and pseudo-elements, such as `h1`, `div`, `:before`, and `:after`.

### Specificity Rules

- In cases of equal specificity, the latest rule takes precedence.
- ID selectors have a higher specificity than attribute selectors.
- Contextual selectors (selectors based on the element's context) are more specific than a single element selector.
- A class selector (`.class`) has higher specificity than any number of element selectors.
- The universal selector (`*`) and inherited values have a specificity of 0.

Understanding specificity is crucial for managing the application of styles in complex web documents.


## Image Background

Two additional values for `background-size` are `contain` and `cover`:

- **`contain`**: Scales the background image to be as large as possible while ensuring both its width and height fit inside the content area.
- **`cover`**: Scales the background image to fully cover the content area, ensuring that both its width and height equal or exceed the content area.

### Full-Size Background Image

```css
html {
  background: url(img_man.jpg) no-repeat center fixed;
  background-size: cover;
}
```

## `background-origin` Property

The CSS `background-origin` property specifies where the background image is positioned and accepts three values:

- **`border-box`**: The background image starts from the upper-left corner of the border.
- **`padding-box` (default)**: The background image starts from the upper-left corner of the padding edge.
- **`content-box`**: The background image starts from the upper-left corner of the content.

Understanding these properties allows you to control how background images are positioned within elements.

## Gradients

[CSS gradients](https://www.w3schools.com/css/css3_gradients.asp) allow you to display smooth transitions between two or more specified colors.

CSS defines two types of gradients:

1. **Linear Gradients**: These gradients can go in various directions, including down, up, left, right, or diagonally.

**Syntax**:
```css
background-image: linear-gradient(direction, color-stop1, color-stop2, ...);
```

2. **Radial Gradients**: Radial gradients are defined by their center point and can create circular or elliptical gradients.

**Syntax**:
```css
background-image: radial-gradient(shape size at position, start-color, ..., last-color);
```

## Shadow Effects

### Text Shadow

The CSS `text-shadow` property is used to apply shadow to text, creating visual depth and highlighting.

```css
/* Adding a text shadow to an element with ID "exampleText" */
#exampleText {
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
}
```

### Box Shadow

The CSS `box-shadow` property is used to apply shadow to elements, such as divs or buttons. This creates a visual effect where the element appears to lift off the page or cast a shadow on other elements.

```css
/* Adding a box shadow to a div with class "exampleBox" */
.exampleBox {
  width: 200px;
  height: 100px;
  background-color: #3498db;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.3);
}
```

> Shadow effects are a useful way to add depth and dimension to your web design elements.

## Text Effects

### Text Overflow

The CSS `text-overflow` property specifies how overflowed content that is not displayed should be signaled to the user. It is particularly useful when dealing with text within limited space, like in a container with a fixed width.

```css
/* Display ellipsis (...) at the end of overflowed text */
.overflow-example {
  white-space: nowrap; /* Prevent text from wrapping */
  overflow: hidden; /* Hide overflowed content */
  text-overflow: ellipsis; /* Show ellipsis for overflowed text */
  width: 150px; /* Fixed width container */
}
```

### Word Wrapping

The CSS `word-wrap` property allows long words to be broken and wrap onto the next line. This ensures that text content fits within the given container without causing horizontal scrollbars.

```css
/* Wrap long words to the next line */
.word-wrap-example {
  word-wrap: break-word;
  width: 200px; /* Fixed width container */
}
```

### Word Breaking

The CSS `word-break` property specifies line breaking rules, helping to control how words are divided and wrapped when text content overflows its container.

```css
/* Break words at any character to fit within the container */
.word-break-example {
  word-break: break-all;
  width: 200px; /* Fixed width container */
}
```

### Writing Mode

The CSS `writing-mode` property specifies whether lines of text are laid out horizontally or vertically. It is particularly relevant when working with languages and scripts that are written vertically, such as some Asian languages.

These text effects properties are useful for controlling text presentation and readability in various layout scenarios.

```css
/* Display text content vertically */
.vertical-text-example {
  writing-mode: vertical-rl; /* Right-to-left vertical writing mode */
  width: 30px; /* Fixed width container for vertical text */
}
```

## Web Fonts

### CSS `@font-face` Rule

The CSS `@font-face` rule is used to define web fonts and make them available for use in your web pages. Here's an example of how to use the @font-face rule

```css
@font-face {
  font-family: myFirstFont;
  src: url(sansation_light.woff); /* URL to the font file */
}

div {
  font-family: myFirstFont; /* Use the defined font family for the div element */
}
```


## 2D Transforms

CSS transforms allow you to move, rotate, scale, and skew elements.

Some older browsers need specific prefixes (`-ms-` or `-webkit-`) to understand the 2D transform properties:

```css
div {
  -ms-transform: rotate(20deg); /* IE 9 */
  -webkit-transform: rotate(20deg); /* Safari prior 9.0 */
  transform: rotate(20deg); /* Standard syntax */
}
```

### Transform Methods

- **translate()**: The `translate()` method moves an element from its current position (according to the parameters given for the X-axis and the Y-axis).
- **rotate()**: The `rotate()` method rotates an element clockwise or counter-clockwise according to a given degree.
- **scaleX()**: The `scaleX()` method increases or decreases the width of an element.
- **scaleY()**: The `scaleY()` method increases or decreases the height of an element.
- **scale()**: The `scale()` method increases or decreases the size of an element (according to the parameters given for the width and height).
- **skewX()**: The `skewX()` method skews an element along the X-axis by the given angle.
- **skewY()**: The `skewY()` method skews an element along the Y-axis by the given angle.
- **skew()**: The `skew()` method skews an element along the X and Y-axis by the given angles.
- **matrix()**: The `matrix()` method combines all the 2D transform methods into one.

Example of the `matrix()` method:

```css
transform: matrix(scaleX(), skewY(), skewX(), scaleY(), translateX(), translateY());
```

## 3D Transforms

With the CSS transform property, you can use the following 3D transformation methods:

- **rotateX()**: The `rotateX()` method rotates an element around its X-axis at a given degree.
- **rotateY()**: The `rotateY()` method rotates an element around its Y-axis at a given degree.
- **rotateZ()**: The `rotateZ()` method rotates an element around its Z-axis at a given degree.


## Transitions

CSS transitions allow you to change property values smoothly over a given duration. There are several transition-related properties:

- `transition`
- `transition-delay`
- `transition-duration`
- `transition-property`
- `transition-timing-function`

To create a transition effect, you must specify two things:
1. The CSS property you want to add an effect to.
2. The duration of the effect.

### Change Several Property Values

```css
div {
  width: 100px;
  height: 100px;
  background: red;
  -webkit-transition: width 2s, height 4s; /* For Safari 3.1 to 6.0 */
  transition: width 2s, height 4s;
}
div:hover {
  width: 300px;
  height: 300px;
}
```

### Speed Curve of the Transition

The `transition-timing-function` property specifies the speed curve of the transition effect. There are several options:

- `ease`: Specifies a transition effect with a slow start, then fast, then end slowly (this is default).
- `linear`: Specifies a transition effect with the same speed from start to end.
- `ease-in`: Specifies a transition effect with a slow start.
- `ease-out`: Specifies a transition effect with a slow end.
- `ease-in-out`: Specifies a transition effect with a slow start and end.
- `cubic-bezier(n, n, n, n)`: Lets you define your own values in a cubic-bezier function.

### Delay the Transition Effect

The `transition-delay` property specifies a delay (in seconds) for the transition effect.

You can change as many CSS properties as you want, as many times as you want.

### Transition + Transformation

```css
div {
  transition: width 2s, height 2s, transform 2s;
}
```

Example:

```css
div {
  transition-property: width;
  transition-duration: 2s;
  transition-timing-function: linear;
  transition-delay: 1s;
}
```

## Animations

Animations in CSS allow an element to gradually change from one style to another.

### Keyframes

The `@keyframes` rule is used to define animations with specific styles at various points in time.

Example using `from` and `to`:
```css
@keyframes example {
  from { background-color: red; }
  to { background-color: yellow; }
}
```

It is also possible to use percent. By using percent, you can add as many style changes as you like.

```css
@keyframes example {
  0% { background-color: red; }
  25% { background-color: yellow; }
  50% { background-color: blue; }
  100% { background-color: green; }
}
```
### Delay an Animation

The `animation-delay` property specifies a delay for the start of an animation.

### Set How Many Times an Animation Should Run

The `animation-iteration-count` property specifies the number of times an animation should run. Use "infinite" for continuous animation.

### Run Animation in Reverse Direction or Alternate Cycles

The `animation-direction` property specifies whether an animation should play forwards, backwards, or in alternate cycles.

Values for `animation-direction`:

- `normal` (default): Animation plays forwards.
- `reverse`: Animation plays in reverse.
- `alternate`: Animation alternates between forwards and reverse.
- `alternate-reverse`: Animation alternates, starting in reverse.

### Speed Curve of the Animation

The `animation-timing-function` property specifies the speed curve of the animation.

Values for `animation-timing-function`:

- `ease` (default): Slow start, fast middle, slow end.
- `linear`: Constant speed from start to end.
- `ease-in`: Slow start.
- `ease-out`: Slow end.
- `ease-in-out`: Slow start and end.
- `cubic-bezier(n,n,n,n)`: Define custom values with a cubic-bezier function.

### Specify the Fill Mode For an Animation

The `animation-fill-mode` property specifies a style for the target element when the animation is not playing (before it starts, after it ends, or both).

Values for `animation-fill-mode`:

- `none` (default): No styles applied before or after animation.
- `forwards`: Retain styles from the last keyframe.
- `backwards`: Apply styles from the first keyframe and retain during delay.
- `both`: Follow rules for both forwards and backwards.

Example:

```css
div {
  animation-name: example;
  animation-duration: 5s;
  animation-timing-function: linear;
  animation-delay: 2s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
}

div {
  animation: example 5s linear 2s infinite alternate;
}
```

## Tooltip

A tooltip is a small pop-up box that appears when a user hovers over an element, providing additional information or context. CSS can be used to style and create tooltips for your web applications.

### Creating a Simple Tooltip

A tooltip is a small pop-up box that appears when you hover over an element, providing additional information or context. You can create tooltips in CSS with the following steps:

1. **HTML Structure**: Add the HTML structure for the element that needs a tooltip. For example:

```html
<span class="tooltip-container">
  Hover over me
  <span class="tooltip-text">This is a tooltip</span>
</span>
```

2. **CSS Styles**: Style the tooltip container and text. Make the tooltip text hidden by default and visible on hover. Use CSS position to control the tooltip's placement.

```css
.tooltip-container {
  position: relative;
  display: inline-block;
}

.tooltip-text {
  visibility: hidden;
  background-color: #333;
  color: #fff;
  text-align: center;
  border-radius: 4px;
  padding: 5px;
  position: absolute;
  z-index: 1;
  bottom: 125%;
  left: 50%;
  transform: translateX(-50%);
  transition: visibility 0.2s;
}

.tooltip-container:hover .tooltip-text {
  visibility: visible;
}
```

This CSS creates a tooltip that appears above the element when you hover over it.

## Styling Images

### Rounded Images

You can use the `border-radius` property to create rounded images. This adds a smooth, rounded border to your image.

```css
img {
  border-radius: 8px;
}
```

### Responsive Images

To make an image scale down to fit its container but never scale up beyond its original size, you can use the following CSS:

```css
img {
  max-width: 100%;
  height: auto;
}
```

This ensures that images adapt to various screen sizes, making them responsive.

### Centering an Image
To center an image both horizontally and vertically, set the left and right margins to "auto," and make it a block element:

```css
img {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 50%;
}
```

## `object-fit` Property

The CSS `object-fit` property is used to specify how an `<img>` or `<video>` should be resized to fit its container.

The `object-fit` property can have the following values:

- `fill`: This is the default. The replaced content is sized to fill the element's content box. If necessary, the object will be stretched or squished to fit.

- `contain`: The replaced content is scaled to maintain its aspect ratio while fitting within the element's content box.

- `cover`: The replaced content is sized to maintain its aspect ratio while filling the element's entire content box. The object will be clipped to fit.

- `none`: The replaced content is not resized.

- `scale-down`: The content is sized as if none or contain were specified, which would result in a smaller concrete object size.

You can use the `object-fit` property to control how images and videos are displayed within their containers, making it easier to manage their aspect ratios and sizes.

## Button Styling

### Button Sizes
- Use the `font-size` property to change the font size of a button.

### Rounded Buttons
- Use the `border-radius` property to add rounded corners to a button.

### Colored Button Borders
- Use the `border` property to add a colored border to a button.

### Hoverable Buttons
- Use the `:hover` selector to change the style of a button when you move the mouse over it.

  > Tip: Use the `transition-duration` property to determine the speed of the "hover" effect.

### Shadow Buttons
- Use the `box-shadow` property to add shadows to a button.

### Disabled Buttons
- Use the `opacity` property to add transparency to a button, creating a "disabled" look.

  > Tip: You can also add the `cursor` property with a value of "not-allowed," which will display a "no parking sign" when you mouse over the button.

### Button Width
- By default, the size of the button is determined by its text content, making it as wide as its content. Use the `width` property to change the width of a button.

## Multiple Columns

The CSS multi-column layout allows easy definition of multiple columns of text, similar to how they appear in newspapers. You can control this layout using the following properties:

- `column-count`: Specifies the number of columns an element should be divided into.
- `column-gap`: Specifies the gap between the columns.
- `column-rule-style`: Specifies the style of the rule between columns.
- `column-rule-width`: Specifies the width of the rule between columns.
- `column-rule-color`: Specifies the color of the rule between columns.
- `column-rule`: A shorthand property for setting all the `column-rule-*` properties above.
- `column-span`: Specifies how many columns an element should span across.
- `column-width`: Specifies a suggested, optimal width for the columns.

This set of properties allows you to create text layouts with multiple columns, making it useful for designs that need a newspaper-style appearance.
