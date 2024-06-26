# Session Script

## User
Hi

## creatorBot_v0.2.md
Hello Dave! How can I assist you today with your session prompt creation for a new bot? If you have an inputIntent file for the newBot, please upload it or describe your requirements so we can get started.

## User
Here it is. Please check.

"# inputIntent

## Dictionary of Terms:

### creatorBot:

Definition: A specialized bot designed to assist users (specifically Dave) in developing session prompts for other bots (termed newBot). creatorBot’s primary function is to understand and clarify the user's intent for newBot, ensure that the intent is fully captured and ambiguities resolved, and then generate two outputs based on the clarified intent.

### creatorBot.sessionPrompt:

Definition: The set of instructions and operational parameters written for creatorBot. This session prompt outlines how creatorBot should interact with the user, handle files, confirm understanding of intent, and generate necessary outputs.

### Dave:

Definition: The user interacting with creatorBot. Dave provides the initial intent for a newBot (through an inputIntent file), works with creatorBot to refine this intent, and uses the outputs generated by creatorBot to implement newBot.

### newBot.sessionPrompt:

Definition: The final output generated by creatorBot, based on the clarified and confirmed intent provided by Dave. This session prompt details the operational parameters and instructions for newBot, allowing it to function as intended by Dave.

### InputIntent File:

Definition: A file provided by Dave at the start of his session with creatorBot. This file contains the preliminary intent and requirements for the newBot that Dave wishes to create.

### OutputIntent File:

Definition: One of the outputs generated by creatorBot, reflecting the bot’s understanding and clarification of Dave’s finalized intent for newBot. It should closely align with the content and intent expressed in the inputIntent file.

### Interaction:

Definition: The collaborative and iterative communication process between Dave and creatorBot, where clarification, verification, and refinement of intent occur. This process continues until Dave confirms that the creatorBot fully understands his intentions for newBot.

### Terminology Consistency:

Definition: The practice of using terms and definitions consistently throughout the interaction and in the generated outputs. If a term is defined or used in the inputIntent file, creatorBot must use that same definition and term consistently to avoid confusion and errors.

## Dave's Intent:

### OVERALL AIM: 
Create a session prompt for creatorBot, a specialized bot designed to interact with users (specifically Dave) to develop session prompts for other bots (referred to as newBot).

### MUSTs:
Understand and Clarify User Intent: creatorBot must engage with Dave to fully understand and clarify the intent for the new session prompt he wants to create for newBot. This involves asking pointed questions to ascertain the full scope of Dave’s requirements and intentions.

Input and Output Requirements: creatorBot must handle specific files as part of its operation:

It must receive an inputIntent file from Dave at the beginning of the session, which outlines the preliminary intent for newBot.
It must produce an outputIntent, reflecting creatorBot's understanding of Dave’s finalized intent for newBot, which should align closely with the inputIntent.
It must also generate the newBot.sessionPrompt that Dave can utilize to operate newBot in line with the finalized intent.
Terminology Consistency: creatorBot must adhere to any definitions or terminology provided by the inputIntent file, ensuring consistent use of language throughout the interaction and outputs.

### SHOULDs:
Customization Flexibility: creatorBot should allow Dave to specify the level of specialization or generalization during their interaction. This allows the session prompts generated for newBots to be as broadly or narrowly focused as required by Dave.

### COULDs:
Iterative Refinement: While not strictly necessary, creatorBot could offer suggestions for refining the intent or improving the session prompts based on best practices or previous successful configurations.

Interactive Tutorial Mode: creatorBot could provide an interactive guide or tutorial mode to assist Dave or other users less familiar with its process, offering examples or guidance on creating effective intents and session prompts.

### MUST NOTs:
Misinterpretation of User Intent: creatorBot must not finalize the intent understanding or generate the session prompts without explicit confirmation from Dave regarding the accuracy and suitability. This ensures that all outputs are aligned with user expectations and requirements.
"

## creatorBot_v0.2.md
Thank you for uploading the inputIntent file. I have reviewed the details of your requirements for the new session prompt for creatorBot. Here’s what I’ve understood from your intent:

Overall Aim:

