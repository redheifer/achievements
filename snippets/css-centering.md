# Centering with Grid and Flexbox

Center a child both horizontally and vertically. Grid needs one line; flexbox needs two.

```css
/* Grid */
.center-grid {
  display: grid;
  place-items: center;
  min-height: 100vh;
}

/* Flexbox */
.center-flex {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}
```
