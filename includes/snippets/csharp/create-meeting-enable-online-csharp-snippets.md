---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

var graphClient = new GraphServiceClient(requestAdapter);

var requestBody = new Event
{
	Subject = "Prep for customer meeting",
	Body = new ItemBody
	{
		ContentType = BodyType.Html,
		Content = "Does this time work for you?",
	},
	Start = new DateTimeTimeZone
	{
		DateTime = "2019-11-20T13:00:00",
		TimeZone = "Pacific Standard Time",
	},
	End = new DateTimeTimeZone
	{
		DateTime = "2019-11-20T14:00:00",
		TimeZone = "Pacific Standard Time",
	},
	Location = new Location
	{
		DisplayName = "Cordova conference room",
	},
	Attendees = new List<Attendee>
	{
		new Attendee
		{
			EmailAddress = new EmailAddress
			{
				Address = "AdeleV@contoso.OnMicrosoft.com",
				Name = "Adele Vance",
			},
			Type = AttendeeType.Required,
		},
	},
	AllowNewTimeProposals = true,
	IsOnlineMeeting = true,
	OnlineMeetingProvider = OnlineMeetingProviderType.TeamsForBusiness,
};
var result = await graphClient.Me.Events.PostAsync(requestBody, (requestConfiguration) =>
{
	requestConfiguration.Headers.Add("Prefer", "outlook.timezone=\"Pacific Standard Time\"");
});


```