# Create MailFolder

Use this API to create a new mail folder.
### Prerequisites
One of the following **scopes** is required to execute this API: 
*Mail.ReadWrite*
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /users/<objectId>/mailFolders
POST /users/<userPrincipalName>/mailFolders
```
### Request headers
| Header       | Value |
|:---------------|:--------|
| Authorization  | Bearer %token%  |
| Content-Type  | application/json  |

### Request body
In the request body, supply a JSON representation of [MailFolder](../resources/mailfolder.md) object.


### Response
If successful, this method returns `201, Created` response code and [MailFolder](../resources/mailfolder.md) object in the response body.

### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "create_mailfolder_from_user"
}-->
```http
POST https://graph.microsoft.com/v1.0/users/<objectId>/mailFolders
Content-type: application/json

{
    "displayName": "Tailspin Pipeline"
}
```
In the request body, supply a JSON representation of [MailFolder](../resources/mailfolder.md) object.

##### Response
Here is an example of the response.
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.mailfolder"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "displayName": "Tailspin Pipeline",
  "parentFolderId": "parentFolderId-value",
  "childFolderCount": 0,
  "unreadItemCount": 0,
  "totalItemCount": 0,
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create MailFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->