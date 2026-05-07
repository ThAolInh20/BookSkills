---
name: "books-story-evaluator"
description: "Đánh giá truyện đa tác giả. Đọc một chương truyện và dùng hồ sơ của các tác giả để tạo ra nhận xét chuyên môn về văn phong, nhịp độ và từ vựng."
---

# books-story-evaluator

**Goal:** Generate a stylistic critique of a chapter in `{project-root}/books/dream_of_boys/reviews/`.

## WORKFLOW ARCHITECTURE

This uses **step-file architecture**.

### Step Processing Rules

1. **READ COMPLETELY**: Always read the entire step file before taking any action.
2. **FOLLOW SEQUENCE**: Execute all numbered sections in order.
3. **WAIT FOR INPUT**: Halt and wait for user selection/answers when prompted.
4. **LOAD NEXT**: When directed, read fully and follow the next step file.

## On Activation

### Step 1: Evaluate Story
Read fully and follow: `./steps-c/step-01-evaluate.md`
