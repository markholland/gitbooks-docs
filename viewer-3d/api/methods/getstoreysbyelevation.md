# getStoreysByElevation

> Example:

```javascript--jquery
var storeys = $('#viewer-2d').viewer2d('getStoreysByElevation', 3.2);
console.log(storeys);
```

> Example output:

```javascript--jquery
[
    {
        id: "2777293459",
        guid: "3eM8WbY_59RR5TDWs3wwJP",
        name: "2. floor",
        elevation: "2.77"
    },
    {
        id: "1579293459",
        guid: "5aa9WbY_59RR5TDWs3wwJP",
        name: "3. floor",
        elevation: "2.5"
    }
]
```

Gets storeys from all models at a given elevation.

**Parameters**:

- elevation - Double
