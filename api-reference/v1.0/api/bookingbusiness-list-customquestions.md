---
title: "List customQuestions"
description: "Get the bookingCustomQuestion resources associated with a bookingBusiness."
author: "razortbone"
ms.localizationpriority: medium
ms.prod: "bookings"
doc_type: apiPageType
---

# List customQuestions

Namespace: microsoft.graph

Get the [bookingCustomQuestion](../resources/bookingcustomquestion.md) resources associated with a [bookingBusiness](../resources/bookingbusiness.md).

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "bookingbusiness_list_customquestions" } -->
[!INCLUDE [permissions-table](../includes/permissions/bookingbusiness-list-customquestions-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}-->

```http
GET /solutions/bookingBusinesses/{bookingBusinessesId}/customQuestions
```

## Optional query parameters

This method supports some of the OData query parameters to help customize the response. For general information, see $count and $expand [OData query parameters](/graph/query-parameters).

## Request headers

| Name          | Description               |
| :------------ | :------------------------ |
| Authorization | Bearer {token}. Required. |

## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a collection of [bookingCustomQuestion](../resources/bookingcustomquestion.md) objects in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "sampleKeys": ["Contosolunchdelivery@contoso.onmicrosoft.com"]
}-->
```http
GET https://graph.microsoft.com/v1.0/solutions/bookingBusinesses/Contosolunchdelivery@contoso.onmicrosoft.com/customQuestions
```

### Response

> **Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.bookingCustomQuestion",
  "isCollection": true
}
-->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
        "@odata.type": "#microsoft.graph.bookingCustomQuestion",
        "id": "3bc6fde0-4ad3-445d-ab17-0fc15dba0774",
        "displayName": "What is your age?",
        "answerInputType": "text",
        "answerOptions": [],
    },
    {
        "@odata.type": "#microsoft.graph.bookingCustomQuestion",
        "id": "dbb865a6-530d-46e1-8e88-5d76789034b2",
        "displayName": "What is your nationality?",
        "answerInputType": "radioButton",
        "answerOptions": [
          "US",
          "UK",
          "Canada",
          "India"
        ],
    }
  ]
}
```
