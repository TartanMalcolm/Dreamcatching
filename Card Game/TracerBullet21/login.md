# Dreamcatcher Login sequenceTest

## Header
 - Name: LoginTest
 - Description: The sequence used to login a User to Dreamcatcher.
 - Entities Used:
    - Dave - The Contributor.
    - Artifact 
    - Backchat
    - Hal
    - Git

## Starting state
None.

## Expertation

Dave now logged in and talking to Hal


---
```mermaid
sequenceDiagram
    participant Dave
    participant Artifact
    participant Backchat
    participant Hal
    participant Git

    %% Note
    note over Dave, Hal: STARTING STATE: None

    %% Login and Initial Setup
    Dave->>Artifact: Input - Logs In
    Artifact->>Dave: Authenticate User
    Artifact->>Backchat: Instantiate Backchat
    Backchat->>Artifact: Requests Hal's Files
    Artifact->>Git: Retrieve Hal's Files from Git
    Git->>Artifact: Send Hal's Files
    Artifact->>Backchat: Gives Hal's Files to Backchat
    Backchat->>Hal: Instantiate Hal
    Backchat->>Dave: Pass Hal to Dave
    Hal->>Dave: Greets User

    %% Note
    note over Dave, Hal: EXPECTATION: Dave now logged in and talking to Hal
```
---