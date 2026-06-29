# 📖 Note 4 - Images, Tables & Lists in HTML

> **Topics Covered**
>
> - Images (`<img>`)
> - Tables (`<table>`)
> - Table Sections (`<thead>`, `<tbody>`, `<tfoot>`)
> - `colspan`
> - Lists (`<ul>`, `<ol>`, `<dl>`)
> - Important Attributes
> - Best Practices

---

# 🖼️ Images in HTML

Images are displayed using the `<img>` tag.

### Syntax

```html
<img src="image.png" alt="Description">
```

### Example

```html
<img width="230" height="230" src="Vit.png" alt="College image">
```

### Explanation

| Attribute | Purpose |
|-----------|----------|
| `src` | Path of the image |
| `alt` | Alternative text shown if image cannot load |
| `width` | Sets image width |
| `height` | Sets image height |

---

## Why is `alt` important?

The `alt` attribute:

- Improves accessibility.
- Helps screen readers.
- Displays text if image fails to load.
- Helps search engines understand the image.

Example:

```html
<img src="college.png" alt="VIT Bhopal Campus">
```

---

## Width and Height

You can use:

```html
width=""
```

or

```html
height=""
```

or both.

Example:

```html
<img width="300" src="image.png">
```

HTML automatically adjusts the height if only width is provided (keeping aspect ratio).

---

# 📋 Tables in HTML

Tables are used to display data in rows and columns.

Basic structure:

```html
<table>
    <tr>
        <th>Name</th>
        <th>Age</th>
    </tr>

    <tr>
        <td>Avikam</td>
        <td>18</td>
    </tr>
</table>
```

---

# Table Tags

## `<table>`

Creates the complete table.

Example:

```html
<table>
...
</table>
```

---

## `<tr>` (Table Row)

Creates one row.

Example:

```html
<tr>
...
</tr>
```

---

## `<th>` (Table Heading)

Creates heading cells.

Example:

```html
<th>Name</th>
```

By default:

- Bold text
- Center aligned

---

## `<td>` (Table Data)

Stores normal table data.

Example:

```html
<td>Student</td>
```

---

# Table Sections

HTML tables are divided into three parts.

```
Table
│
├── thead
├── tbody
└── tfoot
```

---

## `<thead>`

Contains heading rows.

Example

```html
<thead>
    <tr>
        <th>Name</th>
        <th>Age</th>
    </tr>
</thead>
```

---

## `<tbody>`

Contains the main data.

Example

```html
<tbody>
    <tr>
        <td>Avikam</td>
        <td>18</td>
    </tr>
</tbody>
```

---

## `<tfoot>`

Contains footer information.

Example

```html
<tfoot>
    <tr>
        <td>Total</td>
        <td>2 Students</td>
    </tr>
</tfoot>
```

---

# Table Caption

A title for the table.

Example

```html
<caption>Student Details</caption>
```

Output:

```
Student Details
--------------------
Name   Age
```

---

# colspan Attribute

`colspan` merges multiple columns into one cell.

Example

```html
<td colspan="2">Prakhar</td>
```

Meaning:

This cell occupies **2 columns**.

Visual:

Without colspan

```
| Name | Age | Designation |
```

With colspan="2"

```
|      Prakhar      | Student |
```

---

# HTML Lists

There are **3 types** of lists.

1. Unordered List
2. Ordered List
3. Definition List

---

# 1️⃣ Unordered List (`<ul>`)

Creates a bulleted list.

Example

```html
<ul>
    <li>Apple</li>
    <li>Banana</li>
</ul>
```

Output

```
• Apple
• Banana
```

---

## `<li>`

Represents a list item.

Example

```html
<li>Avikam</li>
```

---

## type Attribute in `<ul>`

Changes bullet style.

Example

```html
<ul type="square">
```

Possible values:

| Type | Output |
|------|---------|
| disc | ● |
| circle | ○ |
| square | ■ |

Example

```html
<ul type="square">
```

Output

```
■ Avikam
■ Devansh
■ Ojha
```

---

# 2️⃣ Ordered List (`<ol>`)

Creates a numbered list.

Example

```html
<ol>
    <li>HTML</li>
    <li>CSS</li>
</ol>
```

Output

```
1. HTML
2. CSS
```

---

## type Attribute in `<ol>`

Different numbering styles.

Example

```html
<ol type="I">
```

Possible values

| Type | Output |
|------|---------|
| 1 | 1 2 3 |
| A | A B C |
| a | a b c |
| I | I II III |
| i | i ii iii |

Example

```html
<ol type="I">
```

Output

```
I. HTML
II. CSS
III. JavaScript
```

---

