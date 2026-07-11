# 🎨 Ways to Add CSS in HTML

> **Day 13 – Web Development Journey**
>
> Topic: **Ways to Add CSS to HTML**
>
> Language: HTML5 + CSS3

---

# 📖 Introduction

In the previous lesson, we learned what CSS is and how it styles HTML elements.

Today, we learned **how CSS can be connected to an HTML document.**

There are **three different ways** to apply CSS to an HTML page.

1. Inline CSS
2. Internal CSS
3. External CSS

Every web developer should know all three methods, but in real-world development, **External CSS** is the most commonly used.

---

# Why Do We Need Different Ways?

Suppose you have only one heading.

Using Inline CSS may be fine.

But what if your website has

- 50 pages
- 500 headings
- 100 buttons
- Thousands of lines of HTML

Writing CSS repeatedly would become impossible.

That's why different methods exist.

---

# Three Ways to Add CSS

```text
CSS

│

├── Inline CSS

├── Internal CSS

└── External CSS ⭐ (Most Used)
```

---

# 1. Inline CSS

Inline CSS is written directly inside an HTML element using the **style** attribute.

Syntax

```html
<tag style="property:value;">
```

Example

```html
<h1 style="color:red; background-color:yellow;">
ABOUT ME
</h1>
```

---

## How it Works

```text
HTML Element

↓

style Attribute

↓

CSS Properties

↓

Styled Element
```

---

## Advantages

- Very quick
- Useful for testing
- Good for small changes

---

## Disadvantages

- Code becomes messy
- Cannot reuse styles
- Difficult to maintain
- Not recommended for large websites

---

# 2. Internal CSS

Internal CSS is written inside the `<style>` tag.

The `<style>` tag is placed inside the `<head>` section.

Syntax

```html
<head>

<style>

h1{

color:aqua;

background-color:green;

}

</style>

</head>
```

---

## Example

```html
<style>

h1{

color:aqua;

background-color:green;

}

</style>
```

---

## Advantages

- Better than Inline CSS
- Easy for single-page websites
- All styles remain in one place

---

## Disadvantages

- Cannot reuse in multiple HTML pages
- Large websites become difficult to manage

---

# 3. External CSS ⭐

External CSS is stored in a separate `.css` file.

Example

HTML

```html
<link rel="stylesheet" href="style.css">
```

style.css

```css
h1{

color:aqua;

background-color:green;

}
```

---

## Advantages

✅ Professional

✅ Reusable

✅ Cleaner Code

✅ Faster Maintenance

✅ Used in Real Projects

---

## Disadvantages

- Requires an additional CSS file
- Wrong file path will prevent styles from loading

---

# Understanding `<link>`

Your code contains

```html
<link rel="stylesheet" href="style.css">
```

Explanation

### `<link>`

Connects an external file to the HTML page.

---

### rel="stylesheet"

Tells the browser

> "The linked file is a stylesheet."

---

### href="style.css"

Specifies the location of the CSS file.

---

Flow

```text
HTML File

↓

<link>

↓

style.css

↓

Browser Reads CSS

↓

Styles Applied
```

---

# Your HTML Code Explained

```html
<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Ways to add CSS in our code</title>

<link rel="stylesheet" href="style.css">

</head>

<body>

<h1>ABOUT ME</h1>

<div>

<ol>

<li>INLINE CSS</li>

<li>INTERNAL CSS</li>

<li>EXTERNAL CSS</li>

</ol>

</div>

<div>

I AM A STUDENT ASPIRING EXCELLENCE

</div>

<p>

I AM ABOUT TO JOIN VIT BHOPAL

</p>

</body>

</html>
```

---

## Line-by-Line Explanation

### Title

```html
<title>Ways to add CSS in our code</title>
```

Sets the webpage title.

---

### Link Tag

```html
<link rel="stylesheet" href="style.css">
```

Connects the external CSS file.

---

### Heading

```html
<h1>ABOUT ME</h1>
```

The `<h1>` element will receive the styles written in `style.css`.

---

### Ordered List

```html
<ol>

<li>INLINE CSS</li>

<li>INTERNAL CSS</li>

<li>EXTERNAL CSS</li>

</ol>
```

Displays a numbered list.

Output

```text
1. INLINE CSS

2. INTERNAL CSS

3. EXTERNAL CSS
```

---

### Div

```html
<div>

I AM A STUDENT ASPIRING EXCELLENCE

</div>
```

Displays normal block-level content.

---

### Paragraph

```html
<p>

I AM ABOUT TO JOIN VIT BHOPAL

</p>
```

