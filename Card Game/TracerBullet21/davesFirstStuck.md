sequenceDiagram
    participant Dave
    participant Hal
    participant Backchat
    participant Artifact
    participant Switchboard
    participant Marketplace
    participant StuckBot
    participant Testrunner


    note over Dave, Testrunner: TEST: Login. Description: Dave Logs in
    note over Dave, Testrunner: STATUS: Dave is Talking to Hal

    %% User asks for some stucks to work on
    Dave->>Hal: Prompt - Backchat, show me some available Stucks
    Hal->>Backchat: Instruction: show me some available Stucks
    Backchat->>Switchboard:  Instruction: Take Dave to somewhere that can show available Stucks
    note over Dave, Testrunner: TEST: Switchboard PAYLOAD: None, Expected Response: Switch to Bot/Marketplace
    note over Dave, Testrunner: STATUS: Dave is Talking to Marketplace   

    %% Going to Marketplace
    Dave->>Marketplace: Prompt: what can I work on?

    note over Dave, Testrunner: TEST: Marketplace. Description: Dave asks a number of questions to filter the Stucks available and gets a number ofresponses.  Eventually he chooses one.
    note over Dave, Testrunner: STATUS: Dave is working on the Stuck   
    note over Dave, Testrunner: GIT CHANGE: Create a fork of the Test Repo using Dave's account.  Make non-breaking edits.  Create Merge Request.
    note over Dave, Testrunner: Dave finished working on a stuck and is ready to submit for payment.

    %% User asks for merge request to be considered for payment
    Dave->>Hal: Prompt - Backchat, submit my merge for the stuck I've been working on.
    Hal->>Backchat: Instruction: submit my merge for the stuck I've been working on.
    Backchat->>Switchboard:  Instruction: submit Dave's merge for the stuck I've been working on.
    note over Dave, Testrunner: TEST: Switchboard PAYLOAD: Merge Hash, Expected Response: Switch to Bot/Stuckbot
    note over Dave, Testrunner: STATUS: Dave is Talking to Stuckbot   
    %% Submitting Work
    StuckBot->>Dave: Response: Hi Dave, let me check if you've potentially solved the stuck.
    note over Dave, Testrunner: TEST: Stuckbot PAYLOAD: Merge Hash, Expected Response: Pass
    StuckBot->>Dave: OK, looks good.  Let me run the checks with the other parts of the system.
    note over Dave, Testrunner: TEST: Testrunner PAYLOAD: Merge Hash, Expected Response: All Pass    
    Testrunner->>StuckBot: All passed.  Releasing the funds now.
    StuckBot->>Dave: You're awesome, Dave!  Releasing the funds now.
    note over Dave, Testrunner: TEST: FundsBot PAYLOAD: Dave's HASH, Expected Response: Funds released
    


    %% End Note
    note over Dave, Testrunner: STATUS: Dave successfully completed the stuck task and received escrow.