---
description: Tailor a resume to a specific job description, emphasizing relevant experience and rewording bullets to match the JD's language
allowed-tools: Read, Write, WebFetch
argument-hint: "[paste JD and resume, or provide file paths]"
---

# Resume Tailoring

The user provided the following input which contains both a job description and a resume:

$ARGUMENTS

## Step 1: Identify inputs
Determine which part of the input is the JD and which is the resume. If the user provided file paths, read them. If they pasted text, work with the text.

## Step 2: Extract JD priorities
From the JD, identify:
- The 5-7 most important keywords or skills (technical and soft)
- The core problem the role is meant to solve
- The seniority level

## Step 3: Audit the existing resume
For each bullet point in the resume's experience section, assess:
- Does it demonstrate one of the JD's priorities? If yes, mark it.
- Is it quantified with a real metric? If no, flag it.
- Does the action verb match the energy of the role (build/ship/own vs analyze/research)?

## Step 4: Produce the tailored resume

Output the resume in markdown with these changes:
- Reorder bullets within each role so the most JD-relevant one is first
- Rewrite bullets to use the JD's exact language where truthful (don't fabricate experience)
- Strengthen quantification where the original is vague (e.g. "improved performance" → "improved load time by ~40%")
- Cut bullets that don't support the JD's priorities, unless cutting would leave the role with fewer than 2 bullets
- Adjust the summary/objective line (if present) to mirror the JD's framing

## Step 5: Provide a change log
At the bottom, list:
- Which bullets you rewrote and why
- Which bullets you cut
- Any JD priorities the resume doesn't address at all (these are gaps the candidate needs to address in the cover letter or interview)

Never fabricate experience. If the candidate doesn't have a skill the JD wants, say so in the change log rather than inventing it.