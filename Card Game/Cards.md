# ACTION CARDS

## Create New Hal(Registration request from Dave)

Used by: Dave
Uses: System

Operation: 
	Create this Dave's personal Hal.
	Add Dave's Wallet to Wallet pile
	Add Dave's Hal to Private Bot Pile
Output: 
	Initialised and available Hal
	Hal Private Help Bot

Who pays?: Dave
Who gets paid? System


## Dave-Hal Conversation(Input from Dave, Input from Hal)

Used by: Dave
Uses: Hal

Operation: 
	Hal considers input.
	Either:
		Responds Directly
		Devines Intent
		Commissions(Public Bot, Intent)
Output: 
	Session history stored in Hal.

Who pays?: Dave
Who gets paid? 
		Distribution Event(Dave, Hal Private Help Bot, session payment)

## Dave-Hal Conversation(Message from Hal)

Used by: Hal
Uses: Dave

Operation: 
	Hal raises that there's a message next time Dave comes on line.
	
Output: 
	Session history stored in Hal.
	Dave-Hal Conversation(Input from Dave, Input from Hal) started.

Who pays?: Dave
Who gets paid? 
		Distribution Event(Dave, Hal Private Help Bot, session payment)

## Distribution Event(Payer, Help, session payment)

Used by: Help
Uses: System

Operation:
	Distribute session payment to Attribution Table of Help

Who pays?: Payer
Who gets paid? Contributors to the Helps listed Attribution Table, 


## Register Prior Art(Dave, Data to register)

Used by: Hal
Uses: System

Operation: 
	Registers Data that wasn't previously available on DC on to the DC chain as a Help.

Output: 
	Help

Who pays?: Hal->Dave
Who gets paid? System


## Stuck Creator(Hal, Stuck Details)

Used by: Hal
Uses: System

Operation: 
	Registers a new Stuck on to the DC chain.
	May reference Helps
	May reference other Stucks
	Must include Stuck Details (Intent)

Output: 
	Stuck

Who pays?: Hal->Dave
Who gets paid? System



