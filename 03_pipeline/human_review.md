# human_review.md — When and How to Intervene

## Purpose
Defines when the human operator steps in to edit,
redirect, or override the pipeline. This is not
bureaucracy. It's quality control.

---

## Always Review (never skip)

**Brand-sensitive content:**
Any content including personal stories, specific
metrics, named entities from brand_index.md, or
opinions on named individuals. Numbers and stories
must be verified accurate.

**First run on any new topic:**
The first time the pipeline generates content on a
topic the brand hasn't covered before.

**LinkedIn articles and long-form video scripts:**
High-investment, high-visibility. Always review.

---

## Can Bypass Review

**Repurposed content:**
Derived from a piece already published and approved.
Check the hook and CTA. Trust the body.

**X posts from approved frameworks:**
Clean expression of a well-known pillar. Read, approve, post.

---

## The 5-Minute Review Checklist

**Voice check:**
- Does this sound like the brand or like a template?
- Is the warmth there or does it feel cold?
- Would the operator actually say this out loud?

**Fact check:**
- Are all numbers accurate?
- Are all stories told correctly?
- Is anything exaggerated or understated?

**Hook check:**
- Does the first line make me want to read the second?
- Is it specific enough?
- Could a competitor write this hook? If yes — rewrite.

**Close check:**
- Does it end with intention?
- Is there exactly one CTA?
- Does the CTA match the goal of this piece?

**Gut check:**
- Would I be proud if 10,000 of the ICP saw this?
- Does this make the reader smarter or just feel good?
- Is there anything here I'd regret?

---

## Feedback Formats That Work

Voice off: "This sounds too corporate. Make it sound like
I'm talking to a [TARGET READER] over coffee."

Hook weak: "The hook is too generic. Lead with the
[specific fact] from the fact bank."

Too long: "Cut this by 40%. Keep the framework, cut the setup."

Wrong framework: "This should be a contrarian take, not a how-to."

Fact wrong: "The number is [correct]. Fix and re-check."

Tone wrong: "Too motivational. Ground it with a real example."

---

## The Bypass Protocol

Type AUTOPUBLISH at the manifest stage to skip review.

The agent will:
1. Generate all outputs in sequence
2. Run the pre-publish checklist automatically
3. Flag any output that fails the checklist
4. Deliver all passing outputs in one batch

Use AUTOPUBLISH only for low-stakes content,
repurposed content from approved pieces, and drafting.
Never for first-run topics, brand-sensitive content,
or long-form pieces.

---

## Version Control

Save every approved output to:
07_outputs/v2_reviewed/

Filename format:
YYYY-MM-DD_platform_topic-slug.md

Example:
2025-01-06_linkedin-post_pillar-name-slug.md
