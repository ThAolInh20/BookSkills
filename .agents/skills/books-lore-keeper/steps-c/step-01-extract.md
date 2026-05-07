# Step 1: Extract & Ask for Manual Rules

**Progress: Step 1 of 2** - Next: Finalize Rules

## STEP GOAL:
Identify implied rules from the context and ask the user if they want to add any manual constraints.

## MANDATORY EXECUTION RULES:
- 🛑 NEVER generate the rules.md immediately.
- 💬 Ask exactly ONE set of questions based on this step's goal.
- ⏸️ Wait for the user to answer before moving to the next step.

## Sequence of Instructions

### 1. Present the Questions
Ask the user the following in a conversational tone:
"Dựa vào Story Bible và Dàn ý, tôi sẽ tự động trích xuất các quy tắc chung (hệ thống phép thuật, giới hạn thời gian, quy chuẩn đạo đức của nhân vật...). 
Tuy nhiên, bạn có muốn BỔ SUNG thêm một số quy tắc cứng (Hard Rules) nào mà AI **TUYỆT ĐỐI KHÔNG ĐƯỢC VI PHẠM** khi viết truyện không? 
*(Ví dụ: 'Nhân vật chính không bao giờ được giết người', hoặc 'Công nghệ tối đa chỉ ở mức súng kíp')*"

### 2. Wait for User Input
Halt execution and wait for the user to answer. 

### 3. Handle Continuation
Once the user answers:
- Output: "Đã ghi nhận các quy tắc. Đang tiến hành biên soạn Rules.md..."
- Read fully and follow: `./step-02-finalize.md`
