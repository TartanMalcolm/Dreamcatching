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
  "type": "object",
  "properties": {
    "locationId": {
      "type": "string",
      "description": "Unique identifier for the location"
    },
    "address": {
      "type": "string",
      "description": "Physical address of the location"
    },
    "latitude": {
      "type": "string",
      "description": "Geographic latitude of the location"
    },
    "longitude": {
      "type": "string",
      "description": "Geographic longitude of the location"
    }
  },
  "required": ["locationId", "address", "latitude", "longitude"]
}