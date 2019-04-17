# [wps_filters]

Displays the filters component.

## 🎯 Example Usage

```js
// Drops the search results into a container with the id of #search-container
[wps_filters dropzone_payload="#dropzone-payload" dropzone_options="#dropzone-options"]

```

## ⚡️ Available Attributes

### `dropzone_payload` <span class="attr-type attr-type-required">(required)</span>

Specifies where the actual filter results should render. Takes any valid CSS selector.

```js
[wps_filters dropzone_payload="#dropzone-payload"]
```

### `dropzone_options` <span class="attr-type attr-type-required">(required)</span>

Specifies where the selectable filter options should render. Takes any valid CSS selector.

```js
[wps_filters dropzone_options="#dropzone-options"]
```

### `dropzone_sorting` <span class="attr-type attr-type-optional">(optional)</span>

Specifies where the sorting component should render. Takes any valid CSS selector. Omitting will hide sorting all together.

Default: `false`

```js
[wps_filters dropzone_sorting="#dropzone-sorting"]
```

### `dropzone_selections` <span class="attr-type attr-type-optional">(optional)</span>

Specifies where the selected user choices should render. Takes any valid CSS selector. Omitting will hide user selections all together.

Default: `false`

```js
[wps_filters dropzone_selections="#dropzone-selections"]
```

### `dropzone_pagination` <span class="attr-type attr-type-optional">(optional)</span>

Specifies where the pagination should render. Takes any valid CSS selector. Omitting will hide pagination all together.

Default: `false`

```js
[wps_filters dropzone_pagination="#dropzone-pagination"]
```

### `show_tags` <span class="attr-type attr-type-optional">(optional)</span>

Specifies whether to allow the user to filer by product tags. Setting to false will hide the ability to filter by tags.

Default: `true`

```js
[wps_filters show_tags="false"]
```

### `show_vendors` <span class="attr-type attr-type-optional">(optional)</span>

Specifies whether to allow the user to filer by product vendors. Setting to false will hide the ability to filter by vendors.

Default: `true`

```js
[wps_filters show_vendors="false"]
```

### `show_types` <span class="attr-type attr-type-optional">(optional)</span>

Specifies whether to allow the user to filer by product types. Setting to false will hide the ability to filter by types.

Default: `true`

```js
[wps_filters show_types="false"]
```

### `show_options_heading` <span class="attr-type attr-type-optional">(optional)</span>

Specifies whether to show the filter options heading.

Default: `true`

```js
[wps_filters show_options_heading="false"]
```

### `no_results_text` <span class="attr-type attr-type-optional">(optional)</span>

Specifies the text to use when no filter results are found.

Default: `No results found`

```js
[wps_filters no_results_text="Custom no results text with emojis 🚨"]
```
