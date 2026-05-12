# platform_index.md — Content Router

## Purpose
Routing layer between the brief and platform-specific output.
Tells the pipeline which platform files to load and in what
order for any given run.

---

## Platform Registry

### Written

| Platform | File | Best for |
|---|---|---|
| X post | 04_platforms/written/x/x_post.md | Single punchy idea |
| X thread | 04_platforms/written/x/x_thread.md | Teaching, frameworks |
| X long form | 04_platforms/written/x/x_longform.md | Deep dives, essays |
| LinkedIn post | 04_platforms/written/linkedin/linkedin_post.md | Founder audience |
| LinkedIn article | 04_platforms/written/linkedin/linkedin_article.md | Long-form authority |
| Newsletter — story | 04_platforms/written/newsletter/formats/story.md | Narrative content |
| Newsletter — roundup | 04_platforms/written/newsletter/formats/roundup.md | Multi-topic weeks |
| Newsletter — essay | 04_platforms/written/newsletter/formats/essay.md | Single idea depth |
| Newsletter — announcement | 04_platforms/written/newsletter/formats/announcement.md | Launches, updates |

### Video

| Platform | File | Best for |
|---|---|---|
| Short form | 04_platforms/video/shortform.md | Hook and caption |
| Long form | 04_platforms/video/longform.md | Full script |
| Live | 04_platforms/video/live/run_of_show.md | Live show prep |

---

## Routing Logic

**Single punchy idea or hot take:**
X post first, LinkedIn post second.

**Framework or system explanation:**
X thread, LinkedIn article, Newsletter essay, Long form video.

**Personal story or building-in-public:**
LinkedIn post, Newsletter story, X thread, Long form video.

**Tutorial or how-to:**
X thread, LinkedIn article, Long form video, Newsletter essay.

**Product update or announcement:**
LinkedIn post, Newsletter announcement, X post.

**Live show prep:**
Live run of show only.

---

## Format Selection Rules

X post vs X thread:
- Post: one insight that lands in 280 chars or less
- Thread: needs more than 3 tweets to fully explain

LinkedIn post vs LinkedIn article:
- Post: single insight, story, or take
- Article: framework or system that needs headers

Newsletter story vs essay:
- Story: insight comes through narrative or experience
- Essay: standalone argument or framework, no story needed

When to include video:
- Short form: any input with a strong single hook
- Long form: any input with a framework or multi-beat story
- Live: only when input is specifically about a live topic

---

## Load Order for Each Output

1. brand_index.md (always first)
2. copywriting_principles.md (always second)
3. Relevant storytelling framework excerpt only
4. platform_index.md routing decision (this file)
5. Specific platform file for the output being generated

Never load all platform files at once.
Never load the full storytelling frameworks file.

---

## Quality Gates

Before routing to any platform file, confirm:

- [ ] Brief has been approved
- [ ] Core idea is one sentence
- [ ] At least one proof point exists
- [ ] Hard constraints from brand_index.md are clear
- [ ] Platform selection matches input type

If any gate fails — return to create_content.md.
