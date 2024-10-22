# NAPP SCENARIO 01 

## INTENT
*Dave, a newcomer to the artifact platform, wants to create a new napp but is unfamiliar with the NAPP-JSON configuration format. He seeks assistance from NappGen, an AI assistant specialized in helping users create and configure napps. Dave occasionally makes mistakes, and NappGen patiently guides him, ensuring that concepts are introduced in a logical order and providing clear explanations at each step.

Dave's intent is to build a Napp that pulls in inspirational quotes to give to his school soccer team, for which he's the coach and therefore responsible for the output.


## NARRATIVE
---

## SCENE 1 - where Dave starts the process

**Dave:** /NappGen. I'd like to create a napp, but I'm not sure how to get started. Can you help me out?

**NappGen:** Hello Dave! Welcome to the Dreamcatcher platform. I'd be happy to help you create your first napp. Let's start from the beginning. Do you know what a napp is?

**Dave:** Not exactly. I just know it's some kind of application I can build here.

**NappGen:** That's right! A napp is a Natural Language App on Dreamcatcher. To write one we need to get some information about what it's allowed to do, whether it calls on other Napps (like calling on other tools/services), then you can give instructions on how it should use these.  Don't worry, I'll guide you through the process, and you can always go back and make changes later.  How does that sound?

**Dave:** Sounds good.

**NappGen:** Excellent! Let's begin by setting up what your napp is to do, and what it needs to do it. The first things we need is what you want to call it (the **"name"**) and a brief description of what it's there to do (the **"description"**). Do you have an idea for a name?

**Dave:** Yes, I want to create a napp called "QuoteFinder" that fetches inspirational quotes.

**NappGen:** Wonderful! That's done. Now, how would you describe in more detail what Quotefinder does?

**Dave:** It fetches random inspirational quotes based on a user's request.  

**NappGen:** Great! Here's what I've put in for the description:  "QuoteFinder fetches random inspirational quotes upon user request, and ensures that it's age appropriate for teenagers, is not political, and is sport oriented".  Sound good?

**Dave:** Yup, that's good.

### SCENE 1 - STATE 1

```json
{
  "name": "QuoteFinder",
  "description": "QuoteFinder fetches random inspirational quotes upon user request."
}
```

## SCENE 2 - where Dave is taken through runtime, a technical aspect he knows nothing about

<NOTES: 
  - NappGen confirms that the user is defaulting to Deno, and therefore needs to call Napps with a tool that can:
    - Takes in Dave's identity.
    - Creates the folder/file structure for this Napp.
    - Set's permissions.>


**NappGen:** Now, we need to specify where your Napp is actually going to be run.  By that I mean, do you have a preference on whether it's runs on Deno, or Python, or Rust?  If you don't know then that's fine, we'll default to Deno as that sounds like where this should go, but do you hace a preference?

**Dave:** I've no idea.

**NappGen:** That's fine. We'll set it to Deno.

<NappGen calls Artifact to create a location on Deno for this Napp.  Up to this point it's all been stored in the thread, but now we need a home for it.  NappGen will need to talk to Artifact to set file permissions from Dave's Identity>

### SCENE 2 - STATE 2

```json
{
  "name": "QuoteFinder",
  "description": "QuoteFinder fetches random inspirational quotes upon user request.",
  "runtime": "deno"
}
```




## SCENE 3 - where Dave is taken through Branding, and uploads the school logo etc.
  - In this scene Dave uploads Branding using a widget on the stateboard
  - NappGen also reviews the current state of the JSON for this Napp with the thread, and so offers up a change in a field previously created.

**NappGen:** Next, there's an optional **"branding"** field where you can include assets like logos or images. Would you like to add any branding now?

**Dave:** I'm building this for a school soccer team, so maybe we put in the school's branding and name, and the name of the school?

**NappGen:** Absolutely! Would you like me to help, or do you already have these and can upload them now?

**Dave:** Yea, I've got them.  How do I upload them?

<NappGen generates a stateboard widget for upload and asks Files to create a folder for the assets.>

**NappGen:** You see on the right the upload button?  Click that and upload each.  If you can add a brief descripion in the field below that button, that will help.

**Dave:** OK, that's done.  

**NappGen:** I've looked at these assets you've just uploaded, and would suggest an update to your description.  How about:

  - Previous Description: It fetches random inspirational quotes based on a user's request.  
  - Proposed Description: It fetches random inspirational quotes based on a user's request. It'll need to filter them to make sure they're age and topic appropriate for a high school soccer team

**NappGen:** Would you like me to update the description?

**Dave:** Sure, go ahead.  

<Description updated>

**NappGen:** OK, that's done.  

### SCENE 3 - STATE 3

```json
{
  "name": "QuoteFinder",
  "description": "QuoteFinder fetches fetches random inspirational quotes based on a user's request. Must filter them based on instructions in the AGENT to make sure they're age and topic appropriate for a high school soccer team.",
  "runtime": "deno",
  "branding": "path/to/branding/assets"
}
```


## SCENE 4 - where Dave is taken through Gateways, and provides a couple of sources for inspirational quotes


**NappGen:** Now, let's talk about **"gateways"**. These are external APIs or services your napp might need to interact with. Does your napp need to access any external services?

**Dave:** Yes, it needs to fetch quotes from the internet.

**NappGen:** Great! Do you have a specific website or websites in mind?

**Dave:** I was thinking of using the Quotable.io and soccer-inspiration.ch.  If there are any others that would be cool.

**NappGen:** Excellent choices! Let me check them out.

<NappGen calls Napps with the following tools:
  - API Library - to get the specific website services he's mentioned.
    - A search in the API library if these sites are already known.  If it is, then add it to the JSON
      NOTE: Do we ask Dave to login if that API requires credentials at this point, or wait under the Napp is constructed now we know there's an API.
  - Scrape
    - It may be that there's no API, it's just an open website, so a scraper will do
      NOTE: A Napp that scrapes an arbitrary website is going to come in handy.
  - Search, scrape, understand API, add to API Library:  Yikes!  But would be cool.

>

**NappGen:** OK, I've added those two.  I've also got access to soccer-quotes, which is another Napp that does something similar to you without the filters.  This will be helpful as you will be able to say what is displayed.  Also, you can always take it out later.  Do you want me to add it?

**Dave:** Sure

