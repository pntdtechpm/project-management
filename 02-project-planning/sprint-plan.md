# 02-PROJECT-PLANNING: BÀI 04 - SPRINT PLAN (KẾ HOẠCH SPRINT)

**Tên tài liệu:** `02-project-planning/sprint-plan.md`  
**Chủ đề:** Lập Kế hoạch Sprint (Sprint Planning) trong mô hình Agile/Hybrid theo chuẩn PMI & Scrum  
**Đối tượng hướng tới:** Product Owner (PO), Project Manager (PM), Scrum Master, Tech Lead và Đội ngũ Phát triển (Development Team).

---

## I. Khung kiến thức chuẩn Agile (PMI-ACP® & Scrum Guide)

### 1. Định nghĩa & vị trí của Sprint Planning

Theo hướng dẫn Agile của PMI (*Agile Practice Guide*) và Scrum Guide, **Sprint Planning (Lập kế hoạch Sprint)** là một sự kiện bắt buộc để khởi đầu cho một Sprint mới. Mục đích của sự kiện này là xác định những gì có thể được bàn giao trong Sprint và cách thức thực hiện công việc đó.

- **Thời lượng tiêu chuẩn (Timebox):** Tối đa **8 tiếng** cho một Sprint tiêu chuẩn kéo dài 4 tuần. Với các Sprint phổ biến hiện nay kéo dài 2 tuần, buổi họp này thường được giới hạn trong khoảng **2 đến 4 tiếng**.
- **Nguyên tắc bất biến:** Sprint Planning là hoạt động mang tính **hợp tác (Collaborative)**. Không một cá nhân nào, kể cả PO hay PM, có quyền áp đặt khối lượng công việc lên Development Team. Đội ngũ phát triển là bên đánh giá và cam kết khối lượng User Stories đưa vào Sprint dựa trên năng lực thực tế.

### 2. Ba phần cốt lõi của Sprint Planning: Why, What, How

Một buổi Sprint Planning chuẩn mực phải trả lời được 3 câu hỏi lớn:

1. **Tại sao Sprint này có giá trị? (Why)**
   - **Kết quả:** Xác định **Sprint Goal (Mục tiêu Sprint)**. Đây là mục đích tối thượng mà toàn đội cam kết đạt được thông qua việc triển khai các hạng mục trong Sprint.

2. **Những gì có thể làm trong Sprint này? (What)**
   - **Kết quả:** Lựa chọn các hạng mục từ **Product Backlog** đã được làm mịn (Refined) để đưa vào **Sprint Backlog**.

3. **Làm thế nào để hoàn thành công việc đã chọn? (How)**
   - **Kết quả:** Development Team tự thảo luận, phân rã các User Stories thành các nhiệm vụ chi tiết (Tasks/Sub-tasks) và ước tính kỹ thuật.

### 3. Mối liên hệ giữa PMP (PMBOK® Guide - 6th Edition) và Agile Sprint Planning

Trong môi trường quản lý dự án lai (Hybrid), Sprint Planning có thể xem là phiên lập kế hoạch chi tiết, lặp đi lặp lại của các quy trình **Develop Schedule** (Process 6.5) và **Direct and Manage Project Work** (Process 4.3).

- Thay vì lập kế hoạch chi tiết cho 1 năm, PM phối hợp với Agile Team để lập kế hoạch khả thi cho **1-2 tuần**.
- **Scope Baseline** được kiểm soát linh hoạt thông qua **Sprint Backlog** và **Sprint Goal**.
- Mọi thay đổi trong Sprint phải được đánh giá dựa trên câu hỏi: thay đổi đó có làm ảnh hưởng đến Sprint Goal hay không.

---

## II. Ví dụ & minh họa thực tế

### Ví dụ: Kế hoạch Sprint 2 tuần cho dự án "Epic Center" - Module Tích lũy E-Coffer & Thanh toán

- **Dự án:** Ứng dụng Bất động sản & Dịch vụ Tài chính Epic Center
- **Thời gian Sprint:** Sprint 05, từ 03/08/2026 đến 14/08/2026
- **Velocity trung bình của team:** 40 Story Points (SP)
- **Capacity kế hoạch:** 38 SP sau khi trừ nghỉ phép, hỗ trợ vận hành và các cuộc họp bắt buộc

### 1. Sprint Goal (Mục tiêu Sprint)

