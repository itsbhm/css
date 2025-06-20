# ✅ Chapter 3: Colors and Backgrounds in CSS

---

## 🎨 CSS Colors

You can set color using different **formats**:

| Format | Example             | Notes                           |
| ------ | ------------------- | ------------------------------- |
| Named  | `red`, `blue`       | Easy to remember, limited range |
| HEX    | `#ff0000`           | 6-digit code, popular for web   |
| RGB    | `rgb(255, 0, 0)`    | Red, Green, Blue (0–255)        |
| RGBA   | `rgba(0,0,0,0.5)`   | RGB + Alpha (opacity)           |
| HSL    | `hsl(0, 100%, 50%)` | Hue, Saturation, Lightness      |

---

### Example:

```css
body {
  background-color: #f5f5f5;
  color: rgb(50, 50, 50);
}
```

🎯 Tip: Use **HEX** or **RGBA** for design consistency.

---

## 🧱 CSS Background Properties

CSS allows you to control background colors, images, positions, and repetition.

---

### 1️⃣ Background Color

```css
body {
  background-color: lightblue;
}
```

---

### 2️⃣ Background Image

```css
body {
  background-image: url("images/bg.jpg");
}
```

⚠️ Make sure the path is correct relative to your CSS file.

---

### 3️⃣ Background Repeat

| Value       | Description                         |
| ----------- | ----------------------------------- |
| `repeat`    | Default: repeats in both directions |
| `no-repeat` | Shows only once                     |
| `repeat-x`  | Repeats horizontally                |
| `repeat-y`  | Repeats vertically                  |

```css
body {
  background-repeat: no-repeat;
}
```

---

### 4️⃣ Background Size

```css
background-size: cover;
```

| Value     | Description               |
| --------- | ------------------------- |
| `cover`   | Stretches to fill screen  |
| `contain` | Scales to show full image |
| `auto`    | Keeps original size       |

---

### 5️⃣ Background Position

Control where image appears.

```css
background-position: center center;
```

Other examples: `top right`, `bottom left`, `50% 50%`

---

### 🎯 Shortcut: `background` shorthand

```css
body {
  background: url("bg.jpg") no-repeat center center / cover;
}
```

---

## 💡 Hands-On Task: Color and Background Demo

### File: `background-demo.html`

```html
<!DOCTYPE html>
<html>
<head>
  <title>Background Styling</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>

  <h1>Welcome</h1>
  <p>This page has colors and background image.</p>

</body>
</html>
```

### File: `style.css`

```css
body {
  background-image: url("images/bg.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
  color: white;
  font-family: Arial;
}

h1 {
  color: #ffcc00;
}
```

🧪 Use a high-contrast background image for best effect.

---

## ✅ Summary

* Colors can be set using `color` and `background-color`
* Color formats: Named, HEX, RGB, RGBA, HSL
* `background-image` loads a visual behind content
* Control behavior using:

  * `background-repeat`
  * `background-position`
  * `background-size`
* Combine with shorthand `background` for cleaner code

---

## 🧪 Exercise

1. Create a file `color-bg.html` and `style.css`
2. Add:

   * Background color or image for `<body>`
   * Set text color of heading and paragraph
   * Try `rgba()` to add transparency
   * Try positioning and sizing for background image
