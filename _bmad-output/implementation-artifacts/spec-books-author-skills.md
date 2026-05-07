---
title: 'Author Generation and Evaluation Skills'
type: 'feature'
created: '2026-05-07T08:17:08+07:00'
status: 'done'
context: []
baseline_commit: '3ed6041777459229056191d1fa233b6a2d69c16d'
---

<frozen-after-approval reason="human-owned intent — do not modify unless human renegotiates">

## Intent

**Problem:** The current story generation pipeline relies on a single static set of rules for narrative voice, making it difficult to generate stories with diverse writing styles, tones, and perspectives. There is also no automated system to evaluate the generated stories from the specific stylistic viewpoints of different authors.

**Approach:** Create three new skills (`books-author-generator`, `books-author-updater`, `books-story-evaluator`) to establish an Author ecosystem. The generator and updater will manage Markdown-based author profiles in `books/dream_of_boys/authors/`, defining prose, tone, and pacing without altering the plot. The evaluator will read generated chapters against these profiles to produce stylistic critiques in `books/dream_of_boys/reviews/`. We will also update `docs/story-pipeline-guide.md` to reflect this new architecture.

## Boundaries & Constraints

**Always:**
- Author profiles MUST explicitly state they dictate PROSE, TONE, and PACING, but MUST NOT alter the plot outlined in the chapter specs or Story Bible.
- New skills MUST follow the step-file architecture (e.g., `./steps-c/step-01-...`).
- Evaluation critiques MUST focus on writing style, emotional resonance, and pacing, NOT plot holes or character actions driven by the outline.

**Ask First:**
- If changing the folder structure from `authors/` and `reviews/` to something else.

**Never:**
- Do not modify existing core skills (`books-chapter-writer`, etc.) in this spec; this spec only creates the new skills and updates the documentation.

## I/O & Edge-Case Matrix

| Scenario | Input / State | Expected Output / Behavior | Error Handling |
|----------|--------------|---------------------------|----------------|
| Generate Author | User provides author traits (age, style, tone) via `books-author-generator` | Creates `books/dream_of_boys/authors/{author_id}.md` with YAML frontmatter and markdown body | N/A |
| Update Author | User provides an existing `author_id` and edit instructions via `books-author-updater` | Updates the existing `{author_id}.md` file while preserving unmodified traits | Warn user if author file does not exist |
| Evaluate Story | User runs `books-story-evaluator` on `{chapter_id}` with selected authors | Generates a critique file in `books/dream_of_boys/reviews/{chapter_id}_review.md` | Warn user if chapter or author profiles are missing |

</frozen-after-approval>

## Code Map

- `e:/Truyen/.agents/skills/books-author-generator/` -- New skill directory for generating authors.
- `e:/Truyen/.agents/skills/books-author-updater/` -- New skill directory for updating authors.
- `e:/Truyen/.agents/skills/books-story-evaluator/` -- New skill directory for story evaluation.
- `e:/Truyen/docs/story-pipeline-guide.md` -- Project documentation to be updated with the new Author flow.

## Tasks & Acceptance

**Execution:**
- [x] `e:/Truyen/.agents/skills/books-author-generator/SKILL.md` -- Create skill definition.
- [x] `e:/Truyen/.agents/skills/books-author-generator/steps-c/step-01-generate.md` -- Create execution step for generation.
- [x] `e:/Truyen/.agents/skills/books-author-updater/SKILL.md` -- Create skill definition.
- [x] `e:/Truyen/.agents/skills/books-author-updater/steps-c/step-01-update.md` -- Create execution step for updating.
- [x] `e:/Truyen/.agents/skills/books-story-evaluator/SKILL.md` -- Create skill definition.
- [x] `e:/Truyen/.agents/skills/books-story-evaluator/steps-c/step-01-evaluate.md` -- Create execution step for evaluation.
- [x] `e:/Truyen/docs/story-pipeline-guide.md` -- Add the Author ecosystem documentation and update the workflow flowchart.

**Acceptance Criteria:**
- Given a user intent to create an author, when `books-author-generator` is run, then it creates a standardized markdown profile in the `authors/` directory with a strict "Do not alter plot" constraint.
- Given an existing author, when `books-author-updater` is run, then it modifies the profile successfully.
- Given a written chapter, when `books-story-evaluator` is run, then it outputs a stylistic review artifact in the `reviews/` directory.

## Spec Change Log

## Design Notes

The Author profile should have a structured YAML frontmatter for metadata (Name, Age, Core Style) and a Markdown body for detailed instructions (Pacing, Vocabulary, Tone).
Example frontmatter:
```yaml
name: "Stephen King Style"
age: 50
core_style: "Suspenseful, highly descriptive, internal monologues"
```

## Suggested Review Order

**Project Documentation**

- Cập nhật quy trình thêm bước Author Management và Evaluation.
  [`story-pipeline-guide.md:42`](../../docs/story-pipeline-guide.md#L42)

**Author Generator**

- Khởi tạo file định nghĩa skill tạo tác giả mới.
  [`SKILL.md:1`](../../.agents/skills/books-author-generator/SKILL.md#L1)

- Bước thực thi để prompt người dùng và lưu file tác giả.
  [`step-01-generate.md:1`](../../.agents/skills/books-author-generator/steps-c/step-01-generate.md#L1)

**Author Updater**

- Khởi tạo file định nghĩa skill cập nhật tác giả.
  [`SKILL.md:1`](../../.agents/skills/books-author-updater/SKILL.md#L1)

- Bước thực thi cập nhật nhưng giữ nguyên constraint cốt truyện.
  [`step-01-update.md:1`](../../.agents/skills/books-author-updater/steps-c/step-01-update.md#L1)

**Story Evaluator**

- Khởi tạo file định nghĩa skill đánh giá truyện.
  [`SKILL.md:1`](../../.agents/skills/books-story-evaluator/SKILL.md#L1)

- Bước thực thi đọc chương và các file tác giả để nhận xét văn phong.
  [`step-01-evaluate.md:1`](../../.agents/skills/books-story-evaluator/steps-c/step-01-evaluate.md#L1)
