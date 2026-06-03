# Đề xuất Tích hợp Trí tuệ Nhân tạo (AI Feature Proposal)

## 1. Vấn đề thực trạng
Nút thắt lớn nhất của các ứng dụng Flashcard truyền thống là **Data Entry Bottleneck** (Sự cản trở trong khâu nhập liệu thủ công)[cite: 2]. Sinh viên mất hàng giờ để gõ lại kiến thức từ giáo trình dài hàng trăm trang.

## 2. Đề xuất Giải pháp Kỹ thuật
Tích hợp API của Mô hình Ngôn ngữ Lớn (LLM - Google Gemini) để xây dựng Module Trích xuất Tự động[cite: 2]. AI sẽ đảm nhiệm việc phân tích ngữ nghĩa, bóc tách định nghĩa, công thức cốt lõi và định dạng thành mảng JSON[cite: 2].

## 3. Đặc tả Kịch bản Sử dụng (Use Case Flow)
1. **Tiếp nhận tài liệu:** Người dùng tải lên tệp `.pdf` hoặc `.docx`[cite: 2].
2. **Cấu hình tham số:** Người dùng thiết lập số lượng thẻ tối đa và "Yêu cầu tùy chỉnh" (Custom Prompt) để AI tập trung vào vùng kiến thức cụ thể[cite: 2].
3. **Xử lý LLM:** Hệ thống chuyển đổi tệp thành raw text, đóng gói kèm tham số và gọi API[cite: 2].
4. **Hiển thị & Render:** Trả về danh sách thẻ trên Giao diện duyệt trước (Preview Panel). *Lưu ý:* Các công thức toán học/kỹ thuật được hiển thị động thông qua thư viện **KaTeX**[cite: 2].
5. **Human-in-the-loop:** Người dùng kiểm tra, chỉnh sửa thủ công và lưu vào Cơ sở dữ liệu[cite: 2].

## 4. Giá trị mang lại
Giảm thiểu 90% thời gian chuẩn bị đề cương học tập[cite: 2], cho phép người dùng dành toàn bộ năng lượng vào việc "Học" thay vì "Tạo học liệu".
