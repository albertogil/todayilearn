# React

## Concatenate JSX objects

Pushing in an array.
*DEPRECATED, use an array map*

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

## Passing arguments in JSX props functions

To pass arguments to the function onClick like:

```html
return (<button onClick={this.sayhi} />);
```

You need to bind the parameters to the function, and with lint you cound bind it before assigning it.

```javascript
clickMethod (message) {
  console.log(`Github todayilearn - ${message}`);
}

// ...

let clickMethod = this.sayhi.bind(this, 'parameter for hi');
return (<button onClick={clickMethod} />);
```

## Handle SVG Icons

Load the selection.json generated from icomoon and get the specific path looking the id in the array.

Or create an array of constants, each with the specifici path of the icon.

[More info](https://medium.com/@david.gilbertson/icons-as-react-components-de3e33cb8792#.94idpw6dp)

