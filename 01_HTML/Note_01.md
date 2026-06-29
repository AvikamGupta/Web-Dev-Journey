# 📝 Note 1 - HTML Boilerplate, CSS & JavaScript Introduction

## 🎯 Objective

Learn the basic structure of an HTML document and understand how HTML, CSS, and JavaScript work together to create a webpage.

---

# 📄 HTML Boilerplate

Every HTML document begins with a basic structure called the **HTML Boilerplate**.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Avikam's first website</title>
</head>
<body>
    hey this is my first website

    <link rel="stylesheet" href="style.css">
    <script src="script.js"></script>
</body>
</html>
```

---

# 🏗️ HTML Structure Explained

| Tag                         | Purpose                                              |
| --------------------------- | ---------------------------------------------------- |
| `<!DOCTYPE html>`           | Declares the document as an HTML5 document.          |
| `<html>`                    | Root element that contains the entire webpage.       |
| `lang="en"`                 | Specifies that the webpage language is English.      |
| `<head>`                    | Contains metadata and information about the webpage. |
| `<meta charset="UTF-8">`    | Supports almost every character, emoji, and symbol.  |
| `<meta name="viewport"...>` | Makes the webpage responsive on different devices.   |
| `<title>`                   | Sets the browser tab title.                          |
| `<body>`                    | Contains everything visible on the webpage.          |

---

# 📝 `<!DOCTYPE html>`

```html
<!DOCTYPE html>
```

### Purpose

* Declares the document as an **HTML5** document.
* Helps the browser render the webpage correctly.

---

# 📝 `<html lang="en">`

```html
<html lang="en">
```

### Purpose

* Root element of every HTML page.
* `lang="en"` tells browsers and search engines that the page language is English.

---

# 📝 `<head>`

The `<head>` section stores information **about** the webpage.

Examples include:

* Title
* Meta Tags
* CSS Links
* Fonts
* Icons

**Nothing inside `<head>` is displayed directly on the webpage.**

---

# 📝 `<meta charset="UTF-8">`

```html
<meta charset="UTF-8">
```

### Purpose

Defines the character encoding.

UTF-8 supports:

* English
* Hindi
* Emojis 😀
* Special Characters

---

# 📝 Viewport Meta Tag

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Purpose

Makes webpages responsive on mobile phones, tablets, and desktops.

Without this tag, webpages may appear zoomed out on smaller screens.

---

# 📝 `<title>`

```html
<title>Avikam's first website</title>
```

### Purpose

Displays the page title on the browser tab.

Example:

```
Avikam's first website
```

---

# 📝 `<body>`

Everything inside the `<body>` tag is visible on the webpage.

Example:

```html
<body>
    hey this is my first website
</body>
```

Output:

```
hey this is my first website
```

---

# 🎨 Linking CSS

```html
<link rel="stylesheet" href="style.css">
```

### Purpose

Links an external CSS file with the HTML document.

### Attributes

### `rel`

Defines the relationship between the HTML document and the linked file.

```html
rel="stylesheet"
```

Means the linked file contains CSS.

### `href`

Specifies the location of the CSS file.

```html
href="style.css"
```

---

# ⚡ Linking JavaScript

```html
<script src="script.js"></script>
```

### Purpose

Links an external JavaScript file.

### Attribute

### `src`

Specifies the location of the JavaScript file.

```html
src="script.js"
```

---

# 🎨 CSS Introduction

## CSS Code

```css
body{
    background-color: red;
    color: white;
}
```

---

# CSS Syntax

Every CSS rule has three parts.

```css
selector{
    property: value;
}
```

Example:

```css
body{
    background-color: red;
}
```

| Part     | Meaning                   |
| -------- | ------------------------- |
| Selector | Selects the HTML element. |
| Property | Defines what to change.   |
| Value    | Specifies the new value.  |

---

# Body Selector

```css
body
```

Selects the complete webpage.

Any style applied to the body affects the whole page unless overridden.

---

# `background-color`

```css
background-color: red;
```

Changes the webpage background color.

Output:

🔴 Red Background

---

# `color`

```css
color: white;
```

Changes the text color.

Output:

⚪ White Text

---

# JavaScript Introduction

## JavaScript Code

```javascript
alert("Welcome to web development course");
```

---

# `alert()`

`alert()` is a built-in JavaScript function.

### Purpose

Displays a popup message on the browser.

Example Output

```
Welcome to web development course
```

The popup must be closed before interacting with the webpage.

---

# 🔗 Relationship Between HTML, CSS & JavaScript

```
             index1.html
                  │
        ┌─────────┴─────────┐
        │                   │
   style1.css          script1.js
        │                   │
    Styling            Functionality
```

---

# 📚 What Each Technology Does

| Technology | Purpose                                     |
| ---------- | ------------------------------------------- |
| HTML       | Creates the structure of the webpage.       |
| CSS        | Styles the webpage and improves appearance. |
| JavaScript | Adds interactivity and functionality.       |

---

# 🧠 Key Concepts Learned

* HTML Boilerplate
* HTML Document Structure
* HTML5
* `<!DOCTYPE html>`
* `<html>`
* `<head>`
* `<meta>`
* `<title>`
* `<body>`
* CSS Introduction
* CSS Syntax
* Selectors
* Properties
* Values
* `background-color`
* `color`
* Linking CSS
* Linking JavaScript
* JavaScript `alert()`

---

# 📌 Summary

* HTML provides the structure of a webpage.
* CSS controls the design and appearance.
* JavaScript adds interactivity.
* CSS is linked using the `<link>` tag.
* JavaScript is linked using the `<script>` tag.
* The `body` selector styles the entire webpage.
* `alert()` displays a popup message.

---

# ⚡ Quick Revision

✅ HTML = Structure

✅ CSS = Styling

✅ JavaScript = Functionality

✅ `<head>` stores webpage information

✅ `<body>` stores visible content

✅ `<title>` changes the browser tab title

✅ `<link>` connects CSS

✅ `<script>` connects JavaScript

✅ `background-color` changes the page background

✅ `color` changes the text color

✅ `alert()` displays a popup message
