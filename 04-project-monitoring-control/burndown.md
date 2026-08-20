# 04-PROJECT-MONITORING-CONTROL: BÀI 04 - BURNDOWN (BIỂU ĐỒ TIẾN ĐỘ DỰ ÁN & VÒNG LẶP SPRINT)

## 1. KHUNG KIẾN THỨC CHUẨN PMP (PMBOK 6 & 7) & LIÊN HỆ THỰC TẾ

### A. Khái niệm theo chuẩn Quản trị Dự án Quốc tế (PMP)

Theo dõi tiến độ trong môi trường biến động không đơn thuần là đếm số ngày đã trôi qua, mà là định lượng khối lượng công việc còn lại so với quỹ thời gian khả dụng. **Burndown Chart (Biểu đồ tiến độ còn lại)** là một trong những công cụ trực quan hóa tiến độ cơ bản và mạnh mẽ nhất của trường phái Agile/Hybrid.

* **PMBOK 6th Edition & Agile Practice Guide:**
* Thuộc nhóm quy trình **Monitoring and Controlling Process Group**, trực tiếp phục vụ quy trình *Control Schedule* (Kiểm soát tiến độ) và *Monitor and Control Project Work*.
* Đóng vai trò là một **Information Radiator** (Bộ phát thông tin trực quan) đặt tại không gian làm việc chung để toàn bộ nhóm dự án và Stakeholders nắm bắt trạng thái tiến độ mà không cần thông qua báo cáo trung gian.
* Phản ánh kỹ thuật phân tích xu hướng (**Trend Analysis**), so sánh đường tiến độ thực tế (**Actual Work Remaining**) với đường cơ sở lý tưởng (**Ideal Burndown Line**).


* **PMBOK 7th Edition:**
* Nằm trọng tâm trong **Measurement Performance Domain** (Miền hiệu suất đo lường) và **Delivery Performance Domain**.
* Chuyển dịch trọng tâm từ việc theo dõi giờ công lao động (Man-hours) sang đo lường khối lượng giá trị/độ phức tạp còn lại thông qua **Story Points** hoặc **User Stories**.
* Cung cấp cơ chế cảnh báo sớm (Early Warning System) giúp nhóm tự tổ chức (Self-Organizing Team) phát hiện nguy cơ vỡ kế hoạch ngay từ giữa Sprint để chủ động cắt tỉa phạm vi (Scope Pruning) thay vì đợi đến hạn chót mới đối phó.



---

## 2. PHÂN LOẠI BURNDOWN & SO SÁNH VỚI BURNUP CHART

Để lựa chọn đúng công cụ kiểm soát cho từng cấp độ quản lý, người làm dự án cần phân biệt rõ các biến thể của biểu đồ:

```
                      CÁC CẤP ĐỘ THEO DÕI TIẾN ĐỘ
                      
  ┌─────────────────────────────────────────────────────────────┐
  │ 1. Sprint / Iteration Burndown (Cấp độ Đội ngũ - Vi mô)    │
  │    • Đơn vị: Story Points hoặc Giờ công (Task Hours)        │
  │    • Trục hoành: 10 - 14 ngày làm việc của 1 Sprint         │
  │    • Mục đích: Kiểm soát dòng chảy công việc hàng ngày      │
  └─────────────────────────────────────────────────────────────┘
                                │
                                ▼
  ┌─────────────────────────────────────────────────────────────┐
  │ 2. Release / Epic Burndown (Cấp độ Sản phẩm - Vĩ mô)        │
  │    • Đơn vị: Tổng Story Points của toàn bộ Release/Epic     │
  │    • Trục hoành: Chuỗi 4 - 8 Sprints liên tiếp              │
  │    • Mục đích: Dự báo ngày Launching phiên bản chính thức   │
  └─────────────────────────────────────────────────────────────┘

```

### So sánh chuyên sâu: Burndown Chart vs. Burnup Chart

| Tiêu chí so sánh | Burndown Chart (Biểu đồ đốt việc) | Burnup Chart (Biểu đồ tích lũy việc) |
| --- | --- | --- |
| **Cách thức thể hiện** | Vẽ đường dốc xuống từ Tổng khối lượng về $0$. | Vẽ đường dốc lên từ $0$ tiến tới Đường tổng phạm vi (Total Scope Line). |
| **Độ rõ ràng về Scope Creep** | **Kém:** Khi tổng phạm vi tăng, đường thực tế đột ngột nhảy dựng lên, dễ gây hiểu lầm là team làm việc chậm. | **Rất tốt:** Tách riêng 2 đường: *Đường tổng phạm vi* và *Đường công việc đã hoàn thành*, giúp thấy rõ việc chậm do năng suất hay do bị nhồi thêm việc. |
| **Đối tượng phù hợp** | Đội ngũ phát triển (Dev, QA, PO) theo dõi nội bộ hàng ngày trong Sprint. | Ban điều hành (C-Level, Sponsor, Khách hàng) theo dõi tiến độ tổng thể của toàn bộ Dự án / Release lớn. |

