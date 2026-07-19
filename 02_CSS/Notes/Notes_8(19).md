# 📅 Web Development Journey - Day 19
# Topic: CSS Display Property

---

# 📖 Introduction

The **display** property in CSS controls **how an HTML element is displayed on the webpage**.

Every HTML element has a default display type.

For example:

- `<div>` → Block Element
- `<span>` → Inline Element

Using the `display` property, we can completely change an element's behavior.

---

# 📝 Syntax

```css
selector{
    display: value;
}
```

Example:

```css
.box{
    display: flex;
}
```

---

# 🌟 Default Display Types

| Element | Default Display |
|----------|-----------------|
| div | block |
| span | inline |
| p | block |
| h1-h6 | block |
| img | inline |
| a | inline |

---

# 1️⃣ Block Elements

Block elements:

- Start on a new line.
- Take the full available width.
- Width and height can be changed.
- Margin and padding work normally.

Example:

```html
<div>First Box</div>
<div>Second Box</div>
```

Output:

```
First Box

Second Box
```

---

# 2️⃣ Inline Elements

Inline elements:

- Stay on the same line.
- Only take as much width as needed.
- Width and height usually do not work.
- Horizontal margin and padding work properly.

Example:

```html
<span>Hello</span>
<span>World</span>
```

Output:

```
Hello World
```

---

# 3️⃣ Inline-Block

The **inline-block** display combines features of both inline and block elements.

Properties:

- Appears on the same line.
- Width and height can be set.
- Margin and padding work properly.

Syntax:

```css
display: inline-block;
```

⚠️ **Note:**

In the provided code, it is written as:

```css
display: inline block;
```

This is **incorrect syntax**.

Correct syntax:

```css
display: inline-block;
```

---

# 4️⃣ Flex Display

The code finally uses:

```css
display: flex;
```

Since CSS follows the **last property rule**, this becomes the active display type.

So this line:

```css
display: inline-block;
```

(if written correctly)

gets overridden by:

```css
display: flex;
```

---

# 📖 What is Flexbox?

Flexbox is a layout system used to arrange items easily in rows or columns.

```css
display: flex;
```

makes the element a **Flex Container**.

All direct child elements become **Flex Items**.

---

# justify-content Property

Used for horizontal alignment of flex items.

Example:

```css
.box{
    display:flex;
    justify-content:center;
}
```

Possible values:

- flex-start
- center
- flex-end
- space-between
- space-around
- space-evenly

Example:

```css
justify-content:center;
```

Places content in the center horizontally.

---

# CSS Reset

The code starts with:

```css
*{
    margin:0;
    padding:0;
}
```

The `*` is called the **Universal Selector**.

Purpose:

- Removes default browser spacing.
- Creates a consistent layout.
- Makes designing easier.

---

# Border Property

```css
border:2px solid blue;
```

This creates a border around the element.

Breakdown:

- `2px` → Border thickness
- `solid` → Border style
- `blue` → Border color

---

# Padding

```css
padding:45px;
```

Padding is the space **inside** the border.

It increases the distance between the content and the border.

Example:

```
Border
 ┌───────────────┐
 │   Padding     │
 │  Content      │
 └───────────────┘
```

---

# Margin

```css
margin:34px;
```

Margin is the space **outside** the border.

It creates distance between elements.

Example:

```
Box 1

←34px Gap→

Box 2
```

---

# Width

```css
width:344px;
```

Sets the width of the element to **344 pixels**.

---

# display: none

The code contains:

```css
/* display:none; */
```

It is currently commented.

If enabled:

```css
display:none;
```

Effects:

- Element disappears completely.
- No space is reserved.
- It is removed from the page layout.

Example:

Before:

```
Box 1
Box 2
```

After:

```
Box 2
```

---

# visibility: hidden

The code also contains:

```css
/* visibility:hidden; */
```

If enabled:

```css
visibility:hidden;
```

Effects:

- Element becomes invisible.
- Space remains reserved.

Example:

Before:

```
Box 1
Box 2
```

After:

```
(blank space)

Box 2
```

---

# Difference: display:none vs visibility:hidden

| display:none | visibility:hidden |
|---------------|-------------------|
| Element disappears completely | Element becomes invisible |
| No space is occupied | Space is still occupied |
| Removed from layout | Remains in layout |

---

# Understanding the HTML Code

```html
<div class="box">
    i am a box
</div>

<div class="box">
    also a nice box
</div>
```

Both `<div>` elements:

- Have the same class (`box`).
- Receive the same CSS styling.
- Become flex containers because of `display:flex`.

---

The HTML also contains:

```html
<span>i am a good</span>
<span>boy</span>
```

Since `<span>` is an inline element:

Output:

```
i am a good boy
```

Both appear on the same line.

---

# Important Interview Points

✅ `display` controls how an element appears.

✅ `<div>` is a block element.

✅ `<span>` is an inline element.

✅ `inline-block` combines features of inline and block elements.

✅ `display:flex` creates a flex container.

✅ `justify-content:center` aligns content horizontally.

✅ `display:none` removes the element completely.

✅ `visibility:hidden` hides the element but keeps its space.

✅ Universal selector `*` is commonly used for CSS reset.

✅ If the same property is written multiple times, the **last valid declaration** takes precedence.

---

# Code Summary

```css
*{
    margin:0;
    padding:0;
}

.box{
    border:2px solid blue;
    padding:45px;
    margin:34px;
    width:344px;

    /* Incorrect */
    display:inline block;

    /* Final applied display */
    display:flex;

    justify-content:center;

    /* display:none; */
    /* visibility:hidden; */
}
```

---

# 📚 Key Takeaways

- The **display** property changes how elements are rendered on the page.
- **Block elements** start on a new line and occupy full width.
- **Inline elements** stay on the same line and take only the required width.
- **inline-block** allows inline placement while supporting width and height.
- **Flexbox** is a powerful layout model for aligning and distributing items.
- `justify-content:center` centers flex items horizontally.
- `display:none` removes an element entirely from the layout.
- `visibility:hidden` hides an element while preserving its layout space.
- Always remember that **the last valid CSS declaration overrides earlier ones** when the same property is declared multiple times.
