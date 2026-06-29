# 📘 Notes 3 - HTML Links (Anchor Tag) & Bookmark Manager

## 📌 Topic
HTML Hyperlinks (Anchor Tag), `href`, `target`, and Basic Bookmark Page

---

# 📖 Introduction

Hyperlinks are one of the most important features of HTML.

They allow users to navigate:
- Between different webpages
- To external websites
- To files
- To specific sections of the same page
- To email addresses and phone numbers

In HTML, hyperlinks are created using the **Anchor (`<a>`) Tag**.

---

# 🏗️ Code Breakdown

## 1. HTML Boilerplate

```html
<!DOCTYPE html>
<html lang="en">
```

Declares the document as **HTML5** and specifies that the webpage language is English.

---

## 2. Head Section

```html
<head>
```

Contains metadata about the webpage.

Example from the code:

```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>BookMark manager</title>
```

### Purpose

- UTF-8 supports almost all characters.
- Viewport makes the webpage responsive.
- `<title>` changes the browser tab title.

---

# 3. Body Section

```html
<body>
```

Everything inside the body is displayed on the webpage.

---

# 4. Heading Tags

```html
<h1>My book marks</h1>
<h2>Primary book marks</h2>
```

### `<h1>`

Main heading of the webpage.

### `<h2>`

Sub-heading under the main heading.

Always use headings according to hierarchy.

---

# 5. Anchor Tag (`<a>`)

Syntax

```html
<a href="URL">Link Text</a>
```

Example

```html
<a href="https://www.google.com">
    Open Google
</a>
```

The Anchor tag creates a clickable hyperlink.

---

# 6. `href` Attribute

Example

```html
href="https://www.google.com"
```

### Purpose

`href` stands for **HyperText Reference**.

It specifies the destination where the link should navigate.

Without `href`, the link has no destination.

---

# 7. `target` Attribute

Example

```html
target="_blank"
```

### Purpose

Specifies **where the linked document should open**.

In this code,

```html
target="_blank"
```

means:

👉 Open the webpage in a **new browser tab**.

---

## Common Target Values

| Value | Purpose |
|--------|----------|
| `_self` | Opens in the same tab (Default) |
| `_blank` | Opens in a new tab |
| `_parent` | Opens in the parent frame |
| `_top` | Opens in the full browser window |

---

# 8. Link Examples Used

### Google

```html
<a target="_blank" href="https://www.google.com">
Open Google
</a>
```

Opens Google in a new tab.

---

### Facebook

```html
<a target="_blank" href="https://www.facebook.com">
Open Facebook
</a>
```

Opens Facebook in a new tab.

---

### YouTube

```html
<a target="_blank" href="https://www.youtube.com">
Open Youtube
</a>
```

Opens YouTube in a new tab.

---

# 9. Paragraph Tag with Links

Example

```html
<p>
    <a href="https://google.com">
        Open Google
    </a>
</p>
```

The paragraph tag places each link on a separate line with proper spacing.

---

# 10. HTML Comments

Example

```html
<!-- target section helps to open in a new tab -->
```

### Purpose

Comments are ignored by the browser.

They are used to:

- Explain code
- Leave reminders
- Improve readability
- Document important information

Shortcut in VS Code:

```
Ctrl + /
```

---

# Anchor Tag Attributes

## `href`

Specifies the destination URL.

Example

```html
href="https://google.com"
```

---

## `target`

Specifies where to open the linked page.

Example

```html
target="_blank"
```

---

## `title`

Shows a tooltip when the mouse hovers over the link.

Example

```html
<a href="https://google.com" title="Go to Google">
```

---

## `download`

Downloads the linked file instead of opening it.

Example

```html
<a href="notes.pdf" download>
```

---

# Types of Links

## 1. External Link

Links to another website.

```html
<a href="https://google.com">
```

---

## 2. Internal Link

Links to another page within the same website.

```html
<a href="about.html">
```

---

## 3. Email Link

Opens the user's email application.

```html
<a href="mailto:example@gmail.com">
```

---

## 4. Phone Link

Useful for mobile devices.

```html
<a href="tel:+911234567890">
```

---

## 5. Download Link

```html
<a href="resume.pdf" download>
```

---

# Best Practices

✅ Always use meaningful link text.

Good

```html
Open Google
```

Bad

```html
Click Here
```

---

✅ Use

```html
target="_blank"
```

when linking to external websites.

---

✅ Always include

```html
https://
```

for external links.

---

✅ Organize links using lists or paragraphs for better readability.

---

# Common Mistakes

❌ Forgetting the `href` attribute.

```html
<a>Google</a>
```

This is **not clickable**.

---

❌ Wrong URL

```html
href="google"
```

---

Correct

```html
href="https://www.google.com"
```

---

❌ Typing mistakes in attribute names.

Wrong

```html
hrf=""
```

Correct

```html
href=""
```

---

# HTML Structure of This Page

```
HTML
│
├── Head
│   ├── Meta Charset
│   ├── Viewport
│   └── Title
│
└── Body
    ├── h1
    ├── h2
    ├── Paragraph
    │     └── Google Link
    │
    ├── Paragraph
    │     └── Facebook Link
    │
    ├── Paragraph
    │     └── YouTube Link
    │
    └── Comment
```

---

# Key Points

✅ Anchor tag (`<a>`) creates hyperlinks.

✅ `href` specifies the destination URL.

✅ `target="_blank"` opens the link in a new browser tab.

✅ `<p>` is used here to display each link on a separate line.

✅ HTML comments are ignored by browsers and help explain code.

✅ External links connect to other websites.

✅ Internal links connect to pages within the same website.

---

# Interview Questions

### Q1. Which HTML tag is used to create hyperlinks?

**Answer:** `<a>`

---

### Q2. What does `href` stand for?

**Answer:** HyperText Reference.

---

### Q3. What is the purpose of `target="_blank"`?

**Answer:** It opens the linked webpage in a new browser tab.

---

### Q4. What happens if `href` is missing?

**Answer:** The anchor tag will not navigate anywhere.

---

### Q5. Which tag is used to write comments in HTML?

```html
<!-- Comment -->
```

---

### Q6. Difference between Internal and External Links?

- **Internal Link:** Opens another page within the same website.
- **External Link:** Opens a different website.

---

### Q7. Can an anchor tag link to files?

**Answer:** Yes. It can link to PDFs, images, videos, ZIP files, and more.

---

# Quick Revision

- `<a>` creates hyperlinks.
- `href` specifies the destination.
- `target="_blank"` opens links in a new tab.
- `<p>` keeps links on separate lines.
- HTML comments use `<!-- -->`.
- External links point to other websites.
- Internal links point to pages within the same website.
- `title` shows a tooltip on hover.
- `download` downloads the linked file.
- Use meaningful link text for better readability and accessibility.
