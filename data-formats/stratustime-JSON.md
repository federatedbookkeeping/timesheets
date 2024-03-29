### Based on [startustime API](https://stratustime.centralservers.com/service/home/library/)

### URI explorer: GetUserSchedule

Gets a results list of users schedules and schedule details

Url: `https://stratustime.centralservers.com/service/ws-json/2.0/GetUserSchedule`

Request

```
{
	"AuthToken":"String content",
	"StartDate":"\/Date(928149600000+0000)\/",
	"EndDate":"\/Date(928149600000+0000)\/",
	"DateTimeSchema":0,
	"DataAction":{
		"Name":"String content",
		"Values":["String content"]
	}
}

```

Response

```
{
	"Report":{
		"APIVersion":"String content",
		"ProcessTime":"String content",
		"RequestTime":"\/Date(928149600000+0000)\/",
		"ResponseTime":"\/Date(928149600000+0000)\/",
		"Results":2147483647
	},
	"Results":[{
		"ID":2147483647,
		"EmpIdentifier":"String content",
		"EndDateTime":"\/Date(928149600000+0000)\/",
		"EndDateTimeSchema":"String content",
		"IsAutoGenerated":true,
		"PayTypeID":2147483647,
		"StartDateTime":"\/Date(928149600000+0000)\/",
		"StartDateTimeSchema":"String content",
		"LL01ID":2147483647,
		"LL02ID":2147483647,
		"LL03ID":2147483647,
		"LL04ID":2147483647,
		"LL05ID":2147483647,
		"LL06ID":2147483647,
		"LL07ID":2147483647,
		"LL08ID":2147483647,
		"LL09ID":2147483647,
		"LL10ID":2147483647,
		"LL11ID":2147483647,
		"LL12ID":2147483647,
		"LL13ID":2147483647,
		"LL14ID":2147483647,
		"LL15ID":2147483647,
		"Detail":[{
			"ID":2147483647,
			"ParentID":2147483647,
			"EndDateTime":"\/Date(928149600000+0000)\/",
			"EndDateTimeSchema":"String content",
			"IsAutoGenerated":true,
			"PayTypeID":2147483647,
			"StartDateTime":"\/Date(928149600000+0000)\/",
			"StartDateTimeSchema":"String content",
			"LL01ID":2147483647,
			"LL02ID":2147483647,
			"LL03ID":2147483647,
			"LL04ID":2147483647,
			"LL05ID":2147483647,
			"LL06ID":2147483647,
			"LL07ID":2147483647,
			"LL08ID":2147483647,
			"LL09ID":2147483647,
			"LL10ID":2147483647,
			"LL11ID":2147483647,
			"LL12ID":2147483647,
			"LL13ID":2147483647,
			"LL14ID":2147483647,
			"LL15ID":2147483647
		}]
	}]
}
```
## URI Exploler: UpdateUserSchedule


### Based on [startustime API](https://stratustime.centralservers.com/service/home/library/)

Request

```
{
	"AuthToken":"String content",
	"AutoAdd":true,
	"Payload":[{
		"EmpIdentifier":"String content",
		"EnableHomeLaborLevelAssignment":true,
		"EndDateTime":"\/Date(928149600000+0000)\/",
		"PayTypeID":2147483647,
		"StartDateTime":"\/Date(928149600000+0000)\/",
		"LL01ID":2147483647,
		"LL02ID":2147483647,
		"LL03ID":2147483647,
		"LL04ID":2147483647,
		"LL05ID":2147483647,
		"LL06ID":2147483647,
		"LL07ID":2147483647,
		"LL08ID":2147483647,
		"LL09ID":2147483647,
		"LL10ID":2147483647,
		"LL11ID":2147483647,
		"LL12ID":2147483647,
		"LL13ID":2147483647,
		"LL14ID":2147483647,
		"LL15ID":2147483647,
		"ID":2147483647
	}]
}
```

Response

```
{
	"Report":{
		"APIVersion":"String content",
		"ProcessTime":"String content",
		"RequestTime":"\/Date(928149600000+0000)\/",
		"ResponseTime":"\/Date(928149600000+0000)\/",
		"Results":2147483647
	},
	"Results":[{
		"ID":2147483647,
		"Messages":["String content"],
		"Status":0
	}]
