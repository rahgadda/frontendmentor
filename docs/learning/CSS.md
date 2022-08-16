# My Learning on CSS

## Basics
**CSS(Cascading Style Sheets)** is used for presentation/apparence on HTML.   
It includes simple changes in font,color,layout etc to complex animations as well.
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
      Has Attribute
      ```html
      <style>
          [data-blue]{
            color: blue;
          }
      </style>
      
      <h1 class="header" data-blue>Selected</h1>
      ```
      Exact Attribute Selector
      ```html
      <style>
          [data-blue="blue"]{
            color: blue;
          }
      </style>

      <h1 class="header" data-blue="blue">Selected</h1>
      ```
      Begins With Attribute Selector
      ```html
      <style>
          [data-active^="t"]{
            color: blue;
          }
      </style>

      <div data-active>Not Selected</div>
      <div data-active="true">Selected</div>
      <div data-active="test">Selected</div>
      <div data-active="false">Not Selected</div>
      ```
      Ends With Attribute Selector
      ```html
      <style>
          [data-active$="e"] {
            color: red;
          }
      </style>

      <div data-active>Not Selected</div>
      <div data-active="apple">Selected</div>
      <div data-active="true">Selected</div>
      <div data-active="test">Not Selected</div>
      ```
      Substring Attribute Selector
      ```html
      <style>
          div[data-active*="e"] {
            color: red;
          }
      </style>

      <div data-active>Not Selected</div>
      <div data-active="apple">Selected</div>
      <div data-active="test">Selected</div>
      <div data-active="gap">Not Selected</div>
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
        ```html
        <style>
          div ~ a {
            color: red;
          }
        </style>

        <a>Not Selected</a>
        <div></div>
        <a>Selected</a>
        <a>Selected</a>
        ```
      - Adjacent Sibling
        ```html
        <style>
          div + a {
            color: red;
          }
        </style>
        
        <a>Not Selected</a>
        <div></div>
        <a>Selected</a>
        <a>Not Selected</a>
        ```
- **Pseudo:**
  - **Classes:**
  - **Elements:**
- **Properties:**   
  Some of generally used properties
  ```html
  <style>
   *{
      padding: 0 0 0 100px; /* top right bottom left*/
      border: width style color;
      font: font-style font-variant font-weight font-size font-family;
    }
  </style>
  ```
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
    - `em`&nbsp;&nbsp;&nbsp;Font size of the parent element
- **Fonts:**   
  - The font property in CSS is used to customise the appearance of text. 
  - Font properties details:  
    - **Font-style:** The font can be made `normal` , `italic`, or `oblique` with this attribute.
    - **Font-variant:** You can use the font-variant property to convert the selected text from `normal` to `small-caps`.
    - **Font-weight:** This allows you to change the Boldness and lightness of the font. Value range from `normal|bold|bolder|lighter|[100  ... 900]]|initial|inherit` 
    - **Font-size:** Updates the size of the font.
    - **Font-family:** This property is used to change the type of the font, like Arial, sans-serif, etc.
    - **Font-color:** Updates the color of the font.
- **Positioning:**
  - **Static:**
  - **Relative:**
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