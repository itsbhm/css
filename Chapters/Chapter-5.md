# ✅ Chapter 5: Box Model and Spacing in CSS

---

## 📦 What is the CSS Box Model?

Every HTML element is treated as a **rectangular box** made up of:

```
| Margin |
| Border |
| Padding |
| Content |
```

### Visual Layers (from outside in):

```
+--------------------------+
|        Margin            |
|  +--------------------+  |
|  |     Border         |  |
|  |  +--------------+  |  |
|  |  |   Padding    |  |  |
|  |  | +----------+ |  |  |
|  |  | | Content  | |  |  |
|  |  | +----------+ |  |  |
|  |  +--------------+  |  |
|  +--------------------+  |
+--------------------------+
```

---

## 🔢 Width and Height

Used to control the size of the content area.

```css
div {
  width: 300px;
  height: 200px;
}
```

🔎 This doesn’t include padding, border, or margin by default!

---

## 🔲 Padding

**Padding** is space **inside the border**, around the content.

```css
div {
  padding: 20px;
}
```

| Use        | Example                       |
| ---------- | ----------------------------- |
| All sides  | `padding: 10px;`              |
| Top/Bottom | `padding: 10px 0;`            |
| Individual | `padding-top`, `padding-left` |

---

## 🟥 Border

The line around the element.

```css
div {
  border: 2px solid black;
}
```

| Value | Example                             |
| ----- | ----------------------------------- |
| Width | `1px`, `5px`                        |
| Style | `solid`, `dashed`, `dotted`, `none` |
| Color | `red`, `#000`, `rgb(...)`           |

---

## ⬜ Margin

**Margin** is the space **outside the element**, pushing it away from others.

```css
div {
  margin: 30px;
}
```

Also works with `margin-top`, `margin-left`, etc.

---

## ✂️ box-sizing: border-box

By default, `width` only applies to content.

Use this to include padding + border inside the box size:

```css
* {
  box-sizing: border-box;
}
```

📌 Great for responsive layouts!

---

## 🧠 Real Example

```css
.card {
  width: 300px;
  padding: 20px;
  border: 2px solid gray;
  margin: 30px auto;
  background-color: #f9f9f9;
  box-sizing: border-box;
}
```

---

## 💡 Hands-On Task: Box Model Demo

### File: `box-model.html`

```html
<!DOCTYPE html>
<html>
<head>
  <title>Box Model</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>

  <div class="card">
    <h2>Box Model</h2>
    <p>This box has padding, margin, and border.</p>
  </div>

</body>
</html>
```

### File: `style.css`

```css
* {
  box-sizing: border-box;
}

body {
  font-family: sans-serif;
  background: #f0f0f0;
}

.card {
  width: 400px;
  padding: 20px;
  border: 3px solid #333;
  margin: 50px auto;
  background-color: #fff;
}
```

🧪 Use browser DevTools → inspect `.card` → see margins/paddings visually

---

## ✅ Summary

* Every element is a box: content + padding + border + margin
* `padding` is inside border, `margin` is outside
* `box-sizing: border-box` keeps layout predictable
* Borders can be styled for visual separation
* Use Developer Tools to inspect spacing and box model

---

## 🧪 Exercise

1. Create `spacing.html` and `spacing.css`
2. Add:

   * A card-style box (`div.card`)
   * Padding inside it, margin around it
   * Border with dashed or dotted style
   * Center the box horizontally
