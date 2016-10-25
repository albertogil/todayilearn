# CSS

## Animations

- Things that we can control, Timing (duration) and spacing (easing)
 - Imply laws of physics
 - Establish mood, emotion, reaction
 
### Tips:
 - Similar objects animate in similar ways
 - Entrance informs exist, persistence for user
 - Match Velocities, the one that can have more impact

- Use cubic-bezier() for more control in the ease, [cubic-bezier]()

### References:
- The more good animation you see, the moregood taste you can have
 - [artofthetitle.com](www.artofthetitle.com)
 - iOS animations [capptivate.co](capptivate.co)
 - Different variations [uyi.io](uyi.io)
 - [Animation principles reference](www.the12principles.tumblr.com)

## Masonry display with only CSS

Are not perfect and not the best approach, but can work for only CSS scenarios.

### Flex-box

```css
.container {
  display: flex;
  align-items: flex-start;
  align-content: flex-start;
  justify-content: flex-start;
  flex-direction: row;
  flex-wrap: wrap;
  align-content: flex-end;
}

.card {
  width: 33%;
}
```

### Column-count

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
