---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-beta-sdk-go/models"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphmodels.NewWebAccount()
webUrl := "https://github.com/innocenty.popov"
requestBody.SetWebUrl(&webUrl) 

result, err := graphClient.Me().Profile().WebAccounts().ByWebAccountId("webAccount-id").Patch(context.Background(), requestBody, nil)


```