---

## 3. GIẢI MÃ CÁC HÌNH THÁI ĐẶC TRƯNG CỦA SPRINT BURNDOWN (DIAGNOSTIC PATTERNS)

Biểu đồ Burndown là "bản chụp X-quang" phản ánh chính xác sức khỏe vận hành của đội ngũ. Dưới đây là 4 hình thái phổ biến nhất và phương pháp chẩn đoán:

```
(A) Vực Thẳm Cuối Kỳ (Cliff / Hockey-Stick)   (B) Đường Bằng Phẳng Bế Tắc (Flatline)
Remaining SP                                  Remaining SP
 40 ──┐                                        40 ───────┐
      │                                                  │
 20   │          ┌───┐                         20        │
      │          │   │                                   └───┐
  0 ──┴──────────┴───┴─────►                    0 ───────────┴───►
      Day 1     Day 9 Day 10                       Day 1     Day 9 Day 10
 (Dồn hết việc sang ngày cuối)                (Bị nghẽn dòng chảy / Chờ đợi)

(C) Bậc Thang Đi Lên (Scope Creep)            (D) Dòng Chảy Lý Tưởng (Ideal Flow)
Remaining SP                                  Remaining SP
 50         ┌───┐                              40 ──┐
 40 ──┐  ┌──┘   └───┐                                └──┐
 30   └──┘          │                          20       └──┐
  0 ────────────────┴─────►                     0 ─────────┴─────►
      Day 1     Day 5 Day 10                       Day 1     Day 5 Day 10
 (Bị bơm thêm việc giữa Sprint)                (Tiêu thụ công việc đều đặn)

```

### Chẩn đoán chi tiết:

1. **Hình thái A - Vực thẳm cuối kỳ (Hockey-Stick Drop):**
* *Hiện tượng:* Đồ thị đi ngang suốt 8 ngày đầu, sau đó lao dốc thẳng đứng vào ngày cuối cùng của Sprint.
* *Nguyên nhân:* User Story quá lớn (chưa được chia nhỏ), Dev ôm việc đến khi hoàn thành 100% mới kéo thẻ, hoặc QA bị dồn việc kiểm thử vào 2 ngày cuối cùng.


2. **Hình thái B - Đường bằng phẳng bế tắc (Flatline):**
* *Hiện tượng:* Đồ thị đi ngang nhiều ngày liên tiếp và kết thúc Sprint vẫn còn lượng lớn Story Points chưa đốt được.
* *Nguyên nhân:* Team gặp rào cản kỹ thuật nghiêm trọng (Blocker), phụ thuộc bên ngoài chưa giải quyết, hoặc ước lượng sai lệch quá lớn so với năng lực thực tế.


3. **Hình thái C - Bậc thang đi lên (Upward Staircase):**
* *Hiện tượng:* Điểm Story Points tăng ngược lên giữa chu kỳ Sprint.
* *Nguyên nhân:* Phạm vi bị phình to (Scope Injection) do PO hoặc Stakeholders tự ý đưa thêm User Stories mới vào khi Sprint đang chạy mà không hoãn task cũ tương đương.


4. **Hình thái D - Dòng chảy đều đặn (Healthy Step-down):**
* *Hiện tượng:* Đồ thị bám sát đường cơ sở lý tưởng, giảm dần theo từng bậc thang nhỏ qua từng ngày.
* *Nguyên nhân:* User Stories được chia nhỏ (1-2 ngày/task), QA test cuốn chiếu liên tục ngay khi Dev xong từng phần, quy trình phối hợp mượt mà.



---

## 4. CASE STUDY THỰC TẾ: DỰ ÁN "EPIC CENTER"

* **Bối cảnh:** Ở Sprint 7, đội ngũ phát triển ứng dụng Epic Center (gồm 1 PO, 1 UI/UX Designer, 3 Devs, 2 QAs) cam kết **42 Story Points** cho mục tiêu hoàn thiện module *Đồng bộ Lịch phòng Homestay*.
* **Tín hiệu cảnh báo từ Burndown Chart:**
* Đến ngày thứ 5 của Sprint (một nửa chặng đường 10 ngày), biểu đồ Sprint Burndown hoàn toàn **đi ngang ở mốc 42 SP**, chưa có bất kỳ Story Point nào được chuyển sang cột `Done`.


* **Phân tích nguyên nhân tại buổi Daily Standup ngày thứ 5:**
* PO (Duy) cùng Tech Lead kiểm tra trực quan bảng Kanban:
* Có **5 User Stories** đều đang ở trạng thái `In Progress`.
* Mỗi User Story có kích thước quá lớn (8 - 13 Story Points/story), bao gồm cả Backend, Frontend, UI Mobile và Logic đồng bộ Google Calendar.
* Dev A viết xong API nhưng không thể chuyển Done vì chờ Dev B hoàn thiện giao diện Mobile; QA hoàn toàn ngồi chờ mà không có bản build độc lập để test.




