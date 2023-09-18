# jawal-js

## Instalation

Include the library in your HTML file:

```html
<script src="https://cdn.yastack.app/v0.0.1/jawal-js.min.js"></script>
```

## Usage

To initialize the library, you need to call the `getJawal` method with your API key:

```js
const app = document.getElementById("app");
const jawal = await getJawal("JS_API_KEY", app);
```

The `getJawal` method returns a promise that resolves to a `Jawal` object.

The `Jawal` object has the following methods:

### `loadSessionByExternalId`

```js
jawal.loadSessionByExternalId("session_external_id");
```

this method fetches the session data from the API and loads the "Session details" view in the widget.

!!! note
    The `session_external_id` is the ID that you pass to the `jawal.startSession` method. if there's more than one session with the same external ID, the latest one will be loaded.
