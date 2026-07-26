# Communication Matrix trong giai đoạn Khởi động

## Phần 1: Khung kiến thức chuyên sâu (Knowledge Framework)

Trong quản lý dự án theo chuẩn PMP, **Ma trận Truyền thông (Communication Matrix)** là công cụ cốt lõi thuộc quy trình Quản lý Truyền thông Dự án (Project Communications Management). Tài liệu này được phát triển bằng cách kế thừa trực tiếp dữ liệu từ bản *Phân tích các bên liên quan (Stakeholder Analysis)* ở bước trước nhằm xác định cách thức thông tin được thu thập, lưu trữ, phân phối và phản hồi một cách hiệu quả nhất.

Một Ma trận Truyền thông chuẩn PMP phải làm rõ được **5W1H**:

1. **Who (Ai):** Ai là người cần nhận thông tin và ai là người chịu trách nhiệm tạo ra thông tin.
2. **What (Cái gì):** Nội dung thông tin cụ thể là gì, ví dụ báo cáo tiến độ, tài liệu kỹ thuật, biên bản nghiệm thu.
3. **Why (Tại sao):** Mục đích của luồng truyền thông này để làm gì.
4. **When / Frequency (Khi nào / Tần suất):** Tần suất diễn ra, ví dụ hàng ngày, hàng tuần, hàng tháng hoặc theo sự kiện.
5. **Where / Channel (Ở đâu / Kênh nào):** Phương thức truyền thông, ví dụ họp trực tiếp, Email, Slack, Dashboard, công cụ quản lý dự án.
6. **How (Như thế nào):** Định dạng của thông tin, ví dụ Slide, PDF, Excel, biên bản ký duyệt.

---

# Phần 2: Bảng Ma trận Truyền thông Dự án (Project Communication Matrix)

**Tên dự án:** Phát triển Nền tảng Kỹ thuật số Tích hợp Dịch vụ Toàn diện & Trợ lý Ảo AI

**Giai đoạn:** 01 Project Initiation

**Phiên bản:** 1.0

| Loại thông tin / Cuộc họp (Communication Type) | Mục đích (Purpose) | Người gửi / Chủ trì (Owner) | Người nhận / Đối tượng (Audience) | Tần suất (Frequency) | Kênh / Phương thức (Channel / Method) | Định dạng đầu ra (Format) |
| --- | --- | --- | --- | --- | --- | --- |
| **Họp Khởi động Dự án (Project Kick-off Meeting)** | Công bố chính thức bắt đầu dự án; thống nhất mục tiêu, ranh giới phạm vi và vai trò của các bên. | Quản lý Dự án (PM) | Toàn bộ Stakeholders (Sponsor, CFO, Core Team, Trưởng phòng Vận hành) | 1 lần duy nhất (Bắt đầu dự án) | Họp trực tiếp tại văn phòng kết hợp Video Conference | Slide trình bày dự án.<br>Biên bản họp ký duyệt. |
| **Báo cáo Tiến độ Quản trị (Executive Status Report)** | Cập nhật các mốc quan trọng (Milestones), tình hình giải ngân ngân sách và rủi ro vĩ mô cho cấp quản lý. | Quản lý Dự án (PM) | Nhà tài trợ (Sponsor), Giám đốc Tài chính (CFO) | 2 tuần/lần hoặc hàng tháng | Email chính thức đính kèm link Real-time Dashboard | Biểu đồ Dashboard trực quan.<br>Văn bản PDF tóm tắt ngắn. |
| **Họp Giao ban Kỹ thuật (Daily Standup Meeting)** | Rà soát các đầu việc trong ngày, cập nhật tiến độ Sprint và phát hiện các điểm nghẽn (Blockers) kỹ thuật. | Quản lý Dự án (PM) / Tech Lead | Core Team (BA, UI/UX Designer, Developers, QA/QC) | Hàng ngày (15 phút vào đầu giờ sáng) | Họp nhanh tại khu vực làm việc hoặc qua Slack/Teams | Cập nhật trạng thái thẻ công việc trên Jira/Trello Board. |
| **Đánh giá & Trình diễn Sản phẩm (Sprint Review & Demo)** | Trình diễn phiên bản thử nghiệm như thiết kế UI/UX trên Figma, bản MVP chạy thử, Module AI Chatbot để lấy phản hồi sớm. | Quản lý Dự án (PM) & Đội ngũ thực thi | Trưởng phòng Vận hành, Đại diện người dùng, Sponsor nếu cần | 2 tuần/lần (Kết thúc mỗi Sprint) | Họp trực tuyến và chia sẻ màn hình trực tiếp sản phẩm | Link Prototype tương tác.<br>Danh sách phản hồi (Feedback Log) trên CMS/App. |
| **Họp Điều phối với Đối tác API (Vendor Sync Meeting)** | Kiểm tra tiến độ tích hợp hệ thống eKYC, cổng thanh toán và xử lý các lỗi kỹ thuật phát sinh trên môi trường Sandbox. | Tech Lead / PM | Đội ngũ kỹ thuật của công ty và đội ngũ kỹ thuật của Vendor | Hàng tuần | Gọi trực tuyến chuyên sâu (Google Meet/Zoom) | Tài liệu cập nhật API (Swagger).<br>Nhật ký sửa lỗi (Bug Log). |
| **Họp Tổng kết & Cải tiến (Sprint Retrospective)** | Nhìn nhận lại quy trình làm việc sau mỗi phân đoạn để cải tiến năng suất và giải quyết các xung đột nội bộ. | Quản lý Dự án (PM) | Core Team (BA, UI/UX, Dev, QA) | 2 tuần/lần (Sau buổi Sprint Review) | Họp nhóm tập trung kín (Internal Meeting) | Danh sách hành động cải tiến (Action Items) cho Sprint sau. |
| **Thông báo / Thay đổi Khẩn cấp (Ad-hoc / Escalation)** | Thông báo và giải quyết các sự cố nghiêm trọng như lỗi API hệ thống, thay đổi phạm vi lớn, rủi ro pháp lý eKYC. | Người phát hiện (PM/Tech Lead/Sponsor) | Các bên liên quan chịu trách nhiệm trực tiếp xử lý sự cố | Ngay khi phát sinh sự cố | Nhóm chat khẩn cấp (Zalo/Slack 24/7) kết hợp họp xử lý nhanh | Biên bản xử lý sự cố.<br>Phiếu yêu cầu thay đổi (Change Request) nếu có. |

