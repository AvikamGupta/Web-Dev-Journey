# HTML Notes – From Zero to Pretty-Complete

A friendly, interactive-style guide to HTML. Think of this as your personal notebook you can refer to while building real pages.

---

## 1. What is HTML?

- **HTML** = **HyperText Markup Language**
- It’s not a programming language; it’s a **markup** language.
- HTML describes **structure** and **content** of a webpage.
- Browsers read HTML and render it as what you see on screen.

Basic idea:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>My First Page</title>
  </head>
  <body>
    <h1>Hello, world!</h1>
    <p>This is my first webpage.</p>
  </body>
</html>
```

---

## 2. Document Structure

### 2.1 `<!DOCTYPE html>`

- Tells the browser: “This is HTML5”.
- Must be the very first line.

### 2.2 `<html>`

- Root element of the page.
- `lang` attribute helps with accessibility and SEO:

```html
<html lang="en">
```

### 2.3 `<head>`

Contains **meta-information**:

- `<title>` – shown in browser tab.
- `<meta>` – charset, viewport, description, etc.
- `<link>` – external CSS, icons.
- `<style>` – internal CSS.

Example:

```html
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>My Page</title>
  <meta name="description" content="A short description of my page." />
</head>
```

### 2.4 `<body>`

Contains **visible content**: headings, paragraphs, images, forms, etc.

---

## 3. Text Elements

### 3.1 Headings

```html
<h1>Main Title (only one per page ideally)</h1>
<h2>Section title</h2>
<h3>Subsection</h3>
<h4>Further level</h4>
<h5>Even deeper</h5>
<h6>Smallest heading</h6>
```

- Use headings to create a **logical structure** for accessibility and SEO.

### 3.2 Paragraphs & Line Breaks

```html
<p>This is a paragraph.</p>
<p>Another paragraph.</p>

<p>
  This paragraph has multiple lines in the source,
  but the browser shows it as one continuous line
  unless you use line breaks.
</p>

<p>First line<br />Second line</p>
```

- `<br />` = line break.
- `<p>` = paragraph (block element with spacing).

### 3.3 Formatting Text

```html
<p>
  <strong>Bold for importance</strong><br />
  <em>Italic for emphasis</em><br />
  <b>Bold (visual only)</b><br />
  <i>Italic (visual only)</i><br />
  <u>Underline</u><br />
  <mark>Marked/highlighted text</mark><br />
  <small>Small text</small><br />
  <del>Deleted text</del><br />
  <ins>Inserted text</ins><br />
  <code>code snippet</code><br />
  <pre>
Preserved whitespace:
  this line is indented.
  </pre>
</p>
```

Tip:
- Prefer `<strong>` and `<em>` over `<b>` and `<i>` for语义 (semantic meaning).

### 3.4 Quotes & Code

```html
<p>He said <q>Hello</q> to me.</p>

<blockquote>
  This is a long quote from someone.
  It might span multiple lines.
</blockquote>

<p>
  In code: <code>const x = 5;</code>
</p>

<pre><code>
function greet() {
  console.log("Hello!");
}
</code></pre>
```

---

## 4. Lists

### 4.1 Unordered List (`<ul>`)

```html
<ul>
  <li>Apple</li>
  <li>Banana</li>
  <li>Orange</li>
</ul>
```

### 4.2 Ordered List (`<ol>`)

```html
<ol>
  <li>First step</li>
  <li>Second step</li>
  <li>Third step</li>
</ol>
```

You can change numbering style:

```html
<ol type="1">   <!-- 1, 2, 3 -->
<ol type="A">   <!-- A, B, C -->
<ol type="a">   <!-- a, b, c -->
<ol type="I">   <!-- I, II, III -->
<ol type="i">   <!-- i, ii, iii -->
```

### 4.3 Description List (`<dl>`)

```html
<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language</dd>

  <dt>CSS</dt>
  <dd>Cascading Style Sheets</dd>
</dl>
```

Useful for term–definition pairs.

### 4.4 Nested Lists

```html
<ul>
  <li>Fruits
    <ul>
      <li>Apple</li>
      <li>Banana</li>
    </ul>
  </li>
  <li>Vegetables
    <ul>
      <li>Carrot</li>
      <li>Broccoli</li>
    </ul>
  </li>
</ul>
```

---

## 5. Links (`<a>`)

### 5.1 Basic Link

```html
<a href="https://example.com">Visit Example</a>
```

### 5.2 Link Targets

```html
<!-- Open in same tab -->
<a href="page.html">Same tab</a>

