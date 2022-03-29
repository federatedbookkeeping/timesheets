Adding new and modifying current time entries. Event ID is mandatory for new time entries. Adding "return_data" parameter will control if object data will be returned with successful request. You can only modify invoice_line_id value on time entries related to calendar events. Use the calendar API to modify the event itself if you need to change anything else

Modify
Request URL:

`https://#companyname#.scoro.com/api/v2/timeEntries/modify/(#id)`

Example request body:

```
{
    "lang": "eng",
    "company_account_id": "tutorial",
    "request": {
        "event_id": "1"
    }
}

```.


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
        "user_id": 1,
        "activity_id": 0,
        "invoice_line_id": 0,
        "event_id": 1,
        "event_type": "task",
        "calendar_event_id": 0,
        "time_entry_type": "task",
        "start_datetime": "2016-03-25T15:47:20+02:00",
        "duration": "00:30:00",
        "billable_duration": "00:25:00",
        "is_completed": 1,
        "completed_datetime": "2016-03-25T15:47:20+02:00",
        "is_deleted": 0
    }
}
```

