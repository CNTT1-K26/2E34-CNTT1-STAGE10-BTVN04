# Bài Tập: Thiết Kế Prompt Trợ Lý Học Tập (Mô Hình IPO Trong Trang Trại Thông Minh)

## I. Thiết Kế Kiến Trúc Prompt (3 Phần)

```markdown
# Bối cảnh
Bạn là một gia sư công nghệ thông tin thân thiện, kiên nhẫn và giàu kinh nghiệm sư phạm. Tôi là sinh viên năm nhất ngành Công nghệ Thông tin, chưa có nhiều kiến thức nền tảng và đang gặp khó khăn khi tìm hiểu về "Mô hình IPO (Input - Process - Output) trong Trang trại thông minh (Smart Farm)".

## Nội dung
Hãy giải thích khái niệm Mô hình IPO trong trang trại thông minh một cách đơn giản, trực quan và dễ tiếp thu nhất. Sử dụng các hình ảnh so sánh hoặc ví dụ thực tế gần gũi trong nông nghiệp (như hệ thống tưới nước tự động hay theo dõi nhiệt độ nhà kính) để tôi dễ hình dung.

## Yêu cầu
- [ ] Giải thích rõ nghĩa của 3 thành phần: Input (Đầu vào), Process (Xử lý), và Output (Đầu ra) trong ngữ cảnh nông nghiệp thông minh.
- [ ] Trình bày 01 ví dụ thực tế hoàn chỉnh minh họa trọn vẹn chu trình IPO của một thiết bị IoT nông nghiệp.
- [ ] Ràng buộc ngôn ngữ: Sử dụng tiếng Việt chuẩn xác. Nếu bắt buộc dùng thuật ngữ tiếng Anh, phải mở ngoặc giải thích nghĩa tiếng Việt ngay bên cạnh.
- [ ] Giới hạn độ dài: Câu trả lời không vượt quá 400 từ, trình bày ngắn gọn bằng các đầu dòng ngắn (bullet points).

## Không cần
- Không sử dụng các thuật ngữ kỹ thuật quá chuyên sâu (như kiến trúc vi điều khiển, giao thức mạng MQTT/HTTP, mã nguồn lập trình, thuật toán ML).
- Không đưa ra các lý thuyết hàn lâm dài dòng hoặc các phân tích kinh tế/kinh doanh ngoài phạm vi bài học sinh viên năm 1.
```

---

## II. Xử Lý Trường Hợp Kiểm Thử (Edge Cases)

Để xử lý nguy cơ AI phản hồi quá dài hoặc tràn ngập thuật ngữ tiếng Anh chuyên môn, các ràng buộc sau đã được tích hợp trực tiếp vào Prompt:

1. **Kiểm soát độ dài:**
   - Thêm tiêu chí cụ thể vào **Task List**: `- [ ] Giới hạn độ dài: Câu trả lời không vượt quá 400 từ, trình bày ngắn gọn bằng các đầu dòng ngắn (bullet points).`
2. **Kiểm soát độ khó & Ngôn ngữ:**
   - Thêm quy định giải thích từ vựng: `- [ ] Ràng buộc ngôn ngữ: Sử dụng tiếng Việt chuẩn xác. Nếu bắt buộc dùng thuật ngữ tiếng Anh, phải mở ngoặc giải thích nghĩa tiếng Việt ngay bên cạnh.`
   - Chặn các kiến thức phức tạp tại mục **## Không cần**: Khống chế việc xuất hiện mã nguồn, giao thức mạng hay lý thuyết chuyên ngành sâu.

---

## III. Hướng Dẫn Các Lệnh Git Để Đẩy File Phân Tích Lên GitHub

Thực hiện lần lượt các lệnh sau trong terminal/command prompt tại thư mục dự án của bạn:

### Step 1: Khởi tạo và thiết lập repo (nếu chưa làm)
```bash
# Khởi tạo Git trong thư mục local
git init

# (Tùy chọn) Liên kết với repository trên GitHub
git remote add origin https://github.com/ten-user-cua-ban/ten-repo.git
```

### Step 2: Lưu và Commit file markdown
```bash
# Đưa file vừa tạo vào vùng chuẩn bị (Staging Area)
git add prompt_gaitu_ipo.md

# Tạo commit lưu lại phiên bản
git commit -m "docs: add prompt design and edge case handling for IPO model"
```

### Step 3: Đẩy file lên GitHub
```bash
# Chuyển sang nhánh chính (main)
git branch -M main

# Đẩy dữ liệu lên GitHub
git push -u origin main
```