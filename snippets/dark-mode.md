# Dark Mode with Custom Properties

Define colors once as custom properties and swap them when the OS prefers a dark color scheme.

```css
:root {
  color-scheme: light dark;
  --bg: #ffffff;
  --text: #1a1a1a;
  --accent: #0b62d6;
}

@media (prefers-color-scheme: dark) {
  :root {
    --bg: #121212;
    --text: #eaeaea;
    --accent: #6ea8ff;
  }
}

body {
  background: var(--bg);
  color: var(--text);
}

a {
  color: var(--accent);
}
```