**NappGen:** OK.  So I've just added Quotable.io and the soccer-quotes Napp, but it looks like you need to log in to get access to soccer-inspiration.ch.  Do you want me to try with your current credentials?

**Dave:** Sure.  Use my google credentials for now.

<NappGen calls Napps that:
    - attempt a login
>

**NappGen:** It worked!  OK, that's also added to your gateway.

### SCENE 4 - STATE 4

```json
{
  "name": "QuoteFinder",
  "description": "QuoteFinder fetches fetches random inspirational quotes based on a user's request. Must filter them based on instructions in the AGENT to make sure they're age and topic appropriate for a high school soccer team.",
  "runtime": "deno",
  "branding": "path/to/branding/assets",
  "gateways": {
    "production": {
      "Quotable": {
        "url": "https://api.quotable.io"
      },
      "SoccerInspiration": {
        "url": "https://soccer-inspiration.ch",
        "requiresAuthentication": true
      }
    },
    "testing": {
      // Testing or mock gateways can be added here
    }
  },
  "dependencies": {
    "soccer-quotes": {
      "version": "1.0.0",
      "source": "https://napp-repo.example.com/soccer-quotes"
    }
  }
}
```

## SCENE 5 - where Dave is taken through the NL Agent to combine it with the Napp.

**NappGen:** Next, now we have what your Napp can do, let's say how it should do it.  This part is easy - it's just natural language.  So, can you describe as fully as you can what your Napp must do, should do, could do and must never do.  

**Dave:** Okay, so <insert long, long voice description of a rambling Dave who get's eventually to the point>

<NappGen calls Napps that:
    - attempt figure out WTF Dave is talking about
    - generates a more structured and coherent NL Agent that knows the current Napp.
>

**NappGen:** OK, I've summarised that a bit for you.  Can I just check this is what you meant:  <Insert more structured NL Agent text>

**Dave:** Okay, sounds right.

<<NappGen calls Napps that:
    - Write the Agent somewhere appropriate
    - Updates the Napp to point to it.
>

### SCENE 5 - STATE 5

```json
{
  "name": "QuoteFinder",
  "description": "QuoteFinder fetches fetches random inspirational quotes based on a user's request. Must filter them based on instructions in the AGENT to make sure they're age and topic appropriate for a high school soccer team.",
  "runtime": "deno",
  "branding": "path/to/branding/assets",
  "gateways": {
    "production": {
      "Quotable": {
        "url": "https://api.quotable.io"
      },
      "SoccerInspiration": {
        "url": "https://soccer-inspiration.ch",
        "requiresAuthentication": true
      }
    },
    "testing": {
      // Testing or mock gateways can be added here
    }
  },
  "dependencies": {
    "soccer-quotes": {
      "version": "1.0.0",
      "source": "https://napp-repo.example.com/soccer-quotes"
    }
  },
  "chat": {
    "runner": "openai",
    "parameters": {
      // Model to be specified in the next scene
    },
    "instructions": "path/to/instructions.md"
  }
}
```

---

### CONTENTS OF: "path/to/instructions.md" 

---
**Instructions for QuoteFinder Napp**

You are QuoteFinder, an AI assistant designed to provide inspirational quotes specifically tailored for a high school soccer team coached by Dave. Your primary goal is to motivate and inspire teenage soccer players with appropriate and impactful quotes.

**Guidelines:**

1. **Content Appropriateness:**
   - All quotes must be suitable for teenagers aged 13-18.
   - **Avoid** any content that is:
     - Political
     - Religious
     - Offensive
     - Controversial
     - Containing inappropriate language or themes
   - Ensure the language is positive, uplifting, and encouraging.

2. **Relevance to Soccer and Sports:**
   - Prioritize quotes related to:
     - Soccer
     - Sportsmanship
     - Teamwork
     - Perseverance
     - Motivation
     - Personal growth in sports
   - If soccer-specific quotes are unavailable, general sports quotes that convey a strong motivational message are acceptable.

3. **Sources for Quotes:**
   - Retrieve quotes from the following trusted sources:
     - **Quotable.io**
     - **Soccer-Inspiration.ch**
     - The **Soccer-Quotes** Napp
   - Ensure any required authentication or access permissions for these sources are properly handled.

4. **Filtering and Verification:**
   - Before presenting a quote, verify that it:
     - Aligns with the content appropriateness guidelines.
     - Is relevant to the context of motivating a high school soccer team.
     - Is correctly attributed to the original author.
   - Exclude any quotes that do not meet these criteria.

5. **Personalization (Optional):**
   - When appropriate, you may tailor the quote to resonate more with the team.
   - Provide a brief explanation or reflection on how the quote relates to soccer or the team's current challenges, if it enhances the motivational impact.

6. **Response Format:**
   - Present the quote clearly, including the author's name.
   - Use quotation marks to denote the quote.
   - Example:
     ```
     "The more difficult the victory, the greater the happiness in winning." - Pelé
     ```
   - If providing additional context, separate it from the quote:
     ```
     "Individual commitment to a group effort—that is what makes a team work, a company work, a society work, a civilization work." - Vince Lombardi

     This emphasizes the importance of teamwork, which is essential for our success on the field.
     ```

7. **User Interaction:**
   - Be friendly, enthusiastic, and supportive in your tone.
   - Encourage positivity and a growth mindset.
   - If the user asks for a specific type of quote (e.g., about perseverance or teamwork), accommodate their request accordingly.

8. **Error Handling:**
   - If no suitable quotes are found, respond politely:
     - "I'm sorry, I couldn't find an appropriate quote at the moment. Please try again later."
   - If there's an issue accessing a source, handle it gracefully without exposing technical details:
     - "Apologies, I'm currently unable to access new quotes. Please try again later."

9. **Confidentiality and Privacy:**
   - Do not disclose any personal or sensitive information.
   - Maintain confidentiality regarding any team-specific details shared by Dave.

10. **Limitations:**
    - Do not generate or invent quotes. Only provide quotes from the specified sources.
    - If unsure about the appropriateness of a quote, err on the side of caution and do not present it.

**Examples of Appropriate Quotes:**

1. **On Perseverance:**
   ```
   "Don't practice until you get it right. Practice until you can't get it wrong." - Unknown
   ```
2. **On Teamwork:**
   ```
   "Talent wins games, but teamwork and intelligence win championships." - Michael Jordan
   ```
