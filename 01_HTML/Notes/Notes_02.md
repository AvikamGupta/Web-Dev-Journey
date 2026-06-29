# 📘 Note 2 - HTML Headings & Paragraphs

## 📌 Topic
Introduction to HTML Structure, Headings, Paragraphs & Inline CSS

---

# Complete Code Breakdown

## 1. `<!DOCTYPE html>`

```html
<!DOCTYPE html>
```

### Purpose
- Declares that the document is an **HTML5** document.
- Helps the browser render the page correctly.

> Always write this as the first line of every HTML file.

---

## 2. Root HTML Element

```html
<html lang="en">
```

### Purpose

This is the root element of every HTML page.

### `lang="en"`

- Specifies that the webpage language is English.
- Helps browsers, screen readers, and search engines understand the language.

---

## 3. `<head>` Section

```html
<head>
```

The `<head>` contains information **about the webpage**, not the visible content.

It usually includes:

- Character encoding
- Viewport settings
- Title
- CSS
- JavaScript links
- Meta information

---

## 4. Character Encoding

```html
<meta charset="UTF-8">
```

### Purpose

Defines the character encoding.

### Why UTF-8?

Supports almost every character including:

- English
- Hindi
- Emojis 😄
- Symbols
- Mathematical characters

---

## 5. Viewport Meta Tag

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Purpose

Makes the webpage responsive on different screen sizes.

### Breakdown

`width=device-width`

- Uses the device's actual screen width.

`initial-scale=1.0`

- Opens the page at normal zoom (100%).

Without this tag, webpages may look zoomed out on mobile devices.

---

## 6. Title Tag

```html
<title>My bookmarks-Code with Avikam</title>
```

### Purpose

Sets the title shown on:

- Browser tab
- Search engine results
- Bookmarks

Example:

```
My bookmarks - Code with Avikam
```

---

# Body Section

```html
<body>
```

Everything inside the `<body>` is visible on the webpage.

Examples:

- Headings
- Paragraphs
- Images
- Videos
- Tables
- Forms
- Buttons

---

# HTML Headings

HTML provides **6 heading levels**.

```html
<h1>...</h1>
<h2>...</h2>
<h3>...</h3>
<h4>...</h4>
<h5>...</h5>
<h6>...</h6>
```

### In the code

```html
<h1>My bookmarks Using h1</h1>
<h2>My bookmarks Using h2</h2>
<h3>My bookmarks Using h3</h3>
<h4>My bookmarks Using h4</h4>
<h5>My bookmarks Using h5</h5>
<h6>My bookmarks Using h6</h6>
```

---

## Heading Hierarchy

`<h1>`

- Largest heading
- Most important
- Usually only one per page

`<h2>`

- Main section heading

`<h3>`

- Subsection

`<h4>`

- Sub-subsection

`<h5>`

- Lower-level heading

`<h6>`

- Smallest heading

---

## Best Practice

Use headings according to structure, **not just size**.

Correct Example:

```html
<h1>Website Title</h1>

<h2>About</h2>

<h3>History</h3>

<h2>Contact</h2>
```

Avoid skipping heading levels unnecessarily.

---

# Paragraph Tag

```html
<p>
```

Creates a paragraph of text.

Example:

```html
<p>Hello World!</p>
```

Browsers automatically add spacing before and after paragraphs.

---

# Inline CSS

Your code:

```html
<p style="background-color: aqua;">
```

### What is Inline CSS?

CSS written directly inside an HTML element using the `style` attribute.

Syntax:

```html
<tag style="property:value;">
```

Example:

```html
<p style="color:red;">
```

---

## Background Color

```html
background-color: aqua;
```

Changes the background color of the paragraph.

Result:

- Paragraph background becomes aqua (light blue).

---

# Lorem

Comment from the code:

```
lorem 23
```

### What is Lorem?

In VS Code, typing:

```
lorem
```

or

```
lorem 23
```

generates dummy text automatically.

Example:

```text
Lorem ipsum dolor sit amet...
```

Useful for:

- Testing layouts
- Practicing HTML/CSS
- Filling placeholder content

---

# HTML Structure Recap

```
HTML Document
│
├── <!DOCTYPE html>
│
├── <html>
│
├── <head>
│   ├── meta charset
│   ├── viewport
│   └── title
│
└── <body>
    ├── h1
    ├── h2
    ├── h3
    ├── h4
    ├── h5
    ├── h6
    └── paragraph
```

---

# Key Points

✅ `<!DOCTYPE html>` tells the browser to use HTML5.

✅ `<html>` is the root element.

✅ `<head>` stores metadata (not visible).

✅ `<body>` contains all visible webpage content.

✅ `<title>` changes the browser tab title.

✅ `<meta charset="UTF-8">` supports most characters and symbols.

✅ `<meta viewport>` makes webpages mobile-friendly.

✅ HTML provides six heading levels (`h1` to `h6`).

✅ `<h1>` is the most important heading and should generally be used once per page.

✅ `<p>` creates paragraphs.

✅ Inline CSS is written using the `style` attribute.

✅ `background-color` changes an element's background color.

✅ `lorem` in VS Code quickly generates placeholder text.

---

# Interview Questions

### Q1. What is the purpose of `<!DOCTYPE html>`?

It tells the browser that the document uses HTML5.

---

### Q2. Difference between `<head>` and `<body>`?

- `<head>` contains metadata.
- `<body>` contains visible webpage content.

---

### Q3. What does `<title>` do?

Sets the browser tab title and bookmark name.

---

### Q4. How many heading tags are available in HTML?

Six (`h1` to `h6`).

---

### Q5. Which heading is the most important?

`<h1>`

---

### Q6. What is Inline CSS?

CSS written directly inside an HTML element using the `style` attribute.

Example:

```html
<p style="color:red;">
```

---

### Q7. What does `background-color` do?

Changes the background color of an element.

---

### Q8. Why is the viewport meta tag important?

It makes webpages responsive and display correctly on mobile devices.

---

# Quick Revision

- HTML document starts with `<!DOCTYPE html>`.
- `<html>` is the root element.
- `<head>` stores metadata.
- `<body>` displays visible content.
- `<title>` changes the browser tab text.
- UTF-8 supports most characters.
- Viewport ensures responsiveness.
- `h1` to `h6` define heading hierarchy.
- `<p>` creates paragraphs.
- Inline CSS uses the `style` attribute.
- `background-color` changes the background color.
- `lorem` generates dummy text in VS Code.