* **Hành động can thiệp tức thì (Mid-sprint Course Correction):**
1. **Story Slicing (Cắt nhỏ User Story):** PO cùng team lập tức bẻ nhỏ 5 Stories lớn thành **12 Task độc lập** (mỗi task chỉ từ 2 - 3 SP). Tách riêng phần API Endpoint, UI Component và Logic Sync.
2. **Áp dụng Giới hạn công việc đang xử lý (WIP Limit = 3):** Quy định tại một thời điểm, toàn team chỉ được phép có tối đa 3 items ở cột `In Progress`. Cấm mở task mới khi task cũ chưa được đẩy sang cột Testing/Done.
3. **Kích hoạt luồng Test cục bộ (Mock Testing):** QA sử dụng Postman kiểm thử ngay các API đã xong mà không cần đợi giao diện hoàn thiện.


* **Kết quả đo lường lại:**
* Từ ngày thứ 6 trở đi, biểu đồ Burndown bắt đầu "đốt" đều đặn 6 - 8 SP mỗi ngày.
* Kết thúc Sprint 7, team hoàn thành **38/42 SP** (đạt 90.5% mục tiêu cam kết), module cốt lõi chạy ổn định mà toàn bộ đội ngũ không phải làm thêm giờ (No OT) vào cuối tuần.



---

## 5. CÁC TIPS & ĐIỀU LƯU Ý THỰC CHIẾN (ANTI-PATTERNS & SOLUTIONS)

| Sai lầm phổ biến (Anti-Pattern) | Hậu quả | Giải pháp thực chiến |
| --- | --- | --- |
| **"Tính điểm hoàn thành dở dang" (Partial Story Points)** | Task 8 SP làm được 80% thì tự ý ghi nhận 6.4 SP vào Burndown, tạo ra cảm giác tiến độ ảo. | **Nguyên tắc nhị phân 0-100:** Chỉ có 2 trạng thái: `Chưa xong (0 SP)` hoặc `Hoàn thành 100% theo Definition of Done (Full SP)`. Tuyệt đối không tính điểm nửa vời. |
| **Dùng Burndown làm công cụ chấm điểm cá nhân** | Dev đối phó bằng cách ước lượng khống điểm (Point Inflation) hoặc chia nhỏ task vụn vặt để lấy thành tích. | Burndown là **thước đo của toàn bộ Đội ngũ (Team Metric)**, không phải là bảng KPI đánh giá từng cá nhân. |
| **Chỉ cập nhật trạng thái vào cuối Sprint** | Mất hoàn toàn chức năng cảnh báo sớm của công cụ; dữ liệu tiến độ bị mù mờ suốt chu kỳ. | Cập nhật trạng thái Task Board **hàng ngày (Real-time)**, tốt nhất là ngay trong hoặc trước buổi họp Daily Standup sáng. |
| **Bỏ qua các User Story bị nghẽn (Blocked Stories)** | Thẻ task nằm im nhiều ngày nhưng không ai tìm hiểu nguyên nhân, làm bẹp phẳng đường đồ thị. | Gắn nhãn `[FLAG / BLOCKED]` nổi bật màu đỏ ngay khi phát sinh rào cản; chuyển thành **Issue** nếu không tự gỡ được sau 24h. |

---

## 6. NGUỒN THAM KHẢO CHẤT LƯỢNG (BLOGS, BOOKS & YOUTUBE)

1. **Chuẩn quốc tế & Sách kinh điển:**
* *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) – 6th & 7th Edition* (Phần *Control Schedule* & *Measurement Domain*).
* *Agile Practice Guide* (PMI & Agile Alliance - Mục 5.2.7 *Visual Storytelling and Metrics*).
* *Scrum and XP from the Trenches* – Henrik Kniberg (Chương thực hành theo dõi tiến độ bằng Burndown trực quan).


2. **Blog chuyên ngành uy tín:**
* **Mountain Goat Software (Mike Cohn):** Chuỗi bài viết *"Feel the Burn: A Guide to Burndown Charts"*.
* **Atlassian Agile Coach:** *Burndown charts: What they are and how to use them effectively in Jira*.
* **Scrum.org Community Blog:** *Burndown Chart Antipatterns and How to Remedy Them*.


3. **Kênh YouTube tham khảo:**
* **Agile Academy:** Video *Sprint Burndown Chart Explained - How to Read & Analyze*.
* **Development That Pays:** *Burndown Charts: Don’t Let Them Fool You!*.
* **ScrumMastered:** Video *How to Use a Burndown Chart to Improve Sprint Delivery*.



