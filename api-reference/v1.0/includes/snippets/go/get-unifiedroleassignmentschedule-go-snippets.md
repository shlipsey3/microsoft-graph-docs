---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)



result, err := graphClient.RoleManagement().Directory().RoleAssignmentSchedules().ByRoleAssignmentScheduleId("unifiedRoleAssignmentSchedule-id").Get(context.Background(), nil)


```