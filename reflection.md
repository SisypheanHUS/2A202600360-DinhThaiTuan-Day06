## Individual Reflection — Đinh Thái Tuấn

### 1. Role

* Backend/AI Developer. Phụ trách xây dựng logic hệ thống Agent, triển khai luồng xử lý với LangGraph, tích hợp RAG và tối ưu khả năng truy xuất dữ liệu phục vụ các truy vấn thực tế.

### 2. Đóng góp cụ thể

* Xây dựng và hoàn thiện luồng hoạt động của Agent dựa trên LangGraph, đảm bảo các bước reasoning, tool-calling và phản hồi được thực hiện tuần tự, rõ ràng.
* Thiết kế và tích hợp hệ thống RAG phục vụ truy xuất dữ liệu nội bộ, bao gồm việc xử lý dữ liệu dạng JSON và tối ưu hóa truy vấn thông qua metadata.
* Triển khai các tool hỗ trợ như Web Search, kết hợp với cơ chế fallback nhằm đảm bảo hệ thống vẫn hoạt động khi dữ liệu nội bộ không đủ.
* Viết các hàm xử lý logic bằng Python để bổ trợ cho RAG (đặc biệt với các bài toán liên quan đến filtering hoặc so sánh số liệu), giúp tăng độ chính xác của kết quả.

### 3. Điểm mạnh / điểm yếu

* Mạnh: Khả năng thiết kế luồng xử lý rõ ràng, có kiểm soát. Hệ thống được xây dựng với tư duy hạn chế lỗi từ LLM thông qua việc kết hợp giữa code logic và prompt constraints.
* Yếu: Ở giai đoạn đầu, việc phân định khi nào nên dùng tool chưa tối ưu, dẫn đến hiện tượng gọi tool không cần thiết, làm tăng độ phức tạp và thời gian phản hồi.

### 4. Đóng góp khác

* Đề xuất cải tiến cấu trúc hệ thống theo hướng tách biệt rõ ràng giữa phần khởi tạo dữ liệu và phần xử lý runtime, giúp tăng hiệu năng.
* Tham gia định hướng cải thiện trải nghiệm người dùng bằng cách làm rõ luồng tương tác giữa người dùng và Agent thay vì chỉ trả lời dạng text đơn thuần.

### 5. Điều học được

* RAG không hiệu quả với các bài toán yêu cầu so sánh hoặc xử lý số liệu chính xác nếu không có thêm logic hỗ trợ. Việc kết hợp giữa vector search và xử lý bằng code là cần thiết.
* Xây dựng Agent không chỉ là vấn đề lập trình mà còn là kiểm soát hành vi của mô hình. Prompt Engineering đóng vai trò quan trọng ngang với code.
* LLM có thể dễ dàng mắc lỗi nếu không có cơ chế kiểm soát rõ ràng, đặc biệt trong các trường hợp edge case.

### 6. Nếu làm lại

* Sẽ thiết kế kiến trúc tool rõ ràng hơn ngay từ đầu, bao gồm việc chuẩn hóa schema và quy tắc sử dụng tool.
* Tích hợp giao diện người dùng sớm hơn để kiểm thử thực tế thay vì chỉ chạy thử trên môi trường dòng lệnh.
* Đầu tư nhiều hơn vào việc thiết kế guardrails để hạn chế lỗi từ LLM.

### 7. AI giúp gì / AI sai gì

* Giúp: Hỗ trợ nhanh trong việc xây dựng cấu trúc hệ thống, viết các đoạn code mẫu và đề xuất hướng triển khai LangGraph, RAG.

* Sai/mislead: Có xu hướng đưa ra kết luận sai khi gặp lỗi nhỏ trong dữ liệu hoặc logic, đồng thời dễ lạm dụng tool nếu không được kiểm soát.

* Kết luận: AI là công cụ hỗ trợ hiệu quả, nhưng cần được kiểm soát chặt chẽ thông qua thiết kế hệ thống và các ràng buộc rõ ràng.
