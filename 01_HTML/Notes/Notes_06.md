# 📘 Notes 6 - HTML Forms

## 📖 Introduction

HTML **Forms** ka use user se input collect karne ke liye hota hai. Forms kaafi common hote hain login pages, signup forms, surveys, registrations, feedback forms aur search bars mein.

**Basic Syntax**

```html
<form action="server-url" method="post">
    <!-- Form Elements -->
</form>
```

### Important Attributes

| Attribute | Purpose                                               |
| --------- | ----------------------------------------------------- |
| `action`  | Form submit hone ke baad data kis URL par bhejna hai. |
| `method`  | Data bhejne ka method (`GET` ya `POST`).              |
| `id`      | Element ki unique identity.                           |
| `name`    | Server ko bheja jane wala field name.                 |

---

# 📝 Code Breakdown

## 1️⃣ `<form>`

```html
<form action="post">
```

### Explanation

* Form ki starting hoti hai.
* Iske andar saare input fields aate hain.
* Normally syntax kuch aisa hota hai:

```html
<form action="/submit" method="post">
```

> **⚠️ Note:** Is code mein `action="post"` likha hai jo technically correct nahi hai. Sahi syntax hoga:

```html
<form action="/submit" method="post">
```

---

## 2️⃣ Text Input

```html
<label for="username">Here</label>

<input
type="text"
id="username"
name="username"
placeholder="Enter your username">
```

### Explanation

* `type="text"` → User normal text enter karega.
* `id` → Unique identifier.
* `name` → Form submit hone par server isi naam se value receive karega.
* `placeholder` → Input ke andar hint text.

### Why use `<label>`?

```html
<label for="username">
```

`for` attribute input ke `id` se connect hota hai.

**Benefit**

* Accessibility improve hoti hai.
* Label par click karne se input automatically focus ho jata hai.

---

## 3️⃣ Radio Buttons

```html
<input type="radio" id="Male" name="gender" value="Male">

<label for="Male">Male</label>

<input type="radio" id="female" name="gender" value="female">

<label for="female">Female</label>
```

### Explanation

Radio buttons sirf **ek option** select karne dete hain.

### Important Rule

Agar multiple radio buttons ka

```html
name="gender"
```

same hoga to browser unhe ek group maanega.

Result:

✅ Sirf ek option select hoga.

Agar names alag hote:

```html
name="gender1"

name="gender2"
```

to dono select ho sakte the.

---

## 4️⃣ Checkbox

```html
<input
type="checkbox"
name="Ready"
id="Ready"
value="yes">

<label for="Ready">Are you Ready</label>
```

### Explanation

Checkbox ka use **Yes/No** ya multiple selections ke liye hota hai.

Example:

* Accept Terms & Conditions
* Subscribe Newsletter
* Remember Me

Checkbox ko tick ya untick dono kiya ja sakta hai.

---

## 5️⃣ Textarea

```html
<label for="comment">
Enter your comments
</label>

<textarea
name="comment"
id="comment"
rows="4"
cols="50">
</textarea>
```

### Explanation

Large text input ke liye `<textarea>` use hota hai.

### Attributes

| Attribute | Meaning                  |
| --------- | ------------------------ |
| `rows`    | Height (kitni lines)     |
| `cols`    | Width (kitne characters) |

Example Uses:

* Feedback
* Reviews
* Description
* Comments

---

## 6️⃣ Select Dropdown

```html
<select name="Fruits" id="Fruits">

<option value="apple">Apple</option>

<option value="banana">Banana</option>

<option value="kiwi">Kiwi</option>

</select>
```

### Explanation

Dropdown list create karta hai.

User sirf ek option choose karta hai.

### Components

`<select>` → Dropdown banata hai.

`<option>` → Dropdown ke andar options.

`value` → Server ko bheji jane wali value.

Example

```
Visible Text : Apple

Value Sent   : apple
```

---

# 📚 Form Elements Summary

| Element                   | Purpose                                            |
| ------------------------- | -------------------------------------------------- |
| `<form>`                  | Form create karta hai                              |
| `<input type="text">`     | Text input                                         |
| `<input type="radio">`    | Single option selection                            |
| `<input type="checkbox">` | Multiple/Yes-No selection                          |
| `<textarea>`              | Multi-line text input                              |
| `<select>`                | Dropdown list                                      |
| `<option>`                | Dropdown options                                   |
| `<label>`                 | Input ka label aur accessibility improve karta hai |

---

# 🎯 Best Practices

✅ Hamesha input ke saath `<label>` use karo.

✅ Radio buttons ke liye same `name` rakho.

✅ Meaningful `name` attributes use karo.

✅ Placeholder sirf hint ke liye use karo, label ka replacement nahi.

✅ Proper indentation aur formatting maintain karo.

---

# 💡 Interview Tips

### Difference between Radio Button and Checkbox

| Radio Button                   | Checkbox                                    |
| ------------------------------ | ------------------------------------------- |
| Sirf ek option select hota hai | Ek ya multiple options select ho sakte hain |
| Same `name` required           | Same `name` optional                        |
| Circular UI                    | Square UI                                   |

---

### Difference between Input Text and Textarea

| Input              | Textarea                   |
| ------------------ | -------------------------- |
| Single-line input  | Multi-line input           |
| Chhoti information | Long descriptions/comments |
| `<input>`          | `<textarea></textarea>`    |

---

# ⚡ Key Takeaways

* Forms user input collect karte hain.
* `<label>` accessibility aur usability improve karta hai.
* Radio buttons ek option select karne ke liye use hote hain.
* Checkbox multiple selections ya Yes/No ke liye use hota hai.
* `<textarea>` long text ke liye best hai.
* `<select>` dropdown menu create karta hai.
* `name` attribute server communication ke liye bahut important hota hai.
* `placeholder` sirf hint show karta hai, actual value nahi hoti.

---

# 🧠 Remember

> **Form = Container**
> **Input = Data Entry**
> **Label = Description**
> **Textarea = Large Input**
> **Radio = One Choice**
> **Checkbox = Multiple Choices**
> **Select = Dropdown Menu**
