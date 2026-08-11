# 03-PROJECT-EXECUTION: BÀI 05 - MEETING MINUTES (BIÊN BẢN CUỘC HỌP DỰ ÁN)

## 1. KHUNG KIẾN THỨC CHUẨN PMP (PMBOK 6 & 7) & LIÊN HỆ THỰC TẾ

### A. Khái niệm theo chuẩn Quản trị Dự án Quốc tế (PMP)

Nhiều người coi Biên bản cuộc họp (**Meeting Minutes**) là một thủ tục hành chính nhàm chán. Tuy nhiên, theo chuẩn PMP, đây là một tài liệu truyền thông quan trọng trực tiếp bảo vệ tiến độ và cam kết của dự án.

* **PMBOK 6th Edition:**
* Thuộc **Project Communications Management** (Nhóm quy trình *Manage Communications*).
* Meeting Minutes là một dạng **Communication Artifact** thuộc Tài sản Quy trình Tổ chức (OPAs), giúp ghi nhận chính xác các thông tin đã được trao đổi, giảm thiểu sai lệch thông tin (Miscommunication) và minh bạch hóa trách nhiệm giải trình giữa các bên liên quan (Stakeholders).


* **PMBOK 7th Edition & Agile:**
* Thuộc **Stakeholder Performance Domain** và **Project Work Performance Domain**.
* Tuyên ngôn Agile ưu tiên *"Sự tương tác cá nhân hơn là quy trình và công cụ"*, nhưng điều này **không có nghĩa là không ghi chép**. Trong môi trường Agile/Hybrid, Meeting Minutes được áp dụng theo tinh thần **Lean Documentation** (Tài liệu tinh gọn): Không chép lời thoại chi tiết, chỉ tập trung vào **3A**: *Alignment* (Đồng thuận), *Agreements/Decisions* (Quyết định) và *Action Items* (Hành động).



### B. Liên hệ Thực tế Quản lý Sản phẩm (Product Management)

* **Bản chất:** Một cuộc họp không có Meeting Minutes đồng nghĩa với việc cuộc họp đó **chưa bao giờ diễn ra**.
* **Mục đích cốt lõi:**
1. **Chuyển hóa "Lời nói gió bay" thành "Hành động có trách nhiệm":** Đảm bảo mọi thảo luận đều kết thúc bằng việc phân công cụ thể người làm và thời hạn hoàn thành.
2. **Bảo vệ Product Team:** Tránh tình trạng Stakeholder chối bỏ các cam kết hoặc thay đổi ý định sau cuộc họp mà không có bằng chứng đối soát.
3. **Đồng bộ nhân sự vắng mặt:** Giúp các thành viên không thể tham dự vẫn nắm bắt chính xác bối cảnh và kết quả mà không cần tổ chức lại cuộc họp.



---

## 2. CẤU TRÚC BỘ CÔNG CỤ & KHUNG FILE MEETING MINUTES (ARTIFACTS)

Một mẫu **Meeting Minutes** chuẩn mực (trên Confluence, Notion, Coda hoặc Google Docs) cần tối giản, scannable (dễ đọc lướt) và bao gồm 5 phần chính:

### A. Phần thông tin chung (Header)

* **Project Name:** Tên dự án.
* **Meeting Title:** Tiêu đề cuộc họp (Ví dụ: *Alignment Luồng Hoàn tiền Khách hàng - Sprint 8*).
* **Date & Time:** Ngày, giờ bắt đầu & kết thúc.
* **Location/Link:** Phòng họp hoặc link Google Meet/Zoom.
* **Facilitator (Chủ trì):** Người dẫn dắt.
* **Note-taker (Ghi chép):** Người chịu trách nhiệm viết biên bản.
* **Attendees (Tham dự):** Danh sách người có mặt & vắng mặt (Absentees).

### B. Phần nội dung cốt lõi (Core Body)

```markdown
### 1. Mục tiêu cuộc họp (Meeting Objective)
• Chốt phương án xử lý logic hoàn tiền tự động cho tính năng Đặt phòng Homestay.

### 2. Tóm tắt nội dung & Quyết định (Key Discussions & Decisions)
• [Đã chốt] Khách hủy phòng trước 24h sẽ được hệ thống tự động hoàn 100% tiền qua ví MoMo/Ngân hàng.
• [Đã chốt] Nếu hủy phòng trong vòng 24h, hệ thống thu phí phạt 50% tiền cọc (Chuyển trực tiếp cho Chủ nhà).

### 3. Danh sách hành động (Action Items - Bắt buộc)

```

| Action Item (Việc cần làm) | Assignee (Người chịu trách nhiệm) | Due Date (Hạn chót) | Status |
| --- | --- | --- | --- |
| Cập nhật UI/UX luồng Hủy phòng & hiển thị mức phí phạt | **Duy (UI/UX)** | `18/03/2026` | `In Progress` |
| Bổ sung logic API Webhook hoàn tiền tự động | **Tấn (Tech Lead)** | `20/03/2026` | `To Do` |
| Soạn văn bản CSKH xử lý các ca khiếu nại hoàn tiền | **Hoa (CSKH Lead)** | `21/03/2026` | `To Do` |

---

## 3. QUY TRÌNH QUẢN LÝ CUỘC HỌP & THỰC THI BIÊN BẢN (WORKFLOW)

### 1. Before Meeting (Trước cuộc họp)

* Gửi **Agenda** (Chương trình họp) và tài liệu đọc trước (Pre-read materials) cho các bên tham dự ít nhất **24 giờ** trước khi họp.
* Phân công rõ ai là người làm **Facilitator** và ai là **Note-taker**.

### 2. During Meeting (Trong cuộc họp)

