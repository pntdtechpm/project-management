# 02-PROJECT-PLANNING: BÀI 03 - MILESTONE (CỘT MỐC DỰ ÁN)

**Tên tài liệu:** `02-project-planning/milestone.md`  
**Chủ đề:** Xác định và Quản lý Cột mốc Dự án (Project Milestones) theo chuẩn PMP & thực tế Agile/Hybrid  
**Đối tượng hướng tới:** Project Manager (PM), Product Owner (PO), Technical Lead, Business Analyst (BA) và các stakeholders quan trọng.

---

## I. Khung kiến thức chuẩn PMP (PMBOK® Guide - 6th Edition)

### 1. Định nghĩa & bản chất của Milestone

Theo PMBOK® Guide - 6th Edition, trong quy trình **Define Activities** (Process 6.2), **Milestone (Cột mốc)** là một điểm hoặc sự kiện có ý nghĩa quan trọng trong toàn bộ quá trình thực hiện dự án.

- **Đặc tính kỹ thuật cốt lõi:** Milestone có **thời lượng bằng 0 (Zero Duration)**. Nó không tiêu tốn thời gian hay tài nguyên/chi phí trực tiếp. Nó đại diện cho **sự hoàn thành** của một khối lượng công việc, một giai đoạn hoặc một nghĩa vụ quan trọng.

### 2. Danh sách cột mốc (Milestone List)

Trong Project Schedule Management, **Milestone List** là một tài liệu dự án quan trọng được tạo ra từ quy trình **Define Activities** (Process 6.2):

- **Mandatory Milestones (Cột mốc bắt buộc):** Các cột mốc phải tuân thủ theo điều khoản hợp đồng, yêu cầu pháp lý hoặc cam kết với khách hàng.
- **Optional / Discretionary Milestones (Cột mốc tùy chọn/nội bộ):** Các cột mốc do đội ngũ quản lý dự án tự thiết lập dựa trên kinh nghiệm lịch sử hoặc thói quen vận hành để kiểm soát tiến độ nội bộ.

### 3. Vòng đời của Milestone trong tiến trình quản lý dự án

Milestone xuất hiện liên tục và xuyên suốt từ cấp độ tổng quan đến chi tiết:

1. **Giai đoạn khởi tạo (Initiating):** Tồn tại dưới dạng **Summary Milestone Schedule** trong **Project Charter**.
2. **Giai đoạn lập kế hoạch (Planning):** Được chi tiết hóa thành **Milestone List** và thể hiện trực quan qua **Milestone Chart** trong quy trình **Develop Schedule** (Process 6.5).
3. **Giai đoạn thực thi & kiểm soát (Executing, Monitoring & Controlling):** Được dùng trong **Direct and Manage Project Work** (Process 4.3) và **Monitor and Control Project Work** (Process 4.5) để đánh giá xem dự án có đang đi đúng hướng hay không.

### 4. So sánh phân biệt: Milestone vs. Deliverable vs. Activity vs. Phase Gate

| Khái niệm | Định nghĩa theo PMP | Thời lượng (Duration) | Ví dụ minh họa |
| --- | --- | --- | --- |
| **Deliverable** *(Sản phẩm bàn giao)* | Sản phẩm, kết quả hoặc khả năng cung cấp dịch vụ độc nhất, có thể kiểm tra được. | Không áp dụng trực tiếp; đo bằng trạng thái hoàn thành | Tài liệu Thiết kế Kiến trúc Hệ thống eKYC |
| **Activity** *(Hoạt động/Task)* | Công việc nhỏ được phân rã từ Work Package để tạo ra Deliverable. | > 0 (số giờ/số ngày) | Viết code module OCR đọc thẻ CCCD (5 ngày) |
| **Milestone** *(Cột mốc)* | Điểm hoặc sự kiện quan trọng đánh dấu một thành tựu. | **Đúng 0 (Zero Duration)** | Nghiệm thu & phê duyệt Tài liệu Thiết kế Kiến trúc (ký sign-off) |
| **Phase Gate** *(Cổng giai đoạn)* | Điểm đánh giá cuối mỗi phase để quyết định Go/No-Go tiếp tục dự án. | Thời điểm họp review | Phase Review từ giai đoạn Planning sang Execution |

---

## II. Ví dụ & minh họa thực tế

### Ví dụ: Bộ Milestone chuẩn cho dự án Onboarding & eKYC ngân hàng số ("Epic Center")

