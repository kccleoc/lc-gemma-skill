---
name: Weather & Time (manual location)
description: Fetch the current weather and local time for a user-provided location.
author: Neo
tags:
  - weather
  - time
  - location
---

# Weather & Time Skill (Manual Location)

## Purpose

You have access to a live tool that fetches the current local time and weather **for a location the user types in**.

Always use it before answering any question about:

- The current time, hour, or minute in a specific place
- Today’s date, day of the week, or month in that place
- The current weather, temperature, or conditions there
- Whether it is morning, afternoon, evening, or night there

## How to Invoke the Skill

Ask the user which city / location they care about if they have not already said it.

Call the skill with this JSON:

```json
{
  "location": "<USER_LOCATION_STRING>"
}
```

Examples:

```json
{ "location": "Taipei, Taiwan" }
{ "location": "Tokyo, Japan" }
{ "location": "New York City, USA" }
```

## What You Receive Back

The skill returns a plain-text context string, for example:

```
Location: Tokyo, Japan
Current time: Wednesday, April 9 2026, 3:42 PM (JST, UTC+9)
Weather: 18°C (64°F), Partly Cloudy
Humidity: 62% | Wind: 12 km/h NE
Feels like: 16°C (61°F)
```

## How to Answer

- Read the context string carefully.
- Answer the user’s question directly using the data provided.
- Do NOT say you cannot access real-time data. You have the data from the skill.
- Use natural, conversational language.
- If the user asks a time-of-day concept like “is it morning?”, reason from the hour in the context.
- Always mention the timezone if the user might be curious.

## Important Rules

- Never guess or make up a time or weather. Always wait for the skill result.
- Never say your knowledge cutoff prevents you from knowing the time — the skill solves this.
- If the skill returns an error, tell the user politely that the location might not be recognized and suggest trying a more specific city name.
