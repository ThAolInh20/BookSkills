---
name: books-cover-generator
description: Phân tích chiều sâu cốt truyện từ Story Bible và làm việc với tác giả để tạo ra một ảnh bìa mang tính ẩn dụ sâu sắc cho tác phẩm.
---
# books-cover-generator

**Goal:** Tạo ra một ảnh bìa (Book Cover) có chiều sâu, mang tính biểu tượng và phản ánh đúng tinh thần của tác phẩm, dựa trên sự kết hợp giữa thiết kế thị giác và văn phong của tác giả.

## Hướng dẫn thực thi (Execution Steps)

1. **Nghiên cứu Cốt truyện (Story Context):**
   - Đọc `story-bible.md` của tác phẩm để nắm bắt Thể loại (Genre), Chủ đề (Theme), và Động cơ cốt lõi (Core Motivation) của nhân vật chính.
   - Xác định những nút thắt tâm lý hoặc những yếu tố thế giới quan (World-building) nổi bật.

2. **Nghiên cứu Văn phong (Author Profile):**
   - Đọc file tác giả trong thư mục `authors/` (ví dụ: `stephen-green-hybrid.md`) để hiểu rõ phong cách nghệ thuật, mood & tone (ví dụ: Lyrical Healing, tĩnh lặng, buồn bã).

3. **Phác thảo Ý tưởng Ẩn dụ (Visual Metaphor Brainstorming):**
   - **Không vẽ lại một cảnh hành động đơn thuần.** Thay vào đó, hãy tìm ra một hình ảnh ẩn dụ đại diện cho toàn bộ câu chuyện.
   - *Ví dụ:* Sự giằng xé nội tâm (những mảnh kính vỡ), sự chữa lành (hoa bồ công anh, ánh sáng hổ phách), hoặc sự tĩnh lặng sau cơn bão.

4. **Đề xuất và Tinh chỉnh (Consultation):**
   - Trình bày 1-2 ý tưởng thiết kế (Bố cục, Màu sắc chủ đạo, Hình ảnh trọng tâm) cho người dùng.
   - Điều chỉnh ý tưởng dựa trên phản hồi của người dùng để đảm bảo ảnh bìa đạt được chiều sâu cảm xúc lớn nhất.

5. **Tạo ảnh bìa (Generate Image):**
   - Sử dụng tool `generate_image` với một câu lệnh (prompt) miêu tả bằng tiếng Anh cực kỳ chi tiết về Art Style (vd: Studio Ghibli, Makoto Shinkai), Lighting, Color Palette, và Composition.
   - Đảm bảo trong prompt có câu lệnh "No text on the image" để ảnh không bị dính chữ lỗi.
