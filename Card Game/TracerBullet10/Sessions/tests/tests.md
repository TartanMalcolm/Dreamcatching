
## Customer
### Customer Data Validation

1. Are all of the customer IDs unique?
2. Are all of the customer IDs in the correct format (e.g., "CUST-###")?
3. Do all first names contain only alphabetic characters?
4. Do all last names contain only alphabetic characters?
5. Do all email addresses follow a valid email format?
6. Do all phone numbers follow a valid phone number format (e.g., "555-####")?
7. Do all contactDetails objects contain both an email and a phone field?
8. Are all contactDetails complete and not missing any fields?
9. Do all of the preferredContactMethods refer either to a method of contacting the customer, or a restriction on not using a particular method of contacting the customer?
10. Do all of the schedulePreferences refer either to a type of time, or a restriction on a type of time?
11. Are schedulePreferences arrays non-empty for all customers?
12. Are all of the location IDs in the correct format (e.g., "LOC-###")?
13. Are there any data fields in this data not tested by above list?

### Driver Data Validation
1. Are all of the driver IDs unique?
2. Are all of the driver IDs in the correct format (e.g., "DRV-###")?
3. Do all first names contain only alphabetic characters?
4. Do all last names contain only alphabetic characters?
5. Do all license numbers follow a valid format (e.g., alphanumeric and of appropriate length)?
6. Are all license numbers unique?
7. Are all of the current truck IDs in the correct format (e.g., "TRUCK-##")?
8. Do all contactDetails objects contain both an email and a phoneNumber field?
9. Are all email addresses in the contact details following a valid email format?
10. Are all phone numbers in the contact details following a valid phone number format (e.g., "555-####")?
11. Are any contact details fields missing?
12. Are there any data fields in this data not tested by above list?


### Duty Manager Data Validation

1. Are all of the manager IDs unique?
2. Are all of the manager IDs in the correct format (e.g., "DM-###")?
3. Do all first names contain only alphabetic characters?
4. Do all last names contain only alphabetic characters?
5. Do all contactDetails objects contain both an email and a phone field?
6. Are all email addresses in the contact details following a valid email format?
7. Are all phone numbers in the contact details following a valid phone number format (e.g., "555-####")?
8. Are any contact details fields missing?
9. Do all permission arrays contain valid permission values (e.g., "Operational Adjustment", "System Oversight", etc.)?
10. Are permissions arrays non-empty for all managers?
11. Do any permissions arrays contain duplicate values?
12. Are there any data fields in this data not tested by above list?

### Customer Agent Data Validation

1. Are all of the agent IDs unique?
2. Are all of the agent IDs in the correct format (e.g., "CSA-###")?
3. Do all first names contain only alphabetic characters?
4. Do all last names contain only alphabetic characters?
5. Do all contactDetails objects contain both an email and a phone field?
6. Are all email addresses in the contact details following a valid email format?
7. Are all phone numbers in the contact details following a valid phone number format (e.g., "555-####")?
8. Are any contact details fields missing?
9. Are there any data fields in this data not tested by above list?

### Event Log Data Validation
1. Are all event IDs unique?
2. Are all event IDs in the correct format (e.g., 'event###')?
3. Are all timestamps in valid ISO 8601 format?
4. Do all event descriptions contain non-empty strings?
5. Do all actors have a specified role and name?
6. Are all interaction types correctly specified?
7. Is each context block present and properly formatted?
8. Are all customer IDs in the context blocks in the correct format (e.g., 'CUST-###')?
9. Are all route IDs in the context blocks in the correct format (e.g., 'ROUTE-###')?
10. Are all plan IDs in the context blocks in the correct format (e.g., 'PLAN-###')?
11. Are all truck IDs in the context blocks in the correct format (e.g., 'TRUCK-###')?
12. Are there any data fields in the event logs not tested by the above list?"

### Location Data Validation
1. Are all location IDs unique?
2. Are all location IDs in the correct format (e.g., 'LOC-###')?
3. Are all addresses non-empty strings?
4. Do all latitude values follow valid geographic coordinate formats (e.g., decimal degrees)?
5. Do all longitude values follow valid geographic coordinate formats (e.g., decimal degrees)?
6. Are there any data fields in the location data not tested by the above list?

