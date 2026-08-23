# 04-PROJECT-MONITORING-CONTROL: BÀI 12 - PROJECT HEALTH CHECK (ĐÁNH GIÁ ĐỊNH KỲ SỨC KHỎE DỰ ÁN)

## 1. KHUNG KIẾN THỨC CHUẨN PMP (PMBOK 6 & 7) & LIÊN HỆ THỰC TẾ

### A. Khái niệm theo chuẩn Quản trị Dự án Quốc tế (PMP)

Dự án có thể hoàn thành đúng hạn và trong ngân sách nhưng vẫn thất bại nếu đội ngũ kiệt sức hoặc sản phẩm không mang lại giá trị. **Project Health Check (Đánh giá sức khỏe dự án)** là hoạt động thanh tra và chẩn đoán toàn diện định kỳ nhằm phát hiện sớm các căn bệnh tiềm ẩn trước khi chúng biến thành khủng hoảng.

* **PMBOK 6th Edition:**
* Gắn liền với quy trình **Monitor and Control Project Work**, quy trình kiểm toán (**Audits** trong *Manage Quality*) và đánh giá hiệu suất đội ngũ (**Team Performance Assessments**).
* Kiểm tra tính tuân thủ quy trình quản trị dự án (Project Governance) và đối soát sự liên kết giữa mục tiêu dự án với kế hoạch quản lý lợi ích (**Benefits Management Plan**).


* **PMBOK 7th Edition:**
* Nằm trong mục **Diagnostics (Chẩn đoán dự án)**, **Measurement Performance Domain**, và cơ chế **Checking Results** (Kiểm tra kết quả trên toàn bộ 8 Performance Domains).
* PMBOK 7 khẳng định sức khỏe dự án là một **Hệ sinh thái tương tác đa chiều (Holistic System)**, bao gồm cả các yếu tố định lượng (KPIs, Cost, Schedule) và các yếu tố định tính vô hình (Team Morale, Tâm lý an toàn, Mức độ gắn kết của Stakeholders).



### B. Phân biệt: Status Report vs. Health Check vs. Project Audit

| Tiêu chí | Status Report (Báo cáo trạng thái) | Project Health Check (Khám sức khỏe dự án) | Project Audit (Kiểm toán dự án) |
| --- | --- | --- | --- |
| **Mục đích chính** | Cập nhật tiến độ hoàn thành công việc và số liệu hiện tại. | Chẩn đoán toàn diện "thể trạng", phát hiện nguy cơ và đề xuất giải pháp cải thiện. | Đánh giá mức độ tuân thủ quy trình, pháp lý, tài chính và chuẩn mực tổ chức. |
| **Góc nhìn tiếp cận** | Nhìn vào quá khứ & hiện tại (Output-driven). | Nhìn về tương lai & sự bền vững (Outcome & Health-driven). | Độc lập, khách quan, đối soát chứng từ (Compliance-driven). |
| **Tần suất thực hiện** | Hàng tuần / Hàng Sprint. | Định kỳ 1 - 3 tháng / Giữa dự án (Mid-term). | Theo giai đoạn (Phase-gate) hoặc cuối dự án. |
| **Người thực hiện** | Project Manager / Product Owner. | PM/PO tự đánh giá kết hợp toàn bộ Đội ngũ. | Chuyên gia kiểm toán độc lập / PMO. |

---

## 2. CẤU TRÚC BỘ CÔNG CỤ & KHUNG ĐÁNH GIÁ SỨC KHỎE (ARTIFACTS)

Một hệ thống **Health Check Framework** chuẩn mực (trên Notion, Miro hoặc Google Sheets) cần khảo sát và định lượng trên **5 Trụ cột Sức khỏe Cốt lõi**:

### A. Ma trận 5 Trụ cột Khám Sức khỏe Dự án (Project Health Matrix)

