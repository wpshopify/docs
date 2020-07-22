# Change Selected Button Colors

The below CSS will customize the variant button selected colors, as well as the variant badge within the cart. Replace #000 with the color of your choice.

```css
.wpshopify-variant-buttons button[data-is-variant-selected='true'] {
  background-color: #000;
  border-color: #000;
}

.wps-cart-lineitem-variant-title[class*='badge'] {
  background-color: #000;
}
```
