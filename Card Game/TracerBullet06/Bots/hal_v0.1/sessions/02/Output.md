1. Customer Schema
INTENT: To reliably store and manage detailed customer information necessary for operational and service purposes.
MUST: Accurately capture essential customer details.
SHOULD: Allow easy retrieval and modification of customer information for service and operational purposes.
COULD: Support additional metadata for future marketing or loyalty programs.
MUST NOT: Compromise any personal data security or integrity.
SCHEMA:
{
  "customerId": "string",
  "name": "string",
  "address": {
    "street": "string",
    "city": "string",
    "state": "string",
    "postalCode": "string"
  },
  "telephoneNumber": "string",
  "accountNumber": "string"
}
2. Route Schema
INTENT: To manage routing information, linking customers and geographical areas to ensure operations remain within designated routes.
MUST: Include detailed routing paths linked to geographical areas.
SHOULD: Optimize route planning to enhance operational efficiency.
COULD: Integrate real-time tracking capabilities in future enhancements.
MUST NOT: Overlap routes in a way that could lead to operational inconsistencies.
SCHEMA:
{
  "routeId": "string",
  "bucketId": "string",
  "customerIds": ["string"]
}
3. Plan Schema
INTENT: Designed to manage and schedule route operations, aligning them with specific times and dates.
MUST: Pair routes with specific operational times.
SHOULD: Allow for dynamic adjustments based on operational feedback.
COULD: Provide predictions for future route needs based on historical data.
MUST NOT: Schedule overlapping routes without proper checks.
SCHEMA:
{
  "planId": "string",
  "routeId": "string",
  "truckId": "string",
  "driverId": "string",
  "weekStarting": "date",
  "scheduledTimes": [
    {
      "date": "date",
      "time": "time"
    }
  ]
}
4. Operational Constraints Schema
INTENT: To impose constraints that ensure operational compliance and efficiency.
MUST: Clearly define operational boundaries and rules.
SHOULD: Be dynamically adjustable as operations evolve.
COULD: Allow for the integration of AI to predict and suggest operational adjustments.
MUST NOT: Impose constraints that are infeasible within the current operational capacities.
SCHEMA:
{
  "constraintId": "string",
  "scope": "string", // ["Plan", "Route", "Both"]
  "description": "string",
  "enforcementLevel": "string" // ["Mandatory", "Optional"]
}
5. Customer Service Policies Schema
INTENT: To guide interactions under specified service policies to handle changes and requests effectively.
MUST: Clearly outline applicable policies for different scenarios.
SHOULD: Foster a customer-centric approach in handling inquiries.
COULD: Incorporate feedback mechanisms to refine policies continually.
MUST NOT: Provide loopholes that might lead to service standard inconsistencies.
SCHEMA:
{
  "policyId": "string",
  "type": "string", // ["Option", "Rule", "Guideline"]
  "description": "string",
  "scope": "string", // ["Plan", "Route", "General"]
  "approvalRequirement": "boolean"
}
6. Event Log Schema
INTENT: To maintain a chronological log of significant events, capturing essential details and changes to ensure transparency.
MUST: Log all critical interactions and changes accurately.
SHOULD: Provide easy querying capabilities for logged events.
COULD: Use the event log for analytical insights into operations.
MUST NOT: Miss logging any events that impact operational or customer contextual data.
SCHEMA:
{
  "eventId": "string",
  "timestamp": "date-time",
  "description": "string",
  "actor": "string",
  "context": {
    "customerId": "string",
    "planId": "string",
    "routeId": "string",
    "otherContexts": {}
  }
}
7. Truck Schema
INTENT: To manage all pertinent information about each truck in the fleet, ensuring each truck's status and capability are accurately monitored and utilized.
MUST: Track essential identification and status information for each truck.
SHOULD: Inform operational decisions regarding truck deployment and maintenance.
COULD: Integrate with systems for real-time tracking and advanced diagnostics.
MUST NOT: Exclude any critical data that compromises fleet management or compliance.
SCHEMA:
{
  "truckId": "string",
  "model": "string",
  "licensePlate": "string",
  "status": "string",
  "capacity": "integer",
  "currentDriverId": "string",
  "lastServiceDate": "date"
}
8. Driver Schema
INTENT: To handle all relevant data about individual drivers to synchronize driver assignments with truck deployments and route plans.
MUST: Include comprehensive identification and status information for each driver.
SHOULD: Facilitate operational planning and scheduling by linking drivers to trucks and planned routes.
COULD: Enhance safety and training programs via detailed records of driver qualifications and history.
MUST NOT: Compromise the privacy and security of personal and sensitive data of drivers.
SCHEMA:
{
  "driverId": "string",
  "name": "string",
  "licenseNumber": "string",
  "status": "string",
  "contactInfo": {
    "email": "string",
    "phone": "string"
  },
  "qualification": "string",
  "hireDate": "date"
}
