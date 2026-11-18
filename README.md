# AI Project Starter — Team AI cho dự án mới

Bộ khung làm việc, chưa phải ứng dụng chạy được. Chưa chọn đề tài, stack, mô hình hoặc ngân sách. Mọi trường [điền] cần xác nhận; không xem template là tài liệu đã hoàn thành.

## Bắt đầu trong 30 phút
1. Điền `00_control/PROJECT_BRIEF.md` với ý tưởng, người dùng, vấn đề, đầu ra MVP, dữ liệu, thời gian và ngân sách.
2. Đọc `TEAM_GUIDE_VI.md` để hiểu vai trò và trình tự làm việc.
3. Dùng prompt khởi động trong `ai-team/prompts/START.md` tại một phiên AI có quyền đọc thư mục này. Nếu AI không truy cập file, cung cấp các file đầu vào và tự lưu đầu ra.
4. Hoàn thiện PRD → yêu cầu → backlog → luồng UX → kiến trúc → một lát cắt MVP → đánh giá.
5. Theo dõi nhiệm vụ trong `00_control/TASK_BOARD.csv`; cập nhật `00_control/STATUS.md` sau mỗi vòng.

## Nguyên tắc
Bạn là người chịu trách nhiệm quyết định sản phẩm. AI là trợ lý theo vai trò; nhiều vai không đồng nghĩa nhiều nhân sự tự vận hành. Các file role là prompt, không tự tạo agent hoặc tự chạy nền. Thư mục `ai-team/` dùng để tham khảo rõ ràng, không phụ thuộc cơ chế tự nạp riêng của công cụ.

Khuyến nghị khởi đầu với 5 phiên làm việc: Product (PM + PO + BA), Delivery (Project Manager), Design (Research + Product + UX + UI), Build (Tech + Data + AI + Developer), Review (QA + Security + Ops + Analytics). Tách thêm khi khối lượng tăng.

## Nơi lưu nội dung
- `01_product_strategy/`: Product Manager — Xác định người dùng, vấn đề, giá trị và kết quả sản phẩm.
- `02_product_owner/`: Product Owner (PO) — Sắp xếp backlog, làm rõ phạm vi và đề xuất nghiệm thu.
- `03_project_management/`: Project Manager — Điều phối nhiệm vụ, tiến độ, phụ thuộc, rủi ro và bàn giao.
- `04_business_analysis/`: Business Analyst (BA) — Chuyển nhu cầu thành quy trình, quy tắc nghiệp vụ và yêu cầu kiểm thử được.
- `05_product_design/`: Product Designer — Thiết kế trải nghiệm tổng thể và kiểm chứng giải pháp cho bài toán sản phẩm.
- `06_ux_research/`: UX Researcher — Thu thập bằng chứng từ người dùng và kiểm tra giả thuyết.
- `07_ux_design/`: UX Designer — Thiết kế kiến trúc thông tin, luồng tác vụ và tương tác.
- `08_ui_design/`: UI Designer — Thiết kế giao diện, component và đặc tả bàn giao.
- `09_architecture/`: Tech Lead / Architect — Chọn kiến trúc, hợp đồng dữ liệu và quyết định kỹ thuật.
- `10_data/`: Data Engineer — Quản lý nguồn dữ liệu, chất lượng, ingestion và phiên bản.
- `11_ai/`: AI Engineer — Thiết kế pipeline AI, baseline và thí nghiệm.
- `12_engineering/`: Developer — Frontend / Backend — Xây dựng lát cắt chạy được theo hợp đồng và tiêu chí chấp nhận.
- `13_quality/`: QA / AI Evaluation — Kiểm thử chức năng và đánh giá chất lượng AI độc lập.
- `14_operations/`: DevOps / MLOps — Đóng gói, triển khai, giám sát, rollback và kiểm soát ngân sách.
- `15_security/`: Security / Privacy Reviewer — Rà soát phân quyền, dữ liệu cá nhân, bí mật và rủi ro AI.
- `16_analytics/`: Product Analytics / Growth — Đo giá trị sau thử nghiệm và đề xuất cải tiến.
- `00_control/`: brief, tình trạng hiện tại, bảng việc và quyết định chung.
- `ai-team/`: hướng dẫn vai trò, prompt giao việc và mẫu bàn giao.
- `src/`, `tests/`, `scripts/`, `configs/`: vị trí mã nguồn tương lai.
- `data/`, `evals/`, `experiments/`: dữ liệu cục bộ, tập đánh giá và thí nghiệm.
- `assets/`, `releases/`, `archive/`: thiết kế, gói phát hành và bản cũ.

`FOLDER_MAP.md` liệt kê toàn bộ file. Các CSV ban đầu chỉ có tiêu đề là bảng chưa được điền.
