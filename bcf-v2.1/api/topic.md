# Topic

Get topics

> Example request

```http
GET https://api.catenda.com/opencde/bcf/3.0/projects/3c34c9b3-1b9b-4750-a4f3-0641d58fe48e/topics
```

> Example response

```json
[
    {
        "guid": "ea7ca636-77e9-4e89-9188-aa5fe7f53036",
        "server_assigned_id": "2",
        "topic_type": "Error",
        "topic_status": "Open",
        "reference_links": [],
        "title": "Door issue",
        "labels": [],
        "creation_date": "2020-02-20T15:56:03.254+0000",
        "creation_author": "king@test.com",
        "modified_date": "2020-03-02T11:11:01.771+0000",
        "modified_author": "king@test.com",
        "assigned_to": "king@test.com",
        "description": "Door is misplaced",
        "bimsync_issue_number": 2,
        "bimsync_assigned_to": {
            "user": {
                "ref": "e4d94d45f7194f1f9f7b29ed994d01e4",
                "email": "king@test.com",
                "name": "King"
            },
            "team": {
                "ref": "fc9a1a7e2df143da887aeea27a90c400",
                "email": "team-h9TxeafTR6gWQXxF@bimsync.com",
                "name": "Chess mates"
            }
        },
        "bimsync_creation_author": {
            "user": {
                "ref": "e4d94d45f7194f1f9f7b29ed994d01e4",
                "email": "king@test.com",
                "name": "King Kong"
            },
            "importedBy": null
        }
    },
    {
        "guid": "0a4f77f2-7b6a-467d-ad70-32a3a6e0a345",
        "server_assigned_id": "1",
        "topic_type": "Warning",
        "topic_status": "Open",
        "reference_links": [],
        "title": "Heater in the air",
        "labels": [],
        "creation_date": "2020-02-20T15:55:27.507+0000",
        "creation_author": "king@test.com",
        "modified_date": "2020-03-02T11:11:12.925+0000",
        "modified_author": "king@test.com",
        "assigned_to": "pawn@test.com",
        "description": "Heater is floating in the air",
        "bimsync_issue_number": 1,
        "bimsync_assigned_to": {
            "user": {
                "ref": "f081f1857d124317b2e8f135d605f731",
                "email": "pawn@test.com",
                "name": "Pawn"
            },
            "team": {
                "ref": "fc9a1a7e2df143da887aeea27a90c400",
                "email": "team-h9TxeafTR6gWQXxF@bimsync.com",
                "name": "Chess mates"
            }
        },
        "bimsync_creation_author": {
            "user": {
                "ref": "e4d94d45f7194f1f9f7b29ed994d01e4",
                "email": "king@test.com",
                "name": "King Kong"
            },
            "importedBy": null
        }
    }
]
```

Return the topics. Default size is 100 items, max size is 500 items. Cannot return all issue boards, so a filter is required.

**Filter, sort, skip and limit using OData**

**Odata filter parameters**

| Parameter                 | Type           | Description                                          |   |
| ------------------------- | -------------- | ---------------------------------------------------- | - |
| bimsync\_creation\_author | string         | userRef of the creation author                       |   |
| creation\_author          | string         | email of the creation author (value from extensions) |   |
| modified\_author          | string         | email of the modified author (value from extensions) |   |
| assigned\_to              | string         | email of the assigned person (value from extensions) |   |
| stage                     | string         | stage this topic is part of (value from extensions)  |   |
| topic\_status             | string         | status of a topic (value from extensions)            |   |
| topic\_type               | string         | type of a topic (value from extensions)              |   |
| creation\_date            | datetime       | creation date of a topic                             |   |
| modified\_date            | datetime       | modification date of a topic                         |   |
| labels                    | array (string) | labels of a topic (value from extensions)            |   |

**OData sort parameters**

| parameter      | description                  |
| -------------- | ---------------------------- |
| creation\_date | creation date of a topic     |
| modified\_date | modification date of a topic |
| index          | index of a topic             |

> Odata example requests

> Get topics that are open, assigned to Architect@example.com and created after December 5th 2015. Sort the result on last modified.

