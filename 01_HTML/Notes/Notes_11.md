# 📘 HTML Entities, `<pre>` Tag & `<code>` Tag

> **Day 11 – Web Development Journey**
>
> Topic: **HTML Entities, `<pre>` Tag & `<code>` Tag**
>
> Language: HTML5

---

# 📖 Introduction

While writing HTML, there are some characters that the browser treats as **HTML syntax** instead of normal text.

For example,

```html
<p>Hello</p>
```

The browser interprets this as a paragraph element.

But what if we want to display the text

```html
<p>Hello</p>
```

exactly as it is on the webpage?

This is where **HTML Entities** come into the picture.

---

# What are HTML Entities?

HTML Entities are special codes used to display **reserved characters**, **special symbols**, or **characters that cannot be typed directly** in HTML.

An HTML Entity always starts with

```text
&
```

and ends with

```text
;
```

Example

```html
&lt;
```

Output

```text
<
```

---

# Why do we need HTML Entities?

We use HTML Entities because:

- Some characters are reserved by HTML.
- Some symbols are not available directly on the keyboard.
- We want to display HTML code instead of executing it.
- To create extra spaces where needed.

---

# Syntax

There are two ways to write an HTML Entity.

## 1. Entity Name

```html
&nbsp;
```

---

## 2. Entity Number

```html
&#160;
```

Both produce the same result.

---

# Reserved Characters in HTML

HTML has five important reserved characters.

| Character | Entity |
|-----------|---------|
| < | `&lt;` |
| > | `&gt;` |
| & | `&amp;` |
| " | `&quot;` |
| ' | `&apos;` |

---

# 1. Less Than (`<`)

Without Entity

```html
<p>
```

The browser thinks it is an HTML tag.

Correct way

```html
&lt;p&gt;
```

Output

```text
<p>
```

---

# 2. Greater Than (`>`)

Entity

```html
&gt;
```

Output

```text
>
```

---

# 3. Ampersand (`&`)

Entity

```html
&amp;
```

Output

```text
&
```

Example

```html
HTML &amp; CSS
```

Output

```text
HTML & CSS
```

---

# 4. Double Quotes (`"`)

Entity

```html
&quot;
```

Output

```text
"
```

---

# 5. Apostrophe (`'`)

Entity

```html
&apos;
```

Output

```text
'
```

---

# Commonly Used HTML Entities

## Copyright Symbol

Entity

```html
&copy;
```

Output

```text
©
```

---

## Registered Trademark

Entity

```html
&reg;
```

Output

```text
®
```

---

## Trademark

Entity

```html
&trade;
```

Output

```text
™
```

---

## Rupee Symbol

Entity

```html
&#8377;
```

Output

```text
₹
```

---

## Euro Symbol

Entity

```html
&euro;
```

Output

```text
€
```

---

## Pound Symbol

Entity

```html
&pound;
```

Output

```text
£
```

---

## Degree Symbol

Entity

```html
&deg;
```

Output

```text
°
```

---

## Multiplication Symbol

Entity

```html
&times;
```

Output

```text
×
```

---

## Division Symbol

Entity

```html
&divide;
```

Output

```text
÷
```

---

## Heart Symbol

Entity

```html
&#10084;
```

Output

```text
❤
```

---

# Non-Breaking Space (`&nbsp;`)

Normally HTML ignores multiple spaces.

Example

```html
Hello          World
```

Output

```text
Hello World
```

Only one space is displayed.

---

To create multiple spaces, use

```html
&nbsp;
```

Example

```html
Hello&nbsp;&nbsp;&nbsp;&nbsp;World
```

Output

```text
Hello    World
```

Each `&nbsp;` creates one **non-breaking space**.

---

## Why is it called Non-Breaking Space?

Normally, browsers can move words to the next line.

Example

```text
Hello World
```

The browser may display

```text
Hello
World
```

But if we use

```html
Hello&nbsp;World
```

Both words stay together on the same line whenever possible.

---

# `<pre>` Tag

The `<pre>` tag stands for **Preformatted Text**.

It displays text exactly as written in the HTML file.

It preserves

- Spaces
- Tabs
- Line Breaks

---

Example

```html
<pre>
Hello

This is after many lines.

        This has spaces.
</pre>
```

Output

```text
Hello

This is after many lines.

        This has spaces.
```

---

## Uses of `<pre>`

- Display poems
- ASCII art
- Code formatting
- Terminal output
- Configuration files

---

# Difference Between `<p>` and `<pre>`

| `<p>` | `<pre>` |
|--------|----------|
| Ignores extra spaces | Preserves spaces |
| Ignores extra line breaks | Preserves line breaks |
| Normal text | Preformatted text |

---

Example

```html
<p>
Hello


World
</p>
```

Output

```text
Hello World
```

---

Example

```html
<pre>
Hello


World
</pre>
```

Output

```text
Hello


World
```

---

# `<code>` Tag

The `<code>` tag is used to display programming code.

Example