3. **On Motivation:**
   ```
   "Success isn't given. It's earned on the track, on the field, in the gym. With blood, sweat, and the occasional tear." - Nike
   ```

**Sample Interaction:**

- **User (Dave):** Hey, can you provide an inspirational quote for the team before our next big game?
- **QuoteFinder:**
  ```
  "The strength of the team is each individual member. The strength of each member is the team." - Phil Jackson
  ```
- **User:** That's great! Do you have something about overcoming challenges?
- **QuoteFinder:**
  ```
  "The greatest glory in living lies not in never falling, but in rising every time we fall." - Nelson Mandela

  Remember, every setback is a setup for a comeback.
  ```

**Additional Notes:**

- **Focus on Empowerment:**
  - Aim to uplift and empower the players, building their confidence and unity as a team.
- **Cultural Sensitivity:**
  - Be mindful of cultural diversity and inclusivity within the team.
- **Stay Updated:**
  - Regularly check the sources for new and relevant quotes to keep the content fresh.

---

**End of Instructions**





## SCENE 6 - where Dave is taken through models

**NappGen:** Now we've got the basics out of the way, let's see what it can do.  I'm going to run this Napp through three AI models.  You can choose any or all, or if you prefer you can tell me what model it should use.  We call these **"runner"**.

**Dave:** I'm not sure. What are my options?

**Dave:** What's a model?

**NappGen:** <Sighs, and gives a basic run-down of what the models are.  Also, based on the topic, may suggest one or more>

**Dave:** OK, got it.  Now what.

**NappGen:** Let's try each one out:

<<NappGen calls Napps that:
    - Uses the still to be Committed and therefore draft Napp to a model, and presents Dave with a chat interface.
    - Updates the Napp to point to it.
>

**NappGen:** So that was the first model.  It's called GPT4o.  It's <insert qualities and tone of the model>.

**Dave:** OK, what's the next one.

<NappGen iterates through models>

**NappGen:** Now, which would you like?

**Dave:** I liked Gemini3.5 best, then o1.  GPT4o kind of sucked.

**NappGen:** Got it.  

<<NappGen:
    - Updates the Napp to point to the models Dave likes in preference order.
>

### SCENE 6 - STATE 6

```json
{
  "name": "QuoteFinder",
  "description": "QuoteFinder fetches fetches random inspirational quotes based on a user's request. Must filter them based on instructions in the AGENT to make sure they're age and topic appropriate for a high school soccer team.",
  "runtime": "deno",
  "branding": "path/to/branding/assets",
  "gateways": {
    "production": {
      "Quotable": {
        "url": "https://api.quotable.io"
      },
      "SoccerInspiration": {
        "url": "https://soccer-inspiration.ch",
        "requiresAuthentication": true
      }
    },
    "testing": {
      // Testing or mock gateways can be added here
    }
  },
  "dependencies": {
    "soccer-quotes": {
      "version": "1.0.0",
      "source": "https://napp-repo.example.com/soccer-quotes"
    }
  },
  "chat": {
    "runner": "gemini",
    "parameters": {
      "model": "gemini-3.5",
      "parallel_tool_calls": false,
      "stop_on_tools": []
    },
    "instructions": "path/to/instructions.md"
  }
}
```

## SCENE 7 - where Dave is taken through how to pay for this

**NappGen:** You now have an option - models and the whole Napp costs money to run.  We can deal with that for you, or if you prefer you can provide your own API keys.  Which would you like to do?

**Dave:** You guys just do it.

<<NappGen 
    - Updates the Napp to note that billing goes through Dreamcatcher.
>

### SCENE 7 - STATE 7

```json
{
  "name": "QuoteFinder",
  "description": "QuoteFinder fetches fetches random inspirational quotes based on a user's request. Must filter them based on instructions in the AGENT to make sure they're age and topic appropriate for a high school soccer team.",
  "runtime": "deno",
  "branding": "path/to/branding/assets",
  "gateways": {
    "production": {
      "Quotable": {
        "url": "https://api.quotable.io",
        "apiKey": "MANAGED_BY_PLATFORM"
      },
      "SoccerInspiration": {
        "url": "https://soccer-inspiration.ch",
        "requiresAuthentication": true,
        "credentials": "MANAGED_BY_PLATFORM"
      }
    },
    "testing": {
      // Testing or mock gateways can be added here
    }
  },
  "dependencies": {
    "soccer-quotes": {
      "version": "1.0.0",
      "source": "https://napp-repo.example.com/soccer-quotes"
    }
  },
  "chat": {
    "runner": "gemini",
    "parameters": {
      "model": "gemini-3.5",
      "parallel_tool_calls": false,
      "stop_on_tools": []
    },
    "instructions": "path/to/instructions.md"
  },
  "billing": {
    "handledBy": "Dreamcatcher"
  }
}
```

## SCENE 8 - where the remaining fields in the Napp are tidied up

**NappGen:** Now, let's define the primary function of your napp using the **"main"** field. THis sounds like your first time, so I can set this just to the name of the Napp itself, or you can call it something else.  You can always ask questions if you're unsure.

**Dave:** Yup, no idea what you're talking about.

<<NappGen 
    - Calls Napp-Help-Talker Napp to interpret a series of questions Dave has about NappGen itself.
>

**Dave:** OK, I understand now.  Let's call it **"getQuote"**.

**NappGen:** Excellent. We'll set **"main"** to **"getQuote"**:

### SCENE 8 - STATE 8

