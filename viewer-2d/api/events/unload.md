# viewer2d.unload

> Example:

```javascript--jquery
$('#viewer-2d').bind('viewer2d.unload', function(event, modelId) {
    console.log("Viewer2D model unloaded", modelId);
});
```

Triggered when viewer and content is unloaded.

#### Callback parameters

<table class="table">
  <tr>
    <td>modelId</td>
    <td>String</td>
    <td>ID of model</td>
  </tr>
</table>