```
                            5 TRỤ CỘT SỨC KHỎE DỰ ÁN
                                       │
     ┌───────────────┬─────────────────┼─────────────────┬───────────────┐
     ▼               ▼                 ▼                 ▼               ▼
[1. DELIVERY]  [2. TECHNICAL]    [3. FINANCIAL]     [4. PEOPLE]    [5. BUSINESS]
 • Tiến độ      • Nợ kỹ thuật     • Hiệu suất vốn    • Tinh thần    • Mức độ hài lòng
 • Phạm vi      • Chất lượng      • Rủi ro chi phí   • An toàn      • Giá trị kinh doanh
 • Tắc nghẽn    • Ổn định Infra   • Chi phí Cloud    • Quá tải      • Đồng thuận Sếp

```

### B. Bảng Khung Đánh giá Sức khỏe Chi tiết (Health Check Scorecard)

*Thang điểm đánh giá: 1 (Nguy kịch 🔴) ➔ 3 (Cần chú ý 🟡) ➔ 5 (Khỏe mạnh 🟢)*

| Trụ cột đánh giá | Tiêu chí chẩn đoán (Diagnostic Questions) | Điểm số (1-5) | Hiện trạng thực tế | Hành động điều trị (Prescription) |
| --- | --- | --- | --- | --- |
| **1. Delivery & Flow (Bàn giao & Dòng chảy)** | • Tiến độ có bám sát Milestone cam kết không?<br>

<br>• Dòng chảy công việc có bị nghẽn (Blockers) kéo dài không? | **4.0 / 5** 🟢 | Vận tốc Velocity ổn định 32 SP/Sprint; không có task trễ hạn lớn. | Duy trì cơ chế Daily Walk-the-board. |
| **2. Technical & Quality (Chất lượng & Kỹ thuật)** | • Nợ kỹ thuật (Tech Debt) có được kiểm soát dưới 5% không?<br>

<br>• Mật độ lỗi và độ phủ Unit Test có đạt chuẩn không? | **2.5 / 5** 🔴 | Test coverage đạt 62% (chưa đạt chuẩn 80%); phát sinh nhiều lỗi hồi quy vặt. | Dành 20% capacity Sprint tới để viết Unit Test và refactor code. |
| **3. Financial Health (Sức khỏe Tài chính)** | • Chỉ số CPI có $\ge 1.0$ không?<br>

<br>• Chi phí hạ tầng Cloud có nằm trong ngân sách không? | **4.5 / 5** 🟢 | CPI = 1.04; chi phí AWS được tối ưu qua Reserved Instances. | Duy trì cảnh báo ngân sách tự động. |
| **4. Team Morale & Safety (Con người & Văn hóa)** | • Đội ngũ có cảm thấy an toàn tâm lý khi nói thật không?<br>

<br>• Tình trạng quá tải/làm thêm giờ (OT) có dưới mức báo động không? | **2.0 / 5** 🔴 | Khảo sát ẩn danh: Điểm hạnh phúc đạt 2.2/5; Dev kiệt sức vì nhiều thay đổi ngầm. | Cắt giảm 50% họp vụn vặt; bảo vệ vùng tập trung (Focus time). |
| **5. Stakeholder & Value (Giá trị & Sự đồng thuận)** | • Ban Giám đốc/Sponsor có thấu hiểu và ủng hộ định hướng không?<br>

<br>• Người dùng cuối có phản hồi tích cực với tính năng mới không? | **4.0 / 5** 🟢 | Sponsor đánh giá cao bản Demo gần nhất; CSAT người dùng đạt 4.2/5. | Tiếp tục duy trì Demo định kỳ cuối Sprint. |
| **ĐIỂM SỨC KHỎE TRUNG BÌNH** | $\mathbf{\bar{X} = \frac{4.0 + 2.5 + 4.5 + 2.0 + 4.0}{5}}$ | **3.4 / 5** | 🟡 **MỨC VÀNG (CẦN CAN THIỆP NGAY)** | **Ưu tiên cứu chữa: Con người & Chất lượng kỹ thuật** |

---

