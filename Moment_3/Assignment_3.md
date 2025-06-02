
# 📌 Week 3 Assignment – JavaScript, DOM, Security & Accessibility

This assignment will test your ability to work with JavaScript on the client side, manipulate the DOM, handle events, and apply accessibility and security best practices.

---

## 🎯 Task: Build an Interactive and Accessible Comment Section

Create a fully functional comment component where users can submit messages. Comments should be added dynamically using JavaScript, without page reload. Your implementation must follow secure coding practices and be accessible.

---

## ✅ Requirements

### HTML
- A `<form>` with:
  - A `<textarea>` for user input
  - A `<button>` to submit the comment
- A container (e.g. `<div id="comments">`) to hold posted comments

### JavaScript
- Use `addEventListener` to handle form submission
- Validate that the textarea is not empty
- Use `textContent` to add comments to avoid XSS
- Reset the form after a comment is posted

### Accessibility
- Use a `<label>` for the textarea
- The comments section must use `aria-live="polite"`
- Ensure keyboard accessibility for all interactive elements
- Use semantic HTML elements

### Styling (optional but encouraged)
- Use CSS to make your form and comments visually appealing
- Indicate keyboard focus clearly (e.g., with `:focus` styles)

---

## 💡 Bonus (Optional)
- Add a character limit and display remaining characters
- Add a delete button to remove a comment
- Support keyboard shortcuts (e.g. Ctrl+Enter to submit)

---

## 📦 Submission Instructions

- Submit an `.html` file that includes both the HTML and JavaScript.
- Your file must work when opened in a browser without requiring a server.
- Name your file: `week3_comment_box.html`

---

## ✔️ Checklist Before Submitting

- [ ] Comments are added via JavaScript without reloading the page
- [ ] Input is validated and safely inserted using `textContent`
- [ ] The form has proper labels and is keyboard accessible
- [ ] aria-live is used for accessibility feedback
- [ ] Code is clean and well-commented

---

💬 **Reminder:** Think like a real-world developer. You're building something that real people will use — including those with screen readers or limited motor control.

Good luck!
