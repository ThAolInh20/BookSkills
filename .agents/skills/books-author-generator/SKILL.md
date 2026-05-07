---
name: "books-author-generator"
description: "Tạo hồ sơ tác giả mới. Khởi tạo file định dạng chuẩn trong thư mục authors/ để định hướng văn phong, nhịp độ và từ vựng mà không làm thay đổi cốt truyện."
---

# books-author-generator

**Goal:** Create a new author profile markdown file in `{project-root}/books/dream_of_boys/authors/`.

## WORKFLOW ARCHITECTURE

This uses **step-file architecture**.

### Step Processing Rules

1. **READ COMPLETELY**: Always read the entire step file before taking any action.
2. **FOLLOW SEQUENCE**: Execute all numbered sections in order.
3. **WAIT FOR INPUT**: Halt and wait for user selection/answers when prompted.
4. **LOAD NEXT**: When directed, read fully and follow the next step file.

## On Activation

### Step 1: Initialize Author Generation
Read fully and follow: `./steps-c/step-01-generate.md`
