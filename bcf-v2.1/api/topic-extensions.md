# Topic extensions

## Get objects 
> Example

```http
GET https://api.catenda.com/opencde/bcf/3.0/projects/3c34c9b3-1b9b-4750-a4f3-0641d58fe48e/topics/6411ce04-5391-40a6-97c2-be0ca45fcc96/objects
```
```json
[
    {
        "ifcGuid": "3BY5alwwL00QXHtY2qmHYZ"
    },
    {
        "ifcGuid": "0w1FD2e5L4LOvXHSZSTtLq"
    },
    {
        "ifcGuid": "0Arc0R2mf2Ow2ddxcQ40yG"
    }
]
```

Return a list of objects linked to a topic. Each object has 1 attribute. **ifcGuid**.

**ifcGuid** the ifcGuid of the object 

Note: this resource is additional to the BCF-API standard, and may change in the future

### Resource URL

`https://api.catenda.com/opencde/bcf/{version_id}/projects/{project_id}/topics/{topic_guid}/objects`


