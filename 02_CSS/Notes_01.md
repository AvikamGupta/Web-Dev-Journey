# 🎨 Introduction to CSS (Cascading Style Sheets)

> **Day 12 – Web Development Journey**
>
> Topic: **Introduction to CSS**
>
> Language: HTML5 + CSS3

---

# 📖 What is CSS?

**CSS (Cascading Style Sheets)** is a stylesheet language used to **design and style HTML webpages**.

HTML creates the **structure** of a webpage, while CSS makes it **beautiful, colorful, responsive, and visually appealing**.

Think of it like this:

🏗️ HTML = Skeleton (Structure)

🎨 CSS = Skin, Clothes & Styling (Appearance)

🧠 JavaScript = Brain (Functionality)

---

# Why do we need CSS?

Imagine a webpage without CSS.

Everything would look plain and boring.

CSS helps us:

- Change text color
- Change background color
- Add spacing
- Set fonts
- Create layouts
- Add animations
- Make websites responsive
- Improve user experience

---

# What does CSS stand for?

CSS = **Cascading Style Sheets**

### Cascading

Means when multiple styles are applied, CSS follows priority rules to decide which style will be used.

Example

```css
p{
    color:red;
}

p{
    color:blue;
}
```

Output

```text
Blue
```

Because the last rule overrides the previous one.

---

# Basic Syntax of CSS

```css
selector{
    property: value;
}
```

Example

```css
div{
    color:blue;
}
```

Here,

- `div` → Selector
- `color` → Property
- `blue` → Value

---

# Parts of a CSS Rule

Example

```css
div{
    color: blue;
    background-color: yellow;
}
```

Explanation

```text
div
│
├── Selector

color
│
├── Property

blue
│
├── Value

background-color
│
├── Property

yellow
│
└── Value
```

---

# CSS Selectors

Selectors tell CSS **which HTML element should be styled.**

Example

```css
div{
    color:red;
}
```

This styles every `<div>` element.

---

# Styling Multiple Elements

Example

```css
div{
    color:blue;
    background-color:yellow;
}

span{
    color:red;
    background-color:aqua;
}
```

Here

Every `<div>` becomes

- Blue text
- Yellow background

Every `<span>` becomes

- Red text
- Aqua background

---

# Your Code Explained

Your HTML

```html
<div>Today is css mood</div>

<div>And here we go</div>

<span>its the time</span>
```

Your CSS

```css
div{
    color: blue;
    background-color: yellow;
}

span{
    color: red;
    background-color: aqua;
}
```

Output

```text
Today is css mood
⬜ Blue Text
🟨 Yellow Background

And here we go
⬜ Blue Text
🟨 Yellow Background

its the time
🟥 Red Text
🟦 Aqua Background
```

---

# What is a Selector?

A selector tells CSS

> "Apply these styles to these HTML elements."

Example

```css
span{
    color:red;
}
```

Only `<span>` elements will be affected.

---

# CSS Properties Used Today

---

## color

Changes the text color.

Example

```css
color:red;
```

Output

Text becomes red.

---

## background-color

Changes the background color.

Example

```css
background-color:yellow;
```

Output

Background becomes yellow.

---

# Types of CSS

There are **three ways** to apply CSS.

---

# 1. Inline CSS

CSS is written directly inside an HTML element.

Example

```html
<h1 style="color:red;">
Hello
</h1>
```

Advantages

- Quick styling

Disadvantages

- Difficult to maintain
- Not reusable
- Not recommended

---

# 2. Internal CSS ✅ (Used in Your Code)

CSS is written inside the `<style>` tag.

Example

```html
<head>

<style>

div{
    color:blue;
}

</style>

</head>
```

Advantages

- Good for small websites
- Easy to understand

Disadvantages

- Cannot reuse across multiple pages

---

# 3. External CSS ⭐ (Most Recommended)

CSS is stored in a separate `.css` file.

Example

HTML

```html
<link rel="stylesheet" href="style.css">
```

style.css

```css
div{
    color:blue;
}
```

Advantages

- Professional
- Reusable
- Faster maintenance
- Used in real-world projects

---

# Priority of CSS

If multiple styles are applied

```text
Inline CSS

⬇

Internal CSS

⬇

External CSS
```

Inline has the highest priority.

> Note: This is the basic priority you'll learn first. Later you'll also study specificity and `!important`, which can affect which rule wins.

---

# Internal CSS Structure

```html
<head>

<style>

selector{

property:value;

}

</style>

</head>
```

---

# HTML + CSS Relationship

```text
HTML

↓

Creates Structure

↓

CSS

↓

Styles Structure

↓

Beautiful Webpage
```

---

# Real Life Example

Without CSS

```text
HELLO

WELCOME

CLICK HERE
```

With CSS

```text
HELLO (Blue)

WELCOME (Large Font)

CLICK HERE (Green Button)
```

---

# Advantages of CSS

✅ Makes webpages beautiful

✅ Reduces repeated code

✅ Easy maintenance

✅ Faster website loading (especially with external CSS)

✅ Responsive design

✅ Better user experience

---

# Common Beginner Mistakes

❌ Forgetting the semicolon

Wrong

```css
color:red
```

Correct

```css
color:red;
```

---

❌ Forgetting curly braces

Wrong

```css
div

color:red;
```

Correct

```css
div{

color:red;

}
```

---

❌ Wrong property name

Wrong

```css
font-colour:red;
```

Correct

```css
color:red;
```

---

❌ Writing CSS outside the `<style>` tag (for internal CSS)

Wrong

```html
<head>

div{
color:red;
}

</head>
```

Correct

```html
<head>

<style>

div{
color:red;
}

</style>

</head>
```

---

# Interview Questions

## Q1. What is CSS?

CSS is a stylesheet language used to style and design HTML webpages.

---

## Q2. What does CSS stand for?

Cascading Style Sheets.

---

## Q3. What are the three types of CSS?

- Inline CSS
- Internal CSS
- External CSS

---

## Q4. Which type of CSS is used in your code?

Internal CSS.

---

## Q5. What is a CSS selector?

A selector tells CSS which HTML elements should receive the specified styles.

---

## Q6. Difference between HTML and CSS?

| HTML | CSS |
|------|------|
| Creates structure | Adds design |
| Defines content | Controls appearance |
| Uses tags | Uses selectors and properties |

---

# Quick Revision Table

| Concept | Meaning |
|----------|----------|
| CSS | Cascading Style Sheets |
| Selector | Selects HTML elements |
| Property | What to style |
| Value | Styling value |
| color | Changes text color |
| background-color | Changes background color |
| Inline CSS | Inside HTML element |
| Internal CSS | Inside `<style>` tag |
| External CSS | Separate `.css` file |

---

# Memory Trick 🚀

```text
HTML → Structure 🏗️

CSS → Styling 🎨

JavaScript → Functionality ⚡
```

Remember CSS Rule

```text
Selector

↓

Property

↓

Value
```

Example

```css
div{

color:blue;

background-color:yellow;

}
```

---

# Key Takeaways

- CSS is used to style HTML webpages.
- HTML creates the structure, while CSS controls the appearance.
- A CSS rule consists of a **selector**, **property**, and **value**.
- `color` changes text color, while `background-color` changes the background.
- CSS can be applied in three ways: **Inline**, **Internal**, and **External**.
- Internal CSS is written inside the `<style>` tag, while External CSS (using a separate `.css` file) is the preferred approach for real-world projects.
- Learning CSS is the first step toward building modern, responsive, and visually appealing websites.
