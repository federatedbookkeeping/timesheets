## Glossary

| Name | Type | Description | Example |  
| ---- | ---- | ---- | ---- |
|<ul><li>User name</li><li>Name</li><li>name</li><li>Email</li></ul> | String | Username | Test user, alex.malikov94@gmail.com |
|<ul><li>Employee ID</li><li>Results.EmpIdenitfier</li></ul>| <ul><li>Integer</li><li>String</li></ul> | Unique Employee ID | 1 |
|<ul><li>data.user.id</li><li>userUid</li><li>id</li> </ul> | <ul><li>Integer</li><li>String</li></ul> | Unique User ID | 1 |
| <ul><li>activityStartDate[ms]</li><li>activityStartDate</li><li>Start time</li><li>Start date</li><li>start</li><li>data.start_datetime</li><li> Results.StartDateTime</li></ul> | <ul><li>Integer</li><li>YYYY-MM:DD HH:MM:SS </li><li>Datetime (DATE_ISO8601 - Y-m-d\TH:i:sP)</li><li> Day Month DD HH:MM:SS GMT YY </li><ul> | Time when the task started | <ul><li> 1648217938740 </li><li>2022-03-18 09:39:19</li><li>2017-03-13T18:00:00+02:00</li><li> Fri Mar 25 15:09:38 GMT+01:00 2022 </li></ul>  |
|<ul><li>activityEndDate[ms]</li><li>activityEndDate</li><li>End date</li><li>End time</li><li>end</li><li>end_datetime</li><li>Results.EndDateTime </li></ul> | <ul><li>Integer</li><li>YYYY-MM:DD HH:MM:SS </li><li>Datetime (DATE_ISO8601 - Y-m-d\TH:i:sP)</li><li> Day Month DD HH:MM:SS GMT YY </li><ul>  | Time when the task ended | <ul><li> 1648217938740 </li><li>2022-03-18 09:40:00</li><li>2017-03-13T18:00:00+03:00</li><li> Fri Mar 25 15:09:38 GMT+01:00 2022 </li></ul>  |
| <ul><li><activityDuration[ms]/li><li>activityDuration</li><li>Duration</li><li>data.duration </li><li>Time</li></ul> | <ul><li>Integer(seconds)</li><li>Integer(minutes)</li><li>Time (HH:ii:ss) </li></ul> | Task's duration |  <ul><li>563947</li><li>10 min</li><li> 05:00:00 </li></ul> |
| data.billable_duration |Time (HH:ii:ss) | Billable duration of the actvity/task/project |  01:00:00   |
| <ul><li>activityName</li><li>Project name</li><li>Project</li><li> data.title</li><ul> | String | Project to work on  | Prejournal |
| data.activity_id | Integer | Unique activity/task/project  ID | 1 |  
| <ul><li>activityCategoryName</li><li>data.time_entry_type</li></ul> | String | The type of the activity | Professional |
| <ul><li>Comment</li><li>note</li><li>details</li><li>data.description</li></ul> | String | Comment about the current activity | Last task for today |
| <ul><li>Task</li><li>Issue</li><ul> | String  | Task to accomplish(A project includes many tasks) | Update database  |
| <ul><li>Status</li><li>data.is_completed</li></ul> | <ul><li>String</li><li>Integer</li></ul>  | Checks the situation of the task/project(in progress or not) | Unresolved |  
| data.completed_datetime |  Datetime (DATE_ISO8601 - Y-m-d\TH:i:sP)  | When the task completed | 2017-03-13T18:00:00+02:00 |
| data.is.deleted | Integer | Checks if the project has been deleted  | 0 |
| data_deleted_date | Datetime (DATE_ISO8601 - Y-m-d\TH:i:sP)| Deletion time | 2017-03-13T18:00    :00+02:00|
| Client | String | The Client of the Project | PonderSource |
| data.time_entry_id | Integer | Unique time entry ID | 1 |
|data.is_confirmed  | Integer | Checks if the timesheet has been confirmed | 1 |
|data.invoice_line_id | Integer | Related invoice line ID |  0 |
| data.event_id | Integer | Related event ID |  1 |
| data.event_type | String | Event type, task or cal. |  Task |
| data.time_entry_type | String | Time entry type, task or cal. |  Task |
| User Group | String | We can have a multiple user that will be in group | Test |

