# 04-PROJECT-MONITORING-CONTROL: BÀI 05 - VELOCITY (VẬN TỐC & NĂNG SUẤT ĐỘI NGŨ DỰ ÁN)

## 1. KHUNG KIẾN THỨC CHUẨN PMP (PMBOK 6 & 7) & LIÊN HỆ THỰC TẾ

### A. Khái niệm theo chuẩn Quản trị Dự án Quốc tế (PMP)

Trong quản lý dự án Agile/Hybrid, tốc độ không được đo bằng số giờ ngồi tại văn phòng hay số dòng code viết ra, mà được đo bằng khối lượng giá trị hoàn thành thực tế. **Velocity (Vận tốc đội ngũ)** là chỉ số định lượng năng lực thực nghiệm (**Empirical Capacity**), phản ánh tổng số điểm quy đổi (**Story Points**) hoặc User Stories mà một nhóm dự án đa chức năng hoàn tất $100\%$ theo Định nghĩa Hoàn thành (**Definition of Done - DoD**) trong một chu kỳ Sprint.

* **PMBOK 6th Edition & Agile Practice Guide:**
* Velocity gắn liền với quy trình **Estimate Activity Durations** (Ước lượng thời lượng hoạt động) và **Control Schedule** (Kiểm soát tiến độ).
* Đóng vai trò là đầu vào quan trọng cho phương pháp lập kế hoạch dựa trên năng lực thực tế (**Capacity-based Planning**), giúp xóa bỏ việc lập kế hoạch dựa trên phỏng đoán chủ quan.


* **PMBOK 7th Edition:**
* Nằm trong **Measurement Performance Domain** (Miền hiệu suất đo lường) và **Team Performance Domain**.
* PMBOK 7 nhấn mạnh rằng Velocity là một chỉ số phản ánh tính ổn định và tính dự đoán được (**Predictability**) của quy trình phát triển. Vận tốc ổn định qua 3 - 5 Sprint liên tiếp là bằng chứng cho thấy đội ngũ đã đạt trạng thái hoạt động hiệu quả (**Performing Stage** theo mô hình Tuckman).



### B. 3 Định luật Cốt lõi về Velocity (Bắt buộc phải nắm)

1. **Story Points mang tính tương đối (Relative Metric):** 30 Story Points của Team A hoàn toàn khác 30 Story Points của Team B. Tuyệt đối không quy đổi 1 Story Point ra số giờ cố định cho mọi lập trình viên.
2. **Nguyên tắc Nhị phân Hoàn thành (Binary Done):** Chỉ các User Stories đạt $100\%$ Definition of Done mới được cộng điểm vào Velocity. Một User Story 8 SP dù hoàn thành $90\%$ thì điểm ghi nhận tại cuối Sprint vẫn là **0 SP**.
3. **Không dùng Velocity làm thước đo thi đua cá nhân:** Velocity là năng suất của **cả một tập thể đa chức năng (Collective Team Performance)**. Nếu dùng Velocity để ép chỉ tiêu cá nhân, đội ngũ sẽ phản ứng bằng cách thổi phồng điểm số (Point Inflation).

---

## 2. CÔNG THỨC TÍNH TOÁN & KHUNG BẢNG THEO DÕI VELOCITY (ARTIFACTS)

### A. Các công thức toán học then chốt

#### 1. Vận tốc trung bình trượt (Rolling Average Velocity - $\bar{V}$)

Để triệt tiêu các biến động ngẫu nhiên (nghỉ phép, ngày lễ, sự cố đột xuất), ta tính trung bình cộng của 3 Sprint gần nhất:


$$\bar{V}_n = \frac{V_{n-2} + V_{n-1} + V_n}{3}$$

#### 2. Chỉ số Ổn định Tiến độ (Predictability Ratio - PR)

Đo lường mức độ tin cậy giữa cam kết đầu Sprint và kết quả thực tế bàn giao:


$$\text{PR} = \frac{\text{Completed Story Points (Điểm hoàn thành)}}{\text{Committed Story Points (Điểm cam kết)}} \times 100\%$$

* **Thang đánh giá độ tin cậy:**
* $\text{PR} < 80\%$ 🔴: Nhận quá nhiều việc (Over-commitment), xuất hiện nhiều rào cản Blocker chưa giải quyết, hoặc ước lượng quá lạc quan.
* $85\% \le \text{PR} \le 110\%$ 🟢: **Trạng thái lý tưởng**. Đội ngũ thấu hiểu năng lực bản thân, kế hoạch có độ chính xác cao.
* $\text{PR} > 120\%$ 🟡: Nhận việc quá an toàn (Under-commitment) hoặc đội ngũ đã hạ thấp tiêu chuẩn kiểm thử DoD để chạy theo điểm số.



