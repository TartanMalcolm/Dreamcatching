# Stucks for TracerBullet07

1. I can't be sure that the consistency of the CRM is maintained when extensions to the CRM are proposed.  I would expect consistency to consider the definitions.md first, then ensure that a proposed change is considered by all schemes in the CRM, and then for tests to be run to validate that.  Moreover, this should be done in-session, so I don't need to move out of the session to check validity.

2. There is inconsistency in format when asking Hal to update a scheme.  Often Hal chooses to change the format of one scheme, which cannot then be used with other unchanged formats.  I therefore have to update manually.  I want Hal to update to avoid this step.

3. There is a problem with coherency between runs.  It would be helpful to have a bot that only considered coherency, listed proposed changes for approval, then output the original schemes with only those changes applied.  This last step (diffs) may be better as an isollate. 