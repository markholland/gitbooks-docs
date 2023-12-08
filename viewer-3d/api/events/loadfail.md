# viewer2d.loadfail

> Example:

```javascript--jquery
$('#viewer-2d').bind('viewer2d.loadfail', function(event, modelId) {
    console.log("Viewer2D model load failed", modelId);
});
```

Triggered when model load fails.

#### Callback parameters

<table class="table">
  <tr>
    <td>modelId</td>
    <td>String</td>
    <td>ID of model</td>
  </tr>
</table>
