# ✅ Chapter 8: Grid Layout System in CSS

---

## 🧱 What is CSS Grid?

**CSS Grid** is a powerful layout system for building **rows and columns** on a webpage.
Unlike Flexbox (which is 1D), Grid is **2D**, allowing control over both:

* Rows ↔ (horizontal)
* Columns ↕ (vertical)

---

## 🚀 Enabling Grid

To use Grid, you apply:

```css
.container {
  display: grid;
}
```

Then define **rows** and **columns** using `grid-template-rows` and `grid-template-columns`.

---

## 📐 Basic Example

```css
.container {
  display: grid;
  grid-template-columns: 200px 200px 200px;
}
```

Creates 3 columns of fixed width (200px each).

You can also use:

* `fr` units (fractional space)
* `auto`, `%`, or `repeat()`

```css
grid-template-columns: 1fr 2fr;
```

🧠 Means: 1 part width vs 2 parts

---

## ➕ Adding Gaps

```css
grid-gap: 20px;
/* or */
gap: 20px;
```

This adds spacing **between** rows and columns.

---

## 🔧 Grid Properties Summary

### On the Container:

| Property                | Purpose                        |
| ----------------------- | ------------------------------ |
| `display: grid`         | Enables Grid                   |
| `grid-template-columns` | Defines number/size of columns |
| `grid-template-rows`    | Defines row sizes              |
| `gap` / `grid-gap`      | Space between grid items       |
| `justify-items`         | Aligns items horizontally      |
| `align-items`           | Aligns items vertically        |

---

### On Grid Items:

| Property      | Purpose                           |
| ------------- | --------------------------------- |
| `grid-column` | Span/position item across columns |
| `grid-row`    | Span/position item across rows    |

---

## 💡 Hands-On Task: Simple Grid Layout

### File: `grid.html`

```html
<!DOCTYPE html>
<html>
<head>
  <title>Grid Layout</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>

  <div class="grid-container">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
    <div class="box">Box 5</div>
    <div class="box">Box 6</div>
  </div>

</body>
</html>
```

### File: `style.css`

```css
body {
  font-family: sans-serif;
  padding: 30px;
}

.grid-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

.box {
  background-color: #00bcd4;
  padding: 40px;
  color: white;
  text-align: center;
}
```

---

## 📌 Spanning Rows and Columns

### Example:

```css
.item1 {
  grid-column: span 2;
  grid-row: span 1;
}
```

This makes the item stretch across 2 columns.

---

## ✅ Summary

* `display: grid` enables Grid layout
* `grid-template-columns` and `rows` define structure
* `fr` units help with responsive spacing
* `gap` adds spacing between items
* Grid can place and stretch items in both directions
* Great for dashboards, cards, and layout-heavy pages

---

## 🧪 Exercise

1. Create `grid-layout.html` and `style.css`
2. Add:

   * A 3-column layout using `repeat(3, 1fr)`
   * 6 boxes labeled Box 1 to Box 6
   * One box should `span 2 columns`
   * Add gaps and color to make it look like a card layout
