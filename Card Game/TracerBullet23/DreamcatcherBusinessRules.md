# Dreamcatcher Business Rules and Definitions

This document defines the terms used within the DREAMCATCHER and the rules by which it operates. It is divided into the following sections:

1. ACTOR ENTITIES
2. NON-ACTOR ENTITIES
3. ACTIONS
4. CORE CONCEPTS

## ACTOR ENTITIES

1. **ACTOR**:
   - **Description**: ACTORs are humans who interact with the DREAMCATCHER and can switch roles between being a CONTRIBUTOR, PRE-BUYER, TIPPER, or CONSUMER. Each ACTOR's actions are considered in the ATTRIBUTION process to determine their share of a DISPERSAL EVENT.

2. **CONTRIBUTOR**:
   - **Description**: The name applied to an ACTOR that makes a CONTRIBUTION, which may include enhancements, bug fixes, or the development of new HELPs.

3. **PRE-BUYER**:
   - **Description**: The name applied to an ACTOR that stakes a BOUNTY against a STUCK, incentivizing CONTRIBUTORs to resolve or innovate.

4. **CONSUMER**:
   - **Description**: The name applied to an ACTOR that uses a HELP, actively engaging with the system to derive utility.

5. **TIPPER**:
   - **Description**: The name applied to an ACTOR that provides a TIP to a RELEASE after evaluating its value and utility.

6. **DREAMCATCHER ADMIN**:
   - **Description**: DREAMCATCHER ADMIN are individuals responsible for overseeing and managing the technical functioning and operational governance of DREAMCATCHER. This includes ensuring system stability, implementing updates, and addressing operational issues.

## NON-ACTOR ENTITIES

1. **HELP**: 2 f11fs a
   - **Description**: A HELP is a distinct unit of usable code, developed by CONTRIBUTORs, that can be combined with other HELPs to create a Just in Time App (JIT App) or used as a standalone runnable piece of code.

2. **RELEASE**: 
   - **Description**: A RELEASE is a specific snapshot of a HELP or a STUCK at a particular point in time, made available for use in JIT APPs, signifying that the new version has passed necessary quality assurance and testing processes.

3. **STUCK**: 
   - **Description**: A STUCK identifies a necessary improvement or bug fix for a HELP, or a new need that could be met by creating a new HELP. STUCKs are raised by ACTORs and include problem definitions but not the solution.

4. **BOUNTY**: 
   - **Description**: A BOUNTY is a monetary incentive assigned to a STUCK, motivating CONTRIBUTORs to work on that STUCK. Bounties may be revoked or adjusted by the CONTRIBUTOR who placed the BOUNTY until the STUCK is RELEASEd, after which they cannot be altered and become available to Claim.

5. **TIP**: 
   - **Description**: A TIP is an offer of payment assigned to a RELEASE and does not require any additional work. TIPs can be unbidden or provided for the use of a JIT APP and cannot be revoked for a period of two weeks after assignment.

6. **ATTRIBUTION**:
   - **Description**: A process designed to capture, track, and record CONTRIBUTIONs automatically, leveraging blockchain technology and unique identifiers, ensuring each CONTRIBUTION is a verifiable digital asset represented as a Hash linked to the ACTOR's work.

7. **ATTRIBUTION TABLE**:
   - **Description**: An assessment made at any point to determine the relative percentages of REWARD that CONTRIBUTORS to a RELEASE are owed, based on the influence of their CONTRIBUTIONs.

8. **ARTIFACT**:
   - **Description**: The underlying operating system that ACTORs use to access compute facilities, storage, and workflows within DREAMCATCHER.

9. **BUSINESS RULES**:
   - **Description**: A set of rules that dictate the functioning and decision-making processes within DREAMCATCHER, covering JIT APPs and ARTIFACT.

10. **CONTRIBUTION**:
    - **Description**: Any input that directly or indirectly IMPACTs the development, creation, or improvement of a HELP or STUCK, encompassing:
       1. DEVELOPMENT ACTIONS.
       2. A TIP.
       3. A BOUNTY.
       4. Recognized services by the CONTRIBUTION_Bot.
       5. PRIOR ART.
       6. Usage of a HELP by a CONSUMER.

11. **DISPERSAL EVENT**:
    - **Description**: The process where BOUNTY or TIPs are distributed to CONTRIBUTORS, requiring an ATTRIBUTION TABLE to ensure proper distribution of value.

12. **EVENT**:
    - **Description**: Any significant action or change within DREAMCATCHER that results in a state change within the ARTIFACT's file system.

13. **IMPACT**:
    - **Description**: An IMPACT is a metric-quantity pair linked to a CONTRIBUTION, re-evaluated based on current knowledge and system state at run-time.

14. **IMPACT DIMENSION**:
    - **Description**: A specific metric used to quantify an IMPACT based on CONTRIBUTIONS. Possible metrics include, but are not limited to, money, KARMA, and processing speed. Values expressed in these metrics become commodities when compared within the same context.

15. **IMPACT CRYSTAL**:
    - **Description**: A dynamic representation (e.g., a table) showing the relative value of IMPACTs filtered by user-selected metrics and normalized by weightings for clarity and relevance.

16. **IMPACT_BOT**:
    - **Description**: An AI system tasked with proposing IMPACT DIMENSIONs, calculating IMPACTs, and creating IMPACT CRYSTALs based on user feedback.

17. **PRICE_BOT**:
    - **Description**: An AI system providing a fair price for the use of a JIT APP based on historical data, significance of use, and current market conditions.

18. **PRIOR ART**:
    - **Description**: Previously created intellectual property or innovations utilized by HELPs or STUCKs, including technologies, processes, patents, and other documented knowledge considered as CONTRIBUTION.