<!-- Open in new tab -->
<a href="page.html" target="_blank" rel="noopener noreferrer">New tab</a>
```

### 5.3 Internal Links (Same Page)

```html
<!-- Anchor link -->
<a id="section1">Section 1</a>
...
<a href="#section1">Go to Section 1</a>
```

Or using `id`:

```html
<h2 id="about">About</h2>
<a href="#about">Jump to About</a>
```

### 5.4 Other Link Types

```html
<!-- Email -->
<a href="mailto:someone@example.com">Email me</a>

<!-- Phone -->
<a href="tel:+1234567890">Call me</a>

<!-- Download -->
<a href="file.pdf" download>Download PDF</a>
```

---

## 6. Images (`<img>`)

### 6.1 Basic Image

```html
<img src="image.jpg" alt="A nice landscape" />
```

- `src` = path to image.
- `alt` = alternative text (critical for accessibility).

### 6.2 Image Dimensions

```html
<img src="logo.png" alt="Logo" width="150" height="50" />
```

Or use CSS for better control.

### 6.3 Responsive Images

```html
<img
  src="small.jpg"
  srcset="small.jpg 480w, medium.jpg 768w, large.jpg 1200w"
  sizes="(max-width: 600px) 480px, (max-width: 900px) 768px, 1200px"
  alt="Responsive image"
/>
```

### 6.4 Figures & Captions

```html
<figure>
  <img src="photo.jpg" alt="Group photo" />
  <figcaption>Our team at the conference.</figcaption>
</figure>
```

---

## 7. Tables (`<table>`)

### 7.1 Basic Table

```html
<table>
  <caption>Student Scores</caption>
  <thead>
    <tr>
      <th>Name</th>
      <th>Math</th>
      <th>Science</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Alice</td>
      <td>90</td>
      <td>85</td>
    </tr>
    <tr>
      <td>Bob</td>
      <td>78</td>
      <td>82</td>
    </tr>
  </tbody>
</table>
```

- `<thead>` – header rows.
- `<tbody>` – body rows.
- `<th>` – header cell.
- `<td>` – data cell.

### 7.2 Table Spans

```html
<table>
  <tr>
    <th rowspan="2">Person</th>
    <th colspan="2">Scores</th>
  </tr>
  <tr>
    <th>Math</th>
    <th>Science</th>
  </tr>
  <tr>
    <td>Alice</td>
    <td>90</td>
    <td>85</td>
  </tr>
</table>
```

- `rowspan` – span multiple rows.
- `colspan` – span multiple columns.

### 7.3 Accessibility

- Always use `<caption>` or describe the table in surrounding text.
- Use `<th>` for headers.

---

## 8. Forms (`<form>`)

Forms are how users send data to your server.

### 8.1 Basic Form Structure

```html
<form action="/submit" method="post">
  <!-- inputs here -->
</form>
```

- `action` = where to send data.
- `method` = `get` or `post`.

### 8.2 Labels & Inputs

```html
<form>
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" required />

  <br /><br />

  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required />
</form>
```

- `<label>` improves accessibility.
- `id` links label to input.
- `name` is the key sent to the server.

### 8.3 Input Types

```html
<input type="text" />        <!-- plain text -->
<input type="password" />    <!-- hidden text -->
<input type="number" />      <!-- numbers -->
<input type="email" />       <!-- email validation -->
<input type="tel" />         <!-- phone -->
<input type="url" />         <!-- URL -->
<input type="date" />        <!-- date picker -->
<input type="time" />        <!-- time picker -->
<input type="month" />
<input type="year" />
<input type="datetime-local" />
<input type="checkbox" />    <!-- checkbox -->
<input type="radio" />       <!-- radio button -->
<input type="range" />       <!-- slider -->
<input type="color" />       <!-- color picker -->
<input type="file" />        <!-- file upload -->
<input type="hidden" />      <!-- hidden field -->
<input type="search" />      <!-- search box -->
```

Example with some of them:

```html
<form>
  <label>Age:
    <input type="number" name="age" min="0" max="120" />
  </label>

  <br /><br />

  <label>Like:
    <input type="checkbox" name="likes" value="coding" /> Coding
    <input type="checkbox" name="likes" value="reading" /> Reading
  </label>

  <br /><br />

  <label>Gender:
    <input type="radio" name="gender" value="male" /> Male
    <input type="radio" name="gender" value="female" /> Female
  </label>

  <br /><br />

  <label>Color:
    <input type="color" name="color" />
  </label>

  <br /><br />

  <label>File:
    <input type="file" name="upload" />
  </label>
