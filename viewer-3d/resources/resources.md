# Examples

{% swagger method="get" path="" baseUrl="https://api.catenda.com/v2/projects/:project/members" summary="List project members." %}
{% swagger-description %}
​
{% endswagger-description %}

{% swagger-parameter in="path" name="project" required="true" %}
ID of the project
{% endswagger-parameter %}

{% swagger-parameter in="query" name="userType" %}
Filter by userType. Accepts the values 'user', 'team' or 'organization'
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}

{% endswagger-response %}

{% swagger-response status="404: Not Found" description="Project (:project) not found" %}

{% endswagger-response %}
{% endswagger %}

{% tabs %}
{% tab title="Curl" %}
```bash
curl -X GET \"
    --header "Authorization: Bearer $ACCESS_TOKEN" \
    "https://api.catenda.com/v2/projects/af2d8af0fa54465b89bf26dd3d92cfd0/members"
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
fetch(
  "https://api.catenda.com/v2/projects/af2d8af0fa54465b89bf26dd3d92cfd0/members"
)
  .then((response) => response.json())
  .then((data) => {
    console.log(data);
  });
```
{% endtab %}
{% endtabs %}

{% code title="Response" %}
```json
[
    {
        "role": "owner",
        "user": {
            "avatarUrl": "https://api.catenda.com/v2/avatar/Q4g778jIuQy40X4jaqF7"
            "createdAt": "2016-09-20T14:32:25Z",
            "id": "b8dd966cb6d844d3bbaa2705d9e7d980",
            "name": "Kristine Knight",
            "username": "kristine.knight@example.com"
        }
    },
    {
        "role": "member",
        "user": {
            "avatarUrl": "https://api.catenda.com/v2/avatar/r31Jf8LKkeZ744Gsf"
            "createdAt": "2016-09-20T14:32:25Z",
            "id": "573761199e2147dcae4a7a0661e03a26",
            "name": "Robin Chapel",
            "username": "robin.chapel@example.com"
        }
    }
]
```
{% endcode %}

{% hint style="danger" %}
An important warning about unexpected behaviour you should be aware of
{% endhint %}

{% swagger method="get" path="" baseUrl="https://api.catenda.com/v2/projects/:project/members/:user" summary="Get a project member." %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="project" %}
ID of the project
{% endswagger-parameter %}

{% swagger-parameter in="path" name="user" %}
ID of the user
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}

{% endswagger-response %}

{% swagger-response status="404: Not Found" description="" %}

{% endswagger-response %}
{% endswagger %}

```json
{
    "role": "owner",
    "user": {
        "avatarUrl": "https://api.catenda.com/v2/avatar/Q4g778jIuQy40X4jaqF7"
        "createdAt": "2016-09-20T14:32:25Z",
        "id": "b8dd966cb6d844d3bbaa2705d9e7d980",
        "name": "Kristine Knight",
        "username": "kristine.knight@example.com"
    }
}
```

[![Run In Postman](https://run.pstmn.io/button.svg)](https://god.gw.postman.com/run-collection/:collection\_id)
