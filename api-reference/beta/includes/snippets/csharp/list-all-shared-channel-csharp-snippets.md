---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

var graphClient = new GraphServiceClient(requestAdapter);

var result = await graphClient.Teams["{team-id}"].AllChannels.GetAsync((requestConfiguration) =>
{
	requestConfiguration.QueryParameters.Filter = "membershipType eq 'shared'";
});


```