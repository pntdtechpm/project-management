# 02-PROJECT-PLANNING: BÀI 09 - COMMUNICATION PLAN (KẾ HOẠCH QUẢN LÝ THÔNG TIN LIÊN LẠC)

**Tên tài liệu:** `02-project-planning/communication-plan.md`  
**Chủ đề:** Kế hoạch Quản lý Thông tin liên lạc (Project Communications Management Plan) chuẩn PMP & Agile  
**Đối tượng hướng tới:** Project Manager (PM), Product Owner (PO), Scrum Master, khách hàng (Clients), Ban Giám đốc và toàn bộ đội ngũ dự án.

---

## I. Khung kiến thức chuẩn PMP (PMBOK® Guide - 6th Edition)

### 1. Định nghĩa & bản chất của Communication Plan

Theo chuẩn *PMBOK® Guide - 6th Edition*, quy trình **10.1: Plan Communications Management**, **Communications Management Plan** là một cấu phần của kế hoạch tổng thể, xác định nhu cầu thông tin của các bên liên quan (Stakeholders) và cách thức thông tin sẽ được thu thập, tạo lập, phân phối, lưu trữ, truy xuất và quản lý hiệu quả.

**Tầm quan trọng cốt lõi:** Các nghiên cứu của PMI thường nhấn mạnh rằng PM dành phần lớn thời gian để giao tiếp. Thất bại trong giao tiếp là một trong những nguyên nhân hàng đầu dẫn đến hiểu lầm về phạm vi, trễ hạn tiến độ, xung đột lợi ích và quyết định sai thời điểm.

Communication Plan không chỉ là danh sách cuộc họp. Đây là hệ thống quản trị thông tin giúp đúng người nhận đúng nội dung, đúng cấp độ chi tiết, đúng kênh và đúng thời điểm.

### 2. Các cấu phần kỹ thuật trong giao tiếp PMP

Để xây dựng một kế hoạch truyền thông khoa học, PM cần làm rõ các yếu tố:

- **Communication Requirements (Nhu cầu thông tin):** Ai cần thông tin gì? Khi nào họ cần? Tại sao họ cần thông tin đó? Thông tin đó hỗ trợ quyết định nào?
- **Communication Technology (Công nghệ giao tiếp):** Các công cụ được sử dụng như Email, Slack, Microsoft Teams, Jira, Confluence, SharePoint, dashboard BI hoặc họp trực tiếp.
- **Communication Models (Mô hình giao tiếp):** Cơ chế *Encode -> Transmit -> Decode -> Acknowledge -> Feedback* giúp PM hiểu thông tin có thể bị nhiễu (Noise) ở đâu.
- **Communication Methods (Phương thức giao tiếp):** Cách phân phối thông tin tùy theo mức độ khẩn cấp, độ phức tạp và nhóm người nhận.

Các phương thức giao tiếp chính:

- **Interactive Communication (Giao tiếp tương tác):** Trao đổi đa chiều, thời gian thực, phù hợp với vấn đề phức tạp hoặc cần phản hồi ngay. Ví dụ: họp trực tiếp, điện thoại, video call, workshop.
- **Push Communication (Giao tiếp đẩy):** Gửi thông tin một chiều tới người nhận. Ví dụ: email báo cáo, memo, thông báo release, biên bản họp.
- **Pull Communication (Giao tiếp kéo):** Lưu trữ thông tin tại một nơi trung tâm để người nhận tự truy cập khi cần. Ví dụ: Jira Board, Confluence Wiki, SharePoint, dashboard dự án.

### 3. Công thức tính số lượng kênh giao tiếp

Để thấy mức độ phức tạp khi quy mô team tăng lên, PMP sử dụng công thức tính số lượng kênh giao tiếp tiềm năng:

```text
Số kênh giao tiếp = n x (n - 1) / 2
```

Trong đó `n` là số lượng stakeholders hoặc thành viên tham gia dự án.

Ví dụ:

- Team 5 người có `5 x 4 / 2 = 10` kênh giao tiếp.
- Team 10 người có `10 x 9 / 2 = 45` kênh giao tiếp.

**Lưu ý thực chiến:** Đây là lý do quy mô team Agile lý tưởng thường được giữ nhỏ. Khi số lượng người tăng, chi phí giao tiếp tăng theo cấp số lớn hơn tuyến tính, làm tăng nguy cơ nhiễu thông tin, họp quá nhiều và quyết định chậm.

---

## II. Ví dụ & minh họa thực tế

### Ví dụ: Ma trận Kế hoạch Truyền thông cho Dự án "Epic Center"

