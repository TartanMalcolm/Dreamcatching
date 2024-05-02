
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

1. Create a folder structure and temp JSON for:
    1. Customer
    2. Route
    3. Plans
    4. Constraints, physical/temporal
    5. Constraints, Customer Service.
2. Create customerServiceBot that answers questions from customerServiceDave.
3. Create plannerBot, that updates the planning folder while recognising Constraints, physical/temporal
4. Create testingBot that enforces the JSON and checks for inconsistences between Plans and Routes.

## CHAPTER 1 - Create a folder structure and temp JSON

### Session Prompt

hal_v0.1.md

### Session Script


### Dave's Observations

### Output
