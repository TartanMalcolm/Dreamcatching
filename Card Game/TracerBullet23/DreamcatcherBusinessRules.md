### Dreamcatcher Business Rules and Definitions

This document defines the terms used within the Dreamcatcher, and the rules by which it operates.  It is divided into the following sections:

1. ACTOR ENTITIES.
2. NON-ACTOR ENTITIES.
3. ACTIONS

### ACTOR ENTITIES

1. **ACTOR**:
   - **Description**: ACTORs are humans who interact with the DREAMCATCHER.  From time to time they can switch roles between being a CONTRIBUTOR, PRE-BUYER or CONSUMER. Each ACTOR's actions are considered in the ATTRIBUTION process to determine their share of a DISPERSAL EVENT. 

2. **CONTRIBUTOR**:
   - **Description**: The name applied to an ACTOR that makes a CONTRIBUTION.  

3. **PRE-BUYER**:
   - **Description**: The name applied to an ACTOR that stakes a BOUNTY against a STUCK.   

4. **CONSUMER**:
   - **Description**: The name applied to an ACTOR that uses a HELP.   

5. **TIPPER**:
   - **Description**: The name applied to an ACTOR that provides a TIP to a RELEASE.   

6. **DREAMCATCHER ADMIN**:
    - **Description**: DREAMCATCHER ADMIN are individuals responsible for overseeing, maintaining, and managing the technical and operational aspects of DREAMCATCHER. Their role includes ensuring the DREAMCATCHER runs smoothly, implementing necessary updates or changes, and addressing any issues that arise within the system. Currently, DREAMCATCHER ADMIN has the authority to make decisions about the DREAMCATCHER's functionality, security, and overall governance. In the future, this may be devolved to the community.

### NON-ACTOR ENTITIES

1. **HELP**: 
   - **Description**: A HELP is a distinct unit of usable code. It can be combined with other HELPs in order to create a Just in Time App or used as a standalone runable piece of code. HELPs are under version control and are the output of work from CONTRIBUTORs.

2. **RELEASE**: 
   - **Description**: A RELEASE is a specific snapshot of a HELP or a STUCK at a particular point in time, made available for use in JIT APPs. A RELEASE signifies that the new version of the HELP has passed through necessary  testing processes and is ready for use. A RELEASE can refer to either a single HELP or a combination of HELPs used in a Just in Time App.

3. **STUCK**: 
   - **Description**: A STUCK identifies a change that is needed to improve a HELP, a bug or problem that needs to be solved to improve the HELP, or an identifiied new need that could be met by creating a new HELP. A STUCK includes information about what the new function must do (but not the solution), tracks CONTRIBUTIONs, and provides context for discussions about the HELP being worked on. STUCKs may have a BOUNTY assigned to them.  STUCKs are raised by ACTORs.

4. **BOUNTY**: 
   - **Description**: A BOUNTY is a monetary incentive assigned to a STUCK intended to motivate CONTRIBUTORs to work on that STUCK. Bounties may be revoked or adjusted by the CONTRIBUTOR who placed the BOUNTY up to the point where the STUCK is RELEASEd, after which point it becomes available to Claim.  Once claimed, Bounties are recorded as CONTRIBUTIONs.

5. **TIP**: 
   - **Description**: A TIP is an offer of payment that is assigned to a RELEASE. TIPs do not require completion of any additional work. TIPs can be unbidden, or can be a payment for the use of a JIT APP.  TIPs can be claimed by the CONTRIBUTORs to that RELEASE through the ATTRIBUTION TABLE.  Once claimed, TIPs are recorded as CONTRIBUTIONs.

6. **ATTRIBUTION**:
   - **Description**: A process designed to automatically capture, track, and record CONTRIBUTIONs, leveraging blockchain technology and a unique identifier. Each CONTRIBUTION is referred to as a Hash, serving as a unique and verifiable digital asset that represents the ACTOR's work. Hashes act as dimensions in an IMPACT CRYSTAL. This system ensures that recognition and REWARDs are based on the tangible IMPACT of CONTRIBUTIONs.

7. **ATTRIBUTION TABLE**:
   - **Description**: An assessment made at any point in time about the relative percentages of REWARD that CONTRIBUTORS to a RELEASE are owed.

8. **ARTIFACT**:
   - **Description**: The underlying operating system which ACTORs use to access compute facilities, storage, file manipulation, and workflows within DREAMCATCHER.

9. **BUSINESS RULES**:
   - **Description**: A set of rules that dictate the functioning and decision-making processes within DREAMCATCHER including JIT APPs and ARTIFACT.

