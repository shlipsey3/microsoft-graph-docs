---
title: "Update bookingCustomQuestion"
description: "Update the properties of a bookingCustomQuestion object."
author: "razortbone"
ms.localizationpriority: medium
ms.prod: "bookings"
doc_type: apiPageType
---

# Update bookingCustomQuestion

Namespace: microsoft.graph

Update the properties of a [bookingCustomQuestion](../resources/bookingcustomquestion.md) object.

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "bookingcustomquestion_update" } -->
[!INCLUDE [permissions-table](../includes/permissions/bookingcustomquestion-update-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->

```http
PATCH /solutions/bookingBusinesses/{bookingBusinessesId}/customQuestions/{bookingCustomQuestionId}
```

## Request headers

| Name          | Description                 |
| :------------ | :-------------------------- |
| Authorization | Bearer {token}. Required.   |
| Content-Type  | application/json. Required. |

## Request body

[!INCLUDE [table-intro](../../includes/update-property-table-intro.md)]

| Property        | Type              | Description                                                                                                         |
| :-------------- | :---------------- | :------------------------------------------------------------------------------------------------------------------ |
| answerInputType | answerInputType   | The expected answer type. The possible values are: `text`, `radioButton`, `unknownFutureValue`. Optional.    |
| answerOptions   | String collection | List of possible answer values. Optional.                                                                   |
| displayName     | String            | The question. Required. |

## Response

If successful, this method returns a `200 OK` response code and an updated [bookingCustomQuestion](../resources/bookingcustomquestion.md) object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "sampleKeys": ["Contosolunchdelivery@contoso.onmicrosoft.com", "91f1ef26-ca00-451c-1c64-8f3560c80d3d"]
}-->
```http
PATCH https://graph.microsoft.com/v1.0/solutions/bookingBusinesses/Contosolunchdelivery@contoso.onmicrosoft.com/customQuestions/91f1ef26-ca00-451c-1c64-8f3560c80d3d
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.bookingCustomQuestion",
  "displayName": "What is your age?",
  "answerInputType": "text",
  "answerOptions": []
}
```

### Response

> **Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.bookingCustomQuestion"
}
-->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.bookingCustomQuestion",
  "id": "91f1ef26-ca00-451c-1c64-8f3560c80d3d",
  "displayName": "What is your age?",
  "answerInputType": "text",
  "answerOptions": []
}
```