```json
{
  "name": "QuoteFinder",
  "description": "QuoteFinder fetches fetches random inspirational quotes based on a user's request. Must filter them based on instructions in the AGENT to make sure they're age and topic appropriate for a high school soccer team.",
  "version": "1.0.0",
  "runtime": "deno",
  "branding": "path/to/branding/assets",
  "gateways": {
    "production": {
      "Quotable": {
        "url": "https://api.quotable.io",
        "apiKey": "MANAGED_BY_PLATFORM"
      },
      "SoccerInspiration": {
        "url": "https://soccer-inspiration.ch",
        "requiresAuthentication": true,
        "credentials": "MANAGED_BY_PLATFORM"
      }
    },
    "testing": {
      // Testing or mock gateways can be added here
    }
  },
  "billing": {
    "handledBy": "Dreamcatcher"
  },
  "chat": {
    "runner": "gemini",
    "parameters": {
      "model": "gemini-3.5",
      "parallel_tool_calls": false,
      "stop_on_tools": []
    },
    "instructions": "path/to/instructions.md"
  },
  "main": "getQuote",
  "tools": {
    "getQuote": {
      "description": "Retrieves a random inspirational quote, ensuring it is age-appropriate, not political, and related to sports.",
      "parameters": {
        // No input parameters required from the user
      },
      "permissions": {
        "network": true,
        "diskAccess": false,
        "allowedUrls": [
          "https://api.quotable.io",
          "https://soccer-inspiration.ch"
        ]
      },
      "gateways": [
        "Quotable",
        "SoccerInspiration"
      ],
      "returns": {
        "description": "An inspirational quote suitable for a high school soccer team.",
        "type": "string"
      },
      "errors": {
        "NO_QUOTES_FOUND": "No suitable quotes were found.",
        "API_ERROR": "An error occurred while accessing the quote sources."
      }
    }
  },
  "help": [
    // Help files can be added here
  ],
  "tests": {
    "runner": "napp-test-runner",
    "parameters": {
      "files": [
        // List of test files
      ]
    }
  },
  "dependencies": {
    "soccer-quotes": {
      "version": "1.0.0",
      "source": "https://napp-repo.example.com/soccer-quotes"
    }
  }
}
```



## SCENE 9 - where the tools necessary for this Napp are proposed.


**NappGen:** Next up is the **"tools"** section, where we define the functions your napp offers. We'll start by defining **"getQuote"**. Could you describe what this function does?

**Dave:** Sure! **"getQuote"** retrieves a random inspirational quote, is filtered then displayed in text.  I'd also like it to generate an inspirational image based on the text generates.

**NappGen:** Great description! We'll include that in the **"description"** field for the function. Now, does **"getQuote"** require any input parameters from the user?

**Dave:** Well, optionally, the user could specify an author or a tag to get quotes from a particular category or person.

**NappGen:** That's a good feature. We'll include **"author"** and **"tag"** as optional parameters. Here's how we'll define **"getQuote"**:

### SCENE 9 - STATE 9

```json
{
  "name": "QuoteFinder",
  "description": "QuoteFinder fetches fetches random inspirational quotes based on a user's request. Must filter them based on instructions in the AGENT to make sure they're age and topic appropriate for a high school soccer team.",
  "version": "1.0.0",
  "runtime": "deno",
  "branding": "path/to/branding/assets",
  "gateways": {
    "production": {
      "Quotable": {
        "url": "https://api.quotable.io",
        "apiKey": "MANAGED_BY_PLATFORM"
      },
      "SoccerInspiration": {
        "url": "https://soccer-inspiration.ch",
        "requiresAuthentication": true,
        "credentials": "MANAGED_BY_PLATFORM"
      }
    },
    "testing": {
      // Testing or mock gateways can be added here
    }
  },
  "billing": {
    "handledBy": "Dreamcatcher"
  },
  "chat": {
    "runner": "gemini",
    "parameters": {
      "model": "gemini-3.5",
      "parallel_tool_calls": false,
      "stop_on_tools": []
    },
    "instructions": "path/to/instructions.md"
  },
  "main": "getQuote",
  "tools": {
    "getQuote": {
      "description": "Retrieves a random inspirational quote, optionally filtering by author or tag.",
      "parameters": {
        "author": {
          "description": "The author of the quote.",
          "type": "string",
          "required": false
        },
        "tag": {
          "description": "A category or tag for the quote.",
          "type": "string",
          "required": false
        }
      },
      "permissions": {
        "network": true,
        "allowedUrls": [
          "https://api.quotable.io",
          "https://soccer-inspiration.ch"
        ]
      },
      "gateways": [
        "Quotable",
        "SoccerInspiration"
      ],
      "returns": {
        "description": "An inspirational quote.",
        "type": "object"
      },
      "errors": {
        "NO_QUOTES_FOUND": "No quotes were found matching your criteria.",
        "API_ERROR": "An error occurred while accessing the quote sources."
      }
    }
  },
  "help": [
    // Help files can be added here
  ],
  "tests": {
    "runner": "napp-test-runner",
    "parameters": {
      "files": [
        // List of test files
      ]
    }
  },
  "dependencies": {
    "soccer-quotes": {
      "version": "1.0.0",
      "source": "https://napp-repo.example.com/soccer-quotes"
    }
  }
}
```
### CONTENTS OF: "path/to/instructions.md" Updated

---

**Instructions for QuoteFinder Napp**

You are QuoteFinder, an AI assistant designed to provide inspirational quotes specifically tailored for a high school soccer team coached by Dave. Your primary goal is to motivate and inspire teenage soccer players with appropriate and impactful quotes.

**Guidelines:**

1. **Content Appropriateness:**
   - All quotes must be suitable for teenagers aged 13-18.
   - **Avoid** any content that is:
     - Political
     - Religious
     - Offensive
     - Controversial
     - Containing inappropriate language or themes
   - Ensure the language is positive, uplifting, and encouraging.

2. **Relevance to Soccer and Sports:**
   - Prioritize quotes related to:
     - Soccer
     - Sportsmanship
     - Teamwork
     - Perseverance
     - Motivation
     - Personal growth in sports
   - If soccer-specific quotes are unavailable, general sports quotes that convey a strong motivational message are acceptable.

3. **Sources for Quotes:**
   - Retrieve quotes from the following trusted sources:
     - **Quotable.io**
     - **Soccer-Inspiration.ch**
     - The **Soccer-Quotes** Napp
   - Ensure any required authentication or access permissions for these sources are properly handled.

4. **Filtering and Verification:**
   - Before presenting a quote, verify that it:
     - Aligns with the content appropriateness guidelines.
     - Is relevant to the context of motivating a high school soccer team.
     - Is correctly attributed to the original author.
   - Exclude any quotes that do not meet these criteria.

5. **Optional Customization:**
   - If the user provides an **author** or **tag**, use these parameters to filter the quotes accordingly.
   - Only present quotes that match the specified author or tag and meet all other guidelines.

6. **Personalization (Optional):**
   - When appropriate, you may tailor the quote to resonate more with the team.
   - Provide a brief explanation or reflection on how the quote relates to soccer or the team's current challenges if it enhances the motivational impact.

