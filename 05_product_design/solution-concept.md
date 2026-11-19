# Định hướng giải pháp trải nghiệm

Bản nháp ngày 18/11/2026. Nguồn ý tưởng là sơ đồ Quân gửi cùng ngày. Mục tiêu và ràng buộc học thuật lấy từ [brief](../00_control/PROJECT_BRIEF.md) và [PRD](../01_product_strategy/PRD.md). Các tính năng dưới đây là phương án để lựa chọn cho sản phẩm.

## Cơ hội thiết kế

Khi gặp một đoạn khó trong giáo trình, sinh viên có thể muốn hiểu đoạn đó ngay, đối chiếu lời giải thích rồi lưu lại để viết bài hoặc ôn tập. Đây là giả thuyết thiết kế. Cần quan sát liệu sinh viên có quay về nguồn và sử dụng lại ghi chú trong tác vụ tiếp theo.

## Phương án

| Thành phần trong sơ đồ | Trải nghiệm Quân đề xuất | Chi tiết cần làm rõ khi chọn triển khai |
|---|---|---|
| Academic Assistant | Chat tự do hoặc có cấu trúc, có câu hỏi gợi ý và nhập bằng giọng nói. Với chủ đề khó, dùng nút 1, 2, 3 để chuyển giữa ba cách giải thích. | Thử nhãn “1 · Định nghĩa”, “2 · Ví dụ”, “3 · Từng bước”. Đây là ví dụ về nhãn. Khi chuyển cách giải thích, giữ nguyên câu hỏi, phân biệt ví dụ minh họa với nội dung trích nguồn. |
| Learning Assistant | Bôi đen thuật ngữ để hiện giải thích tại chỗ. Tạo lộ trình từ kiến thức nền lên chủ đề đích (bottom-up) hoặc từ mục tiêu học lần về kiến thức cần ôn (top-down). | Tooltip cần giữ vị trí đọc và cho phép mở nguồn. Với lộ trình, cần xác định người học chọn mục tiêu và điểm xuất phát như thế nào. |
| Knowledge Hub | Quản lý học liệu đa phiên bản, tìm bằng ma trận lọc và tra bảng thuật ngữ. | Có thể thử lọc kết hợp môn, loại tài liệu và phiên bản. Trích dẫn cần dẫn về đúng bản đã dùng ngay cả khi có bản mới. |
| Ghi chú và hỗ trợ viết | Lưu ghi chú cùng trích dẫn, chụp ghi chú giấy để đưa vào kho. AI phân tích ghi chú để gợi ý lỗ hổng kiến thức. | Ghi chú có thể chứa ý hay hoặc dẫn chứng dùng để viết. Kiểm chứng giả thuyết “người học ghi điều mình chưa biết” bằng cách hỏi lý do lưu. Cho người học xác nhận chủ đề muốn ôn. |
| Trải nghiệm đọc | Lật trang như sách, chuyển PDF sang EPUB, xem mục lục kèm thời gian đọc ước tính cho từng mục, có “level đọc” và màn hình đôi để so sánh, đối chiếu. | Cần làm rõ “level đọc” chỉ độ khó của văn bản hay cấp độ của người đọc. Nếu chuyển định dạng, thử mở một trích dẫn từ EPUB về đúng đoạn trong PDF gốc. |
| Phân loại và phân quyền | AI tự gắn nhãn tài liệu mới nạp để hỗ trợ tổ chức kho và quy trình phân quyền. | Đề xuất dùng nhãn để gợi ý cho người quản lý. Quyền truy cập cần dựa trên vai trò, môn và phiên bản mà giảng viên đã duyệt. |
| Động lực học | Duy trì chuỗi ngày học khi mỗi ngày tạo ít nhất một ghi chú hoặc hỏi một câu. Dùng Pomodoro để bố trí giờ nghỉ, hoặc ôn một ghi chú ngẫu nhiên. | Khi thử, quan sát việc người học có đọc lại và nhớ được nội dung đã lưu. Số ngày quay lại chỉ phản ánh tần suất sử dụng. |
| Cá nhân hóa giao diện | Tùy biến giao diện, đổi bìa ghi chú, dán sticker và gắn charm. | Có thể thử trên cùng một cuốn sổ để tìm hiểu người học muốn cá nhân hóa hình thức hay dùng dấu hiệu trực quan để nhận ra từng sổ. |

## Hành trình

Hai điểm bắt đầu dẫn về cùng một tác vụ học tập. **Bắt đầu bằng câu hỏi** phù hợp khi sinh viên đã biết mình cần hỏi gì. Sinh viên mở Academic Assistant, nhập câu hỏi hoặc chọn gợi ý, đổi cách giải thích nếu cần rồi mở trích dẫn. **Bắt đầu khi đang đọc** phù hợp khi sinh viên gặp một thuật ngữ khó trong một đoạn cụ thể. Sinh viên bôi đen thuật ngữ, xem giải thích ngắn và có thể hỏi sâu hơn trong ngữ cảnh đoạn đang đọc.

Ở cả hai hướng, sinh viên có thể lưu nhận xét của mình cùng đoạn trích. Khi mở lại ghi chú để viết hoặc ôn, sinh viên cần nhận ra đâu là lời mình viết và mở lại được đoạn học liệu tương ứng trong phạm vi quyền hiện tại.

## Giải pháp chọn thử

**Đề xuất prototype để Quân rà soát.** Giữ luồng hỏi đáp có nguồn trong PRD làm mốc. Với cùng một đoạn khó, thử hai biến thể: (A) bắt đầu từ chat và chuyển giữa ba cách giải thích, (B) bắt đầu bằng bôi đen thuật ngữ khi đang đọc. Cả hai cho phép lưu ghi chú kèm trích dẫn. Hướng A cần ba lời giải thích nhất quán về nội dung. Hướng B cần nhận diện đúng đoạn được chọn và giữ vị trí đọc khi đóng tooltip.

Giao cho người học một đoạn tài liệu, yêu cầu họ giải thích khái niệm bằng lời của mình, rồi dùng ghi chú để chỉ lại bằng chứng. Ghi nhận cách giải thích họ thực sự dùng, số lượt cần trợ giúp, thời gian mở đúng đoạn và trường hợp ghi chú mất nguồn. Nếu người học chỉ dùng một cách giải thích hoặc vẫn phải dò lại tài liệu, xem lại thiết kế tương ứng trước khi thêm vào backlog triển khai. Chưa có kết quả thử nghiệm.
