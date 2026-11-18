# Kế hoạch kiểm thử và đánh giá AI

Trạng thái: TEMPLATE — chưa có dữ liệu dự án
Chủ trì: QA
Cập nhật: [ngày]
Nguồn đầu vào: [đường dẫn, phiên bản]

## Tiêu chí
REQ-ID/STORY-ID, metric, công thức, ngưỡng được chốt trước khi xem kết quả.

## Bộ đánh giá
Eval ID, nguồn, version, tập giữ riêng, đại diện use case và các ca khó; không điều chỉnh trên holdout.

## Rubric
Đúng/sai hoặc thang điểm có mô tả; đáp án tham chiếu do người có chuyên môn xác minh; double-review mẫu bất đồng.

## Chỉ số
Task success, tính đúng, độ bám nguồn khi áp dụng, độ trễ p50/p95, chi phí mỗi tác vụ; báo số mẫu và giới hạn.

## Regression và an toàn
Input lỗi, quyền, injection, dữ liệu nhạy cảm, fallback; test lại sau đổi prompt/model/data.

## Quyết định release
Kết quả so baseline, lỗi chặn, mức độ đại diện; đạt test chưa chứng minh hiệu quả ngoài thực tế.