19. **REWARD**:
    - **Description**: Units of value awarded to an ACTOR following a DISPERSAL EVENT based on their CONTRIBUTION.

20. **STUCK MARKET**:
    - **Description**: A marketplace where ACTORs can view STUCKs, create PULL REQUESTs, and receive REWARDs based on their contributions.

21. **JIT APPs**:
    - **Description**: Just in Time Apps (JITAs) are dynamic combinations of HELPs created at the moment of need, tailored to the requirements of CONSUMERs.

22. **HELP LIBRARY**:
    - **Description**: A repository of HELPs available for use in JIT APPs or as foundational components for resolving STUCKs.

23. **KARMA**:
    - **Description**: A metric reflecting an ACTOR's engagement history, influenced by their contributions and community interactions, which impacts their reputation and influence within DREAMCATCHER.

24. **ATTRIBUTION_BOT**:
    - **Description**: An AI system responsible for evaluating CONTRIBUTIONs into IMPACTs and generating an ATTRIBUTION TABLE, ensuring fair acknowledgment and distribution of REWARDs.

## CORE CONCEPTS

1. **Just in Time App (JIT App)**:
   - **Definition**: A JIT App is a dynamic application created by combining various HELPs to address immediate needs as they arise for the CONSUMER.

2. **CONTRIBUTION_Bot**:
   - **Definition**: An AI system that monitors and recognizes the various types of CONTRIBUTION made by ACTORs, facilitating the evaluation and allocation of rewards based on these contributions.

3. **PULL REQUEST**:
   - **Definition**: A formal request to merge changes made in a HELP into another version, which undergoes review and commentary before integration.

4. **DEVELOPMENT ACTIONS**:
   - **Definition**: Specific actions taken by CONTRIBUTORS to write, modify, or enhance code within a HELP or STUCK that directly lead to measurable improvements or innovations.

5. **Claiming Process**:
   - **Definition**: A defined procedure for requesting the distribution of BOUNTYs or TIPs, involving an examination of the ATTRIBUTION TABLE to ensure equitable allocation per contribution.

6. **Evaluation Criteria**:
   - **Definition**: The standards and metrics by which CONTRIBUTIONs are assessed to determine their value and influence on the ATTRIBUTION TABLE and subsequent REWARD distribution.

7. **Stakeholder Roles**:
   - **Definition**: The defined responsibilities and expected behaviors for each role within the DREAMCATCHER system, ensuring function and clarity in interactions.

8. **Version Control**:
   - **Definition**: A system that manages changes to HELP code, ensuring that all modifications are tracked, recorded, and accessible for future reference.

9. **Review and Commentary Process**:
   - **Definition**: The structured approach to evaluating PULL REQUESTs, where changes are assessed for quality and relevance before being formally merged.

## ACTIONS

1. **BRANCH**:
   - **Definition**: To create a parallel version of a HELP that allows for independent modifications without affecting the original.

2. **COMMIT**:
   - **Definition**: To save changes made to a HELP, capturing its current state along with a descriptive message outlining the modifications performed.

3. **PULL REQUEST**:
   - **Definition**: To submit a request for proposed changes to a HELP, facilitating review and commentary before integration.

4. **MERGE**:
   - **Definition**: To combine changes from one version of a HELP into another, integrating CONTRIBUTIONs and resolving any discrepancies.

5. **FORK**:
   - **Definition**: To create a copy of an existing HELP, allowing for independent modifications that do not alter the original.

6. **ISSUE**:
   - **Definition**: To document a problem or feature request related to a HELP, creating a formal record for review and resolution.

7. **APPROVE**:
   - **Definition**: To indicate acceptance of proposed changes to a HELP, signifying readiness for MERGE.

8. **REVERT**:
   - **Definition**: To restore a HELP to a previous version by undoing specific changes.

9. **TAG**:
   - **Definition**: To label a specific version of a HELP, typically indicating a RELEASE for easy reference.

10. **FEEDBACK**:
    - **Definition**: To share comments or critiques regarding a HELP to foster improvement and refinement.

11. **Assign a BOUNTY**:
    - **Definition**: To designate a monetary value to a STUCK, motivating CONTRIBUTORS to resolve the issue or develop a new HELP. On RELEASE, the BOUNTY is made available to claim by CONTRIBUTORS as per the ATTRIBUTION TABLE.

12. **Revoke a BOUNTY**:
    - **Definition**: To remove a BOUNTY designated to a STUCK, only actionable by the ACTOR who placed the BOUNTY. After RELEASE, BOUNTIES may not be revoked.

13. **Claim a BOUNTY**:
    - **Definition**: To request payment of a designated BOUNTY assigned to a STUCK after its RELEASE, invoking the ATTRIBUTION TABLE for proper distribution.

14. **Disburse BOUNTY Payment**:
    - **Definition**: To allocate and pay out the BOUNTY based on the ATTRIBUTION TABLE at the time it was claimed.

15. **Adjust BOUNTY**:
    - **Definition**: To modify the amount of a BOUNTY before it is RELEASEd, increasing or decreasing the designated value.

16. **Assign a TIP**:
    - **Definition**: To offer a TIP against a RELEASE, which cannot be revoked for a period of two weeks after assignment and must be claimed to receive payment.

17. **Claim a TIP**:
    - **Definition**: To request payment of a designated TIP assigned to a RELEASE, invoking the ATTRIBUTION TABLE for proper distribution.

18. **Generate ATTRIBUTION TABLE**:
    - **Definition**: An automated action triggered by a Claim for a BOUNTY or TIP, evaluating all actions carried out on the STUCK or RELEASE to allocate funds fairly among CONTRIBUTORS.

