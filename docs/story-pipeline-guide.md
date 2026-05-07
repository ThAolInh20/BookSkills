# Hướng dẫn Kịch bản Sáng tác Truyện với BMad (Story Pipeline)

Tài liệu này hướng dẫn bạn cách sử dụng bộ 4 skill chuyên biệt trong hệ thống BMad để tạo ra một bộ truyện dài tập nhất quán, logic và hấp dẫn từ con số 0.

---

## 1. Tổng quan Kiến trúc (Pipeline)

Quy trình viết truyện được chia làm 4 công đoạn rõ ràng. Việc chia nhỏ này giúp AI:
- Không bị quá tải bộ nhớ (Context window).
- Đảm bảo tính nhất quán từ đầu đến cuối.
- Cho phép con người can thiệp, chỉnh sửa ở từng khâu trước khi đi vào chi tiết.

### Sơ đồ Quy trình:
`Ý Tưởng (Bible)` ➡️ `Dàn ý (Outline)` ➡️ `Luật lệ (Rules)` ➡️ `Viết Chương (Drafting)`

---

## 2. Các Bước Thực Hiện Cụ Thể

### Bước 1: Khởi tạo Story Bible (Kinh thánh Truyện)
**Mục tiêu:** Định hình Thể loại, Thông điệp, Nhân vật và Thế giới.

* **Lệnh gọi:** 
  > `@[/books-story-elicitation] Hãy phỏng vấn tôi để tạo truyện mới`
* **Cách hoạt động:** Skill sẽ đóng vai trò như một biên tập viên, phỏng vấn bạn 4 câu hỏi lần lượt. Hãy trả lời tự nhiên.
* **Đầu ra:** Tự động tạo file `docs/story-bible.md`.

### Bước 2: Chia Dàn ý các Chương (Outlining)
**Mục tiêu:** Chia nhỏ nội dung truyện thành các chương, đảm bảo nhịp độ (pacing) hợp lý.

* **Lệnh gọi:** 
  > `@[/books-story-outliner] Hãy lên dàn ý cho truyện`
* **Cách hoạt động:** Nó sẽ đọc `story-bible.md` và hỏi bạn dự định truyện dài bao nhiêu chương. Sau đó nó sẽ sinh ra dàn ý sự kiện cho từng chương.
* **Đầu ra:** Tự động tạo file `docs/chapter-outline.md`.
* **Lưu ý:** Bạn NÊN mở file này ra và chỉnh sửa lại bằng tay (thêm bớt tình tiết) cho đúng ý mình trước khi qua Bước 3.

### Bước 3: Khóa chặt Quy tắc Thế giới (Lore Keeping)
**Mục tiêu:** Trích xuất các ranh giới và luật lệ cứng để ngăn AI viết sai logic (OOC - Out of Character hoặc phi logic).

* **Lệnh gọi:** 
  > `@[/books-lore-keeper] Khởi tạo bộ luật cho truyện`
* **Cách hoạt động:** Nó phân tích 2 file ở trên và cho phép bạn bổ sung các luật "Tuyệt đối không được vi phạm".
* **Đầu ra:** Tự động tạo file `docs/rules.md`.

### Bước 4: Viết Chi tiết Từng Chương (Chapter Writing)
**Mục tiêu:** Hành văn, viết lời thoại và miêu tả chi tiết.

* **Lệnh gọi:** 
  > `@[/books-chapter-writer] Viết truyện`
* **Cách hoạt động:** Skill này sẽ bắt buộc đọc cả 3 file (Bible, Outline, Rules). Nó sẽ hỏi bạn muốn viết chương nào. Sau khi bạn chọn, nó sẽ dành toàn bộ tài nguyên để hành văn thật trau chuốt cho đúng chương đó.
* **Đầu ra:** Tự động tạo file `docs/chapters/chap-[số thứ tự].md`.

---

## 3. Lời khuyên Thực chiến

- **Mở rộng Truyện:** Nếu bạn muốn truyện dài hơn dàn ý ban đầu, hãy gọi lại `books-story-outliner` và bảo nó "viết dàn ý cho Arc 2" (Phần 2).
- **Sửa Lỗi Tức thời:** Nếu `books-chapter-writer` viết một chương mà nhân vật hành xử kỳ lạ, đừng cãi nhau với nó. Hãy mở file `docs/rules.md`, bổ sung thêm một luật về tính cách của nhân vật đó, rồi gọi lại skill viết chương. AI sẽ lập tức ngoan ngoãn tuân theo!