</form>
```

### 8.4 Textarea

For multi-line text:

```html
<label for="comment">Comment:</label>
<textarea id="comment" name="comment" rows="4" cols="40"></textarea>
```

### 8.5 Select & Options

```html
<label for="country">Country:</label>
<select id="country" name="country">
  <option value="">Select a country</option>
  <option value="in">India</option>
  <option value="us">USA</option>
  <option value="uk">UK</option>
</select>
```

Multiple selection:

```html
<select name="topics" multiple>
  <option value="html">HTML</option>
  <option value="css">CSS</option>
  <option value="js">JavaScript</option>
</select>
```

### 8.6 Buttons

```html
<button type="submit">Submit</button>
<button type="reset">Reset</button>
<button type="button">Plain button</button>
```

- `submit` – sends form.
- `reset` – resets form fields.
- `button` – does nothing by default (use with JS).

### 8.7 Form Validation

```html
<input type="text" required />
<input type="email" required />
<input type="number" min="0" max="100" />
<input type="text" pattern="[A-Za-z]{3,}" />
```

- `required` – must be filled.
- `min`, `max` – numeric limits.
- `pattern` – regex pattern.

You can also use `title` and custom messages with JS, but basic validation is built-in.

---

## 9. Media

### 9.1 Audio

```html
<audio src="song.mp3" controls>
  Your browser does not support audio.
</audio>
```

Attributes:
- `controls` – show play/pause.
- `autoplay` – start automatically (often blocked by browsers).
- `loop` – repeat.
- `preload` – `auto`, `metadata`, `none`.

### 9.2 Video

```html
<video src="movie.mp4" width="640" controls>
  Your browser does not support video.
</video>
```

Same attributes as `<audio>`.

You can provide multiple sources:

```html
<video controls>
  <source src="movie.mp4" type="video/mp4" />
  <source src="movie.webm" type="video/webm" />
  Your browser does not support video.
</video>
```

### 9.3 Embedding External Content

```html
<!-- YouTube example -->
<iframe
  src="https://www.youtube.com/embed/VIDEO_ID"
  width="640"
  height="360"
  title="YouTube video"
></iframe>
```

Be careful with:
- `width`/`height`
- `title` for accessibility
- `sandbox` and other security attributes in real projects.

---

## 10. Semantic HTML

Semantic elements describe **what** content is, not just how it looks.

### 10.1 Layout Semantics

```html
<header>
  <h1>Site Title</h1>
  <nav>
    <a href="/">Home</a>
    <a href="/about">About</a>
  </nav>
</header>

<main>
  <article>
    <h2>Article Title</h2>
    <p>Article content...</p>
  </article>
</main>

<footer>
  <p>&copy; 2026 My Site</p>
</footer>
```

- `<header>` – intro content, often with logo + nav.
- `<nav>` – navigation links.
- `<main>` – main content (only one per page).
- `<article>` – self-contained content.
- `<section>` – thematic grouping.
- `<aside>` – side content (related but separate).
- `<footer>` – ending content.

### 10.2 Time & Details

```html
<time datetime="2026-07-04">July 4, 2026</time>
<mark>Important note</mark>

<details>
  <summary>Click for more</summary>
  <p>Hidden content appears here.</p>
</details>
```

- `<details>` + `<summary>` = interactive disclosure widget.

### 10.3 Figures & Groups

```html
<div class="card">
  <h3>Product</h3>
  <p>Description</p>
  <button>Add to cart</button>
</div>
```

`<div>` is generic; use it when no better semantic element exists.

---

## 11. Accessibility Basics (a11y)

HTML can be made much more accessible with a few habits:

- Use **semantic elements** (`<nav>`, `<main>`, `<button>`, etc.).
- Always provide **alt text** for images.
- Use **labels** for form inputs.
- Use **headings** in order (`h1` → `h2` → `h3`...).
- Avoid using color alone to convey meaning.
- Use `aria-*` attributes only when necessary (advanced).

Example:

```html
<button aria-label="Close dialog">✕</button>
```

---

## 12. Global Attributes

These can be used on almost any element:

```html
<div id="main-content" class="card highlighted" title="Main card">
  Content
