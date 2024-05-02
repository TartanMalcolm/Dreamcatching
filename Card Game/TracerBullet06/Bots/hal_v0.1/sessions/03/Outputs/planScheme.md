Scheme Name: Plan Scheme
OVERALL INTENT:

The Plan Scheme is established to add temporal dimensions to the routing operations in the CRM system of a trucking company, specifying when particular routes are active. It will connect route details with specific dates and times, aiding in operational planning and management on a weekly basis.

MUSTs:

Be a valid, internally consistent JSON.
Include fields for the plan identifier (planId), the identifier linking to a pre-defined route (routeId), the start of the week (weekStarting), and a detailed schedule of times when the route is to be driven (scheduledTimes).
Ensure all required temporal data is included to define when routes will be executed, avoiding any ambiguity in route activation.
SHOULDs:

Cover a complete week’s schedule to allow effective planning and resource allocation, ensuring the CRM system can efficiently manage weekly operations.
Provide clear descriptions for each time-related field to ensure ease of understanding and use.
COULDs:

Later incorporate elements such as adjustments for rescheduling or cancellations, allowing operational flexibility based on real-time needs or unforeseen changes.
Enhance monitoring and reporting features to manage and analyze route efficiency and timely executions.
MUST NOTs:

Omit any temporal data essential for the operational use of routes, as this would hinder the effectiveness of logistical and scheduling processes.
SCHEMA:

{
  "type": "object",
  "properties": {
    "planId": {
      "type": "string",
      "description": "Unique identifier for the plan"
    },
    "routeId": {
      "type": "string",
      "description": "Identifier of the route this plan corresponds to, linking to the previously defined 'Route' schema"
    },
    "weekStarting": {
      "type": "string",
      "format": "date",
      "description": "The date marking the beginning of the week for which this plan is active"
    },
    "scheduledTimes": {
      "type": "array",
      "description": "List of dates and times when the route is scheduled to be driven within the week",
      "items": {
        "type": "object",
        "properties": {
          "date": {
            "type": "string",
            "format": "date",
            "description": "Specific date when the route is driven"
          },
          "time": {
            "type": "string",
            "format": "time",
            "description": "Time of the day when the route starts"
          }
        },
        "required": ["date", "time"]
      }
    }
  },
  "required": ["planId", "routeId", "weekStarting", "scheduledTimes"]
}
