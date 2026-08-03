# 02-PROJECT-PLANNING: BÀI 07 - CAPACITY PLANNING (KẾ HOẠCH SỨC CHỨA/NĂNG LỰC ĐỘI NGŨ)

**Tên tài liệu:** `02-project-planning/capacity-planning.md`  
**Chủ đề:** Kế hoạch Sức chứa & Quản lý Năng lực Đội ngũ (Capacity Planning) trong Agile/Hybrid  
**Đối tượng hướng tới:** Project Manager (PM), Product Owner (PO), Scrum Master, Tech Lead và PMO.

---

## I. Khung kiến thức chuẩn PMP (PMBOK® Guide - 6th Edition) & Agile

### 1. Định nghĩa & bản chất của Capacity Planning

Theo chuẩn PMP phối hợp cùng *Agile Practice Guide*, **Capacity Planning (Lập kế hoạch Sức chứa)** là quá trình xác định khối lượng công việc thực tế, tính bằng giờ công hoặc Story Points, mà đội ngũ dự án có thể đảm nhận trong một khoảng thời gian cụ thể như Sprint hoặc Phase mà không gây ra tình trạng quá tải (Burnout).

**Sự khác biệt cốt lõi với Resource Allocation:**

- **Resource Allocation (Phân bổ nguồn lực):** Chỉ định **ai** làm **việc gì**, thường gắn với giao task, phân vai hoặc phân bổ nhân sự vào work package.
- **Capacity Planning (Kế hoạch sức chứa):** Tính toán xem **đội ngũ có bao nhiêu thời gian/năng lực thực tế** để làm việc sau khi đã trừ đi các hao phí vận hành như họp, hỗ trợ, nghỉ phép, onboarding và xử lý việc phát sinh.

Nói cách khác, Resource Allocation trả lời câu hỏi "giao cho ai", còn Capacity Planning trả lời câu hỏi "team thực sự có đủ sức làm bao nhiêu".

### 2. Các chỉ số đo lường năng lực trong Agile & Hybrid

Để tính toán sức chứa một cách khoa học, PM/Scrum Master cần nắm vững 3 chỉ số:

- **Total Available Hours (Tổng giờ danh nghĩa):** Tổng số giờ làm việc lý thuyết. Ví dụ: 8 tiếng/ngày x 5 ngày = 40 tiếng/tuần/người.
- **Focus Factor (Hệ số tập trung):** Tỷ lệ phần trăm thời gian thực tế một thành viên dành cho việc phát triển sản phẩm/dự án như code, test, design hoặc review sau khi trừ thời gian "chết" như họp hành, email, hỗ trợ kỹ thuật đột xuất và context switching. Hệ số này thường dao động từ **0.65 đến 0.80**.
- **Historical Velocity (Vận tốc lịch sử):** Số lượng Story Points trung bình mà team hoàn thành qua các Sprint trước đó. Chỉ số này được dùng làm căn cứ quy đổi năng lực và không nên dùng như KPI cá nhân.

### 3. Mối liên hệ với quản lý tiến độ PMP

Trong PMBOK, việc không tính toán đúng Capacity sẽ trực tiếp dẫn đến ước tính sai thời lượng hoạt động (**Estimate Activity Durations - 6.4**), làm lệch đường găng (Critical Path) và gây vỡ tiến độ. Lập kế hoạch sức chứa chính là kỹ thuật **Resource Leveling (Cân bằng nguồn lực)** chủ động ngay từ vạch xuất phát.

Trong môi trường Hybrid, Capacity Planning thường là đầu vào quan trọng cho:

- Sprint Planning
- Release Planning
- Schedule Baseline
- Resource Histogram
- Risk Register liên quan đến overload, thiếu kỹ năng hoặc phụ thuộc nhân sự chủ chốt

---

## II. Ví dụ & minh họa thực tế

### Ví dụ: Tính toán Capacity cho đội ngũ phát triển Dự án "Epic Center" trong Sprint 2 tuần

