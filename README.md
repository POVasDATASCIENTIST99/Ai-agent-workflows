# AI Agent Workflows

Two automated AI agent workflows that let a customer get information at any time, without waiting for a person. I designed and built them as a solo project in 2026. They are demonstrations, not live systems with real customers.

## Workflow 1: Shipment tracking (inbound voice agent)
A customer calls and the agent answers. It follows a written prompt and uses two tools during the call:
- **lookup_shipment:** calls a shipment API and reads back the shipment's status.
- **verify_carrier:** looks up a carrier's MC number through an API to check that the carrier is real.

Why it helps: a customer can call at any hour and get live shipment information, and the support team handles only the cases that need a person.

## Workflow 2: Weather delay check
A user names a city and the agent returns the current weather for that city from a live public data source.

Example use case: a house construction business could use it to decide where to send crews. Dry and sunny sites get the building and digging crews, and sites where rain is coming get the leakage, water-clogging, and drainage crews. The same logic applies to any business that plans work around weather, such as deliveries, events, or field service.

## What they use
- Branching logic that changes what the agent does based on what the caller says
- Live lookups from APIs during the conversation
- A webhook that logs results to a spreadsheet when a direct integration was not available
- Severity-style routing so urgent cases are handled first

## Screenshots
![Shipment tracking workflow](shipment-tracking.png)
![Weather delay check workflow](weather-delay-check.png)

## Limits
- Built to demonstrate the design, not used with real customers.
- The platform and its data sources are not named here.

## Author
Vaddadi Sthitapragnya
