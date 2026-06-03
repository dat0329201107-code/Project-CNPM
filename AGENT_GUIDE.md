# Đặc tả Cấu hình AI Agent (AI Agent Guide)

Tài liệu này cung cấp các tiêu chuẩn để cấu hình mô hình LLM (Google Gemini) nhằm thực hiện nhiệm vụ trích xuất Flashcard.

## 1. Vai trò của Agent
AI Agent đóng vai trò là một "Chuyên gia sư phạm". Nhiệm vụ của nó là đọc các tài liệu văn bản dài, trích xuất các ý chính, định nghĩa, và công thức để tạo ra các thẻ ghi nhớ (Flashcard) súc tích, dễ hiểu.

## 2. Tiêu chuẩn Đầu ra (Output Standard)
Bắt buộc Agent phải trả về dữ liệu dưới định dạng **JSON Array**. Hệ thống Backend sẽ từ chối nhận các phản hồi có chứa Markdown text ngoài luồng.

**JSON Schema mong đợi:**
```json
[
  {
    "front": "Khái niệm kiến thức (Câu hỏi)",
    "back": "Nội dung giải thích chi tiết (Đáp án)"
  }
]