Dưới đây là Milestone List mẫu đại diện cho luồng triển khai thực tế:

```text
[M1: Project Charter Approved] -> [M2: Architecture Freeze] -> [M3: Core eKYC Engine Ready] -> [M4: UAT Sign-off] -> [M5: Go-Live]
```

1. **`M1` - Phê duyệt Project Charter & Ngân sách** *(Mandatory / Business Milestone)*
   - **Ngày dự kiến:** 15/01/2026 | **Duration:** 0 days
   - **Ý nghĩa:** Ban Giám đốc đã ký duyệt Project Charter, cấp quyền cho PM sử dụng nguồn lực.

2. **`M2` - Chốt Thiết kế Kiến trúc & An toàn Bảo mật (Architecture Freeze)** *(Technical Milestone)*
   - **Ngày dự kiến:** 28/02/2026 | **Duration:** 0 days
   - **Ý nghĩa:** Hoàn thành 100% tài liệu System Architecture, Security Compliance và được CTO/Kiểm toán Security chấp thuận.

3. **`M3` - Hoàn thành Tích hợp & Kiểm thử Môi trường Sandbox eKYC** *(Internal Milestone)*
   - **Ngày dự kiến:** 30/04/2026 | **Duration:** 0 days
   - **Ý nghĩa:** Module OCR và Face Matching đã chạy thông suốt trên môi trường thử nghiệm.

4. **`M4` - Báo cáo Nghiệm thu UAT từ Khối Vận hành (UAT Sign-off)** *(Contractual / Mandatory Milestone)*
   - **Ngày dự kiến:** 15/06/2026 | **Duration:** 0 days
   - **Ý nghĩa:** Khối Ngân hàng số & Vận hành ký xác nhận hệ thống đáp ứng đủ tiêu chí nghiệp vụ.

5. **`M5` - Hệ thống Chính thức Go-Live trên Production** *(Major Release Milestone)*
   - **Ngày dự kiến:** 01/07/2026 | **Duration:** 0 days
   - **Ý nghĩa:** Mở cổng cho end-user thực tế đăng ký tài khoản qua ứng dụng di động.

### Template Milestone List nên dùng

| ID | Milestone | Loại | Ngày mục tiêu | Deliverable liên quan | Acceptance Criteria | Approver | Trạng thái |
| --- | --- | --- | --- | --- | --- | --- | --- |
| M1 | Project Charter Approved | Mandatory / Business | 15/01/2026 | Project Charter | Charter được ký duyệt, ngân sách được phân bổ | Sponsor | Planned |
| M2 | Architecture Freeze | Technical | 28/02/2026 | Architecture & Security Design | CTO và Security chấp thuận, không còn critical finding | CTO / Security Lead | Planned |
| M3 | Core eKYC Engine Ready | Internal | 30/04/2026 | OCR, Face Matching, Sandbox Integration | Test sandbox đạt pass rate đã thống nhất | Tech Lead | Planned |
| M4 | UAT Sign-off | Mandatory / Contractual | 15/06/2026 | UAT Report | UAT pass, defect Sev1/Sev2 = 0, business sign-off | Business Owner | Planned |
| M5 | Production Go-Live | Major Release | 01/07/2026 | Production Release | Release checklist hoàn tất, rollback plan sẵn sàng | Steering Committee | Planned |

---

## III. Case study dẫn chứng thực tế

### Thảm họa lập tiến độ khi biến Activity thành Milestone và thiếu tiêu chí nghiệm thu

**Bối cảnh:** Một dự án chuyển đổi số portal tài chính bất động sản kéo dài 12 tháng. PM thiết lập bảng tiến độ gồm 60 "milestones". Tuy nhiên, PM đưa vào danh sách các mục như *"Bắt đầu phát triển Module Chatbot AI"*, *"Đang làm kiểm thử UAT"* và *"Họp cập nhật tiến độ tuần 10"*.

**Vấn đề phát sinh:**

1. **Mơ hồ về trạng thái:** Ban Giám đốc thấy cột mốc *"Bắt đầu phát triển Chatbot AI"* báo màu xanh (đã đạt), nhưng không biết khi nào Chatbot AI đó **xong và dùng được**.
2. **Trượt tiến độ dây chuyền (Milestone Drift):** Do không gắn cột mốc với deliverable và acceptance criteria cụ thể, công việc bị kéo dài mà không ai phát hiện sớm, dẫn đến ngày Go-Live thực tế bị chậm 4 tháng.
3. **Mất giá trị báo cáo điều hành:** Milestone Chart biến thành task list, khiến các cột mốc thật sự quan trọng bị chìm trong các hoạt động vận hành hằng tuần.

