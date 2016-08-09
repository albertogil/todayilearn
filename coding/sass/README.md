# SASS

## Extend %placeholder selector

Instead of using regular @extend, use %placeholders so that the base css is not rendered.

```css
%error {
    color: red;
    
    &:hover {
        text-decoration: underline;
    }
}

.sign-up__name--error {
    @extend %error;
}
```
[Reference source](http://thesassway.com/intermediate/understanding-placeholder-selectors)

