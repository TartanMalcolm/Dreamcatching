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
Dave is logged in.

## Expertation

Dave is now logged out.

sequenceDiagram
    participant Dave
    participant Artifact
    participant Backchat
    participant Hal

    %% Note
    note over Dave, Hal: STARTING STATE: Logged in

    %% Logout Process
    Dave->>Hal: Prompt: log me out
    Hal->>Artifact: Request - Logs Out
    Artifact->>Artifact: Terminate Session

    %% Note
    note over Dave, Hal: EXPECTATION: Dave now logged out.
