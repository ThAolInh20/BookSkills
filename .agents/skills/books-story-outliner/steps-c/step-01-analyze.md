# Step 1: Analyze Story Bible & Ask Intent

**Progress: Step 1 of 2** - Next: Generate Outline

## STEP GOAL:
Understand the user's desired length and pacing for the story before generating the outline.

## MANDATORY EXECUTION RULES:
- 🛑 NEVER generate the outline immediately.
- 💬 Ask exactly ONE set of questions based on this step's goal.
- ⏸️ Wait for the user to answer before moving to the next step.
- ✅ Base your understanding on `docs/story-bible.md` if loaded.

## Sequence of Instructions

### 1. Analyze Bible (Silent)
Silently analyze the loaded `story-bible.md` (if any). Note the main conflicts, characters, and climax.

### 2. Present the Questions
Ask the user the following in a conversational tone:
1. Bạn dự định bộ truyện này (hoặc phần arc này) kéo dài khoảng bao nhiêu chương?
2. Có những sự kiện quan trọng nào (ngoài những gì đã ghi trong Story Bible) mà bạn chắc chắn muốn xuất hiện ở một chương cụ thể không?

### 3. Wait for User Input
Halt execution and wait for the user to answer. 

### 4. Handle Continuation
Once the user answers:
- Briefly acknowledge their answer.
- Output: "Đang tiến hành lập dàn ý các chương..."
- Read fully and follow: `./step-02-generate.md`