## 3. MÔ HÌNH THỰC THI: SPOTIFY SQUAD HEALTH CHECK MODEL

Mô hình **Squad Health Check** (do Henrik Kniberg khởi xướng tại Spotify) là phương pháp thực chứng trực quan nhất để đo lường sức khỏe nội bộ:

### Quy trình 4 bước tổ chức buổi Health Check Workshop (60 phút)

1. **Chuẩn bị Thẻ Khảo sát (Health Cards):** Chuẩn bị sẵn 8-10 khía cạnh (ví dụ: *Dễ phát hành, Giá trị mang lại, Tốc độ làm việc, Tinh thần đồng đội, Học hỏi & Phát triển, Sự hỗ trợ từ Sếp*).
2. **Bỏ phiếu Ẩn danh (Traffic Light Voting):** Từng thành viên dùng 3 màu để biểu quyết cho từng khía cạnh:
* 🟢 **Xanh (Awesome):** Mọi thứ đang diễn ra rất tuyệt vời, không cần lo lắng.
* 🟡 **Vàng (Stable):** Tạm chấp nhận được nhưng có nguy cơ tiềm ẩn.
* 🔴 **Đỏ (Painful):** Tồi tệ, gây ức chế, cần hành động cứu vãn ngay lập tức.


3. **Đánh giá Xu hướng (Trend Arrow):** Thành viên đánh giá xu hướng so với tháng trước: $\nearrow$ *(Đang tốt lên)*, $\rightarrow$ *(Giậm chân tại chỗ)*, hay $\searrow$ *(Đang tệ đi)*.
4. **Lập Kế hoạch Điều trị (Prescription Plan):** Cả nhóm thảo luận để chọn ra **DUY NHẤT 2 điểm Đỏ nhức nhối nhất** để chuyển hóa thành Action Items xử lý trong tháng.

---

## 4. CASE STUDY THỰC TẾ: DỰ ÁN "EPIC CENTER"

* **Bối cảnh:** Sau 4 tháng phát triển ứng dụng Epic Center, các báo cáo tiến độ và KPI Dashboard gửi lên Ban Giám đốc đều hiển thị màu XANH 🟢 (Velocity đạt 95%, chi phí nằm trong dự toán). Tuy nhiên, một số thành viên bắt đầu xin nghỉ phép liên tục và không khí làm việc trở nên nặng nề.
* **Tổ chức buổi Health Check định kỳ Quý 1:**
* Product Owner (Duy) cùng Scrum Master tổ chức buổi khảo sát sức khỏe ẩn danh cho toàn bộ 8 thành viên.


* **Sự thật bộc lộ (Thoát khỏi "Bẫy Dưa hấu" - Watermelon Effect):**
* Kết quả biểu quyết màu ĐỎ 🔴 tập trung tuyệt đối vào 2 hạng mục:
1. *Khía cạnh "Cảm xúc & Tải công việc":* Dev và QA đánh giá **1.8/5** $\searrow$. Lý do: Các tính năng thay đổi luồng nghiệp vụ liên tục giữa Sprint khiến họ phải đập đi xây lại trong âm thầm để kịp tiến độ bàn giao cho Sếp.
2. *Khía cạnh "Kiến trúc & Nợ kỹ thuật":* Tech Lead đánh giá **2.0/5** $\searrow$. Lý do: Hệ thống Database chưa được tối ưu hóa Index, có nguy cơ sập nếu lượng người dùng tăng đột biến vào mùa cao điểm.




* **Hành động can thiệp (Toa thuốc điều trị của PO - Duy):**
1. **Thiết lập "Maintenance & Innovation Sprint" (Sprint Dưỡng sức):** PO thống nhất với Ban Giám đốc dành trọn vẹn Sprint 9 **không nhận bất kỳ tính năng mới nào từ Kinh doanh**. Trọn vẹn 2 tuần được dùng để: Tối ưu Database, nâng độ phủ Unit Test lên 82%, và chuẩn hóa lại tài liệu API.
2. **Quy định ranh giới "Bảo vệ Đội ngũ" (Team Shielding):** PO ban hành quy tắc: Bất kỳ yêu cầu thay đổi nào xuất hiện giữa Sprint bắt buộc phải đưa vào Backlog của Sprint sau; cấm mọi hành vi giao việc trực tiếp qua tin nhắn cá nhân cho Developer.