10. **CONTRIBUTION**:
   - **Description**: Any input that directly or indirectly IMPACTs the development, creation, or improvement of a HELP or STUCK.  CONTRIBUTIONs are always recorded in ARTIFACT as EVENTs.  Types of CONTRIBUTIONs are:
    1. DEVELOPMENT ACTIONS
    2. A TIP
    3. A BOUNTY
    4. Any service provided by an ACTOR that is recognised by the CONTRIBUTION_Bot as promoting the creation or improvement of the STUCK or HELP.
    5. PRIOR ART that directly or indirectly IMPACTs the STUCK or HELP. 
    6. Comsumption or use of a HELP by a CONSUMER.

11. **DISPERSAL EVENT**:
   - **Description**: The process where the BOUNTY or TIPs are distributed to CONTRIBUTORs. DISPERSAL EVENTs and require an ATTRIBUTION TABLE in order to properly disperse the value to the CONTRIBUTORs in the correct proportions.  

12. **EVENT**:
   - **Description**: Any significant action, occurrence, or change within DREAMCATCHER that leads to a state change within the file system of ARTIFACT. 

13. **IMPACT**:
   - **Description**: An IMPACT is a metric:quantity pair value matched to a CONTRIBUTION (and which therefore is linked to the CONTRIBUTORs to that CONTRIBUTION).  IMPACTs are re-calculated based on current knowledge and system state at run-time.  

14. **IMPACT DIMENSION**:
   - **Description**: A specific metric used to measure an IMPACT based on CONTRIBUTIONS.  There can be any number of types of metric (e.g. money, KARMA, utility, the speed of processing for a HELP).  A value expressed in units of the metric for a CONTRIBUTION are commodities when compared to other other CONTRIBUTIONS within the same Help or Stuck who use the same metric. E.g. If a CONTRIBUTION has five units of 'metric 1', a second CONTRIBUTION also has five units of 'metric 1', they are identical in value. IMPACT DIMENSIONs are used in IMPACT CRYSTALS.

15. **IMPACT CRYSTAL**:
    - **Description**: A representation (e.g. a table), filtered dynamically by an Actor who states which metrics to filter by, which shows the relative value of IMPACTs.  IMPACT CRYSTALs consider what metrics are required to be considered, a weighting to normalise between the metrics, then provides that representation to show the relative value of the IMPACTs being considered.  

16. **IMPACT_BOT**:
    - **Description**: An AI system tasked with proposing IMPACT DIMENSIONs (given feedback from an ACTOR), calculating IMPACTs and creating IMPACT CRYSTALs. 

17. **PRICE_BOT**:
    - **Description**: An AI system provides a fair pricing for the use of a JIT APP. PRICE_BOT takes into account historical pricing data, the significance of the use of the JIT APP to the CONSUMER, and market conditions to advise on the optimal price at time of use. 

18. **PRIOR ART**:
    - **Description**: Previously created intellectual property or innovations used by HELPs or STUCKs. PRIOR ART includes existing technologies, processes, designs, patents, and other documented knowledge that can be drawn upon to inform and support the creation or improvement of new innovations. The use of PRIOR ART is considered a CONTRIBUTION.  The ACTOR who created the PRIOR ART may not be defined, but is still uniquely identified and accrue the results owed to them through DISPERSAL EVENTs.  Once defined as a unique ACTOR, those results are instantiated to that ACTOR.

19. **REWARD**:
    - **Description**: The units of value assigned to an ACTOR following a DISPERSAL EVENT.  

20. **STUCK MARKET**:
    - **Description**: A marketplace where ACTORs can view STUCKs, create PULL REQUESTs, and receive REWARDs.

21. **JIT APPs**:
    - **Description**: JIT APPs, also known as Just in Time Apps or JITAs are combinations of HELPs that are deployed when they are needed based on the needs of the CONSUMER at the time of use. JIT APPs are not pre-built; instead, they are created "just in time" from a library of HELPs.

22. **HELP LIBRARY**:
    - **Description**: A library of HELPs which are available to be used either in a JIT APP or as the basis for solving a STUCK.

23. **KARMA**:
    - **Description**: A conceptual metric used to reflect an ACTOR's historical behavior and engagement within the DREAMCATCHER system. KARMA is influenced by various factors such as the consistency of CONTRIBUTIONs, adherence to fair practices, and the degree of collaboration with other ACTORs. Positive KARMA can enhance an ACTOR's reputation and influence within the DREAMCATCHER, while negative KARMA can result from actions that undermine the community's values. KARMA is considered when determining ATTRIBUTION and dispersal of REWARDs.

