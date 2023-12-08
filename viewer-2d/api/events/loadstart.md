# viewer2d.loadstart

> Example:

```javascript--jquery
$('#viewer-2d').bind('viewer2d.loadstart', function(event, modelId) {
    console.log("Viewer2D model load started", modelId);
});
```

Triggered when model load is started.

#### Callback parameters

<table class="table">
  <tr>
    <td>modelId</td>
    <td>String</td>
    <td>ID of model</td>
  </tr>
</table>
