# Dreamcatching

This is the first attempt to specify the process by which helps are produced, combined, used, and the authors fairly recognised and recompensed. 

It's probably wrong.

## Nomenclature 

    - A verb refers to a run-time process.  This can either be through code or through a bot session.
    - A noun refers to a static piece of data that can be retrieved and used by a verb.

## Definitions

### Verbs

    - Devining - a method to ascertain exactly what Dave wants from what Dave actually says
    - Assessing - a method which requires a value assessment criterior, and which applies that criterior at run time to a help or output.
    - Contributing - a method of storing a help alongside that help's history.  I.e. what did that help refer to or rely on to come into existence. 
    - Jittering - a method of taking in a stuck, searching helps, combining those, generating any required wrapping to make it coherent and allowing Hal to present it to Dave in response to a request by Dave.
    - Attributing - a method to decide, at this point in time, what the relative value to Dave a Jitter was, and to express that as a dynamic (ie just in time) cap table. Taking that dynamic cap table it applies  real world numbers to it (e.g. cash, kudos), and recording or distributing that value.

### Nouns

    - Dave.  A human.  Can only talk to Hal.
    - Hal. A personal AI to Dave, with access to the historic data on preferences, previous requests, context.  Hal can only talk to Dave,  Orchestators and System.
    - System. Baked code that provides the substrate OS calls necessary to store data, run code and run Bots.
    - Orchestators.  A bot that has access to helps, including Drones, to execute the intent.
    - Drones.  AI's that are single function and highly confined, but which can be relied on to produce the right output given the right input.
    - Contribution. A record attached to each Help, of who or what allowed that Help to come into existence. Contribution includes references to previous Helps, external data, and Context.
    - Stuck. An NL description of something that has previously been required but wasn't available.
    - Help. A unit of useful data that can be used to construct a Jitter. Types of Helps: Isolate, data object, Jitter, Bot, Stuck.  Helps incorporate their own Provenance.
    - Jitter. A just-in-time app, constructing using Helps and, if necessary, a wrapper to make it coherent.  A Jitter, once constructed, is also made available as a Help in future runs.
    - Provenance. A record of who and what has aided the construction of a Help.
    - Isolate. A fragment of code or a static piece of data that can be used in the traditional (non-Bot) sense. 
    - Event. A change of state within the System.
    - Observation Event. A request to assess Contribution of a Help against all available data at that point in time.
    - Intent: What Dave wants the Jitter to do.

TODO: This isn't complete.  I'll get back to this.

## Dreamcatching Process

### Aim

Dreamcatching aims to:
    - Record and keep up to date all Contribution to Helps
    - Provides a method to pull those Helps together into a Jitter and make it available to Dave, updating Contribution as required.
    - At any Event, provide a Report on the Impact of each contribution to each Help used.

### Processes

#### Peanut Pushing

Aim: without permission, improve stuff.

##### Create Raw
    
    1. Create Raw
        - Actor: Isolate
        - Aim: Create a usable Help.  May be as a response to a Stuck or a novel idea.
        - Input: Stuck, or nothing.
        - Operation: With Hal or alone, work on the idea, and register the first version on the System.
        - Output: A Help and its Provenance. 
        - Talks to:
            - Hal (optional) 

##### Iterate

    1. Iterate Help
        - Actor: Isolate
        - Aim: Take an existing Help and push the peanut on.
        - Input: Help.  Other evidence of work being carried out.
        - Operation: With Hal or alone, improve a Help directly, collaborate to improve it, quality assess it, manage a team to improve it, or otherwise make the Help more usable.  
        - Output: Updated Help and its Provenance
        - Talks to:
            - Hal (optional) 

#### Build Jitter

    1. Dave/HAL
        - Actor: Hal (bot).
        - Aim: Provide a consistent Human/AI interface where the AI has access to the context of what Dave has said before, can judge what he wants now, can model what he actually means and can commission the construction of a Jitter.
        - Input: Dave/Hal session. 
        - Operation: Try to figure out what Dave actually wants.  Prompt responses from Dave to fill in the gaps.  Use context from previous session summaries. Commission a Jitter. 
        - Output: 
            - Updating the history of this session for future use between Dave/Hal.
            - Dave's Intent. Actioning Jitter Maker when it becomes clear WTF Dave wants.
        - Talks to:
            - Dave
            - Jitter Maker

    3. Jittering:
        - Actor: Jitter Maker (bot)
        - Input: Helps, Intent.
        - Operation: Given an Intent, search and pull together Helps, provide any required wrapper to make it coherent.  Assess against Intent. Pass the Jitter back.  Identify and Register Stucks. Register Jitter as a Help. Update Contribution.
        - Output: A Jitter. Updated Contribution. Stucks. 
        - Talks to:
            - Hal
            - Create Raw
            - Evalulator

        3.1 Evaluating:
        - Actor: Evalulator (bot)
        - Session Aim: Identify, given multiple possible Jitters, which best meets Dave's Intent.
        - Input: Intent, Jitter.
        - Operation: Consider the Intent, list the dimensions that Dave cares about.  Produce a Report Card.
        - Output: Report Card.
        - Talks to:
            - Jitter Maker
            - Judge

        3.2 Judging:
        - Actor: Judge (bot)
        - Session Aim: Stack rank multiple possible Jitters based on their Report Card, and the coherence of the Evaluation.
        - Input: Intent, Jitters, Report Cards.
        - Operation: Consider the Intent, check the internal coherence of the Report Card.  Adjust, normalise and weight the Impact.  Stack rank the Jitters.
        - Output: Jitter Stack Rank.

#### Updating Contribution

Add any additional external information that pretains to the value that a Jitter has produced.

    1. Updating, External
        - Actor: Scraper or other source, or random Dave.
        - Session Aim: Allow the consideration of information outside of Dreamcatcher to be incorporated into Contribution.
        - Input: NL new info, external data sources, opinion.
        - Operation: Update the Contribution of a Help, cascading through it's Provenance.  Dedupe similar updates.
        - Output: Updated Contribution.
        - Talks to:
            - System

    1. Updating, Internal
        - Actor: Isolate. 
        - Session Aim: Allow the update of Contribution.
        - Input: New information on the use of an existing Help.
        - Operation: Update the Contribution of a Help, cascading through it's Provenance.
        - Output: Updated Contribution.
        - Talks to:
            - System

#### Attributing

On request, provide the Impact Report for a given Help or Jitter.

    1. Attributing
        - Actor: Attributor (bot)
        - Session Aim: Proportion the Impact (praise/blame) of a Help.  Provide a view of Karma.
        - Input: Help to consider. (Optionally) Filter.
        - Operation: Given a Help, proportion NL Impacts (praise/blame) by cascading through the Provenance chain.  Optionally, apply on a filter on what should be considered.  Continue through the cascade until praise/blame can be attributed to each End User.
        - Output: Impact report.
        - NOTE: This could and probably should be triggered each time Dave looks at his Wallet, or when anyone asks 'what is this End User's Impact?'
        TODO: How to calibrate.

##### Distributing

    1. Distributing
        - Bot: Distributor
        - Session Aim: Distribute rewards.
        - Operation: When an End User is offering to pay or provide any tangible benefit, calculate who gets what portion of that benefit. NB this isn't necessarily cash. This is the disperal event, and so will call on the Attributor to decide the cut. Record the fact in the Wallet of the End User, in order to provide a view of what that End User has received versus, at any point through an Attribution call, what they really should have.
        - Output: Updated Wallet. Updated contribution.
        - Talks to:
            - Attributor
            - System

