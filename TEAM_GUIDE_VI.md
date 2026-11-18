# Hướng dẫn vận hành team AI

## 1. Chọn mô hình làm việc
Đây là mô hình tổ chức đề xuất cho dự án nhỏ, không phải quy định bắt buộc về chức danh. Đủ trách nhiệm không có nghĩa cần thuê đủ người hoặc mở đồng thời 16 agent.

Bạn giữ quyền quyết định mục tiêu, người dùng, ưu tiên, ngân sách và chấp nhận đánh đổi. AI có thể nghiên cứu, soạn thảo, thiết kế, viết code, kiểm tra và đề xuất; bằng chứng người dùng và kết quả thực nghiệm vẫn phải được thu thập thực.

Bắt đầu với 5 phiên: Product, Delivery, Design, Build, Review. Một phiên có thể đổi vai theo nhiệm vụ nhưng phải nêu rõ vai đang dùng. Khi review việc quan trọng, nên dùng phiên riêng với đầu vào gốc để giảm xu hướng đồng ý với bản nháp. Nhiều AI cùng đồng ý không phải xác nhận độc lập của thực tế.

## 2. Phân biệt trách nhiệm
| Vai trò | Câu hỏi chính | Đầu ra chủ đạo |
|---|---|---|
| Product Manager | Làm cho ai, giải quyết gì, giá trị nào? | PRD, outcome, phạm vi MVP |
| PO | Việc nào trước, thế nào là chấp nhận được? | Backlog, acceptance criteria, nghiệm thu |
| Project Manager | Ai làm, khi nào, phụ thuộc gì, đang tắc đâu? | Kế hoạch, task board, rủi ro |
| BA | Hệ thống phải hoạt động theo quy tắc nào? | Quy trình, yêu cầu, ngoại lệ |
| Product Designer | Giải pháp trải nghiệm nào tạo giá trị? | Concept, hành trình, kế hoạch thử |
| UX Researcher | Có bằng chứng gì về người dùng? | Research plan, findings |
| UX Designer | Người dùng hoàn thành tác vụ thế nào? | IA, user flow, wireframe |
| UI Designer | Giao diện và tương tác cụ thể ra sao? | UI spec, component, states |
| Tech Lead | Xây hệ thống ra sao? | Kiến trúc, API, ADR |
| Data Engineer | Dữ liệu từ đâu, chất lượng và quyền dùng? | Catalog, pipeline, version |
| AI Engineer | AI có tạo giá trị hơn baseline? | AI spec, thí nghiệm |
| Developer | Biến yêu cầu thành phần mềm thế nào? | Code, test, hướng dẫn chạy |
| QA / Evaluation | Có hoạt động đúng và đạt ngưỡng? | Eval plan, test report |
| MLOps | Phát hành và vận hành ổn định thế nào? | Runbook, monitoring, rollback |
| Security Reviewer | Dữ liệu và hành động có được kiểm soát? | Threat/risk review |
| Analytics | Người dùng thực sự được lợi gì? | Measurement plan, kết quả |

PM sản phẩm sở hữu PRD; PO sở hữu backlog; BA sở hữu chi tiết yêu cầu; Project Manager sở hữu lịch và bảng việc. Dùng ID liên kết, tránh duy trì bốn bản mô tả khác nhau. Product Designer điều phối trải nghiệm tổng thể; Research, UX, UI là các chuyên môn có thể do cùng một người đảm nhiệm.

## 3. Thực hiện theo giai đoạn
| Giai đoạn | Chủ trì | Đầu ra | Điều kiện chuyển tiếp |
|---|---|---|---|
| 0 — Định hình | Bạn + Product Manager | Brief, PRD nháp | Có người dùng, vấn đề, tác vụ MVP và giới hạn |
| 1 — Khám phá | Research + BA + Product Designer | Bằng chứng, yêu cầu, concept | Phân biệt rõ đã biết và giả thuyết; có kế hoạch thử |
| 2 — Phạm vi | PO + Project Manager | Backlog, kế hoạch vòng | Một lát cắt có tiêu chí kiểm chứng được |
| 3 — Thiết kế | UX/UI + Tech + Data + QA | Flow, UI spec, kiến trúc, dữ liệu, eval plan | Hợp đồng và cách kiểm tra đủ rõ để xây |
| 4 — Xây | AI Engineer + Developer | Baseline, lát cắt chạy được | Demo được luồng chính, xử lý lỗi thiết yếu |
| 5 — Kiểm chứng | QA + Security + bạn | Test/eval và review thực | Đạt ngưỡng đã chốt, biết giới hạn, lỗi chặn được xử lý |
| 6 — Thử nghiệm sử dụng | Ops + Analytics + PM | Bản thử, quan sát, phản hồi | Có monitoring, rollback, phạm vi sử dụng phù hợp |

Quay lại bước trước khi bằng chứng bác bỏ giả định. Không cần điền mọi template trước khi code: chỉ hoàn thiện tài liệu cần cho lát cắt sắp làm. Một dự án học thuật cần mô tả tập đánh giá, rubric và nguồn; một sản phẩm cần thêm kiểm chứng giá trị với người dùng.

## 4. Cách giao một việc cho AI
Mở thư mục dự án trong môi trường AI có thể đọc/ghi file, hoặc gửi đúng các file liên quan trong hội thoại. Dán prompt START ở lần đầu. Mỗi lượt sau dùng mẫu TASK: một mục tiêu, một owner, đầu vào cụ thể, đầu ra cụ thể, tiêu chí hoàn tất. Không yêu cầu “hãy làm cả team và hoàn thiện toàn bộ sản phẩm” trong một lượt.

