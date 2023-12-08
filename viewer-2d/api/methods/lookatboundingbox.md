# lookAtBoundingBox

> Example:

```javascript--jquery
$('#viewer-2d').viewer2d(
  'lookAtBoundingBox',
  {
    min: { x: -50.6115, y: -58.1927 },
    max: { x: 1.648, y: 7.6145 }
  }
);
$('#viewer-2d').viewer2d(
  'lookAtBoundingBox',
  {
    min: { x: -50.6115, y: -58.1927, z: 2.1 },
    max: { x: 1.648, y: 7.6145, z: 3.1 }
  },
  {
    retainStoreys: true
  }
);
```

Set view to a bounding box.

The retainStoreys option works as in lookAt when z is present. If z is absent, the storeys will be retained.

**Parameters**:

- boundingBox
    - min
        - x - numbers
        - y - numbers
        - z - numbers - optional
    - max
        - x - numbers
        - y - numbers
        - z - numbers - optional

- options
    - retainStoreys - boolean (optional) Retain current storeys. Default is false if z is present and true if z is absent.