**Giải pháp khắc phục:**

1. Xóa bỏ toàn bộ activity/task khỏi Milestone List.
2. Chuẩn hóa lại các cột mốc theo nguyên tắc: **Zero Duration + Outcome / Sign-off rõ ràng**.
3. Thay *"Bắt đầu làm Chatbot"* bằng *"Nghiệm thu Tích hợp AI Chatbot Engine thành công"*.
4. Bổ sung **Acceptance Criteria** và **Approver** bắt buộc cho từng Milestone.

**Kết quả:** Steering Committee nhìn thấy trạng thái thật của dự án rõ hơn, PM phát hiện trễ hạn sớm hơn và lịch Go-Live được tái baseline theo change control thay vì trôi âm thầm.

---

## IV. Tips & điều lưu ý thực chiến cho PM/PO

1. **Nguyên tắc vàng "Zero Duration"**
   - Khi nhập Milestone vào các phần mềm quản lý như MS Project, Jira, Primavera hoặc ClickUp, luôn đảm bảo đặt `Duration = 0 days`.
   - Nếu một mục có thời lượng 3 ngày, đó là **Task / Activity**, không phải **Milestone**.

2. **Nguyên tắc "vừa đủ"**
   - **Quá nhiều Milestone:** Biến Milestone Chart thành Task List, làm giảm giá trị theo dõi tổng quan cho Ban Giám đốc/stakeholders.
   - **Quá ít Milestone:** Dự án chạy 6 tháng mới có 1 cột mốc sẽ làm PM thiếu visibility và khó phát hiện rủi ro trễ hạn sớm.
   - **Best practice:** Mỗi giai đoạn 1-2 tháng nên có từ 1 đến 3 milestone chính.

3. **Gắn Milestone với Deliverable và Acceptance Criteria**
   - Một milestone tốt nên trả lời được ba câu hỏi: đã đạt điều gì, bằng chứng nào chứng minh đã đạt, ai có quyền xác nhận.
   - Tránh các milestone dạng hành động đang diễn ra như *"Đang kiểm thử"*, *"Đang tích hợp"*, *"Bắt đầu phát triển"*.

4. **Mối quan hệ với Critical Path (Đường găng)**
   - Hãy cẩn trọng với các cột mốc nằm trên Critical Path của dự án.
   - Nếu một milestone trên Critical Path bị trễ 1 ngày, toàn bộ ngày Go-Live của dự án có thể bị trễ tương ứng 1 ngày nếu không có float hoặc phương án recovery.

5. **Milestone trong mô hình Agile/Scrum**
   - Trong Agile, milestone thường gắn với **End of Sprint**, **Release Date** hoặc thời điểm hoàn thành một product increment.
   - Ví dụ: *"Release v1.2 Candidate Available"*, *"Sprint 5 Review & Demo Sign-off"*, *"MVP Feature Set Accepted"*.
   - Không nên biến mọi sprint ceremony thành milestone; chỉ chọn các sự kiện có ý nghĩa kiểm soát hoặc ra quyết định.

---

## V. Tài liệu & nguồn tham khảo

### 1. Sách & chuẩn quốc tế

- *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) - 6th Edition*, Chapter 6: Project Schedule Management, Section 6.2 Define Activities, Section 6.2.3.3 Milestone List.
- *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) - 6th Edition*, Chapter 6: Project Schedule Management, Section 6.5 Develop Schedule, Section 6.5.3.2 Project Schedule.
- *Practice Standard for Scheduling - 3rd Edition* (PMI).

### 2. Blog & bài viết chuyên ngành

- PMI.org: *Project Milestones: How to Use Them to Keep Projects on Track*.
- ProjectManagement.com: *Milestones vs Deliverables vs Tasks - Clear Definitions for PMs*.

### 3. Video / YouTube nên xem

- Search keyword: *"Project Milestones Explained - PMBOK Framework"* (Ricardo Vargas hoặc ProjectManager).
- Search keyword: *"How to create a Milestone Chart in Gantt Charts"*.
