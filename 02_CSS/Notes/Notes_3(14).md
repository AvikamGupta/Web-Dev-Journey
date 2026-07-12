# 🌐 Web Development Journey - Day 14
# Topic: CSS Selectors

---

# 📌 What are CSS Selectors?

CSS Selectors are used to **select HTML elements** so that styles can be applied to them.

Think of selectors as a way to tell CSS:

> "Apply this styling only to these specific elements."

Syntax:

```css
selector{
    property: value;
}
```

Example:

```css
h1{
    color: red;
}
```

This changes every `<h1>` text color to red.

---

# 🎯 Types of CSS Selectors Covered

1. Class Selector
2. ID Selector
3. Child Selector
4. Descendant Selector
5. Universal Selector
6. Pseudo Selectors

---

# 1️⃣ Class Selector

A class selector selects every element having the same class.

Syntax

```css
.className{
    property:value;
}
```

Example

```css
.red{
    background-color: red;
}
```

HTML

```html
<div class="red">
    Hello
</div>
```

Output

The background of the div becomes **red**.

### Why use Class?

- Reusable
- Multiple elements can share one class
- Most commonly used selector

Example

```html
<h1 class="red">Heading</h1>

<p class="red">
Paragraph
</p>

<div class="red">
Div
</div>
```

All three get the same styling.

---

# 2️⃣ ID Selector

Used for selecting one unique element.

Syntax

```css
#idName{
    property:value;
}
```

Example

```css
#yellow{
    background-color: yellow;
}
```

HTML

```html
<div id="yellow">
Hello
</div>
```

Output

Background becomes yellow.

### Difference between Class and ID

| Class | ID |
|--------|----|
| Starts with `.` | Starts with `#` |
| Can be reused | Should be unique |
| Many elements | One element |

---

# 3️⃣ Child Selector (`>`)

Selects only the **direct child**.

Syntax

```css
parent > child{
    property:value;
}
```

Example

```css
div > p{
    color: white;
    background-color: blue;
}
```

HTML

```html
<div>

<p>Hello</p>

</div>
```

Output

The paragraph becomes:

- White text
- Blue background

### Important

Works **only if `<p>` is directly inside `<div>`**.

Example

✅ Selected

```html
<div>
    <p>Hello</p>
</div>
```

❌ Not Selected

```html
<div>

<section>

<p>Hello</p>

</section>

</div>
```

Because `p` is inside `section`, not directly inside `div`.

---

# 4️⃣ Descendant Selector (Space)

Selects every matching element inside another element, no matter how deeply nested.

Syntax

```css
parent child{
    property:value;
}
```

Example

```css
div p{
    color: red;
    background-color: yellow;
}
```

HTML

```html
<div>

<section>

<p>Hello</p>

</section>

</div>
```

Output

The paragraph is selected.

### Difference

Child Selector

```css
div > p
```

Only direct child.

Descendant Selector

```css
div p
```

Any paragraph inside the div.

---

# Child vs Descendant

Example

```html
<div>

<p>Direct Child</p>

<section>

<p>Nested Paragraph</p>

</section>

</div>
```

Child Selector

```css
div > p
```

✔ Selects

```
Direct Child
```

Descendant Selector

```css
div p
```

✔ Selects

```
Direct Child
Nested Paragraph
```

---

# 5️⃣ Universal Selector (`*`)

Selects every element.

Syntax

```css
*{
    property:value;
}
```

Example

```css
*{
    margin:0;
    padding:0;
}
```

This removes default spacing from all elements.

Mostly used as CSS Reset.

---

# 6️⃣ Pseudo Selectors

Pseudo selectors style elements based on **state**.

General Syntax

```css
selector:pseudo{
    property:value;
}
```

---

## a) :visited

Applied after visiting the link.

Example

```css
a:visited{
    color: yellow;
}
```

Visited links become yellow.

---

## b) :link

Styles links that have **not been visited**.

Correct syntax:

```css
a:link{
    color: black;
}
```

⚠ **Important:** In your code, it is written as:

```css
a :link
```

This is incorrect because the space changes the meaning. It should be:

```css
a:link
```

---

## c) :hover

Applied when mouse is over the element.

Example

```css
a:hover{
    background-color: aqua;
}
```

Hovering over the link gives it an aqua background.

---

## d) :active

Applied while clicking the element.

Example

