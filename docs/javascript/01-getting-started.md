# jawal-js

## Instalation

If you're using a bundler like webpack or rollup, you can install the library from npm:

```bash
npm install jawal-js
```

```js
import { getJawal } from "jawal-js";
```

If you're not using a bundler, you can include the library from a CDN:

```html
<script src="https://cdn.yastack.app/v0.0.3/jawal-js.min.js"></script>
```

And then you can access the library from the `window` object:

```js
const { getJawal } = window.Jawal;
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
