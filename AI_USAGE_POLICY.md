# Chính sách và Nguyên tắc Sử dụng AI (AI Usage Policy)

## 1. Quy định về Quyền kiểm soát dữ liệu (Human-in-the-Loop)
Hệ thống KHÔNG được phép ghi dữ liệu do AI sinh ra trực tiếp vào Cơ sở dữ liệu chính thức. 
* Mọi kết quả trả về từ API bắt buộc phải hiển thị trên màn hình "Preview Panel"[cite: 2].
* Người dùng phải là chốt chặn cuối cùng, thực hiện việc rà soát, chỉnh sửa (Inline Edit) và xác nhận "Lưu tất cả"[cite: 2]. Điều này đảm bảo tính chính xác của học liệu học thuật.

## 2. Cơ chế Dự phòng & Xử lý lỗi (Fallback Mechanism)
Để đảm bảo trải nghiệm người dùng không bị gián đoạn, hệ thống phải tuân thủ các quy tắc bắt lỗi sau[cite: 2]:
* **Lỗi 404/500 từ máy chủ AI:** Hệ thống không được crash. Phải hiển thị thông báo lỗi thân thiện và gợi ý người dùng sử dụng phương pháp tạo thẻ thủ công[cite: 2].
* **Lỗi cấu trúc dữ liệu:** Nếu LLM trả về chuỗi văn bản không đúng chuẩn định dạng JSON Schema yêu cầu, khối Backend phải tự động bắt lỗi (Catch error) và yêu cầu sinh lại hoặc báo cáo lỗi cho người dùng[cite: 2].

## 3. Chính sách Bảo mật Dữ liệu
* Chỉ truyền văn bản thô (raw text) đã bóc tách từ tài liệu học thuật lên máy chủ LLM[cite: 2].
* Không nhúng thông tin định danh cá nhân (PII) của người dùng vào các prompt gửi cho bên thứ ba.
