
# 📘 Layout, Typography & Frameworks

This week focuses on improving your design and layout skills using **CSS layout systems**, selecting appropriate **typography**, and getting started with **design libraries** or frameworks like Bootstrap. We also explore principles of interface design and how to apply them in your own projects.

---

## ✅ Learning Goals

By the end of this week, you will be able to:

- Understand and apply CSS layout techniques (Flexbox & Grid)
- Choose and apply suitable fonts and color schemes
- Use design frameworks like Bootstrap to streamline styling
- Apply UI design principles such as alignment, balance, contrast, and spacing
- Validate and organize your code for readability and maintainability

---

## 1. CSS Layout Systems

### 1.1 Flexbox

A one-dimensional layout system for aligning items in a row or column.

```css
.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```

Useful properties:
- `justify-content`: main-axis alignment
- `align-items`: cross-axis alignment
- `flex-grow`, `flex-shrink`, `flex-basis`

### 1.2 CSS Grid

A two-dimensional system ideal for page layouts.

```css
.container {
  display: grid;
  grid-template-columns: 1fr 2fr;
  grid-gap: 1rem;
}
```

Grid gives you control over both rows and columns at the same time.

---

## 2. Typography in Web Design

Typography affects readability, accessibility, and tone.

### 2.1 Font Selection

- Use system fonts for performance (e.g., Arial, Georgia, Verdana)
- Use web fonts like Google Fonts:

```html
<link href="https://fonts.googleapis.com/css2?family=Roboto&display=swap" rel="stylesheet">
```

```css
body {
  font-family: 'Roboto', sans-serif;
}
```

### 2.2 Line Height & Spacing

```css
body {
  line-height: 1.6;
  letter-spacing: 0.5px;
}
```

- Use relative units (`em`, `rem`) for scalability

---

## 3. UI & Design Principles

### 3.1 Layout & Alignment

- Use grid or flex to create structured, balanced layouts
- Align text and buttons consistently

### 3.2 Color Schemes

- Choose a palette with contrast and visual harmony
- Try tools like [Coolors](https://coolors.co/) or [Adobe Color](https://color.adobe.com/)

### 3.3 Spacing & Grouping

- Use consistent padding/margins to group related items
- Use white space to avoid clutter

---

## 4. Frameworks: Bootstrap Basics

### 4.1 What is Bootstrap?

A popular front-end CSS framework that includes ready-made components like:

- Grids
- Buttons
- Forms
- Cards
- Navigation bars

### 4.2 Using Bootstrap

Add the Bootstrap CDN to your HTML:

```html
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
```

Example of a responsive button:

```html
<button class="btn btn-primary">Click me</button>
```

Example of a grid layout:

```html
<div class="container">
  <div class="row">
    <div class="col-md-6">Left</div>
    <div class="col-md-6">Right</div>
  </div>
</div>
```

---

## 5. Code Quality: Validation & Organization

### 5.1 HTML & CSS Validation

- [W3C HTML Validator](https://validator.w3.org/)
- [W3C CSS Validator](https://jigsaw.w3.org/css-validator/)

### 5.2 Code Style Best Practices

- Consistent indentation (2 or 4 spaces)
- Descriptive class names
- Comment complex logic

---

## 🛠️ Practical Exercise

### 💡 Task: Create a Responsive Webpage with Layout and Bootstrap

1. Create a responsive page that includes:
   - A grid-based layout using Flexbox or Bootstrap
   - At least two fonts (one for headings, one for body text)
   - A navbar and one or more content cards
2. Use proper spacing, visual hierarchy, and contrast.
3. Validate your HTML and CSS before submitting.

```html
<!-- Sample Bootstrap Card -->
<div class="card">
  <div class="card-body">
    <h5 class="card-title">Responsive Design</h5>
    <p class="card-text">Using Bootstrap makes layout easier.</p>
  </div>
</div>
```
