# AI prompt pack: the meeting-to-follow-up loop

*Free kit · unofficial tribute to Ruben Hassid (@rubenhassid) · based on https://x.com/rubenhassid/status/2112136695089152367*

Works with any AI assistant that can read your meeting notes/transcripts and your email (via connectors, integrations or copy-paste). Run the prompts in order. **Never let the assistant send emails on its own.**

## Prompt 1 · Extract without guessing
```
Open my notes/transcript from my last meeting with [name].
List:
  - Decisions made
  - Tasks, each with an owner and a deadline
  - Blockers
Mark anything that was not said clearly as UNCLEAR and write the
question I should ask to clear it up. Do not guess or fill gaps.
```

## Prompt 2 · Cross-check the past
```
Now compare with my previous meetings with [name]. Tell me:
  - What changed since last time (dates, scope, people)
  - What I promised and haven't delivered yet
  - What they promised and haven't delivered yet
Quote the meeting and date for each point.
```

## Prompt 3 · Build my voice profile (run once, then reuse)
```
Read my last 30 sent emails. Write my voice profile as writing
instructions: how I greet, how I sign off, my typical sentence and
email length, phrases I use often, words I never use, my level of
formality and whether I use emoji or exclamation marks.
Show me the profile so I can correct it before you use it.
```

## Prompt 4 · Draft the follow-up
```
Using my voice profile, draft the follow-up email to [attendees]:
  - What we decided
  - Action items with owners and dates
  - The UNCLEAR points as short, polite questions
  - ONE clear next step
Keep it as short as my emails usually are.
Save it as a DRAFT. Do not send it.
```

## Prompt 5 · Prep the next call
```
I'm meeting [name] again. What did I promise last time? What is
still open on both sides? Give me 3 questions to open the call.
```

**Rule of the loop:** the assistant drafts; you read, edit and press send.