```css
a:active{
    background-color: red;
}
```

While the mouse button is pressed, the background becomes red.

---

## e) :first-child

Selects an element only if it is the **first child** of its parent.

Example

```css
p:first-child{
    background-color: aqua;
}
```

HTML

```html
<main>

<p>First</p>

<p>Second</p>

</main>
```

Output

Only the first paragraph gets an aqua background.

---

# Order of Anchor States

Best practice order:

```css
a:link

a:visited

a:hover

a:active
```

Easy to remember:

> **LVHA**
>
> Link → Visited → Hover → Active

---

# Output Explanation of Today's Code

### First Paragraph

```html
<main>

<p>I am first child</p>

</main>
```

Matches

```css
p:first-child
```

Result

- Aqua Background

---

### Second Paragraph

```html
<p>I am second child</p>
```

Not first child.

No styling.

---

### First Div

```html
<div class="red">
```

Matches

```css
.red
```

Result

Background becomes red.

---

### Paragraph inside First Div

```html
<div>

<p>Hello</p>

</div>
```

Matches

```css
div > p
```

AND

```css
div p
```

Since both have the same specificity and the **descendant selector appears later in the CSS**, it overrides the child selector.

Final Result:

- Red text
- Yellow background

---

### Second Div

```html
<div id="yellow">
```

Matches

```css
#yellow
```

Result

Background becomes yellow.

---

### Google Link

```html
<a href="">
```

Different styles depending on state:

- Normal → Black (`a:link`)
- Visited → Yellow (`a:visited`)
- Hover → Aqua Background (`a:hover`)
- Clicking → Red Background (`a:active`)

*(Remember to correct `a :link` to `a:link`.)*

---

# Specificity (Basic Idea)

When multiple selectors target the same element, CSS decides which style wins.

Priority (Highest → Lowest)

```
Inline Style

↓

ID Selector

↓

Class Selector

↓

Element Selector

↓

Universal Selector
```

If specificity is equal, **the selector written later in the CSS file wins.**

Example

```css
div > p{
    color:white;
}

div p{
    color:red;
}
```

Both select the same paragraph.

Since `div p` comes later, the text becomes **red**.

---

# Best Practices

✅ Use classes for reusable styling.

✅ Use IDs only for unique elements.

✅ Prefer classes over IDs for styling.

✅ Use `*` only for reset styles.

✅ Keep selectors simple.

✅ Write pseudo selectors in the order:

```
Link
Visited
Hover
Active
```

---

# Common Mistakes

❌ Writing

```css
a :link
```

✔ Correct

```css
a:link
```

---

❌ Confusing Child and Descendant

Child

```css
div > p
```

Descendant

```css
div p
```

---

❌ Using the same ID on multiple elements.

IDs should always be unique.

---

# Quick Revision

| Selector | Symbol | Example | Purpose |
|----------|--------|---------|---------|
| Class | `.` | `.red` | Reusable styling |
| ID | `#` | `#yellow` | Unique element |
| Child | `>` | `div > p` | Direct child only |
| Descendant | Space | `div p` | Any nested child |
| Universal | `*` | `*` | Select everything |
| Visited | `:visited` | `a:visited` | Visited links |
| Link | `:link` | `a:link` | Unvisited links |
| Hover | `:hover` | `a:hover` | Mouse over |
| Active | `:active` | `a:active` | While clicking |
| First Child | `:first-child` | `p:first-child` | First child only |

---

# Interview Questions

### Q1. What are CSS selectors?

Selectors are used to target HTML elements so CSS styles can be applied.

---

### Q2. Difference between Class and ID?

Class is reusable.

ID is unique.

---

### Q3. Difference between Child and Descendant selector?

Child (`>`) selects only direct children.

Descendant (space) selects every matching element inside the parent.

---

### Q4. What does the Universal Selector do?

It selects every element on the webpage.

---

### Q5. What is a Pseudo Selector?

A selector that styles an element based on its state (hover, visited, active, etc.).

---

# Day 14 Summary

✅ CSS Selectors

✅ Class Selector

✅ ID Selector

✅ Child Selector

✅ Descendant Selector

✅ Universal Selector

✅ Pseudo Selectors

✅ `:hover`

✅ `:visited`

✅ `:link`

✅ `:active`

✅ `:first-child`

✅ CSS Specificity Basics

✅ Child vs Descendant Difference

---
```
