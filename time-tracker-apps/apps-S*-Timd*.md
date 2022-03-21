# [Time trackers S*-Timd*](https://github.com/federatedbookkeeping/timesheets/blame/b017c0c/apps-list.md#L150-L180)

First round of filtering. We also need to: 

* Find out all the import/export data formats.
* Fill the 'Data from multiplie collaborators'  fields


| App| Description | Tracker | Data export | Data import | Data from multiplie collaborators | Open Source | Price(US$/month) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| [Saas-Timetracker](https://github.com/federatedbookkeeping/timesheets/new/main#saas-timetracker-%EF%B8%8F) | Rails Software(server-side web application framework) as a Service Application for time tracking| ✔️  | ❌ | ❌ | -  |  ✔️   | Free |
| [Sage HR](https://github.com/federatedbookkeeping/timesheets/new/main#sage-hr-%EF%B8%8F) | A simple, easy to use interface to adjust hours worked & submit a timesheet for approval to a manager | ✔️  | ✔️  | ✔️  | - | ❌  | [7$/employee](https://sage.hr/pricing) |
| [Samay](https://github.com/federatedbookkeeping/timesheets/new/main#samay-%EF%B8%8F) | Command line Time tracking and reporting | ✔️  | ✔️  | ✔️  | - | ✔️   | Free |
| [SAP Fieldglass](https://github.com/federatedbookkeeping/timesheets/new/main#sap-fieldglass-%EF%B8%8F) | Cloud-based Vendor Management System (VMS) | ✔️  | JSON/CSV |  JSON/CSV | - |  ❌  | Free(too good to be true) |
| [Savemytime](https://github.com/federatedbookkeeping/timesheets/new/main#savemytime) | Mobile timetracker  | ✔️  |  CSV export (proffesional 3$) | ❌(?) | - | ❌ | 0-3$ |
| [Scoro](https://github.com/federatedbookkeeping/timesheets/new/main#scoro-%EF%B8%8F) | Software as a Service (SaaS)| ✔️  |  HTTP/JSON |  HTTP/JSON  | -  | ❌ | [19$-49$+](https://www.scoro.com/pricing/) |
| [SimpleTimeTracker-Razeeman](https://github.com/federatedbookkeeping/timesheets/new/main#simple-time-tracker-razeeman-%EF%B8%8F) | Time tracker app | ✔️  | CSV | - | - | ✔️  | Free |
| [Simple TimeTracker with Notion](https://github.com/federatedbookkeeping/timesheets/new/main#simple-time-tracker-minhyeok-lee-with-notion-integration-%EF%B8%8F) | IOS app time tracker | ✔️  | ❌ |  ❌ |  - |  ❌ | Free |
| [SINC](https://github.com/federatedbookkeeping/timesheets/new/main#sinc-%EF%B8%8F) | Timecard And Location Tracking App | ✔️   | PDF/Excel(the excel file can be opened and saved as a CSV file) |  ❌ | - | ❌ | 0-50$ | 
| [Smarter Time](https://github.com/federatedbookkeeping/timesheets/new/main#smarter-time-%EF%B8%8F) | Time tracker app for iOS,Web and  Android | ✔️  | CSV | - | - | ❌ | 0-5$ | 
| [Sprint App](https://github.com/federatedbookkeeping/timesheets/new/main#sprint-app-deprecated-%EF%B8%8F) | Project management and time tracking app | ✔️  | ❌(Html response. No clear doc, conclusion made by looking the code) | - | - | ✔️  | Free |
| [Staple](https://github.com/federatedbookkeeping/timesheets/new/main#staple--%EF%B8%8F) | Staple tracker. CVPR 2017: End-To-End Representation Learning for Correlation Filter Based Tracking | ❌ | -  | -  | - | ✔️  | Free |

##  [Saas-Timetracker](https://github.com/appcasts/saas-timetracker) ⏲️

```
$ snap install ruby-bundler 
$ duble install
$ gem install simple_form 3.0.0
$ rake generate_erd
```
 
Error occurred
 
```
Could not find gem 'simple_form (~> 3.0.0)' in https://github.com/plataformatec/simple_form.git (at
master@1b3e910).
The source contains 'simple_form' at: 5.1.0

```

* Seems that is not a time tracker at all. From the db we can see that we can only store `accounts/users/projects(name,client,archived,created_at,updated_at)`
* Must have graphvis

##  [Sage HR](https://sage.hr/features/timesheets) ⏲️

A simple, easy to use interface to adjust hours worked & submit a timesheet for approval to a manager.

* The Timesheets module in Sage HR you can use to record the amount of time an employee has spent on a job for a defined time period
* The Sage HR authentication scheme uses an API key (API token). 
* By using the API we can send data about the clock in/out (Timesheets module) to Sage HR.
* We can add historical timesheets.

#### Useful links 

[Sage API](https://developer.columbus.sage.com/docs#/uk/sage200extra/accounts/gs-what-makes-up-an-api-request)
[Sage HR API](https://sagehr.docs.apiary.io/#reference) (All request are required to pass a X-Auth-Token header)
[Sage HR endpoints](https://www.merge.dev/docs/integrations/ats/sage-hr)

#### Example - Time Schedule information transfer from Sage HR to Vikarina


Endpoint: `https://subdomain.sage.hr/api/vikarina/timesheets`

Response 200 Content type:application/json

```
{
	"data": {
	"employee_id": 1,
	"employee_number": 123,
	"date": "2020-10-10",
	"stand_by": 8,
	"hours": 8.5,
	"nightours": 0.5,
	"cost_center_code": "cost center code (custom field)",
	"overtime_title": 0.5,
	"status": 1
	}
}
```

## [Samay](https://github.com/nexneo/samay) ⏲️

Command line based time tracker built with Go(programming language) and protocol buffers.

* Command line based simple interface
* Uses simple files to store data.
* Store files in Dropbox(detects dropbox folder)
* Basic reporting (monthly)

##  [SAP Fieldglass](https://www.fieldglass.com) ⏲️

* Cloud-based, open [Vendor Management System (VMS)](https://www.fieldglass.com/solutions/vendor-management-system), to manage services procurement and external workforce management programs
* Uses the OAuth 2.0 protocol to access the API.
* REST API resource allows clients to send and receive integrated data directly against the application
* Information can either upload (POST) or download (GET) data from the authenticated user, with data In/Out supported in JSON/CSV formats
* Can also PUSH data real time to the client-defined end point

" The SAP Fieldglass Supplier Contractor Access Agreement (CAA) is a legal agreement that defines the usage of and access to the SAP Fieldglass system for a Supplier. All Suppliers must have a signed CAA on file in order to access the SAP Fieldglass system."

Comment: Too much effort to create an account

#### Useful links

[SAP Fieldglass Timesheet Integration](https://www.fieldglass.com/resources/datasheets/sap-fieldglass-timesheet-integration)
[SAP FIeldglass APIs](https://api.sap.com/package/FieldglassAPI/all)

##  [Savemytime](https://savemytime.co/)

"Track all your activities no matter if they are online or offline, with no effort and need to remember to start a timer". 

Looks like an app(not for professionals) to keep track of their programm(where they spend their time( sports, work, hobbies etc)


## [Scoro](https://www.scoro.com/time-management-software/) ⏲️


"Deliver high-quality work on time by planning, scheduling and tracking your team’s time in one place. Track the hours spent on projects, analyze the results and optimize activities to improve efficiency."

* The Scoro API has a single point of entry, derived from your account URL
* All API communication is encrypted over HTTPS
* Any non-secure requests are automatically rejected

 #### Useful links 

[Scoro API](https://apitracker.io/a/scoro)
[Scoro API v2](https://api.scoro.com/api/v2)

##  [Simple Time Tracker (Razeeman)](https://play.google.com/store/apps/details?id=com.razeeman.util.simpletimetracker) ⏲️


* View previous records and statistics over time.
* Widgets, backups, notifications...
* Unit tests, UI tests
* CI with github actions
 
##  [Simple Time Tracker (Minhyeok Lee)](https://apps.apple.com/nl/app/simple-timetracker-with-notion/id1590343222) (with Notion integration) ⏲️

IOS Time tracker app. Not much info about it online. Website not found

##  [SINC](https://sinc.business/) ⏲️
 
* Mobile app+web console
* An admin can generate a detailed excel hour summary for any given period(hours worked by each staff member, overtime, and even any notes added by staff during their shifts)
* Historical data is stored in the cloud and is accessible to admins from any computer or mobile device

"Once you link an integration provider, it is simply a matter of choosing the pay period and staff to send time sheets for, and our integrations will take care of the rest, allowing your payroll software to run payroll accurate to the minute."

They have integrations with Leading Payroll Software with:

1) [Gusto](https://gusto.com/)
2) [Xero](https://www.xero.com/us/)
3) [MYOB](https://www.myob.com/au)

## [Smarter Time](https://www.smartertime.com/) ⏲️

"Web-based solution that enables time tracking through calls tracking, maps, goals tracking, weekly reporting and more."

* Devices: Web-based, iOS, Android
* COstumer types: small/medium business, enterprise

##  [Sprint App](https://github.com/macfanatic/SprintApp) (deprecated) ⏲️

"NO LONGER MAINTAINED - Project management and time tracking app(9-10 years ago)"

* Calendar View
* Time Tracking
* Repoting data
	- [Employee Timesheet](https://github.com/macfanatic/SprintApp/tree/master/app/views/employee_timesheet)
	- [Hours worked report](https://github.com/macfanatic/SprintApp/blob/master/app/views/hours_worked_report)

Looks reports are in html form.
Example: [hours_worked_report](https://github.com/macfanatic/SprintApp/blob/master/app/views/hours_worked_report/view.html.haml#L6-L10) 
```
- c = GoogleCharts::Charts::Line.new self, @comments
- c.title "Hours Worked Report: #{@start.humanize} - #{@end.humanize}"
- c.label "Date", :first
- c.value "Hours Worked", lambda { |day| day.last.values.sum.to_f.round(2) }
= raw c.to_html
```
[Deploying to Heroku](https://github.com/macfanatic/SprintApp/wiki/Deploying-to-Heroku)

## [Staple](https://github.com/bertinetto/staple)  ⏲️

Field: Computer vision

"Correlation Filter-based trackers have recently achieved excellent performance, showing great robustness to challenging situations exhibiting motion blur and illumination changes"
* Problem: track an arbitrary object selected online. 
