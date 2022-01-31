# Federated Timesheets

## Answers to grant review questions

1. Is the rate you used the same for each of the tasks?
No, not exactly.
We have divided the work into four sub-teams (Ponder Source, m-ld, WikiSuite, Muze).
Our rates vary from 25 to 65 euros per hour, depending on location and seniority.

2. Is there already a draft format, and if so could you share?

We will support many different formats, not one "best / preferred" format. Our goal is to support all formats we can find. We will document how each format looks and how timesheet entries can be converted from one format to another. If anything, our draft format would be just a list of entries, where each entry has:
* start timestamp
* end timestamp
* project name
* worker name
* description of work performed

Or, equivalently:
* timestamp
* number of hours worked
* project name
* worker name
* description of work performed

For instance, a VEVENT in CalDAV (RFC 4791) has a DTSTART and a DTEND datetime. An entry in a timedot file has a number of hours worked. The format used by uren.muze.nl has a number of minutes worked. Here is an example of the uren.muze.nl format:
`
[
  {
    "desc": "rest API REVA + invite flow + oplevering",
    "id": "20751",
    "klantdesc": "Nextcloud",
    "minuten": "120",
    "persname": "Yvo",
    "projectdesc": "Science Mesh IOP integration",
    "time": "2021-12-01 00:00:00"
  }
]
`
And here is an example timedot file: https://github.com/simonmichael/hledger/blob/master/examples/sample.timedot


We will support all of these, and provide conversion back and forth between all of them!

3. You mention IETF as a standardisation venue, is there an existing working group you are targetting?

We previously thought IETF might be the best venue, but later realised that this work is more at the web level than at the internet level, so we created a W3C CG: https://www.w3.org/community/timesh

4. Are you aware of calconnect.org?

We were not aware of CalConnect, thanks for the pointer!
They don't seem to have an explicit standard for timesheets yet, but we will reach out to them to notify them about our project.

