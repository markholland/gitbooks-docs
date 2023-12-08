# getStoreyByElevation

> Example:

```javascript--jquery
var storey = $('#viewer-2d').viewer2d('getStoreyByElevation', 3.2);
console.log(storey);
```

> Example output:

```javascript--jquery
{
    id: "2777293459",
    guid: "3eM8WbY_59RR5TDWs3wwJP",
    name: "2. floor",
    elevation: "2.77"
}
```

Gets the storey at a given elevation. This will only give the storey for the first model loaded.
Use getStoreysByElevation to get storeys for all models.

**Parameters**:

- elevation - Double
