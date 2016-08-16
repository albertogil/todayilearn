# CSS

## Masonry display with only CSS

Using column-count and column-gap, with break-inside on elements. [caniuse multicolumn](http://caniuse.com/#feat=multicolumn)

```css
.container {
  column-count: 3;
  column-gap: 0;
}
.card {
  break-inside: avoid;
  padding: 5px;
}
.card__content {
  padding: 10px;
  border-radius: 10px;
}
```

```html
<div class="container">
  <div class="card">
    <div class="card__content">
       ...
    </div>
  </div>
</div>
```

[Reference](https://medium.com/@_jh3y/how-to-pure-css-masonry-layouts-a8ede07ba31a#.jj1zboaj7)
