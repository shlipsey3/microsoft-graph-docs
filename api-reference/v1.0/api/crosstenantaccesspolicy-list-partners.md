---
title: "List partners"
description: "Get a list of all partner configurations within a cross-tenant access policy."
author: "jkdouglas"
ms.localizationpriority: medium
ms.prod: "identity-and-sign-in"
doc_type: apiPageType
---

# List partners

Namespace: microsoft.graph

Get a list of all partner configurations within a cross-tenant access policy.

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "crosstenantaccesspolicy_list_partners" } -->
[!INCLUDE [permissions-table](../includes/permissions/crosstenantaccesspolicy-list-partners-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->

``` http
GET /policies/crossTenantAccessPolicy/partners
```

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a collection of [crossTenantAccessPolicyConfigurationPartner](../resources/crosstenantaccesspolicyconfigurationpartner.md) objects in the response body.

## Examples

### Request


# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "list_crosstenantaccesspolicyconfigurationpartner"
}
-->

``` http
GET https://graph.microsoft.com/v1.0/policies/crossTenantAccessPolicy/partners
```

# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/list-crosstenantaccesspolicyconfigurationpartner-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/list-crosstenantaccesspolicyconfigurationpartner-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/list-crosstenantaccesspolicyconfigurationpartner-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/list-crosstenantaccesspolicyconfigurationpartner-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PHP](#tab/php)
[!INCLUDE [sample-code](../includes/snippets/php/list-crosstenantaccesspolicyconfigurationpartner-php-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PowerShell](#tab/powershell)
[!INCLUDE [sample-code](../includes/snippets/powershell/list-crosstenantaccesspolicyconfigurationpartner-powershell-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

### Response

>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.crossTenantAccessPolicyConfigurationPartner)"
}
-->

``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "tenantId": "123f4846-ba00-4fd7-ba43-dac1f8f63013",
      "inboundTrust": null,
      "b2bCollaborationInbound": null,
      "b2bCollaborationOutbound": null,
      "b2bDirectConnectOutbound": null,
      "b2bDirectConnectInbound":
      {
        "usersAndGroups": 
        {
          "accessType": "allowed",
          "targets": [
            {
              "target": "AllUsers",
              "targetType": "user"
            }
          ]
        },
        "applications":
        {
          "accessType": "allowed",
          "targets": [
            {
              "target": "Office365",
              "targetType": "application"
            }
          ]
        }
      }
    }
  ]
}
```
