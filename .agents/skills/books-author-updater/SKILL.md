---
name: "books-author-updater"
description: "Cập nhật hồ sơ tác giả. Đọc và chỉnh sửa file hồ sơ tác giả hiện có trong thư mục authors/."
---

# books-author-updater

**Goal:** Update an existing author profile markdown file in `{project-root}/books/dream_of_boys/authors/`.

## WORKFLOW ARCHITECTURE

This uses **step-file architecture**.

### Step Processing Rules

1. **READ COMPLETELY**: Always read the entire step file before taking any action.
2. **FOLLOW SEQUENCE**: Execute all numbered sections in order.
3. **WAIT FOR INPUT**: Halt and wait for user selection/answers when prompted.
4. **LOAD NEXT**: When directed, read fully and follow the next step file.

## On Activation

### Step 1: Update Author Profile
Read fully and follow: `./steps-c/step-01-update.md`
