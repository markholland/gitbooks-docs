# Click

Triggered when the user clicks inside the viewer. Returning false from the event handler will cancel the default viewer behavior.

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
    <td>Id of the object below the cursor. Undefined if no objects are below the cursors.</td>
  </tr>
</table>
