# Escalation Process

Tài liệu quy định quy trình leo thang vấn đề trong giai đoạn thực thi dự án.

## Mục tiêu

- Xác định rõ khi nào một issue cần escalation.
- Rút ngắn thời gian xử lý blocker có tác động lớn đến scope, schedule, cost hoặc quality.
- Tránh tình trạng team giữ vấn đề quá lâu mà không có quyết định cấp cao.

## Ngưỡng escalation

- Issue có nguy cơ làm trễ milestone quan trọng.
- Blocker không được xử lý sau thời gian SLA đã thống nhất.
- Dependency bên ngoài không có phản hồi đúng hạn.
- Chi phí thực tế có nguy cơ vượt cost baseline.
- Quyết định vượt thẩm quyền của PM hoặc PO.
- Rủi ro chuyển thành sự cố thực tế có tác động cao.

## Ma trận escalation

| Cấp | Điều kiện kích hoạt | Người xử lý | SLA phản hồi | Kênh |
| --- | --- | --- | --- | --- |
| Level 1 | Issue trong phạm vi team | Team Lead / Scrum Master | Trong ngày | Daily / Slack / Teams |
| Level 2 | Ảnh hưởng milestone hoặc nhiều team | PM / PO | 24 giờ | Project sync / Email |
| Level 3 | Ảnh hưởng ngân sách, scope hoặc cam kết với khách hàng | Sponsor / Steering Committee | 48 giờ | Steering meeting / Escalation memo |

## Mẫu ghi nhận escalation

| ID | Issue liên quan | Lý do escalation | Cấp escalation | Owner | Deadline | Kết quả |
| --- | --- | --- | --- | --- | --- | --- |
| ESC-001 | ISS-001 |  | Level 1 / 2 / 3 |  | YYYY-MM-DD |  |
