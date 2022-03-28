## [Sage HR](https://sage.hr/)

[Sage HR API-Timesheets](https://sagehr.docs.apiary.io/#reference/timesheets)

`POST https://private-anon-35f92daa31-sagehr.apiary-mock.com/api/timesheets/clock-in`

Headers:
```
  "Content-Type: application/json",
  "Accept: application/json",
  "X-Auth-Token: "
```

Body: 

```

{
  "override": "",
  "clocked_time": {
    "YYYY/MM/DD": {
      "employee_id": [
        {
          "clock_in": "",
          "clock_out": ""
        }
      ]
    }  
  }
}

```

Times on specific dates for specific employees as json

* override: string
        -'true' if override provided days clocked entries
* clocked_time: object

