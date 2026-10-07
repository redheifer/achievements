# Throttle

Run a function at most once every `limit` ms, with a trailing call so the final event is not lost. Useful for scroll and pointermove handlers.

```js
function throttle(fn, limit = 200) {
  let lastRun = 0;
  let timeoutId;
  return function (...args) {
    const now = Date.now();
    const remaining = limit - (now - lastRun);
    clearTimeout(timeoutId);
    if (remaining <= 0) {
      lastRun = now;
      fn.apply(this, args);
    } else {
      timeoutId = setTimeout(() => {
        lastRun = Date.now();
        fn.apply(this, args);
      }, remaining);
    }
  };
}

// Usage
window.addEventListener('scroll', throttle(() => {
  console.log('scrollY:', window.scrollY);
}, 200));
```
