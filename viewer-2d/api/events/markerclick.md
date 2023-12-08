# viewer2d.markerclick

> Example:

```javascript--jquery
var marker = $('#viewer-2d').viewer2d('addMarker', {
  id: 42,
  x:1.45,
  y:0.34,
  color: 'yellow',
  text: 'Remove door',
  clickable: true
});
$('#viewer-2d').bind('viewer2d.markerclick', function(event, marker) {
    console.log('Marker clicked', marker.id);
});
```

Triggered when the user clicks on a [marker](#marker-interface). The marker must be created as `clickable`.

Returning false from the event handler will cancel the default viewer behavior.

#### Callback Parameters

Name | Type | Description
---- | ---- | ---------
marker | [Marker](#marker-interface) | The clicked marker
