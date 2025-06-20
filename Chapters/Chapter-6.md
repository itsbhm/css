# ✅ Chapter 6: Display, Positioning, and Z-Index in CSS

---

## 📺 `display` Property

Controls **how** an element is rendered in the layout.

### Common Values:

| Value          | Description                               |
| -------------- | ----------------------------------------- |
| `block`        | Starts on a new line and takes full width |
| `inline`       | Stays in line with other elements         |
| `inline-block` | Like inline, but allows width/height      |
| `none`         | Completely hides the element              |

### Example:

```css
span {
  display: block;
}
```

---

### Demo:

```html
<p>This is <span style="display: inline">inline</span> and <span style="display: block">block</span></p>
```

---

## 📍 `position` Property

Controls **exact placement** of an element on the page.

### Position Types:

| Type       | Description                                                 |
| ---------- | ----------------------------------------------------------- |
| `static`   | Default; follows normal flow                                |
| `relative` | Moves **relative to its original position**                 |
| `absolute` | Moves **relative to nearest positioned ancestor**           |
| `fixed`    | Stays in place **even when scrolling** (like sticky navbar) |
| `sticky`   | Scrolls normally until it “sticks” at a certain position    |

---

### Example:

```css
.box {
  position: relative;
  top: 20px;
  left: 30px;
}
```

📌 Works only with `relative`, `absolute`, `fixed`, or `sticky` (not static)

---

## ⚙️ `top`, `right`, `bottom`, `left`

Used with positioning to move elements.

```css
.banner {
  position: absolute;
  top: 0;
  left: 0;
}
```

---

## 🧱 `z-index` (Layering)

Determines **which element appears on top** when they overlap.

Higher `z-index` = higher in the stack.

```css
.box1 {
  position: absolute;
  z-index: 2;
}

.box2 {
  position: absolute;
  z-index: 1;
}
```

---

## 💡 Hands-On: Floating Box and Sticky Header

### File: `positioning.html`

```html
<!DOCTYPE html>
<html>
<head>
  <title>Positioning Demo</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>

  <header class="sticky-header">
    <h2>Sticky Header</h2>
  </header>

  <div class="box absolute-box">Absolute Box</div>
  <div class="content">
    <p>This content scrolls normally.</p>
    <p style="height: 1000px;"></p>
  </div>

</body>
</html>
```

### File: `style.css`

```css
body {
  margin: 0;
  font-family: sans-serif;
}

.sticky-header {
  position: sticky;
  top: 0;
  background: darkblue;
  color: white;
  padding: 10px;
  z-index: 10;
}

.absolute-box {
  position: absolute;
  top: 100px;
  left: 30px;
  background-color: tomato;
  color: white;
  padding: 20px;
  z-index: 5;
}

.content {
  padding: 20px;
}
```

---

## ✅ Summary

* `display` controls layout type: `block`, `inline`, `none`, etc.
* `position` allows precise placement:

  * `relative` shifts from normal spot
  * `absolute` anchors to a positioned parent
  * `fixed` pins to screen
  * `sticky` sticks after scrolling
* `z-index` controls stacking order
* Use `top`, `left`, `right`, `bottom` to move positioned elements

---

## 🧪 Exercise

1. Create `positioning-demo.html` and `style.css`
2. Add:

   * A sticky `<header>`
   * An `absolute` box that overlaps another
   * A `z-index` demo where one box overlaps another
3. Use browser DevTools to move and inspect layers