Creates a paragraph.

---

# Your CSS File Explained

Your CSS

```css
h1{

color:aqua;

background-color:green;

}
```

Explanation

Selector

```css
h1
```

Selects every `<h1>` element.

---

Property

```css
color
```

Changes text color.

Value

```css
aqua
```

---

Property

```css
background-color
```

Changes background color.

Value

```css
green
```

---

Final Output

```text
ABOUT ME

Text → Aqua

Background → Green
```

---

# File Structure

```text
Project Folder

│

├── index.html

└── style.css
```

---

# How Browser Applies External CSS

```text
Browser Opens

↓

index.html

↓

<link> Found

↓

Reads style.css

↓

Matches Selector

↓

Applies Styles

↓

Styled Webpage
```

---

# CSS File Naming

Common names

```text
style.css

styles.css

main.css

index.css
```

---

# Rules for External CSS

✅ CSS file must end with `.css`

✅ HTML and CSS should be in the correct location.

✅ File name must match exactly.

Correct

```html
href="style.css"
```

Wrong

```html
href="Style.css"
```

(File names are case-sensitive on many servers.)

---

# Difference Between Three Methods

| Feature | Inline | Internal | External |
|----------|---------|-----------|-----------|
| Location | Inside HTML element | `<style>` tag | Separate `.css` file |
| Reusable | ❌ | ❌ | ✅ |
| Easy Maintenance | ❌ | ⭐ | ⭐⭐⭐ |
| Professional | ❌ | ⭐⭐ | ⭐⭐⭐⭐⭐ |
| Used in Real Projects | Rarely | Sometimes | Almost Always |

---

# CSS Priority (Basic)

If all three methods style the same element

```text
Inline CSS

↓

Internal CSS

↓

External CSS
```

Inline generally has the highest priority.

> Note: Later you'll learn about **Specificity**, **Cascade**, and `!important`, which refine how CSS decides the winning style.

---

# Best Practices

✅ Use External CSS for almost every project.

✅ Keep HTML and CSS in separate files.

✅ Use meaningful file names like `style.css`.

✅ Organize CSS properly.

✅ Avoid Inline CSS unless absolutely necessary.

---

# Common Beginner Mistakes

❌ Forgetting to link the CSS file.

Wrong

```html
<h1>Hello</h1>
```

(No CSS connected.)

Correct

```html
<link rel="stylesheet" href="style.css">
```

---

❌ Wrong file name

```html
href="styles.css"
```

when the actual file is

```text
style.css
```

The CSS will not load.

---

❌ Writing CSS inside the HTML body

Wrong

```html
<body>

h1{

color:red;

}

</body>
```

Correct

```html
<style>

h1{

color:red;

}

</style>
```

or use an external file.

---

# Interview Questions

## Q1. What are the three ways to apply CSS?

- Inline CSS
- Internal CSS
- External CSS

---

## Q2. Which method is most commonly used in professional projects?

External CSS.

---

## Q3. Why is External CSS preferred?

Because it is reusable, cleaner, easier to maintain, and can style multiple pages using one file.

---

## Q4. What does the `<link>` tag do?

It connects an external resource (such as a CSS file) to the HTML document.

---

## Q5. What does `rel="stylesheet"` mean?

It tells the browser that the linked file is a stylesheet.

---

## Q6. What does `href` represent?

It specifies the path to the external CSS file.

---

# Quick Revision Table

| Concept | Meaning |
|----------|----------|
| Inline CSS | CSS inside an HTML element |
| Internal CSS | CSS inside the `<style>` tag |
| External CSS | CSS in a separate `.css` file |
| `<link>` | Connects external resources |
| `rel="stylesheet"` | Defines the linked file as CSS |
| `href` | Specifies the file path |

---

# Memory Trick 🚀

```text
Inline CSS

↓

One Element

Internal CSS

↓

One Page

External CSS

↓

Entire Website
```

Remember

```text
Inline → Small Changes

Internal → Single Page

External → Professional Websites
```

---

# Key Takeaways

- CSS can be added using **Inline**, **Internal**, or **External** methods.
- **Inline CSS** is applied directly to an HTML element using the `style` attribute.
- **Internal CSS** is written inside the `<style>` tag within the `<head>` section.
- **External CSS** is stored in a separate `.css` file and connected using the `<link>` tag.
- The `<link rel="stylesheet" href="style.css">` tag tells the browser to load styles from an external CSS file.
- External CSS is the **industry standard** because it keeps code organized, reusable, and easier to maintain.
