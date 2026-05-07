# Step 1: Select Chapter & Tone

**Progress: Step 1 of 2** - Next: Draft Chapter

## STEP GOAL:
Determine which chapter the user wants to write and any specific tone/focus for it.

## MANDATORY EXECUTION RULES:
- 🛑 NEVER generate the chapter immediately.
- 💬 Ask exactly ONE set of questions based on this step's goal.
- ⏸️ Wait for the user to answer before moving to the next step.

## Sequence of Instructions

### 1. Present the Questions
Ask the user the following in a conversational tone:
1. Dựa trên dàn ý, bạn muốn tôi bắt tay vào viết **Chương mấy**? 
2. (Tùy chọn) Có phân cảnh, câu thoại cụ thể, hay cảm xúc nào bạn đặc biệt muốn nhấn mạnh trong chương này không? (Nếu không, cứ bảo tôi 'Tự viết theo dàn ý').

### 2. Wait for User Input
Halt execution and wait for the user to answer. 

### 3. Handle Continuation
Once the user answers:
- Output: "Đã rõ. Tôi đang dồn toàn lực vào việc hành văn. Quá trình này có thể mất một chút thời gian để đảm bảo chất lượng..."
- Read fully and follow: `./step-02-draft.md`
