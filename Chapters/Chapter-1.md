# ✅ Chapter 1: Introduction to CSS

---

## 🎨 What is CSS?

**CSS** stands for **Cascading Style Sheets**.
It is the language used to **style** and **design** HTML web pages.

> ✨ If HTML is the **structure**, CSS is the **skin and appearance** of a website.

---

## 🔍 Why Use CSS?

Without CSS, all web pages look plain and similar.
CSS allows you to:

* Change **colors**, **fonts**, and **spacing**
* Control **layout and responsiveness**
* Add **animations**, **hover effects**, and **themes**
* Make the website look **beautiful and modern**

---

## 🤝 How CSS Works with HTML

CSS targets HTML **elements** and applies **style rules** to them.

### Example:

**HTML:**

```html
<p>Hello World!</p>
```

**CSS:**

```css
p {
  color: red;
  font-size: 20px;
}
```

🔎 Result: The paragraph will be **red** and have a **larger font**.

---

## 🔗 Three Ways to Add CSS

| Method       | Where it's Written           | Use Case                         |
| ------------ | ---------------------------- | -------------------------------- |
| Inline CSS   | Inside HTML tag              | For quick, one-time styling      |
| Internal CSS | Inside `<style>` in `<head>` | For small pages or single files  |
| External CSS | Linked as a `.css` file      | For large or multi-page projects |

---

### 1️⃣ Inline CSS

```html
<p style="color: green; font-size: 18px;">This is styled text.</p>
```

⚠️ Avoid inline CSS in real projects — hard to maintain.

---

### 2️⃣ Internal CSS

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    h1 {
      color: blue;
    }
    p {
      font-family: Arial;
    }
  </style>
</head>
<body>
  <h1>Welcome</h1>
  <p>This page is styled using internal CSS.</p>
</body>
</html>
```

---

### 3️⃣ External CSS

Create a separate file: `style.css`

```css
body {
  background-color: #f5f5f5;
}

h1 {
  color: #007bff;
}
```

Then link it in your HTML:

```html
<link rel="stylesheet" href="style.css" />
```

✅ Best for real websites — **separates structure from design**

---

## 💡 Hands-On Task: Your First Styled Page

### Step 1: Create `style.css`

```css
body {
  font-family: sans-serif;
  background-color: #fafafa;
}

h1 {
  color: #e91e63;
}

p {
  font-size: 18px;
  color: #333;
}
```

---

### Step 2: Create `style-demo.html`

```html
<!DOCTYPE html>
<html>
<head>
  <title>My First CSS Page</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>

  <h1>Hello CSS!</h1>
  <p>This page is styled using an external stylesheet.</p>

</body>
</html>
```

---

## ✅ Summary

* CSS is used to **style** HTML pages
* 3 methods: Inline, Internal, External
* External CSS is the **best practice**
* CSS uses **selectors** and **rules** to style elements
* You can change fonts, colors, sizes, layouts, and more

---

## 🧪 Exercise

1. Create a file `css-practice.html`
2. Link a new file called `main.css`
3. Style:

   * Background color of the body
   * A heading in any color
   * A paragraph with custom font and size
4. Open it with Live Server and test!
