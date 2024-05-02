Scheme Name: Customer Scheme
OVERALL INTENT:

The Customer Scheme is engineered to capture essential customer data in a CRM system designed for a trucking company, supporting efficient logistical management through tailored routing based on geographic constraints.

MUSTs:

Be a valid, internally consistent JSON.
Include fields for name, address (including street, city, state, postal code), telephone number, and account number.
Maintain data integrity, consistency, and deduplication with other schemes it interacts with, like potential routing or geographic bucket schemes.
SHOULDs:

Provide clear and helpful descriptions for each field to ensure correct data entry and ease of data use. This assists in minimizing potential data entry errors and enhances usability.
COULDs:

Consider the potential inclusion of fields such as country or specific subdivisions in the address, aiding extended functionalities like international operations or more granular routing.
MUST NOTs:

The schema must not omit any of the required fields as this could lead to incomplete records, potentially disrupting operational efficiency and management processes.
SCHEMA:

{
  "type": "object",
  "properties": {
    "name": {
      "type": "string",
      "description": "Full name of the customer"
    },
    "address": {
      "type": "object",
      "properties": {
        "street": {
          "type": "string",
          "description": "Street part of the postal address"
        },
        "city": {
          "type": "string",
          "description": "City part of the postal address"
        },
        "state": {
          "type": "string",
          "description": "State part of the postal address"
        },
        "postalCode": {
          "type": "string",
          "description": "Postal code of the customer's address"
        }
      },
      "required": ["street", "city", "state", "postalCode"]
    },
    "telephoneNumber": {
      "type": "string",
      "description": "Contact telephone number of the customer"
    },
    "accountNumber": {
      "type": "string",
      "description": "Unique account number assigned to the customer"
    }
  },
  "required": ["name", "address", "telephoneNumber", "accountNumber"]
}
