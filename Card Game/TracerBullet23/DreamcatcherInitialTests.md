

### Actor to Actor Interactions
1. **CONTRIBUTOR to HELP**: 
   - Create a HELP.
   - Modify an existing HELP.
   - Submit a Pull Request for a HELP.
   - Commit changes to a HELP.
   - Issue a problem related to a HELP.

2. **PRE_BUYER to BOUNTY**:
   - Assign a BOUNTY to a STUCK.
   - Adjust an existing BOUNTY.
   - Claim a BOUNTY associated with a STUCK.

3. **TIPPER to TIP**:
   - Assign a TIP to a RELEASE.
   - Claim a TIP associated with a RELEASE.

4. **DREAMCATCHER_ADMIN to all entities**:
   - Create a new ACTOR.
   - Delete a HELP.
   - Update a BOUNTY.
   - Generate an ATTRIBUTION TABLE.
   - Modify user roles.

### Interactions with Other Entities
1. **CONTRIBUTOR**:
   - Contributes to HELP: CREATE, MODIFICATION (to HELP).
   - NOTE: Each contribution should link to a respective HELP.

2. **PRE_BUYER**:
   - Manages BOUNTY: CREATE, ADJUST, CLAIM (to BOUNTY).
   - NOTE: Each bounty should be linked with a STUCK.

3. **TIPPER**:
   - Interacts with TIP: CREATE, CLAIM (to TIP).
   - NOTE: Each tip should link with a RELEASE.

4. **DREAMCATCHER_ADMIN**:
   - Oversees all interactions with entities, including:
     - Managing actors (CREATE, UPDATE, DELETE ACTORS).
     - Adjusting system-wide settings related to any entity.

### General Test Data
- **ACTOR Sample Data**:
    - (1) Scott - Contributor
    - (2) Amy - Pre-Buyer
    - (3) Tom - Tipper
    - (4) John - Admin
- **HELP Sample Data**:
    - (1) "Help with Feature A"
    - (2) "Bug Fix for Feature B"
- **STUCK Sample Data**:
    - (1) "Issue with Feature A"
    - (2) "Bug in Feature B"
- **BOUNTY Sample Data**:
    - (1) Stuck ID 1, Amount $100
    - (2) Stuck ID 2, Amount $150
- **RELEASE Sample Data**:
    - (1) Help ID 1, Release Date 2023-10-01
    - (2) Help ID 2, Release Date 2023-10-03
- **TIP Sample Data**:
    - (1) Release ID 1, Amount $10
    - (2) Release ID 2, Amount $20
