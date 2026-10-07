# Sticky Footer

Keep the footer at the bottom of the viewport when content is short, and below content when it is long.

```css
body {
  min-height: 100vh; /* fallback */
  min-height: 100dvh;
  display: grid;
  grid-template-rows: auto 1fr auto;
  margin: 0;
}
```

```html
<body>
  <header>…</header>
  <main>…</main>
  <footer>…</footer>
</body>
```
