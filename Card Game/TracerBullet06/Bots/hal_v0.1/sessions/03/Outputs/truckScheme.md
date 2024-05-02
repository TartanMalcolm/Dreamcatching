Scheme Name: Truck Information Scheme
OVERALL INTENT:

The Truck Information Scheme is designed to comprehensively capture and manage data related to each truck in the fleet, including its current operational status, assigned driver, and associated bucket. This scheme facilitates effective fleet management and operational readiness within the CRM system.

MUSTs:

Be a valid, internally consistent JSON.
Include fields for a unique truck identifier (truckId), basic information about the truck (make, model, year), the bucket identifier indicating its current geographic assignment (bucketId), the driver identifier (driverId), and status (in operation or unavailable).
Ensure that each truck is linked to a specific driver via driverAssignmentScheme and a specific bucket, ensuring clear accountability and location tracking.
SHOULDs:

Provide detailed descriptions for each field to ensure clarity and ease of data use.
Be designed to seamlessly integrate with other related schemes, such as bucketScheme and driverAssignmentScheme, for cohesive operational insights.
COULDs:

Include additional fields detailing maintenance schedules or other operational notes that might affect the truck’s availability or performance.
Prepare for future expansions to include real-time GPS tracking data or integration with automated dispatch systems.
MUST NOTs:

Omit essential data fields such as truckId, bucketId, driverId, or status, as these are crucial for the effective management and tracking of the fleet.
SCHEMA:

{
  "type": "object",
  "properties": {
    "truckId": {
      "type": "string",
      "description": "Unique identifier for the truck"
    },
    "make": {
      "type": "string",
      "description": "Manufacturer of the truck"
    },
    "model": {
      "type": "string",
      "description": "Model of the truck"
    },
    "year": {
      "type": "integer",
      "description": "Year the truck was manufactured"
    },
    "bucketId": {
      "type": "string",
      "description": "Identifier of the bucket the truck is currently assigned to"
    },
    "driverId": {
      "type": "string",
      "description": "Identifier of the driver currently assigned to the truck"
    },
    "status": {
      "type": "string",
      "enum": ["In Operation", "Unavailable"],
      "description": "Current operational status of the truck"
    }
  },
  "required": ["truckId", "make", "model", "year", "bucketId", "driverId", "status"]
}
