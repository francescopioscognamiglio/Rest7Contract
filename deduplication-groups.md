## Main Endpoint
**GET /api/core/deduplications/groups/<signature_type>:<group_id>**   
(prima era /api/core/deduplications/signatures/<:signature_id>/groups/<:group_id>)

Provide detailed information about a specific group. The JSON response document is as follow

```json
{
  items: [
    {
	  ...
	},
    {
	  ...
	}
  ]
}
```

Attributes:
* signature_id: the id of the signature
* group_id: the id of the group

Exposed links:

Return codes:
* 200 OK - if the operation succeed
* 401 Unauthorized - if you are not authenticated
* 403 Forbidden - if you are not logged in with sufficient permissions, only system administrators can access
* 404 Not found - if the signature or the group doesn't exist
