## Main Endpoint
**GET /api/core/deduplications/signatures**   

Provide access to the configured signatures. It returns the list of existent signatures.

Return codes:
* 200 OK - if the operation succeed
* 401 Unauthorized - if you are not authenticated
* 403 Forbidden - if you are not logged in with sufficient permissions, only system administrators can access

## Single Signature
**GET /api/core/deduplications/signatures/<:signature-type>**

Provide detailed information about a specific signature. The JSON response document is as follow

```json
{
  groupReviewerCheck: 0,
  groupSubmitterCheck: 0,
  groupAdminstratorCheck: 0
}
```

Attributes:
* signature-type: the type of the signature (es. title_signature)

Return codes:
* 200 OK - if the operation succeed
* 401 Unauthorized - if you are not authenticated
* 403 Forbidden - if you are not logged in with sufficient permissions, only system administrators can access
* 404 Not found - if the signature doesn't exist

## Signature groups
**GET /api/core/deduplications/signatures/<:signature-type>/groups**

Provide access to the groups of a specific signature. It returns the list of existent groups of a signature.

Attributes:
* signature-type: the type of the signature (es. title_signature)

Return codes:
* 200 OK - if the operation succeed
* 401 Unauthorized - if you are not authenticated
* 403 Forbidden - if you are not logged in with sufficient permissions, only system administrators can access

To access single signature group see [deduplication-groups endpoint](deduplication-groups.md#main-endpoint)
