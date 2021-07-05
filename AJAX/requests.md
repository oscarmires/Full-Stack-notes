# Requests

## XHR - XML HTTP Request
- uses aynchronous JavaScript and XML (AJAX)
- not restricted to XML (can use other formats)
- API is XMLHttpRequest (XHR)

```js
// AJAX GET boilerplate
const xhr = new XMLHttpRequest();
const url = 'https://api-to-call.com/endpoint';

xhr.responseType = 'json';
xhr.onreadystatechange = () => {
  if (xhr.readyState === XMLHttpRequest.DONE) {
    return xhr.response;
  }
}

xhr.open('GET', url);
xhr.send();
```
\* different way to do this at https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Fetching_data with `request.onload`

```js
// AJAX POST boilerplate
const xhr = new XMLHttpRequest();
const url = 'https://api-to-call.com/endpoint';
const data = JSON.stringify({id: '200'});

xhr.responseType = 'json';
xhr.onreadystatechange = () => {
  if (xhr.readyState === XMLHttpRequest.DONE) {
    return xhr.response;
  }
}

xhr.open('POST', url);
xhr.send(data);
```

## `fetch` requests
- uses promises
- uses `Request` and `Response` objects

```js
// fetch GET boilerplate

fetch('https://api-to-call.com/endpoint')
.then(
  response => {
    if (response.ok) {
      return response.json();
    }
    throw new Error('Request failed!');
  },
  networkError => {
    console.log(networkError.message);
  }
)
.then(
  jsonResponse => {
    return jsonResponse;
  }
);
```

\* `Response` object's `.json()` returns a promise.

```js
// fetch POST boilerplate
fetch('https://api-to-call.com/endpoint', {
  method: 'POST',
  body: JSON.stringify({id: '200'})
})
.then(
  response => {
    if (response.ok) {
      return response.json();
    }
    throw new Error('Request failed!');
  },
  networkError => {
    console.log(networkError.message);
  }
)
.then(
  jsonResponse => {
    return jsonResponse
  }
);
```

## `async`/`await` requests with `fetch()`
Similar to `.then()`
```js
// async await GET boilerplate
const getData = async () => {
  try {
    const response = await fetch('https://api-to-call.com/endpoint');
    if (response.ok) {
      const jsonResponse = await response.json();
      return jsonResponse;
    }
    throw new Error('Request failed!');
  } catch(error) {
    console.log(error)
  }
}
```

```js
// async await POST boilerplate
const getData = async () => {
  try {
    const response = await fetch('https://api-to-call.com/endpoint', {
      method: 'POST',
      body: JSON.stringify({id: 200})
    });
    if (response.ok) {
      const jsonResponse = await response.json();
      return jsonResponse;
    }
    throw new Error('Request failed!');
  } catch (error) {
    console.log(error);
  }
}
```
