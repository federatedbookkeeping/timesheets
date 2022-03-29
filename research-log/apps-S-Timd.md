# [Time trackers S*-Timd*](https://github.com/federatedbookkeeping/timesheets/blame/b017c0c/apps-list.md#L150-L180)

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

Time tracker mobile App

"Track all your activities no matter if they are online or offline, with no effort and need to remember to start a timer". 


## [Scoro](https://www.scoro.com/time-management-software/) ⏲️


"Deliver high-quality work on time by planning, scheduling and tracking your team’s time in one place. Track the hours spent on projects, analyze the results and optimize activities to improve efficiency."

* The Scoro API has a single point of entry, derived from your account URL
* All API communication is encrypted over HTTPS
* Any non-secure requests are automatically rejected

 #### Useful links 

[Scoro API](https://apitracker.io/a/scoro)
[Scoro API v2](https://api.scoro.com/api/v2)

##  [Simple Time Tracker (Razeeman)](https://github.com/Razeeman/Android-SimpleTimeTracker) ⏲️


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

##  [Stratustime](https://stratustime.centralservers.com/)  ⏲️

### [FAQ for Integrating stratustime](https://www.nettimesolutions.com/blog/faq-for-integrating-stratustime/)

#### What is stratustime Web Services (STWS) API?              

Stratustime Web Services (STWS) API is designed to allow external systems to connect with the stratustime SaaS engine. stratustime can import and export data from its data store in multiple different ways including flat files, FTP, and web services. The STWS API is designed for end users to consume and send data via XML, JSON, or SOAP.

#### How does the API work?

STWS is composed of three different web service URLs. Users can use any language to interact with the STWS API as long as XML, JSON, or SOAP is the standard for sending and receiving data.

#### How do I set up Single Sign-On?

Enabling SSO can be done in a few simple steps.  When in stratustime, navigate to the configuration interface and select General. Under General, the SSO options can be found in the Web Services section. Proper permission levels in the system are required to enable SSO. When under Web Services, you can check the box to enable SSO. At this time, a “Shared Key” GUID will be issued. After you enable SSO, you can choose to have web access & SSO, or SSO log in only. If “SSO log in only” is selected, stratustime login will be disabled


[Web Services API](https://stratustime.centralservers.com/service/)

## [StreamDeck-Toggl](https://github.com/tobimori/streamdeck-toggl)  ⏲️

"Time tracking using [Elgato Stream Deck](https://www.elgato.com/en/stream-deck) and [Toggl Track](https://toggl.com/track/)"

The time tracker here is just the Toogle Tracker:) 

* Elgato Stream Deck: Live Content Creation Controller
* Toggl Track: Time tracking app that allows you to track your daily activities across different platforms
	- [What is Toggl track?](https://support.toggl.com/en/articles/2220404-what-is-toggl-track)
	- [Toggle API doc](https://github.com/toggl/toggl_api_docs)
	- Available via web application, desktop apps (Windows, Mac, Linux), browser extensions (Chrome, Firefox) and mobile apps (Android, iOS).
	- Free(most of the features) 
	- [Get Time Entries](https://github.com/toggl/toggl_api_docs/blob/master/chapters/time_entries.md)

#### Create a time entry

`POST https://api.track.toggl.com/api/v8/time_entries`

Example request

```shell
curl -v -u 1971800d4d82861d8f2c1651fea4d212:api_token \
	-H "Content-Type: application/json" \
	-d '{"time_entry":{"description":"Meeting with possible clients","tags":["billed"],"duration":1200,"start":"2013-03-05T07:58:58.000Z","pid":123,"created_with":"curl"}}' \
	-X POST https://api.track.toggl.com/api/v8/time_entries

```

Successful response
```json
{
	"data":
	{
		"id":436694100,
		"pid":123,
		"wid":777,
		"billable":false,
		"start":"2013-03-05T07:58:58.000Z",
		"duration":1200,
		"description":"Meeting with possible clients",
		"tags":["billed"]
	}
}
```
#### Get time entry details

`GET https://api.track.toggl.com/api/v8/time_entries/{time_entry_id}`

Example request:

```shell
curl -v -u 1971800d4d82861d8f2c1651fea4d212:api_token \
-X GET https://api.track.toggl.com/api/v8/time_entries/436694100
```

Successful response
```json
{
	"data":{
		"id":436694100,
		"wid":777,
		"pid":193791,
		"tid":13350500,
		"billable":false,
		"start":"2013-02-27T01:24:00+00:00",
		"stop":"2013-02-27T07:24:00+00:00",
		"duration":21600,
		"description":"Some serious work",
		"tags":["billed"],
		"at":"2013-02-27T13:49:18+00:00"
	}
}
```

## [Super Productivity](https://github.com/johannesjo/super-productivity)  ⏲️

"Todo list app with integrated Timeboxing and time tracking capabilities. Comes with integrations for Jira, Gitlab, GitHub and Open Project."

#### Issues

* [API server (preferably Dockerised) #1948](https://github.com/johannesjo/super-productivity/discussions/1948)
* [ME-Where is the API doc](https://github.com/johannesjo/super-productivity/discussions/1973)

## [swdc-vscode](https://github.com/swdotcom/swdc-vscode)  ⏲️

"Code Time is an open source plugin for automatic programming metrics and time tracking in Visual Studio Code"

(email sent to ask for available API doc)

## [Swipetimes](https://www.swipetimes.com/en/) ⏲️

• Daily/weekly backups to SD card, Google Drive or Dropbox.
• Categorisation of time entries using tags/labels.
• Invoice management and printing.



## [Syncrew](https://syncrew.com/)


* No API available.
* Direct integration with Quickbooks( we do custom data exports for other systems. Just email us at info@syncrew.com for details about what can be synced
* Data lives in the cloud
* Supports: Android, iPhone, iPad
"SYNCrew is a mobile workforce management solution which allows managers to track their work teams out in the field. The platform offers clock-in/clock-out with photo & GPS verification, time tracking, employee and team scheduling, email alerts, progress photos, customizable forms, reporting, and more.

## [Synerion](https://www.synerion.com/time-and-attendance-software/)]

* No API available
* Integrations payroll, ERP, HR software, and 100+ systems

## [TagTime](https://github.com/tagtime/TagTime)
"
To determine how you spend your time, TagTime literally randomly samples you. At random times it pops up and asks what you're doing right at that moment"

## [Task Tracker](https://www.tasktracker.in/)

* track time on your activities

* view stats for particular tasks or for all of them

*  simple extension for notification center

## [Taxi](https://github.com/sephii/taxi)

* CLI to time tracking backends

#### Usage 

 All you'll do is edit a text file and write down what you've worked on and how long, like so:

```
23/01/2014

pingpong 09:00-10:00 Play ping-pong
infra         -11:00 Repair coffee machine
```

You can then get a summary of your timesheet:

```
Staging changes :

# Thursday 23 january #
pingpong (123/456)             1.00  Play ping-pong
infra (123/42)                 1.00  Repair coffee machine
                               2.00

Total                          2.00

Use `taxi ci` to commit staging changes to the server
```

Supported backends:

* [zebra](https://github.com/sephii/taxi-zebra) : Liip's zebra backend
* [tempo](https://github.com/alexandreblin/taxi-tempo) : Atlassian JIRA's [Tempo Timesheets](https://tempo.io/) backend
* [tipee](https://github.com/alexandreblin/taxi-tipee) : Gammadia's [tipee](https://tipee.ch/)  backend
* [bexio](https://github.com/alexandreblin/taxi-bexio) : [Bexio Timesheets](https://bexio.com/) backend
* [multi](https://github.com/alexandreblin/taxi-multi) : a special backend to push entries over multiple other backends
* [clockify](https://github.com/sephii/taxi-clockify) : backend for the free timesheeting tool [clockify.me](https://clockify.me/)


Through the use of backends, Taxi allows you to push your timesheets to different systems

## [Team Timesheets](https://github.com/thdk/team-timesheets)

* Bigquery Can be set up to sync with bigquery for advanced reports.

## [Teramind](https://www.teramind.co/landing/time-tracking-software)

## [ti](https://github.com/richmeta/ti)

Small command line time-tracking application. 

#### Usage 

```
$ ti on my-project
Start working on my-project.

$ ti status
You have been working on my-project for less than a minute.

$ ti fin
So you stopped working on my-project.

```

You can also give it human-readable times:

```
$ ti on my-project 30mins ago
```

* All data is saved in a JSON file ,``~/.ti-sheet``. (This can be changed using the $SHEET_FILE environment variable.)


##  [Tie Tracker](https://github.com/peterpeterparker/tietracker)

Tie Tracker is a free and open source time tracking application

* You must have your API key available in your account
* You must also prepare your domain name in the format: `https://domain-name.freshdesk.com`


## [Tick](https://www.tickspot.com/time-tracking-app)

* Integration with Quickbooks. [More about Tick’s integration with QuickBoooks](https://www.tickspot.com/quickbooks)
* [API](https://github.com/tick/tick-api)

#### Example requests

##### GET

```
curl -H "Authorization: Token token=ApV99yzvwApV99yzvwApV99yzvwApV99yzvw" \
     -H 'User-Agent: MyCoolApp (me@example.com)' \
  https://www.tickspot.com/999999999/api/v2/projects.json
```

##### POST(JSON data)

```
curl -H "Authorization: Token token=ApV99yzvwApV99yzvwApV99yzvwApV99yzvw" \
     -H 'Content-Type: application/json' \
     -H 'User-Agent: MyCoolApp (me@example.com)' \
     -d '{ "name": "My new project!", "client_id": "999" }' \
  https://www.tickspot.com/999999999/api/v2/projects.json
```

## [Ticket Timer](https://www.freshworks.com/apps/freshdesk/ticket_timer/), [Ticket Timer Premium](https://www.freshworks.com/apps/freshdesk/ticket_timer_premium/)

Ticket Timer allows you to automatically save your time as soon as you answer a ticket.

## [Tim](https://github.com/MatthiasKauer/tim) 

* CL for recording time logs
* All aggregation is handled by [hledger](https://hledger.org/)
* tim tries to simplify [ti](https://github.com/sharat87/ti) by relying on hledger (which must be on your path) for number crunching.See [differences](https://github.com/MatthiasKauer/tim#differences-to-ti)
* Text file storage
* Uses JSON to store data


## [Timav](https://szymonkaliski.com/projects/timav/)

Time Tracking system backed by Google Calendar

[GitHub](https://github.com/szymonkaliski/timav-standalone) (from https://github.com/merveilles/Time-Travelers#time-travellers)
 
## 

Can't create a new registration(working data), because even when we fill all the fields we get this message:`Some fields are missing in current regigration`. That means that we can't export data(no even with empty values)

## [Tie tracker](https://github.com/peterpeterparker/tietracker)

Export data choice is not workin