# 3️⃣ Definition List (`<dl>`)

Used for terms and their meanings.

Contains:

- `<dl>` → Definition List
- `<dt>` → Definition Term
- `<dd>` → Definition Description

Example

```html
<dl>
    <dt>HTML</dt>
    <dd>HyperText Markup Language</dd>
</dl>
```

Output

```
HTML
    HyperText Markup Language
```

---

# Difference Between Lists

## Unordered List

```html
<ul>
```

Output

```
• Apple
• Banana
```

---

## Ordered List

```html
<ol>
```

Output

```
1. Apple
2. Banana
```

---

## Definition List

```html
<dl>
```

Output

```
Apple
    A fruit

Banana
    Yellow fruit
```

---

# Complete Table Structure

```html
<table>

    <caption>Student Details</caption>

    <thead>
        <tr>
            <th>Name</th>
            <th>Age</th>
        </tr>
    </thead>

    <tbody>
        <tr>
            <td>Avikam</td>
            <td>18</td>
        </tr>
    </tbody>

    <tfoot>
        <tr>
            <td colspan="2">End</td>
        </tr>
    </tfoot>

</table>
```

---

# Best Practices

✅ Always provide an `alt` attribute for images.

✅ Use `thead`, `tbody`, and `tfoot` to organize tables.

✅ Use `caption` to describe the table.

✅ Use `th` only for headings.

✅ Use `td` for normal data.

✅ Use `colspan` only when merging columns.

✅ Use unordered lists for items without sequence.

✅ Use ordered lists when order matters.

✅ Use definition lists for terms and descriptions.

---

# Tags Covered

| Tag | Purpose |
|------|----------|
| `<img>` | Displays an image |
| `<table>` | Creates a table |
| `<caption>` | Table title |
| `<thead>` | Table header |
| `<tbody>` | Main table content |
| `<tfoot>` | Table footer |
| `<tr>` | Table row |
| `<th>` | Table heading |
| `<td>` | Table data |
| `<ul>` | Unordered list |
| `<ol>` | Ordered list |
| `<li>` | List item |
| `<dl>` | Definition list |
| `<dt>` | Definition term |
| `<dd>` | Definition description |

---

# Attributes Covered

| Attribute | Used In | Purpose |
|-----------|----------|----------|
| `src` | `<img>` | Image path |
| `alt` | `<img>` | Alternative text |
| `width` | `<img>` | Image width |
| `height` | `<img>` | Image height |
| `colspan` | `<td>` | Merge columns |
| `type` | `<ul>` / `<ol>` | Changes bullet/number style |

---

# Quick Revision 🚀

- `<img>` → Displays images.
- `src` → Image location.
- `alt` → Alternative text.
- `width` / `height` → Image size.
- `<table>` → Creates a table.
- `<caption>` → Table title.
- `<tr>` → Table row.
- `<th>` → Heading cell.
- `<td>` → Data cell.
- `<thead>` → Header section.
- `<tbody>` → Main data.
- `<tfoot>` → Footer section.
- `colspan` → Merges multiple columns.
- `<ul>` → Bulleted list.
- `<ol>` → Numbered list.
- `<li>` → List item.
- `<dl>` → Definition list.
- `<dt>` → Definition term.
- `<dd>` → Definition description.

---

# Interview Questions

### Q1. What is the purpose of the `alt` attribute?

**Answer:** It provides alternative text if an image fails to load and improves accessibility for screen readers.

---

### Q2. Difference between `<th>` and `<td>`?

- `<th>` is used for table headings (bold and centered by default).
- `<td>` is used for normal table data.

---

### Q3. What is `colspan`?

It merges two or more columns into a single cell.

Example:

```html
<td colspan="2">Merged Cell</td>
```

---

### Q4. Difference between `<ul>` and `<ol>`?

- `<ul>` creates a bulleted (unordered) list.
- `<ol>` creates a numbered (ordered) list.

---

### Q5. What are `<thead>`, `<tbody>`, and `<tfoot>` used for?

They divide a table into header, body, and footer sections, making the table more organized and easier to style.

---

# 🎯 Key Takeaway

This lesson introduced three essential HTML concepts:

- **Images** using `<img>` with attributes like `src`, `alt`, `width`, and `height`.
- **Tables** using `<table>`, `<tr>`, `<th>`, `<td>`, along with semantic sections like `<thead>`, `<tbody>`, `<tfoot>`, and the `colspan` attribute.
- **Lists** in three forms: unordered (`<ul>`), ordered (`<ol>`), and definition (`<dl>`), each serving different purposes for organizing content.

Mastering these elements helps you build structured, readable, and accessible web pages.