Dưới đây là bảng kế hoạch chi tiết cho dự án phát triển Module eKYC & Ví, phân loại theo đối tượng nhận tin, tần suất và phương thức thực hiện.

| Loại sự kiện / báo cáo | Mục đích | Tần suất | Phương thức | Người gửi (Sender) | Người nhận (Receiver) |
| --- | --- | --- | --- | --- | --- |
| **Daily Standup** *(Agile)* | Cập nhật tiến độ 24h qua, kế hoạch 24h tới và các điểm nghẽn (Impediments). | Hàng ngày, 15 phút | Interactive (họp trực tiếp/Teams) | Dev Team, Scrum Master | Toàn bộ Project Team |
| **Sprint Review / Demo** | Trực quan hóa sản phẩm tăng trưởng (Increment) và lấy phản hồi kiểm thử từ Business. | Cuối mỗi Sprint, 2 tuần | Interactive (demo hệ thống thật) | Dev Team, PO | Stakeholders, Ban Giám đốc, QA |
| **Báo cáo tiến độ dự án (Status Report)** | Cập nhật các chỉ số sức khỏe dự án, rủi ro lớn và trạng thái các milestone. | Hàng tháng / hàng quý | Push (email kèm PDF hoặc dashboard link) | Project Manager (PM) | Project Sponsor, Steering Committee |
| **Tài liệu kỹ thuật & API (Architecture Document)** | Tra cứu cấu trúc hệ thống, tài liệu tích hợp webhook ngân hàng. | Cập nhật khi có thay đổi | Pull (Confluence Wiki) | Tech Lead / Solution Architect | Developers, đối tác ngân hàng |
| **Biên bản quyết định thay đổi baseline** | Ghi nhận quyết định thay đổi phạm vi, tiến độ, ngân sách hoặc kiến trúc quan trọng. | Khi phát sinh | Push + Acknowledge | PM / PO | Sponsor, Tech Lead, QA Lead, Operations |

### Ví dụ: Nguyên tắc chọn kênh giao tiếp

| Tình huống | Kênh nên dùng | Lý do |
| --- | --- | --- |
| Bug nhỏ trong Sprint | Slack/Teams channel của team | Nhanh, ít hình thức, không làm nhiễu stakeholder ngoài team |
| Thay đổi nghiệp vụ ảnh hưởng scope | Workshop hoặc họp tương tác | Cần hỏi đáp, làm rõ acceptance criteria và tác động |
| Quyết định đổi deadline hoặc ngân sách | Email chính thức + biên bản phê duyệt | Cần bằng chứng, audit trail và xác nhận của người có thẩm quyền |
| Tài liệu API dùng lâu dài | Confluence / Wiki | Cần truy xuất, versioning và cập nhật tập trung |
| Trạng thái tổng quan cho lãnh đạo | Dashboard Đỏ/Vàng/Xanh | Ngắn gọn, định hướng quyết định, tránh quá tải chi tiết |

---

## III. Case study dẫn chứng thực tế

### Hội chứng quá tải email và thảm họa lệch pha thông tin tại dự án khởi động hệ thống eKYC

**Bối cảnh:** Một dự án tích hợp module eKYC vào ứng dụng Epic Center có sự tham gia của 3 bên: đội Dev nội bộ, đối tác cung cấp giải pháp AI Core và khối Kiểm toán Bảo mật của ngân hàng liên kết. PM không lập Communication Plan mà mặc định: *"Có việc gì cứ email cc tất cả mọi người"*.

**Vấn đề phát sinh:**

1. **Nhiễu thông tin (Information Overload):** Mỗi ngày có hơn 100 email trao đổi về các lỗi kỹ thuật nhỏ, được cc cho cả Ban Giám đốc và đội kiểm toán. Các email quan trọng về thay đổi cấu trúc bảo mật API bị chìm trong luồng thông tin.
2. **Hiểu lầm nghiêm trọng:** Đội Kiểm toán bảo mật nghĩ rằng Dev Team đã nắm tiêu chuẩn mã hóa dữ liệu mới gửi qua email từ tuần trước. Trong khi đó, Dev Lead nghĩ đó chỉ là email thảo luận chung nên bỏ qua.
3. **Tác động:** Đến ngày nghiệm thu, hệ thống bị đánh trượt vì không tuân thủ yêu cầu an toàn thông tin, khiến dự án chậm Go-live 1.5 tháng.

**Giải pháp khắc phục:**

