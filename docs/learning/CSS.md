# My Learning on CSS

## Basics
**CSS(Cascading Style Sheets)** is used for presentation/apparence on HTML.
- **Applying CSS:**    
  - CSS can be added to HTML documents in 3 ways as given below.
    - **Inline:**
      ```html
      <h1 style="color:blue;">A Blue Heading</h1>
      ```
    - **Internal:**
      ```html
      <style>
          h1   {color: blue;}
      </style>

      <h1>A Blue Heading</h1>
      ```
    - **External:**
      ```html
      <head>
          <link rel="stylesheet" href="styles.css">
      </head>
      
      <h1>A Blue Heading</h1>
      ```
  - `Internal/External` rules that appear later in the code override earlier rules if both have the same specificity.
  - `Inline` CSS take preceidence over `Internal/External`.
- **Selector:**
  - Selector is used to identify which HTML elements should be selected to have the CSS property values inside the rule applied to them.
  - A more specific selector takes precedence over a less specific one. Example `id` overrides `class` overrides `element`.
  - A CSS rule with `!important` always takes precedence.
    - **Univesal:**
      ```html  
      <style>
          *,*::before,*::after{
            color: blue;
          }
      </style>
      
      <h1 class="header">Testing</h1>
      ```
    - **Element:**
      ```html
      <style>
          h1{
            color: blue;
          }
      </style>
      
      <h1 class="header">Testing</h1>
      ``` 
    - **ID:**
      ```html
      <style>
          #header{
            color: blue;
          }
      </style>
      
      <h1 id="header">Testing</h1>
      ```
    - **Class:**
      ```html
      <style>
          .header{
            color: blue;
          }
      </style>
      
      <h1 class="header">Testing</h1>
      ``` 
    - **Attribue:**
      ```html
      <style>
          [data-blue]{
            color: blue;
          }
      </style>
      
      <h1 class="header" data-blue>Testing</h1>
      ```
      Exact Attribute Selector
      ```html
      <style>
          [data-blue="blue"]{
            color: blue;
          }
      </style>

      <h1 class="header" data-blue="blue">Testing</h1>
      ```
    - **Nesting:**
      - Descendant
        ```html
        <style>
          div span {
            color: red;
          }
        </style>

        <div>
          <span>Selected</span>
          <a>
            <span>Selected</span>
          </a>
        </div>
        <span>Not Selected</span>
        ```
      - Direct Descendant
        ```html
        <style>
          div > span {
            color: red;
          }
        </style>

        <div>
          <span>Selected</span>
          <a>
            <span>Not Selected</span>
          </a>
        </div>
        <span>Not Selected</span>
        ```
      - Sibling 
      - Adjacent Sibling
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
  - **Absolute:**
    - `px` pixle is the defulat absolute size used.
  - **Relative:**
    - `%`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;percentage
    - `rem`&nbsp;Font size of the root element
    - `em`&nbsp;&nbsp;&nbsp;Font size of the parent
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

## Appendix
- Html syntax
  ![](./images/html-syntax.png)