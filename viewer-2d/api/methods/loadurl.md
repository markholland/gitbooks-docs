# loadUrl

> Example:

```javascript--jquery
$('#viewer-2d').viewer2d(
  'loadUrl',
  'https://api.catenda.com/v2/projects/dabc6df.../viewer2d/geometry?token=410c0aa7...',
  { append: true }
);
```

Load the contents of a viewer-2d access token.

**Parameters**:

- url - String
- options
    - append - boolean (optional, default is false) - If append is set to true, the model will be appended to the existing models in the viewer. If set to false, all existing models will be removed before the model is loaded.
    - modelId - String (optional) - The modelId is used to identify the loaded model. Removal of a single model will require the modelId. If not present, a random id will be assigned.
    - modelName - String (optional) - The name of the model. This can be used to store a user friendly name of the model.
