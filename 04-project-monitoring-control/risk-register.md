# 04-PROJECT-MONITORING-CONTROL: BÀI 02 - RISK REGISTER (SỔ ĐĂNG KÝ RỦI RO DỰ ÁN)

## 1. KHUNG KIẾN THỨC CHUẨN PMP (PMBOK 6 & 7) & LIÊN HỆ THỰC TẾ

### A. Khái niệm theo chuẩn Quản trị Dự án Quốc tế (PMP)

Quản trị rủi ro không phải là hành động né tránh sự không chắc chắn, mà là chuẩn bị sẵn sàng để làm chủ các biến số. **Risk Register (Sổ đăng ký rủi ro)** là tài liệu sống cốt lõi xuyên suốt vòng đời dự án, lưu trữ mọi dữ liệu về rủi ro từ lúc phát hiện cho đến khi đóng lại.

* **PMBOK 6th Edition:**
* Risk Register là đầu ra (Output) chính của quy trình **Identify Risks** và được liên tục cập nhật qua các quy trình:
* *Perform Qualitative Risk Analysis* (Phân tích định tính rủi ro: Đánh giá Xác suất - Probability & Mức độ ảnh hưởng - Impact).
* *Perform Quantitative Risk Analysis* (Phân tích định lượng: Tính giá trị tiền tệ kỳ vọng - EMV, mô phỏng Monte Carlo).
* *Plan Risk Responses* (Lập kế hoạch ứng phó).
* *Implement Risk Responses* & *Monitor Risks* (Thực thi và Giám sát rủi ro trong nhóm *Monitoring & Controlling*).




* **PMBOK 7th Edition & Agile/Hybrid:**
* Nằm trọng tâm trong **Uncertainty Performance Domain** (Miền hiệu suất xử lý sự bất định).
* Chuyển dịch tư duy: Rủi ro bao gồm cả **Mối đe dọa (Threats - Rủi ro tiêu cực)** và **Cơ hội (Opportunities - Rủi ro tích cực)**.
* Trong Agile/Hybrid, việc ứng phó rủi ro được tích hợp trực tiếp vào **Risk-Adjusted Backlog** (Backlog đã điều chỉnh theo rủi ro) thông qua các **Spikes** (Nghiên cứu kỹ thuật thăm dò) hoặc các User Stories dự phòng.



### B. Liên hệ Thực tế Quản lý Sản phẩm (Product Management)

* **Bản chất:** Risk Register giúp Product Manager/PO chuyển từ thế "chữa cháy bị động" (Fire-fighting) sang thế "phòng ngừa chủ động" (Fire-prevention).
* **Mục đích cốt lõi đối với Product Team:**
1. **Định lượng tác động đến Launching:** Đánh giá xem rủi ro nếu xảy ra sẽ làm dời ngày ra mắt sản phẩm bao lâu hoặc tiêu tốn thêm bao nhiêu ngân sách.
2. **Xác lập "Ngòi nổ kích hoạt" (Risk Triggers):** Nhận biết sớm các dấu hiệu cảnh báo trước khi rủi ro thực sự biến thành sự cố (Issue).
3. **Tối ưu hóa nguồn lực dự phòng (Contingency Reserves):** Giúp PM/PO bảo vệ ngân sách dự phòng có cơ sở khoa học trước CFO/Sponsor.



---

## 2. CẤU TRÚC BỘ CÔNG CỤ & KHUNG FILE RISK REGISTER (ARTIFACTS)

Một file **Risk Register** chuẩn quốc tế (trên Excel, Google Sheets, Jira hoặc Notion) cần có đầy đủ các trường thông tin tiêu chuẩn sau:

