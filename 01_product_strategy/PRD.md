# PRD · Kho tri thức hỗ trợ học thuật

**Bản nháp 0.2 · 18/11/2026 · TASK-002**

Chủ trì soạn thảo: Product Manager. Người rà soát đề xuất: Product Owner và Product Designer. Người có thẩm quyền nghiệm thu sản phẩm đang chờ xác nhận.

**Nguồn đầu vào** gồm [Brief ngày 18/11/2026](../00_control/PROJECT_BRIEF.md), [SRS 0.1](../04_business_analysis/SRS.md), [yêu cầu chức năng](../04_business_analysis/requirements.md), [use case](../04_business_analysis/use-cases.md) và [sổ giả định, rủi ro](../04_business_analysis/assumptions-risk-register.md). Các lựa chọn ghi “đề xuất” đang chờ người phụ trách quyết định.

## Vấn đề và bằng chứng

**FACT theo đề bài, ghi trong brief.** Giáo trình, slide, đề cương và tài liệu tham khảo của Trung tâm nằm rải rác, có nhiều phiên bản. Sinh viên và giảng viên mất thời gian tìm và đối chiếu tài liệu. Giảng viên phụ trách duyệt học liệu trước khi đưa vào Knowledge Hub. Chưa có kết quả quan sát hoặc số đo cho thấy bước nào mất nhiều thời gian nhất.

**ASSUMPTION cần kiểm chứng.** Khi gặp một khái niệm khó, sinh viên cần cả lời giải thích lẫn đoạn học liệu để tự kiểm tra. Nếu đoạn trích mở đúng vị trí trong phiên bản đang dùng cho môn học, sinh viên có thể tự giải quyết câu hỏi với ít thời gian tra cứu hơn. Đề xuất ưu tiên tình huống này trong lần thử đầu. Với giảng viên, tác vụ cần hỗ trợ là xác định chính xác phiên bản mình cho phép trợ lý sử dụng.

## Mục tiêu và cách đo

| Câu hỏi đánh giá | Phép đo | Mốc so sánh và tiêu chí |
|---|---|---|
| Sinh viên có tìm đúng nguồn nhanh hơn? | Thời gian từ lúc nhận câu hỏi đến khi mở đoạn nguồn đúng. Báo trung vị của lượt thành công và số lượt thất bại. | Đo cách tra cứu hiện tại trước khi thử MVP. Đề xuất hai lượt với câu tương đương. Mức cải thiện cần đạt sẽ chốt sau khi có mốc ban đầu và trước khi thử MVP. |
| Sinh viên có tự hoàn thành tác vụ? | Số lượt người học tự giải thích đúng ý và chỉ ra đoạn hỗ trợ, chia cho tổng số lượt được giao. | Ghi nhận lượt cần người hướng dẫn trợ giúp. So sánh cùng tiêu chí giữa cách hiện tại và MVP. Chưa có số đo hoặc ngưỡng đã duyệt. |
| Câu trả lời có đúng và có căn cứ? | Số câu đạt chia tổng số câu trong tập kiểm chứng có nhãn. Đề xuất một câu chỉ đạt khi đúng ý và nguồn hỗ trợ các nhận định học thuật. | **FACT theo đề bài: ≥80%.** Chấm trên tập tách khỏi tập phát triển. Nếu dùng đúng 30 câu như brief đề xuất, cần ít nhất 24 câu đạt. Chưa đo. |
| Chi phí và thời gian chờ có phù hợp với buổi demo? | Ghi chi phí mỗi truy vấn và độ trễ p95 trên cùng tập câu hỏi, kèm phiên bản mô hình và quy mô kho. | Đo khi có bản chạy. Nhóm cần xác nhận ngân sách và thời gian chờ chấp nhận được. |

## MVP và phạm vi

**Luồng demo đề xuất cho một môn.** Giảng viên duyệt một phiên bản học liệu. Sinh viên chọn môn, tìm học liệu, đặt câu hỏi, đọc câu trả lời rồi mở đúng đoạn nguồn. Nếu vẫn chưa hiểu, sinh viên yêu cầu giải thích đơn giản hơn hoặc gợi ý nội dung cần ôn.

| Bước | Hành vi cần quan sát được trong web app đề xuất | Đối chiếu BA |
|---|---|---|
| Chuẩn bị và duyệt học liệu | Tệp có thông tin môn, phiên bản, quyền sử dụng và trạng thái xử lý. Chỉ phiên bản đã xử lý thành công, được giảng viên duyệt và thuộc quyền người học mới xuất hiện khi tra cứu. | UC-04, UC-05 · FR-009–011. Cần BA bổ sung bước duyệt học thuật riêng sau khi nạp. |
| Tìm trong Knowledge Hub | Sinh viên chọn môn, tìm theo từ khóa, nhận ra tài liệu và phiên bản đang dùng, mở được tài liệu. | UC-02 · FR-001, FR-002, FR-008 |
| Hỏi Academic Assistant | Mỗi nhận định học thuật có dẫn nguồn. Sinh viên mở được đúng đoạn, đúng phiên bản và trang hoặc slide khi xác định được. Khi thiếu căn cứ, trợ lý chỉ rõ phần chưa thể trả lời. | UC-01 · FR-003–005, FR-014 |
| Ôn với Learning Assistant | Sinh viên nhận lời giải thích dễ hiểu hoặc gợi ý phần nên đọc tiếp có dẫn nguồn. Với bài tính điểm, trợ lý gợi ý bước tự làm và giữ lại đáp án cuối. | UC-03 · FR-006–007. Cần BA bổ sung tiêu chí cho bài tính điểm. |