- **Quy mô team:** 5 thành viên full-time gồm 2 Backend Developers, 2 Mobile Developers và 1 QA Tester.
- **Thời gian Sprint:** 10 ngày làm việc (2 tuần).
- **Hệ số tập trung (Focus Factor):** 70% (0.7).

### Bước 1: Tính tổng giờ làm việc lý thuyết (Gross Capacity)

```text
Gross Capacity = 5 người x 10 ngày x 8 giờ/ngày = 400 giờ công
```

### Bước 2: Trừ lịch nghỉ phép & ngày lễ đã biết trước

Giả sử 1 Backend Developer xin nghỉ phép 1 ngày trong Sprint này, tương đương trừ 8 giờ.

```text
Net Available Hours = 400 - 8 = 392 giờ
```

### Bước 3: Áp dụng Focus Factor để tính sức chứa thực tế

```text
Real Capacity = 392 giờ x 0.7 = 274.4 giờ công thực tế
```

### Bước 4: Quy đổi sang Story Points nếu dùng mô hình Agile

Nếu dữ liệu lịch sử cho thấy team mất trung bình **7 giờ công** để hoàn thành **1 Story Point (SP)**:

```text
Sprint Capacity = 274.4 giờ / 7 giờ mỗi SP ~= 39 Story Points
```

**Kết luận:** Tại buổi Sprint Planning, PO và PM chỉ nên chọn các User Stories có tổng điểm tối đa khoảng **39 SP** từ Product Backlog đưa vào Sprint. Nếu có rủi ro cao hoặc nhiều dependency chưa chắc chắn, nên tiếp tục giảm phạm vi hoặc thêm buffer.

---

## III. Case study dẫn chứng thực tế

### Hội chứng "cháy túi thời gian" do lập kế hoạch theo năng lực 100%

**Bối cảnh:** Một dự án tích hợp hệ thống Core Banking. PM lập kế hoạch dựa trên giả định mỗi lập trình viên làm việc năng suất 8 tiếng/ngày, 5 ngày/tuần, tức là 80 tiếng cho mỗi Sprint 2 tuần.

**Vấn đề phát sinh:**

1. Thực tế, các Developer phải tham gia Daily Standup, họp với khách hàng, hỗ trợ sửa lỗi khẩn cấp (Hotfix) cho hệ sinh thái cũ đang chạy và xử lý nhiều yêu cầu vận hành xen ngang.
2. Thời gian thực tế để viết code chỉ còn khoảng 4.5 tiếng/ngày, thấp hơn rất nhiều so với giả định 8 tiếng/ngày.
3. Do kế hoạch bị nhồi nhét 100% dung lượng lý thuyết, team rơi vào trạng thái nợ đọng công việc dây chuyền. Bug phát sinh không có thời gian sửa, QA không có thời gian test kỹ.
4. Để kịp deadline, team phải OT liên tục, dẫn đến việc 2 Developer chủ chốt xin nghỉ việc ngay trước giai đoạn UAT quan trọng nhất.

**Giải pháp khắc phục:**

1. PMO yêu cầu áp dụng ngay kỹ thuật **Focus Factor 0.7** vào bộ công cụ tính toán Capacity tự động trên Jira.
2. Thiết lập khoảng đệm an toàn **15-20%** cho các công việc không tên, bug phát sinh, cuộc họp đột xuất và hỗ trợ vận hành.
3. Mọi Sprint Planning phải đối chiếu với Historical Velocity của 3-5 Sprint gần nhất, thay vì chỉ dựa trên mong muốn của stakeholder.
4. Các trường hợp vượt quá capacity phải được escalation sớm để giảm scope, đổi thứ tự ưu tiên hoặc bổ sung nguồn lực thật sự.

---

## IV. Tips & điều lưu ý thực chiến cho PM/PO

### 1. Đừng dùng Capacity để so sánh hiệu suất giữa các team

