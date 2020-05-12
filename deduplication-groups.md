## Main Endpoint
**GET /api/core/deduplications/groups/<signature_type>:<group_id>**   

Provide access to the items of a specific group. It returns the list of items of a specific group.

Attributes:
* signature-type: the type of the signature (es. title_signature)
* group_id: the id of the group

Return codes:
* 200 OK - if the operation succeed
* 401 Unauthorized - if you are not authenticated
* 403 Forbidden - if you are not logged in with sufficient permissions, only system administrators can access
* 404 Not found - if the signature or the group doesn't exist
