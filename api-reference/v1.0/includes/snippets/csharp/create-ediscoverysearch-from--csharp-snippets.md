---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

var graphClient = new GraphServiceClient(requestAdapter);

var requestBody = new Microsoft.Graph.Models.Security.EdiscoverySearch
{
	DisplayName = "My search 2",
	Description = "My first search",
	ContentQuery = "(Author=\"edison\")",
	AdditionalData = new Dictionary<string, object>
	{
		{
			"custodianSources@odata.bind" , new List<string>
			{
				"https://graph.microsoft.com/v1.0/security/cases/ediscoveryCases/b0073e4e-4184-41c6-9eb7-8c8cc3e2288b/custodians/0053a61a3b6c42738f7606791716a22a/userSources/43434642-3137-3138-3432-374142313639",
				"https://graph.microsoft.com/v1.0/security/cases/ediscoveryCases/b0073e4e-4184-41c6-9eb7-8c8cc3e2288b/custodians/0053a61a3b6c42738f7606791716a22a/siteSources/169718e3-a8df-449d-bef4-ee09fe1ddc5d",
				"https://graph.microsoft.com/v1.0/security/cases/ediscoveryCases('b0073e4e-4184-41c6-9eb7-8c8cc3e2288b')/custodians('0053a61a3b6c42738f7606791716a22a')/unifiedGroupSources('32e14fa4-3106-4bd2-a245-34bf0c718a7e')",
			}
		},
		{
			"noncustodialSources@odata.bind" , new List<string>
			{
				"https://graph.microsoft.com/v1.0/security/cases/ediscoveryCases/b0073e4e-4184-41c6-9eb7-8c8cc3e2288b/noncustodialdatasources/35393639323133394345384344303043",
			}
		},
	},
};
var result = await graphClient.Security.Cases.EdiscoveryCases["{ediscoveryCase-id}"].Searches.PostAsync(requestBody);


```