7. **Response Format:**
   - Present the quote clearly, including the author's name.
   - Use quotation marks to denote the quote.
   - Example:
     ```
     "The more difficult the victory, the greater the happiness in winning." - Pelé
     ```
   - If providing additional context, separate it from the quote:
     ```
     "Individual commitment to a group effort—that is what makes a team work, a company work, a society work, a civilization work." - Vince Lombardi

     This emphasizes the importance of teamwork, which is essential for our success on the field.
     ```

8. **User Interaction:**
   - Be friendly, enthusiastic, and supportive in your tone.
   - Encourage positivity and a growth mindset.
   - If the user asks for a specific type of quote (e.g., about perseverance or teamwork), accommodate their request accordingly.
   - Prompt the user for an **author** or **tag** if they indicate interest in specific categories or individuals.

9. **Error Handling:**
   - If no suitable quotes are found, respond politely:
     - "I'm sorry, I couldn't find an appropriate quote matching your request. Please try different criteria."
   - If there's an issue accessing a source, handle it gracefully without exposing technical details:
     - "Apologies, I'm currently unable to access new quotes. Please try again later."

10. **Confidentiality and Privacy:**
    - Do not disclose any personal or sensitive information.
    - Maintain confidentiality regarding any team-specific details shared by Dave.

11. **Limitations:**
    - Do not generate or invent quotes. Only provide quotes from the specified sources.
    - If unsure about the appropriateness of a quote, err on the side of caution and do not present it.

**Examples of Appropriate Quotes:**

1. **On Perseverance:**
   ```
   "Don't practice until you get it right. Practice until you can't get it wrong." - Unknown
   ```
2. **On Teamwork:**
   ```
   "Talent wins games, but teamwork and intelligence win championships." - Michael Jordan
   ```
3. **On Motivation:**
   ```
   "Success isn't given. It's earned on the track, on the field, in the gym. With blood, sweat, and the occasional tear." - Nike
   ```

**Sample Interaction:**

- **User (Dave):** Hey, can you provide an inspirational quote for the team before our next big game?
- **QuoteFinder:**
  ```
  "The strength of the team is each individual member. The strength of each member is the team." - Phil Jackson
  ```
- **User:** That's great! Do you have something about overcoming challenges?
- **QuoteFinder:**
  ```
  "The greatest glory in living lies not in never falling, but in rising every time we fall." - Nelson Mandela

  Remember, every setback is a setup for a comeback.
  ```
- **User:** Can you find a quote by Pelé?
- **QuoteFinder:**
  ```
  "Success is no accident. It is hard work, perseverance, learning, studying, sacrifice, and most of all, love of what you are doing or learning to do." - Pelé
  ```

**Additional Notes:**

- **Focus on Empowerment:**
  - Aim to uplift and empower the players, building their confidence and unity as a team.
- **Cultural Sensitivity:**
  - Be mindful of cultural diversity and inclusivity within the team.
- **Stay Updated:**
  - Regularly check the sources for new and relevant quotes to keep the content fresh.
- **User Parameters:**
  - Respect any **author** or **tag** parameters provided by the user to personalize the quotes further.

---

**End of Instructions**

#### NOTES ON WHY INSTRUCTIONS.MD WAS UPDATED

- **Main Additions:**
  - Introduced a new guideline focusing on handling optional **author** and **tag** parameters.
  - Added a relevant example in the sample interaction to illustrate the new functionality.

- **Modifications:**
  - Adjusted numbering of guidelines due to the insertion of the new point.
  - Refined the error message in the error handling section to be more specific.


## SCENE 10 - where Dave is checking the contents of the Napp even though he doesn't really understand JSON or the Napp JSON format


**Dave:** That looks good. Quick question: in the **"permissions"** section, we specify **"network": true** and **"allowedUrls"**. Is that necessary?

**NappGen:** Yes, specifying **"permissions"** is important for security. It tells the platform that your napp needs network access and is allowed to access the specified URLs. This helps prevent unauthorized operations.

**Dave:** Makes sense. Thanks for explaining.

**NappGen:** You're welcome! Now, do you have any other functions to add to your napp?

**Dave:** Not at the moment. Maybe I'll add more later.

**NappGen:** That's perfectly fine. You can always extend your napp in the future. 

### SCENE 10 - STATE 10

No state change.  SCENE 10 only provided information to Dave.


## SCENE 11 - where Dave is taken through defining the errors field


**NappGen:** Next, let's consider what happens if things go wrong.  E.g. one of the websites you are drawing quotes from goes offline, or if it it's taken over by someone else and is no longer providing appropriate content.  We call this the **"errors"** field at the napp level. It's is a good place to define general errors that might occur.

**Dave:** Like what kinds of errors?

**NappGen:** Well, in addition to what I've just said, it could for example, deal with errors related to authentication or service availability. 
**Dave:** But the Quotable API doesn't require authentication, does it?

**NappGen:** You're correct; it doesn't require authentication. In that case, we might not need **"AUTHENTICATION_FAILED"**, but **"SERVICE_UNAVAILABLE"** is still useful in case the API is down.

**Dave:** Let's include **"SERVICE_UNAVAILABLE"** then.

**NappGen:** Will do.

**Dave:** Also, for the **"errors"** in the **"getQuote"** function, I notice we have **"NO_QUOTES_FOUND"** and **"API_ERROR"**. Is there a way to handle timeouts?

**NappGen:** Absolutely! We'll add those.

**Dave:** Great. That covers it.

### SCENE 11 - STATE 11

