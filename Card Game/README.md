# Dreamcatcher Card Game 

The game is run from the point of view of the Dreamcatcher.  It's run in a series or rounds, using a queue stack for actions requested (this can be async, ie shuffle the queue, but for the first few tracer bullets atomic is probably easier.)  At each round:

    1. Start: The only Bot that can talk to a Dave is that Dave's personal Hal.  This is denoted by e.g. Dave01, who talks to Hal01.
    1. Hal starts the action stream by commisioning work from other Bots.  In doing so Hal states:
            1. Which Bot is carrying out the work and what is that work? The Bot can:
                1. Commission another Bot to do part or all of that work.  
                1. A Bot that can carry out the work using a Card does so.  A Bot can use Helps as input to a card.
            1. The result
    1. Action the stack. Pop an actionWhat is at the top of the queue stack?  Action that using:




1. Hal/Dave - As there are multiple Bots that are owned and run by the Dreamcatcher are in ./Bots.md.  Format:
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
        Draws on: <Record of how this help has been built up over time and which Helps/Bots used.>
        Events: <Log of information about: where has this has been used, by whom; new external information, e.g. >
            Template created YY.MM.DD by Dave101.
        Distribution: <Log of what distribution has already happened.  Ie what is paid out>
        Metrics: <Quantifiable non-distribution metrics, available at each Assessment to say what should have been paid, verus what was paid.  E.g. for an article - number of direct views, number of times quoted, and by who, number of times linked.  MAY be generated from Events.> 
'''
1. Helps record after creation is there to capture qualitative statements and quantative measurements, to make them available for future consideration.  E.g.
    1. Quantative:
        1. This article was read by a Student.
            1. In Events, read 100 times.
        1. This article was read by the Prime Minister, once.
        1. This article was quoted in 5 newspapers, and the Prime Minister in a Parliamentary session.
        1. This article received at time T, $NN dollars of ad revenue.
        1. The website on which this article was hosted has just received $NNN dollars in sponsership.
    1. Qualitative:
        1. DaveNN states that the Prime Minister viewed this article as important in policy making.
        1. DaveNN+102 states that the policy put in place appears to have made it into law, and that this Help should be considered as contributing to that.
        1. DaveNN+106 states that this article, because it was part of a wider website, increased the value of that website that is now getting offers to buy from other websites.

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
