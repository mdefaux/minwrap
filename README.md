# Min Wrap
Minimal Wrapper for DOM

#### Synopsis
A collection of utility classes and methods for managing DOM objects and create a minimal support for creating a single-page application. DOM objects are created and wrapped in an utility class that provide methods with uniform syntax style and convention.

#### Example

```html
<body>
  <div class='my-class' />
</body>
```

Traditional:
```js
let dom = document.querySelector('.my-class');
if( !dom )
  throw new Error('Not found.');
wrapper.onclick= function(evt) 
{
    show();
};
```

Using minwrap:
```js
let wrapper = $select('.my-class'); // implicit assertion of object found
wrapper.onClick( (evt) => // uses camel case syntax with onClick
{
    show();
});
```
