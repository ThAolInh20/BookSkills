# Step 1: Update Author Profile

## INSTRUCTIONS

1. List the available author profiles by searching the `{project-root}/books/dream_of_boys/authors/` directory. If the directory does not exist or is empty, inform the user and suggest using `books-author-generator` first.
2. Ask the user:
   - Which author profile they want to update.
   - What specific changes they want to make (e.g., "Thay đổi nhịp độ cho chậm lại", "Dùng từ vựng cổ kính hơn").
3. Halt and wait for the user's response.
4. Once received, read the specified author profile file.
5. Apply the user's requested changes to the content. 
   - **CRITICAL CONSTRAINT:** You must preserve the existing `Constraints` section that strictly prohibits altering the plot. Do NOT remove or modify this core rule.
   - You may update the YAML frontmatter if the user requests changes to age, name, or core style.
6. Write the updated content back to the file, overwriting the old content.
7. Confirm to the user that the profile has been successfully updated.
