# create_content.md — Pipeline Entry Point

## Purpose
This is the first file the agent reads on every single run.
It accepts any input format, compresses it into a structured
brief, and produces a run manifest before generating anything.

No content is generated until the brief is approved.
No platform output is generated until "next" is typed.

---

## Accepted Input Formats

- Voice memo transcripts (any length)
- Interview or podcast transcripts
- Research dumps or article notes
- Existing posts or pieces to repurpose
- Bullet points or rough notes
- A single idea or sentence
- Agent-generated research briefs

---

## Step 1: Compression (always runs first)

When input is received, the agent does NOT generate
content immediately. It compresses the input into a
structured brief using this template:

BRIEF TEMPLATE

Date: [DATE]
Input type: [voice memo / transcript / notes / idea]
Input length: [approximate word count or duration]

Core idea (one sentence):
[The single most important thing this input is about]

Supporting ideas (max 3):
1.
2.
3.

Best hook candidate:
[The sharpest, most specific, most visual moment
from the input — a stat, story, or provocation]

Proof points available:
[Real numbers, stories, or examples from the input]

Relevant content pillars:
[Which pillars from brand_index.md this content touches]

Relevant framework:
[Which storytelling framework fits best]

Recommended formats:
[Which platform outputs make sense and why]

---

## Step 2: Brief Review

After the brief is generated, the agent presents it and asks:

"Does this brief capture the right core idea?
Type APPROVED to generate the run manifest
or tell me what to adjust."

The agent does not proceed until the brief is approved.

---

## Step 3: Run Manifest

Once the brief is approved, the agent generates a run manifest.

RUN MANIFEST TEMPLATE

RUN MANIFEST — [DATE]
Input: [one line description]
Core idea: [one sentence from brief]

Queue:
[ ] 1. X post (short form)
[ ] 2. X thread
[ ] 3. LinkedIn post
[ ] 4. LinkedIn article
[ ] 5. Newsletter — [format: story/roundup/essay/announcement]
[ ] 6. Video — short form hook and caption
[ ] 7. Video — long form outline
[ ] 8. Live — run of show talking points

Type NEXT to generate output 1.
Type SKIP to skip any output.
Type PAUSE to stop and resume later.
Type AUTOPUBLISH to run all outputs automatically.

---

## Step 4: Output Generation

For each output:
1. Load the relevant platform file from 04_platforms/
2. Apply copywriting_principles.md as the filter
3. Apply brand_index.md for voice and tone
4. Apply the relevant storytelling framework excerpt
5. Generate the output
6. Check the box in the manifest
7. Show what's next and wait for NEXT

Each output is generated one at a time.
The brief stays constant across all outputs.
Only the platform file swaps out.

---

## Step 5: Quality Check

Before presenting any output, run the pre-publish checklist:

- [ ] Passes 3-question master test
- [ ] One clear idea
- [ ] Hook earns the next line
- [ ] At least one concrete proof point
- [ ] Practical takeaway present
- [ ] Close tells reader what to think, feel, or do
- [ ] Could not be signed by a competitor
- [ ] Sounds like the brand voice, not a template

If any box fails — rewrite before presenting.

---

## Token Budget Rules

- Brief: 400 words max
- Each platform file: loaded one at a time
- Brand index: always loaded
- Copywriting principles: always loaded
- Storytelling frameworks: load only the relevant excerpt
- Never load all platform files simultaneously

---

## Input Size Guidelines

| Input size | Expected brief | Expected outputs |
|---|---|---|
| Single idea | 100 words | 1-3 outputs |
| Short notes 500 words | 150 words | 3-5 outputs |
| 5-7 min voice memo | 250 words | 4-6 outputs |
| 15-20 min voice memo | 350 words | 6-8 outputs |
| 30+ min voice memo | 400 words max | Full manifest |

For inputs over 30 minutes — compress aggressively.
Brief never exceeds 400 words regardless of input size.
If input has more than 5 core ideas, flag and ask which
single idea to prioritize for this run.

---

## Default Behavior

If no ICP is specified: default to Primary ICP.
If no platform preference: default to full manifest.
If no framework is obvious: PAS for short form,
Story Circle for long form.
If no proof points in input: flag and pull from
the fact bank in brand_index.md.
If input conflicts with hard constraints: flag before generating.
