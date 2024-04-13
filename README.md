# Dreamcatching

This is the first attempt to specify the process by which helps are produced, combined, used, and the authors fairly recognised and recompensed. 

It's probably wrong.

## Nomenclature 

    - A verb refers to a run-time process.  This can either be through code or through a bot session.
    - A noun refers to a static piece of data that can be retrieved and used by a verb.

## Definitions

### Verbs

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

## Dreamcatching Process

### Intent

A Jitter has been used.  Therefore, it's generated value.  Attribute that value to everyone and every supporting system that was necessary to make it happen.

### Process

    1. Enable Dave/HAL
        - Intent: Provide a consistent Human/AI interface where the AI has access to the context of what Dave has said before, can judge what he wants now, and can model what he actually means.
        - Input: Prompt responses from Dave.  Previous session summaries.
        - Output: Updating the history of this session for future use.  Actioning Orchestrators to create Jitters.
    2. Enable Contributing:
        - Intent: For a help, what is its provenance?  What prior-art contributed to it being produced?
        - Input: Interactions between Dave and Hal that result in a Help.
        - Operation: Record the output from the interaction on the system.
        - Output: An update of the state of the Contributions on the underlying OS.
    3. Enable Jittering:
        - Intent: Given a request from Dave, search and pull together helps, provide any required wrapper to make it coherent, and allow Dave to use it.
        - Input: Helps, intent.
        - Operation: Present the Jitter for use and what was used in bringing it together.
        - Output: Log of use, the value of that use, and the helps used.
    4. Enable Attributing:
        - Intent: Given a use, and the record of value, distribute that value to the authors who contributed.

## Supporting Processes

    1. Assessing: 
        Given a scorecard of what value means, provide a report card for each of the helps used.
    2. Judging:
        Run a process against multiple modals, providing scorecard that compares their output against the intent, and ruling on which to go with.

