# setSpaceNames

> Example:

```javascript--jquery
$('#viewer-2d').viewer2d(
  'setSpaceNames',
  {
    '123456789': {
      name: '001.001'
      longName: 'Kitchen'
    },
    '987654321': {
      name: '001.002'
      longName: 'Living room'
    }
  }
);
```

Change the names being displayed for spaces.

**Parameters**:

- names - object
    Map from object ID to an object containing name and/or longname values.
