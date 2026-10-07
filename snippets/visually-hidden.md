# Visually Hidden (Screen Reader Only)

Hide content visually while keeping it available to screen readers, e.g. labels for icon-only buttons.

```css
.visually-hidden {
  position: absolute !important;
  width: 1px !important;
  height: 1px !important;
  padding: 0 !important;
  margin: -1px !important;
  overflow: hidden !important;
  clip: rect(0, 0, 0, 0) !important;
  white-space: nowrap !important;
  border: 0 !important;
}
```

```html
<button type="button">
  <svg aria-hidden="true" focusable="false"><!-- icon --></svg>
  <span class="visually-hidden">Close menu</span>
</button>
```
