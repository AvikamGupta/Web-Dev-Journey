# 📘 Note 8 – ID and Classes in HTML

## 🎯 Objective

Learn what **ID** and **Class** attributes are in HTML, understand their differences, and know when to use each.

---

# 🆔 What is an ID?

An **ID** is a unique identifier assigned to a single HTML element.

- Each ID should be **unique** on a webpage.
- One element can have **only one ID**.
- IDs are mainly used for:
  - CSS styling
  - JavaScript DOM manipulation
  - Creating bookmarks within a webpage

## ✅ Syntax

```html
<tag id="uniqueName">Content</tag>
```

### Example

```html
<div id="header">Welcome</div>
```

---

# 🏷️ What is a Class?

A **Class** is used to group multiple HTML elements together.

- Many elements can have the **same class**.
- One element can have **multiple classes**.
- Classes are mainly used for:
  - Applying the same CSS styles
  - Selecting multiple elements in JavaScript

## ✅ Syntax

```html
<tag class="className">Content</tag>
```

### Example

```html
<p class="text">Hello</p>
<div class="text">World</div>
```

Both elements belong to the same class and can share the same styling.

---

# 💻 Code Used

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ID and Classes in HTML</title>
    <link rel="stylesheet" href="style.css">
</head>

<body>

    <div id="firstdiv" class="red bg-yellow">
        First
    </div>

    <div id="seconddiv">
        Second
    </div>

    <span class="red"></span>

</body>
</html>
```

---

# 🔍 Code Explanation

## 1. First `<div>`

```html
<div id="firstdiv" class="red bg-yellow">
    First
</div>
```

### Explanation

- ID = **firstdiv**
- Classes = **red** and **bg-yellow**
- The element has **one unique ID**.
- It also belongs to **two different classes**.

This means CSS from both classes will be applied.

---

## 2. Second `<div>`

```html
<div id="seconddiv">
    Second
</div>
```

### Explanation

- ID = **seconddiv**
- No class is assigned.
- Can be styled individually using its unique ID.

---

## 3. `<span>`

```html
<span class="red"></span>
```

### Explanation

- No ID
- Class = **red**

Since it has the same class as the first `<div>`, both can receive identical CSS styling.

---

# 🎨 Multiple Classes

HTML allows multiple classes on the same element.

Example:

```html
<div class="red bg-yellow rounded shadow">
    Hello
</div>
```

This element belongs to **four different classes** simultaneously.

---

# 🎨 CSS Selectors

## Selecting an ID

```css
#firstdiv{
    color: white;
}
```

`#` is used for selecting IDs.

---

## Selecting a Class

```css
.red{
    color: red;
}
```

`.` is used for selecting classes.

---

## Multiple Classes

```css
.bg-yellow{
    background-color: yellow;
}
```

```html
<div class="red bg-yellow">
    Hello
</div>
```

Both styles are applied together.

---

# 📊 Difference Between ID and Class

| Feature | ID | Class |
|----------|----|-------|
| Symbol in CSS | `#` | `.` |
| Must be unique | ✅ Yes | ❌ No |
| Can be reused | ❌ No | ✅ Yes |
| One element can have multiple? | ❌ Only one ID | ✅ Multiple classes |
| Used for | Unique elements | Group of elements |

---

# 🖥️ Visual Representation

```
HTML Page

──────────────────────────

<div id="firstdiv"
     class="red bg-yellow">

<div id="seconddiv">

<span class="red">

──────────────────────────
```

### CSS Connections

```
#firstdiv
     │
     ▼
 First Div Only

.red
     │
     ├────────► First Div
     │
     └────────► Span

.bg-yellow
     │
     ▼
 First Div Only
```

---

# 💡 Easy Trick to Remember

## 🆔 ID

Think of your **Aadhaar Number**.

- Unique
- Belongs to only one person
- Cannot be shared

Similarly,

```
id="firstdiv"
```

belongs to only one HTML element.

---

## 🏷️ Class

Think of a **School Classroom**.

Many students belong to the same class.

Similarly,

```
class="red"
```

can be used on many HTML elements.

---

# ⚡ Best Practices

✅ Use IDs only when an element is unique.

✅ Use Classes for styling multiple elements.

✅ Give meaningful names.

Good

```html
id="navbar"

class="btn"

class="card"
```

Avoid

```html
id="abc"

class="xyz"
```

---

# 📝 Interview Questions

### Q1. What is an ID in HTML?

An ID is a unique identifier assigned to one HTML element.

---

### Q2. Can two elements have the same ID?

❌ No.

Every ID should be unique.

---

### Q3. Can two elements have the same class?

✅ Yes.

Classes are reusable.

---

### Q4. Can one element have multiple classes?

✅ Yes.

Example

```html
<div class="red bg-yellow rounded"></div>
```

---

### Q5. What symbols are used in CSS?

- `#` → ID Selector
- `.` → Class Selector

---

# 🚀 Key Takeaways

- `id` uniquely identifies an HTML element.
- `class` groups similar HTML elements together.
- One element can have only one ID.
- One element can have multiple classes.
- IDs use `#` in CSS.
- Classes use `.` in CSS.
- Classes are preferred for reusable styling.
- IDs are mainly used for unique elements and JavaScript targeting.
- Learning IDs and Classes is essential before moving on to CSS selectors, Flexbox, Grid, and JavaScript DOM manipulation.
