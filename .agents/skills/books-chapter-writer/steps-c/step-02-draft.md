# Step 2: Draft Chapter & Save

**Progress: Step 2 of 2** - Workflow Complete

## STEP GOAL:
Write the full chapter in high-quality prose and save it to a file.

## MANDATORY EXECUTION RULES:
- 🛑 Do NOT ask the user any more questions.
- ✅ Create the output document silently, then notify the user.
- ❗ CRITICAL: Strictly follow the events for this specific chapter as defined in `chapter-outline.md`. Do not write ahead into the next chapter's events.

## Sequence of Instructions

### 1. Write the Chapter (Memory)
Draft the entire chapter based on the user's choice in Step 1.
- Use rich prose, descriptive language, and natural dialogue.
- Ensure the tone matches the Story Bible.
- Ensure NO rules from `rules.md` are broken.

### 2. Save the Chapter Document
Create (or overwrite if it exists) a file named `docs/chapters/chap-{number}.md` (e.g., `docs/chapters/chap-01.md`) in the `{project-root}` directory with the generated chapter content.
*Note: If the `docs/chapters` directory does not exist, standard write tools will create it.*

### 3. Report Completion
Present the user with the following completion message:
"✍️ **Chương truyện đã được hoàn thành!**

Tôi đã viết xong và lưu tại `docs/chapters/chap-{number}.md`.
Bạn hãy đọc thử để xem văn phong, nhịp độ và các tình tiết đã đúng ý bạn chưa. Nếu cần chỉnh sửa một đoạn cụ thể, bạn có thể gọi tôi lại hoặc tự edit trực tiếp vào file.

Khi nào sẵn sàng cho chương tiếp theo, cứ gọi lại skill `bmad-chapter-writer` nhé!"

### 4. Workflow Exit
End the workflow. No further actions required.
