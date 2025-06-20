# ✅ Chapter 9: Responsive Design with Media Queries

---

## 📱 What is Responsive Design?

**Responsive design** means your website **adapts to any screen size**, whether it’s:

* Mobile 📱
* Tablet 📲
* Desktop 💻

The layout should adjust **without zooming or scrolling sideways**.

---

## 🧩 Role of HTML + CSS

* HTML should use **semantic**, clean structure
* CSS should use **media queries** to change layout, font sizes, visibility, etc.

---

## 🔍 Viewport Meta Tag (Must Have)

Add this in `<head>` of your HTML:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

It tells the browser to scale the page based on screen width.

---

## 🧪 What Are Media Queries?

Media queries allow you to apply CSS **only when certain conditions are true**, such as:

* screen width
* device type
* orientation

---

### Basic Syntax

```css
@media (condition) {
  /* CSS rules here */
}
```

### Example:

```css
/* Default (desktop) */
body {
  background-color: white;
}

/* For screens ≤ 768px (tablet/mobile) */
@media (max-width: 768px) {
  body {
    background-color: lightgray;
  }
}
```

---

## 🔢 Common Breakpoints

| Device       | Breakpoint (max-width) |
| ------------ | ---------------------- |
| Mobile       | 480px                  |
| Tablet       | 768px                  |
| Small Laptop | 1024px                 |
| Desktop      | 1200px and above       |

---

## 📐 Real Example: Responsive Layout

### File: `responsive.html`

```html
<!DOCTYPE html>
<html>
<head>
  <title>Responsive Demo</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <link rel="stylesheet" href="style.css" />
</head>
<body>

  <h1>Welcome</h1>
  <p>This page changes based on your screen size.</p>

  <div class="container">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
  </div>

</body>
</html>
```

### File: `style.css`

```css
body {
  font-family: sans-serif;
  text-align: center;
  padding: 20px;
}

.container {
  display: flex;
  gap: 20px;
  justify-content: center;
}

.box {
  background-color: #4caf50;
  color: white;
  padding: 20px;
  flex: 1;
}

/* For smaller screens */
@media (max-width: 768px) {
  .container {
    flex-direction: column;
  }
}
```

📱 Now open this on mobile or resize your browser — boxes stack vertically!

---

## 🧠 Other Use Cases

* Change font size for readability
* Hide/show elements
* Adjust layout or spacing
* Stack columns into rows (grid to block)

---

## ✅ Summary

* Use `<meta name="viewport">` to scale layout
* Use `@media` to write **conditional CSS**
* Target devices by **max-width** or **min-width**
* Make layouts **flexible** using Flexbox/Grid + media queries
* Always test on multiple screen sizes

---

## 🧪 Exercise

1. Create `media-query.html` and `style.css`
2. Add:

   * 3 cards in a Flexbox row (desktop)
   * Use `@media` to make them stack in column (mobile)
   * Change `font-size` on small screens
