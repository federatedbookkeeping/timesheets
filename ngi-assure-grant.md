# Federated Timesheets

NGI Assure proposal, 1 Dec 2021

## Data to fill in on https://nlnet.nl/propose/
### Basics
* User Operated Internet Fund
* Contact information: Bänz Schenk et al.
* Project name: Federated Timesheets
* Website / wiki: https://gitter.im/federatedbookkeeping/timesheets
### Abstract: Can you explain the whole project and its expected outcome(s) (max 1200 chars)
This project is quite unique in that it brings together developers from 5 enthusiastic projects:
WikiSuite, <span>m-ld</span>.io, AgendaUren, Muze, and Ponder Source. This collaboration between multiple sovereign teams
is a deliberate part of this research experiment, studying how federated machine-readable data can work
between independent software projects on the user-operated internet.

The topic we chose is timesheet data. Each project has a timesheet system to track billable hours.
Workers often spend time manually filling in this data multiple times.

Instead, a worker's time tracker app (locally or on a self-hosted server) could expose machine-readable
timesheet data through a query endpoint (reader pull) or through a webhook (writer push).

Timesheet data is relatively simple in terms of data format, data replication only flows in one direction,
and there are not too many identities involved in the authentication / authorization of the data source connections.

This simplicity makes the "Federated Timesheets" project an ideal case study for Federated Bookkeeping in general.
We want to show case how our vision of Federated Bookkeeping can make internet users "connected but sovereign".

### Have you been involved with projects or organisations relevant to this project before? And if so, can you tell us a bit about your contributions? (max 10000 characters)
#### Team:

* Bänz Schenk (Switzerland) is a senior php developer at Ponder Source, focused on FOSS development
* George Svarovsky (UK) is an expert in data management, shared data types and linked data, and the lead developer of m-ld, for which he received NGI Assure funding
* Victor Emanouilov (Bulgaria) is a senior developer of WikiSuite, and most involved in WikiSuite's data federation roadmap
* Andrej Bagoutdinov (Germany) is a volunteer researcher at Ponder Source
* Yvo Brevoort (Netherlands) is a senior php developer and visionary at Muze, and has worked on NGI-funded projects like Solid-Nextcloud, Solid-Migrator, and ScienceMesh-Nextcloud
* Lambert Beekhuis (Netherlands) is the founder and developer of "AgendaUren", a hosted timekeeping application that integrates with Google Calendar

#### Advisors:
* Marc LaPorte (Canada) is the long-term visionary behind "WikiSuite"
* Michiel de Jong (Netherlands) is the founder of "Ponder Source" and sparked the "Federated Bookkeeping" movement


### Explain what the requested budget will be used for?
#### 5 Publishers (5kEUR each):
* Add an API to [Nextcloud/TimeTracker](https://apps.nextcloud.com/apps/timetracker) (Bänz Schenk)
* Add an API to [uren.muze.nl](https://uren.muze.nl) (Yvo Brevoort)
* Add an API to [AgendaUren](https://agenda-uren.nl) (Lambert Beekhuis)
* Add an API to [WikiSuite](https://wikisuite.org/Software) (Victor Emanouilov)
* Develop a simple example time tracker app using m-ld, which can push its data to a configurable webhook (George Svarovsky)

#### 1 Polyglot spec (3kEUR):
* Aggregate the 5 publisher formats into one superset spec (Andrej Bagoutdinov)

#### 3 Subscribers (5kEUR each):
* Newly developed Nextcloud invoice generator that can read from 5 data source types (Bänz Schenk)
* Make the app based on m-ld read from the other 4 data source types (George Svarovsky)
* Make WikiSuite's [Tiki Trackers](https://doc.tiki.org/Trackers) read from the other 4 data source types (Victor Emanouilov)

#### Overhead (remaining 7kEUR):
* Problem ownership, project management (Andrej Bagoutdinov)
* Documentation, promotion, user support (Andrej Bagoutdinov)
* Travel, hosting, other expenses