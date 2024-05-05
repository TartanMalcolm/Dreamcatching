Scheme Name: Roles and Responsibilities Scheme
OVERALL INTENT:
The Roles and Responsibilities Scheme aims to provide a structured framework that defines and limits the roles and responsibilities of various human users interacting with the CRM system of a trucking company. This is designed to maintain operational efficiency, compliance, and effective decision-making across different CRM interactions.

MUSTs:
Be a valid, internally consistent JSON.
Clearly enumerate responsibilities specific to each role to prevent overlap and ensure clear demarcation of duties.
Link each role to their respective operational schemes such as Routes, Customers, Trucks ensuring seamless integration.
Include mechanisms for audit trails to track decisions made by the Duty Manager and Customer Service Agents.
SHOULDs:
Facilitate clear definitions that support scalability and flexibility for evolving business needs without conflicting with established responsibilities.
Provide access levels for each role to protect sensitive information pertinent to the operations and interactions within the CRM.
COULDs:
Incorporate a feedback mechanism for roles like Drivers and Customer Service Agents to suggest improvements in operational processes or customer relations.
Offer role-based customization options that allow adjusting certain scheme parameters according to specific user needs or business growth phases.
MUST NOTs:
Duty Manager must not bypass CRM system constraints and operational policies laid out in the Operational Constraints Scheme.
Customer Service Agents must not make changes to customer or route data without following proper authorization and verification processes.
Drivers must not access or alter customer or operational data beyond their designated privilege levels.
Customers must not be granted access to back-end operational data or sensitive company information.
SCHEMA:
{
  "type": "object",
  "description": "Defines roles and responsibilities within the CRM system.",
  "properties": {
    "userRoles": {
      "type": "array",
      "description": "Delineates the specific roles and bounds of their responsibilities.",
      "items": {
        "type": "object",
        "properties": {
          "roleID": {
            "type": "string",
            "description": "Unique identifier for the role"
          },
          "roleName": {
            "type": "string",
            "description": "Name of the role"
          },
          "responsibilities": {
            "type": "array",
            "items": {
              "type": "string",
              "description": "Detailed list of role-specific duties and limits"
            },
            "description": "Detailed responsibilities and operational limits"
          },
          "interactionPoints": {
            "type": "array",
            "items": {
              "type": "string",
              "description": "CRM components the role interacts with, detailing scope of interaction"
            },
            "description": "Defined interaction points within the CRM system"
          }
        },
        "required": ["roleID", "roleName", "responsibilities"]
      }
    }
  },
  "required": ["userRoles"]
}