* Chiếu trực tiếp file ghi chú (Confluence/Notion) lên màn hình để mọi người cùng theo dõi real-time.
* **Ghi chép tinh gọn:** Dùng dạng gạch đầu dòng (Bullet points), tuyệt đối không chép từng câu từng chữ.
* **Dành 3-5 phút cuối cùng (Wrap-up):** Đọc lại toàn bộ *Decisions* và *Action Items* (ai làm gì, deadline khi nào) để tất cả thành viên xác nhận tại chỗ.

### 3. After Meeting (Sau cuộc họp)

* **Quy tắc 24h:** Phát hành Biên bản cuộc họp đến toàn bộ người tham dự và các bên liên quan trong vòng **vốn dĩ tốt nhất là ngay sau 1 - 2 giờ**, chậm nhất là 24 giờ.
* Đính kèm link Meeting Minutes vào kênh chat chung (Slack/Teams) hoặc thẻ công việc trên Jira.

---

## 4. CASE STUDY THỰC TẾ: DỰ ÁN "EPIC CENTER"

* **Bối cảnh:** Cuộc họp liên phòng ban giữa Product Team (Duy - PO), Đội Kỹ thuật (Tech Team), và Đội Chăm sóc khách hàng (CSKH) để giải quyết xung đột về tính năng *"Tự động hủy đơn đặt phòng nếu khách không thanh toán sau 15 phút"*.
* **Xung đột:** CSKH lo ngại 15 phút là quá ngắn khiến khách hàng bức xúc. Tech Team khẳng định nếu kéo dài 60 phút thì phòng sẽ bị giữ "ảo", ảnh hưởng tới Chủ nhà.
* **Tóm tắt Meeting Minutes được lập ngay trong cuộc họp:**
* **Meeting Title:** Alignment Thời gian giữ phòng tạm thời (Epic Center App).
* **Key Decision:** Thống nhất khoảng thời gian chờ (Hold time) là **30 phút**. Trong thời gian này, ứng dụng sẽ gửi 02 thông báo Push Notification (ở phút thứ 15 và phút thứ 25) để nhắc nhở khách.
* **Action Items chốt tại chỗ:**
1. *Duy (PO):* Cập nhật lại Timer Countdown trên UI màn hình Checkout. ➔ *Deadline: 12:00 PM - 16/03*.
2. *Hoa (CSKH Lead):* Duyệt lại nội dung 2 Push Notifications nhắc thanh toán. ➔ *Deadline: 17:00 PM - 16/03*.
3. *Tấn (Tech Lead):* Cấu hình Cronjob tự động giải phóng phòng sau 30 phút trên Server. ➔ *Deadline: 18/03*.




* **Kết quả:** Biên bản được gửi qua Slack ngay sau khi họp 15 phút. Tất cả các bên nắm rõ công việc, tính năng được bàn giao đúng hạn vào Sprint 9 mà không xảy ra tình trạng "tranh cãi lại lý do tại sao lại chọn 30 phút".

---

## 5. CÁC TIPS & ĐIỀU LƯU Ý THỰC CHIẾN (ANTI-PATTERNS & SOLUTIONS)

| Sai lầm phổ biến (Anti-Pattern) | Hậu quả | Giải pháp thực chiến |
| --- | --- | --- |
| **"Bản chép thoại Drama" (Transcript Style)** | Ghi chép quá chi tiết từng lời cãi vã, khiến tài liệu dài 5 trang không ai muốn đọc. | Chỉ ghi kết quả: **Đã chốt cái gì (Decisions)** và **Ai phải làm gì (Actions)**. Bỏ qua các tranh luận dông dài. |
| **Action Item "vô chủ" hoặc không có Deadline** | Công việc bị trôi, mọi người đùn đẩy trách nhiệm khi bị hỏi đến. | Áp dụng quy tắc **"Rule of One"**: 1 Action Item chỉ có **DUY NHẤT 01 Assignee** và bắt buộc kèm **01 Hard Deadline** cụ thể. |
| **Gửi Meeting Minutes quá trễ (Sau 3-4 ngày)** | Mọi người đã quên nội dung họp, công việc bị chậm mất 1/2 tuần làm việc. | Tận dụng công cụ AI Meeting Assistants (Otter.ai, Fathom, Zoom/Teams AI Companion) để tóm tắt nhanh, chỉnh sửa và gửi trong vòng **2 giờ** sau họp. |
| **Bỏ qua bước Follow-up (Theo dõi)** | Meeting Minutes viết xong bị đóng lại và lãng quên. | Dành 3 phút đầu của cuộc họp tiếp theo để **Review trạng thái các Action Items** của cuộc họp trước. |

---

## 6. NGUỒN THAM KHẢO CHẤT LƯỢNG (BLOGS, BOOKS & YOUTUBE)

1. **Chuẩn quốc tế & Sách:**
* *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) – 6th & 7th Edition* (Phần *Project Communications Management*).
* *Death by Meeting* – Patrick Lencioni (Cuốn sách kinh điển về cách tổ chức và làm chủ các cuộc họp hiệu quả).


2. **Blog chuyên ngành uy tín:**
* **Harvard Business Review (HBR):** Chuỗi bài viết *"How to Write Meeting Minutes That Actually Get Read"*.
* **Atlassian Team Playbook:** *Meeting Notes Template & Best Practices for Agile Teams*.
* **Mind the Product:** *How Product Managers Can Run Better Alignment Meetings*.


3. **Kênh YouTube tham khảo:**
* **Harvard Business Review:** Video *How to Run an Effective Meeting*.
* **Jeff Su (Productivity Expert):** Video *How to Take Actionable Meeting Notes (Template Included)*.
* **ProjectManager:** Video *How to Write Meeting Minutes Step-by-Step*.