We'll also read and follow their work on improving CalDAV and related interoperability work. For instance their [additional notes on CalDAV's DATE-TIME format](https://devguide.calconnect.org/iCalendar-Topics/Handling-Dates-and-Times/) look very useful!

5. Have you looked at other SDO's like OASIS?

Yes! And we intend to use OData's REST based Extension for Temporal Data Version 4.0. But for the dissemination of our work we chose to create a W3C CG (https://www.w3.org/community/timesh).

6. It is not clear to us whether your final approach is time tracker data ("punch in/out") based or calendar data ("appointment"/"scheduled") based? Agenda-uren seems the latter category (uren.muze.nl is behind a password so we can't check), while most of the others seem of the former category? Can you clarify?

Both! We will not force a choice for one or the other. Conversion between the two models is very easy, so each tracker can use the approach it prefers. The real value is supporting 30 different formats in 3 apps and promoting this ability to other time tracking apps. We want to show the world that formats don't matter (that much). And provide documentation and tooling to help developers grasp the current reality more quickly.

Our project output will include documentation comparing all known formats and an online tester - converter - validator tool, where a developer can see how to convert one format to another.

7. Would this difference be somehow reflected in the exported data?

See above. Some systems will export to only one format. Other systems will export to a choice of formats, including "hours worked" vs "start time + end time", JSON, csv, CalDAV, etcetera.


8. Time sheets are easy to meddle with. Will there be any digital signatures or timestamping added to the exported data to provide some assurance that the data comes from the source in an unmodified state?

In the one-hop case, both push (webhook) and pull (query endpoint) would rely on TLS. The webhook case would additionally use some sort of shared secret to make sure the data comes from the real source. Timestamping would be a side-effect of when the data moves. For instance, each time B receives data from A, they could compare it to the data that was retrieved last-time, and have a special notification if the change since last time is not an append-only change.

For resharing, W3C-VC could be used. We hadn't considered that, but it's an interesting idea!
The source could then sign all the data they publish using their public key, and the resharer could also provide a timestamp of when they witnessed the publication by the source, using their own public key. We have to see if we could bring this into scope in the final milestones list.

9. Is one export enough, or would there be a need for different views (e.g. this also depends on whether raw data needs to be shared with the customer as proof).

Yes, good point. For auditability it makes sense to publish both the original individual entries, and the aggregate totals. The recipient of the data can then sanity-check whether the aggregating calculation was performed correctly.

For instance, in the Ponder Source part of the milestones (nextcloud-based producer/consumer) we will bridge from this project to the "Peppol for the Masses" project that was funded by NGI Assure in 2021. An aggregated project-timesheet from multiple worker-timesheets will be converted into a Peppol invoice, with totals as line items (unit price = hourly rate) and the detailed source documents as attachments.

For a query endpoint or webhook, typically, the export would be parameterised in two dimensions: Project(s) and Date range.
Say a worker is involved in a number of projects, and for one of these, they need to share with a customer or other stakeholder which hours they claim to have worked on that specific project.
Then the other data from the worker's timetracker database (unrelated to the specific project in question) should stay private.

10. Do you see a way for clients to validate that the same hours were not sold twice?

Good question! This is probably hard to do without centralisation. Also, forcing a worker to sell each hour of the clock only once is not a sufficient guarantee that they actually did work on the project during that hour. Because another similar risk is of course that hours are sold as "worked" while really the worker was at the beach instead. Or maybe they were physically at their work place, but were playing Free Cell instead of doing the work they were paid for.

We think a more useful form of proof in this context would be to link to traceable actions that the worker took during the time. For instance, emails sent, documents edited, code committed into version control, issue tracker items closed, etcetera.

11. Is there some form of transparency in that regard?

Only what each participant chooses to disclose as supporting evidence. When data is exposed from one system to another, it should be clear to both the producer and the consumer what the level of transparency is (e.g. "for your eyes only", "shared among this list of project particants" or "public").

12. How 'auditor-proof' is the proposed setup?

It would make it easier for auditors if timesheets are federated because they get better access to more information. Especially if the data provenance information is kept as metadata. We will definitely explore this in the project, report our findings on how to make timesheet reporting auditor-proof, and propose best practices for this. Good point!

13. Does this work with repeated events, and/or is the reverse trajectory to fill ones agenda based on a template also available? E.g. when you have reserved 'coder on call' time for clients, you don't want to have to manually create and tag every time slot...

Regarding repetition, yes, the simple way, you can use your favourite time tracker tool to generate the repetition, then the tool will generate the repetition, and you will see it in all the other data nodes.

A more advance way is if the data format used is expressive enough to express repetition, like for instance https://icalendar.org/iCalendar-RFC-5545/3-8-5-3-recurrence-rule.html .

When converting from a richer format (with support for repetition) to a simpler one (without support for repetition), we will try to find a way to include the lost detail as metadata or comments. That way, when converting to the simpler format, a repeating event is converted to a series of individual entries, but when converting back to the richer format, the original data can be rehydrated correcly, using these metadata comments.

Regarding the reverse trajectory, in the simple case data only flows from authoritative source to data consumer, but especially in the case of m-ld, the multiple-editor setup is also supported out of the box. There, the calendar app and the timesheet reporting app will have an eventually convergent two-way communication.

So the m-ld-based application will be able to read from a CalDAV server, and also write back to it. That way you could even set up `CalDAV <-> m-ld <-> CalDAV` and sync between two CalDAV servers, with m-ld inbetween.


14. Do you envision a way to integrate with issue trackers or forge applications, or for these to be used instead of time trackers (e.g. Gitlab even has a built-in time tracker) ? E.g. to automatically join commits into the time slot. The same conditions more or less holds for issue trackers as for time trackers: they can be 1:1 linked to remuneration, they contain metadata including specific date/time registration on work done and effort to copy data from them is more or less wasted time.

Yes! We want to integrate with as many tools, platforms, and formats as possible. That definitely also includes Gitlab's built-in time tracker. There, the worker needs to add `/spend` into an issue comment to make it count.

But once they have done this, Federated Timesheets could pick it up from Gitlab's GraphQL API (https://docs.gitlab.com/ee/api/issues.html#get-time-tracking-stats), and the worker wouldn't have to write down their hours worked anywhere else.

There are also time tracker tools that link with issue trackers in other ways, for instance through a browser plugin. Rather than inventing the perfect brain interface, which we think depends on each individual's work flow habits and will not be a one-size-fits-all, the Federated Timesheets project aims to liberate the worker from the need to use any particular tool (give them a choice), or from logging data in more than one tool (avoid repetition). The worker will just be able to use their own preferred tool, whatever it is, and there the data will become machine-readable and make its way onto the network.


















--- below is the content we used during submit-phase:

NGI Assure proposal, 1 Dec 2021

## Data to fill in on https://nlnet.nl/propose/
### Basics
* User Operated Internet Fund
* Contact information: Bänz Schenk et al.
* Project name: Federated Timesheets
* Website / wiki: https://gitter.im/federatedbookkeeping/timesheets
### Abstract: Can you explain the whole project and its expected outcome(s) (max 1200 chars)
This project is quite unique in that it brings together developers from 5 enthusiastic projects:
WikiSuite, m-ld.io, AgendaUren, Muze, and Ponder Source. This collaboration between multiple sovereign teams
is a deliberate part of this research experiment, studying how federated machine-readable data can work
between independent software projects on the user-operated internet.

The topic we chose is timesheet data. Each project has a timesheet system to track billable hours.
Workers often spend time manually filling in this data multiple times.

Instead, we'll make time tracker apps (locally or on a self-hosted server) expose machine-readable
timesheet data through a query endpoint (reader pull) or through a webhook (writer push).

Timesheet data is relatively simple in terms of data format, data replication only flows in one direction,
and there are not too many identities involved in the authentication / authorization of the data source connections.

This simplicity makes the "Federated Timesheets" project an ideal case study for Federated Bookkeeping in general.
We want to show case how our vision of Federated Bookkeeping can make internet users "connected but sovereign".

### Have you been involved with projects or organisations relevant to this project before? And if so, can you tell us a bit about your contributions? (max 10000 characters)
Our team is uniquely qualified to deliver on this proposal because of our combined backgrounds in development, research and data management.

#### Team:

* Bänz Schenk (Switzerland) is a senior php developer at Ponder Source, focused on FOSS development
* George Svarovsky (UK) is an expert in data management, shared data types and linked data, and the lead developer of m-ld, for which he received NGI Assure funding
* Victor Emanouilov (Bulgaria) is a senior developer of WikiSuite, and most involved in WikiSuite's data federation roadmap
* Andrej Bagoutdinov (Germany) is a volunteer researcher at Ponder Source
* Yvo Brevoort (Netherlands) is a senior php developer and visionary at Muze, and has worked on NGI-funded projects like Solid-Nextcloud, Solid-Migrator, and ScienceMesh-Nextcloud
* Lambert Beekhuis (Netherlands) is the founder and developer of "AgendaUren", a hosted timekeeping application that integrates with Google Calendar

#### Advisors:
* Marc Laporte (Canada) is the long-term visionary behind "WikiSuite"
* Michiel de Jong (Netherlands) is the founder of "Ponder Source" and sparked the "Federated Bookkeeping" movement


### Explain what the requested budget will be used for?
The requested budget will mainly be used on interoperability development between existing timesheet tools.

#### 3 Additional Publishers (5kEUR  each):
We already have 2 publishers of Federated Timesheet data working ([uren.muze.nl](https://uren.muze.nl) and [AgendaUren](https://agenda-uren.nl)).
Both are (still) closed-source and this development was financed by Ponder Source and Muze.
We aim to add 3 more:

##### Add an API to [Nextcloud/TimeTracker](https://apps.nextcloud.com/apps/timetracker) (Bänz Schenk)
Nextcloud's open source TimeTracker app has a csv/json export function, but it doesn't have a query API where the user can give out an API token for access to the hours worked on one specific project. This is what we will add, and we will send a pull request to the maintainer of this Nextcloud app.

##### Add an API to [WikiSuite](https://wikisuite.org/) (Victor Emanouilov)
WikiSuite is a widely used open source web server stack, and a lot of timesheet data is stored in Tiki Trackers on WikiSuite installations. As part of the core WikiSuite team, Victor will add an API that allows reading out this data as machine-readable JSON, as a new feature of WikiSuite. The code developed for this feature will be merged into the main open source and freely licensed WikiSuite code repository. 

##### Develop a simple example time tracker app using [m-ld](https://m-ld.org/), which can push its data to a configurable webhook (George Svarovsky)
We think m-ld could be a useful foundation for a time tracker app.
To demonstrate how m-ld could be used, George will create a simple open source and freely licensed time tracker demo app, and include a feature that allows the user to push out all change events to a remote webhook.

#### 1 Superset spec and Documentation (9kEUR, Andrej Bagoutdinov):
* Aggregate the 5 publisher formats into one superset spec
* Submit this standard to the IETF as an Internet Draft
* Help the 3 subscribers understand how to consume data from the 5 publishers.
* Problem ownership, project management
* Documentation, promotion, user support

#### 3 Subscribers (5kEUR each):
##### Newly developed Nextcloud invoice generator that can read from 5 data source types (Bänz Schenk)
Integrating with the Nextcloud app that Michiel de Jong is developing for the "Peppol for the Masses" grant, Bänz will develop a simple invoice generator in PHP, that can compose invoices aggregating data about billable hours, which it receives from any of the 5 data source types. The code for this feature will be open source and freely licensed.

#### Make the time tracker demo app based on m-ld read from the other 4 data source types (George Svarovsky)

Apart from being able to subscribe to a data source from another instance of the same app, George's simple time tracker app will also be able to subscribe to timesheet data from any of the other 4 data source types. The code for this feature will be open source and freely licensed.

#### Make WikiSuite's [Tiki Trackers](https://doc.tiki.org/Trackers) read from the other 4 data source types (Victor Emanouilov)

Apart from being able to subscribe to a data source from another WikiSuite instance, Victor will also enable WikiSuite to subscribe to timesheet data from any of the other 4 data source types. The code for this feature will be open source and freely licensed, and merged into the main WikiSuite code repository.

#### Other (10kEUR):
Apart from these milestones, which are the ones we agreed on with the team so far,
we would like to discuss some options for additional work with you, for the last 20% of the budget. Some options:

##### Spreadsheet plugins
Since many people keep their time tracking data in a spreadsheet, we could see if we can develop open source
plugins for LibreOffice Calc and MicroSoft Excel.

##### Open Source Time Trackers
We want to prepare pull requests that add either a query endpoint or a webhook client into existing
popular open source time tracking tools like Timetagger, Kimai, Pendulums, Titra, Cattr, etc
(see https://medevel.com/20-os-time-tracker-solutions-boost-productivity/).

##### Open Source API Improvements on uren.muze.nl and agenda-uren.nl
Another option would be to open source uren.muze.nl and/or (part of) agenda-uren.nl,
and work on improvements on the timesheet publisher APIs which we already developed using our own time and funds.

#### Overhead (remaining 1kEUR):
* Travel, hosting, other expenses


### Compare your own project with existing or historical efforts. (max 5000 characters)
As far as we know this is the first serious attempt to solve the problem
of manual timesheet data re-entry across multiple disconnected data storage systems. There is quite some prior art though, in spreadsheet technology and in federated data architectures with open protocols.

We could not find much existing work specifically on federated timesheets.
We found one description of a project plan similar to ours, "P2P Time Ledger" (http://confocal-manawatu.pbworks.com/w/page/140705757/P2P%20Time%20Ledger), and we had a video call with the person behind it, Dmitry Solokov, but he confirmed that this project was never executed yet.

In spreadsheet technology there, for instance, is the concept of a "data source", which comes close to the machine-readable query endpoints we will be building, and especially George Svarovsky brings a lot of knowledge about this to the team.

Federated Data Architectures in general is a small but interesting field of technology - examples are the fediverse (Mastodon, ActivityPub, ...), its predecessor "Federated Social Web", the Indie Web (which is basically a successor of the blogosphere), Open Cloud Mesh (a standard for sharing documents between personal cloud servers), Linked Data / Solid, and PDS Interop, and especially Yvo Brevoort and Michiel de Jong have been involved in all of these communities in some way or another over the years.

Learning from past projects trying to reconcile different data formats and API interfaces from independent and unrelated code bases, the approach we will take in this project is the "superset spec" approach. This means that data subscribers are required to support more than one data publisher behaviour. The data publisher can publish the data in a way that is closest to its own software architecture.

### What are significant technical challenges you expect to solve during the project, if any? (max. 8000 characters)

We will have to overcome differences in the data models. Since the data is relatively simple, we expect this to be doable.

We will implement both the "push" and the "pull" setup, since some time tracker systems are server-hosted, and others are client-side on the user's device.
In each interaction, at least one of the two systems involved (data publisher and data subscriber) needs to be addressable via https. We think the plan we have for this will work.

For authentication and authorization, we need to consider various options. We think https + http basic auth will be enough to guarantee optimal security.

We should not fall for the classic "one universal standard that covers everyone's use cases" pitfall (see https://xkcd.com/927/).

Regarding integration with existing spreadsheet software like LibreOffice Calc and MicroSoft Excel, we don't know exactly how their plugin
sandboxing works, so this might prove impossible.

Regarding contributing to existing open source time trackers, we don't know what each project's policy is for accepting external contributions,
so we could contact multiple projects and ask them, and then continue with the ones that respond positively.

### Describe the ecosystem of the project, and how you will engage with relevant actors and promote the outcomes? (max. 8000 characters)

The ecosystem of this projects expands at two levels. At the technological level, there is the Federated Bookkeeping community (https://federatedbookkeeping.org) which has only just started to grow this year, and we see this project as a pilot for years of research and development to come. If we can federate timesheet data, then we can also federate shopping cart data, inventory data, production scheduling data, and any other kind of business and project planning data.

We already received NGI Assure funding for two projects in Federated Bookkeeping: "Peppol for the Masses" (NGI Assure grant to Michiel de Jong, ongoing) and "Collaborative Invoice Composition" (one of two use-cases of NGI Assure grant to George Svarovsky). We hold a community call every Thursday morning, with usually about 6 participants, and there are 30 community members in our Gitter channel. This third grant would give us a great demo to show when pitching the vision of Federated Bookkeeping to innovation departments of big corporations, for which we already made some first connections.

At the end-user level of user-operated internet, Federated Timesheets will facilitate new levels of cooperation and innovation,
as users can easily and more fluidly work together on projects and will no longer have to manually copy-paste their working hours into several closed systems.

We know we would benefit from Federated Timesheets ourselves, in the way our open source projects collaborate in our personal experience.

In fact, Federated Timesheets are already in use between Muze (data publisher) and Ponder Source (data subscriber), and between AgendaUren (data publisher) and Ponder Source (data subscriber).

In the short term, the main impact would be for projects and organizations that use WikiSuite Tiki Trackers for their timesheets. There, contributors would benefit from entering timesheet data only into their own self-hosted WikiSuite instance, instead of having to take extra steps to also manually upload this same data to the project's or client's WikiSuite instance.

Also, depending on which spreadsheet plugins and open source time tracker integrations we would decide to build as part of the 'Other' milestone,
our work would help the users of those software tools to join the user-operated internet of federated timesheets using their own favorite tool
which they are already using.

In the longer term, once this federated network of timesheet servers exists, with five different compatible implementations of a well-documented superset standard, more open source  and SmallTech timesheet apps will join the federation, and the standard will grow in use, until also closed-source and BigTech will adopt this standard, in the same way they already adopt standards like VCard or iCalendar.