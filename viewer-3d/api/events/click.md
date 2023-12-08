# click

Triggered when the user clicks inside the viewer. Returning false from the event handler will cancel the default viewer behavior.

#### Callback Parameters

| location | Object | Global coordinate of the cursor. Z value is the height of the intersection plane. |
| -------- | ------ | --------------------------------------------------------------------------------- |
| id       | String | Id of the object below the cursor. Undefined if no objects are below the cursors. |
