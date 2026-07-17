# Web Development Journey - Day 17
# Topic: CSS Specificity

## What is CSS Specificity?

CSS Specificity is a set of rules used by the browser to decide **which CSS style should be applied** when multiple selectors target the same HTML element.

In simple words:

> **Higher Specificity = Higher Priority**

If two or more CSS rules target the same element, the browser calculates the specificity of each selector and applies the one with the highest specificity.

---

# Why is CSS Specificity Important?

Imagine you have written multiple CSS rules for the same element.

Example:

```css
h1{
    color: aqua;
}

.cred{
    color: red;
}

.cpurple{
    color: purple;
}
```

Now if your HTML is

```html
<h1 class="cred cpurple">Hello</h1>
```

Which color will be shown?

This is where **CSS Specificity** decides the winner.

---

# How CSS Calculates Specificity

CSS gives different weights to different selectors.

| Selector | Specificity Value |
|-----------|------------------|
| Inline Style | 1000 |
| ID Selector | 100 |
| Class Selector | 10 |
| Attribute Selector | 10 |
| Pseudo-class | 10 |
| Element Selector | 1 |
| Universal Selector (*) | 0 |

---

# 1. Element Selector

Example

```css
h1{
    color:aqua;
}
```

Specificity

```
1
```

Reason

- It targets an HTML element directly.
- Element selectors have the lowest priority.

---

# 2. Class Selector

Example

```css
.cpurple{
    color:purple;
}
```

Specificity

```
10
```

Reason

- Class selectors are more specific than element selectors.

---

# 3. Element + Class Selector

Example

```css
h1.yellow{
    color:yellow;
}
```

Specificity

```
Element = 1
Class = 10

Total = 11
```

This selector is stronger than

```css
h1
```

or

```css
.yellow
```

alone.

---

# 4. Attribute Selector

Example

```css
[data-x=a]{
    color:maroon;
}
```

HTML

```html
<h1 data-x="a">
```

Specificity

```
10
```

Reason

Attribute selectors have the same specificity as class selectors.

---

# 5. Another Class Selector

Example

```css
.cred{
    color:red;
}
```

Specificity

```
10
```

---

# 6. Complex Selector

Example

```css
a.harryclass.rohan-class[href]:hover{
    color:blueviolet;
}
```

Let's calculate:

```
a                = 1
.harryclass      = 10
.rohan-class     = 10
[href]           = 10
:hover           = 10

Total = 41
```

This selector is much stronger because it combines multiple selectors.

---

# HTML Used

```html
<h1 class="yellow cred cpurple" data-x="a">
    CSS Specificity
</h1>
```

This `<h1>` has

- Element → `h1`
- Classes → `yellow`
- `cred`
- `cpurple`
- Attribute → `data-x="a"`

So multiple CSS rules match this element.

---

# Which Rule Wins?

Applicable selectors:

```css
h1
```

Specificity

```
1
```

---

```css
.cpurple
```

Specificity

```
10
```

---

```css
.cred
```

Specificity

```
10
```

---

```css
[data-x=a]
```

Specificity

```
10
```

---

```css
h1.yellow
```

Specificity

```
11
```

Highest specificity is

```
11
```

So this rule wins.

Final Output

```
Text Color = Yellow
```

---

# What if Two Selectors Have the Same Specificity?

Example

```css
.cred{
    color:red;
}

.cpurple{
    color:purple;
}
```

Both have specificity

```
10
```

Now HTML

```html
<h1 class="cred cpurple">
```

Both selectors match.

Since specificity is equal,

**the rule written later in the CSS file wins.**

Output

```
Purple
```

because

```css
.cpurple
```

is written after

```css
.cred
```

This is called the **Cascade Rule**.

---

# Order of Priority in CSS

Highest to Lowest

```
Inline Style
        ↓
ID Selector
        ↓
Class Selector
Attribute Selector
Pseudo-class
        ↓
Element Selector
        ↓
Universal Selector (*)
```

---

# Important Rules of CSS Specificity

### Rule 1

Higher specificity always wins.

Example

```
ID (100)

beats

Class (10)
```

---

### Rule 2

If specificity is equal,

the selector written later in the stylesheet wins.

---

### Rule 3

Inline CSS has the highest priority.

Example

```html
<h1 style="color:red;">
```

Specificity

```
1000
```

It overrides almost every normal CSS rule.

---

### Rule 4

Universal selector has no specificity.

Example

```css
*{
    margin:0;
}
```

Specificity

```
0
```

---

### Rule 5

Multiple selectors add their specificity values together.

Example

```css
h1.red.big[data-x=a]:hover
```

Calculation

```
h1 = 1
.red = 10
.big = 10
[data-x] = 10
:hover = 10

Total = 41
```

---

# Specificity Cheat Sheet

| Selector | Value |
|-----------|-------|
| Inline Style | 1000 |
| ID | 100 |
| Class | 10 |
| Attribute | 10 |
| Pseudo-class | 10 |
| Element | 1 |
| Universal (*) | 0 |

---

# Key Takeaways

- CSS Specificity decides which style is applied when multiple CSS rules target the same element.
- Higher specificity has higher priority.
- Element selectors have the lowest priority.
- Class, attribute, and pseudo-class selectors have the same specificity value (10).
- ID selectors are stronger than class selectors.
- Inline styles have the highest priority.
- If two selectors have the same specificity, the rule written later in the CSS file wins (Cascade Rule).
- Complex selectors combine the specificity values of all their parts.