24. **ATTRIBUTION_BOT**:
    - **Description**: An AI system responsible for evaluating CONTRIBUTIONs into IMPACTs, and producing an ATTRIBUTION TABLE.  ATTRIBUTION_BOT ensures that CONTRIBUTORs receive fair acknowledgment and REWARDs according to the significance and relevance of their work. This ENTITY plays a crucial role in maintaining transparency and fairness within the DREAMCATCHER system.

### ACTIONS

1. **BRANCH**:
   - **Definition**: To create a parallel version of a HELP that allows CONTRIBUTORs to modify or enhance it independently without affecting the original HELP.

2. **COMMIT**:
   - **Definition**: To save changes made to a HELP, capturing a snapshot of its current state along with a descriptive message outlining the modifications performed.

3. **PULL REQUEST**:
   - **Definition**: Also known as 'PR'.  To submit a request for the proposed changes made to a HELP to be MERGEd into another version of the HELP, facilitating review and commentary before integration.

4. **MERGE**:
   - **Definition**: To combine changes from one version of a HELP into another, integrating CONTRIBUTIONs while resolving any discrepancies between different versions.

5. **FORK**:
   - **Definition**: To create a copy of an existing HELP, allowing for independent modifications that do not alter the original HELP.

6. **ISSUE**:
   - **Definition**: To document and communicate a problem, feature request, or suggestion related to a HELP, creating a formal record for review and resolution that may lead to the creation of a new HELP.

7. **APPROVE**:
   - **Definition**: To indicate acceptance of proposed changes to a HELP after evaluating the modifications, signaling that the changes are ready to be MERGEd.

8. **REVERT**:
   - **Definition**: To undo a previous change made to a HELP by applying adjustments that restore it to a former version, effectively negating the specific modifications.

9. **TAG**:
   - **Definition**: To mark a specific version of a HELP with a label, typically indicating a RELEASE, allowing easy reference to that specific version in the future.

10. **FEEDBACK**:
    - **Definition**: To share comments, suggestions, or critiques regarding a HELP to foster improvement and refinement of its content or functionality.

11. **Assign a BOUNTY**:
   - **Definition**: To designate a monetary value to a STUCK, motivating CONTRIBUTORs to resolve the identified issue or develop a new HELP. On RELEASE the BOUNTY is made available to Claim by CONTRIBUTORs to that RELEASE through the ATTRIBUTION TABLE.  

12. **Revoke a BOUNTY**:
   - **Definition**: To remove a BOUNTY designate a monetary value to a STUCK, motivating CONTRIBUTORs to resolve the identified issue or develop a new HELP. Only the ACTOR who placed the BOUNTY can revoke that BOUNTY. On RELEASE the BOUNTY may not be revoked and is made available to Claim.    

13. **Claim a BOUNTY**:
   - **Definition**: To request the payout of a designated BOUNTY assigned to a STUCK after its RELEASE.  Claims invoke the ATTRIBUTION TABLE to disperse the BOUNTY to the CONTRIBUTORs of that RELEASE.  

14. **Disbirse BOUNTY Payment**:
   - **Definition**: To allocate and pay out the BOUNTY based on the ATTRIBUTION TABLE at the time it was Claimed based on the ATTRIBUTION TABLE at that time.  

15. **Adjust BOUNTY**:
   - **Definition**: To alter up or down the amount of a BOUNTY prior to RELEASE.

16. **Assign a TIP**:
   - **Definition**: To offer to pay a TIP against a RELEASE.  A TIP cannot be revoked for 2 weeks.  A TIP needs to be Claimed to be paid out.  

17. **Claim a TIP**:
   - **Definition**: To request the payout of a designated TIP assigned to a RELEASE.  Claims invoke the ATTRIBUTION TABLE to disperse the TIP to the CONTRIBUTORs of that RELEASE.  

18. **Generate ATTRIBUTION TABLE**:
   - **Definition**: An automated AI action that is triggered by a Claim for a BOUNTY or TIP.  ATTRIBUTION considers all information about actions carried out on the STUCK or RELEASE at that point in time by the CONTRIBUTORs involved, and provides an allocation of the funds to those CONTRIBUTORs.  ATTRIBUTION also takes into account the use of other HELPs that are required and used by this STUCK or RELEASE, and lists those in the ATTRIBUTION TABLE, and generates a TIP to the other HELPs at the point of Dispersal. 






