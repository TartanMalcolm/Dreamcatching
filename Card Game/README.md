# Dreamcatcher Card Game 

1. Bots that are owned and run by the Dreamcatcher are in ./Bots.md.  Format:
'''
    ## Name of Bot(Inputs)

    Used by: 
        Dave <Which Bot can commission this Bot to do work. NB Dave is also a Bot.>
    Uses: Search Bot <Which Bots can this Bot commission to do work for it.>

    Operation: 
        <The sequence of Cards that this Bot carries out.>

    Output: 
        <The list of state changes this Bot is constrained to >
    
    Who pays?: <Who picks up the tab when this Bot is run.> 
    Who gets paid? <Who gets paid when this Bot is run.>
'''
1. Helps that are owned and run by the Dreamcatcher are in ./Helps.md. Format:
'''
    ## System.Help01: <Unique name of help>
        Description: <The template, content or method this help offers.>
        Owner: System <Who created it>
        History:
            Template created YY.MM.DD by us. <Record of how this help has been built up over time.>
'''
1. Cards constrain and describe state changes.  Format:
'''
    ## Name of State change(inputs)

    Used by: Dave <Who can action this state change>
    Uses: System <what does this state change call on to do work.  Can be System, a Bot, a Help>

    Operation: <what happens>
        Create this Dave's personal Hal.
        Add Dave's Wallet to Wallet pile
        Add Dave's Hal to Private Bot Pile
    Output: <what's stored back on the Sytem>
        Initialised and available Hal
        Hal Private Help Bot

    Who pays?: Dave <Who's responsible for paying for this state change to happen?>
    Who gets paid? System <Who gets paid for carrying out this work?>
'''
1. Tracer Bullets are one instance of running through the game, aimed and finding holes in the game itself.  Each Tracer Bullet has:
    1. Narrative - time sequenced set of events.
    1. Helps.md - the Helps that are generated in this Narrative.
    1. Stucks.md - the Stucks generated in this Narrative.
1. Tracer Bullets can call on ../*, but can't alter them.  That's for us to do.