```html
<code>
console.log("Hello");
</code>
```

Output

```text
console.log("Hello");
```

---

Usually `<code>` is combined with `<pre>`.

Example

```html
<pre>
<code>
print("Hello World")
</code>
</pre>
```

This preserves formatting while displaying code.

---

# Why use `<pre><code>` together?

`<code>` tells the browser:

> "This is programming code."

`<pre>` tells the browser:

> "Keep formatting exactly the same."

Together they create nicely formatted code blocks.

---

# Your Code Explained

You wrote

```html
we use this for paragraph &lt;p&gt;&lt;/p&gt;
```

Explanation

The browser displays

```text
<p></p>
```

instead of creating a paragraph because of the entities

```html
&lt;
```

and

```html
&gt;
```

---

You wrote

```html
<pre>
<p>this is a para</p>


this is after few lines            and some spaces
</pre>
```

Explanation

The `<pre>` tag preserves

- Blank lines
- Multiple spaces
- Formatting

Exactly as written.

---

You wrote

```html
&copy;
```

Output

```text
©
```

---

You wrote

```html
&nbsp;&nbsp;&nbsp;&nbsp;
```

Every `&nbsp;` adds one non-breaking space.

Example

```text
Hello       World
```

---

You wrote

```html
<pre><code>

...
HTML Code
...

</code></pre>
```

This is the professional way of displaying source code on a webpage.

Because

- `<code>` identifies code.
- `<pre>` keeps formatting.

---

# Difference Between `<pre>` and `<code>`

| `<pre>` | `<code>` |
|-----------|------------|
| Preserves formatting | Identifies programming code |
| Displays text exactly as written | Represents code snippets |
| Can contain any text | Usually contains code |
| Often used together with `<code>` | Often placed inside `<pre>` |

---

# Best Practices

✅ Use HTML Entities whenever you want to display HTML tags.

✅ Use `&nbsp;` only when necessary.

✅ Use `<pre>` whenever formatting must remain unchanged.

✅ Wrap programming code inside `<code>`.

✅ Combine `<pre>` and `<code>` for displaying source code.

---

# Common Mistakes

❌ Writing

```html
<p>
```

when you actually want to display it.

Correct

```html
&lt;p&gt;
```

---

❌ Using many normal spaces

```text
Hello       World
```

HTML ignores them.

Correct

```html
Hello&nbsp;&nbsp;&nbsp;&nbsp;World
```

---

❌ Using only `<code>` for long code blocks.

Better

```html
<pre>
<code>

...

</code>
</pre>
```

---

# Interview Questions

## Q1. What are HTML Entities?

HTML Entities are special codes used to display reserved characters and special symbols in HTML.

---

## Q2. Why do we use HTML Entities?

To display reserved characters, special symbols, and HTML code as text instead of letting the browser interpret it.

---

## Q3. What is `&nbsp;`?

`&nbsp;` stands for **Non-Breaking Space**.

It creates a space that the browser does not collapse and tries not to split across lines.

---

## Q4. What is the `<pre>` tag?

The `<pre>` tag displays preformatted text while preserving spaces and line breaks.

---

## Q5. What is the `<code>` tag?

The `<code>` tag represents programming code or code snippets.

---

## Q6. Why are `<pre>` and `<code>` often used together?

`<pre>` preserves formatting, while `<code>` tells the browser that the content is programming code.

---

# Quick Revision Table

| Entity | Output | Purpose |
|---------|--------|---------|
| `&lt;` | `<` | Less than |
| `&gt;` | `>` | Greater than |
| `&amp;` | `&` | Ampersand |
| `&quot;` | `"` | Double quote |
| `&apos;` | `'` | Apostrophe |
| `&copy;` | © | Copyright |
| `&reg;` | ® | Registered |
| `&trade;` | ™ | Trademark |
| `&#8377;` | ₹ | Rupee |
| `&euro;` | € | Euro |
| `&pound;` | £ | Pound |
| `&deg;` | ° | Degree |
| `&times;` | × | Multiplication |
| `&divide;` | ÷ | Division |
| `&nbsp;` | Space | Non-breaking space |

---

# Memory Trick 🚀

```text
&lt;     → Less Than

&gt;     → Greater Than

&amp;    → Ampersand

&nbsp; → Extra Space

&copy; → Copyright

<pre> → Preserve Formatting

<code> → Programming Code

<pre><code> → Display Source Code Professionally
```

---

# Key Takeaways

- HTML Entities allow reserved characters and special symbols to be displayed safely.
- Reserved characters like `<`, `>`, and `&` must be written using entities when shown as text.
- `&nbsp;` creates a non-breaking space and prevents unwanted line breaks.
- `<pre>` preserves spaces, tabs, and line breaks exactly as written.
- `<code>` identifies programming code and is commonly used inside `<pre>` for well-formatted code blocks.
- Using HTML Entities, `<pre>`, and `<code>` is a standard and professional practice in web development, documentation, blogs, and technical websites.