---

### B. Khung Bảng Theo dõi Velocity (Velocity Tracking Sheet)

| Sprint ID | Cam kết đầu Sprint (Committed SP) | Hoàn thành thực tế (Completed SP) | Tỷ lệ cam kết (PR %) | Vận tốc TB trượt 3 Sprint ($\bar{V}$) | Ghi chú & Biến động nhân sự |
| --- | --- | --- | --- | --- | --- |
| **Sprint 01** | 35 SP | 22 SP | $62.8\%$ 🔴 | - | Sprint khởi động, setup môi trường CI/CD |
| **Sprint 02** | 30 SP | 26 SP | $86.7\%$ 🟢 | - | Đội ngũ bắt đầu quen với codebase |
| **Sprint 03** | 32 SP | 30 SP | $93.8\%$ 🟢 | **26.0 SP** | Nhịp độ làm việc bắt đầu ổn định |
| **Sprint 04** | 32 SP | 34 SP | $106.3\%$ 🟢 | **30.0 SP** | Quy trình phối hợp Dev-QA mượt mà |
| **Sprint 05** | 35 SP | 33 SP | $94.3\%$ 🟢 | **32.3 SP** | Hiệu suất đạt đỉnh ổn định |
| **Sprint 06** | 35 SP | 27 SP | $77.1\%$ 🔴 | **31.3 SP** | 01 Senior Backend nghỉ phép 4 ngày |

---

## 3. ỨNG DỤNG VELOCITY TRONG DỰ BÁO LỘ TRÌNH PHÁT HÀNH (RELEASE FORECASTING)

Thay vì hứa hẹn một ngày cố định thiếu cơ sở khoa học với Ban Giám đốc hoặc Khách hàng, Product Owner sử dụng Velocity để xây dựng **Dự báo xác suất 3 kịch bản**:

```
                       MÔ HÌNH DỰ BÁO TIẾN ĐỘ RELEASE
                       
  Tổng khối lượng Backlog cần bàn giao: S = 160 Story Points
  Dữ liệu lịch sử: V_min = 26 SP/Sprint | V_avg = 32 SP/Sprint | V_max = 35 SP/Sprint
  
  ┌────────────────────────────────────────────────────────────────────────┐
  │ Kịch bản Lạc quan (Optimistic):   160 / 35 = 4.57 ➔ 5 Sprints (10 tuần)│
  │ Kịch bản Thực tế (Realistic):     160 / 32 = 5.00 ➔ 5 Sprints (10 tuần)│
  │ Kịch bản Bi quan (Pessimistic):   160 / 26 = 6.15 ➔ 7 Sprints (14 tuần)│
  └────────────────────────────────────────────────────────────────────────┘

```

* **Dải dự báo ngày phát hành (Release Range):** Sản phẩm sẽ sẵn sàng bàn giao trong khoảng từ **Sprint 5 đến Sprint 7** (tương đương 10 - 14 tuần làm việc).
* **Quản trị phạm vi linh hoạt (Scope Flexibility):** Nếu Sponsor bắt buộc phải ra mắt đúng mốc Sprint 5 (10 tuần), PO sẽ chốt phạm vi chắc chắn bàn giao là:

$$\text{Scope Cố định} = 5 \times 32 = 160 \text{ SP (Tính năng Must-have)}$$



Phần còn lại sẽ được đưa sang giai đoạn Phase 2.

---

## 4. CASE STUDY THỰC TẾ: DỰ ÁN "EPIC CENTER"

* **Bối cảnh:** Ban Giám đốc công ty yêu cầu Product Owner (Duy) cam kết thời điểm phát hành tính năng lớn *"Gợi ý Lịch trình Du lịch Tự động tích hợp Homestay"*.
* **Hiện trạng Backlog:** Đội ngũ PO, BA và UI/UX đã phân tích và ước lượng toàn bộ Epic này với tổng dung lượng là **144 Story Points**.
* **Phân tích dữ liệu Velocity của Epic Center qua 5 Sprint gần nhất:**
* Nhóm dự án gồm: 1 PO, 1 UI/UX, 3 Devs, 2 QAs.
* Vận tốc 5 Sprint liên tiếp: $30 \rightarrow 32 \rightarrow 31 \rightarrow 35 \rightarrow 32 \text{ SP}$.
* Vận tốc trung bình ổn định: $\bar{V} = 32 \text{ SP/Sprint}$ (mỗi Sprint kéo dài 2 tuần).


