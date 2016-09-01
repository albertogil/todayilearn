# React

## Concatenate JSX objects

Pushing in an array.

```javascript
let returnValue = [];
for (var i = breaks; i > 0; i--) {
  returnValue.push(<p className='test'>hi</p>);
}
return returnValue;
```

## Pass style attributes in JSX

Passing Javasctipt object

```javascript
let styleConfig = { width: ((100 / 3) + '%'), backgroundColor : 'red' };

return (<div  style={ styleConfig }>Box Content</div>);
```
