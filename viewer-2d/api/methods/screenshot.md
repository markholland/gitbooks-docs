# screenshot

> Example:

```javascript--jquery
$('#viewer-2d').viewer2d('screenshot', { width: 1024, height: 768 }, function(image) {
  $element.attr('src', image);
});
```

Get a 2D screenshot in PNG format.

**Parameters**:

- options
    - width - width of the screenshot,
    - height - height of the screenshot 

- callback - method - returns the image produced