---

## Phần 3: Nguyên tắc và Lưu ý Vận hành Truyền thông (Communication Ground Rules)

Để Ma trận Truyền thông này hoạt động trơn tru trong thực tế và tránh nhiễu thông tin, PM cần thiết lập các quy tắc ứng xử sau cho đội ngũ dự án:

### 1. Quy tắc Phản hồi (SLA Phản hồi)

- **Kênh khẩn cấp (Zalo/Slack):** Phải phản hồi trong vòng 15-30 phút trong giờ làm việc.
- **Kênh Email:** Phải phản hồi trong vòng 24 giờ kể từ khi nhận được thư.

### 2. Quản lý Lưu trữ Tập trung (Single Source of Truth)

- Tất cả tài liệu dự án (SRS, bản vẽ UI/UX Figma, biên bản nghiệm thu) phải được lưu trữ trên một thư mục dùng chung duy nhất, ví dụ Google Drive hoặc Confluence của dự án.
- Tuyệt đối không gửi file rời rạc qua chat để tránh lẫn lộn phiên bản tài liệu.

### 3. Quy trình Báo cáo Leo thang (Escalation Path)

- **Mức độ 1 (Nghẽn kỹ thuật thông thường):** Lập trình viên làm việc trực tiếp với Tech Lead/BA để xử lý trong ngày.
- **Mức độ 2 (Nguy cơ chậm mốc Milestone >3 ngày hoặc xung đột phòng ban):** Tech Lead chuyển thông tin để PM đứng ra chủ trì giải quyết.
- **Mức độ 3 (Vượt ngân sách, trễ Go-live, thay đổi tính năng cốt lõi):** PM lập hồ sơ trình lên Nhà tài trợ dự án (Sponsor) để đưa ra quyết định tối cao.

---

*Ma trận Truyền thông này là mảnh ghép quan trọng giúp chuyển hóa các chiến lược từ bản **Phân tích các bên liên quan (Stakeholder Analysis)** thành hành động giao tiếp cụ thể mỗi ngày, tạo nền tảng vững chắc cho sự phối hợp nhịp nhàng giữa các phòng ban.*
