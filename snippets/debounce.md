# Debounce

Run a function only after calls have stopped for `wait` ms. Useful for search inputs and resize handlers.

```js
function debounce(fn, wait = 300) {
  let timeoutId;
  return function (...args) {
    clearTimeout(timeoutId);
    timeoutId = setTimeout(() => fn.apply(this, args), wait);
  };
}

// Usage
const search = document.querySelector('#search');
search.addEventListener('input', debounce((event) => {
  console.log('Searching for', event.target.value);
}, 300));
```
