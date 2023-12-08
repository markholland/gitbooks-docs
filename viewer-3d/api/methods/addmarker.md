# addMarker

> Example:

```javascript--jquery
var id = $('#viewer-2d').viewer2d('addMarker', {
    id: 'P325',
    x:1.45,
    y:0.34,
    color: '#aaaaaa',
    text: 'Test',
    data: { owner: 'Jan Erik' },
    clickable: true,
    draggable: false
});
```

Add a marker to specific location.

**Properties**

Name | Type | Description
---- | ---- | ---------
marker | [MarkerParams](#markerparams-interface) | The parameters to add a new [Marker](#marker-interface)

**Returns**
Type | Description
---- | ---------
string | The id of the new [Marker](#marker-interface)
