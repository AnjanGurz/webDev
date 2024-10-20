# CSS Selectors: Comprehensive Guide

## 1. Type Selector
- **Syntax**: `element`
- **Example**: 
    ```css
    p {
      color: blue;
    }
    ```
- **Explanation**: Selects all instances of the specified element (e.g., all `<p>` tags).

---

## 2. Class Selector
- **Syntax**: `.className`
- **Example**: 
    ```css
    .button {
      background-color: green;
    }
    ```
- **Explanation**: Selects all elements with the class `button`.

---

## 3. ID Selector
- **Syntax**: `#id`
- **Example**: 
    ```css
    #header {
      font-size: 20px;
    }
    ```
- **Explanation**: Selects the element with the `id="header"`. Each `id` must be unique.

---

## 4. Universal Selector
- **Syntax**: `*`
- **Example**: 
    ```css
    * {
      margin: 0;
      padding: 0;
    }
    ```
- **Explanation**: Selects all elements on the page.

---

## 5. Group Selector
- **Syntax**: `selector1, selector2, ...`
- **Example**: 
    ```css
    h1, h2, p {
      color: purple;
    }
    ```
- **Explanation**: Applies the same styles to multiple elements.

---

## 6. Descendant Selector
- **Syntax**: `ancestor descendant`
- **Example**: 
    ```css
    div p {
      color: orange;
    }
    ```
- **Explanation**: Selects all `<p>` elements inside any `<div>`.

---

## 7. Child Selector
- **Syntax**: `parent > child`
- **Example**: 
    ```css
    ul > li {
      list-style: none;
    }
    ```
- **Explanation**: Selects only the direct children of the parent (e.g., direct `<li>` children of `<ul>`).

---

## 8. Adjacent Sibling Selector
- **Syntax**: `element1 + element2`
- **Example**: 
    ```css
    h1 + p {
      margin-top: 0;
    }
    ```
- **Explanation**: Selects the first `<p>` immediately following any `<h1>`.

---

## 9. General Sibling Selector
- **Syntax**: `element1 ~ element2`
- **Example**: 
    ```css
    h1 ~ p {
      color: red;
    }
    ```
- **Explanation**: Selects all `<p>` elements that are siblings of an `<h1>`.

---

## 10. Attribute Selectors
- **Syntax**: `[attribute]`, `[attribute="value"]`, `[attribute^="value"]`, `[attribute$="value"]`, `[attribute*="value"]`
- **Examples**: 
    ```css
    input[required] { border: 2px solid red; }      /* Elements with the 'required' attribute */
    input[type="text"] { background-color: gray; }  /* Elements with exact attribute value */
    a[href^="https"] { color: green; }              /* Attribute value starts with "https" */
    img[src$=".jpg"] { border: 1px solid blue; }    /* Attribute value ends with ".jpg" */
    a[href*="google"] { font-weight: bold; }        /* Attribute value contains "google" */
    ```
- **Explanation**: Targets elements based on their attribute and value. Can be used to match starting, ending, or containing strings.

---

## 11. Pseudo-class Selectors
- **Syntax**: `:pseudo-class`
- **Examples**: 
    ```css
    a:hover { color: red; }                  /* When an anchor is hovered */
    li:nth-child(2) { background: yellow; }  /* The second child of a parent */
    input:focus { border-color: green; }     /* When an input is focused */
    ```
- **Explanation**: Targets elements based on a dynamic state like `:hover`, `:focus`, `:nth-child`, etc.

---

## 12. Pseudo-element Selectors
- **Syntax**: `::pseudo-element`
- **Examples**: 
    ```css
    p::before { content: "Note: "; }    /* Adds content before the paragraph */
    p::after { content: " End."; }      /* Adds content after the paragraph */
    ```
- **Explanation**: Selects and styles parts of an element (e.g., text inserted before or after content).

---

## 13. Combinators
### a. Descendant Combinator
- **Syntax**: `parent child`
- **Example**: 
    ```css
    div p {
      color: blue;
    }
    ```
- **Explanation**: Selects all descendants of the specified parent.

### b. Child Combinator
- **Syntax**: `parent > child`
- **Example**: 
    ```css
    ul > li {
      background-color: yellow;
    }
    ```
- **Explanation**: Selects direct children of the parent.

### c. Adjacent Sibling Combinator
- **Syntax**: `element1 + element2`
- **Example**: 
    ```css
    h2 + p {
      margin-top: 0;
    }
    ```
- **Explanation**: Selects the next sibling element following another element.

### d. General Sibling Combinator
- **Syntax**: `element1 ~ element2`
- **Example**: 
    ```css
    h2 ~ p {
      color: blue;
    }
    ```
- **Explanation**: Selects all siblings following the specified element.

---

## 14. Specificity and Importance
- **Order of specificity**:
  1. Inline styles: `1000`
  2. ID selectors: `100`
  3. Class/attribute/pseudo-class: `10`
  4. Type/universal: `1`

- **Example of specificity**:
    ```css
    #nav { color: red; }        /* ID selector (100) */
    .nav { color: blue; }       /* Class selector (10) */
    nav { color: green; }       /* Type selector (1) */
    ```

- **Important Rule**: 
    ```css
    p {
      color: green !important;
    }
    ```
    - **Explanation**: The `!important` rule overrides all other specificity calculations for a given property.
