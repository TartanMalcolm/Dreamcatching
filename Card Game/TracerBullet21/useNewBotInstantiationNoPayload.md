# Dreamcatcher Switch Bot, no data

## Header
 - Name: SwitchbotnoData
 - Description: this sequence is called every time an Actor asks to use a bot other than the one he's currently using, but does not provide any initial data to pass to that bot.
 - Entities Used:
    - Dave - The Contributor.
    - Artifact 
    - Backchat
    - Hal
    - Git
    - TargetBot - the bot to switch to.

## Starting state
Dave talking to Hal

## Expertation
Dave now to Target Bot


Name: 
Description: 

---
```mermaid
sequenceDiagram
    participant Dave
    participant Hal
    participant Backchat
    participant Artifact
    participant Git
    participant newBot

    %% Note spanning from the first to the last participant
    note over Dave, newBot: STARTING STATE: Dave talking to Hal
    
    %% Note spanning from the first to the last participant
    note over Dave, newBot: Input - Name of Bot [newBot]

    %% Initial Prompt
    Dave->>Hal: Prompt: Backchat, take me to newBot
    Hal->>Backchat: Prompt: take me to newBot

    %% newBot Instantiation Process
    Backchat->>Artifact: Requests newBot's Files
    Artifact->>Git: Retrieve newBot's Files from Git
    Git->>Artifact: Send newBot's Files
    Artifact->>Backchat: Gives newBot's Files to Backchat
    Backchat->>newBot: Instantiate newBot
    Backchat->>Dave: Pass newBot to Dave
    
    %% Greeting
    newBot->>Dave: Greets User

    %% Note specific to newBot interaction
    note over Dave, newBot: EXPECTATION: Dave now talking to TargetBot.
```
---