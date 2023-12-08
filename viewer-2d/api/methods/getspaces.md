# getSpaces

> Examples:
```javascript--jquery
// Get all spaces from first loaded model
var spaces = $('#viewer-2d').viewer2d('getSpaces');
console.log(spaces);
```

```javascript--jquery
// Get all spaces
var spaces = $('#viewer-2d').viewer2d('getSpaces', { all: true });
console.log(spaces);
```

```javascript--jquery
// Get all visible spaces
var spaces = $('#viewer-2d').viewer2d('getSpaces', { all: true, visible: true });
console.log(spaces);
```

```javascript--jquery
// Get spaces for a specific building
var spaces = $('#viewer-2d').viewer2d('getSpaces', { buildingId: '0.wskqcff1ik' });
console.log(spaces);
```

```javascript--jquery
// Get spaces for a specific storey
var spaces = $('#viewer-2d').viewer2d('getSpaces', { storeyId: "72150032" });
console.log(spaces);
```

> Example output

```javascript--jquery
[
    {
        id: "2776903120",
        guid: "3gw3QKdmzBThLITx3QSRY2",
        name: "1E16"
        longName: "CENTRAL WAITING",
        storey: "First Floor"
        storeyId: "2776903125"
        boundingBox: {
            height: 10.2760009765625
            width: 4.792999267578125
            x: -50.61149978637695
            y: -48.75149917602539
        }
    }
]
```

Returns an array of space objects.

Due to backward compatibility we will only add spaces from the first loaded model. Add the all flag to the options to get spaces from all models.

**Parameters**:

- object
    - all - boolean (optional) Get spaces from all models.
    - buildingId - string (optional) Get spaces for a specific building.
    - storeyId - string (optional) Get spaces for a specific storey.
    - visible - boolean (optional) Filter query to only include spaces visible in the viewer. This can be combined with other options.
