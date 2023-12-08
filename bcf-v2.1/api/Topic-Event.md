# Topic Event

## Get topic events

> Example request
```http
GET https://api.catenda.com/opencde/bcf/3.0/projects/5af9e867-659d-4eee-ae56-2370aaf8aabe/topics/c84392ec-065f-4c89-aa2b-644486ca8e34/events
```

> Example response
```json
[
    {
        "topic_guid": "c84392ec-065f-4c89-aa2b-644486ca8e34",
        "date": "2020-02-21T14:59:48.828+0000",
        "author": "user1@test.com",
        "actions": [
            {
                "type": "topic_created"
            },
            {
                "type": "title_updated",
                "value": "my changed title"
            },
            {
                "type": "status_updated",
                "value": "Open"
            },
            {
                "type": "type_updated",
                "value": "Error"
            },
            {
                "type": "priority_removed"
            }
        ]
    }
]
```

Return all events for the given topic.

### Resource URL

`https://api.catenda.com/opencde/bcf/{version_id}/projects/{project_id}/topics/{topic_guid}/events`

### Response schema
[topic_event_GET.json](https://github.com/buildingSMART/BCF-API/blob/release_3_0/Schemas_draft-03/Collaboration/Events/topic_event_GET.json)


