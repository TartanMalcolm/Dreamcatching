# Dreamcatcher Switch Bot, no data

Name: SwitchbotnoData
Description: this sequence is called every time a user (Dave e.g) asks to use a bot other than the one he's currently using, but does not provide any initial data to pass to that bot.

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
    note over Dave, targetBot: Exit conditions - Dave now has access to targetBot
    ```
---