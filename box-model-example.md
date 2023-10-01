# Box Model Example

Let's create an example that visually demonstrates how the CSS Box Model works by adding borders, padding, and margins to a simple HTML element.

**HTML:**

```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" type="text/css" href="styles.css" />
  </head>
  <body>
    <div class="box">Box Model Example</div>
  </body>
</html>
```

**CSS (styles.css):**

```css
/* Apply styles to the box */
.box {
  width: 200px;
  height: 100px;
  background-color: #ff9900; /* Amazon orange */

  /* Border styles */
  border: 5px solid #333; /* Border width, style, color */

  /* Padding */
  padding: 20px; /* Padding on all sides */

  /* Margin */
  margin: 30px; /* Margin on all sides */
}
```

In this example, we have a `<div>` element with the class "box," representing a simple box. We apply various CSS properties to demonstrate the Box Model:

1. `width` and `height` set the dimensions of the content area.
2. `background-color` sets the background color of the content area.
3. `border` sets a border around the content area. It specifies the border width, style, and color.
4. `padding` adds padding inside the content area, creating space between the content and the border.
5. `margin` adds margin outside the border, creating space between the box and surrounding elements.

The CSS properties collectively demonstrate how the content, padding, border, and margin interact to create the final appearance of the box. You'll notice that the total width of the box includes the content width, padding, border, and margin. This illustrates the concept of the CSS Box Model.

When you view this HTML and CSS in a web browser, you'll see how the box is rendered with the specified dimensions, padding, border, and margin, visually showcasing how each part of the Box Model affects the layout of the element.
