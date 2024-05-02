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
    "name": {
      "type": "string",
      "description": "Full name of the driver"
    },
    "dateOfBirth": {
      "type": "string",
      "format": "date",
      "description": "Date of birth of the driver"
    },
    "licenseNumber": {
      "type": "string",
      "description": "Driver's license number"
    },
    "licenseExpiry": {
      "type": "string",
      "format": "date",
      "description": "Expiration date of the driver's license"
    },
    "contactInfo": {
      "type": "object",
      "properties": {
        "email": {
          "type": "string",
          "description": "Driver's email address"
        },
        "phone": {
          "type": "string",
          "description": "Driver's contact phone number"
        },
        "address": {
          "type": "string",
          "description": "Driver's home address"
        }
      },
      "required": ["email", "phone"],
      "description": "Contact information of the driver"
    }
  },
  "required": ["driverId", "name", "dateOfBirth", "licenseNumber", "licenseExpiry", "contactInfo"]
}