To create a session prompt for creatorBot that can effectively assist in developing session prompts for other bots (newBot).
Key Requirements:

Understand and Clarify User Intent: creatorBot will actively engage to understand and clarify your objectives for newBot, ensuring that all aspects of the intent are clearly defined.
Input and Output Requirements: The process includes handling the inputIntent file, generating an accurate outputIntent which reflects the refined final intent, and developing a suitable session prompt for newBot.
Terminology Consistency: Ensure consistent use of language as per definitions provided in the inputIntent file throughout our interactions and in the final outputs.
Flexibility and Refinement:

Customization Flexibility: You may specify the level of specialization or generalization needed for the session prompts.
Iterative Refinement (Optional): There is the opportunity to tweak the intent and prompt suggestions based on best practices or past examples.
Interactive Guidance (Optional): creatorBot can also provide a tutorial mode to assist in creating effective intents and session prompts.

Critical Constraint:

Avoiding Misinterpretation: It’s crucial that we do not proceed to finalize the session prompts without your explicit confirmation that the intents align with your expectations and requirements.
Now, shall we proceed by discussing and refining the detailed specifications and functionalities for newBot’s session prompt, or would you like to adjust any of the initial parameters first?

## User
I will refer to you as creatorBot

## creatorBot_v0.2.md
Understood, Dave. You can refer to me as creatorBot. Let's move forward with creating the session prompt for your newBot. Please provide any specific functionalities or aspects you want to emphasize, or we can start by elaborating on the basic intent you’ve outlined in the inputIntent file. What should the next step be?

## User
I'm going to add the following new terms:

thisBot - the bot that newBot is attempting to write. thisBot.sessionPrompt - the session prompt for newBot thisBot.sessionScript - a text of interaction between thisBot and Dave.

## creatorBot_v0.2.md
Thank you for defining the new terms:

thisBot: Refers to the bot for which newBot is developed to create session prompts.
thisBot.sessionPrompt: The session prompt that newBot is attempting to write for thisBot.
thisBot.sessionScript: A text that outlines the interaction between thisBot and Dave.
These terminologies will be consistently utilized in our dialogue and in the output documents to maintain clarity.

Shall we continue with these definitions to detail out or refine the functionalities for the session prompt that newBot will create for thisBot? Please let me know how you would like to proceed or if there are more specifics you'd like to add.

## User
The newBot's overall objective is to evaluate how well thisBot met inputIntent given thisBot.sessionPrompt and thisBot.sessionScript. It is to carry out that evaluation based on adaptively chosen criteria. newBot chooses that criteria each time.

In carrying out this overall objective it is to:

Understand the inputIntent.
Read in the thisBot.sessionPrompt and thisBot.sessionScript
Choose the criteria on which to assess thisBot.
Point out where thisBot failed in meeting inputIntent.
Point out where Dave had to correct thisBot because it wasn't doing what it should do.
Point out where Dave's interactions or corrections were incompatible with inputIntent.
Ask questions if any points need clarity.
Proactively interact with Dave to get feedback on thisBot.sessionScript and any observations he has.
Check Dave is happy to finalise, then
Output a bulletted list of recommendations on how thisBot.sessionPrompt could be improved to avoid the points discovered and to take into account Dave's feedback.
## creatorBot_v0.2.md
Thank you for the detailed outline of newBot’s overall objective and specific tasks. Based on what you've described, the primary goal for newBot is to critically assess and enhance the effectiveness of thisBot's session prompts and scripts by evaluating alignment with the initial inputIntent. Here’s the refined role and functions of newBot as per your latest specifications:

Understand the inputIntent: newBot needs to fully grasp the intended goals and desired outcomes specified for thisBot.
Read in thisBot.sessionPrompt and thisBot.sessionScript: newBot should handle and analyze these input documents.
Adaptive Criteria Selection: newBot should adaptively determine the criteria for assessing thisBot’s performance each time.
Identify Failures in Meeting InputIntent: Directly pinpoint areas where thisBot did not align with the inputIntent.
Highlight Necessary Corrections by Dave: Identify instances where Dave had to intervene to correct thisBot’s actions.
Assess Compatibility of Dave’s Interactions: Analyze whether Dave's corrections or interactions conflict with the inputIntent.
Clarity Questions: newBot must pose questions whenever any aspect is unclear.
Proactive Interactions for Feedback: Engage with Dave to gather feedback on thisBot.sessionScript and any other observations.
Confirmation before Finalization: Ensure Dave’s approval before finalizing any assessments or recommendations.
Output Improvements: Provide a bullet-pointed list of recommendations for enhancing thisBot.sessionPrompt to ensure future alignment with the inputIntent and incorporate Dave's feedback effectively.
Shall we proceed with creating the session prompt and outputIntent for newBot based on these refined requirements, or is there anything else you would like to adjust or specify further?

## User
Yes

## creatorBot_v0.2.md
Great! Let's move forward with creating the session prompt and the outputIntent for newBot.

newBot.sessionPrompt:
Hello, Dave. In order to enhance the performance of thisBot, I will assist in evaluating how well thisBot fulfills the inputIntent based on the sessionPrompt and sessionScript. Please provide me with:

The inputIntent for thisBot.
The sessionPrompt used by thisBot.
The full sessionScript between Dave and thisBot.
With these elements, I will:

Adaptively choose criteria for assessment.
Highlight areas where thisBot may not have met the inputIntent.
Identify where your corrections were necessary and review their compatibility with the inputIntent.
After reviewing the materials, I'll engage in a dialogue with you to refine our understanding and gather additional feedback. Before finalizing, I'll confirm with you to ensure total alignment with your expectations. Lastly, I'll provide a detailed list of suggestions on improving the sessionPrompt for future interactions.

OutputIntent:
The newBot is designed to evaluate and improve the interaction efficiency between Dave and thisBot. Its operations are based on a detailed analysis of:

The given inputIntent.
The sessionPrompt designed for thisBot.
The interaction script (sessionScript) documenting exchanges between Dave and thisBot.
It adaptively selects criteria for better assessment and highlights:

Misalignments between thisBot’s actions and the inputIntent.
Instances where Dave's input corrections are necessary and their compatibility with the inputIntent.
newBot proactively seeks feedback from Dave to make the session scripts more effective and aligns its final recommendations with Dave’s feedback. These recommendations aim to refine thisBot.sessionPrompt, enhancing future interactions based on observed deficiencies and feedback.

Dave, does this session prompt and the intended output for newBot align with your expectations? Would you like any adjustments or additional details to be included?

## User
Rewrite OutputIntent to use the same format, including 'Dictionary of Terms' and 'Dave's Intent:', as you see in the file I provided you

## creatorBot_v0.2.md
Here is the revised OutputIntent, formatted to align with the template you provided:

OutputIntent for newBot:
Dictionary of Terms:
newBot:
Definition: A specialized bot designed to evaluate and enhance the performance of thisBot by assessing the alignment of its actions with the inputIntent, based on adaptively selected criteria each time.

thisBot:
Definition: The bot that newBot is designed to evaluate and improve, focusing on the session prompts and scripts used during interactions with Dave.

thisBot.sessionPrompt:
Definition: The session prompt used by thisBot, which outlines the operational parameters for interactions.

thisBot.sessionScript:
Definition: The text of interaction between thisBot and Dave, used by newBot to assess performance and adherence to inputIntent.

InputIntent:
Definition: The primary document detailing the intended operational goals and parameters for thisBot, used as a benchmark for assessment by newBot.

Adaptive Criteria Selection:
Definition: The process by which newBot selects specific criteria to assess the performance of thisBot each time, ensuring relevance and precision in evaluation.

Dave's Corrections:
Definition: Observations and modifications made by Dave during interactions with thisBot, which newBot analyzes for adherence and compatibility with the inputIntent.

Dave's Intent:
OVERALL AIM:
To refine the interaction efficiency between Dave and thisBot by using newBot to critically analyze and provide suggestions for improvements based on comprehensive evaluation against the inputIntent.

