# ✅ Chapter 7: Flexbox Layout System in CSS

---

## 🔄 What is Flexbox?

**Flexbox** (Flexible Box) is a layout model in CSS used to **arrange items in a row or column**, even when the size of items is unknown or dynamic.

It solves common layout problems like:

* Centering items
* Equal spacing
* Making flexible grids
* Aligning content both horizontally and vertically

---

## 📦 Flexbox Basics

To use Flexbox:

1. Set the **container** to `display: flex`
2. Then apply flex properties to the container or its children

```css
.container {
  display: flex;
}
```

---

## 🔠 Main Axis vs Cross Axis

* **Main Axis**: Defined by `flex-direction`
* **Cross Axis**: Perpendicular to main axis

---

## 🔧 Container Properties

### 1️⃣ `display: flex`

Activates Flexbox on a container

```css
.container {
  display: flex;
}
```

---

### 2️⃣ `flex-direction`

Sets the main axis: `row` (default), `row-reverse`, `column`, `column-reverse`

```css
.container {
  flex-direction: row;
}
```

---

### 3️⃣ `justify-content`

Aligns items **on main axis** (horizontally by default)

| Value           | Description                  |
| --------------- | ---------------------------- |
| `flex-start`    | Items at start (default)     |
| `flex-end`      | Items at end                 |
| `center`        | Center items                 |
| `space-between` | Equal spacing between items  |
| `space-around`  | Equal space around each item |

```css
.container {
  justify-content: space-between;
}
```

---

### 4️⃣ `align-items`

Aligns items **on cross axis** (vertical by default)

| Value        | Description              |
| ------------ | ------------------------ |
| `stretch`    | Default, fills container |
| `center`     | Centered vertically      |
| `flex-start` | Top                      |
| `flex-end`   | Bottom                   |

---

### 5️⃣ `gap`

Adds space **between flex items** without using margin

```css
.container {
  display: flex;
  gap: 20px;
}
```

---

## 🔧 Item Properties

### 1️⃣ `flex-grow`

Defines how much an item **can grow**

```css
.item {
  flex-grow: 1;
}
```

---

### 2️⃣ `flex-shrink`

Defines how much an item **can shrink**

---

### 3️⃣ `flex-basis`

Initial size before growing/shrinking

---

### 4️⃣ Shorthand: `flex: grow shrink basis`

```css
.item {
  flex: 1 1 200px;
}
```

---

## 💡 Hands-On: Flexbox Card Layout

### File: `flexbox.html`

```html
<!DOCTYPE html>
<html>
<head>
  <title>Flexbox Demo</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>

  <div class="container">
    <div class="card">Card 1</div>
    <div class="card">Card 2</div>
    <div class="card">Card 3</div>
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

.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 20px;
}

.card {
  background-color: lightblue;
  padding: 20px;
  flex: 1;
  text-align: center;
}
```

🧪 Try resizing the browser window — items stay aligned and spaced!

---

## ✅ Summary

* `display: flex` activates Flexbox
* Use `justify-content` for main axis alignment
* Use `align-items` for cross axis alignment
* Use `flex` property on items to grow or shrink
* Add spacing using `gap`
* Flexbox makes layout easier than floats or inline-block

---

## 🧪 Exercise

1. Create `flex-layout.html` and `style.css`
2. Add:

   * A container with 3 boxes inside
   * Align them with `space-around`
   * Center vertically using `align-items: center`
   * Give each box equal width using `flex: 1`
