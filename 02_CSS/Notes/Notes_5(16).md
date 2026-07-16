
# Web Development Journey – Day 16
# Topic: CSS Fonts, Text Styling & Colors

---

# What I Learned Today

Today I learned how to style text using CSS. I learned how to import custom fonts from Google Fonts, change font styles, control spacing between letters and lines, decorate text, transform text into uppercase, and understand different ways to represent colors in CSS.

---

# 1. Google Fonts

Google Fonts provides hundreds of free fonts that can be used in websites.

### Steps to use Google Fonts

1. Open **Google Fonts**
2. Choose a font.
3. Click **Get Font**.
4. Select **Embed Code**.
5. Copy the `@import` code.
6. Paste it at the top of the CSS file.
7. Copy the `font-family` and use it wherever needed.

Example:

```css
@import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400..700&display=swap');
```

Using the font:

```css
h1{
    font-family: "Dancing Script", cursive;
}
```

### Why use Google Fonts?

- Free to use
- Looks more attractive
- Gives websites a professional appearance
- Large collection of fonts

---

# 2. font-family

The `font-family` property specifies which font should be used.

Example:

```css
font-family: "Dancing Script", cursive;
```

Another example:

```css
font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
```

### Fallback Fonts

If the first font is unavailable, the browser tries the next one.

Example:

```css
font-family: Arial, Helvetica, sans-serif;
```

---

# 3. text-decoration

Adds decorations to text.

Example:

```css
text-decoration: underline;
```

Result:

```
Fonts
_____
```

Possible values:

- underline
- overline
- line-through
- none

---

# 4. letter-spacing

Controls the space between letters.

Example:

```css
letter-spacing: 40px;
```

Without:

```
Fonts
```

With large spacing:

```
F   o   n   t   s
```

---

# 5. text-align

Controls horizontal alignment.

Example:

```css
text-align: center;
```

Possible values:

- left
- right
- center
- justify

---

# 6. color

Changes the text color.

Example:

```css
color: darkred;
```

Result:

The heading becomes dark red.

---

# 7. font-style

Changes the style of the font.

Example:

```css
font-style: italic;
```

Possible values:

- normal
- italic
- oblique

---

# 8. font-weight

Controls how thick or bold the text appears.

Example:

```css
font-weight: 500;
```

Common values:

- 100 → Thin
- 200
- 300
- 400 → Normal
- 500 → Medium
- 600
- 700 → Bold
- 800
- 900 → Extra Bold

---

# 9. line-height

Controls the space between lines.

Example:

```css
line-height: 3;
```

Larger values create more vertical spacing.

Without:

```
Line 1
Line 2
```

With larger line-height:

```
Line 1


Line 2
```

---

# 10. text-indent

Adds space before the first line of a paragraph.

Example:

```css
text-indent: 50px;
```

Result:

The first line starts 50px away from the left side.

---

# 11. border

Adds a border around an element.

Example:

```css
border: 2px solid blue;
```

Meaning:

- 2px → Thickness
- solid → Border style
- blue → Border color

---

# 12. text-transform

Changes the case of letters.

Example:

```css
text-transform: uppercase;
```

Result:

```
about the task
```

becomes

```
ABOUT THE TASK
```

Other values:

- uppercase
- lowercase
- capitalize
- none

---

# 13. text-decoration-color

Changes the color of the decoration.

Example:

```css
text-decoration-color: blue;
```

Only the underline becomes blue.

---

# 14. text-decoration-style

Changes the style of the decoration.

Example:

```css
text-decoration-style: wavy;
```

Other values:

- solid
- double
- dotted
- dashed
- wavy

---

# 15. text-decoration-thickness

Controls the thickness of the decoration.

Example:

```css
text-decoration-thickness: 4px;
```

A larger value creates a thicker underline.

---

# 16. text-overflow

Controls what happens when text is too long for its container.

Example:

```css
text-overflow: ellipsis;
```

Ellipsis means:

```
This is a very long tex...
```

### Note

`text-overflow: ellipsis` works properly only when used with properties like:

```css
overflow: hidden;
white-space: nowrap;
```

In this code, only `text-overflow` and `width` are applied, so the effect may not be visible.

---

# 17. width

Defines the width of an element.

Example:

