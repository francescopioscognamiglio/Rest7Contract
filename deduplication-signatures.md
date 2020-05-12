## Main Endpoint
**GET /api/core/deduplications/signatures**   

Provide access to the configured signatures. It returns the list of existent signatures.

Return codes:
* 200 OK - if the operation succeed
* 401 Unauthorized - if you are not authenticated
* 403 Forbidden - if you are not logged in with sufficient permissions, only system administrators can access

## Single Signature
**GET /api/core/deduplications/signatures/<:id>**

Provide detailed information about a specific signature. The JSON response document is as follow

```json
{
  id: "title",
  signatureType: "title",
  groupReviewerCheck: 0,
  groupSubmitterCheck: 0,
  groupAdminstratorCheck: 0
}
```

Attributes:
* signatureType: the type of the signature
* groupReviewerCheck: number of groups identified by the system and not reject by the reviewers
* groupSubmitterCheck: number of groups identified by the system and not reject by the submitters
* groupAdminstratorCheck: number of groups identified by the system and not reject by the administrators

Return codes:
* 200 OK - if the operation succeed
* 401 Unauthorized - if you are not authenticated
* 403 Forbidden - if you are not logged in with sufficient permissions, only system administrators can access
* 404 Not found - if the signature doesn't exist
