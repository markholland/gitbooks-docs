# viewer2d.load

> Example:

```javascript--jquery
$('#viewer-2d').bind('viewer2d.load', function(event, modelId) {
    console.log("Viewer2D model loaded", modelId);
});
```

Triggered when viewer and content is completely loaded.

#### Callback parameters

<table class="table">
  <tr>
    <td>modelId</td>
    <td>String</td>
    <td>ID of model</td>
  </tr>
</table>
