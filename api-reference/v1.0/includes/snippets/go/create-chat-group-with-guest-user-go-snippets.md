---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-sdk-go/models"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphmodels.NewChat()
chatType := graphmodels.GROUP_CHATTYPE 
requestBody.SetChatType(&chatType) 
topic := "Group chat title"
requestBody.SetTopic(&topic) 


conversationMember := graphmodels.NewConversationMember()
roles := []string {
	"owner",

}
conversationMember.SetRoles(roles)
additionalData := map[string]interface{}{
	"odataBind" : "https://graph.microsoft.com/v1.0/users('8c0a1a67-50ce-4114-bb6c-da9c5dbcf6ca')", 
}
conversationMember.SetAdditionalData(additionalData)
conversationMember1 := graphmodels.NewConversationMember()
roles := []string {
	"owner",

}
conversationMember1.SetRoles(roles)
additionalData := map[string]interface{}{
	"odataBind" : "https://graph.microsoft.com/v1.0/users('82fe7758-5bb3-4f0d-a43f-e555fd399c6f')", 
}
conversationMember1.SetAdditionalData(additionalData)
conversationMember2 := graphmodels.NewConversationMember()
roles := []string {
	"guest",

}
conversationMember2.SetRoles(roles)
additionalData := map[string]interface{}{
	"odataBind" : "https://graph.microsoft.com/v1.0/users('8ba98gf6-7fc2-4eb2-c7f2-aef9f21fd98g')", 
}
conversationMember2.SetAdditionalData(additionalData)

members := []graphmodels.ConversationMemberable {
	conversationMember,
	conversationMember1,
	conversationMember2,

}
requestBody.SetMembers(members)

result, err := graphClient.Chats().Post(context.Background(), requestBody, nil)


```