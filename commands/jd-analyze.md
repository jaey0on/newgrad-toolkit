---
description: Analyze a job description to extract must-haves, nice-to-haves, hidden signals, and likely salary band
allowed-tools: WebSearch, WebFetch, Read
argument-hint: "[paste JD text or provide a URL]"
---

# Job Description Analysis

The user wants a deep breakdown of the following job description:

> $ARGUMENTS

If the input is a URL, fetch the page first using WebFetch. If the input is pasted text, work with it directly.

Produce an analysis with these exact sections:

## 1. Role Summary
One sentence on what this role actually does day-to-day. Cut through the marketing language.

## 2. Must-Haves (Hard Requirements)
List every requirement that's truly non-negotiable. For each, mark:
- Whether it's technical (skill/tool) or experiential (years/domain)
- A rough proficiency bar (entry / intermediate / senior)

## 3. Nice-to-Haves
Preferred but not required. These are differentiators if the candidate has them.

## 4. Hidden Signals
What the JD reveals about the company that they're not explicitly saying. Examples:
- Words like "fast-paced" / "wear many hats" → understaffed or chaotic
- "Self-starter" with no mention of mentorship → minimal onboarding
- Heavy emphasis on "ownership" → individual contributor expected to drive their own roadmap
- Long list of nice-to-haves → company doesn't know exactly what they need
- Specific frameworks/tools mentioned multiple times → that's the real tech stack

## 5. Likely Compensation Band
Estimate base salary range based on:
- Role level (entry, mid, senior, staff)
- Location (if specified) or default to US-remote
- Company stage/size (if identifiable)
- Industry norms

Provide a range like "$X - $Y base, possibly + equity if startup." If you can't determine, say so and explain what you'd need to estimate.

## 6. Red Flags
Anything concerning. Examples:
- No salary listed when state law requires it (CA, CO, NY, WA, etc.) → either willful violation or low pay
- Vague title like "Rockstar Engineer"
- Mismatched seniority (entry-level title with 5+ years required)
- Buzzword stew with no concrete responsibilities

## 7. Application Strategy
Given everything above, the top 3 things a candidate should emphasize in their application to stand out for this specific role.

Be direct and specific. Avoid generic advice. If the JD is light on detail, say so and work with what's there.