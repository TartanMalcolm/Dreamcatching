Scheme Name: Operational Constraints Scheme
OVERALL INTENT:

The Operational Constraints Scheme is designed to document and enforce rules that govern the creation and management of Plans and Routes within the CRM system of a trucking company. These rules ensure compliance with internal policies and operational capacities, enhancing logistical efficiency and adherence to set protocols.

MUSTs:

Be a valid, internally consistent JSON.
Include fields for a unique identifier (constraintId), the scope of application (scope), detailed description of the constraint (description), and the level of enforcement (enforcementLevel).
Clearly define whether each constraint applies to Plans, Routes, or both to prevent any operational misinterpretations.
Specify whether the constraint is mandatory or optional, ensuring clarity on compliance requirements.
SHOULDs:

Cover all major operational parameters that could significantly impact the efficiency, legality, and effectiveness of Routes and Plans.
Provide comprehensive, clear descriptions to ensure that all users and systems interacting with the constraints understand their implications and requirements.
COULDs:

Later expand to include more dynamic or complex constraints as the business scales or external regulations evolve, addressing needs like environmental considerations or new traffic regulations.
Incorporate feedback mechanisms to assess the impact of constraints on operational efficiency and adjust them as necessary.
MUST NOTs:

Leave any ambiguity concerning the scope (Plan, Route, or Both) and enforcement level (Mandatory or Optional) of each constraint, as this could lead to non-compliance or operational inefficiencies.
SCHEMA:

{
  "type": "object",
  "properties": {
    "constraintId": {
      "type": "string",
      "description": "Unique identifier for the constraint"
    },
    "scope": {
      "type": "string",
      "enum": ["Plan", "Route", "Both"],
      "description": "Scope of application of the constraint"
    },
    "description": {
      "type": "string",
      "description": "Detailed description of the constraint"
    },
    "enforcementLevel": {
      "type": "string",
      "enum": ["Mandatory", "Optional"],
      "description": "Indicates how strictly the constraint must be followed"
    }
  },
  "required": ["constraintId", "scope", "description", "enforcementLevel"]
}