# Dreamcatcher Switch Bot, no data

## Header
 - Name: SwitchbotWithData
 - Description: this sequence is called every time an Actor asks to use a bot other than the one he's currently using, and requires data to be passed to that bot.
 - Entities Used:
    - Dave - The Contributor.
    - Artifact 
    - Backchat
    - Hal
    - Git
    - TargetBot - the bot to switch to.

## Starting state
Dave is asking Hal to send payload to TargetBot

## Expectation
Dave now talking to TargetBot, who has been given the data.



---
```mermaid
sequenceDiagram
    participant Dave
    participant Hal
    participant Backchat
    participant targetBot

    %% Note spanning from the first to the last participant
    note over Dave, targetBot: Initial conditions - Dave is asking Hal to send payload to targetBot

    %% Dave asks Hal
    Dave->>Hal: Prompt - Backchat, please send the payload to targetBot
    Hal->>Backchat: Prompt - Send the payload to targetBot
    Backchat->>targetBot: Instantiate targetBot
    Backchat->>targetBot: Sends payload to targetBot
    Backchat->>Dave: Makes targetBot Available to Dave

    %% Greeting
    targetBot->>Dave: Response: Got it.

    %% Note specific to targetBot interaction
    note over Dave, targetBot: EXPECTATION: Dave now talking to TargetBot, who has been given the data.
    ```
---