> "Tích hợp thành công cổng thanh toán VietQR tự động và cho phép người dùng nạp tiền giữ chỗ trực tuyến để nhận ưu đãi từ quỹ E-Coffer."

### 2. Danh sách User Stories được chọn (Sprint Backlog - Tổng: 38 SP)

1. **US-01 (8 SP):** Là một Người thuê phòng, tôi muốn thanh toán tiền cọc qua mã VietQR động để giao dịch được xử lý tức thì mà không cần nhập tay số tiền.
   - **Definition of Done:** Chạy ổn định trên iOS/Android, quét được qua ít nhất 3 app ngân hàng lớn, cập nhật trạng thái hóa đơn dưới 5 giây.

2. **US-02 (13 SP):** Là một Thành viên Epic Center, tôi muốn nạp tiền vào quỹ tích lũy "E-Coffer" để nhận voucher giảm giá 10% khi đặt homestay du lịch.
   - **Definition of Done:** Người dùng nạp tiền thành công, số dư E-Coffer cập nhật chính xác, voucher được phát sinh theo rule đã duyệt.

3. **US-03 (5 SP):** Là một Host (Chủ nhà), tôi muốn nhận thông báo (Push Notification) ngay lập tức khi khách hàng nạp tiền cọc phòng thành công.
   - **Definition of Done:** Push notification gửi trong vòng 10 giây, có deep link vào chi tiết booking, log gửi thông báo được lưu để audit.

4. **US-04 (12 SP):** Phát triển hệ thống core tính toán lợi nhuận cấu hình linh hoạt cho quỹ E-Coffer ở backend.
   - **Definition of Done:** Admin cấu hình được rule lợi nhuận, backend tính toán đúng theo test case tài chính, có unit test cho các scenario chính.

### 3. Kế hoạch triển khai chi tiết (phân rã task mẫu cho US-01)

| Task | Owner | Estimate | Ghi chú |
| --- | --- | ---: | --- |
| Thiết kế giao diện hiển thị QR Code động trên Mobile App | Design / Frontend | 6h | Bao gồm trạng thái loading, expired và payment success |
| Tích hợp API webhook nhận IPN (Instant Payment Notification) từ đối tác ngân hàng | Backend | 12h | Cần xử lý idempotency và retry |
| Viết script kiểm thử tự động luồng thanh toán lỗi/hết hạn mã QR | QA / Tester | 8h | Bao phủ happy path, timeout và duplicate callback |

### 4. Sprint Plan template nên dùng

| Trường thông tin | Nội dung cần có |
| --- | --- |
| Sprint ID | Tên/ID Sprint, ngày bắt đầu, ngày kết thúc |
| Sprint Goal | Một mục tiêu rõ ràng, ngắn gọn, định hướng giá trị |
| Capacity | Số người, số ngày làm việc, nghỉ phép, hệ số tập trung |
| Velocity tham chiếu | Velocity trung bình 3-5 Sprint gần nhất |
| Sprint Backlog | Danh sách User Stories, Story Points, owner, dependency |
| Definition of Ready | Tiêu chí để story được phép đưa vào Sprint |
| Definition of Done | Tiêu chí để story được công nhận hoàn thành |
| Rủi ro & phụ thuộc | API, vendor, môi trường, dữ liệu test, approval |
| Kế hoạch demo | Nội dung demo cuối Sprint và stakeholder cần tham dự |

---

## III. Case study dẫn chứng thực tế

### Hệ lụy của việc "nhồi nhét" Backlog và hệ thống sập Staging do chạy theo số lượng

**Bối cảnh:** Một dự án làm ví điện tử du lịch đang chậm so với Roadmap tổng thể. Tại buổi Sprint Planning, Product Owner yêu cầu Development Team nhận gấp đôi số lượng công việc so với năng lực bình thường: 80 Story Points trong khi Velocity lịch sử của team chỉ khoảng 45 SP.

**Vấn đề phát sinh:**

1. **Bỏ qua phần How:** Do bị áp lực thời gian, Development Team không phân rã task chi tiết và không thảo luận kỹ về thiết kế kỹ thuật. Mọi người bắt tay vào code ngay với nhiều giả định khác nhau.
2. **Không story nào thật sự Done:** Đến cuối Sprint, không có User Story nào đạt **Definition of Done**. Một số phần "xong code" nhưng chưa test, chưa review, chưa deploy được lên Staging.
3. **Lỗi tích hợp nghiêm trọng:** Các nhánh code chắp vá gây merge conflict lớn và làm sập môi trường Staging trong giai đoạn demo.
4. **Tinh thần team đi xuống:** PO và Development Team đổ lỗi lẫn nhau trong Sprint Retrospective vì cam kết Sprint ban đầu không dựa trên dữ liệu thực tế.

