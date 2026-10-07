# Copy to Clipboard

Use the async Clipboard API (requires a secure context, i.e. HTTPS or localhost, and a user gesture).

```js
async function copyText(text) {
  try {
    await navigator.clipboard.writeText(text);
    return true;
  } catch (err) {
    console.error('Copy failed:', err);
    return false;
  }
}

// Usage
document.querySelector('#copy-btn').addEventListener('click', async (event) => {
  const ok = await copyText(document.querySelector('#code').textContent);
  event.currentTarget.textContent = ok ? 'Copied!' : 'Copy failed';
});
```
