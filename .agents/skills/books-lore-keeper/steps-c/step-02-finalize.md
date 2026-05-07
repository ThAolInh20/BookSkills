# Step 2: Finalize Rules & Save

**Progress: Step 2 of 2** - Workflow Complete

## STEP GOAL:
Generate a definitive `rules.md` and save it to `docs/rules.md`.

## MANDATORY EXECUTION RULES:
- 🛑 Do NOT ask the user any more questions.
- ✅ Create the output document silently, then notify the user.

## Sequence of Instructions

### 1. Structure the Document
Format the rules into a clean Markdown structure:
- **Hệ thống Thế giới (World Systems):** Magic, Tech, Physics.
- **Giới hạn Nhân vật (Character Constraints):** What characters CANNOT do.
- **Luật Xã hội/Chính trị (Social/Political Laws)**
- **Quy tắc của Tác giả (Author's Hard Rules):** The specific rules the user provided in Step 1.

### 2. Create the Rules Document
Create (or overwrite if it exists) a file named `docs/rules.md` in the `{project-root}` directory with the generated rules content. Use standard tools/instructions for writing files.

### 3. Report Completion
Present the user with the following completion message:
"🛡️ **Cuốn Luật Lệ (Lore/Rules) đã được niêm phong!**

Tôi đã lưu tất cả quy tắc vào `docs/rules.md`. Bất kỳ khi nào skill `bmad-chapter-writer` hoạt động, nó sẽ phải soi chiếu vào cuốn luật này để tránh viết những tình tiết phi logic.
Bạn đã sẵn sàng để viết chương đầu tiên chưa? Hãy gọi `bmad-chapter-writer` nhé!"

### 4. Workflow Exit
End the workflow. No further actions required.
