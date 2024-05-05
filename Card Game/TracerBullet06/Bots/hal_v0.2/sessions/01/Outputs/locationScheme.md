## Location Scheme
- **Scheme Name**: Location

### OVERALL INTENT
To provide centralized and accurate management of geographic data associated with various aspects of trucking operations, ensuring all entities within the CRM utilize consistent location information.

### MUSTs
1. **Maintain Precise Geographic Data**: Ensure all location data stored in the scheme are accurate and reflect the correct geographic coordinates.
2. **Update Regularly**: Continuously update the location data to reflect changes due to operational shifts or geographic developments.

### SHOULDs
1. **Support Real-time Updates**: Implement capabilities to allow real-time updates to location data, enhancing responsiveness in operational planning and execution.
2. **Integrate Geofencing**: Support geofencing capabilities to trigger alerts or actions based on geographical boundaries.

### COULDs
1. **Provide Reverse Geocoding Services**: Offer functionality to convert geographic coordinates into a human-readable address, which could be useful for logistical planning and reporting.

### MUST NOTs
1. **Use Inaccurate or Outdated Data**: Avoid the utilization of known outdated or incorrect geographic data to prevent operational inefficiencies and potential safety issues.

SCHEMA
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