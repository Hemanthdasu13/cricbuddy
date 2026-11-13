# CricBuddy

**A cricket companion that sits alongside a live match and tells the fan what to watch for, before it happens.**

Status: in development. A personal project by Hemanth Dasu. The source code is private; I am happy to walk through it in an interview.

## The problem

Many people would like to enjoy cricket, but without context it looks like the same thing again and again. The interest lies in details most viewers never see: this batter scores freely off pace but gets stuck against off-spin; that bowler beats left-handers by angling the ball across them. Experts carry this in their heads. Most fans do not.

## The idea

CricBuddy does the remembering for the fan. When a matchup comes up that history has something to say about, it says so in plain language:

> **Watch this over.** An off-spinner is coming on, and this batter has struggled against off-spin in the middle overs. Expect him to slow down, or to take a risk.
>
> *(An illustration of the intended output, not a computed result.)*

Then the over plays out, and the fan has a reason to watch each ball closely. The fan can also ask questions, such as "Is bringing on the leg-spinner a good idea here?", and get an answer with the evidence behind it.

## Design rules

- **Code does the maths, the model does the talking.** Every number comes from deterministic Python over the data. A language model only turns that evidence into conversation.
- **A call is a probability, not a promise.** Each one carries its sample size, and thin evidence is said to be thin.
- **Calls are checked.** Each call is logged and compared with what happened.
- **For fans, not punters.** It is an engagement and explanation product, not a betting tool.

## Where it stands

| Part | Status |
|---|---|
| Ball-by-ball data layer (37,512 deliveries from 120 internationals) | Built |
| Matchup analysis by bowler type and phase of the innings | In development |
| Live match prompts and conversation | In development |

## Why the method travels

The core question is the same one a bank or a retailer asks about customers: given what we know about this segment, how will it respond to this offer, and how sure are we? CricBuddy answers it for batters and bowlers.

## Built with

Python, REST APIs, the Claude API and agentic workflows, Vercel.

---

Hemanth Dasu · [linkedin.com/in/hemanth-dasu](https://linkedin.com/in/hemanth-dasu)