```http
GET https://api.catenda.com/opencde/bcf/3.0/projects/F445F4F2-4D02-4B2A-B612-5E456BEF9137/topics?$filter=assigned_to eq 'Architect@example.com' and status eq 'Open' and creation_date gt 2015-12-05T00:00:00+01:00&$orderby=modified_date desc
```

> Get topics that have at least one of the labels 'Architecture', 'Structural' or 'Heating'.

```http
GET https://api.catenda.com/opencde/bcf/3.0/projects/F445F4F2-4D02-4B2A-B612-5E456BEF9137/topics?$filter=contains(labels, 'Architecture') or contains(labels, 'Structural') or contains(labels, 'Heating')
```

> Get 50 topics and skip the first 100.

```http
GET https://api.catenda.com/opencde/bcf/3.0/projects/F445F4F2-4D02-4B2A-B612-5E456BEF9137/topics?$top=50&$skip=100
```

#### Select

> Example request with select

```http
GET https://api.catenda.com/opencde/bcf/3.0/projects/3c34c9b3-1b9b-4750-a4f3-0641d58fe48e/topics?$select=creation_date,modified_date,assigned_to
```

> Example response with select

```json
[
    {
        "guid": "44405b7c-7bc1-4ea7-813b-e0ef156eb6db",
        "server_assigned_id": "12",
        "creation_date": "2020-03-03T08:06:39.264+0000",
        "modified_date": "2020-03-06T12:31:58.018+0000",
        "assigned_to": "king@test.com",
        "bimsync_issue_number": 12,
        "bimsync_assigned_to": {
            "user": {
                "ref": "e4d94d45f7194f1f9f7b29ed994d01e4",
                "email": "king@test.com",
                "name": "King"
            },
            "team": null
        },
        "bimsync_imported_at": "2020-03-03T11:10:46.986+0000"
    },
    {
        "guid": "c720fd87-75ad-4ba6-ac26-9296b4f6ff73",
        "server_assigned_id": "11",
        "creation_date": "2020-03-03T08:06:39.264+0000",
        "modified_date": "2020-03-03T08:06:39.264+0000",
        "assigned_to": "king@test.com",
        "bimsync_issue_number": 11,
        "bimsync_assigned_to": {
            "user": {
                "ref": "e4d94d45f7194f1f9f7b29ed994d01e4",
                "email": "king@test.com",
                "name": "King"
            },
            "team": null
        },
        "bimsync_imported_at": "2020-03-03T11:10:23.158+0000"
    }
]
```

Use **$select** as a query parameter to choose which properties to include in the response. **guid**, **server\_assigned\_id** and **bimsync\_issue\_number** are always returned in addition.

| Parameter                           | Returns                                     |
| ----------------------------------- | ------------------------------------------- |
| \*                                  | all default fields                          |
| title                               | title                                       |
| description                         | description                                 |
| index                               | index                                       |
| labels                              | labels                                      |
| due\_date                           | due\_date                                   |
| stage                               | stage                                       |
| creation\_author                    | creation\_author, bimsync\_creation\_author |
| creation\_date                      | creation\_date, bimsync\_imported\_at       |
| modified\_date                      | modified\_date                              |
| modified\_author                    | modified\_author                            |
| assigned\_to, bimsync\_assigned\_to | assigned\_to, bimsync\_assigned\_to         |
| topic\_status                       | topic\_status                               |
| topic\_type                         | topic\_type                                 |
| topic\_priority                     | topic\_priority                             |
| reference\_links                    | reference\_links                            |
| bim\_snippet                        | bim\_snippet                                |
| bimsync\_comments\_size             | bimsync\_comments\_size                     |
| bimsync\_requester                  | bimsync\_requester                          |
| bimsync\_custom\_fields             | bimsync\_custom\_fields                     |
| bimsync\_points                     | bimsync\_points                             |

#### Resource URL

`https://api.catenda.com/opencde/bcf/{version_id}/projects/{project_id}/topics`

#### Response schema

List of [topic\_GET.json](https://github.com/buildingSMART/BCF-API/blob/release\_3\_0/Schemas\_draft-03/Collaboration/Topic/topic\_GET.json)
