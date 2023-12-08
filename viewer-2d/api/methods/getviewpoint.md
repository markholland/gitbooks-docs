# getViewpoint

> Example

```javascript--jquery
var viewpoint = $('#viewer-2d').viewer2d('getViewpoint');
console.log(viewpoint);
```

> Example output:

```javascript--jquery
{
    location: {
        x: 1, 
        y: 2,
        z: 34
    },
    direction: {
        x: 0.39,
        y: 0.9,
        z: 0
    }
}
```

Get the viewpoint. Viewpoint is the red arrow which shows where you are looking from.

The height (location.z) is the height of the active storey.
The direction is in the horizontal plane (xy), facing in the direction of the arrow.
