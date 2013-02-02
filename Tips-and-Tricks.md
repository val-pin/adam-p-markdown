Please add any tips and tricks that you come up with. For now it'll be a flat list and we'll add structure as needed.

Salutation Styling
==================

If you want to style the salutation of your email differently from the rest of the email, you can add a CSS rule that applies to the very first paragraph like so:

```css
.markdown-here-wrapper:first-of-type > p:first-of-type {
  color: red;
}
```

