---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

var graphClient = new GraphServiceClient(requestAdapter);

var requestBody = new Microsoft.Graph.Models.ReferenceCreate
{
	OdataId = "https://graph.microsoft.com/v1.0/directoryObjects/{id}",
};
await graphClient.Groups["{group-id}"].Members.Ref.PostAsync(requestBody);


```