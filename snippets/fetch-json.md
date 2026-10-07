# fetch with async/await and Error Handling

`fetch` only rejects on network errors, so check `response.ok` to catch HTTP errors too. Includes a timeout via `AbortSignal.timeout`.

```js
async function getJSON(url, options = {}) {
  const response = await fetch(url, {
    signal: AbortSignal.timeout(10_000),
    ...options,
    headers: { Accept: 'application/json', ...options.headers },
  });

  if (!response.ok) {
    throw new Error(`HTTP ${response.status} ${response.statusText} for ${url}`);
  }
  return response.json();
}

// Usage
try {
  const user = await getJSON('https://api.github.com/users/octocat');
  console.log(user.name);
} catch (err) {
  console.error('Request failed:', err.message);
}
```
