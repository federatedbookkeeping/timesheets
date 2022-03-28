Based on [Tick API-entries](https://github.com/tick/tick-api/blob/master/sections/entries.md)


`GET /entries/235.json` will return the specified entry:

```

[
  {
    "id":"234",
    "date":"2014-09-17",
    "hours":2.88,
    "notes":"Stocking up on Bacta.",
    "task_id":24,
    "user_id":4,
    "url":"https://www.tickspot.com/api/v2/123/entries/234.json",
    "created_at":"2014-09-18T15:03:19.000-04:00",
    "updated_at":"2014-09-18T15:03:19.000-04:00"
  },

  {
    "id":"235",
    "date":"2014-09-17",
    "hours":12,
    "notes":"Making the Kessel run.",
    "task_id":24,
    "user_id":4,
    "url":"https://www.tickspot.com/api/v2/123/entries/235.json",
    "created_at":"2014-09-18T15:03:19.000-04:00",
    "updated_at":"2014-09-18T15:03:19.000-04:00"
  }

]

```

