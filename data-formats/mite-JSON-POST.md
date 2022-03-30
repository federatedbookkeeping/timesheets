
### Create a time entry

Create a new time entry. All attributes are optional.

```
POST /time_entries.json
```

#### Attributes

`date_at`

Date of the time entry formatted as  `YYYY-MM-DD`.  
Default:  _today_

`minutes`

Default:  `0`

`note`

Default:  `""`  (empty string)

`user_id`

Can only be set by an  _administrator_.  
Default:  _ID of the authenticated user_

`project_id`

Default:  `null`  (without a project)

`service_id`

Default:  `null`  (without a service)

`locked`

Can only be set by an  _administrator_. A locked entry can not be modified or deleted.  [Details](https://mite.yo.lk/en/api/time-entries.html#locked-entries)  
`false`  (Default) or  `true`

#### Request

```
Content-Type: application/json
```

```
{
   "time_entry": {
      "date_at": "2015-9-15",
      "minutes": 185,
      "service_id": 243
   }
}
```

#### Response

```
Status: 201 Created
Location: https://demo.mite.yo.lk/time_entries/52324.json
```

```
{
   "time_entry": {
      "id": 52324,
      "minutes": 185,
      "date_at": "2015-9-12",
      "note": "",
      "billable": true,
      "locked": false,
      "revenue": null,
      "hourly_rate": 0,
      "user_id": 211,
      "user_name": "Noah Scott",
      "project_id": null,
      "service_id": 243,
      "service_name": "Documentation",
      "created_at": "2015-09-13T18:54:45+02:00",
      "updated_at": "2015-09-13T18:54:45+02:00"
   }
}
```
