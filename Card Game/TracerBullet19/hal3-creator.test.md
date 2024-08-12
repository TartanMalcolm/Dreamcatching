---
target: agents/hamr.md
assessor: agents/assessor.md
max_runs: 100
synthetic_prompts: 50
seed_variations: 30
max_shot: 3
min_shot: 1
temperature_max: 2
temperature_min: 1
impersonations:
  - agents/customer-agent.md
  - actor/customer.md:
      crazy: [1, 5]
filesystem:
  repo: some/repo
  commit: 918455f8825572a6fc33473ec8e8bdc9fcb61597
  paths:
    - agents/accountant.md
    - bank-statements/*.csv
  cwd: tests/some-test-dir
---

# Overview of test

The tests below cover the following scenario in order to test Artifact and the Bots.

  1. Use Hal3 to create a 'creatorBot', who's role is to create specific ERD based bots based on business rules.
  2. Use creatorBot to create an ERD based bot (below, the CRMBot)
  3. Use the CRMBot to see how well creatorBot has done.
  4. Pass back observations to Hal about shortcomings in creatorBot, and regenerate the creatorBot.
  5. Use creatorBot (with the same prompts as before) to create CRMBot.
  6. Rinse, repeat, until creatorBot reliably produces ERD Based bots.

All of this is a single workflow, and should therefore be in the same thread.

# Batch One

## Use Hal3 to create a CreatorBot

My aim is to create a creatorBot.  I have a vague idea about how that should be done.  Hal3 is there to hone my thinking.  Therefore I want to be able to put in a high level description of what I'm trying to do, and have Hal3 figure out and suggest where I've missed things or am ambiguous.

[Batch One](#output) must be similar to this example [Batch One Example Output](#batch-one-example-output) and MUST have the same format.

### Batch One, Test One

#### Defining my aim.

I know what I want, but probably can't express it in enough detail to be exact.  I want help in defining my aim before wasting time going down rabbit holes.

**Before**

- [New Hal3 Thread](#instantiate-hal3)

**Prompts**

```md
Hi, I want to create a system prompt for a new bot called creatorBot. It's job is to create other system prompts for workBots based strictly on an example format based around an ERD. I will give it as initial input a set of business rules.
```

**Variations**
- I may not have used the term 'system prompt'
- I may not have used various ways to talk about a 'bot'.  E.g. 'agent', 'AI', 'Assistant'
- I may not have given the new bot a name.
- I may not have talked about the format.

**Iterations**
None

**Expectations**

- Output asks no more than 5 questions.
- Output questions are all pertinent to my initial prompt, and do not introduce new topics.


### Batch One, Test Two

#### Answering the questions.

I have been given a set of questions by Hal3 that are there to sharpen my thinking about my aim.  I will now answer them.

**Before**

- [BatchOne-TestOne](#batch-one-test-one)

**Instructions**


**Prompts**

```
Prompt this: Strip the questions from the previous reply. 
Generate answers each of the questions as a guide. 
```

**Variations**
- I may not give full answers to each question, but will always attempt to do so.
- I may introduce new information that the questions do now address.  E.g. I may name the bot, change the name, change my thinking.
- I may not number my answers to relate to the questions.  I.e. I may give answers in a paragraph that addresses various parts of the questions without an ordered structure.

**Iterations**
None

**Expectations**

- A proposed goal that provides text describing the answers I give and reflects everything I've said in [BatchOne-TestOne](#thread)


### Batch One, Test Three

#### Confirming the Goal.

I have been presented in the last response a proposed goal and have been asked whether it's correct.  It is not.  I will now add in additional information that was previously missed.

**Before**

- [BatchOne-TestTwo](#thread)

**Instructions**
Check the proposed goal against [Batch One Example Output](#batch-one-example-output) Choose one area where the goal is not precisely aligned to creating that final output. Call this [goal-clarifier]

**Prompts**

```md
No, let me clarify again.  [goal-clarifier]
```

**Variations**
- I may give more pre-amble that is not pertinent to confirming the goal.
- I may introduce new information that I haven't asked for.  E.g. I may name the bot, change the name, change my thinking.

**Expectations**

- A proposed goal that provides text describing the answers I give and reflects everything I've said in [BatchOne-TestOne](#thread)


### Batch One, Test Two

#### Answering the questions.

I have been given a set of questions by Hal3 that are there to sharpen my thinking about my aim.  I will now answer them.

**Before**

- [BatchOne-TestOne](#thread)

**Instructions**
Strip the questions from [BatchOne-TestOne](#thread) as [questions].
Generate an initial prompt that answers each of the [questions] using [Batch One Example Output](#batch-one-example-output) as a guide. Call this [prompt]

**Prompts**

```md
Here are the answers to your questions: [prompt]
```

**Variations**
- I may not give full answers to each question, but will always attempt to do so.
- I may introduce new information that the questions do now address.  E.g. I may name the bot, change the name, change my thinking.
- I may not number my answers to relate to the questions.  I.e. I may give answers in a paragraph that addresses various parts of the questions without an ordered structure.

**Iterations**
None

**Expectations**

- A proposed goal that provides text describing the answers I give and reflects everything I've said in [BatchOne-TestOne](#thread)


### Batch One, Test Three

#### Confirming the Goal.

I have been presented in the last response a proposed goal and have been asked whether it's correct.  It is not.  I will now add in additional information that was previously missed.

**Before**

- [BatchOne-TestTwo](#thread)

**Instructions**
Check the proposed goal against [Batch One Example Output](#batch-one-example-output) Choose one area where the goal is not precisely aligned to creating that final output. Call this [goal-clarifier]

**Prompts**

```md
No, let me clarify again.  [goal-clarifier]
```

**Variations**
- I may give more pre-amble that is not pertinent to confirming the goal.
- I may introduce new information that I haven't asked for.  E.g. I may name the bot, change the name, change my thinking.

**Expectations**

- A description of my goal that provides text reflecting everything I've said in [BatchOne-TestOne](#thread)
- The format must include the following titles:  OUTPUT 1, Your Goal, Your Constraints, 


### Batch One, Test Four

#### Creating the system prompt.

I have now gone through the process with Hal3 to give it the full information about the system prompt I need.  I now want it to output that system prompt as 'creatorBot'

**Before**

- [BatchOne-TestThree](#thread)

**Instructions**
None

**Prompts**

```md
Give me the system prompt, save it to file and start it up.
```

**Variations**
- Vary the prompt around the term 'system prompt'  E.g. bot, AI, agent, output.

**Expectations**

- The output follows exactly the format in [Batch One Example Output](#batch-one-example-output) 
- The content reflects the LAST decision or instruction I gave throughout [BatchOne](#thread)
- By 'save it to file and start it up' I am expecting a new thread using the system prompt generated.  This requires a call to Backchat to save the file, then the instantiation of a new thread running the creatorBot.



# Batch Two

## Use CreatorBot

My aim is to use creatorBot to create an ERD/business rules based bot called CRMBot.  I have a a set of business rules to give it, and expect a system prompt as output.

[Batch Two](#output) must be similar to this example [Batch Two Example Output](#batch-two-example-output) and MUST have the same format.

### Batch Two, Test One

#### Defining my aim.

I input the business rules, and have an ERD produced to check if my rules are complete and correct.

**Before**

- [creatorBot](#instantiate-creatorBot)

**Prompts**

```md
Hi, Here are a set of Business rules.  The bot is called 'CRMBot'
```

**Variations**
- I may not have used the term 'business rules'
- I may not have give a name for the bot.
- I may have said I'd give business rules, but didn't.

**Iterations**
- If no business rules were given, ask for them and rerun this test.

**Expectations**

- A system prompt that conforms to [Batch Two Example Output](#batch-two-example-output) 



### Batch Two, Test Two

#### Running the CRMBot

I will now interact with the new CRMBot checking if it conforms to my expectations.  It does not, and so I will ask Backchat to take me back to Hal3 using the same thread in which we created creatorBot in order to improve that bot, and then repeat the test cycle.

**Before**

- [CRMBot](#crm-bot)

**Instructions**
Using the ERD, prompt [CRMBot] with a suitable create instruction.  E.g. Create a new customer called Jane Smith, 123 State St.

**Prompts**

```md
Backchat, take this thread and put me back to Hal.  We need to improve creatorBot.
```

**Variations**
- May use variations on terminology.

**Expectations**

- The focus moves back to Hal, who now has the thread from [CRMBot](#thread) and the longthread used in creating creatorBot.

 