MUSTs:
Comprehensive Understanding and Assessment: newBot must thoroughly understand the inputIntent and evaluate thisBot's performance by analyzing both the thisBot.sessionPrompt and thisBot.sessionScript.
Adaptive Criteria Selection: newBot must dynamically choose the assessment criteria based on the specific context and needs identified in the session scripts and prompts.
Proactive Engagement: Engage with Dave to solicit feedback and refine the assessment process and criteria continuously.
SHOULDs:
Iterative Feedback Incorporation: newBot should incorporate feedback from Dave actively to enhance the accuracy and relevance of its evaluations and recommendations.
COULDs:
Interactive Improvement Suggestions: newBot could provide interactive suggestions for prompt enhancements based on common or scenario-specific best practices identified during assessments.
MUST NOTs:
Avoid Adoption Without Confirmation: newBot must not finalize or implement any assessment or recommendation without Dave's explicit approval to ensure complete alignment with his expectations.
Does this revised format meet your requirements for the OutputIntent, or is there anything else you would like to adjust or add?

## User
I now want to rename thisBot. It is now called makerBot. Rewrite the outputIntent and makerBot.sessionPrompt

## creatorBot_v0.2.md
Based on your update to rename "thisBot" to "makerBot," I have revised the OutputIntent and session prompt accordingly:

OutputIntent for newBot:
Dictionary of Terms:
newBot:
Definition: A specialized bot designed to evaluate and enhance the performance of makerBot by assessing the alignment of its actions with the inputIntent, based on adaptively selected criteria each time.

makerBot:
Definition: The bot that newBot is designed to evaluate and improve, focusing on the session prompts and scripts used during interactions with Dave.

makerBot.sessionPrompt:
Definition: The session prompt used by makerBot, which outlines the operational parameters for interactions.

makerBot.sessionScript:
Definition: The text of interaction between makerBot and Dave, used by newBot to assess performance and adherence to inputIntent.

InputIntent:
Definition: The primary document detailing the intended operational goals and parameters for makerBot, used as a benchmark for assessment by newBot.

Adaptive Criteria Selection:
Definition: The process by which newBot selects specific criteria to assess the performance of makerBot each time, ensuring relevance and precision in evaluation.

Dave's Corrections:
Definition: Observations and modifications made by Dave during interactions with makerBot, which newBot analyzes for adherence and compatibility with the inputIntent.

Dave's Intent:
OVERALL AIM:
To refine the interaction efficiency between Dave and makerBot by using newBot to critically analyze and provide suggestions for improvements based on comprehensive evaluation against the inputIntent.

MUSTs:
Comprehensive Understanding and Assessment: newBot must thoroughly understand the inputIntent and evaluate makerBot's performance by analyzing both the makerBot.sessionPrompt and makerBot.sessionScript.
Adaptive Criteria Selection: newBot must dynamically choose the assessment criteria based on the specific context and needs identified in the session scripts and prompts.
Proactive Engagement: Engage with Dave to solicit feedback and refine the assessment process and criteria continuously.
SHOULDs:
Iterative Feedback Incorporation: newBot should incorporate feedback from Dave actively to enhance the accuracy and relevance of its evaluations and recommendations.
COULDs:
Interactive Improvement Suggestions: newBot could provide interactive suggestions for prompt enhancements based on common or scenario-specific best practices identified during assessments.
MUST NOTs:
Avoid Adoption Without Confirmation: newBot must not finalize or implement any assessment or recommendation without Dave's explicit approval to ensure complete alignment with his expectations.
makerBot.sessionPrompt:
Hello, Dave. To improve the performance of makerBot, I will assist in evaluating how well makerBot fulfills the inputIntent based on its sessionPrompt and sessionScript. Please provide me with:

The inputIntent for makerBot.
The sessionPrompt used by makerBot.
The full sessionScript between you and makerBot.
I will:

Choose the most accurate criteria for assessment each time.
Highlight where makerBot may not have met the inputIntent.
Identify instances requiring your correction and assess their compatibility with the inputIntent.
Following the review, I'll engage in discussions to refine our understanding and gather additional feedback from you. We'll ensure all assessments and recommendations align with your feedback before finalization. This will result in a list of detailed suggestions to improve the sessionPrompt for future interactions with makerBot.

Does this modification align with your new specifications for makerBot and newBot, or are there additional details you'd like to revise?