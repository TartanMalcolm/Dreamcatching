
# Dreamcatcher Card Game - Narrative 06 

## Overall Aim

To model out a single type of transaction on a CRM.  That transaction is:

1. The company has the following information:
    1. Customers:
        1. Name
        2. Location
        3. Required pick-up time.
    2. Buckets:
        1. A method for sorting postcodes into available pick-up routes.
    3. Plans:
        1. A day-by-day work-order to a truck to pick up from a number of customers.
    4. Constraints:
        1. A list of constraints which the plans must all pass before going for approval and execution.
    5. Customer interaction rules
        1. A list of what's possible and what's not, given a customer's changing requirements.
    6. Event Log:
        1. A timestamped list of things that have happened.  E.g.
            1. A collection has been made.
            2. A truck has recorded additional information in NL about a collection. E.g.
                1. Couldn't do it, big dog.
                2. Couldn't find the bin.
            3. A customer has asked for X.
    7. Services available:
        1. Derived from constraints such as:
            1. A plan can only consider picking up within a single bucket.
            2. A plan can only be changed with 24 hours notice.
            3. A Plan needs a single truck.
            4. There are more than one trucks available, but can't be used if they're on other plans.

## Plan

1. Use Hal to create JSON schema for the following, get him to reconcile and propose improvements, and check for correctness.
    1. Customer
    2. Route
    3. Plans
    4. Constraints, physical/temporal
    5. Constraints, Customer Service.
2. Use Hal to use the schema provided to carry out a test scenario:
    1. Generate some test data.
    2. Change a customer delivery date, following all constraints.
    3. Update constraints.
3. Create a customerServiceBot that knows and adheres to the schema, and test it manually on a similar scenario.
4. Create a dutyManagerBot that similarly knows the schema but also knows the live data from test (3)
5. Createa consistencyBot that looks at the schema and data, and checks for inconsistencies and irregularities.  Mess with it by adding in a few.
6. Create plannerBot, that updates the planning folder while recognising Constraints, physical/temporal


## CHAPTER 1 - Use Hal to create JSON schema for the following, get him to reconcile and propose improvements, and check for correctness.

### Session Prompt

hal_v0.1.md

### Session Script
 ./Bots/hal_v0.1/sessions/01/session.md

### Dave's Observations

1. Pretty fucking good actually.  Nice one Hal.
2. The time consuming part in this run was pre-run time.  You need to go in with a fairly precise idea of the top level structure, but then Hal takes over and makes consistent.
3. NB that during the creation session I was also able to switch out to a 'Test', then take on different personas.  Need to check if Hal was cheating by using the full session, but don't think so.

### Output

Have editted down the session to the JSON as I'm getting repeated Error Streaming run.  Possibly session too long?


## CHAPTER 2 - Create a folder structure and temp JSON

### Session Prompt

hal_v0.1.md

### Input

### Session Script
 ./Bots/hal_v0.1/sessions/02/session.md

### Dave's Observations


### Output



