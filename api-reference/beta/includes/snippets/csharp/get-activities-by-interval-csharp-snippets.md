---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

var graphClient = new GraphServiceClient(requestAdapter);

var result = await graphClient.Drives["{drive-id}"].Items["{driveItem-id}"].GetActivitiesByIntervalWithStartDateTimeWithEndDateTimeWithInterval("{endDateTime}","{interval}","{startDateTime}").GetAsync();


```