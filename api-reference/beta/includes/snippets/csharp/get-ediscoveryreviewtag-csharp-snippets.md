---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

var graphClient = new GraphServiceClient(requestAdapter);

var result = await graphClient.Security.Cases.EdiscoveryCases["{ediscoveryCase-id}"].Tags["{ediscoveryReviewTag-id}"].GetAsync();


```