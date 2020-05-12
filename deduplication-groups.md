## Main Endpoint
**GET /api/core/deduplications/groups/<:signature-id>:<:group-checksum>**

Provide access to the items of a specific group. It returns the list of items of a specific group.

Exposed links:
* items: link to the items of a specific group

Return codes:
* 200 OK - if the operation succeed
* 401 Unauthorized - if you are not authenticated
* 403 Forbidden - if you are not logged in with sufficient permissions, only system administrators can access
* 404 Not found - if the signature or the group doesn't exist

### Search methods
#### findBySignature
**/api/core/deduplications/groups/search/findBySignature?signature-type=<:signature-type>**

The supported parameters are:
* **(mandatory)** signature-type, the type of the signature (i.e. "title", etc.)
* page, size [see pagination](README.md#Pagination)

Return codes:
* 200 OK - if the operation succeed
* 400 Bad Request - if the signature-type parameter is missing or invalid

#### findBySignatureAndRule
**/api/core/collections/search/findBySignature?signature-type=<:signature-type>&rule=<:rule>**

The supported parameters are:
* **(mandatory)** signature-type, the type of the signature (i.e. "title", etc.)
* **(mandatory)** rule, is "submitter", "reviewer" or "administrator"
* page, size [see pagination](README.md#Pagination)

Return codes:
* 200 OK - if the operation succeed
* 400 Bad Request - if the signature-type or the rule parameter is missing or invalid
