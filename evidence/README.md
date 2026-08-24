# Phân tích kết quả RAGAS: So sánh Prompt V1 và Prompt V2

## 1. Bảng so sánh chỉ số

| Chỉ số | Prompt V1 | Prompt V2 | Kết quả |
| :--- | :---: | :---: | :---: |
| **Faithfulness** | **0.9614** | 0.9283 | V1 cao hơn |
| **Answer Relevancy** | **0.9097** | 0.8579 | V1 cao hơn |
| **Context Recall** | **1.0000** | **1.0000** | Bằng nhau |
| **Context Precision** | **0.9483** | 0.9450 | V1 cao hơn |

## 2. Phân tích chi tiết

- **Độ trung thực (Faithfulness):** Prompt V1 (0.9614) nhỉnh hơn V2 (0.9283) do quy định chặt chẽ việc chỉ sử dụng thông tin trong ngữ cảnh được cung cấp, giúp mô hình hạn chế tối đa việc tự suy diễn ngoài tài liệu.
- **Độ liên quan câu trả lời (Answer Relevancy):** Prompt V1 (0.9097) cao hơn rõ rệt so với V2 (0.8579). Việc yêu cầu trả lời trực tiếp và ngắn gọn giúp câu trả lời đi thẳng vào trọng tâm câu hỏi, tránh dài dòng.
- **Độ phủ và độ chính xác ngữ cảnh (Context Recall & Precision):** Cả hai phiên bản đều dùng chung hệ thống truy xuất FAISS nên khả năng tìm kiếm tài liệu tương đương nhau (Context Recall đạt tuyệt đối 1.0).

## 3. Kết luận

Prompt V1 mang lại hiệu quả tổng thể tốt hơn Prompt V2, đặc biệt là ở tính chính xác và độ liên quan của câu trả lời, phù hợp để triển khai trong hệ thống hỏi đáp thực tế.
