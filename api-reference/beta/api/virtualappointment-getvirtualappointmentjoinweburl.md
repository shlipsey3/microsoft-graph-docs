---
title: "virtualAppointment: getVirtualAppointmentJoinWebUrl"
description: "Get a virtual appointment join link."
author: "benmicrosoft"
ms.localizationpriority: medium
ms.prod: "cloud-communications"
doc_type: apiPageType
---

# virtualAppointment: getVirtualAppointmentJoinWebUrl

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a join web URL for [Microsoft Virtual Appointments](/microsoft-365/frontline/virtual-appointments). This web URL includes enhanced business-to-customer experiences such as mobile broswer join and virtual lobby rooms.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "virtualappointment_getvirtualappointmentjoinweburl" } -->
[!INCLUDE [permissions-table](../includes/permissions/virtualappointment-getvirtualappointmentjoinweburl-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /me/onlineMeetings/{onlineMeetingId}/getVirtualAppointmentJoinWebUrl
GET /users/{userId}/onlineMeetings/{onlineMeetingId}/getVirtualAppointmentJoinWebUrl
```

## Request headers

| Name            | Description               |
| :-------------- | :------------------------ |
| Authorization   | Bearer {token}. Required. |
| Accept-Language | Language. Optional.       |

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a String in the response body. The **value** field represents the join web URL for [Microsoft Virtual Appointments](https://learn.microsoft.com/microsoft-365/frontline/virtual-appointments).

## Examples

### Request
The following is an example of a request.

# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_virtualappointment_getVirtualAppointmentJoinWebUrl",
  "sampleKeys": ["MSpkYzE3Njc0Yy04MWQ5LTRhZGItYmZi"]
}
-->
``` http
GET https://graph.microsoft.com/beta/me/onlineMeetings/MSpkYzE3Njc0Yy04MWQ5LTRhZGItYmZi/getVirtualAppointmentJoinWebUrl
```

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/get-virtualappointment-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-virtualappointment-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

### Response
The following example shows the response.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.virtualAppointment"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{ "value": "https://visit.teams.microsoft.com/webrtc-svc/api/route?tid=a796be92-&convId=19:meeting_=True" }
```
