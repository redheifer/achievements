# Responsive Images with srcset and sizes

Let the browser pick the best image file for the viewport width and screen density.

```html
<img
  src="photo-800.jpg"
  srcset="photo-400.jpg 400w, photo-800.jpg 800w, photo-1600.jpg 1600w"
  sizes="(max-width: 600px) 100vw, 50vw"
  alt="Mountain lake at sunrise"
  width="800"
  height="533"
  loading="lazy"
  decoding="async"
>
```