Quyền truy cập phải có hiệu lực khi tìm kiếm, sinh câu trả lời, mở trích dẫn và đọc lại nội dung lưu đệm nếu có. Đề xuất hoãn lịch sử hỏi đáp dài hạn, dashboard giảng viên, cá nhân hóa theo năng lực, tích hợp LMS và điều phối đa tác tử. Quy mô một môn và mức chức năng của mỗi mô-đun vẫn là đề xuất.

**Ý tưởng đang xem xét cho lần thử với sinh viên.** Từ sơ đồ của Quân, đề xuất so sánh cách hỏi qua chat (chuyển giữa ba cách giải thích) với cách bôi đen thuật ngữ ngay trong học liệu. Cả hai thử thao tác lưu ghi chú kèm trích dẫn và mở lại đúng đoạn nguồn. Theo dõi tác vụ nào giúp sinh viên tự giải thích đúng và tìm lại căn cứ trước khi chốt tính năng cho MVP. Các phương án về đọc sách, lộ trình ôn, động lực học và cá nhân hóa được mô tả trong [định hướng giải pháp trải nghiệm](../05_product_design/solution-concept.md).

## Giải pháp và đánh đổi

| Phương án | Giá trị | Chi phí và giới hạn |
|---|---|---|
| Kho học liệu đã duyệt, tìm bằng từ khóa và bộ lọc | Người học tự mở nguồn và đối chiếu phiên bản. Đây là phương án đối chứng để đo phần giá trị AI mang lại. | Cần chuẩn hóa tài liệu và quyền truy cập. Sinh viên tự chọn đoạn và tổng hợp lời giải thích. |
| Cùng kho học liệu, bổ sung trợ lý tìm đoạn liên quan trước khi trả lời (RAG) | Hỗ trợ câu hỏi diễn đạt khác giáo trình và cho phép người học kiểm tra căn cứ ngay khi đọc. Đề xuất thử cho luồng demo. | Phát sinh chi phí mô hình và thời gian chờ. Truy xuất nhầm phiên bản, OCR sai hoặc nguồn chỉ hỗ trợ một phần đều có thể làm câu trả lời sai. |

Trước khi so sánh, dùng cùng học liệu và quyền truy cập cho hai phương án. Kiểm tra một số đoạn trích trên tệp gốc, nhất là trang chứa bảng hoặc công thức. Nếu nguồn sai hoặc thiếu, xác định lỗi ở khâu trích xuất, tìm đoạn hay sinh câu trả lời trước khi chọn mô hình hoặc công cụ khác. Tham chiếu FR-003–005, FR-011, FR-014 và NFR-001, NFR-003, NFR-008.

## Kế hoạch kiểm chứng

1. **Kiểm tra giả định về nhu cầu.** UX Researcher quan sát sinh viên thực hiện một tác vụ tra cứu thật và hỏi giảng viên cách nhận biết bản học liệu còn hiệu lực. Ghi bước thực hiện, thời gian, lần chọn nhầm phiên bản và lúc cần trợ giúp. Nếu trở ngại chính khác với giả định, xem lại tác vụ ưu tiên trước khi dựng prototype.
2. **Thử luồng với người dùng.** Product Designer cho giảng viên thử duyệt một phiên bản và cho sinh viên thử hỏi, mở nguồn rồi tự giải thích. Dùng hai câu tương đương và đổi thứ tự hai cách tra cứu giữa người tham gia để giảm ảnh hưởng do đã biết đáp án. Ghi riêng trường hợp mở đúng tệp nhưng sai đoạn. Nếu người học vẫn cần trợ giúp để tìm đoạn nguồn, chỉnh luồng và thử lại.
3. **Đánh giá chất lượng AI.** Đề xuất giảng viên xác nhận đáp án và đoạn nguồn chuẩn, QA cố định tập câu hỏi cùng quy tắc chấm trước khi chạy. Ghi số câu đạt trên tổng số câu, mức đúng của trích dẫn và nguyên nhân từng câu sai. Nếu dưới 80%, sửa và đánh giá lại với tập kiểm chứng độc lập trước khi kết luận đạt.
4. **Thử các tình huống có thể làm hỏng buổi demo.** QA kiểm tra câu hỏi thiếu nguồn, tài liệu chưa duyệt, truy cập chéo môn qua liên kết trực tiếp hoặc cache, và yêu cầu giải hộ bài tính điểm. Đề xuất dừng đưa bản thử cho người dùng khi phát hiện lộ học liệu, trích dẫn giả hoặc trả đáp án cuối cho bài tính điểm. Ghi riêng các kết quả này với điểm chính xác AI.

**Bàn giao.** PO rà phạm vi một môn và mức tối thiểu của ba mô-đun. Product Designer rà luồng duyệt và mở nguồn. BA đối chiếu hai điểm còn thiếu trong bảng phạm vi trước khi PO tách story. Các quyết định về môn mẫu, học liệu được phép dùng, người nghiệm thu, nguồn lực và cách chấm được theo dõi tại [STATUS.md](../00_control/STATUS.md). Các phép đo và thử nghiệm trên đều đang ở bước lập kế hoạch.
