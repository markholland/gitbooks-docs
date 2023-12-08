# getStoreys

> Examples:

```javascript--jquery
// Get all storeys from first loaded model
var storeys = $('#viewer-2d').viewer2d('getStoreys');
console.log(storeys);
```

```javascript--jquery
// Get all storeys
var storeys = $('#viewer-2d').viewer2d('getStoreys', { all: true });
console.log(storeys);
```

```javascript--jquery
// Get all visible storeys
var storeys = $('#viewer-2d').viewer2d('getStoreys', { all: true, visible: true });
console.log(storeys);
```

```javascript--jquery
// Get storeys for a given building
var storeys = $('#viewer-2d').viewer2d('getStoreys', { buildingId: '0.aqifqv5mjx7' });
console.log(storeys);
```

> Example output:
```javascript--jquery
[
    {
        elevation: "-2.77",
        id: "2776903120",
        guid: "3eM8WbY_59RR5TDWs3wwJP",
        name: "basement"
    }
]
```

Returns an array of storey objects.
Due to backward compatibility we will only include storeys from the first loaded model. Use the all flag to the options to get storeys from all models.

**Parameters**:

- object
    - buildingId - string (optional) Get storeys for a specific building.
    - all - boolean (optional) Get storeys from all models.
    - visible - boolean (optional) Filter query to only include storeys visible in the viewer. This can be combined with other options.
