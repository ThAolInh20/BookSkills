# Step 1: Generate Author Profile

## INSTRUCTIONS

1. Ask the user for the following details to create the new author profile:
   - **Name** (Tên tác giả hoặc tên phong cách)
   - **Age** (Độ tuổi/Kinh nghiệm)
   - **Core Style** (Phong cách cốt lõi)
   - **Pacing & Dialogue** (Sở thích về nhịp độ câu chuyện và mật độ thoại)
   - **Tone & Vocabulary** (Giọng điệu và thói quen dùng từ)
2. Halt and wait for the user's response.
3. Once received, generate the markdown content for the profile. 
   The file MUST have the following structure:
   ```markdown
   ---
   name: "[Author Name]"
   age: [Age]
   core_style: "[Core Style]"
   ---

   # Author Profile: [Author Name]

   ## Constraints
   > [!IMPORTANT]
   > Your role is to dictate PROSE, TONE, and PACING. You MUST NOT add new events, remove characters, or alter the plot outlined in the chapter specs or the Story Bible.

   ## Pacing & Dialogue
   [Detailed pacing and dialogue preferences]

   ## Tone & Vocabulary
   [Detailed tone and vocabulary preferences]
   ```
4. Write the generated content to `{project-root}/books/dream_of_boys/authors/<author-slug>.md` (use a kebab-case filename based on the author's name).
5. Confirm to the user that the profile has been created and remind them they can now provide this file to `books-chapter-writer` to apply the style.
