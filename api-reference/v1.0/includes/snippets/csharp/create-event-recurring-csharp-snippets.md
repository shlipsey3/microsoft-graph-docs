---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

var graphClient = new GraphServiceClient(requestAdapter);

var requestBody = new Event
{
	Subject = "Let's go for lunch",
	Body = new ItemBody
	{
		ContentType = BodyType.Html,
		Content = "Does noon time work for you?",
	},
	Start = new DateTimeTimeZone
	{
		DateTime = "2017-09-04T12:00:00",
		TimeZone = "Pacific Standard Time",
	},
	End = new DateTimeTimeZone
	{
		DateTime = "2017-09-04T14:00:00",
		TimeZone = "Pacific Standard Time",
	},
	Recurrence = new PatternedRecurrence
	{
		Pattern = new RecurrencePattern
		{
			Type = RecurrencePatternType.Weekly,
			Interval = 1,
			DaysOfWeek = new List<DayOfWeekObject?>
			{
				DayOfWeekObject.Monday,
			},
		},
		Range = new RecurrenceRange
		{
			Type = RecurrenceRangeType.EndDate,
			StartDate = new Date(DateTime.Parse("2017-09-04")),
			EndDate = new Date(DateTime.Parse("2017-12-31")),
		},
	},
	Location = new Location
	{
		DisplayName = "Harry's Bar",
	},
	Attendees = new List<Attendee>
	{
		new Attendee
		{
			EmailAddress = new EmailAddress
			{
				Address = "AdeleV@contoso.onmicrosoft.com",
				Name = "Adele Vance",
			},
			Type = AttendeeType.Required,
		},
	},
	AllowNewTimeProposals = true,
};
var result = await graphClient.Me.Events.PostAsync(requestBody);


```