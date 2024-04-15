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
    - System. Baked code that presents capabilities such as recording stucks.
    - Orchestators.  A bot that has access to helps, including Drones, to execute the intent.
    - Drones.  AI's that are single function and highly confined, but which can be relied on to produce the right output given the right input.
    - Contribution Log. The system, by which any artifact or event is logged.
    - Stuck. An NL description of something that has previously been required but wasn't available as a Help.
    - Help. A unit of useful data that can be incorporated into a Jitter.

TODO: This isn't complete.  I'll get back to this.

## Dreamcatching Process

### Intent

A Jitter has been used, or the knowledge in Helps has been used on other systems.  Therefore, there's been an Impact, which can be positive or negative.  Acknowledge, record and Attribute that to everyone and every supporting system that was necessary to make it happen.

### Processes

#### Peanut Pushing

Without permission, improve stuff.

##### Create Raw
    
    1. Create Raw
        - Intent: Dave has an idea.  May be as a response to a Stuck or a novel idea.
        - Session Aim: With Hal or alone, work on the idea, and register the first version on the Contribution Log.
        - Input: Stuck, or nothing.
        - Output: A Help. An update to Contribution Log. 
        - Talks to:
            - Hal (optional) 

##### Iterate

    1. Iterate Help
        - Intent: Take an existing Help and push the peanut on.
        - Session Aim: Dave can improve a Help directly, collaborate to improve it, quality assess it, manage a team to improve it, or otherwise make the Help more usable.  
        - Input: Help.  Other evidence of work being carried out.
        - Output: Updated Help. Update to Contribution Log
        - Talks to:
            - Hal (optional) 

##### End output  
        - A Help, either new or changed.
        - An update to the record of the Provenance of that Help

#### Build Jitter

    1. Dave/HAL
        - Bot: Hal.
        - Intent: Provide a consistent Human/AI interface where the AI has access to the context of what Dave has said before, can judge what he wants now, and can model what he actually means.
        - Session Aim: Try to figure out what Dave actually wants.  Prompt responses from Dave to fill in the gaps.  Use context from previous session summaries.
        - Input: Dave/Hal session. 
        - Output: 
            - Updating the history of this session for future use between Dave/Hal.
            - Dave's Intent. Actioning Jitter Maker when it becomes clear WTF Dave wants.
        - Talks to:
            - Dave
            - Jitter Maker

    3. Jittering:
        - Bot: Jitter Maker
        - Session Aim: Given an Intent, search and pull together Helps, provide any required wrapper to make it coherent.  Assess against intent. Allow Dave to use it.  Identify and Register Stucks. Register Jitter as a Help. Registor use.
        - Input: Helps, intent.
        - Operation: Present the Jitter for use and what was used in bringing it together.
        - Output: Log of use, the value of that use, and the helps used.  Records of any Stucks identified.
        - Talks to:
            - Hal
            - Contribution Recorder
            - Bot: Evalulator

        3.1 Evaluating:
        - Bot: Evalulator
        - Session Aim: Identify, given multiple possible Jitters, which best meets Dave's intent.
        - Input: Intent, Jitter.
        - Operation: Consider the Intent, list the dimensions that Dave cares about.  Using that, consider each proposed Jitter and return your recommendation about which is best.
        - Output: Recommendation.

    End output:
        - A Jitter
        - To the Record, the fact that this was used and the Context, the Helps used in building it, the bots used in building the Jitter, the input from the session with Dave/Hal, the run-time costs, and any value exchange (e.g payment.).

#### Record Updating

Add any additional information that pretains to the value that a Jitter has produced into the Record.

    1. Updating
        - Bot: Scraper or other source, or random Dave.
        - Session Aim: Update the Record with new information about the Impact a Jitter or Help has caused.
        - Input: NL new info
        - Operation: Update the Record with the new information available.  Dedupe similar updates.
        - Output: Record update.
        - Talks to:
            - Contribution Recorder


#### Attributing

On request, provide the Impact Report for a given Help or Jitter.

    1. Attributing
        - Bot: Attributor
        - Session Aim: Give an NL report on the Impact that a Help/Jitter has had, taking the Record into account.
        - Input: Record.
        - Operation: Given what the Record holds now, and (optionally) the impact values the user cares about, provide an report card of what the help/jitter has had.   
        - Output: Impact report.
        - NOTE: This could and probably should be triggered each time Dave looks at his Wallet.

##### Distributing

When a debtor is offering to pay the use of a Jitter/Help, calculate who gets what. NB this isn't necessarily cash. This is the disperal event, and so will call on the Attributor to decide the cut.

    1. Distributing
        - Bot: Attributor
        - Session Aim: Balance Karma.
        - Operation: Assess what is owed by any value offered, translate into the denomination offered, and record the fact.  
        - Output: Updated Record.

