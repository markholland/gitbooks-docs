# Viewpoint

## Get viewpoints 

> Example request
```http
GET https://api.catenda.com/opencde/bcf/3.0/projects/3c34c9b3-1b9b-4750-a4f3-0641d58fe48e/topics/6411ce04-5391-40a6-97c2-be0ca45fcc96/viewpoints
```

> Example response
```json
[
    {
        "guid": "82d00ffb-22aa-48b1-924f-dc59c487d585",
        "lines": [],
        "clipping_planes": [],
        "bitmaps": [],
        "snapshot": {
            "snapshot_type": "png"
        }
    },
    {
        "index": 2,
        "guid": "25777de1-b354-4432-88a9-fd45f0e4aea7",
        "perspective_camera": {
            "camera_view_point": {
                "x": -1.3757544290857453,
                "y": -14.084548687547457,
                "z": 15.77535220227417
            },
            "camera_direction": {
                "x": 0.48836276817323054,
                "y": 0.6442499485024906,
                "z": -0.5885947761547989
            },
            "camera_up_vector": {
                "x": 0.3555637551166773,
                "y": 0.4690610051624899,
                "z": 0.808428221602439
            },
            "field_of_view": 60.0
        },
        "lines": [],
        "clipping_planes": [],
        "bitmaps": [
            {
                "guid": "3a720dc7-2b3e-418c-82b4-42c129105ecc",
                "location": {
                    "x": 21.97304764097038,
                    "y": -24.86912390497038,
                    "z": 19.66912390497035
                },
                "normal": {
                    "x": -0.5773502691896258,
                    "y": 0.5773502691896258,
                    "z": -0.5773502691896258
                },
                "up": {
                    "x": -0.4082482904638631,
                    "y": 0.4082482904638631,
                    "z": 0.8164965809277261
                },
                "height": -1.0
            }
        ],
        "snapshot": {}
    }
]
```

Return the viewpoints.

### Resource URL

`https://api.catenda.com/opencde/bcf/{version_id}/projects/{project_id}/topics/{topic_guid}/viewpoints`

### Response schema
List of [viewpoint_GET.json](https://github.com/buildingSMART/BCF-API/blob/release_3_0/Schemas_draft-03/Collaboration/Viewpoint/viewpoint_GET.json)
 