Ví dụ khi đã có brief:

> Đóng vai Product Manager. Đọc AGENTS.md, 00_control/PROJECT_BRIEF.md và ai-team/roles/product-manager.md. Viết 01_product_strategy/PRD.md bản nháp, gồm vấn đề, người dùng, một tác vụ MVP, non-goals và cách đo giá trị. Mọi giả định phải ghi ASSUMPTION. Chưa lựa chọn stack. Bàn giao cho PO và BA; nêu tối đa 5 điểm cần tôi xác nhận.

Tiếp theo:

> Đóng vai BA. Đọc PRD và role business-analyst. Viết requirements.md, làm rõ luồng chính, ngoại lệ, quyền và tiêu chí Given/When/Then. Nối các yêu cầu bằng REQ-ID. Không tự mở rộng phạm vi.

Sau đó:

> Đóng vai PO. Từ PRD và requirements, tạo tối đa 8 story cho MVP trong backlog.csv, sắp xếp theo giá trị, rủi ro và phụ thuộc. Mỗi story có acceptance criteria và reviewer. Chỉ đề xuất Ready nếu đủ thông tin.

Khi xây:

> Đóng vai Developer. Thực hiện [STORY-ID] đã Ready. Đọc API contract, UI spec, tiêu chí và mã hiện có. Xây một lát cắt nhỏ, chạy kiểm tra phù hợp, ghi lệnh và kết quả thực. Không nói đã kiểm thử nếu chưa chạy.

Khi tiếp tục ở phiên mới, dùng CONTINUE.md. Khi kiểm tra, dùng REVIEW.md và chỉ cung cấp input/output cần thiết.

## 5. Nhịp làm việc mỗi phiên
1. Delivery đọc STATUS và TASK_BOARD, chọn tối đa 1–3 việc đủ điều kiện.
2. Owner thực hiện từng việc; lưu output và bàn giao.
3. Reviewer kiểm tra với tiêu chí và nguồn gốc, ghi PASS/REWORK/BLOCKED.
4. Owner sửa lỗi cần thiết. Quá 2 vòng vẫn bất đồng thì tóm tắt điểm cần người phụ trách quyết định.
5. Delivery cập nhật trạng thái, phụ thuộc và việc kế tiếp; bạn xem demo hoặc thay đổi cụ thể.

Không chờ AI tự hoạt động sau khi kết thúc hội thoại: bộ khung này chưa có bộ thực thi nền, lịch chạy hoặc tích hợp API.

## 6. Khi cần nhiều agent chạy song song
Chỉ triển khai khi môi trường hỗ trợ và bạn yêu cầu. Người điều phối tạo task độc lập, chỉ rõ file được ghi và reviewer. Ví dụ sau khi chốt PRD, Research chuẩn bị phỏng vấn trong 06_ux_research/ và Tech khảo sát kiến trúc trong 09_architecture/; kết luận phải quay về đối chiếu chung. Không chạy UI cuối cùng khi flow còn thay đổi lớn.

Một agent ghi một file tại một thời điểm. Với code, dùng nhánh/worktree riêng nếu đã có git, sau đó review và hợp nhất. Chỉ người điều phối cập nhật STATUS, TASK_BOARD, DECISIONS. Nếu chưa có subagent, chạy tuần tự cùng các role; không cần cài framework để bắt đầu.

## 7. Kiểm soát dự án AI
- Đặt baseline trước; dùng AI vì có lợi ích kiểm chứng được.
- Chốt tập dữ liệu, rubric và ngưỡng trước khi tối ưu; giữ holdout ngoài vòng chỉnh prompt.
- Theo dõi code + model + prompt + data version cho mỗi run; lưu chất lượng, latency và chi phí thực.
- Không áp một con số “accuracy” chung cho mọi tác vụ. Nếu dùng 80%, phải định nghĩa một ca đúng là gì, mẫu số, độ đại diện và người chấm.
- Với hỏi đáp tài liệu, đánh giá riêng độ đúng, độ bám nguồn, nguồn trích dẫn và khả năng nói chưa đủ thông tin.
- Không đưa secrets hoặc dữ liệu cá nhân thô vào prompt/tài liệu. Kiểm tra quyền nguồn dữ liệu trước ingestion.
- Trước release thật: lỗi chặn, rollback, ngân sách và quyền truy cập phải có người chịu trách nhiệm.

## 8. Gợi ý vòng đầu 5 buổi
Đây là nhịp tham khảo, không phải ước lượng hoàn thành mọi dự án.

| Buổi | Kết quả |
|---|---|
| 1 | Điền brief; PRD một tác vụ; liệt kê giả định |
| 2 | Thu thập bằng chứng ban đầu; yêu cầu và backlog |
| 3 | Flow/wireframe; phương án kiến trúc và dữ liệu; eval plan |
| 4 | Một baseline hoặc prototype có thể thử |
| 5 | Demo, kiểm tra, ghi phát hiện; chọn tiếp tục/sửa/thu hẹp |

Nếu thiếu dữ liệu hoặc chưa tìm được người dùng, dùng buổi đó để giải quyết điểm thiếu; không tạo findings giả cho đủ lịch.