Mỗi team có một Focus Factor, văn hóa kỹ thuật, mức độ legacy, độ phức tạp domain và cách chấm Story Point khác nhau. Team A làm 40 SP/Sprint không có nghĩa là giỏi hơn Team B làm 20 SP/Sprint. Capacity nên được dùng để lập kế hoạch nội bộ cho chính team đó, không phải để xếp hạng.

### 2. Theo dõi Resource Utilization so với Capacity

Hãy cập nhật Capacity định kỳ trước mỗi kỳ lập kế hoạch. Năng lực của team sẽ thay đổi khi:

- Có thành viên mới vào team và cần thời gian onboarding
- Có người nghỉ phép hoặc chuyển dự án
- Team phải hỗ trợ vận hành nhiều hơn dự kiến
- Kiến trúc hoặc công cụ đã ổn định hơn, giúp Focus Factor tăng
- Sprint chứa nhiều công việc discovery, research hoặc dependency vendor

### 3. Quản lý "hiệu ứng giờ mù" (Blind Hours)

Đối với các dự án outsource hoặc bàn giao đa quốc gia lệch múi giờ, hãy trừ thời gian trễ do chờ phản hồi thông tin giữa các bên vào phần hao phí năng lực. Ví dụ, một câu hỏi kỹ thuật gửi cuối ngày tại Việt Nam có thể chỉ được phản hồi vào ngày làm việc tiếp theo ở Mỹ, làm chậm cả chuỗi xử lý.

### 4. Không lấp đầy 100% Capacity bằng feature work

Ngay cả khi phép tính cho thấy team có thể làm 39 SP, PM/PO không nên lấp kín toàn bộ bằng feature mới nếu Sprint có nhiều rủi ro. Nên giữ một phần capacity cho:

- Bug fix
- Code review
- Refactoring nhỏ cần thiết
- Hỗ trợ QA/UAT
- Việc phát sinh từ vận hành
- Cải thiện pipeline hoặc môi trường test

---

## V. Template Capacity Planning nên dùng

| Trường thông tin | Nội dung cần có |
| --- | --- |
| Planning Period | Sprint, phase, tháng hoặc release window |
| Team Members | Danh sách thành viên, vai trò và mức độ allocation |
| Gross Capacity | Tổng giờ danh nghĩa trước khi trừ hao phí |
| Planned Absence | Nghỉ phép, ngày lễ, training, sự kiện công ty |
| Operational Load | Họp, support, hotfix, vận hành, context switching |
| Focus Factor | Hệ số tập trung áp dụng cho từng người hoặc toàn team |
| Real Capacity | Giờ công thực tế có thể dùng cho project work |
| Historical Velocity | Velocity trung bình 3-5 Sprint gần nhất |
| SP Conversion | Quy đổi giờ công sang Story Points nếu cần |
| Capacity Buffer | Phần trăm dự phòng cho rủi ro và việc phát sinh |
| Committed Scope | Tổng SP hoặc work items được nhận vào kỳ kế hoạch |
| Overload Signals | Dấu hiệu quá tải cần theo dõi |
| Action Plan | Giảm scope, đổi ưu tiên, bổ sung nguồn lực hoặc dời mốc |

---

## VI. Tài liệu & nguồn tham khảo

### 1. Chuẩn quốc tế & sách gối đầu giường

- *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) - 6th Edition*, Section 6.4: Estimate Activity Durations.
- *Agile Estimating and Planning* - Mike Cohn, chương về lập kế hoạch năng lực và quy đổi vận tốc.

### 2. Blog chuyên môn uy tín

- Scrum.org: *Capacity Planning in Scrum: How to calculate team availability accurately*.
- Atlassian Blog: *How to master capacity planning for agile teams*.

### 3. Video / YouTube hữu ích

- Search keyword: *"Agile Capacity Planning Excel Template Tutorial"*.
- Search keyword: *"Focus Factor and Velocity in Agile Scrum Explained"*.
