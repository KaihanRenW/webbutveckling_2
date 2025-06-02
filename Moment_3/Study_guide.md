
# 📘 Week 3 – JavaScript, DOM, Security & Accessibility

This week, we transition into client-side development. You'll learn to use JavaScript and the DOM to make pages interactive, understand real-world security risks (like XSS and CSRF), and learn how to build websites that everyone — including people with disabilities — can use.

---

## ✅ What You'll Be Able to Do

- Select and modify HTML elements using JavaScript
- React to user input with events and handlers
- Understand how client-side vulnerabilities work and how to protect against them
- Apply accessibility best practices (contrast, navigation, alternative content)

---

## 2. The DOM – Document Object Model

The DOM is a **live representation of the HTML document** as a structured tree. Every element becomes a node in this tree. JavaScript interacts with this tree to **read or modify content**.

### 2.1 Selecting Elements

To interact with an element in HTML, we first need to reference it:

```js
const button = document.getElementById("myBtn");
```

- `getElementById()` — fast and specific, finds an element by `id`.
- `querySelector()` — flexible, uses CSS selector syntax:
  ```js
  const firstItem = document.querySelector("ul li");
  ```

- `querySelectorAll()` — returns a static list of all matching elements:
  ```js
  const items = document.querySelectorAll("ul li");
  items.forEach(item => console.log(item.textContent));
  ```

### 2.2 Editing Content and Attributes

Once you've selected an element, you can change it.

```js
const header = document.querySelector("h1");
header.textContent = "Updated Title";
```

- `textContent` — sets plain text safely.
- `innerHTML` — injects raw HTML (avoid for security).
- `classList.add()` — adds a CSS class.
- `setAttribute()` — sets attributes like `href`, `src`, etc.

```js
header.setAttribute("role", "banner");
```

### 2.3 Creating, Inserting, and Removing Elements

```js
const newPara = document.createElement("p");
newPara.textContent = "This paragraph was added with JavaScript!";
document.body.appendChild(newPara);
```

Other methods:

- `appendChild()` – add as last child
- `insertBefore()` – insert before a specific node
- `removeChild()` – remove an element
- `replaceChild()` – replace an existing element

---

## 3. Events & Interactivity

Websites react to user actions like clicks, typing, scrolling, etc.

### 3.1 Adding Event Listeners

```js
const btn = document.getElementById("clickMe");

btn.addEventListener("click", () => {
  alert("Button was clicked!");
});
```

Event types include:

- `click`
- `submit`
- `keydown`, `keyup`
- `change`, `input`
- `mouseenter`, `mouseleave`

### 3.2 The Event Object

Each event has a built-in object passed to your function.

```js
element.addEventListener("click", (event) => {
  console.log("You clicked:", event.target);
});
```

Properties:

- `event.target` — the element that was interacted with
- `event.currentTarget` — the element the listener was attached to
- `event.preventDefault()` — stops default behavior (e.g. form submission)
- `event.stopPropagation()` — stops event bubbling

### 3.3 Bubbling and Delegation

Events "bubble" from the innermost target element up the DOM tree.

#### Why it's useful:
You can attach a listener to a parent element and react when children are clicked.

```js
document.querySelector("ul").addEventListener("click", (e) => {
  if (e.target.tagName === "LI") {
    e.target.classList.toggle("selected");
  }
});
```

This is called **event delegation** and is useful for dynamic lists.

---

## 4. Web Security – XSS & CSRF

Security is essential when your code interacts with users and external data.

### 4.1 XSS – Cross-Site Scripting

**XSS** happens when attackers inject malicious scripts into your page. This can happen if you use `innerHTML` carelessly:

```js
element.innerHTML = userInput; // ❌ Dangerous
```

A malicious user could input:
```html
<script>alert('Hacked!')</script>
```

**Safe alternative:**

```js
element.textContent = userInput; // ✅ Safe
```

**Best practices:**
- Use `textContent`, not `innerHTML`
- Escape output server-side as well
- Validate/clean all user input

### 4.2 CSRF – Cross-Site Request Forgery

**CSRF** tricks a logged-in user into performing unintended actions on another website.

#### Example:
You're logged into `mybank.com`. A malicious website silently submits a form to `mybank.com/transfer`.

#### Protection:
- Use **CSRF tokens** — random keys tied to session
- Use **SameSite cookies** (`Strict` or `Lax`) to block cross-origin requests

---

## 5. Accessibility (WCAG)

Web content should be usable by everyone, including people with disabilities. WCAG = Web Content Accessibility Guidelines.

### 5.1 Semantic HTML & ARIA

Use proper HTML elements for what they are:

| Purpose | Semantic Element |
|--------|------------------|
| Button | `<button>`       |
| Navigation | `<nav>`     |
| Section of page | `<section>` |
| Form | `<form>` |

#### ARIA attributes (used sparingly):
- `aria-label="Close menu"`
- `aria-hidden="true"` to hide from screen readers
- `aria-live="polite"` for updating content

### 5.2 Color & Contrast

Low contrast makes text unreadable for many users (e.g. colorblindness or vision impairment).

- **Minimum contrast**: 4.5:1 for normal text
- Use tools like [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/)

```css
/* Good contrast */
body {
  background-color: #ffffff;
  color: #111111;
}
```

Don't rely on color alone for meaning — use icons, text, patterns.

### 5.3 Keyboard Navigation

Many users rely on keyboards only.

- Make sure all interactive elements are focusable:
  - Links, buttons, inputs are focusable by default
  - Use `tabindex="0"` on custom focusable elements

```html
<div tabindex="0">Custom focusable box</div>
```

- Style focus state clearly:

```css
button:focus {
  outline: 2px dashed #007acc;
}
```

- Provide “skip to content” links:

```html
<a href="#main" class="skip-link">Skip to main content</a>
```

### 5.4 Media & Captions

Video and audio should have:

- **Captions** for spoken content
- **Transcripts** for audio-only
- `aria-label` or descriptive labels

Example with video captions:

```html
<video controls>
  <source src="demo.mp4" type="video/mp4">
  <track src="captions.vtt" kind="captions" srclang="en" label="English">
</video>
```

---

## 6. Bonus Tools & Resources

Improve your development workflow and understanding:

### Browser DevTools

- Inspect DOM
- See event listeners
- Debug JavaScript line-by-line
- Use accessibility tab (in Firefox/Chrome)

### Accessibility Testing Tools

- [axe DevTools extension](https://www.deque.com/axe/)
- [Lighthouse in Chrome DevTools](https://developer.chrome.com/docs/lighthouse/overview/)

### Learn More

- [JavaScript on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [Web.dev on accessibility](https://web.dev/accessible/)
- [WCAG Quick Reference](https://www.w3.org/WAI/WCAG21/quickref/)

---

✅ **Next Step:** Practice building a secure and accessible comment box using the techniques above.
