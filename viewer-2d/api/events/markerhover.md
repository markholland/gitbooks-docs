# viewer2d.markerhover

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
$('#viewer-2d').bind('viewer2d.markerhover', function(event, marker) {
    console.log('Hovered over marker', marker.id);
});
```

Triggered when the user hovers over a [marker](#marker-interface).

Returning false from the event handler will cancel the default viewer behavior.

#### Callback Parameters

<table class="table">
  <tr>
    <td>marker</td>
    <td>[Marker](#marker-interface)</a></td>
    <td>The hovered marker.</td>
  </tr>
</table>
