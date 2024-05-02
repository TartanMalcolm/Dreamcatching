Scheme Name: Event Log Scheme
OVERALL INTENT:

The Event Log Scheme is designed to chronologically record activities and interactions involving multiple entities within the CRM system, facilitating accountability, system audits, and operational insights. It captures the nature of each event, the participants involved, and the related operational context.

MUSTs:

Be a valid, internally consistent JSON.
Include fields for event identifier (eventId), timestamp, descriptive details of the event (description), actor, and contextual links to other CRM system entities.
Ensure that each entry has a unique ID and timestamp to preserve the sequence and timing integrity of logged events.
SHOULDs:

Maintain concise, clear descriptions and actor identification to ensure accountability and clarify the role of various individuals or entities in specific actions or decisions.
Utilize thoroughly defined context structures to link each event with relevant CRM entities such as customers, plans, or buckets.
COULDs:

Later incorporate more detailed context categories, example, mapping IDs to names or roles via a lookup for enhanced readability and analysis.
Expand to include automated flags or alerts based on specific event types or actor actions that might require immediate attention or follow-up.
MUST NOTs:

Allow any ambiguity in the event's chronological sequence, actor involvement, or associated CRM entities, which could lead to operational confusion or misinterpretations.
SCHEMA:

{
  "type": "array",
  "items": {
    "type": "object",
    "properties": {
      "eventId": {
        "type": "string",
        "description": "Unique identifier for the event"
      },
      "timestamp": {
        "type": "string",
        "format": "date-time",
        "description": "ISO 8601 formatted timestamp indicating when the event occurred"
      },
      "description": {
        "type": "string",
        "description": "Brief description of the event"
      },
      "actor": {
        "type": "string",
        "description": "The entity or individual responsible for the event"
      },
      "interactionType": {
        "type": "string",
        "enum": ["Customer Interaction", "Route Planning", "Truck Usage"],
        "description": "The category of interaction that the event pertains to"
      },
      "context": {
        "type": "object",
        "description": "Contextual data linking the event to other CRM entities",
        "properties": {
          "customerId": {
            "type": "string",
            "description": "Identifier of the customer involved, if applicable"
          },
          "routeId": {
            "type": "string",
            "description": "Identifier of the route involved, if applicable"
          },
          "planId": {
            "type": "string",
            "description": "Identifier of the plan involved, if applicable"
          },
          "truckId": {
            "type": "string",
            "description": "Identifier of the truck involved, if applicable"
          }
        }
      }
    }
  }
}