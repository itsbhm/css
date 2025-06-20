# ✅ Chapter 2: CSS Syntax and Selectors

---

## 🧾 CSS Rule Syntax

A CSS rule is made up of **three parts**:

```css
selector {
  property: value;
}
```

### Example:

```css
p {
  color: red;
  font-size: 16px;
}
```

🟢 This means: “Target all `<p>` elements and make the text red and 16px in size.”

---

## 🏷️ Selectors in CSS

Selectors tell the browser **which elements** to apply styles to.

---

### 1️⃣ Element Selector

Targets all elements of a specific type (like `p`, `h1`, `div`).

```css
h1 {
  color: blue;
}
```

🎯 Affects: All `<h1>` elements

---

### 2️⃣ Class Selector: `.classname`

* Add `class="name"` to any HTML element
* Use `.` in CSS to target it

```html
<p class="highlight">Important note</p>
```

```css
.highlight {
  background-color: yellow;
}
```

🎯 Use when you want to style **multiple elements** the same way

---

### 3️⃣ ID Selector: `#idname`

* Add `id="name"` to a unique element
* Use `#` in CSS to style it

```html
<h2 id="main-title">Welcome</h2>
```

```css
#main-title {
  color: green;
}
```

🛑 Only use **one ID per page**. IDs must be unique!

---

### 4️⃣ Grouping Selectors

Apply same style to multiple selectors:

```css
h1, h2, h3 {
  font-family: Arial;
}
```

✅ Saves time when styling multiple tags the same way

---

## 💡 Hands-On: ID vs Class Styling

### File: `selectors-demo.html`

```html
<!DOCTYPE html>
<html>
<head>
  <title>Selectors Demo</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>

  <h1 id="header-title">Welcome to My Site</h1>

  <p class="info">This is a paragraph with class-based styling.</p>
  <p class="info">This is another paragraph using the same class.</p>

</body>
</html>
```

### File: `style.css`

```css
#header-title {
  color: darkblue;
  text-transform: uppercase;
}

.info {
  font-size: 18px;
  color: gray;
  font-style: italic;
}
```

---

## 🔄 Order of Preference (Specificity)

| Selector Type  | Priority Level |
| -------------- | -------------- |
| Inline Style   | Highest        |
| ID Selector    | High           |
| Class Selector | Medium         |
| Element Tag    | Low            |

📌 In conflicts, **more specific selector wins**.

---

## ✅ Summary

* CSS selectors target **HTML elements**
* Use:

  * `p` for all paragraphs
  * `.className` for reusable styles
  * `#idName` for one-time unique styling
* You can **group** selectors with commas
* **Specificity** determines which style is applied when multiple rules match

---

## 🧪 Exercise

1. Create a file `selectors.html` + `selectors.css`
2. Add:

   * A heading with ID `site-name`
   * 2 paragraphs with class `highlighted`
   * Style them differently using the right selectors
3. Use both element and grouped selectors