</div>
```

Common ones:

- `id` – unique identifier.
- `class` – for styling and grouping.
- `title` – extra info (tooltip in many browsers).
- `lang` – language of element content.
- `dir` – text direction (`ltr` or `rtl`).
- `hidden` – hide element.
- `data-*` – custom data attributes.

Example with `data-*`:

```html
<div data-product-id="123" data-price="999">
  Product
</div>
```

---

## 13. meta & head Extras

### 13.1 Charset & Viewport

```html
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

Essential for modern sites.

### 13.2 SEO & Social

```html
<meta name="description" content="Short description of the page." />
<meta name="keywords" content="html, tutorial, basics" />

<!-- Open Graph for social -->
<meta property="og:title" content="My Page" />
<meta property="og:description" content="Short description." />
<meta property="og:image" content="image.jpg" />
```

### 13.3 Icons

```html
<link rel="icon" href="favicon.ico" type="image/x-icon" />
<link rel="apple-touch-icon" href="apple-icon.png" />
```

---

## 14. Interactive Patterns (Without JavaScript)

HTML alone can do some interactivity:

### 14.1 `<details>` / `<summary>`

Already shown:

```html
<details>
  <summary>Toggle info</summary>
  <p>Hidden content.</p>
</details>
```

### 14.2 Focus & Target

```html
<a href="#section1">Go to Section 1</a>

<section id="section1">
  <h2>Section 1</h2>
  <p>This section is linked.</p>
</section>
```

CSS can use `:focus`, `:hover`, `:target` to change styles based on these states.

---

## 15. Common Pitfalls & Best Practices

- Don’t skip `alt` on images.
- Don’t use `<h1>` for styling; use it for structure.
- Don’t overuse `<div>`; prefer semantic elements.
- Keep forms simple and labeled.
- Test your pages with a basic accessibility checker.
- Use meaningful `id` and `name` attributes.
- Always close elements properly (especially in complex pages).

---

## 16. Mini “Cheat Sheet” by Category

### Structure

- `<!DOCTYPE html>`
- `<html>`, `<head>`, `<body>`
- `<meta>`, `<title>`, `<link>`, `<style>`

### Text

- `<h1>`–`<h6>`, `<p>`, `<br />`
- `<strong>`, `<em>`, `<b>`, `<i>`, `<u>`, `<mark>`
- `<small>`, `<del>`, `<ins>`, `<code>`, `<pre>`
- `<blockquote>`, `<q>`, `<dt>`, `<dd>`

### Lists

- `<ul>`, `<ol>`, `<li>`
- `<dl>`, `<dt>`, `<dd>`

### Links & Images

- `<a href="">`
- `<img src="" alt="" />`
- `<figure>`, `<figcaption>`

### Tables

- `<table>`, `<caption>`
- `<thead>`, `<tbody>`, `<tr>`
- `<th>`, `<td>`
- `colspan`, `rowspan`

### Forms

- `<form>`, `<input>`, `<label>`
- `<textarea>`, `<select>`, `<option>`
- `<button>`
- Types: `text`, `password`, `email`, `number`, `date`, `checkbox`, `radio`, `file`, etc.

### Media

- `<audio>`, `<video>`, `<source>`
- `<iframe>`

### Semantics

- `<header>`, `<nav>`, `<main>`, `<article>`
- `<section>`, `<aside>`, `<footer>`
- `<details>`, `<summary>`, `<time>`, `<mark>`

### Globals

- `id`, `class`, `title`, `lang`, `dir`, `hidden`, `data-*`

---

## 17. How to Use These Notes

- Read a section, then try to build a tiny example on your own.
- Copy snippets into your own HTML files and tweak them.
- Use this as a reference while you code:
  - “How do I make a select dropdown?” → look at Forms → Select.
  - “How do I add an image with caption?” → look at Images → Figures.
- Extend this file:
  - Add your own examples.
  - Add notes about things you discover.

---

## 18. Next Steps After HTML

Once you feel comfortable with HTML:

1. Learn **CSS** to style your pages.
2. Learn **JavaScript** to add real interactivity.
3. Explore **responsive design** and **frameworks** (optional later).

But HTML is the foundation: everything else builds on it.

---

Enjoy building! If you want, you can later add:
- Example pages (e.g., `example-form.html`, `example-table.html`)
- Links to official docs (like [https://developer.mozilla.org/en-US/docs/Web/HTML](https://developer.mozilla.org/en-US/docs/Web/HTML))
- Your own exercises and solutions.
