---
title: "Delete timeCard"
description: "Delete a timeCard instance in the schedule."
author: "akumar39"
ms.localizationpriority: medium
ms.prod: "microsoft-teams"
doc_type: apiPageType
---

# Delete timeCard

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Delete a [timeCard](../resources/timeCard.md) instance in a [schedule](../resources/schedule.md).

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "timecard_delete" } -->
[!INCLUDE [permissions-table](../includes/permissions/timecard-delete-permissions.md)]

>\* **Important:** When you use application permissions, you must include the `MS-APP-ACTS-AS` header in the request.

## HTTP request

<!-- { "blockType": "ignored" } -->

```http
DELETE /teams/{teamId}/schedule/timeCards/{timeCardID}
```

## Request headers

| Header       | Value |
|:---------------|:--------|
| Authorization  | Bearer {token}. Required.  |
| MS-APP-ACTS-AS | The ID of the user on behalf of whom the app is acting. Required when you use the application permission scope. |

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `204 No Content` response code.

## Example

### Request
The following is an example of the request. 


# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "timecard-delete"
}-->

```http
DELETE https://graph.microsoft.com/beta/teams/871dbd5c-3a6a-4392-bfe1-042452793a50/schedule/timeCards/3895809b-a618-4c0d-86a0-d42b25b7d74f
```

# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/timecard-delete-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/timecard-delete-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/timecard-delete-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/timecard-delete-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PHP](#tab/php)
[!INCLUDE [sample-code](../includes/snippets/php/timecard-delete-php-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PowerShell](#tab/powershell)
[!INCLUDE [sample-code](../includes/snippets/powershell/timecard-delete-powershell-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

### Response

The following is an example of the response. 

<!-- {
  "blockType": "response",
  "truncated": true
} -->

```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Delete timeCard",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
