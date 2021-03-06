---
title: List endpoints
description: Retrieve a list of endpoints exposed by a print service.
author: braedenp-msft
localization_priority: Normal
ms.prod: universal-print
doc_type: apiPageType
---

# List endpoints

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Retrieve a list of endpoints exposed by a print service.

## Permissions
No permissions are needed to call this API, but the user's tenant must have an active Universal Print subscription.

|Permission type | Permissions (from least to most privileged) |
|:---------------|:--------------------------------------------|
|Delegated (work or school account)|None.|
|Delegated (personal Microsoft account)|None.|
|Application|None.|

## HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /print/services/{id}/endpoints
```

## Optional query parameters
This method supports some of the OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers
| Name      |Description|
|:----------|:----------|
| Authorization | Bearer {token}. Required. |

## Request body
Do not supply a request body for this method.
## Response
If successful, this method returns a `200 OK` response code and a collection of [printServiceEndpoint](../resources/printserviceendpoint.md) objects in the response body.
## Example
##### Request
The following is an example of the request.
<!-- {
  "blockType": "request",
  "name": "get_endpoints"
}-->
```http
GET https://graph.microsoft.com/beta/print/services/{id}/endpoints
```
##### Response
The following is an example of the response.
>**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.printServiceEndpoint",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 305

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.printServiceEndpoint)",
  "value": [
    {
      "id": "mpsdiscovery",
      "displayName": "Microsoft Universal Print Discovery Service",
      "uri": "https://discovery.print.microsoft.com"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List endpoints",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->