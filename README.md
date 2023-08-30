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
16. [`position` Property](#position-property)


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
