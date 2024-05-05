Scheme Name: Driver Scheme
OVERALL INTENT:

The Driver Scheme is intended to maintain a registry of drivers, keeping essential personal and professional information. It serves as the central reference for identifying drivers within the CRM system, allowing other schemes, specifically planScheme, to reference drivers for assigning specific driving tasks and routes.

MUSTs:

Be a valid, internally consistent JSON.
Include fields for the unique driver identifier (driverId), driver's personal information (name, date of birth), and professional details (license number, license expiration date).
Ensure that each driver's information is updated and includes all necessary details for legal and operational requirements.
SHOULDs:

Include contact information to facilitate communication and coordination.
Provide clear, detailed descriptions for each field to ensure ease of understanding and correct use, minimizing potential errors during data entries.
COULDs:

Later include additional fields related to driver performance metrics or feedback scores to aid in performance reviews or training needs assessments.
MUST NOTs:

Omit any of the required fields that are crucial for operational compliance and identity verification of the driver.
SCHEMA:

{
  "type": "object",
  "properties": {
    "driverId": {
      "type": "string",
      "description": "Unique identifier for the driver"
    },
    "firstName": {
      "type": "string",
      "description": "First name of the driver"
    },
    "lastName": {
      "type": "string",
      "description": "Last name of the driver"
    },
    "licenseNumber": {
      "type": "string",
      "description": "Driver's license number"
    },
    "currentTruckId": {
      "type": "string",
      "description": "Identifier for the truck currently assigned to the driver"
    },
    "contactDetails": {
      "type": "object",
      "properties": {
        "email": {
          "type": "string",
          "description": "Driver's email address"
        },
        "phoneNumber": {
          "type": "string",
          "description": "Driver's phone number"
        }
      },
      "required": ["email", "phoneNumber"]
    }
  },
  "required": ["driverId", "firstName", "lastName", "licenseNumber", "currentTruckId", "contactDetails"]
}