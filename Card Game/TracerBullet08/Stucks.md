# Stucks for TracerBullet07

1. I can't be sure that the consistency of the CRM is maintained when extensions to the CRM are proposed.  I would expect consistency to consider the definitions.md first, then ensure that a proposed change is considered by all schemes in the CRM, and then for tests to be run to validate that.  Moreover, this should be done in-session, so I don't need to move out of the session to check validity.

2. There is inconsistency in format when asking Hal to update a scheme.  Often Hal chooses to change the format of one scheme, which cannot then be used with other unchanged formats.  I therefore have to update manually.  I want Hal to update to avoid this step.

3. There is a problem with coherency between runs.  It would be helpful to have a bot that only considered coherency, listed proposed changes for approval, then output the original schemes with only those changes applied.  This last step (diffs) may be better as an isollate. 

4. When given a list of operations to carry out on a list, Hal stalls.  E.g. I ask it to carry out an operation on a number of files, say 8, and it gets to 4 and stops.  It still remembers the full list, but it needs prodded to continue.  

(Ref: TracerBullet07/Bots/hal_v0.2/sessions/01/session.md)

Here's an example, where Hal remembers the batch to do, but stalls, resulting in me having to tell it to "Proceed".

User:
"I'm about to give you a list of schemes. Take each one in turn. For each you are to:

Provide the updated scheme, if you have suggested one in this session. If you have suggested more than one, give the latest.
Retrieve the original scheme I uploaded, and provide a list of diffs between the new one, and the original.
Here is the list of schemes:

1. Driver Scheme 
2. Event Log Scheme 
3. Location Scheme 
4. Operational Constraints Scheme 
5. Plan Scheme 
6. Roles and Responsibilities 
7. Scheme Route Scheme 
8. Truck Information Scheme
"

Hal:
<Generates appropriate output for 1-2>

"Given that no specific updates were proposed during this session for the Event Log Scheme, there are no differences to highlight between the newly suggested schema and the original.

Let’s proceed to the next scheme in the list for update and difference analysis."

<Stalls>

User:
"Proceed"

Hal:
<Generates appropriate output for 3-4>
"Given that no changes were suggested within this session for the Operational Constraints Scheme, there are no differences to highlight between the original and any newly proposed updates.

Next, let’s move on to retrieve the original scheme for the next item in the list, Plan Scheme, to continue the requested process."

<Stalls>

User:
"Proceed"

5. Hal often truncatates answers e.g. for JSON despite me telling him not to do that.  This means that I can't trust that his output is immediately usable, a characteristic we'll need when getting bots to generate dataspecs.

