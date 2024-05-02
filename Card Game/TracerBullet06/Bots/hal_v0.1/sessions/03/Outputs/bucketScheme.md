Scheme Name: Bucket Scheme
OVERALL INTENT:

The Bucket Scheme is intended to define geographic areas for the purpose of organizing and managing routes within the CRM system of a trucking company. Each bucket contains multiple routes but is confirmed to a specific geographical area defined initially by postcodes and potentially by more complex shapes like polygons in the future.

MUSTs:

Be a valid, internally consistent JSON.
Include fields for the bucket identifier and a list of associated postcodes that define the geographic area.
Enhance operational efficiencies by clearly grouping related routes and ensuring that all routes linked to a bucket fall within its geographical confines.
SHOULDs:

Provide clear descriptions for each field to ensure correct data entry and ease of use.
Facilitate geographic delimitation that may evolve to include more detailed representations like coordinates or polygons, compatible with GIS systems for potential future needs.
COULDs:

Prepare for future integration of GIS data formats for detailed geographic rendering.
Include metadata that may help in managing or visualizing the areas such as labels, historical changes, or notes on specific zoning laws or restrictions.
MUST NOTs:

Must not allow routes to be assigned to buckets if they fall outside the defined geographical boundaries to prevent operational conflicts and inefficiencies.
SCHEMA:

{
  "type": "object",
  "properties": {
    "bucketID": {
      "type": "string",
      "description": "Unique identifier for the geographic bucket"
    },
    "postcodes": {
      "type": "array",
      "items": {
        "type": "string",
        "description": "Postcode defining part of the bucket's geographic area"
      },
      "description": "Array of postcodes that collectively define the bucket's geographic boundaries"
    }
  },
  "required": ["bucketID", "postcodes"]
}