* **Ứng dụng tính toán Release Plan:**

$$\text{Số Sprints cần thiết} = \frac{144 \text{ SP}}{32 \text{ SP/Sprint}} = 4.5 \text{ Sprints}$$


* **Hành động thích ứng thực tế:**
* PO (Duy) không làm tròn xuống 4 Sprint (quá rủi ro) mà lập kế hoạch bàn giao kéo dài **5 Sprints** (10 tuần làm việc).
* Trong 5 Sprints đó:
* Sprint 1 đến Sprint 4: Tiêu thụ $4 \times 32 = 128 \text{ SP}$ cho toàn bộ tính năng cốt lõi.
* Sprint 5: Tiêu thụ $16 \text{ SP}$ còn lại, đồng thời dành $16 \text{ SP}$ dung lượng trống (Buffer Capacity) để chạy kiểm thử tải, tối ưu trải nghiệm UI/UX và xử lý lỗi hồi quy (Regression bugs).




* **Kết quả:** Đội ngũ phát hành tính năng đúng ngày đã cam kết với chất lượng chuẩn mực, không có thành viên nào bị kiệt sức (No Burnout), tỷ lệ sai lệch tiến độ dưới $3\%$.

---

## 5. CÁC TIPS & ĐIỀU LƯU Ý THỰC CHIẾN (ANTI-PATTERNS & SOLUTIONS)

| Sai lầm phổ biến (Anti-Pattern) | Hậu quả | Giải pháp thực chiến |
| --- | --- | --- |
| **"Lạm phát Story Points" (Point Inflation)** | Khi bị ép tăng năng suất, Dev tự động nâng ước lượng task từ 3 SP lên 5 SP để làm đẹp đồ thị. | Duy trì **Baseline Reference Stories** (Các User Story mẫu chuẩn cố định 1, 2, 3, 5, 8 SP) để đối chiếu trong các buổi Backlog Refinement. |
| **So sánh Velocity giữa các Team (Cross-team comparison)** | Team bị ức chế tâm lý, dẫn đến văn hóa cạnh tranh không lành mạnh và gian lận số liệu. | Quán triệt nguyên tắc: Velocity là **chỉ số nội bộ riêng biệt của từng team**. Chỉ so sánh tính ổn định của chính team đó qua thời gian. |
| **Bỏ qua biến động nhân lực (Capacity Blindness)** | Lập kế hoạch Sprint 32 SP như bình thường dù có 2 Dev xin nghỉ phép cưới/nghỉ ốm ➔ Vỡ kế hoạch. | Kết hợp **Capacity-based Planning**: Điều chỉnh điểm cam kết của Sprint dựa trên số ngày công thực tế sẵn có ($Actual\_Days / Total\_Days \times \bar{V}$). |
| **Tính điểm cho User Story chưa xong (Partial Points)** | Ghi nhận 5 SP cho task 8 SP vì "đã dev xong chỉ chờ test", làm sai lệch năng lực bàn giao thực sự. | Giữ vững kỷ luật: **"Chưa Done theo DoD = 0 điểm"**. User Story chưa xong sẽ được chuyển sang Sprint sau và ước lượng lại phần khối lượng còn lại. |

---

## 6. NGUỒN THAM KHẢO CHẤT LƯỢNG (BLOGS, BOOKS & YOUTUBE)

1. **Chuẩn quốc tế & Sách kinh điển:**
* *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) – 6th & 7th Edition* (Phần *Measurement Performance Domain*).
* *Agile Estimating and Planning* – Mike Cohn (Cuốn sách kinh điển thế giới về Story Points, Velocity và Release Forecasting).
* *Agile Practice Guide* (Project Management Institute & Agile Alliance - Mục 5.2.7 *Predicting Delivery*).


2. **Blog chuyên ngành uy tín:**
* **Mountain Goat Software (Mike Cohn):** Chuỗi bài viết *"Velocity: What It Is, How to Use It, and What Not to Do"*.
* **Scrum.org Community:** *Why Comparing Velocity Between Teams Destroys Value*.
* **Atlassian Agile Coach:** *Velocity in Agile: How to measure and predict team performance*.


3. **Kênh YouTube tham khảo:**
* **Agile Academy:** Video *Agile Velocity Explained - How to Calculate and Use It Correctly*.
* **Development That Pays:** *Velocity in Agile: The 3 Rules You Must Follow*.
* **ScrumMastered:** Video *How to Accurately Forecast Delivery Using Velocity*.



---

