This API endpoint supports requests authenticated by either user_token or apiKey.

View time entry:

Request URL:`https://#companyname#.scoro.com/api/v2/timeEntries/view/(#id)`

Example request body:

```
{
    "lang": "eng",
    "company_account_id": "tutorial",
    "request": {}
}

```

Example response body:

```
{
    "status": "OK",
    "statusCode": 200,
    "messages": null,
    "data": {
        "time_entry_id": 1,
        "description": "",
        "title": "",
        "user_id": 3,
        "activity_id": 0,
        "invoice_line_id": 0,
        "event_id": 48,
        "event_type": "task",
        "calendar_event_id": 0,
        "time_entry_type": "task",
        "start_datetime": "2010-03-16T11:00:00+02:00",
        "duration": "01:30:00",
        "billable_duration": "00:00:00",
        "is_completed": 0,
        "is_confirmed": 0,
        "is_billable": 0,
        "completed_datetime": null,
        "is_deleted": 0,
        "deleted_date": null
    }
}
```

| Name                | Type                                      | Description                                                                                                                                          |
| ------------------- | ----------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
|  |
| time\_entry\_id     | Integer                                   | Time entry ID.                                                                                                                                       |
| description         | String                                    | Description.                                                                                                                                         |
| title               | String                                    | Time Entry title. It will be constructed dynamically based on description and activity id values.                                                    |
| user\_id            | Integer                                   | Related user ID.                                                                                                                                     |
| activity\_id        | Integer                                   | Related activity ID.                                                                                                                                 |
| invoice\_line\_id   | Integer                                   | Related invoice line ID.                                                                                                                             |
| event\_id           | Integer                                   | Related event ID.                                                                                                                                    |
| event\_type         | String                                    | Event type, task or cal.                                                                                                                             |
| calendar\_event\_id | Integer                                   | Calendar event id for consolidated time entry.                                                                                                       |
| time\_entry\_type   | String                                    | Time entry type, task or cal.                                                                                                                        |
| start\_datetime     | Datetime (DATE\_ISO8601 - Y-m-d\\TH:i:sP) | Planned start date and time.                                                                                                                         |
| end\_datetime       | Datetime (DATE\_ISO8601 - Y-m-d\\TH:i:sP) | Planned end date and time.                                                                                                                           |
| duration            | Time (HH:ii:ss)                           | Time entry duration. Rounded to the nearest minute.                                                                                                  |
| billable\_duration  | Time (HH:ii:ss)                           | Billable duration for time entry. Only used if site has billable hours feature activated. Rounded to the nearest minute.                             |
| is\_completed       | Boolean                                   | Is the time entry completed or not.                                                                                                                  |
| is\_confirmed       | Boolean                                   | Is the time entry confirmed or not.                                                                                                                  |
| is\_billable        | Boolean                                   | Is the time entry billable or not.                                                                                                                   |
| completed\_datetime | Datetime (DATE\_ISO8601 - Y-m-d\\TH:i:sP) | Date and time when the time entry was completed. Will be set to current time, if time entry is completed and no datetime provided.                   |
| is\_locked          | Boolean                                   | Is the time entry locked or not. The parameter is available only if the ["Use time locking" setting](https://help.scoro.com/manuals/383) is enabled. |
| permissions         | Array                                     | Object user permissions. Used only for user based API                                                                                                |
| modified\_date      | Datetime (DATE\_ISO8601 - Y-m-d\\TH:i:sP) | Date and time when the time entry was modified. If a new time entry is added - it will be set to the current time (created\_date).                   |
| is\_deleted         | Boolean                                   | Is deleted. Use 'include\_deleted = 1' in [request object](https://api.scoro.com/api/#filters) to get deleted objects to response as well.           |
| deleted\_date       | Datetime (DATE\_ISO8601 - Y-m-d\\TH:i:sP) | The date when object was deleted.                                                                                                                    |
