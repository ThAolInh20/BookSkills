# Step 5: Compilation

**Progress: Step 5 of 5** - Workflow Complete

## STEP GOAL:
Synthesize all collected information into a structured Story Bible document.

## MANDATORY EXECUTION RULES:
- 🛑 Do NOT ask the user any more questions.
- ✅ Rely entirely on the information gathered from Step 1, 2, 3, and 4.
- ✅ Create the output document silently, then notify the user.

## Sequence of Instructions

### 1. Structure the Document
Format the gathered information into a clean Markdown structure with the following sections:
- `# Bảng thông tin Truyện (Story Bible)`
- `## 1. Tổng quan (Overview)` (Genre, Premise, Theme)
- `## 2. Nhân vật (Characters)` (Protagonist, Antagonist, Motivations, Flaws)
- `## 3. Cốt truyện & Cấu trúc (Plot & Structure)` (Inciting Incident, Conflict, Climax)
- `## 4. Bối cảnh & Thế giới (World-building)` (Setting, Rules, Atmosphere)

### 2. Create the Story Bible
Create (or overwrite if it exists) a file named `docs/story-bible.md` in the `{project-root}` directory with the generated content. Use standard tools/instructions for writing files.

### 3. Report Completion
Present the user with the following completion message:
"🎉 **Story Bible đã được tạo thành công!**

Tôi đã tổng hợp tất cả câu trả lời của bạn và lưu vào `docs/story-bible.md`. 
Tài liệu này sẽ đóng vai trò như một 'nguồn chân lý' (Source of Truth) cho tất cả các hoạt động viết lách sau này. Bạn có thể mở file này ra để xem hoặc chỉnh sửa trực tiếp nếu cần thiết.

Luồng phỏng vấn kết thúc tại đây. Chúc bạn sáng tác vui vẻ!"

### 4. Workflow Exit
End the workflow. No further actions required.
