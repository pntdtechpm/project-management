# 03-PROJECT-EXECUTION: BÀI 01 - DAILY TRACKING (THEO DÕI TIẾN ĐỘ HÀNG NGÀY)

## 1. Khung kiến thức chuẩn PMP (PMBOK 6 & 7) & liên hệ thực tế

### A. Khái niệm theo chuẩn quản trị dự án quốc tế (PMP)

**PMBOK 6th Edition:**

- Daily Tracking nằm ở giao điểm của nhóm quy trình **Executing** (*Direct and Manage Project Work*) và **Monitoring & Controlling** (*Monitor and Control Project Work*).
- Mục tiêu chính là thu thập dữ liệu thực hiện công việc (**Work Performance Data**), biến đổi thành thông tin (**Work Performance Information**) nhằm phát hiện sớm các lệch lạc so với đường cơ sở (Baseline).

**PMBOK 7th Edition & Agile Practice Guide:**

- Thuộc **Project Work Performance Domain** và **Measurement Performance Domain**.
- Chuyển dịch tư duy từ "giám sát & kiểm soát" (*control*) sang "tối ưu hóa dòng chảy giá trị" (*optimizing flow*) và thúc đẩy sự chủ động của đội ngũ tự quản (**Self-Organizing Team**).
- Trong môi trường Agile/Hybrid, hoạt động này được cụ thể hóa bằng buổi họp **Daily Standup / Daily Scrum** với nguyên tắc đóng khung thời gian (**timebox <= 15 phút**) diễn ra hằng ngày.

### B. Liên hệ thực tế quản lý sản phẩm (Product Management)

**Bản chất:** Daily Tracking **không phải là điểm danh hay báo cáo chấm công** cho PM/PO.

**Mục đích cốt lõi:**

1. Đồng bộ hóa mục tiêu làm việc trong ngày hướng tới **Sprint Goal**.
2. Minh bạch hóa trạng thái dòng chảy công việc trên **Task Board / Kanban Board**.
3. Nhận diện và gỡ bỏ sớm các rào cản (**Impediments / Blockers**) làm đình trệ tiến độ.

---

## 2. Bộ công cụ & artifacts cần có

### 1. Task Board trực quan (Kanban / Scrum Board)

- Trạng thái dòng chảy đề xuất: `To Do` -> `In Progress` (áp dụng hạn ngạch công việc - WIP Limit) -> `Review (Code/Design)` -> `Testing (QA)` -> `Done`.
- Công cụ phổ biến: Jira, ClickUp, Trello, Notion.

### 2. Chỉ số đo lường tiến độ (Agile Metrics)

- **Burndown Chart:** Theo dõi lượng khối lượng công việc (Story Points / Tasks) còn lại qua từng ngày của sprint.
- **Cumulative Flow Diagram (CFD):** Phát hiện nhanh công đoạn đang bị ứ đọng công việc (Bottlenecks).

---

## 3. Khung câu hỏi & phương pháp triển khai

### A. Mô hình 3 câu hỏi Scrum truyền thống

1. *Hôm qua tôi đã hoàn thành việc gì để đóng góp vào Sprint Goal?*
2. *Hôm nay tôi sẽ làm gì để đóng góp vào Sprint Goal?*
3. *Tôi có đang gặp khó khăn/rào cản (Blocker) nào ngáng đường không?*

### B. Mô hình nâng cao cho Product Team: Walk the Board

Thay vì hỏi lần lượt từng cá nhân, dễ biến thành buổi báo cáo đối phó, PM/PO cùng team duyệt board theo hướng **từ phải qua trái**: bắt đầu từ các công việc sắp hoàn thành nhất.

- *Thẻ này ở cột Testing cần thêm điều kiện gì để chuyển sang Done ngay hôm nay?*
- *User Story này ở cột In Progress đã giậm chân tại chỗ 3 ngày rồi, ai đang gặp vướng mắc gì không?*

---

## 4. Case study thực tế

**Dự án:** Phát triển tính năng đặt đa dịch vụ (Multi-service Booking) trên ứng dụng Epic Center.

**Bối cảnh:** Buổi họp Daily Standup vào ngày thứ 4 của sprint, đội ngũ gồm 1 PO, 1 UI/UX Designer, 3 Devs và 2 QAs.

**Hiện trạng phát hiện:** Task *"Tích hợp cổng thanh toán MoMo"* bị kẹt ở cột *In Progress* ngày thứ 3 liên tiếp.

**Rào cản (Blocker):** Phía đối tác MoMo đột xuất bảo trì môi trường thử nghiệm (Sandbox API), khiến Dev không thể test luồng callback và QA bị hoãn việc test.

**Hành động xử lý:** Tech Lead chủ động đề xuất dựng ngay một **Mock API** giả lập phản hồi nội bộ trong ngày để Dev & QA tiếp tục hoàn thiện giao diện UI/UX và logic ứng dụng mà không phải ngồi chờ đối tác.

**Kết quả:** Sprint Goal không bị vỡ; tiến độ công việc được duy trì liên tục.

---

## 5. Các tips & điều lưu ý thực chiến (Anti-patterns & Solutions)

| Sai lầm phổ biến (Anti-Pattern) | Nguyên nhân gốc rễ | Giải pháp thực chiến |
| --- | --- | --- |
| **Cuộc họp kéo dài quá 15 phút** | Sa lầy vào việc tranh luận giải pháp kỹ thuật chi tiết. | Sử dụng quy tắc **Parking Lot**: đưa các chủ đề kỹ thuật sâu vào buổi thảo luận riêng ngay sau Daily, chỉ gồm những người liên quan. |
| **Thành viên báo cáo mang tính đối phó** | Xem PM/PO là "sếp" đến kiểm tra công việc thay vì là người hỗ trợ. | PM/PO đóng vai trò **Servant Leader**; lùi lại phía sau và giao quyền dẫn dắt (Facilitator) luân phiên cho các thành viên. |
| **Dời lịch họp liên tục, không đều** | Lịch làm việc cá nhân chồng chéo, thiếu tính kỷ luật. | Đóng khung giờ cố định, ví dụ đúng 9:15 AM hằng ngày. Đúng giờ là tiến hành, không chờ đợi cá nhân đi muộn. |
| **Phát hiện Blocker nhưng không gỡ** | Thiếu người chịu trách nhiệm theo sát rào cản (Impediment Owner). | Chuyển ngay các blocker phức tạp vào **Issue Log** và phân công Scrum Master/PM theo dõi gỡ bỏ. |

---

## 6. Nguồn tham khảo chất lượng (Blogs & YouTube)

### 1. Chuẩn quốc tế & sách

- *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) - 6th & 7th Edition* (Project Management Institute).
- *Agile Practice Guide* (PMI & Agile Alliance).

### 2. Blog chuyên ngành uy tín

- **Mountain Goat Software (Mike Cohn):** Các bài viết chuyên sâu về *Daily Standup Meeting Best Practices*.
- **Scrum.org:** *Common Daily Scrum Anti-Patterns and How to Fix Them*.
- **Atlassian Agile Coach:** *How to run an effective daily standup meeting*.

### 3. Kênh YouTube tham khảo

- **Development That Pays:** Chuỗi video *Daily Standup Meetings - Rules for Success*.
- **Agile Academy:** *Daily Scrum Explained in 5 Minutes*.
