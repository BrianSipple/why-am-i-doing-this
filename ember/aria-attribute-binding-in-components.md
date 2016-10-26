# ARIA Attribute Binding in Components

For boolean ARIA attributes (otherwise known as ARIA "state" attributes), 
we need to 
[explicitly have "true" or "false" assigned](https://www.w3.org/TR/wai-aria/appendices#typemapping) 
to the attribute in the DOM.

However, Ember's Component `attributeBinding` follow the 
more common practice of simply placing the attribute on the element
if its `true`, or removing it if it's `false`.

**component**:
```js 
attributeBindings: ['aria-hidden', 'foo', 'bar'],

'aria-hidden': true,
foo: true,
bar: false
```

**resulting DOM Node**:

```html
<div aria-hidden foo></div>
```


To get around this for ARIA attributes, we can associate 
the bouund property with a string value of "true" or "false":

**component**:
```js 
attributeBindings: ['aria-hidden', 'foo', 'bar'],

'aria-hidden': 'true',
foo: true,
bar: false
```

**resulting DOM Node**:

```html
<div aria-hidden="true" foo></div>
```



