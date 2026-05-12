# Master Content OS

A white-label operating system for personal-brand content
production. Bring your own brand. Run the system.

The OS is a layered set of markdown files an LLM agent
reads in order to compress raw input (voice memos,
transcripts, notes, ideas) into platform-native content
that sounds like you, not like a template.

---

## Folder Map

```
01_brand/        Identity layer. Fill these in once per brand.
02_principles/   Universal copywriting and CTA rules.
03_pipeline/     Entry point + routing + human review.
04_platforms/    Platform-specific output rules.
  video/         Long form, short form, live.
  written/       X, LinkedIn, newsletter.
05_frameworks/   Storytelling and video hook libraries.
08_agents/       Agent role definitions (content, researcher, repurpose).
```

---

## How to Set Up a New Brand

1. Open `01_brand/brand_index.md` and fill in every
   bracketed field. This is the master file every
   other file inherits from.
2. Fill in the rest of the `01_brand/` folder:
   - `values.md` — core values + contrarian belief
   - `voice_and_tone.md` — voice attributes + banned phrases
   - `icp.md` — primary, secondary, tertiary audience
   - `origin_story.md` — story assets the OS pulls from
   - `content_pillars.md` — the topics you cover
3. Leave `02_principles/`, `05_frameworks/`, and `08_agents/`
   alone unless you have a specific reason to edit them.
   They're universal.
4. Optionally update `04_platforms/` platform files
   with brand-specific examples once you have them.

---

## How to Run a Content Generation Session

Point an LLM agent at the repo and give it raw input
(voice memo transcript, notes, an idea). The agent enters
through `03_pipeline/create_content.md`, which:

1. Compresses input into a structured brief
2. Waits for you to approve the brief
3. Generates a run manifest of all recommended outputs
4. Generates each output one at a time on your command

The pipeline never generates content until the brief
is approved. The agents never invent numbers or stories —
they pull only from the fact bank in `brand_index.md`.

---

## Conventions

- Bracketed placeholders like `[BRAND NAME]`, `[TARGET ROLE]`,
  or `[FACT 1]` mark fields to fill in.
- The fact bank in `brand_index.md` is the single source
  of truth for numbers and proof points. If a fact isn't
  there, it doesn't ship.
- Hard constraints in `brand_index.md` are non-negotiable
  filters every output passes through.
