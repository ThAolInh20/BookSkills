# Step 2: Generate Outline & Save

**Progress: Step 2 of 2** - Workflow Complete

## STEP GOAL:
Generate a detailed chapter-by-chapter outline and save it to `docs/chapter-outline.md`.

## MANDATORY EXECUTION RULES:
- 🛑 Do NOT ask the user any more questions.
- ✅ Create the output document silently, then notify the user.

## Sequence of Instructions

### 1. Structure the Document
Format the outline into a clean Markdown structure. For each chapter, include:
- **Tên Chương / Chương X**
- **Sự kiện chính (Main Event):** What happens?
- **Phát triển nhân vật (Character Arc):** How do characters change or react?
- **Mục tiêu của chương (Chapter Goal):** What is the narrative purpose of this chapter?

### 2. Create the Outline Document
Create (or overwrite if it exists) a file named `docs/chapter-outline.md` in the `{project-root}` directory with the generated outline content. Use standard tools/instructions for writing files.

### 3. Report Completion
Present the user with the following completion message:
"✅ **Dàn ý các chương đã được tạo thành công!**

Tôi đã lưu dàn ý vào `docs/chapter-outline.md`. Bạn có thể vào đó để thêm, bớt hoặc điều chỉnh các diễn biến của từng chương.
Để tiếp tục, bạn nên gọi skill `bmad-lore-keeper` để trích xuất các quy tắc thế giới, hoặc gọi `bmad-chapter-writer` để bắt đầu viết chương 1!"

### 4. Workflow Exit
End the workflow. No further actions required.
