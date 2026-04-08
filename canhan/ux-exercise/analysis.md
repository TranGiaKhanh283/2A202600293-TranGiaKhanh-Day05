# UX exercise — Vietnam Airlines Chatbot NEO

## Sản phẩm: Vietnam Airlines — Chatbot NEO

## 4 paths

### 1. AI đúng
- User hỏi các tác vụ có cấu trúc như: tra cứu mã đặt chỗ, giờ bay, điều kiện check-in.
- NEO phản hồi nhanh, thường trả kết quả theo form/menu có sẵn.
- UI có quick-reply và card thông tin, giúp hoàn thành tác vụ cơ bản tương đối mượt.

### 2. AI không chắc
- Khi user hỏi mơ hồ hoặc nhiều ý cùng lúc, bot thường trả menu chung hoặc yêu cầu chọn lại chủ đề.
- Hệ thống chưa hiển thị mức độ tự tin (confidence), nên user không biết bot đang "đoán" hay "chắc chắn".
- Trải nghiệm là bot vẫn trả lời như bình thường, nhưng chất lượng gợi ý giảm rõ rệt.

### 3. AI sai
- Với câu hỏi phức tạp (hoàn/đổi vé có nhiều điều kiện), bot có thể trả lời thiếu ngữ cảnh hoặc chưa đúng trường hợp.
- User khó biết đâu là phần sai nếu không tự đối chiếu quy định trên web hoặc hỏi tổng đài.
- Recovery flow còn yếu: chưa có nút "báo sai/cần sửa", user thường phải gõ lại từ đầu hoặc thoát ra kênh hỗ trợ khác.

### 4. User mất niềm tin
- Sau vài lần không giải quyết được nhu cầu, user có xu hướng bỏ chatbot và chuyển sang tổng đài/nhân viên thật.
- Fallback sang con người có nhưng chưa đủ nổi bật trong toàn bộ hành trình chat.
- Nếu thiếu cơ chế khôi phục niềm tin (xin lỗi, chuyển tuyến nhanh, xác nhận xử lý), user dễ đánh giá bot "chỉ để tham khảo".

## Path yếu nhất: Path 3
- Điểm yếu lớn nhất là lúc AI sai: user không có công cụ sửa trực tiếp trong hội thoại.
- Từ sai -> sửa hiện tốn nhiều thao tác và thiếu phản hồi "hệ thống đã học từ lỗi này chưa".
- Khi lỗi lặp lại, niềm tin giảm nhanh và user rời bỏ kênh chatbot.

## Gap marketing vs thực tế
- Marketing hứa "hỗ trợ 24/7, thông minh như nhân viên thật", tạo kỳ vọng bot xử lý tốt cả tình huống phức tạp.
- Thực tế NEO làm tốt tác vụ đơn giản, nhưng với case nhiều điều kiện thì còn loop menu hoặc trả lời chưa đúng ngữ cảnh.
- Gap lớn nhất: thông điệp marketing chưa làm rõ giới hạn khi AI không chắc hoặc khi AI sai.


- As-is: User hỏi -> bot trả lời/menu -> nếu sai user gõ lại hoặc tự chuyển kênh khác.
- To-be:
  - Hiển thị confidence badge (`Cao/Trung bình/Thấp`) cho câu trả lời quan trọng.
  - Thêm nút inline: `Thông tin này chưa đúng` và `Chuyển nhân viên`.
  - Hotline/live-agent luôn hiển thị ở footer cuộc chat.
  - Khi user sửa, bot xác nhận đã ghi nhận feedback: "Cảm ơn bạn, chúng tôi đã ghi nhận để cải thiện."
