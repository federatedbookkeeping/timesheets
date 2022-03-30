
### List all time entries

List all time entries of all users, sorted by  `date_at`.  _Time trackers_  can only access their own entries.

```
GET /time_entries.json
```

#### Parameters

`user_id`

Filters the list by user. Can be either a single ID,  `current`  for the authenticated user, or multiple comma-separated IDs.

`customer_id`

Filters the list by customer. Can be either a single ID, or multiple comma-separated IDs.

`project_id`

Filters the list by project. Can be either a single ID, or multiple comma-separated IDs.

`service_id`

Filters the list by service. Can be either a single ID, or multiple comma-separated IDs.

`note`

Search within the notes. To filter by multiple criteria connected with OR, set the parameter as  `note[]`  multiple times.

`at`

The date of the entry.  
`today`,  `yesterday`,  `this_week`,  `last_week`,  `this_month`,  `last_month`,  `this_year`,  `last_year`  or date formatted as  `YYYY-MM-DD`

`from,to`

The date span the time entry falls into – both attributes can be formatted like  `at`.

`billable`

Is the time entry billable or not?  
`true`  or  `false`

`locked`

Is the time entry locked or not?  
`true`  or  `false`

`tracking`

Is a timer running on the time entry?  
`true`  or  `false`

`sort`

What to sort results by. Can be either  `date`,  `user`,  `customer`,  `project`,  `service`,  `note`,  `minutes`, or  `revenue`.  
Default:  `date`

`direction`

The direction of the sort. Can be either  `asc`  or  `desc`.  
Default: depends on  `sort`:  `date`,  `minutes`, and  `revenue`  default to  `desc`, all others to  `asc`.

`group_by`

What to group results by.  [Details](https://mite.yo.lk/en/api/time-entries.html#list-grouped)

`limit`

Limits the list to the given number of entries.  
Default:  _indefinite_

`page`

Allows to access follow-up pages when combined with  `limit`.  
Default:  `1`

#### Response

```
Status: 200 OK
```

```
[
   {
      "time_entry": {
		  "id": 36159117,
	      "minutes": 15,
	      "date_at": "2015-10-16",
	      "note": "Rework description of authentication process",
	      "billable": true,
	      "locked": false,
	      "revenue": null,
	      "hourly_rate": 0,
	      "user_id": 211,
	      "user_name": "Noah Scott",
	      "project_id": 88309,
	      "project_name": "API Docs",
	      "customer_id": 3213,
	      "customer_name": "King Inc.",
	      "service_id": 12984,
	      "service_name": "Writing",
	      "created_at": "2015-10-16T12:39:00+02:00",
	      "updated_at": "2015-10-16T12:39:00+02:00"
      }
   },
   {
      "time_entry": {...}
   }
]
```
