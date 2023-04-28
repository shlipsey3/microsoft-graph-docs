---
title: "reports: getGroupArchivedPrintJobs"
description: Get a list of archived print jobs for a particular group.
author: braedenp-msft
ms.localizationpriority: medium
ms.prod: cloud-printing
doc_type: apiPageType
---

# reports: getGroupArchivedPrintJobs

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of archived print jobs for a particular group.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

In addition to the following permissions, the user's tenant must have an active Universal Print subscription.

<!-- { "blockType": "permissions", "name": "reports_getgrouparchivedprintjobs" } -->
[!INCLUDE [permissions-table](../includes/permissions/reports-getgrouparchivedprintjobs-permissions.md)]

## HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /print/reports/getGroupArchivedPrintJobs(groupId=groupId-value,startDateTime=startDateTime-value,endDateTime=endDateTime-value)
GET /reports/getGroupArchivedPrintJobs(groupId=groupId-value,startDateTime=startDateTime-value,endDateTime=endDateTime-value)
```
## Request headers
| Name          | Description   |
|:--------------|:--------------|
| Authorization | Bearer {token}. Required. |

## Function parameters

In the request URL, provide the following function parameters with values:

| Parameter     | Type                 | Required? | Description                                                          |
|---------------|----------------------|-----------|----------------------------------------------------------------------|
| `groupId`     | `Edm.String`         | Yes       | The ID of the group to return data for.                              |
| `startDateTime` | `Edm.DateTimeOffset` | No        | The start date (inclusive) for the time period to include data from.|
| `endDateTime`   | `Edm.DateTimeOffset` | No        | The end date (inclusive) for the time period to include data from.|

>**Note:** If a value is not required, pass the parameter with null value.
## Response
If successful, this method returns a `200 OK` response code and a collection of [archivedPrintJob](../resources/archivedprintjob.md) objects in the response body.

## Example
The following example shows how to call this API.
##### Request
The following is an example of the request.

<!-- {
  "blockType": "request",
  "name": "reports-getgrouparchivedprintjobs",
  "sampleKeys": ["016b5565-3bbf-4067-b9ff-4d68167eb1a6"]
}-->
```msgraph-interactive
GET https://graph.microsoft.com/beta/print/reports/getGroupArchivedPrintJobs(groupId='016b5565-3bbf-4067-b9ff-4d68167eb1a6',startDateTime=2021-05-24,endDateTime=2021-05-25)
```

##### Response
The following is an example of the response.
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.archivedPrintJob"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "id": "016b5565-3bbf-4067-b9ff-4d68167eb1a6",
      "printer": {
        "id": "016b5565-3bbf-4067-b9ff-4d68167eb1a6"
      },
      "createdBy": {},
      "processingState": "completed"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "printJob: getGroupArchivedPrintJobs",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

