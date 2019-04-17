# [wps_search]

Displays the search component.

## 🎯 Example Usage

```js
// Drops the search results into a container with the id of #search-container
[wps_search dropzone="#search-container"]

```

## ⚡️ Available Attributes

### `dropzone` <span class="attr-type attr-type-required">(required)</span>

Specifies where the search results should render. Takes any valid CSS selector.

Default: `false`

```js
[wps_search dropzone="#search-container"]
```

### `no_results_text` <span class="attr-type attr-type-optional">(optional)</span>

Specifies the text to use when no results are found.

Default: `No results found`

```js
[wps_search no_results_text="Custom no results text with emojis 🚨"]
```
