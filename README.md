# timesheets
Federated Timesheets Project. Gitter: https://gitter.im/federatedbookkeeping/timesheets

We are still in the investigative phase, analysing what time tracker apps exist and which CSV/JSON/XML/... formats they export to.
See [app-list.md](./apps-list.md) and [data-formats/](./data-formats/).

# Management Summary

This project brings together developers from WikiSuite, m-ld.io, Muze and Ponder Source in a collaboration
to deliberately research how federated machine-readable data can work between independent software projects on the user-operated internet. We want to showcase how our vision of Federated Bookkeeping can make internet users "connected but sovereign".

Each project's timesheet system that tracks billable hours will be extended with time tracker apps (locally or on a self-hosted server) to expose machine-readable
timesheet data through a query endpoint (reader pull) or through a webhook (writer push).

Furthermore, a W3C interest group "federated timesheets" has been started that will contain and maintain a repository of time tracker schemas and extend this continuously in an orderly fashion to enable developers to import recipients' schemas as well as add their own to the repository.
