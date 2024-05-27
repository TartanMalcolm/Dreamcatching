These are the DEFINITIONS of terms we use.  YOU ARE ONLY to use these definitions.  When you have read and understood them, you are to say "Definitions Loaded".

# CRM DEFINITIONS

## General Terms
### PLAN
A sequence of STEPS that performs a FUNCTION.
### FUNCTION:
This is a natural language explanation of what the PLAN is intending to do.
### DESCRIPTION
This is a natural language explanation that goes alongside EVERY field in the JSON format.  It is there to enable the next steps to execute knowing the context in which the PLAN was built, as well as understanding the structure of the JSON.
### STEPS
Steps are a wrap of the data of ACTION, DATASOURCE and INPUT.  Together these are used as instructions to other bots about what to do and how to respond.
### ACTION
Actions are ALWAYS in two parts.  The first is what to do for this step, the second is what data is required back.  E.g. "action": "List all customers with a collection next weekend.  Provide customer IDs only",
### DATASOURCE
The JSON bot that can best respond to the ACTION.  These are listed below and map to the Example CRM JSON Data.
### INPUT
This is the information that is required to carry out the action, possibly from a previous step.
### ACTOR
The user requesting this plan to be executed.  An ACTOR must be listed in List of customer service agent records, List of duty manager records or List of driver records.
### ROLE
The role, from the List of role records, that the ACTOR has.  Roles provide PERMISSIONS.
### PERMISSIONS
Rules that MUST BE FOLLOWED to allow the PLAN to be created.

## DataSource Specific Terms


## Customer Service Agent Data
### Agent
The data concerning individuals who are employed as customer service agents.
### agentId
A unique ID, one per agent. The format is e.g. "CSA-001," where "CSA" identifies it as a Customer Service Agent ID, and "001" is a number.
### name
The full name of the agent, including:
#### firstName
The agent's first name.
#### lastName
The agent's last name.
### contactDetails
The contact information for the agent, including:
#### email
The agent's preferred contact email address.
#### phone
The agent's preferred phone contact number.


## Customer Data
### Customer
The data concerning the people who have paid for the pickup service.
### customerId
A unique ID, one per customer.  The format is e.g. "CUST-001", where "CUST" identifies it as a Customer ID, and "001" is a number.
### locationId
A unique ID, one per customer.  The format is e.g. "CUST-001", where "CUST" identifies it as a Customer ID, and "001" is a number.
### name
#### firstName
The customer's first name.
#### lastName
The customer's last name
### contactDetails
#### email
The customer's preferred contact email address.
#### phone
The customer's preferred phone contact number.

## Customer Service Policy Data
### Policy
The data concerning the customer service policies meant to guide agents’ actions.
### policyId
A unique ID, one per policy. The format is e.g. "CSP-001," where "CSP" identifies it as a Customer Service Policy ID, and "001" is a number.
### type
The category of the policy, which describes its nature. Examples include "Option," "Rule," or "Guideline."
### description
A detailed explanation of what the policy entails and how it should be implemented.
### scope
The context or situation to which the policy applies. Examples include "Plan," "General," "Incident," "Post-Interaction," "Pre-Interaction," or "During Interaction."
### approvalRequirement
The person or role required to approve actions under this policy. Examples include "Duty Manager" or "None."
### action
The specific actions required by the policy for agents to follow, if any. These actions include logging events, contacting customers, or updating records.


## Driver Data
### Driver
The data concerning individuals who are employed to drive the company's trucks.
### driverId
A unique ID, one per driver. The format is e.g. "DRV-001," where "DRV" identifies it as a Driver ID, and "001" is a number.
### name
The full name of the driver, including:
#### firstName
The driver's first name.
#### lastName
The driver's last name.
### licenseNumber
A unique alphanumeric identifier issued to the driver as their driving license number.
### currentTruckId
A unique ID of the truck currently assigned to the driver. The format is e.g. "TRUCK-01," where "TRUCK" identifies it as a Truck ID, and "01" is a number.
### contactDetails
The contact information for the driver, including:
#### email
The driver's preferred contact email address.
#### phone
The driver's preferred phone contact number.