**Giải pháp khắc phục:**

1. Thiết lập lại nguyên tắc: khối lượng Sprint phải dựa trên **Velocity lịch sử** và **Capacity thực tế**, không dựa trên kỳ vọng chủ quan.
2. Áp dụng nghiêm ngặt **Product Backlog Refinement** ít nhất 3 ngày trước Sprint Planning để đảm bảo các User Stories đã đạt **Definition of Ready**.
3. Không đưa story chưa rõ acceptance criteria, dependency hoặc thiết kế UX/API vào Sprint Backlog.
4. Sprint Goal được dùng như tiêu chí ra quyết định khi có yêu cầu chen ngang giữa Sprint.

**Kết quả:** Sau 3 Sprint, số story bị carry-over giảm mạnh, Staging ổn định hơn và Sprint Review chuyển từ báo cáo "đang làm" sang demo được increment chạy thật.

---

## IV. Tips & điều lưu ý thực chiến cho PM/PO/Scrum Master

1. **Sử dụng công thức sức chứa thực tế (Capacity Planning)**
   - Đừng giả định team có 100% thời gian để code.
   - Công thức tham khảo:

```text
Capacity = (Số thành viên x Số ngày làm việc x 8 giờ x 0.75) - Giờ họp hành/nghỉ phép/hỗ trợ vận hành
```

   - Hệ số 0.75 giúp bù đắp cho việc đột xuất, fix bug phát sinh, hỗ trợ kỹ thuật và context switching.

2. **Định nghĩa rõ DoR và DoD**
   - **DoR (Definition of Ready):** Tiêu chí để một hạng mục **được phép** đưa vào Sprint Planning. Ví dụ: đầy đủ UI/UX, mô tả nghiệp vụ rõ ràng, có acceptance criteria, dependency đã được nhận diện.
   - **DoD (Definition of Done):** Tiêu chí để công nhận một hạng mục đã **hoàn thành** ở cuối Sprint. Ví dụ: code đã review, pass test case, không còn defect nghiêm trọng, đã deploy lên Staging, tài liệu cần thiết đã cập nhật.

3. **Không đổi Sprint Goal tùy tiện giữa Sprint**
   - Nếu có yêu cầu khẩn cấp từ thị trường hoặc cấp trên, PO cần đánh giá mức độ ảnh hưởng đến Sprint Goal.
   - Trong trường hợp mục tiêu Sprint không còn giá trị, PO có thể cân nhắc hủy Sprint theo Scrum Guide, thay vì liên tục chèn thêm việc làm phá vỡ cam kết ban đầu.

4. **Không dùng Velocity như KPI cá nhân**
   - Velocity là công cụ lập kế hoạch của team, không phải thước đo năng suất cá nhân.
   - Nếu biến Velocity thành KPI, team có xu hướng inflate Story Points hoặc chia nhỏ story không tự nhiên để làm đẹp số liệu.

5. **Sprint Planning cần đầu vào sạch**
   - Product Backlog phải được refine trước.
   - Các dependency lớn như API vendor, môi trường test, dữ liệu mẫu và approval nghiệp vụ phải được làm rõ trước khi team cam kết.
   - Story chưa đạt DoR nên quay lại Product Backlog, không ép vào Sprint để "giữ tiến độ".

---

## V. Tài liệu & nguồn tham khảo

### 1. Tài liệu & chuẩn quốc tế

- *Project Management Institute (PMI) - Agile Practice Guide* (2017), Section 5.2.5: Execution Practices.
- *The 2020 Scrum Guide* - Ken Schwaber and Jeff Sutherland.

### 2. Blog chuyên sâu dành cho quản lý sản phẩm

- Mountain Goat Software (Mike Cohn): *Sprint Planning Tips for Agile Teams*.
- Scrum.org Blog: *The Purpose of Sprint Planning and the Sprint Goal*.

### 3. Video / YouTube hữu ích

- Search keyword: *"Sprint Planning Meeting Explained - Role of PO, SM, and Dev"* (Agile Alliance hoặc Scrum.org).
- Search keyword: *"How to estimate Story Points in Sprint Planning"*.
