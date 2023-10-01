# CSS Inheritance

CSS inheritance is a fundamental concept that describes how styles are inherited by child elements from their parent elements in the HTML document. To explain this concept using plants as an analogy:

Imagine you have a garden with different types of plants. Each type of plant is represented by a different HTML element, and you want to style them with CSS. You have common styles that apply to all plants in the garden (the "parent" styles), and you also have specific styles for certain types of plants (the "child" styles).

Here's a simple example:

**HTML:**

```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" type="text/css" href="styles.css" />
  </head>
  <body>
    <div class="garden">
      <p class="flower">A beautiful flower</p>
      <p class="tree">A tall tree</p>
      <p class="shrub">A small shrub</p>
    </div>
  </body>
</html>
```

**CSS (styles.css):**

```css
/* Common styles for all plants */
.garden {
  font-family: Arial, sans-serif;
  color: #333;
  background-color: #f0f0f0;
}

/* Styles for specific types of plants */
.flower {
  color: #ff69b4; /* Pink color for flowers */
  font-style: italic; /* Italics for flowers */
}

.tree {
  color: #228b22; /* Green color for trees */
  font-weight: bold; /* Bold text for trees */
}

.shrub {
  color: #800000; /* Maroon color for shrubs */
  text-decoration: underline; /* Underlined text for shrubs */
}
```

In this garden analogy:

- The `.garden` class represents the garden itself and applies common styles like `font-family`, `color`, and `background-color` to all the plants in the garden. These styles act as the "parent" styles.

- The `.flower`, `.tree`, and `.shrub` classes represent specific types of plants (flower, tree, and shrub) and apply their unique styles such as `color`, `font-style`, `font-weight`, and `text-decoration`. These styles act as the "child" styles that override or complement the parent styles.

The key concept here is that child elements inherit styles from their parent elements, and you can further customize or override those styles for specific child elements. In this way, you can create a consistent design for all elements while still having the flexibility to apply specific styles to individual elements when needed.

# But some CSS properties are not inherited

Not all CSS properties are inherited by default. CSS properties are categorized into two main groups: inherited properties and non-inherited properties.

1. **Inherited Properties:**

   - Inherited properties are those that are automatically passed down from a parent element to its child elements. Child elements inherit the computed value of these properties unless they are explicitly overridden.
   - Examples of inherited properties include `font-family`, `font-size`, `font-weight`, `color`, `line-height`, and `text-align`. When you set these properties on a parent element, their values are inherited by its child elements.

2. **Non-inherited Properties:**
   - Non-inherited properties are those that are not automatically inherited by child elements. Child elements do not inherit the computed value of these properties unless you specifically apply them to the child element.
   - Examples of non-inherited properties include `border`, `margin`, `padding`, `background`, `width`, `height`, `position`, `display`, and `float`. These properties must be explicitly set on each child element if you want them to have specific values.

Here's an example to illustrate the difference:

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      /* Parent Styles */
      .parent {
        font-family: Arial, sans-serif; /* Inherited */
        background-color: #f0f0f0; /* Non-inherited */
      }

      /* Child Styles */
      .child {
        font-weight: bold; /* Inherited */
        border: 1px solid #333; /* Non-inherited */
      }
    </style>
  </head>
  <body>
    <div class="parent">
      <p class="child">This is a paragraph</p>
    </div>
  </body>
</html>
```

In this example:

- The `font-family` property set on the parent element (`.parent`) is inherited by the child element (`.child`) without the need for additional styling.
- The `background-color` property set on the parent element is not inherited by the child element. If you want the child element to have a background color, you must apply it directly to the child element.
- The `font-weight` property set on the child element is inherited by the child element itself but does not affect other elements.
- The `border` property set on the child element must be applied directly to that element; it does not inherit from the parent.

Understanding the distinction between inherited and non-inherited properties is essential when working with CSS, as it affects how styles cascade and are applied to elements in your web page.
