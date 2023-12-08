# lookAt

> Example:

```javascript--jquery
$('#viewer-2d').viewer2d('lookAt', '123456');
$('#viewer-2d').viewer2d('lookAt', ['123456', '234567']);
$('#viewer-2d').viewer2d('lookAt', ['123456', '234567'], { retainStoreys: true });
$('#viewer-2d').viewer2d('lookAt', ['123456', '234567'], { retainStoreys: true, expand: 1.8 });
$('#viewer-2d').viewer2d('lookAt', ['123456', '234567'], { retainStoreys: true, expand: { x: 2, y: 3 } });
```

Move given objects into view.

If any of the objects are visible, we will retain the current storeys. 
Otherwise we will change to the storeys matching the lowest elevation of the objects.
If you always want to retain the current storeys you can set the retainStoreys option to true.

**Parameters**:

- objectId - string or array of string
- options
    - retainStoreys - boolean (optional) Always retain current storeys. Default is false.
    - expand - numbers or vector - Expand the view to include some of the area surrounding the objects. Unit is in meters.