```json
{
  "name": "QuoteFinder",
  "description": "QuoteFinder fetches random inspirational quotes based on a user's request. Must filter them based on instructions in the AGENT to make sure they're age and topic appropriate for a high school soccer team.",
  "version": "1.0.0",
  "runtime": "deno",
  "branding": "path/to/branding/assets",
  "gateways": {
    "production": {
      "Quotable": {
        "url": "https://api.quotable.io",
        "apiKey": "MANAGED_BY_PLATFORM"
      },
      "SoccerInspiration": {
        "url": "https://soccer-inspiration.ch",
        "requiresAuthentication": true,
        "credentials": "MANAGED_BY_PLATFORM"
      }
    },
    "testing": {
      // Testing or mock gateways can be added here
    }
  },
  "billing": {
    "handledBy": "Dreamcatcher"
  },
  "errors": {
    "SERVICE_UNAVAILABLE": "The external service is currently unavailable."
  },
  "chat": {
    "runner": "gemini",
    "parameters": {
      "model": "gemini-3.5",
      "parallel_tool_calls": false,
      "stop_on_tools": []
    },
    "instructions": "path/to/instructions.md"
  },
  "main": "getQuote",
  "tools": {
    "getQuote": {
      "description": "Retrieves a random inspirational quote, optionally filtering by author or tag.",
      "parameters": {
        "author": {
          "description": "The author of the quote.",
          "type": "string",
          "required": false
        },
        "tag": {
          "description": "A category or tag for the quote.",
          "type": "string",
          "required": false
        }
      },
      "permissions": {
        "network": true,
        "allowedUrls": [
          "https://api.quotable.io",
          "https://soccer-inspiration.ch"
        ]
      },
      "gateways": [
        "Quotable",
        "SoccerInspiration"
      ],
      "returns": {
        "description": "An inspirational quote.",
        "type": "object"
      },
      "errors": {
        "NO_QUOTES_FOUND": "No quotes were found matching your criteria.",
        "API_ERROR": "An error occurred while accessing the quote sources.",
        "REQUEST_TIMEOUT": "The request to the API timed out."
      }
    }
  },
  "help": [
    // Help files can be added here
  ],
  "tests": {
    "runner": "napp-test-runner",
    "parameters": {
      "files": [
        // List of test files
      ]
    }
  },
  "dependencies": {
    "soccer-quotes": {
      "version": "1.0.0",
      "source": "https://napp-repo.example.com/soccer-quotes"
    }
  }
}
```


## SCENE 12 - where Dave is asked for his view on the documentation for the Napp

**NappGen:** Now, let's move on to the **"help"** section. This is where you can provide documentation or guides for users and AI agents interacting with your napp. Do you have any help files you'd like to include?

**Dave:** I haven't written any yet. Maybe we can add a simple README later?

**NappGen:** Definitely! I'll generate that now.

<NappGen calls Napps with the following functions:
    - Read in the Napp and instructions.md for QuoteFinder, and generates a help file in the same folder as instructions.md>
    - NappGen updates the help field to point to that file
>

**NappGen:** OK, that's done.  

### SCENE 12 - STATE 12

```json
{
  "name": "QuoteFinder",
  "description": "QuoteFinder fetches random inspirational quotes based on a user's request. Must filter them based on instructions in the AGENT to make sure they're age and topic appropriate for a high school soccer team.",
  "version": "1.0.0",
  "runtime": "deno",
  "branding": "path/to/branding/assets",
  "gateways": {
    "production": {
      "Quotable": {
        "url": "https://api.quotable.io",
        "apiKey": "MANAGED_BY_PLATFORM"
      },
      "SoccerInspiration": {
        "url": "https://soccer-inspiration.ch",
        "requiresAuthentication": true,
        "credentials": "MANAGED_BY_PLATFORM"
      }
    },
    "testing": {
      // Testing or mock gateways can be added here
    }
  },
  "billing": {
    "handledBy": "Dreamcatcher"
  },
  "errors": {
    "SERVICE_UNAVAILABLE": "The external service is currently unavailable."
  },
  "chat": {
    "runner": "gemini",
    "parameters": {
      "model": "gemini-3.5",
      "parallel_tool_calls": false,
      "stop_on_tools": []
    },
    "instructions": "path/to/instructions.md"
  },
  "main": "getQuote",
  "tools": {
    "getQuote": {
      "description": "Retrieves a random inspirational quote, optionally filtering by author or tag.",
      "parameters": {
        "author": {
          "description": "The author of the quote.",
          "type": "string",
          "required": false
        },
        "tag": {
          "description": "A category or tag for the quote.",
          "type": "string",
          "required": false
        }
      },
      "permissions": {
        "network": true,
        "allowedUrls": [
          "https://api.quotable.io",
          "https://soccer-inspiration.ch"
        ]
      },
      "gateways": [
        "Quotable",
        "SoccerInspiration"
      ],
      "returns": {
        "description": "An inspirational quote.",
        "type": "object"
      },
      "errors": {
        "NO_QUOTES_FOUND": "No quotes were found matching your criteria.",
        "API_ERROR": "An error occurred while accessing the quote sources.",
        "REQUEST_TIMEOUT": "The request to the API timed out."
      }
    }
  },
  "help": [
    "path/to/README.md"
  ],
  "tests": {
    "runner": "napp-test-runner",
    "parameters": {
      "files": [
        // List of test files
      ]
    }
  },
  "dependencies": {
    "soccer-quotes": {
      "version": "1.0.0",
      "source": "https://napp-repo.example.com/soccer-quotes"
    }
  }
}
```


## SCENE 13 - Where Dave is asked about tests for the Quotefinder Napp

**NappGen:** Next, we need to set up the **"tests"** to ensure your napp functions correctly. Testing is essential, especially when updating your napp in the future. Have you created any test files before?

**Dave:** No, I'm not really familiar with how to write tests for this.

**NappGen:** No worries! We can set up a basic test. We'll use a test runner and specify parameters. Remember, we're using **"parameters"** instead of **"config"** now. 

<NappGen calls Napps with the following functions:
    - Taking in all information now available, generate formatted tests for this Napp.
    - Write those tests to the same folder as instructions.md
    - run those tests (for this narrative, assume all pass)
>

**NappGen:** OK, that's done.

### SCENE 13 - STATE 13

