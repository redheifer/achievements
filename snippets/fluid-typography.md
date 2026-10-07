# Fluid Typography with clamp()

Font size scales with the viewport but never goes below the minimum or above the maximum.

```css
:root {
  /* min 1rem, preferred 0.875rem + 0.5vw, max 1.25rem */
  font-size: clamp(1rem, 0.875rem + 0.5vw, 1.25rem);
}

h1 {
  font-size: clamp(2rem, 1.5rem + 2.5vw, 3.5rem);
  line-height: 1.1;
}
```
