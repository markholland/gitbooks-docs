# Viewpoint extensions

## Get viewpoint models

> Example request
```http
GET https://api.catenda.com/opencde/bcf/3.0/projects/3c34c9b3-1b9b-4750-a4f3-0641d58fe48e/topics/6411ce04-5391-40a6-97c2-be0ca45fcc96/viewpoints/63fc95fa-0dcc-4e5b-b889-72db4a467113/models
```

> Example response
```json
[
    {
        "modelRef": "3a8a62f0226b4a1da994481730de6adf",
        "revisionRef": "a21ed391-f9e0-46a2-bb2b-c879c48f1d48"
    },
    {
        "modelRef": "b8beba1a10fb44c8a67fefb2d182f3e4",
        "revisionRef": "4e8e119a-dbdf-4ce7-bf54-6de38cd171f9"
    }
]
```

Return the viewpoint models.

The initial value is calculated when the viewpoint is created.
- For viewpoints created from BCF-API or BCF file import, the models is a "best guess", based on components being marked as selected or visible.
- For viewpoints created inside arena, the models are the visible models at the time the viewpoint was created.

Each element has 2 attributes. **modelRef** and **revisionRef**.
**modelRef** A reference to the model.
**revisionRef** A reference to the model revision.

Note: this resource is additional to the BCF-API standard

### Resource URL

`https://api.catenda.com/opencde/bcf/{version_id}/projects/{project_id}/topics/{topic_guid}/viewpoints/{viewpoint_guid}/models`