```css
width: 40px;
```

Another example:

```css
width: 500px;
```

A smaller width gives less horizontal space.

---

# 18. Class Selector

HTML:

```html
<p class="lorem">
```

CSS:

```css
.lorem{
    width:500px;
    border:2px solid yellowgreen;
}
```

The dot (`.`) represents a class selector.

---

# 19. word-break

Controls how long words wrap.

Example:

```css
word-break: break-all;
```

Without:

```
Supercalifragilisticexpialidocious
```

It may overflow outside the box.

With `break-all`:

```
Supercalif
ragilistic
expialidoc
ious
```

Useful for long words or URLs.

---

# 20. Styling Ordered Lists

The ordered list is transformed to uppercase.

CSS:

```css
ol{
    text-transform: uppercase;
}
```

Result:

```
1. COLOR KEYWORD
2. HEX COLOR CODE
3. RGB
...
```

---

# 21. Ways to Represent Colors in CSS

Your code lists different ways to define colors.

## 1. Color Keywords

Example:

```css
color: red;
color: blue;
color: darkred;
color: green;
```

Easy to read and remember.

---

## 2. HEX Color Code

Uses hexadecimal values.

Example:

```css
color: #ff0000;
```

Structure:

```
#RRGGBB
```

Example:

```
#000000 → Black
#ffffff → White
#ff0000 → Red
```

---

## 3. RGB

RGB stands for:

- Red
- Green
- Blue

Example:

```css
color: rgb(255,0,0);
```

Range:

```
0–255
```

---

## 4. RGBA

RGBA stands for:

- Red
- Green
- Blue
- Alpha (Transparency)

Example:

```css
color: rgba(255,0,0,0.5);
```

Alpha values:

```
0   → Fully transparent
0.5 → Half transparent
1   → Fully visible
```

**Note:** In your HTML list, `rsba` is written. The correct CSS term is **RGBA**.

---

## 5. HSL

HSL stands for:

- Hue
- Saturation
- Lightness

Example:

```css
color: hsl(0,100%,50%);
```

Meaning:

- Hue → Color
- Saturation → Intensity
- Lightness → Brightness

---

# Code Summary

## h1

```css
font-family: "Dancing Script", cursive;
text-decoration: underline;
letter-spacing: 40px;
text-align: center;
color: darkred;
```

Effects:

- Uses Google Font
- Underlined
- Large letter spacing
- Center aligned
- Dark red text

---

## p

```css
font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
font-style: italic;
font-weight: 500;
line-height: 3;
text-indent: 50px;
border: 2px solid blue;
```

Effects:

- Uses Segoe UI
- Italic text
- Medium weight
- More space between lines
- First line indented
- Blue border

---

## h2

```css
text-transform: uppercase;
text-decoration: underline;
text-decoration-color: blue;
text-decoration-style: wavy;
text-decoration-thickness: 4px;
text-overflow: ellipsis;
width: 40px;
```

Effects:

- Uppercase letters
- Blue wavy underline
- Thick underline
- Small width
- Ellipsis property added (may not show without additional properties)

---

## .lorem

```css
width: 500px;
border: 2px solid yellowgreen;
word-break: break-all;
```

Effects:

- Width set to 500px
- Green border
- Long words wrap automatically

---

## ol

```css
text-transform: uppercase;
```

Effect:

Every list item appears in uppercase.

---

# Important Notes

- `font-family` changes the font.
- Google Fonts allows us to use custom fonts.
- `font-style` changes the text style.
- `font-weight` controls boldness.
- `line-height` controls spacing between lines.
- `letter-spacing` controls spacing between letters.
- `text-indent` adds space before the first line.
- `text-align` aligns text.
- `text-decoration` adds underlines or other decorations.
- `text-transform` changes letter case.
- `word-break` prevents long words from overflowing.
- `text-overflow: ellipsis` usually needs `overflow: hidden` and `white-space: nowrap` to work.
- CSS colors can be represented using **Color Keywords, HEX, RGB, RGBA, and HSL**.
- Your HTML contains `<p><h1>...</h1></p>`, which is **not valid HTML** because a heading (`<h1>`) should not be placed inside a paragraph (`<p>`). The `<h1>` should be outside the `<p>` tag.
```
