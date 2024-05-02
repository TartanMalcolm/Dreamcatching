Scheme Name: Route Scheme
OVERALL INTENT:

The Route Scheme is designed to structure and manage route data within a CRM system for a trucking company. Each route consists of an ordered list of locations, each associated with a customer, and is confined to a specific geographic 'bucket', ensuring efficient management and planning of delivery paths within distinct areas.

MUSTs:

Be a valid, internally consistent JSON.
Include fields for the route identifier, list of location identifiers (linked to customer scheme data), and the bucket identifier it belongs to.
Ensure that all routes remain constrained within a single bucket.
Each location within the route must be linked or related to customer data to facilitate clear logistical planning.
SHOULDs:

Include clear descriptions for each field and linkage to the appropriate data from other schemes (e.g., customer data for location identifiers) to facilitate understanding and correct usage of the data.
Provide foundational structure that allows future expansion for storing and representing geographic area data more complexly, such as polygons for greater precision in routing.
COULDs:

The scheme could prepare for integration with mapping tools by anticipating the inclusion of more complex geographic data structures such as coordinates or polygons.
Consider including optimization or sequence algorithms suggestions for route planning based on geographic or temporal parameters.
MUST NOTs:

A route must not include locations from multiple buckets, ensuring each route's geographic containment for logistical efficiency and planning simplicity.
Must not omit any essential linkages to customer data for any location in the route.
SCHEMA:

{
  "type": "object",
  "properties": {
    "routeId": {
      "type": "string",
      "description": "Unique identifier for the route"
    },
    "bucketId": {
      "type": "string",
      "description": "Identifier for the bucket or geographic area this route covers"
    },
    "locations": {
      "type": "array",
      "items": {
        "type": "object",
        "properties": {
          "locationId": {
            "type": "string",
            "description": "Identifier linking to a customer's location"
          },
          "customerID": {
            "type": "string",
            "description": "Unique customer identifier linked to the location"
          }
        },
        "required": ["locationId", "customerID"]
      },
      "description": "Ordered list of locations within the route, each linked to a customer"
    }
  },
  "required": ["routeId", "bucketId", "locations"]
}