---
title: "Update organization"
description: "Update the properties of a organization object."
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# Update organization

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Update the properties of a [organization](../resources/intune-onboarding-organization.md) object.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_onboarding_organization_update" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-onboarding-organization-update-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /organization/{organizationId}
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
In the request body, supply a JSON representation for the [organization](../resources/intune-onboarding-organization.md) object.

The following table shows the properties that are required when you create the [organization](../resources/intune-onboarding-organization.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|The GUID for the object.|
|mobileDeviceManagementAuthority|[mdmAuthority](../resources/intune-onboarding-mdmauthority.md)|Mobile device management authority. Possible values are: `unknown`, `intune`, `sccm`, `office365`.|
|certificateConnectorSetting|[certificateConnectorSetting](../resources/intune-onboarding-certificateconnectorsetting.md)|Certificate connector setting.|



## Response
If successful, this method returns a `200 OK` response code and an updated [organization](../resources/intune-onboarding-organization.md) object in the response body.

## Example

### Request
Here is an example of the request.
``` http
PATCH https://graph.microsoft.com/beta/organization/{organizationId}
Content-type: application/json
Content-length: 492

{
  "@odata.type": "#microsoft.graph.organization",
  "mobileDeviceManagementAuthority": "intune",
  "certificateConnectorSetting": {
    "@odata.type": "microsoft.graph.certificateConnectorSetting",
    "status": 6,
    "certExpiryTime": "2017-01-01T00:00:03.9979674-08:00",
    "enrollmentError": "Enrollment Error value",
    "lastConnectorConnectionTime": "2017-01-01T00:02:50.2393584-08:00",
    "connectorVersion": "Connector Version value",
    "lastUploadVersion": 1
  }
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 541

{
  "@odata.type": "#microsoft.graph.organization",
  "id": "9efe224a-224a-9efe-4a22-fe9e4a22fe9e",
  "mobileDeviceManagementAuthority": "intune",
  "certificateConnectorSetting": {
    "@odata.type": "microsoft.graph.certificateConnectorSetting",
    "status": 6,
    "certExpiryTime": "2017-01-01T00:00:03.9979674-08:00",
    "enrollmentError": "Enrollment Error value",
    "lastConnectorConnectionTime": "2017-01-01T00:02:50.2393584-08:00",
    "connectorVersion": "Connector Version value",
    "lastUploadVersion": 1
  }
}
```
