## setViewpoint

> Examples:

```javascript--jquery
$('#viewer-2d').viewer2d('setViewpoint', {location: {x: 1, y: 2}});
$('#viewer-2d').viewer2d('setViewpoint', {location: {x: 1, y: 2}, direction: 90});
$('#viewer-2d').viewer2d('setViewpoint', {location: {x: 1, y: 2}, direction: {x: 0.39, y: 0.92} });
```

Set the location and orientation of the viewpoint.

**Parameters**:

- object
    - location - { x, y }
    - direction - numbers in degrees or normalized vector { x, y }
