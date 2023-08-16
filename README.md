# css-recap

A cheat-sheet for CSS with tips and tricks gathered from different sources. 

I was going through some of my old drives and stumbled upon this complete notes for when I was learning CSS.

## Table of Contents

1. [CSS Selectors](https://github.com/AmirLavasani/css-recap#css-selectors)
    - [Simple Selectors](#1-simple-selectors)
    - [Combinator Selectors](#2-combinator-selectors)
    - [Pseudo-class Selectors](#3-pseudo-class-selectors)
    - [Pseudo-element Selectors](#4-pseudo-element-selectors)
    - [Attribute Selectors](#5-attribute-selectors)
2. [Cascading Order](https://github.com/AmirLavasani/css-recap#cascading-order)
3. [Colors](https://github.com/AmirLavasani/css-recap#colors)
4. [Background Properties](https://github.com/AmirLavasani/css-recap#background)
5. [Border Properties](https://github.com/AmirLavasani/css-recap#border)


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