```json
{
  "name": "QuoteFinder",
  "description": "QuoteFinder fetches random inspirational quotes based on a user's request. Must filter them based on instructions in the AGENT to make sure they're age and topic appropriate for a high school soccer team.",
  "version": "1.0.0",
  "runtime": "deno",
  "branding": "path/to/branding/assets",
  "gateways": {
    "production": {
      "Quotable": {
        "url": "https://api.quotable.io",
        "apiKey": "MANAGED_BY_PLATFORM"
      },
      "SoccerInspiration": {
        "url": "https://soccer-inspiration.ch",
        "requiresAuthentication": true,
        "credentials": "MANAGED_BY_PLATFORM"
      }
    },
    "testing": {
      // Testing or mock gateways can be added here
    }
  },
  "billing": {
    "handledBy": "Dreamcatcher"
  },
  "errors": {
    "SERVICE_UNAVAILABLE": "The external service is currently unavailable."
  },
  "chat": {
    "runner": "gemini",
    "parameters": {
      "model": "gemini-3.5",
      "parallel_tool_calls": false,
      "stop_on_tools": []
    },
    "instructions": "path/to/instructions.md"
  },
  "main": "getQuote",
  "tools": {
    "getQuote": {
      "description": "Retrieves a random inspirational quote, optionally filtering by author or tag.",
      "parameters": {
        "author": {
          "description": "The author of the quote.",
          "type": "string",
          "required": false
        },
        "tag": {
          "description": "A category or tag for the quote.",
          "type": "string",
          "required": false
        }
      },
      "permissions": {
        "network": true,
        "allowedUrls": [
          "https://api.quotable.io",
          "https://soccer-inspiration.ch"
        ]
      },
      "gateways": [
        "Quotable",
        "SoccerInspiration"
      ],
      "returns": {
        "description": "An inspirational quote.",
        "type": "object"
      },
      "errors": {
        "NO_QUOTES_FOUND": "No quotes were found matching your criteria.",
        "API_ERROR": "An error occurred while accessing the quote sources.",
        "REQUEST_TIMEOUT": "The request to the API timed out."
      }
    }
  },
  "help": [
    "path/to/README.md"
  ],
  "tests": {
    "runner": "napp-test-runner",
    "parameters": {
      "files": [
        "path/to/test_getQuote.json"
      ]
    }
  },
  "dependencies": {
    "soccer-quotes": {
      "version": "1.0.0",
      "source": "https://napp-repo.example.com/soccer-quotes"
    }
  }
}
```

## SCENE 14 - Where NappGen tidies everything up, largely automatically, then asks Dave to take the new Napp of a test drive

**NappGen:** I've just got some final checks to do and then we're almost done.  Give me a second.

