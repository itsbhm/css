# ✅ Chapter 10: CSS Transitions and Effects

---

## ✨ What are CSS Transitions?

**Transitions** allow you to smoothly change a CSS property **from one state to another** — like when you hover over a button and it changes color or size with animation.

---

## 🔄 Basic Transition Syntax

```css
selector {
  transition: property duration timing-function delay;
}
```

### Example:

```css
button {
  background-color: blue;
  transition: background-color 0.5s ease;
}

button:hover {
  background-color: green;
}
```

🎯 When you hover over the button, the background color changes smoothly in 0.5 seconds.

---

## 🔧 Common Transition Properties

| Property                     | Description                          |
| ---------------------------- | ------------------------------------ |
| `transition-property`        | Which property to animate            |
| `transition-duration`        | How long it takes                    |
| `transition-timing-function` | Speed curve (`ease`, `linear`, etc.) |
| `transition-delay`           | Wait time before animation           |

---

## ⏱ Shorthand Syntax

```css
transition: all 0.3s ease;
```

* `all`: apply to all changeable properties
* `0.3s`: animation duration
* `ease`: transition speed curve

---

## 🎯 Hover Effects

You can combine `:hover` and `transition` for smooth UI changes.

```css
.card {
  background: white;
  transition: transform 0.3s ease;
}

.card:hover {
  transform: scale(1.05);
}
```

📌 This zooms in the card on hover smoothly.

---

## 🔁 Transform Property

Transforms allow rotation, scaling, and moving elements.

| Function       | Example             | Description    |
| -------------- | ------------------- | -------------- |
| `scale()`      | `scale(1.1)`        | Zoom in/out    |
| `rotate()`     | `rotate(45deg)`     | Rotate element |
| `translateX()` | `translateX(20px)`  | Move on X-axis |
| `translateY()` | `translateY(-10px)` | Move on Y-axis |

---

## 🧩 Combining Transitions & Transforms

```css
.image {
  transform: scale(1);
  transition: transform 0.4s ease-in-out;
}

.image:hover {
  transform: scale(1.2) rotate(5deg);
}
```

---

## ✨ Bonus: Keyframe Animations (Intro)

```css
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

.box {
  animation: fadeIn 1s ease-in;
}
```

📌 You can use this to animate something when the page loads.

---

## 💡 Hands-On Project: Animate Button

### File: `effects.html`

```html
<!DOCTYPE html>
<html>
<head>
  <title>Transitions Demo</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>

  <h1>Hover Animation</h1>
  <button class="btn">Hover Me</button>

</body>
</html>
```

### File: `style.css`

```css
body {
  font-family: sans-serif;
  text-align: center;
  padding: 50px;
}

.btn {
  background-color: #2196f3;
  color: white;
  padding: 15px 30px;
  border: none;
  font-size: 16px;
  cursor: pointer;
  transition: background-color 0.4s, transform 0.3s;
}

.btn:hover {
  background-color: #0b7dda;
  transform: scale(1.1);
}
```

---

## ✅ Summary

* Use `transition` to animate changes smoothly
* Use `:hover` for interactivity
* `transform` allows scaling, moving, rotating
* Combine them for modern, clean UI effects
* Use `@keyframes` for more advanced animations

---

## 🧪 Exercise

1. Create `transition-demo.html` and `style.css`
2. Add:

   * A card or image that scales on hover
   * A button that changes background and grows slightly
   * Try using `rotate()` or `translateX()` for fun effects
