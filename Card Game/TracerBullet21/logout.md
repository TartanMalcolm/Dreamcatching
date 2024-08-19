sequenceDiagram
    participant Dave
    participant Artifact
    participant Backchat
    participant Hal

    %% Logout Process
    Dave->>Hal: Prompt: log me out
    Hal->>Artifact: Request - Logs Out
    Artifact->>Artifact: Terminate Session