| Trường thông tin | Ý nghĩa & Quy chuẩn điền | Ví dụ minh họa |
| --- | --- | --- |
| **Risk ID** | Mã định danh duy nhất. | `RSK-042` |
| **Risk Description** | Viết theo cấu trúc chuẩn: **"Bởi vì [Nguyên nhân] -> Có thể xảy ra [Sự kiện rủi ro] -> Dẫn đến [Hậu quả]"**. | *Bởi vì chính sách Apple siết chặt quyền riêng tư (Cause), Apple có thể từ chối phê duyệt bản build iOS mới (Event), dẫn đến việc tính năng Smart Check-in bị trễ ngày Launching 2 tuần (Impact).* |
| **Category (RBS)** | Phân loại theo Cơ cấu phân chia rủi ro (*Technical, External, Organizational, Management*). | `External / App Store Policy` |
| **Probability (P)** | Xác suất xảy ra (Thang điểm 1 đến 5 hoặc *Low/Med/High*). | `4 (High - 70%)` |
| **Impact (I)** | Mức độ ảnh hưởng (Thang điểm 1 đến 5 hoặc *Low/Med/High*). | `4 (Major - Trễ tiến độ > 1 tuần)` |
| **Risk Score** | Điểm rủi ro = $P \times I$ (Thang điểm 1 - 25). | **16 (Đỏ - Nghiêm trọng)** |
| **Response Strategy** | Chiến lược ứng phó chuẩn PMP (*Mitigate, Avoid, Transfer, Accept*). | `Mitigate (Giảm thiểu)` |
| **Action Plan** | Kế hoạch hành động cụ thể để giảm thiểu P hoặc I. | *Lập tài liệu giải trình chi tiết về quyền truy cập Bluetooth và quay video demo luồng cấp quyền gửi trước cho Apple Review Team.* |
| **Risk Trigger** | Dấu hiệu cảnh báo sớm để kích hoạt Action Plan. | *Apple gửi thông báo cảnh báo cập nhật Privacy Manifest trước 30 ngày.* |
| **Risk Owner** | **DUY NHẤT 01 cá nhân** theo dõi và chịu trách nhiệm hành động. | *Duy (Product Owner)* |
| **Status** | Trạng thái rủi ro (`Identified`, `Mitigating`, `Occurred - Moved to Issue`, `Closed`). | `Mitigating` |

---

## 3. MA TRẬN ĐÁNH GIÁ & CHIẾN LƯỢC ỨNG PHÓ RỦI RO (RISK STRATEGIES)

### A. Ma trận Xác suất & Tác động (Probability and Impact Matrix)

Ma trận giúp trực quan hóa thứ tự ưu tiên xử lý rủi ro:

* **Vùng Đỏ (Điểm 15 - 25 - Rủi ro Nghiêm trọng):** Bắt buộc phải có kế hoạch ứng phó chi tiết, theo dõi hàng ngày và báo cáo định kỳ cho Ban Giám đốc/Sponsor.
* **Vùng Vàng (Điểm 6 - 14 - Rủi ro Trung bình):** Lập kế hoạch theo dõi định kỳ hàng tuần, chuẩn bị sẵn giải pháp tình thế.
* **Vùng Xanh (Điểm 1 - 5 - Rủi ro Thấp):** Đưa vào danh sách theo dõi thụ động (**Watchlist**), chấp nhận rủi ro nếu chi phí xử lý lớn hơn thiệt hại tiềm năng.

### B. 4 Chiến lược Ứng phó Rủi ro Tiêu cực (Threats) chuẩn PMP

1. **Avoid (Né tránh):** Thay đổi hẳn kế hoạch/phạm vi để loại bỏ hoàn toàn nguyên nhân gây rủi ro (Ví dụ: Bỏ không dùng công nghệ A chưa ổn định mà chọn công nghệ B đã kiểm chứng).
2. **Mitigate (Giảm thiểu):** Giảm xác suất xảy ra hoặc giảm mức độ thiệt hại (Ví dụ: Viết Unit Test tự động, chạy Load test trước khi Release).
3. **Transfer (Chuyển giao):** Chuyển giao trách nhiệm/thiệt hại tài chính cho bên thứ ba (Ví dụ: Mua bảo hiểm an ninh mạng, thuê dịch vụ Cloud có cam kết SLA bồi thường).
4. **Accept (Chấp nhận):** * *Chấp nhận chủ động (Active Acceptance):* Trích lập ngân sách dự phòng (**Contingency Reserve**) và thời gian dự phòng.
* *Chấp nhận thụ động (Passive Acceptance):* Không làm gì cả, khi nào xảy ra thì xử lý theo Issue thông thường.



---

## 4. CASE STUDY THỰC TẾ: DỰ ÁN "EPIC CENTER"

