# viewer2d.contextmenu

> Example:

```javascript--jquery
$('#viewer-2d').bind('viewer2d.contextmenu', function(event, location, id) {
    console.log('viewer2d.contextmenu', 'location', location, 'id', id);
});
```

Triggered when the user summons the context menu (e.g. by right-clicking).

#### Callback Parameters

<table class="table">
  <tr>
    <td>location</td>
    <td>Object</td>
    <td>Global coordinate of the cursor. Z value is the height of the intersection plane.</td>
  </tr>
  <tr>
    <td>id</td>
    <td>String</td>
    <td>Id of the object below the cursor. Undefined if no objects are below the cursor.</td>
  </tr>
</table>

