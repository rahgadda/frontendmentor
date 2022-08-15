# My Learning on CSS

## Basics
**CSS(Cascading Style Sheets)** is used for presentation/apparence on HTML.
- **Applying CSS:**    
  - CSS can be added to HTML documents in 3 ways as given below.
  - `Internal/External` rules that appear later in the code override earlier rules if both have the same specificity.
  - `Inline` CSS take preceidence over `Internal/External`.
    - **Inline:**
      ```html
      <h1 style="color:blue;">A Blue Heading</h1>
      ```
    - **Internal:**
      ```html
      <style>
          h1   {color: blue;}
      </style>
      ```
    - **External:**
      ```html
      <head>
          <link rel="stylesheet" href="styles.css">
      </head>
      ```
- **Selector:**
  - A more specific selector takes precedence over a less specific one. Example `id` overrides `class` overrides `element`.
  - A css rule with `!important` always takes precedence.
    - **tag:** 
    - **id:** 
    - **class:** 
    - **nesting:**
    - **univesal:**   
      `*, *::before, *::after`
- **Properties:**
- **Box Model:** 
  - Browser rendering engine using this model to represent each element.
  - Every box is composed of four parts.
    - **Content:** Contains the `real` content of the element.
    - **Padding:** Extends the content area to include the element's padding.
    - **Border:** Extends the padding area to include the element's borders.
    - **Margin:** Extends the border area to include an empty area used to separate the `element from its neighbors`.
    ![](./images/boxmodel.png)
- **Units:**
- **Fonts:**
- **Positioning:**
  - **Static:**
  - **Relative:**
- **Pseudo:**
  - **Classes:**
  - **Elements:**
- **Transitions:**
- **Animations:**
- **Box Sizing:**
  - **content-box:** `Default` The width and height properties (and min/max properties) includes only the content. Border and padding are not included.
  - **border-box:** The width and height properties (and min/max properties) includes content, padding and border
  - **initial:** Sets this property to its default value
  - **inherit:** Inherits this property from its parent element
- **Box Alignment:**
- **Media Queries:**
- **Layouts:**
  - **Flex Box:**
  - **Grid:**