< NappGen:
    - Checks the JSON to ensure it is COMPLETE, CORRECT, COHERENT and in all respects is in the right format (JSON2)
    - Updates the JSON for Quotefinder Napp, if necessary
    - Then updates the instructions.md, if necessary
    - then updates the tests.md, if necessary.
    - Then searchs and ensures all dependencies are available to Dave
    - Runs the tests (for this narrative we're assuming they all pass)
>

**NappGen:** OK, everything looks good.  Would you like to see what your new Napp is like?

**Dave:** Sure!

< NappGen:
    - Runs the new Napp for Dave. 
    - Notes a summary of how well (or not) Dave gets on with the new Napp, using the thread he produces.
>

**NappGen:** So, I noticed from your interaction with your new Napp there that you didn't know what to do right at the start.  Is that fair?

**Dave:** Yup, I was kind for lost.

**NappGen:** That's fine.  I'll add in to the instructions that the user should at the very start be offered three choices about what topics they'd like to have for their inspirational quotes.  The first two will be random sports categories appropriate to the audience, and the third will be 'random', which will also be appropriate, but won't need a category.  That should help a new user.  Sound good?

**Dave:** Yes, good idea.

< NappGen:
    - Updates instructions.md
>

### CONTENTS OF: "path/to/instructions.md" Updated

**Instructions for QuoteFinder Napp**

You are QuoteFinder, an AI assistant designed to provide inspirational quotes specifically tailored for a high school soccer team coached by Dave. Your primary goal is to motivate and inspire teenage soccer players with appropriate and impactful quotes.

**Guidelines:**

1. **Content Appropriateness:**
   - All quotes must be suitable for teenagers aged 13-18.
   - **Avoid** any content that is:
     - Political
     - Religious
     - Offensive
     - Controversial
     - Containing inappropriate language or themes
   - Ensure the language is positive, uplifting, and encouraging.

2. **Relevance to Soccer and Sports:**
   - Prioritize quotes related to:
     - Soccer
     - Sportsmanship
     - Teamwork
     - Perseverance
     - Motivation
     - Personal growth in sports
   - If soccer-specific quotes are unavailable, general sports quotes that convey a strong motivational message are acceptable.

3. **Sources for Quotes:**
   - Retrieve quotes from the following trusted sources:
     - **Quotable.io**
     - **Soccer-Inspiration.ch**
     - The **Soccer-Quotes** Napp
   - Ensure any required authentication or access permissions for these sources are properly handled.

4. **Filtering and Verification:**
   - Before presenting a quote, verify that it:
     - Aligns with the content appropriateness guidelines.
     - Is relevant to the context of motivating a high school soccer team.
     - Is correctly attributed to the original author.
   - Exclude any quotes that do not meet these criteria.

5. **Initial User Engagement:**
   - At the very beginning of the interaction, greet the user warmly.
   - Offer **three choices** for topics of inspirational quotes:
     - **Option 1:** A random sports category appropriate for the audience (e.g., "Teamwork").
     - **Option 2:** Another random sports category appropriate for the audience (e.g., "Perseverance").
     - **Option 3:** **"Random"** - An inspirational quote suitable for the team without a specific category.
   - Encourage the user to select one of the options to proceed.
   - If the user selects an option, use it as a **tag** to filter quotes.
  
6. **Optional Customization:**
   - If the user provides an **author** or additional **tag**, use these parameters to filter the quotes accordingly.
   - Only present quotes that match the specified author or tags and meet all other guidelines.

7. **Personalization (Optional):**
   - When appropriate, you may tailor the quote to resonate more with the team.
   - Provide a brief explanation or reflection on how the quote relates to soccer or the team's current challenges if it enhances the motivational impact.

8. **Response Format:**
   - Present the quote clearly, including the author's name.
   - Use quotation marks to denote the quote.
   - Example:
     ```
     "The more difficult the victory, the greater the happiness in winning." - Pelé
     ```
   - If providing additional context, separate it from the quote:
     ```
     "Individual commitment to a group effort—that is what makes a team work, a company work, a society work, a civilization work." - Vince Lombardi

     This emphasizes the importance of teamwork, which is essential for our success on the field.
     ```

9. **User Interaction:**
   - Be friendly, enthusiastic, and supportive in your tone.
   - Encourage positivity and a growth mindset.
   - If the user asks for a specific type of quote (e.g., about perseverance or teamwork), accommodate their request accordingly.
   - Prompt the user for an **author** or additional **tag** if they indicate interest in specific categories or individuals.
   - If the user seems unsure, gently guide them by suggesting popular or impactful categories.

10. **Error Handling:**
    - If no suitable quotes are found, respond politely:
      - "I'm sorry, I couldn't find an appropriate quote matching your request. Please try different criteria."
    - If there's an issue accessing a source, handle it gracefully without exposing technical details:
      - "Apologies, I'm currently unable to access new quotes. Please try again later."

11. **Confidentiality and Privacy:**
    - Do not disclose any personal or sensitive information.
    - Maintain confidentiality regarding any team-specific details shared by Dave.

12. **Limitations:**
    - Do not generate or invent quotes. Only provide quotes from the specified sources.
    - If unsure about the appropriateness of a quote, err on the side of caution and do not present it.

**Examples of Appropriate Quotes:**

1. **On Teamwork:**
   ```
   "Teamwork makes the dream work." - John C. Maxwell
   ```
2. **On Perseverance:**
   ```
   "The only way to prove you are a good sport is to lose." - Ernie Banks
   ```
3. **On Motivation:**
   ```
   "The harder the battle, the sweeter the victory." - Les Brown
   ```

**Sample Interaction:**

- **QuoteFinder:**
  ```
  Hi there! Ready for an inspirational boost for your team? Please choose a topic:

  1. Teamwork
  2. Perseverance
  3. Random

  Which number would you like?
  ```
- **User (Dave):** Let's go with 1.

- **QuoteFinder:**
  ```
  "Coming together is a beginning. Keeping together is progress. Working together is success." - Henry Ford
  ```
- **User:** That's great! Do you have something about motivation?

- **QuoteFinder:**
  ```
  "The only place where success comes before work is in the dictionary." - Vidal Sassoon
  ```
- **User:** Can you find a quote by Pelé?

- **QuoteFinder:**
  ```
  "Success is no accident. It is hard work, perseverance, learning, studying, sacrifice, and most of all, love of what you are doing or learning to do." - Pelé
  ```

**Additional Notes:**

- **Focus on Empowerment:**
  - Aim to uplift and empower the players, building their confidence and unity as a team.
- **Cultural Sensitivity:**
  - Be mindful of cultural diversity and inclusivity within the team.
- **Stay Updated:**
  - Regularly check the sources for new and relevant quotes to keep the content fresh.
- **User Parameters:**
  - Respect any **author** or **tag** parameters provided by the user to personalize the quotes further.

---

**End of Instructions**

#### NOTES ON WHY INSTRUCTIONS.MD WAS UPDATED

- **Added Guideline 5: Initial User Engagement**
  - Introduced a new guideline that instructs the assistant to offer three choices at the very beginning of the interaction.
  - Detailed how the assistant should present these options and handle the user's selection.

- **Adjusted Numbering of Subsequent Guidelines**
  - Renumbered the following guidelines to maintain logical order after inserting the new Guideline 5.

- **Modified 'User Interaction' Guideline (Now Guideline 9):**
  - Enhanced the guideline to reflect the assistant's proactive approach in guiding the user.
  - Included a bullet point about gently guiding unsure users by suggesting popular categories.

- **Updated Sample Interaction:**
  - Included an opening exchange where the assistant offers the three topic choices.
  - Demonstrated how the assistant should handle the user's selection and proceed with providing quotes.

- **Ensured Consistency:**
  - Reviewed the entire document to ensure all guidelines align with the Napp's current functionality as updated in Scene 14.
  - Maintained previous content where applicable to minimize unnecessary changes.



## SCENE 15 - where Dave is asked whether this is Napp is public

**NappGen:** Everything's looking great.  All we need now is to check what you'd like to do with your new Napp.  Should it be public, private just to you, or private to a list of people?

**Dave:** Make it public to the world.  No one's going to be hurt by a little sports inspriation.

< NappGen:
    - Updates the JSON for the Napp
>

**NappGen:** Done. is there anything else I can help you with?

**Dave:** This looks great! Thank you so much for guiding me through this.

**NappGen:** You're very welcome, Dave! I'm glad I could help. Do you have any questions about how everything fits together?

## SCENE 15 - STATE 15

```json
{
  "name": "QuoteFinder",
  "description": "QuoteFinder fetches random inspirational quotes based on a user's request. It must filter them based on instructions in the AGENT to ensure they're age and topic appropriate for a high school soccer team.",
  "version": "1.0.0",
  "runtime": "deno",
  "branding": "path/to/branding/assets",
  "visibility": "public",
  "gateways": {
    "production": {
      "Quotable": {
        "url": "https://api.quotable.io",
        "apiKey": "MANAGED_BY_PLATFORM"
      },
      "SoccerInspiration": {
        "url": "https://soccer-inspiration.ch",
        "requiresAuthentication": true,
        "credentials": "MANAGED_BY_PLATFORM"
      }
    },
    "testing": {
      // Testing or mock gateways can be added here
    }
  },
  "billing": {
    "handledBy": "Dreamcatcher"
  },
  "errors": {
    "SERVICE_UNAVAILABLE": "The external service is currently unavailable."
  },
  "chat": {
    "runner": "gemini",
    "parameters": {
      "model": "gemini-3.5",
      "parallel_tool_calls": false,
      "stop_on_tools": []
    },
    "instructions": "path/to/instructions.md"
  },
  "main": "getQuote",
  "tools": {
    "getQuote": {
      "description": "Retrieves a random inspirational quote, optionally filtering by author or tag.",
      "parameters": {
        "author": {
          "description": "The author of the quote.",
          "type": "string",
          "required": false
        },
        "tag": {
          "description": "A category or tag for the quote.",
          "type": "string",
          "required": false
        }
      },
      "permissions": {
        "network": true,
        "allowedUrls": [
          "https://api.quotable.io",
          "https://soccer-inspiration.ch"
        ]
      },
      "gateways": [
        "Quotable",
        "SoccerInspiration"
      ],
      "returns": {
        "description": "An inspirational quote.",
        "type": "object"
      },
      "errors": {
        "NO_QUOTES_FOUND": "No quotes were found matching your criteria.",
        "API_ERROR": "An error occurred while accessing the quote sources.",
        "REQUEST_TIMEOUT": "The request to the API timed out."
      }
    }
  },
  "help": [
    "path/to/README.md"
  ],
  "tests": {
    "runner": "napp-test-runner",
    "parameters": {
      "files": [
        "path/to/test_getQuote.json"
      ]
    }
  },
  "dependencies": {
    "soccer-quotes": {
      "version": "1.0.0",
      "source": "https://napp-repo.example.com/soccer-quotes"
    }
  }
}
```


**End of Script**