1. Thiết lập lại Communication Plan với luồng kênh rõ ràng: lỗi kỹ thuật thảo luận trên Slack kênh `#dev-ekyc`, tài liệu kỹ thuật đưa lên Confluence, quyết định thay đổi lớn mới dùng email chính thức gửi đích danh.
2. Bắt buộc áp dụng quy trình **xác nhận chủ động (Acknowledge)** đối với các thông tin làm thay đổi baseline, tiêu chuẩn bảo mật, API contract hoặc điều kiện nghiệm thu.
3. Tạo trang "Decision Log" để mọi quyết định quan trọng có owner, ngày hiệu lực, người phê duyệt và tác động liên quan.

---

## IV. Tips & điều lưu ý thực chiến cho PM/PO

### 1. Áp dụng nguyên tắc "đúng người - đúng việc - đúng lúc"

Đừng kéo Ban Giám đốc vào các cuộc họp kéo dài 2 tiếng để thảo luận lỗi cú pháp backend. Họ thường cần dashboard ngắn gọn dạng Đỏ/Vàng/Xanh, top risks, quyết định cần phê duyệt và tác động kinh doanh.

Ngược lại, đừng chỉ gửi một email chung chung cho Dev Team về thay đổi nghiệp vụ lớn từ Product Owner. Với thay đổi có tác động tới scope hoặc kiến trúc, cần họp tương tác để giải thích bản chất, trả lời câu hỏi và chốt acceptance criteria.

### 2. Quản lý kỳ vọng bằng Information Radiators

Sử dụng các bảng Kanban trực quan như Jira hoặc Trello, dashboard milestone và burndown/burnup chart. Đây là phương thức **Pull Communication** hiệu quả, giúp stakeholder tự xem trạng thái dự án mà không phải liên tục hỏi PM.

### 3. Lưu ý giao tiếp đa văn hóa và làm việc từ xa

Khi làm việc từ xa, thiếu ngôn ngữ cơ thể khiến xung đột dễ xảy ra qua chat text. PM/Scrum Master nên:

- Khuyến khích bật camera trong các buổi họp quan trọng
- Chốt cuộc họp bằng meeting minutes ngắn
- Ghi rõ decision, action item, owner và deadline
- Tránh dùng từ mơ hồ như "sớm", "gấp", "xử lý nhanh" nếu không có thời hạn cụ thể
- Tôn trọng múi giờ và khung giờ tập trung của team

### 4. Thiết lập quy tắc escalation rõ ràng

Communication Plan cần chỉ rõ vấn đề nào xử lý trong team, vấn đề nào báo PM, và khi nào phải escalation lên Sponsor hoặc Steering Committee. Nếu không có ngưỡng escalation, team dễ rơi vào hai cực đoan: hoặc giấu vấn đề quá lâu, hoặc đẩy mọi việc lên cấp trên.

---

## V. Template Communication Plan nên dùng

| Trường thông tin | Nội dung cần có |
| --- | --- |
| Stakeholder Group | Nhóm nhận thông tin: Sponsor, PMO, Dev Team, QA, Vendor, Client |
| Information Needs | Họ cần biết thông tin gì và để ra quyết định nào |
| Communication Objective | Mục đích: cập nhật, xin phê duyệt, cảnh báo, đào tạo, alignment |
| Message Format | Dashboard, email, meeting minutes, report, demo, wiki page |
| Communication Method | Interactive, push hoặc pull |
| Channel / Tool | Teams, Slack, Email, Jira, Confluence, SharePoint |
| Frequency | Hàng ngày, hàng tuần, mỗi Sprint, theo milestone hoặc khi phát sinh |
| Sender / Owner | Người chịu trách nhiệm tạo và gửi thông tin |
| Receiver | Người nhận hoặc nhóm nhận thông tin |
| Required Response | Có cần acknowledge, approve, comment hoặc chỉ informed |
| Storage Location | Nơi lưu trữ chính thức để truy xuất sau này |
| Escalation Rule | Khi nào cần chuyển cấp và chuyển cho ai |
| Confidentiality Level | Công khai nội bộ, hạn chế, bảo mật, chỉ lãnh đạo |

---

## VI. Tài liệu & nguồn tham khảo

### 1. Chuẩn quốc tế & sách gối đầu giường

- *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) - 6th Edition*, Chapter 10: Project Communications Management.
- *Project Communications Management in Action* - Frank P. Saladis.

### 2. Blog quản trị & Agile toàn cầu

- Atlassian Guide: *How to create a project communication plan that actually works*.
- PMI.org: *Art of Communication in Agile Project Frameworks*.

### 3. Video / YouTube hữu ích

- Search keyword: *"Project Communication Plan - PMP Exam Prep Tutorial"*.
- Search keyword: *"How to manage communication in remote software teams"*.