## Duty Manager Data
### Manager
The data concerning individuals who hold the position of Duty Manager.
### managerId
A unique ID, one per manager. The format is e.g. "DM-001," where "DM" identifies it as a Duty Manager ID, and "001" is a number.
### name
The full name of the manager, including:
#### firstName
The manager's first name.
#### lastName
The manager's last name.
### contactDetails
The contact information for the manager, including:
#### email
The manager's preferred contact email address.
#### phone
The manager's preferred phone contact number.
### permissions
A list of privileges or areas of responsibility assigned to the manager. Examples include "Operational Adjustment," "System Oversight," "Decision Making," and "Emergency Handling."




## Event Log Data
### Event
The data concerning individual events recorded in the system.
### eventId
A unique ID, one per event. The format is e.g. "event001."
### timestamp
The date and time when the event occurred, formatted as ISO 8601.
### content
A brief description of the event and its details.
### actor
The individual or role responsible for the event, including:
#### role
The role of the individual responsible for the event. Examples include "Customer Service Agent," "Duty Manager," or "Driver."
#### name
The name of the individual responsible for the event.
### interactionType
The type of interaction or activity represented by the event. Examples include "Customer Interaction," "Route Planning," or "Truck Usage."
### context
Additional contextual data relevant to the event, where appropriate, including:
#### customerId
A unique ID referring to the customer involved in the event. The format is e.g. "CUST-002."
#### routeId
A unique ID referring to the delivery route involved in the event. The format is e.g. "ROUTE-005."
#### planId
A unique ID referring to the plan involved in the event. The format is e.g. "PLAN-012."
#### truckId
A unique ID referring to the truck involved in the event. The format is e.g. "TRUCK-103."

## Location Data
### Location
The data concerning specific geographical locations important to the operations.
### locationId
A unique ID, one per location. The format is e.g. "LOC-001," where "LOC" identifies it as a Location ID, and "001" is a number.
### address
The full address of the location, including street name, city, and state.
### latitude
The geographical latitude of the location, in decimal degrees.
### longitude
The geographical longitude of the location, in decimal degrees.


## Operational Constraint Data
### Constraint
The data concerning specific operational constraints that must be adhered to.
### constraintId
A unique ID, one per constraint. The format is e.g. "OC-001," where "OC" identifies it as an Operational Constraint ID, and "001" is a number.
### scope
The specific area or operational context to which the constraint applies. Examples include "Route," "Plan," or "Both."
### description
A detailed explanation of the constraint, including its requirements and purpose.
### enforcementLevel
The level of enforcement required for the constraint. Examples include "Mandatory."


## Role Data
### Role
The data concerning specific roles within the organization.
### roleName
The name of the role. Examples include "Duty Manager," "Customer Service Agent," and "Driver."
### responsibilities
A list of key tasks and duties that the role is responsible for. Examples include "Route planning and optimization," "Handling customer queries and complaints," and "Following assigned routes."
### permissions
A list of privileges or permissions granted to the role. Examples include "Edit route plans," "View customer details," and "Mark deliveries as completed."


## Route Plan Data
### Route Plan
The data concerning specific route plans designed to manage deliveries and pickups.
### routePlanId
A unique ID, one per route plan. The format is e.g. "RP-01," where "RP" identifies it as a Route Plan ID, and "01" is a number.
### planDescription
A detailed explanation of the route plan, including its focus and objective. Examples include preferences for specific times or days of the week.
### activeFrom
The start date when the route plan becomes active, formatted as YYYY-MM-DD.
### activeTo
The end date when the route plan ceases to be active, formatted as YYYY-MM-DD.
### scheduledRoutes
Details of the routes scheduled under the plan, including:
#### Date
The specific date of the scheduled route, formatted as YYYY-MM-DD.
#### Locations
A list of location IDs included in the route. Examples include "LOC-001," "LOC-003."
#### Estimated Time
The estimated time required to complete the route. Examples include "2 hours," "3 hours."
### bucketId
A unique ID associated with the bucket to which this route plan belongs. The format is e.g. "BUCKET-01."
