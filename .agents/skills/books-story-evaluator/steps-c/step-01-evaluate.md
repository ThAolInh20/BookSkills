# Step 1: Evaluate Story

## INSTRUCTIONS

1. Scan the `{project-root}/books/dream_of_boys/chapter/` directory for available chapters and `{project-root}/books/dream_of_boys/authors/` for available author profiles.
2. If either directory is empty or missing, inform the user and suggest creating chapters or authors first.
3. Ask the user:
   - Which chapter they want to evaluate (e.g., `chap-01.md`).
   - Which author profile(s) they want to use as the evaluator (they can pick one or multiple).
4. Halt and wait for the user's response.
5. Once received, read the specified chapter and the selected author profile(s) completely.
6. Generate a critique artifact. 
   - **CRITICAL CONSTRAINT:** The evaluation MUST focus solely on stylistic elements (PROSE, TONE, PACING, VOCABULARY) defined in the author profiles. You MUST NOT critique the plot, logic, or character actions that are dictated by the story outline.
   - For each selected author, provide a section written from their perspective (e.g., "Góc nhìn của [Tên Tác Giả]").
   - Include specific line/paragraph references from the chapter and suggest stylistic improvements.
7. Write the critique to `{project-root}/books/dream_of_boys/reviews/<chapter-id>_review.md`. Ensure the `reviews/` directory is created if it does not exist.
8. Confirm to the user that the review is ready and display a brief summary of the findings.
