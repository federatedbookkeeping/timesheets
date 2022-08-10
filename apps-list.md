# Applications that record or consume timesheet data

## Shortlist

Prejournal [supports](https://github.com/pondersource/prejournal/blob/e8ad195/src/commands/import-hours.php#L32-L50) all shortlisted formats except Mite directly.
Furthermore, Prejournal also support import/export to/from WikiSuite, which is how it supports Mite indirectly.

WikiSuite [supports](https://gitter.im/federatedbookkeeping/timesheets?at=62ab2467e393a318065d4dd1) Scoro, Mite and Time directly.
Furthermore, WikiSuite  support import/export to/from Prejournal, which is how it support the other shortlisted formats indirectly.

Timeld supports none of the shortlisted formats directly, but it support import/export to/from both WikiSuite and Prejournal, which is how it supports
all shortlisted formats indirectly.

| App| Description | Usable? | Export Formats | Import Formats | Supports Teams? | Open Source? | Price(US$/month) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| [Mite CMD](https://github.com/Overbryd/mite.cmd) | mite is a sleek online time tracking tool. Built in collaboration with the people who rely on it now: designers, developers, architects, and attorneys. Freelancers as well as small teams. | ✔️ | [JSON](./data-formats/mite-JSON-GET.md) | [JSON](./data-formats/mite-JSON-POST.md) | ✔️ | ❌ | €5/user/month | 
| [Savemytime](https://play.google.com/store/apps/details?id=com.godmodev.optime) | Mobile timetracker  | ✔️  | [CSV](./data-formats/saveMyTime-CSV.md) (proffesional 3$) | ❌(?) |  ❌  | ❌ | 0-3$ |
| [Scoro](https://www.scoro.com/time-management-software/) | Software as a Service (SaaS)| ✔️  | [JSON](./data-formats/scoro-JSON.md) |  [JSON](./data-formats/scoro-JSON.md)  | ✔️  | ❌ | [19$-49$+](https://www.scoro.com/pricing/) |
| [Stratustime](https://stratustime.centralservers.com/) |  Employees can record their time  | ✔️   | [JSON](./data-formats/stratustime-JSON.md), [XML](./data-formats/stratustime-XML.md)| [XML](./data-formats/stratustime-XML.md), [JSON](./data-formats/stratustime-JSON.md)  |  ✔️  | ❌  | 4$+/employee |
| [Time](https://github.com/wbbly/time) | React UI for Wobbly Time Tracker for the Teams | ✔️ | [CSV](./data-formats/time-CSV.md) | (❌) | ✔️ | ✔️ | 0-29.99$| 
| [TimeBro](https://www.timebro.com/) | Never lose a minute with time tracking again | ✔️ | [TimeBroCSV](https://github.com/federatedbookkeeping/timesheets/blob/main/data-formats/timeBro-CSV.md) [TimeBroExcel](./data-formats/timeBro-Excel.md) [TimeBroPDF](https://github.com/federatedbookkeeping/timesheets/blob/main/data-formats/timeBro-PDF.pdf)| ❌ | ❌ | ❌ | 14-30$| 
| [Timecamp](https://www.timecamp.com/) | Track time against your projects and create reports and timesheets in seconds. | ✔️ | [TimeCampCSV](https://github.com/federatedbookkeeping/timesheets/blob/main/data-formats/timecamp-CSV.md) [TimeCampExcel](./data-formats/timeCamp-Excel.md) [TimeCampPDF](https://github.com/federatedbookkeeping/timesheets/blob/main/data-formats/timeCamp-PDF.pdf) | ❌ | ✔️ | ❌ | 0-9$ | 
| [Time Doctor](https://www.timedoctor.com/) | Automatic time tracking lets you know where the team excels and where it needs help so you can easily improve individual and overall performance.| ✔️ | [TimeDoctorCSV](https://github.com/federatedbookkeeping/timesheets/blob/main/data-formats/timeDoctor.CSV.md) [TimeDoctorExcel](./data-formats/timeDoctor-Excel.md) | ❌ | ✔️ | ✔️ | 7-24$ | 
| [Timely](https://www.freshworks.com/apps/freshdesk/timely/) ([Android app](https://play.google.com/store/apps/details?id=com.timeapp.devlpmp) | Works with Freshdesk / Freshworks) | ✔️ | [TimelyCSV](https://github.com/federatedbookkeeping/timesheets/blob/main/data-formats/timely-CSV.md) [TimelyExcel](./data-formats/timely-Excel.md) [TimelyPDF](https://github.com/federatedbookkeeping/timesheets/blob/main/data-formats/timely-PDF.pdf) | ❌ | ✔️ | ❌ | 8-20$ | 
| [Time Manager](https://apps.nextcloud.com/apps/timemanager) ([repo](https://github.com/te-online/timemanager) | (description) | ✔️ | [TimeManagerCSV](./data-formats/timeManager-CSV.csv) | ✔️ | (supports teams?) | ✔️ | Free ) | 
| [Timesheet](https://play.google.com/store/apps/details?id=robin.urenapp) | By Robin Dijkhof | ✔️ | [TimeSheetCSV](https://github.com/federatedbookkeeping/timesheets/blob/main/data-formats/timesheet-CSV.md) [TimeSheetPDF](https://github.com/federatedbookkeeping/timesheets/blob/main/data-formats/timesheet-PDF.pdf) | ❌ | ❌ | ❌ | Free | 
| [Timesheet Mobile](https://apps.apple.com/us/app/timesheet-mobile/id560462162) | Timesheet Mobile | ✔️ | [TimeSheetMobileCSV](https://github.com/federatedbookkeeping/timesheets/blob/main/data-formats/timesheetMobile-CSV.md | ❌ | ✔️| ❌ | 3-149$ | 
| Timesheets Time Tracker | See Veryfi | ✔️ | [TimeSheetVerifyUiJSON](https://github.com/federatedbookkeeping/timesheets/blob/main/data-formats/timesheetVerifyUiJSON.md | ❌ | ✔️ | ❌ | 0-500$ |
| [Timetip](https://github.com/rstacruz/timetip) | Deliciously-minimal time tracker for the command-line | ✔️ | [TimeSheetTimeTrackerExcel](./data-formats/timeTip-JSON.md)| ❌ | ❌ | ✔️ | Free | 
| [Timetracker](https://github.com/anuko/timetracker) | By Anuko | ✔️ | [TimeTrackerCSV](./data-formats/timeTracker-CSV.md) [TimeTrackerPDF](./data-formats/timeTracker-PDF.pdf) [TimeTrackerXML](./data-formats/timeTracker-XML.md) | ✔️ | ✔️ | ✔️ | Free | 
| [Time Tracker CLI](https://github.com/danibram/time-tracker-cli) | Node JS cli application | ✔️ | [TimeTrackerCliCSV](./data-formats/timeTrackerCli-CSV.md) [TimeTrackerCliJSON](./data-formats/timeTrackerCli-JSON.md)| ❌ | ❌ | ✔️ | Free | 
| [Time Tracker](https://play.google.com/store/apps/details?id=com.cg.android.ebillitytimetracker) | By eBillity | ✔️ | [TimeTrackerCSV](./data-formats/timeTrackerDaily-CSV.md) [TimeTrackerExcel](./data-formats/timeTrackerDaily-Excel.md)| ❌ | ✔️ | ❌ | 6-24$ | 
| [Time Tracker](https://apps.nextcloud.com/apps/timetracker) | On Nextcloud | ✔️ | [TimeTrackerCSV](./data-formats/timeTrackerNextcloud-CSV.md) [TimeTrackerJSON](./data-formats/timeTrackerNextcloud-JSON.md)| ❌ | ❌ | ✔️ | Free | 

## Other Time Tracker Apps

| App| Description | Usable? | Export Formats | Import Formats | Supports Teams? | Open Source? | Price(US$/month) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| [Darkyenus Time Tracker](https://github.com/Darkyenus/DarkyenusTimeTracker) | Tracks time in the IDE. Adds it to git commit messages | ✔️ | Git log | ❌ | ✔️ | ✔️ (Unlicense) |N/A |
| [Dart](https://github.com/tschmidt23/dart) | Not a time tracker, but a real-time tracker thingy | N/A | N/A | N/A | N/A | N/A | N/A |
| [Deep Work Hours](https://github.com/co0lsky/deep-work-hours-phoenix) | pubsub for time tracking | Maybe? | Pubsub | Pubsub | ✔️ | No license | N/A |
| [Doing](https://brettterpstra.com/projects/doing/) | Command line time tracker | ✔️ | CSV/JSON/Markdown | JSON | (supports teams?) | ✔️ (MIT) | N/A | 
| Dotoo (see Vim-DoToo) | see Vim-DoToo | N/A | N/A | N/A | N/A | N/A | N/A |
| [Easy Hours](https://play.google.com/store/apps/details?id=com.thirtyxi.easyhourslite) | Android app for time tracking. Has a free version, but that does not support exports | ✔️ | CSV | ❌ | No | ❌ | 5,49 one time |
| [Employee Time Clock](https://play.google.com/store/apps/details?id=com.timesheetmobile) | Android app companion for www.timesheetmobile.com | ✔️ | REST API | REST API | ✔️ | ❌ | 14,99 base + 3,49 per employee |
| Employee Time Clock - SINC (see SINC) | See SINC | N/A | N/A | N/A | N/A | N/A | N/A | 
| [Emoji Log](https://emojilog.rosano.ca/)| (from https://github.com/merveilles/Time-Travelers#time-travellers) | ✔️? | JSON | JSON | ❌ | ✔️ (Hippocratic License) | N/A | 
| [Episodie](https://github.com/hypeapps/episodie) | Track time you spend watching TV! See also Youtube Time Tracker | ❌? | ❌ | No | ❌ | ✔️ (GPL-3) | N/A | 
| [Faereld](https://hraew.autophagy.io/faereld/) ([repo](https://github.com/autophagy/faereld))| CLI time tracker. Configurable | ✔️? | Maybe text output? | ❌ | No | ✔️ (MIT) | N/A | 
| [Forge](https://github.com/micromata/projectforge) | (description) | ✔️ | Excel / scripting available | ❌ | ✔️ | GPL-3 | price (US$/month) | 
| Freckle | Renamed to Noko | N/A | N/A | N/A | N/A | N/A | N/A | 
| [FreshBooks](https://www.freshbooks.com/en-eu/timesheets-and-time-tracking) | Commercial time tracking and more | ✔️ | REST API JSON | REST API POST | ✔️ | ❌ | 4.80/month |
| [Git Time Metric (GTM)](https://github.com/git-time-metric/gtm) | Tracks time through IDE usage. Stored as git notes | ✔️ | Git notes | Git notes | ✔️ | ✔️ (MIT) | N/A | 
| [Gitlab Time Tracker Taskbar](https://github.com/kriskbx/gitlab-time-tracker-taskbar) | taskbar thing for Gitlab time tracker | See Gitlab time tracker | N/A | N/A | N/A | ✔️ (GPL-2) | N/A | 
| [GitHub Time Tracking](https://github.com/StephenOTT/GitHub-Time-Tracking) | By Stephen Russett, archived. Tracks time in git commit messages | ✔️? | Git commit messages | Git commit messages | ✔️ | ✔️ (GPL-3) | N/A |
| [GitHub Time Tracking](https://github.com/klokantech/github-time-tracking) | By Petr Pridal – time tracker extension for Harvest. See Harvest | ❌ | N/A | N/A | N/A | (open source?) | N/A | 
| [Glass](https://github.com/timeglass/glass) | Deprecated | ✔️? | Git notes | Git notes | ✔️ | ✔️ (MPL-2) | N/A | 
| [Gitlab Time Tracker](https://github.com/kriskbx/gitlab-time-tracker) | By Kris – stores data in gitlab | ✔️? | JSON | JSON? | ✔️ | ✔️ (GPL-2) | N/A | 
| [Gitlab Time Tracking](https://github.com/dzaporozhets/gitlab-time-tracking) | By Dmitriy Zaporozhets – stores data in postgresql | (usable?) | ❌ | No | ❌? | ✔️ (MIT) | N/A |
| [GitLab Time Tracking](https://github.com/StephenOTT/GitLab-Time-Tracking) | By Stephen Russett - Time Tracking application for GitLab Issue Queues built on Ruby Sinatra and MongoDB. | ✔️ | XLSX  | ❌? | ✔️ | No license | N/A | 
| [Gitpaid](https://github.com/rcrowley/gitpaid) | CLI application that posts time tracking in Git | ❌? | Git repo | Git repo | ❌ | No license | N/A |
| [golog](https://github.com/mlimaloureiro/golog) | CLI start/stop tracking. Short lived data | ✔️ | Text output | N/A | ❌ | ✔️ (Apache-2) | N/A | 
| [Gotime](https://github.com/nanohard/gotime) | Linux only | ✔️? | Text export | N/A | ❌ | ✔️ (BSD-3) | N/A | 
| [Gtimelog](https://github.com/gtimelog/gtimelog) | Gnome based time tracker | ✔️ | Text based format, CSV | Text based format | ❌ | ✔️ (GPL-2) | N/A |
| [i4ware](https://www.freshworks.com/apps/freshdesk/i4ware_-_timesheet_for_freshdesk/) | Seems discontinued but they have a different one now that works with Jira: [Rabid Timesheets for Jira](https://marketplace.atlassian.com/apps/1223446/rabid-timesheets-for-jira?tab=overview&hosting=cloud) | ❌ | ❌ | ❌ | ❌ | ❌ | $1/user/month | 
| Intuit ([sample app, deprecated](https://github.com/IntuitDeveloper/SampleApp-TimeTracking_Invoicing-Java)) | This sample app is meant to provide working examples of how to integrate your app with the Intuit Small Business ecosystem. Fails to build java executable as it requires too old spring gradle plugin no longer available. | ❌ | N/A | N/A | N/A | N/A | Free |
| [Jiffy](https://play.google.com/store/apps/details?id=com.nordicusability.jiffy) | A lightning fast time tracker that increases productivity by quickly generating time sheets. | ✔️ | [jiffy-CSV](./data-formats/jiffy-CSV.md) | ❌ | ❌ | ❌ | Free | 
| [Jirassic](https://github.com/cristibaluta/Jirassic) | Jirassic is a Mac app that runs in background and tracks automatically the work you do at your workplace. At the end of the day creates a worklog which you can save to Jira Tempo. Its purpose is to replace primitive tracking methods or relying on memory and do everything automatically. | N/A | HTML/Jira | ❌ | ❌ | ✔️ | Free | 
| [Jobsworth](https://github.com/ari/jobsworth) | Jobsworth can be used for helpdesk support ticketing, customer liasion, resource management (eg. systems and password tracking) and has a range of CRM type functionality. | ❌ | N/A | N/A | ❌ | ✔️ | Free | 
| [Global Time Tracker](https://github.com/g-timetracker/g-timetracker) | G-TimeTracker is a simple and cloud-friendly open source time tracker. Unable to compile. | ❌ | N/A | N/A | ❌ | ✔️ | Free | 
| [Kimai](https://www.kimai.org/) / [Kimai 2](https://github.com/kevinpapst/kimai2) / [Kimai Cloud](https://www.kimai.cloud/) | Kimai is a free & open source timetracker. It tracks work time and prints out a summary of your activities on demand. Yearly, monthly, daily, by customer, by project … Its simplicity is its strength. Due to Kimai’s browser based interface it runs cross-platform, even on your mobile device. | ✔️ | [kimai-CSV](./data-formats/kimai-CSV.md) [kimai-XLSX](./data-formats/kimai-XLSX.xlsx) [kimai-Excel](./data-formats/kimai-Excel.md) [kimai-PDF](./data-formats/kimai-PDF.pdf) | ❌ | ✔️ | ✔️ | Free | 
| [Klog](https://github.com/jotaen/klog) | klog is a plain-text [file format](https://github.com/jotaen/klog/blob/main/Specification.md) and a command line tool for time tracking. | ✔️ | [klog-JSON](./data-formats/klog-JSON.md) | klog | ❌ | ✔️ | Free | 
| [Kosmos](https://play.google.com/store/apps/details?id=com.cosmicpie.spacetodolist) | Kosmos is a time tracker (timesheet and time recording app) that makes it fun to track time spent on work, sport, education - or any other activity. | N/A | ❌ | ❌ | ❌ | ❌ | $2.78 | 
| [Laravel-Angular Time Tracker](https://github.com/scotch-io/laravel-angular-time-tracker) | Hobby project - Build a Time Tracker with AngularJS and Laravel 5 | ❌ | N/A | N/A | N/A | ✔️ | Free | 
| [Laravel Time Tracker](https://github.com/jeremykenedy/laravel-time-tracker) | Laravel Angular Time Tracker is a simple time tracking application built on Laravel 5.2, Angular 2, and Bootstrap 3 | ❌ | N/A | N/A | N/A | ✔️ | Free | 
| [Laravel-Vue Time Tracker Example](https://github.com/neoighodaro/Laravel-Vue-Time-Tracker-Example) | Create a time tracker using Laravel and Vue | ❌ | N/A | N/A | N/A | ✔️ | Free | 
| [Latte](https://github.com/flakas/Latte) | Automatic Time Tracker for Linux | ❌ | N/A | N/A | N/A | ✔️ | Free | 
| [Ledge](https://github.com/maxdeviant/ledge) | Personal time tracker app with custom JSON format. | ✔️ | [ledge-JSON](./data-formats/ledge-JSON.md) | [ledge-JSON](./data-formats/ledge-JSON.md) | ❌ | ✔️ | Free | 
| [Ledger-CLI](https://www.ledger-cli.org/3.0/doc/ledger3.html#Time-Keeping) | Ledger is a command-line accounting tool that provides double-entry accounting based on a text journal. It provides no bells or whistles, and returns the user to the days before user interfaces were even a twinkling in their fathers’ CRTs. | ✔️ | [ledger-CLI-CSV](./data-formats/ledger-CLI-CSV.md) | csv/proprietary | ❌ | ✔️ | Free | 
| [Letnice](https://github.com/nomand/Letnice)| Letnice is a simple JavaScript Gregorian calendar visualizer that tracks year progress. NOT a time tracker. | ✔️ | ❌ | ❌ | ❌ | ✔️ | Free | 
| [Life Cycle](https://apps.apple.com/nl/app/life-cycle-track-your-time/id1064955217) | Life Cycle automatically keeps track of your time and presents your life sorted into slices. | ✔️ | ❌ | ❌ | ❌ | ❌ | Free | 
| [Log](https://avanier.vercel.app/tracker) | Cannot seem to download or find [log app](https://avanier.vercel.app/log) source or binary. Found [log](https://github.com/composition4/log) which seems by the same author but is not usable.  | ❌ | N/A | N/A | N/A | ✔️ | Free | 
| [Log](https://github.com/v-exec/Log) | The Log is a timekeeping tool for productivity and time management. It uses a generic text file as a collection of logs, converts these logs to mySQL entry commands through a simple Ruby parsing script, uploads them to a remote mySQL database, and visualizes this data through a web-based interface using PHP. | ✔️ | ❌ | [log-CSV.md](./data-formats/log-CSV.md) | ✔️ | ✔️ | Free | 
| [MacTimeLog](https://github.com/SPlyer/MacTimeLog) | MacTimeLog is a simple time tracking tool for Mac OS X. | ❌ | N/A | N/A | N/A | ✔️ | Free | 
| [Metime](https://github.com/jdleesmiller/metime) | Personal time tracker tool | ✔️ | ❌ | ❌ | ❌ | ✔️ | Free | 
| [Monday.com](https://monday.com/lp/mb/time-tracking/comparison2) | Team-based time tracking platform | ✔️ | [XLSX](./data-formats/monday.com-XLSX.xlsx) [Excel](./data-formats/monday.com-Excel.md) | ❌ | ✔️ | ❌ | $0-$22/user/month | 
| [Muze in-house tool (not public)](https://uren.muze.nl/) | Not for public use | Yes | Muze-JSON | No | No | No | N/A | 
| [My Worktime](https://play.google.com/store/apps/details?id=com.danielg.myworktime) | My Worktime is the kind of app that makes your smartphone a great tool for tracking your jobs, calculating your pay and tracking your project time. | ✔️ | CSV/XLSX/PDF (needs in-app purchase) | ❌ | ❌ | ❌ | $0-$2 | 
| [Nettime](https://www.nettimesolutions.com/) | This is the developer of Stratustime | N/A | N/A | N/A | N/A | N/A | N/A | 
| [Nexonia](https://play.google.com/store/apps/details?id=com.nexonia.android.timesheets) | Fully integrated expense reporting, invoice management, time tracking, and travel solutions. | Demo request required | N/A | N/A | ✔️ | ❌ | $12+/user/month | 
| Nextcloud | See "Time Tracker" and "Time Manager") | N/A | N/A | N/A | N/A | N/A | N/A | 
| [Noko](https://nokotime.com/freckle-getting-new-name-noko/)  ([API docs](https://github.com/cheerful/freckle-apidocs)) | Time tracking web/mobile app | ✔️ | [noko-CSV](./data-formats/noko-CSV.md)/XLSX/[noko-JSON](./data-formats/noko-JSON-GET.md) | [noko-import-CSV](./data-formats/noko-import-CSV.md)/[noko-JSON](./data-formats/noko-JSON-POST.md) | ✔️ | ❌ | $49-$199-$499/month | 
| [Notion](https://notion.so) (see Simple Time Tracker with Notion) ([TMetric integration](https://tmetric.com/integrations/notion-time-tracking)) ([Clockify integration](https://clockify.me/notion-time-tracking)) | A custom time tracking app could be created inside notion but mostly there are 3rd party time tracking tools that integrate with notion: Tmetric, [TrackingTime](https://trackingtime.co/time-tracking-in-notion), Toggl, Clockify. The formats and import/export here depend on these 3rd parties, so let's document them under corresponding entries. | ✔️ | N/A | N/A | ✔️ | ❌ | Free-$10+/user/month | 
| [Odoo-mobile/hr](https://github.com/Odoo-mobile/hr) [Android app](https://play.google.com/store/apps/details?id=com.odoo.OdooTimesheets) | Simple time tracking app with projects/tasks selection. | ✔️ | N/A | N/A | ✔️ | ✔️ | Free | 
| [Onehour-app](https://github.com/fayeed/Onehour-app) | Personal time tracking app built with Flutter (android/ios versions available) | ✔️ | N/A | N/A | ❌ | ✔️ | Free | 
| [One Inch Punch](https://github.com/ymendel/one_inch_punch) | Ruby gem to be integrated into projects. Usable by ruby programmers. | ✔️ | [punch-YAML](./data-formats/punch-YAML.yaml) | [punch-YAML](./data-formats/punch-YAML.yaml) | ❌ | ✔️ | Free | 
| [On The Clock](https://apps.apple.com/us/app/ontheclock-employee-time-clock/id1029560603) [Web app](https://www.ontheclock.com/) | Mobile/Web time tracking app for businesses. | ✔️ | [ontheclock-CSV](./data-formats/ontheclock-CSV.md) | N/A | ✔️ | ❌ | $2.70-$3/employee/month | 
| [Page Timer](https://github.com/google/page-timer) | A Chrome plugin that measures the time you spend on a task (equated to how long you are on a specific url. Data saved to local storage. | Not in our context | JSON | JSON  | N/A |  ✔️  | Free | 
| [Parent-Child time tracker](https://www.freshworks.com/apps/freshdesk/parent-child_time_tracker/) | Works with Freshdesk / Freshworks. It copies time logs from child service tickets to the parent service ticket. | Looks usable if you have Freshworks. | N/A | N/A | support@freshdesk.com | No | Free if you have freshworks. | 
| [Paychex Flex](https://www.paychex.com/time-attendance) (see also Stratustime and "Time and Labor") | Automated Tracking and Reporting, flexible punch options. Looks like for reasonable size companies, maybe manufacturing type work. |  ✔️ | Not sure | Not sure | ✔️  |  ✔️  | Need to get a quote. | 
| [Plain Text Accounting](https://plaintextaccounting.org/#time-logging) | Time cli tool that can be used with hledger | I couldn't get it to work on Mac, but it may work on Windows or Linux| JSON (start, end, taskname) |  ❌ | Log a Git ticket |  ✔️ | Free| 
| [Personio](https://www.personio.com/product/attendance-tracking/) | Professional attendance tracker whereby employees can enter time and managers can approve it. (In order to test you need to book a demo.)  |  ✔️  | Not Sure | Not sure | ✔️ | ❌ | Not listed | 
| [Planet](https://github.com/xvw/planet)| (from https://github.com/merveilles/Time-Travelers#time-travellers). Written in a language called OCaml, says WIP for a long time. | ❌  | N/A | N/A | Log Github Issue | ✔️  | Free | 
| [Pom](https://github.com/tobym/pom) | A minimalist pomodoro-style time-tracker. Shell script. No data saved. |  ✔️ | N/A | N/A | ❌  |  ✔️  | Free | 
| [Pomidorus](https://github.com/tatyshev/pomidorus) | Very neat pomodoro-style timer. No data saved.| ✔️  | N/A | N/A | GitHub ticket | ✔️  | Free | 
| [Pomobot](https://github.com/Intery/PomoBot) | Discord bot. Manage group study. Show stats. Can show history with a command in Discord.  | ✔️ | N/A | N/A | Log Github issue| ✔️  | Free | 
| [Pomodo on Rails](https://github.com/dima/pomodo_on_rails) | RESTful Flex Development Demo App (Rails Version) |  ❌  | ❌  | ❌  |  ❌ | ✔️  | Free | 
| [React Time Tracking](https://github.com/tuanngominh/react-time-tracking) | Track your tasks and start a timer. You can tag/categorize your tasks. | ✔️  | Firebase dump | Import into Firebase | 2019 last activity |  ✔️  | Free | 
| [Redmine Time Tracker](https://github.com/fernandokosh/redmine_time_tracker) | By Fernando Kosh, plugin for Redmine. Track time with a start/stop timer. Can be started with or without reference to Redmine issue. Can be used to generate invoices. Not maintained since 2014. | ❌  | Not obvious | Not obvious| ❌  | ✔️ | Free | 
| [Redmine Hourglass](https://github.com/hicknhack-software/redmine_hourglass) | Rewrite of Fernando Kosh's Redmine Time Tracker. Redmine plugin to aid in tracking spent time on projects and issues. A timer you can stop/start with an optional reference to what you are working on. Can be used to generate invoices. | ✔️ | Dump from mysql | csv | Log issues on Github | ✔️ | Free | 
| [Redtimer](https://github.com/fathomssen/redtimer) | Easy-to-use platform-independent time tracker. Allows user to track time while working on issues. | ✔️  | Not obvious | Not obvious| Looks like you can log issues on Github. Not sure what response is like. |  ✔️  | Free | 
| [RescueTime](https://play.google.com/store/apps/details?id=com.rescuetime.android) | Android app used to track all your screen time. Can also add your own meetings etc.| ✔️ | Not obvious | Not obvious | Yes, with paid subscription | ❌ | Free/Premium $12/month or $78/year | 
| [Rubytime](https://github.com/LunarLogic/rubytime) | Merb-based time tracking and invoicing system. Web application for time tracking and invoicing | At your own risk | N/A | N/A| ❌  | ✔️ | Free | 
| [rtw](https://github.com/PicoJr/rtw) | Rust Time Watcher, cli is stable. This is a personal project though and the developer suggests if you want a real tool to use Time Warrior | ❌  | json | N/A | Not really, but PicoJr may help |  ✔️ | Free | 
| [Saas-Timetracker](https://github.com/appcasts/saas-timetracker) | Rails Software(server-side web application framework) as a Service Application for time tracking| ✔️  | ❌ | ❌ | ❌   |  ✔️   | Free |
| [Sage HR](https://sage.hr/features/timesheets) | A simple, easy to use interface to adjust hours worked & submit a timesheet for approval to a manager | ✔️  | ✔ | [JSON](./data-formats/sageHR-JSON.md) | ✔️  | ❌  | [7$/employee](https://sage.hr/pricing) |
| [Samay](https://github.com/nexneo/samay) | Command line Time tracking and reporting | ✔️  |  ❌  |  ❌  | ❌ | ✔️   | Free |
| [SAP Fieldglass](https://play.google.com/store/apps/details?id=com.sap.ui5.timeentry) | Cloud-based Vendor Management System (VMS) | ✔️  | JSON/CSV |  JSON/CSV | ✔️   |  ❌  | Free(too good to be true) |
| [SimpleTimeTracker-Razeeman](https://play.google.com/store/apps/details?id=com.razeeman.util.simpletimetracker) | Time tracker app | ✔️  | [CSV](./data-formats/simpleTimeTracker-CSV.md) | N/A |  ❌  | ✔️  | Free |
| [Simple TimeTracker with Notion](https://apps.apple.com/nl/app/simple-timetracker-with-notion/id1590343222) | IOS app time tracker | ✔️  | ❌ |  ❌ |  ❌  |  ❌ | Free |
| [SINC](https://play.google.com/store/apps/details?id=com.sinc.sincandroid) | Timecard And Location Tracking App | ✔️   | PDF/Excel(the excel file can be opened and saved as a CSV file) |  ❌ | ✔️    | ❌ | 0-50$ |
| [Smarter Time](https://play.google.com/store/apps/details?id=com.smartertime) | Time tracker app for iOS,Web and  Android | ✔️  | [CSV](./data-formats/smarterTime-CSV.md) | N/A | ❌ | ❌ | 0-5$ |
| [Sprint App](https://github.com/macfanatic/SprintApp) | Project management and time tracking app | ✔️  | ❌(Html response. No clear doc, conclusion made by looking the code) | N/A |  ✔️  | ✔️  | Free |
| [Staple](https://github.com/bertinetto/staple) | Staple tracker. CVPR 2017: End-To-End Representation Learning for Correlation Filter Based Tracking | ❌ | N/A  | N/A  | N/A | ✔️  | Free |
| [StreaDeck-Toggl](https://github.com/tobimori/streamdeck-toggl) |Time tracking using [Elgato Stream Deck](https://www.elgato.com/en/stream-deck) and [Toggl Track](https://toggl.com/track/) | ✔️  | JSON | JSON |  ✔️   | ✔️  | Free |
| [Super Productivity](https://github.com/johannesjo/super-productivity) | todo list app with integrated [Timeboxing](https://en.wikipedia.org/wiki/Timeboxing) and time tracking capabilities | ✔️  | N/A | N/A | ✔️   |  ❌  | Free |
| [swdc-vscode](https://github.com/swdotcom/swdc-vscode) | Time-tracking plugin for Visual Studio Code | ✔️   | N/A | N/A |  ✔️  | ✔️  | Free |
| [SwipeTimes](https://play.google.com/store/apps/details?id=lc.st.free) | Time tracker app | ✔️    | [Excel](./data-formats/swipetimes-XLS.xls),[PDF](./data-formats/swipetimes-PDF.pdf),[XML](./data-formats/swipetimes-XML.md),[CSV](./data-formats/swipetimes-CSV.md)  | N/A |  ❌  | ❌ |    |
| [Syncrew](https://syncrew.com/features.shtml) | Mobile workforce managment platform   | ✔️   | ❌  |  ❌  |  ❌  | ✔️  |  ❌  | 5$-25$
| [Synerion](https://www.synerion.com/time-and-attendance-software/) | Workforce managment software | ✔️ | N/A | N/A  |  ✔️  | ❌  | 2$+ |
| [TagTime](https://github.com/tagtime/TagTime) |At unpredictable [3] times, a box pops up and asks, what are you doing right at this moment |  ❌ | N/A | N/A |  ❌  | ✔️  | Free |
| [Task Tracker](https://apps.apple.com/nl/app/task-tracker-time-tracking-for-people/id1114876492)| Task tracker app | ❌  | N/A | N/A  | ✔️ | | ❌  | N/A |
| [Taxi](https://github.com/sephii/taxi) | CLI to time tracking backends | CLI to time tracking backends |  ✔️  | N/A  |  ❌  | ✔️  | Free |
| [Team Timesheets](https://github.com/thdk/team-timesheets) | Time tracking web app | ✔️ | CSV/month  | N/A | ✔️  | ✔️  | Free |
| [Tempo](https://www.tempo.io/) by Jira | Jira time tracking app  | ✔️  | XLS,CSV,PDF | N/A | ✔️  | ❌  | 10$+ |
| [Teramind](https://www.teramind.co/landing/time-tracking-software)| Time Tracking Platform | ✔️ |  ✔️  | ✔️  | ✔️  | ❌  | 10$-25$ |
| [ti](https://github.com/richmeta/ti) | Command line Time tracker | ✔️  | [JSON](./data-formats/ti-JSON.md) | ❌ |  ❌  | ✔️  | Free |
| [Tietracker](https://github.com/peterpeterparker/tietracker) | Time tracker app | ✔️  | XLSX timesheets (Excel, LibreOffice, Numbers, etc),PDF| N/A |  ❌  | ✔️  | Free |
| [Tick](https://www.tickspot.com/time-tracking-app) | Time tracking software |✔️  | [CSV](./data-formats/tick-CSV.md)/[JSON](./data-formats/tick-JSON.md)  | [JSON](./data-formats/tick-JSON.md) |  ❌  | ❌ | 0-149$ |
| [Ticket Timer](https://www.freshworks.com/apps/freshdesk/ticket_timer/)  |Time tracker app, which uses tickets to save time(Need for [Freshworks](https://www.freshworks.com/)) account | ✔️  - | - |  ❌  | ❌  | Free/Premium(price is not clear) |
| [Tim](https://github.com/MatthiasKauer/tim) |  CL for recording time logs(Handled by [hledger](https://hledger.org/)) | ✔️  | JSON | - |  ❌  | ✔️  | Free |
| [Timav](https://szymonkaliski.com/projects/timav/) | Time Tracking system backed by Google Calendar | ✔️  | - | - |  ❌  | ✔️  | Free |
| [Time and Labor](https://timeandlabor.paychex.com/secure/) | See also Paychex | (waiting for response) | (waiting for response) | (waiting for response) | (waiting for response) | (waiting for response) | (waiting for response) | 
| [Timecop](https://github.com/hamaluik/timecop) | A time tracking app that respects your privacy and gets the job done without getting too fancy.| ❌ | CSV | ❌ | ❌ | ✔️ | 0.79$ | 
| [Timed](https://github.com/adeel/timed) | Timed is a command-line time tracker. | ❌ | ❌ | ❌ | ❌ | ✔️| Free | 
| [Timeero](https://play.google.com/store/apps/details?id=com.timeero.time_clock) | Track employee hours, mileage and location with our GPS time tracking app.| ✔️ | ❌ | ❌ | ❌ | ❌| 5-10$ | 
| [Timeglass](http://timeglassapp.io/) | Time anything.
Or everything. | ✔️ | ❌| ❌ | ❌ | ❌ | ❌ | 
| [Timelog](https://play.google.com/store/apps/details?id=dev.giall.timelog) | Make time tracking a no-brainer. | ✔️ | ❌ | ❌ | ❌ | ❌ | 0-40$ | 
| [Time Meter](https://play.google.com/store/apps/details?id=com.rk.timemeter) | Time Meter| ✔️ | ✔️ | ❌ | ❌ | ❌ | 0-5$| 
| [TimePouch](https://github.com/chesles/timepouch) | timepouch is a command-line time tracking utility  | ❌| ❌ | ❌ | ❌ | ✔️ | Free | 
| [Time Recorder](https://play.google.com/store/apps/details?id=com.dynamicg.timerecording) | Time Recorder | ✔️ | [TimeRecordExcel](./data-formats/timeRecorder-Excel.md) [TimeRecorderPDF](./data-formats/timeRecorder-PDF.pdf) | ❌ | ❌ | ❌ | Free | 
| [Timesheet](https://play.google.com/store/apps/details?id=com.unidevsolutions.timesheet) | By Unidev Solutions | ✔️ | [TimeSheetCSV](https://github.com/federatedbookkeeping/timesheets/blob/main/data-formats/timesheet-CSV-1.md) | ❌ | ❌| ❌ | 0-5.35$ | 
| [Timesheet History](https://play.google.com/store/apps/details?id=com.forutan.app.timesheethistory) | by Forutan Software | ✔️ | Excel - but need pay before export | ❌ | ❌ | ❌ | 2.24$ | 
| Timesheet PDF [Android app](https://play.google.com/store/apps/details?id=com.mds.tplus) [iOS app](https://apps.apple.com/us/app/timesheet-pdf/id898115583) | by Mobile and Database Solutions | ✔️ | [TimeSheetPDF](https://github.com/federatedbookkeeping/timesheets/blob/main/data-formats/timesheetPDF-PDF.pdf | ❌ | ❌ | ❌| The price is not set. | 
| [Timesheet - Time Tracker](https://play.google.com/store/apps/details?id=com.rauscha.apps.timesheet) | Timesheet - Time Tracker | ✔️ | [TimeSheetTimeTrackerCSV](https://github.com/federatedbookkeeping/timesheets/blob/main/data-formats/timesheetTimeTracker-CSV.md [TimeSheetTimeTrackerExcel](./data-formats/timesheetTimeTracker-Excel.md)| ❌ | ❌ | ❌ | 0-10$ | 
| [Timesheet - Time Card](https://play.google.com/store/apps/details?id=com.aadhk.time) | Timesheet - Time Card | ✔️ | CSV/Excel | CSV/Excel | ❌ | ❌ | Free | 
| [Timesheet Track Hours Salary](https://play.google.com/store/apps/details?id=com.bakua.worktimemanager) | (description) | ✔️ | [TimeSheetTrackHoursSalaryExcel](./data-formats/timesheetTrackHours.md) | ❌ | ❌ | ❌| 2.55$ | 
| Timesheet - Track Work Hours [Android app](https://play.google.com/store/apps/details?id=com.sullivansoftware.timesheetapp) [iOS app](https://apps.apple.com/us/app/timesheet-track-work-hours/id1326395665) | Timesheet - Track Work Hours  | ✔️ | ❌ | ❌| ❌ | ❌ | Free | 
| [Timesheets](https://github.com/hardchor/timesheets) | By hardchor | ❌ | ❌ | ❌ | ❌| ✔️ | Free | 
| [Timesheets](https://play.google.com/store/apps/details?id=com.singlebyte.harvest) | By SingleByte | ❌  | ❌ | ❌ | ❌ | ❌ | Free | 
| [Timestrap](https://github.com/overshard/timestrap) | Full export support in multiple formats | ❌ | ✔️ | ❌ | ❌ | ✔️ | Free | 
| [TimeTell](https://timetell.com/software-modules/) | TimeTell | ❌ | ✔️ | ❌ | ❌ | ❌ | Not find | 
| [TimeTrack](https://play.google.com/store/apps/details?id=com.time_tracking.user006test.timetracking)  | TimeTrack | waiting for response | ❌ | ❌ | ❌ | ❌ | I don't know | 
| [Time Track](https://github.com/torsten/TimeTrack) | A minimalist time tracking app for Mac OS | ❌ | ❌ | ❌ | ❌ | ✔️ | Free | 
| [TimeTracker](https://github.com/knewter/time-tracker) | By Knewter | ❌ | ❌ | ❌ | ❌ | ✔️ | Free | 
| [Timetracker](https://github.com/eyscode/timetracker) | By Eysenk, CLI client for BairesDev TimeTracker | ❌ | CSV | ❌ | ❌ | ✔️ | Free | 
| [Time Tracker](https://play.google.com/store/apps/details?id=zzz1zzz.tracktime) | By Zafer Ertas | ✔️ | ✔️ | ❌ | ❌ | ❌ | 6$ | 
| [Time Tracker - Timesheet](https://play.google.com/store/apps/details?id=ch.gridvision.pbtm.androidtimerecorder) | By Gridvision | ✔️ | [TimeTrackerTimesheetCSV](./data-formats/timeTrackerTimesheet-CSV.md) | ❌ | ❌ | ❌ | Free | 
| [Time Tracker Mac](https://github.com/rburgst/time-tracker-mac) | By Rainer Burgstaller | ❌ | ✔️ | ❌ | ❌ | ✔️ | Free | 
| [Time Tracker Mac](https://github.com/avh4/time-tracker-for-mac) | By Aaron VonderHaar, archived? | ❌ | ✔️ | ❌ | ❌ | ✔️ | Free | 
| [Time Tracking](https://github.com/derhuerst/time-tracking) | Minimalistic command line time tracking | ✔️ | ❌ | ❌ | ❌ | ✔️ | Free | 
| [Timetrackrs](https://github.com/phiresky/timetrackrs) | WIP | ❌ | ❌ | ❌ | ✔️ | ✔️ | Free | 
| [Timetrap](https://github.com/samg/timetrap) | simple command line time tracker | ✔️ | [TimeTrapCliCSV](./data-formats/timetrapCli-CSV.md) | ❌ | ❌ | ✔️ | Free | 
| [Time Tracker Flutter Course](https://github.com/bizz84/time_tracker_flutter_course) | Time Tracker Flutter Course | ✔️ | ❌ | ❌ | ❌ | ✔️ | Free | 
| [Timewarrior](https://timewarrior.net/) | Timewarrior | ✔️ | [TimeWarriorJSON](./data-formats/timewarrior-JSON.md) | ❌ | ❌ | ✔️ | Free | 
