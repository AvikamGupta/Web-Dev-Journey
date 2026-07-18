# 📘 Web Development Journey – Day 18
# Topic: CSS Sizing Units

## 📖 Introduction

In CSS, **Sizing Units** are used to define the width, height, font size, margins, padding, gaps, and many other dimensions of an element.

CSS provides two main categories of sizing units:

1. **Absolute Units** → Fixed size
2. **Relative Units** → Size depends on another value

Choosing the correct unit makes your website responsive and easier to maintain.

---

# 1. Absolute Units

Absolute units always have a fixed size.

| Unit | Meaning |
|------|---------|
| px | Pixels |
| cm | Centimeters |
| mm | Millimeters |
| in | Inches |
| pt | Points |
| pc | Picas |

Example:

```css
.box{
    width:300px;
    height:150px;
}
```

Here the width will always remain **300 pixels**, regardless of screen size.

### 📌 Most commonly used absolute unit:
- **px (Pixels)**

The other absolute units (cm, mm, pt, etc.) are rarely used in web development.

---

# 2. Relative Units

Relative units change depending on screen size, parent size, or font size.

These are used to create responsive websites.

---

# 3. Percentage (%)

Percentage is calculated relative to the parent element.

Example:

```css
.parent{
    width:500px;
}

.child{
    width:50%;
}
```

Result:

```
Parent Width = 500px
Child Width = 250px
```

### Important

If the parent size changes, the child size changes automatically.

---

# 4. Viewport Width (vw)

`1vw = 1% of browser width`

Example:

```css
.box{
    width:50vw;
}
```

If browser width is **1200px**

```
50vw = 600px
```

Useful for making layouts responsive.

---

# 5. Viewport Height (vh)

`1vh = 1% of browser height`

Example:

```css
.hero{
    height:100vh;
}
```

This makes the hero section take the **full height of the screen**.

Very common for landing pages.

---

# 6. vmin

Uses the **smaller value** between viewport width and height.

Example:

```
Viewport Width = 1200px
Viewport Height = 800px

1vmin = 8px
```

Useful when you want sizing based on the smaller screen dimension.

---

# 7. vmax

Uses the **larger value** between viewport width and height.

Example:

```
Viewport Width = 1200px
Viewport Height = 800px

1vmax = 12px
```

Useful when sizing should depend on the larger screen dimension.

---

# 8. em

`em` is relative to the **font size of the parent element**.

Example:

```css
.parent{
    font-size:20px;
}

.child{
    font-size:2em;
}
```

Result:

```
2 × 20px = 40px
```

### Remember

`em` depends on the parent's font size.

---

# 9. rem

`rem` stands for **Root EM**.

It is always relative to the font size of the `<html>` element.

Example:

```css
html{
    font-size:16px;
}

h1{
    font-size:2rem;
}
```

Result:

```
2 × 16px = 32px
```

### Advantage

Unlike `em`, `rem` does not depend on the parent element, making layouts more consistent.

---

# 10. Root Element

The root element of every HTML page is:

```html
<html>
```

Example:

```css
html{
    font-size:18px;
}
```

Now:

```
1rem = 18px
2rem = 36px
3rem = 54px
```

Changing the root font size automatically updates all `rem` values across the website.

---

# 11. Default Browser Font Size

By default,

```css
1rem = 16px
```

unless you change it using:

```css
html{
    font-size:20px;
}
```

---

# 12. Why Responsive Units Matter

Imagine you write:

```css
width:1000px;
```

On a mobile phone, this may overflow the screen.

Instead:

```css
width:90%;
```

or

```css
width:80vw;
```

These automatically adjust to different screen sizes.

---

# 13. Quick Comparison

| Unit | Relative To | Common Use |
|------|-------------|------------|
| px | Fixed size | Borders, icons, small elements |
| % | Parent element | Flexible layouts |
| vw | Viewport width | Responsive width |
| vh | Viewport height | Full-screen sections |
| vmin | Smaller viewport dimension | Responsive sizing |
| vmax | Larger viewport dimension | Special responsive effects |
| em | Parent font size | Component spacing and typography |
| rem | Root (`html`) font size | Consistent fonts and spacing |

---

# 14. Best Practices

✅ Use `rem` for font sizes.

✅ Use `%` for flexible layouts.

✅ Use `vw` and `vh` for responsive sections.

✅ Use `px` for borders and very small fixed elements.

✅ Avoid using `cm`, `mm`, `pt`, and `pc` in web development.

---

# 15. Example

```css
html{
    font-size:16px;
}

.container{
    width:80vw;
    height:70vh;
    padding:2rem;
}

.card{
    width:50%;
    font-size:1.2rem;
    margin:1em;
}
```

Explanation:

- `80vw` → Container width is 80% of the browser width.
- `70vh` → Container height is 70% of the browser height.
- `2rem` → Padding is based on the root font size.
- `50%` → Card width is half of the container width.
- `1.2rem` → Font size is 1.2 times the root font size.
- `1em` → Margin depends on the parent element's font size.

---

# 🎯 Key Takeaways

- **Absolute Units** have fixed sizes (`px`, `cm`, `mm`, etc.).
- **Relative Units** adjust based on the parent, root, or viewport.
- `%` is based on the **parent element**.
- `vw` is based on the **viewport width**.
- `vh` is based on the **viewport height**.
- `vmin` uses the **smaller** viewport dimension.
- `vmax` uses the **larger** viewport dimension.
- `em` is based on the **parent's font size**.
- `rem` is based on the **root (`html`) font size**.
- By default, **1rem = 16px**.
- `rem`, `%`, `vw`, and `vh` are the most commonly used units for building responsive websites.