* **Kết quả đo lường lại ở Quý 2:** Điểm sức khỏe tinh thần đội ngũ tăng từ **2.0 lên 4.4/5** 🟢; tỷ lệ lỗi hệ thống giảm 45%; năng suất bàn giao của các Sprint tiếp theo tăng trưởng bền vững mà không có bất kỳ nhân sự nào xin nghỉ việc.

---

## 5. CÁC TIPS & ĐIỀU LƯU Ý THỰC CHIẾN (ANTI-PATTERNS & SOLUTIONS)

| Sai lầm phổ biến (Anti-Pattern) | Hậu quả | Giải pháp thực chiến |
| --- | --- | --- |
| **"Hiệu ứng Dưa hấu" (Watermelon Effect)** | Báo cáo bên ngoài toàn màu XANH, nhưng thực chất bên trong ruột ĐỎ LÈ (Team sắp gãy đổ). | Đưa các chỉ số **Sức khỏe Tinh thần (Morale)** và **Nợ kỹ thuật** vào bảng báo cáo chính thức của Lãnh đạo. |
| **Biến Health Check thành buổi "Phán xét"** | Thành viên sợ bị trừ lương/khiển trách nên không dám đánh giá màu Đỏ, chỉ chấm điểm ảo để vừa lòng Sếp. | **Bảo đảm tính Ẩn danh tuyệt đối (Anonymous Voting)** và xây dựng môi trường **An toàn tâm lý (Psychological Safety)**. |
| **"Chẩn đoán mà không bốc thuốc" (Diagnose without Treatment)** | Tổ chức đánh giá rầm rộ, chỉ ra cả tá vấn đề nhưng không có hành động khắc phục nào được thực thi. | Giới hạn nghiêm ngặt: Mỗi đợt Health Check chỉ chọn **tối đa 1-2 vấn đề nghiêm trọng nhất** để đưa vào kế hoạch hành động. |
| **Chỉ nhìn vào Số liệu mà bỏ qua Con người** | Quản lý cứng nhắc chỉ nhìn vào bảng số giờ làm việc, bỏ quên cảm xúc và sự gắn kết của đội ngũ. | Kết hợp giữa **Dữ liệu định lượng (Hard Metrics)** và **Cảm nhận định tính (Soft Feedback)** qua các buổi trò chuyện 1-on-1. |

---

## 6. NGUỒN THAM KHẢO CHẤT LƯỢNG (BLOGS, BOOKS & YOUTUBE)

1. **Chuẩn quốc tế & Sách kinh điển:**
* *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) – 7th Edition* (Phần *Section 3.6 Diagnostics* & *Measurement Performance Domain*).
* *Squad Health Check Model: Visualizing What to Improve* – Henrik Kniberg (Spotify Engineering Culture).
* *The Fearless Organization: Creating Psychological Safety in the Workplace for Learning, Innovation, and Growth* – Amy C. Edmondson.


2. **Blog chuyên ngành uy tín:**
* **Atlassian Team Playbook:** *Team Health Monitor for Software & Project Teams*.
* **Crisp's Blog (Henrik Kniberg):** *Squad Health Check Model - How we do it at Spotify and Lego*.
* **ProjectManagement.com (PMI Portal):** *How to Conduct an Objective Project Health Check*.


3. **Kênh YouTube tham khảo:**
* **Spotify Engineering:** Video *Spotify Engineering Culture (Part 1 & 2 - Squad Health Checks)*.
* **Agile Academy:** Video *How to Facilitate a Spotify Squad Health Check*.
* **Continuous Delivery (Dave Farley):** Video *Measuring Team Health and Software Delivery Performance*.



---
