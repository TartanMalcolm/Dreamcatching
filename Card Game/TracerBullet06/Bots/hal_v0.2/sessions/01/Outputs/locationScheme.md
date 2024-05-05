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