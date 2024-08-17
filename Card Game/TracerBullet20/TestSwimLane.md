sequenceDiagram
    participant Scott
    participant Artefact
    participant Backchat
    participant Hal
    participant FlowchartBot
    participant TestBot
    participant TestRunner
    participant ERDcreatorBot
    participant Git
    participant Target

    %% Login and Initial Setup
    Scott->>Artefact: Prompt - Logs In
    Artefact->>Scott: Authenticate User
    Artefact->>Backchat: Instantiate Backchat
    Backchat->>Artefact: Requests Hal's Files
    Artefact->>Git: Retrieve Hal's Files from Git
    Git->>Artefact: Send Hal's Files
    Artefact->>Backchat: Gives Hal's Files to Backchat
    Backchat->>Hal: Instantiate Hal
    Backchat->>Scott: Pass Hal to Scott
    Hal->>Scott: Greets User
    
    %% FlowchartBot Instantiation Process
    Scott->>Backchat: Prompt - Backchat, take me to FlowchartBot
    Backchat->>Artefact: Requests FlowchartBot's Files
    Artefact->>Git: Retrieve FlowchartBot's Files from Git
    Git->>Artefact: Send FlowchartBot's Files
    Artefact->>Backchat: Gives FlowchartBot's Files to Backchat
    Backchat->>FlowchartBot: Instantiate FlowchartBot
    Backchat->>Scott: Pass FlowchartBot to Scott
    
    %% FlowchartBot Operations
    FlowchartBot->>Scott: Asks for Target ERD File
    Scott->>FlowchartBot: Prompt - Provides Target ERD File
    FlowchartBot->>Scott: Asks for User Stories
    Scott->>FlowchartBot: Prompt - Provides User Stories

    %% Flowchart Suggestion and Feedback
    FlowchartBot->>Scott: Suggests Flowchart
    Scott->>FlowchartBot: Prompt - Provides Feedback
    FlowchartBot->>Scott: Provides Updated Flowchart
    Scott->>FlowchartBot: Prompt - Confirms Updated Flowchart and asks for tests to be created

    %% FlowchartBot Creates Stories and Provides to Scott
    FlowchartBot->>Scott: Creates Stories and Provides to Scott
    Scott->>Backchat: Prompt - Backchat, send those Stories to TestBot
    Backchat->>TestBot: Instantiate TestBot
    Backchat->>TestBot: Sends Stories to TestBot
    Backchat->>Scott: Makes TestBot Available to Scott
    Scott->>TestBot: Prompt - Create tests based on these stories

    %% TestBot Creates Tests and Sends to Scott for Approval
    TestBot->>TestBot: Creates Tests
    TestBot->>Scott: Sends Tests for Approval

    %% Target Instantiation and Test Cycle
    Scott->>Backchat: Prompt - Instantiate Target for Tests
    Backchat->>Target: Instantiate Target
    Backchat->>TestRunner: Pass Target to TestRunner

    %% First Test Cycle
    loop Test Cycle 1
        TestRunner->>Target: Instantiate New Target
        TestRunner->>TestRunner: Run Test 1 with Target
        TestRunner->>Scott: Send Test 1 Results to Scott
    end

    %% Second Test Cycle
    loop Test Cycle 2
        TestRunner->>Target: Instantiate New Target
        TestRunner->>TestRunner: Run Test 2 with Target
        TestRunner->>Scott: Send Test 2 Results to Scott
    end

    %% Pass Summary of Results Back to Scott
    TestRunner->>Scott: Pass Summary of Results Back to Scott

    %% Handling Failed Tests and ERDcreatorBot Interaction
    alt Failed Tests?
        Scott->>Backchat: Prompt - Backchat, I need ERDcreatorBot to fix these failed results
        Backchat->>ERDcreatorBot: Instantiate ERDcreatorBot
        ERDcreatorBot->>Scott: Discuss Changes to Target
        Scott->>ERDcreatorBot: Prompt - Propose Changes
        ERDcreatorBot->>Scott: Propose Updates to Target
        Scott->>Backchat: Prompt - Backchat, happy with those changes, let's test them.
        alt Scott now happy with changes
            Scott->>Backchat: Prompt - Run Updated Target Against All Tests
            Backchat->>TestRunner: Run Tests Again
            TestRunner->>Scott: Pass Test Results to Scott
            Scott->>Backchat: Prompt - Merge the new version of Target
            Backchat->>Git: Merge Target and Update Test Suite
            Git->>Scott: Confirm Merge and Update
        end
    else
        Scott->>Backchat: Prompt - Merge Final Version to Main
        Backchat->>Git: Save Final Version to Git
        Git->>Scott: Confirm Save to Repository
    end
