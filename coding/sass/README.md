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

## Using BEMify to create BEM structure

Simple mixins that can help make an easy BEM structure and avoid typos. (Used on Walton project)

[Mixin source](https://gtihub.com/franzheidl/bemify)

### Sample

```css
@include block('login') {
    display: block;
    margin-bottom: 15px;

    @include element('title') {
        margin-bottom: 15px;
        font-size: 14px;
        text-transform: uppercase;

        @include bp-medium {
            margin-bottom: 25px;
        }
    }

    @include element('email') {
        color: #333;
        font-size: 10px;
        letter-spacing: 1.5px;

        @include modifier('invalid') {
            color: red;
        }

        @include bp-medium {
            width: 200px
            font-size: 12px;
        }
    }
}
```

## Using Bootstrap Grid mixins
With npm module [boostrap-sass](https://github.com/twbs/bootstrap-sass), use mixin to custom CSS classes instead of the default Bootstrap CSS classes.

```css
@include container-fixed($gutter: $grid-gutter-width);

@include make-row($gutter: $grid-gutter-width);

@include make-xs-column($columns, $gutter: $grid-gutter-width);
@include make-xs-column-offset($columns);
@include make-xs-column-push($columns);
@include make-xs-column-pull($columns);

@include make-sm-column($columns, $gutter: $grid-gutter-width);
@include make-sm-column-offset($columns);
@include make-sm-column-push($columns);
@include make-sm-column-pull($columns);

@include make-md-column($columns, $gutter: $grid-gutter-width);
@include make-md-column-offset($columns);
@include make-md-column-push($columns);
@include make-md-column-pull($columns);

@include make-lg-column($columns, $gutter: $grid-gutter-width);
@include make-lg-column-offset($columns);
@include make-lg-column-push($columns);
@include make-lg-column-pull($columns);
```