* **Bối cảnh:** Ứng dụng Epic Center chuẩn bị bước vào chiến dịch Siêu Sale mùa du lịch (Dự kiến lưu lượng người dùng truy cập đặt phòng tăng gấp 10 lần ngày thường).
* **Nhận diện Rủi ro đưa vào Risk Register:**
* **Risk ID:** `RSK-058`
* **Mô tả:** *Bởi vì lượng truy cập đặt phòng tăng đột biến trong khung giờ Flash Sale (Cause), hệ thống Database có thể bị nghẽn I/O và treo dịch vụ (Event), dẫn đến việc người dùng không thể thanh toán và gây thiệt hại doanh thu ước tính 500 triệu VNĐ (Impact).*
* **Đánh giá ban đầu:** Probability = 4, Impact = 5 ➔ **Risk Score = 20 (Vùng Đỏ - Critical)**.
* **Chiến lược:** `Mitigate` (Giảm thiểu).
* **Action Plan thực thi:**
1. Đội DevOps thiết lập cơ chế **Auto-scaling** tự động tăng số lượng Pods/Instances khi CPU vượt quá 70%.
2. Backend Team cấu hình bộ nhớ đệm **Redis Cache** cho toàn bộ dữ liệu danh sách phòng và giá để giảm 80% tải đọc trực tiếp từ Database chính.
3. Mua thêm gói hỗ trợ kỹ thuật chuyên gia 24/7 từ AWS trong 3 ngày diễn ra sự kiện.


* **Đánh giá Rủi ro còn lại (Residual Risk):** Sau khi thực thi các biện pháp trên, Xác suất giảm từ 4 xuống 1, Mức độ ảnh hưởng giảm từ 5 xuống 2 ➔ **Risk Score còn lại = 2 (Vùng Xanh - An toàn)**.


* **Kết quả thực tế:** Vào ngày Flash Sale, lượng truy cập chạm mốc 50,000 người dùng đồng thời (CCU), hệ thống tự động scale mượt mà, tỷ lệ giao dịch thành công đạt 99.85%.

---

## 5. CÁC TIPS & ĐIỀU LƯU Ý THỰC CHIẾN (ANTI-PATTERNS & SOLUTIONS)

| Sai lầm phổ biến (Anti-Pattern) | Hậu quả | Giải pháp thực chiến |
| --- | --- | --- |
| **"Mô tả rủi ro mơ hồ" (Vague Risks)** | Ghi chung chung: *"Dự án có thể bị chậm"* khiến team không biết nguyên nhân do đâu để xử lý. | Bắt buộc áp dụng công thức PMP: **Nguyên nhân (If/Because) ➔ Sự kiện (Event) ➔ Hậu quả (Impact)**. |
| **"Sổ đăng ký ma" (Ghost Risk Register)** | Lập Risk Register hoành tráng lúc khởi tạo dự án rồi cất vào ngăn kéo, không bao giờ mở lại. | Tổ chức **Risk Review định kỳ (Bi-weekly)**: Đánh giá lại điểm P và I, đóng các rủi ro đã qua mốc thời gian và bổ sung rủi ro mới. |
| **Nhầm lẫn giữa Kế hoạch phòng ngừa và Kế hoạch ứng biến** | Chỉ nghĩ cách khắc phục khi sự cố đã nổ ra mà quên mất việc ngăn chặn từ trước. | Phân biệt rõ: **Mitigation Plan** (Làm NGAY để giảm rủi ro) vs. **Contingency Plan** (Chỉ làm KHI rủi ro đã chuyển thành Issue). |
| **Rủi ro không có "Người gác đền" (Risk Owner)** | Mọi người nghĩ rủi ro là của chung, không ai theo dõi dấu hiệu kích hoạt (Trigger). | Mỗi dòng trong Risk Register bắt buộc phải có **chính xác 01 Risk Owner**. Owner không nhất thiết phải tự làm, nhưng chịu trách nhiệm giám sát. |

---

## 6. NGUỒN THAM KHẢO CHẤT LƯỢNG (BLOGS, BOOKS & YOUTUBE)

1. **Chuẩn quốc tế & Sách kinh điển:**
* *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) – 6th & 7th Edition* (Chương *Project Risk Management* & *Uncertainty Domain*).
* *The Standard for Risk Management in Portfolios, Programs, and Projects* – Project Management Institute (PMI).
* *Waltzing with Bears: Managing Risk on Software Projects* – Tom DeMarco & Timothy Lister (Cuốn sách gối đầu giường về quản trị rủi ro phần mềm).


2. **Blog chuyên ngành uy tín:**
* **ProjectManagement.com:** Chuỗi bài viết *"Practical Risk Register Guidelines for Agile/Hybrid Projects"*.
* **Mountain Goat Software (Mike Cohn):** *Managing Risk on Agile Projects with Risk-Adjusted Backlogs*.
* **Continuous Delivery Blog:** *Risk Management in Modern DevOps and Continuous Deployment*.


3. **Kênh YouTube tham khảo:**
* **Praizion Performance Management:** Video *Risk Management Process Breakdown for PMP*.
* **ProjectManager:** Video *How to Create a Risk Register - Step-by-Step Guide*.
* **Agile Academy:** *Risk Management in Agile - How to Handle Uncertainties*.



---