# ✅ Chapter 4: Fonts and Text Styling in CSS

---

## 🔤 Changing Fonts with `font-family`

The `font-family` property lets you change the **typeface** of your text.

### Example:

```css
body {
  font-family: Arial, sans-serif;
}
```

📌 Always provide a **fallback** font in case the first one isn’t available.

---

## 🔠 Font Size: `font-size`

Controls the **size** of the text.

### Common Units:

| Unit  | Meaning                             |
| ----- | ----------------------------------- |
| `px`  | Pixels (fixed size)                 |
| `em`  | Relative to parent font size        |
| `rem` | Relative to root (`html`) font size |
| `%`   | Percentage                          |

### Example:

```css
h1 {
  font-size: 32px;
}

p {
  font-size: 1.2em;
}
```

---

## 🅰️ Font Style and Weight

* `font-style`: normal, italic, oblique
* `font-weight`: normal, bold, 100–900

```css
p {
  font-style: italic;
  font-weight: bold;
}
```

---

## 🔠 Text Transformation

Use `text-transform` to change **text case**:

```css
h2 {
  text-transform: uppercase;
}
```

| Value        | Effect                   |
| ------------ | ------------------------ |
| `uppercase`  | ALL CAPS                 |
| `lowercase`  | all lowercase            |
| `capitalize` | First Letter Capitalized |

---

## ↔️ Text Alignment: `text-align`

```css
p {
  text-align: center;
}
```

Options: `left`, `right`, `center`, `justify`

---

## 🔠 Text Decoration

Adds or removes lines (like underlining):

```css
a {
  text-decoration: none;
}
```

Options: `underline`, `overline`, `line-through`, `none`

---

## 🔡 Line Height and Letter Spacing

### Line Height:

```css
p {
  line-height: 1.6;
}
```

### Letter Spacing:

```css
h1 {
  letter-spacing: 2px;
}
```

---

## 🔗 Using Google Fonts

Go to [https://fonts.google.com](https://fonts.google.com)

1. Choose a font (e.g., **Poppins**)
2. Copy the `<link>` tag into your `<head>`:

```html
<link href="https://fonts.googleapis.com/css2?family=Poppins&display=swap" rel="stylesheet">
```

3. Use it in CSS:

```css
body {
  font-family: 'Poppins', sans-serif;
}
```

---

## 💡 Hands-On Task: Style an Article Page

### File: `text-style.html`

```html
<!DOCTYPE html>
<html>
<head>
  <title>Text Styling</title>
  <link href="https://fonts.googleapis.com/css2?family=Roboto&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="style.css" />
</head>
<body>

  <h1>CSS Text Styling</h1>
  <h2>Subheading Example</h2>
  <p>This is a paragraph showing various text styles in CSS.</p>

</body>
</html>
```

### File: `style.css`

```css
body {
  font-family: 'Roboto', sans-serif;
  line-height: 1.6;
  color: #333;
}

h1 {
  text-align: center;
  text-transform: uppercase;
  letter-spacing: 2px;
  color: darkblue;
}

h2 {
  font-style: italic;
  font-weight: 400;
  text-decoration: underline;
}

p {
  font-size: 18px;
  text-align: justify;
}
```

---

## ✅ Summary

* Use `font-family` to change typeface
* Control size with `font-size` (`px`, `em`, `rem`)
* Style text using:

  * `font-weight`, `font-style`, `text-transform`
  * `text-align`, `text-decoration`
  * `line-height`, `letter-spacing`
* You can import custom fonts from **Google Fonts**

---

## 🧪 Exercise

1. Create `typography.html` and `typography.css`
2. Add:

   * Headings and paragraphs
   * Different font families and sizes
   * Google Font (`Poppins` or any you like)
   * Spacing and transformation effects