### RoutePlan Data Validation
1. Are all routePlan IDs unique?
2. Are all routePlan IDs in the correct format (e.g., 'RP-##')?
3. Are all descriptions non-empty strings?
4. Are all activeFrom dates in valid YYYY-MM-DD format?
5. Are all activeTo dates in valid YYYY-MM-DD format?
6. Is activeTo date always later than the activeFrom date?
7. Are all scheduledRoutes arrays non-empty?
8. Do all scheduledRoutes contain valid dates in YYYY-MM-DD format?
9. Do all scheduledRoutes have non-empty locations arrays?
10. Do all locations within scheduledRoutes follow the correct format (e.g., 'LOC-###')?
11. Do all scheduledRoutes contain non-empty estimatedTime fields?
12. Are all estimatedTime values in valid time formats (e.g., 'X hours', 'X.Y hours')?
13. Are all bucketIds in the correct format (e.g., 'BUCKET-##')?
14. Are there any data fields in the route plan data not tested by the above list?"

### Customer Service Policy Data Validation
1. Are all policy IDs unique?
2. Are all policy IDs in the correct format (e.g., 'CSP-###')?
3. Are all types valid and specified (e.g., 'Option', 'Rule', 'Guideline')?
4. Are all descriptions non-empty strings?
5. Are all scopes within the valid expected categories (e.g., 'Plan', 'General', 'Incident', 'Post-Interaction', 'Pre-Interaction', 'During Interaction')?
6. Are all approval requirements valid and specified (e.g., 'None', 'Duty Manager')?
7. If present, are all action fields non-empty strings?
8. Are there any data fields in the customer service policy data not tested by the above list?"

### Definitions Data Validation
1. Is the 'type' field for 'Schema' defined as 'object'?
2. Are all required properties ('Concepts', 'Actors', 'Actions', 'Inputs', 'Outputs') present under 'Schema'?
3. Is the 'type' field for 'Concepts' defined as 'object'?
4. Are all required properties ('CRM System', 'Operational Integrity', 'Audit Trail') present under 'Concepts'?
5. Is the 'type' field for each property under 'Concepts' defined as 'string'?
6. Do all properties under 'Concepts' have non-empty 'description' fields?
7. Is the 'type' field for 'Actors' defined as 'object'?
8. Are all required properties ('Driver', 'Duty Manager', 'Customer Service Agent') present under 'Actors'?
9. Is the 'type' field for each property under 'Actors' defined as 'string'?
10. Do all properties under 'Actors' have non-empty 'description' fields?
11. Is the 'type' field for 'Actions' defined as 'object'?
12. Are all required properties ('Routing', 'Scheduling', 'Logging Events') present under 'Actions'?
13. Is the 'type' field for each property under 'Actions' defined as 'string'?
14. Do all properties under 'Actions' have non-empty 'description' fields?
15. Is the 'type' field for 'Inputs' defined as 'object'?
16. Are all required properties ('Route Details', 'Customer Feedback') present under 'Inputs'?
17. Is the 'type' field for each property under 'Inputs' defined as 'string'?
18. Do all properties under 'Inputs' have non-empty 'description' fields?
19. Is the 'type' field for 'Outputs' defined as 'object'?
20. Are all required properties ('Operational Reports', 'Alerts and Notifications', 'Compliance Summaries') present under 'Outputs'?
21. Is the 'type' field for each property under 'Outputs' defined as 'string'?
22. Do all properties under 'Outputs' have non-empty 'description' fields?
23. Are there any data fields in the schema not tested by the above list?"

### Operational Constraints Data Validation
1. Are all constraint IDs unique?
2. Are all constraint IDs in the correct format (e.g., 'OC-###')?
3. Are all scopes within the valid expected categories (e.g., 'Route', 'Plan', 'Both')?
4. Are all descriptions non-empty strings?
5. Are all enforcement levels valid and specified (e.g., 'Mandatory')?
6. Are there any data fields in the operational constraints data not tested by the above list?

### Roles Data Validation
1. Are all role names unique?
2. Are all role names non-empty strings?
3. Are all responsibilities fields non-empty arrays?
4. Do all responsibilities arrays contain non-empty strings?
5. Are all permissions fields non-empty arrays?
6. Do all permissions arrays contain non-empty strings?
7. Are there any data fields in the roles data not tested by the above list?





### Prompts used to generate the above

I will now give you a new JSON data file.  Keeping the same data, reformat it into a similar format as the customer data, e.g. adding a description to each field where necessary.

Generate a comprehensive list of validation questions for this data

Are there any data fields are are not tested by above list?

Does the data pass all of these tests?