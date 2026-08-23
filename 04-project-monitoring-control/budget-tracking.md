# 04-PROJECT-MONITORING-CONTROL: BÀI 06 - BUDGET TRACKING (THEO DÕI NGÂN SÁCH & HIỆU SUẤT TÀI CHÍNH DỰ ÁN)

## 1. KHUNG KIẾN THỨC CHUẨN PMP (PMBOK 6 & 7) & LIÊN HỆ THỰC TẾ

### A. Khái niệm theo chuẩn Quản trị Dự án Quốc tế (PMP)

Theo dõi ngân sách không đơn thuần là việc ghi chép sổ sách thu chi kế toán. Trong quản trị dự án chuyên nghiệp, **Budget Tracking** là hoạt động đo lường tương quan giữa **khối lượng giá trị công việc đã tạo ra** so với **số tiền thực tế đã tiêu tốn** tại từng thời điểm.

* **PMBOK 6th Edition:**
* Thuộc nhóm quy trình **Monitoring and Controlling Process Group**, trực tiếp là quy trình **Control Costs** (Kiểm soát chi phí).
* Sử dụng phương pháp luận cốt lõi **Quản lý Giá trị Thu được (Earned Value Management - EVM)** để phân tích chênh lệch chi phí, chênh lệch tiến độ và dự báo tổng chi phí khi hoàn thành dự án.
* Giám sát việc sử dụng Đường cơ sở Chi phí (**Cost Baseline**) và Quỹ dự phòng rủi ro (**Contingency Reserve & Management Reserve**).


* **PMBOK 7th Edition & Agile/Hybrid:**
* Nằm trong **Measurement Performance Domain** (Miền hiệu suất đo lường) và **Planning Performance Domain**.
* Chuyển dịch từ việc "quản lý ngân sách cố định một lần" (Fixed Upfront Budget) sang "cấp vốn theo gia số giá trị" (**Incremental Funding / Dynamic Budgeting**).
* Trong môi trường Agile/Tech, ngân sách được kiểm soát thông qua tốc độ đốt tiền (**Burn Rate**), chi phí trên mỗi Sprint (**Cost per Sprint**) và chi phí trên mỗi điểm giá trị (**Cost per Story Point**).



### B. Liên hệ Thực tế Quản lý Sản phẩm (Product Management)

* **Cơ cấu chi phí trong dự án phần mềm/sản phẩm số hiện đại:**
1. **Chi phí Nhân sự (Labor Costs - 70-80%):** Lương thưởng, phúc lợi của đội ngũ (PO, UI/UX, Dev, QA, DevOps).
2. **Chi phí Hạ tầng & Đám mây (Cloud & SaaS Infrastructure):** Chi phí biến đổi hàng tháng từ AWS, Google Cloud, Docker, CDN, Sentry, Jira...
3. **Chi phí Đối tác bên thứ ba (Third-party APIs & Licenses):** Phí bản quyền SDK (eKYC, Map APIs, Cổng thanh toán, SMS OTP).
4. **Phân bổ CapEx vs. OpEx:** Phân định rõ chi phí đầu tư phát triển tài sản vô hình (CapEx - R&D tính năng mới) và chi phí vận hành bảo trì thường xuyên (OpEx).



---

## 2. PHƯƠNG PHÁP QUẢN TRỊ TÀI CHÍNH CỐT LÕI: EARNED VALUE MANAGEMENT (EVM)

EVM là phương pháp duy nhất tích hợp cả 3 yếu tố: **Phạm vi (Scope) - Tiến độ (Schedule) - Chi phí (Cost)** vào một hệ thống đo lường thống nhất.

### A. 3 Đại lượng Nền tảng của EVM

| Đại lượng | Tên tiếng Anh | Định nghĩa chuẩn PMP | Ý nghĩa thực tiễn |
| --- | --- | --- | --- |
| **PV** | **Planned Value** | Giá trị kế hoạch của khối lượng công việc *lẽ ra phải hoàn thành* tính đến thời điểm hiện tại. | *Theo kế hoạch, đến hôm nay tôi phải làm xong khối lượng việc trị giá bao nhiêu tiền?* |
| **EV** | **Earned Value** | Giá trị thực tế của khối lượng công việc *đã hoàn thành thực sự* tính đến thời điểm hiện tại. | *Thực tế khối lượng công việc đã hoàn thành tương đương bao nhiêu tiền theo đơn giá kế hoạch?* |
| **AC** | **Actual Cost** | Tổng chi phí thực tế *đã chi trả* để hoàn thành khối lượng công việc tương ứng với EV. | *Thực tế tôi đã rút hầu bao chi hết bao nhiêu tiền?* |

---

### B. Hệ thống Chỉ số Phân tích & Dự báo Tài chính (Bắt buộc phải nắm)

#### 1. Đo lường Hiệu suất (Variances & Indices)

* **Chênh lệch Chi phí (Cost Variance - CV):**

$$\text{CV} = \text{EV} - \text{AC}$$


* $\text{CV} > 0$ 🟢: Tiết kiệm chi phí (Under Budget).
* $\text{CV} < 0$ 🔴: Bị vượt ngân sách (Over Budget).


* **Chỉ số Hiệu suất Chi phí (Cost Performance Index - CPI):**

$$\text{CPI} = \frac{\text{EV}}{\text{AC}}$$


* $\text{CPI} > 1.0$ 🟢: Sử dụng vốn hiệu quả (Mỗi $1 tiêu ra thu về $> $1 giá trị).
* $\text{CPI} < 1.0$ 🔴: Sử dụng vốn kém hiệu quả (Báo động tài chính).


* **Chỉ số Hiệu suất Tiến độ (Schedule Performance Index - SPI):**

$$\text{SPI} = \frac{\text{EV}}{\text{PV}}$$


* $\text{SPI} \ge 1.0$ 🟢: Tiến độ đúng hạn hoặc vượt kế hoạch.
* $\text{SPI} < 1.0$ 🔴: Dự án đang bị trễ tiến độ.



#### 2. Dự báo Tương lai (Forecasting Formulas)

* **Tổng ngân sách được duyệt ban đầu (Budget at Completion - BAC):** Tổng ngân sách kế hoạch toàn bộ dự án.
* **Dự toán Tổng chi phí khi hoàn thành (Estimate at Completion - EAC):**
* *Trường hợp hiệu suất hiện tại (CPI) tiếp tục duy trì đến hết dự án:*

$$\text{EAC} = \frac{\text{BAC}}{\text{CPI}}$$




* **Dự toán Chi phí còn lại để làm nốt (Estimate to Complete - ETC):**

$$\text{ETC} = \text{EAC} - \text{AC}$$


* **Chênh lệch khi hoàn thành (Variance at Completion - VAC):**

$$\text{VAC} = \text{BAC} - \text{EAC}$$



---

## 3. CẤU TRÚC BỘ CÔNG CỤ THEO DÕI NGÂN SÁCH (ARTIFACTS)

Một file **Budget Tracking Sheet** chuyên nghiệp (trên Google Sheets/Excel) cần kết hợp giữa theo dõi EVM tổng thể và chi tiết giải ngân từng Sprint:

### Bảng Theo dõi Ngân sách Dự án Tổng thể (Master Budget Tracking)

| Hạng mục chi phí (Cost Category) | Dự toán ban đầu (BAC) | Chi phí Thực tế lũy kế (AC) | Giá trị hoàn thành (EV) | Chênh lệch (CV = EV - AC) | Hiệu suất (CPI) | Dự báo tổng chi phí (EAC) | Trạng thái (RAG) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **1. Nhân sự nội bộ (Dev, QA, UI/UX)** | $100,000 | $55,000 | $60,000 | $+ \$5,000$ | **1.09** | $91,743 | 🟢 Xanh |
| **2. Hạ tầng Cloud (AWS / GCP)** | $12,000 | $8,500 | $6,000 | $- \$2,500$ | **0.71** | $16,901 | 🔴 Đỏ |
| **3. API & Licenses bên thứ ba (eKYC, Map)** | $8,000 | $4,000 | $4,000 | $\$0$ | **1.00** | $8,000 | 🟢 Xanh |
| **4. Dự phòng rủi ro (Contingency)** | $10,000 | $2,000 | - | - | - | $10,000 | 🟢 Xanh |
| **TỔNG CỘNG DỰ ÁN** | **$130,000** | **$69,500** | **$70,000** \vert{} **$+ $500** | **1.01** | **$128,712** | 🟢 **XANH** |  |

---

## 4. CASE STUDY THỰC TẾ: DỰ ÁN "EPIC CENTER"

* **Bối cảnh:** Dự án phát triển nền tảng ứng dụng Epic Center có tổng ngân sách được phê duyệt là $\text{BAC} = \$120,000$ cho 6 tháng phát triển (gồm 12 Sprints, tương đương $\$10,000/\text{tháng}$).
* **Thời điểm kiểm tra:** Cuối tháng thứ 3 (kết thúc Sprint 6 - mốc 50% thời gian dự án).
* **Số liệu thu thập thực tế tại tháng thứ 3:**
* $\text{PV (Planned Value)} = \$60,000$ (Theo kế hoạch phải hoàn thành $50\%$ khối lượng).
* $\text{EV (Earned Value)} = \$48,000$ (Thực tế mới chỉ hoàn thành $40\%$ khối lượng tính năng).
* $\text{AC (Actual Cost)} = \$54,000$ (Thực tế đã chi tiêu hết $\$54,000$, do phát sinh chi phí server AWS tăng vọt và tiền tăng ca OT).


* **Phân tích toán học EVM của PO (Duy):**
1. $\text{CV} = \text{EV} - \text{AC} = \$48,000 - \$54,000 = -\$6,000$ 🔴 (Đang bị bội chi $\$6,000$).
2. $\text{CPI} = \frac{\text{EV}}{\text{AC}} = \frac{\$48,000}{\$54,000} = \mathbf{0.89}$ 🔴 (Mỗi 1 USD bỏ ra chỉ tạo ra $0.89 USD giá trị).
3. $\text{SPI} = \frac{\text{EV}}{\text{PV}} = \frac{\$48,000}{\$60,000} = \mathbf{0.80}$ 🔴 (Tiến độ đang chậm $20\%$).
4. $\text{Dự báo tổng chi phí mới (EAC)} = \frac{\text{BAC}}{\text{CPI}} = \frac{\$120,000}{0.89} = \mathbf{\$134,831}$ (Dự án có nguy cơ vượt ngân sách gần $\$15,000$).


* **Hành động can thiệp chiến lược của Product Owner:**
* **Tối ưu chi phí hạ tầng Cloud (AWS):** Cùng Tech Lead rà soát hệ thống, chuyển đổi các Database RDS sang dạng Reserved Instances (tiết kiệm $40\%$ chi phí Cloud mỗi tháng) và tắt các máy chủ thử nghiệm ngoài giờ làm việc.
* **Cắt tỉa phạm vi tính năng (Scope Pruning):** Đàm phán với Sponsor tạm hoãn module phụ *"Chia sẻ khoảnh khắc du lịch lên mạng xã hội"* (tiết kiệm $15$ Story Points) để dồn nhân sự hoàn thiện các tính năng lõi tạo ra dòng tiền.


* **Kết quả:** Sau 3 tháng tiếp theo, CPI tăng trở lại mức **1.02**; dự án về đích an toàn ở mốc **$118,500** (nằm trong trần ngân sách cho phép).

---

## 5. CÁC TIPS & ĐIỀU LƯU Ý THỰC CHIẾN (ANTI-PATTERNS & SOLUTIONS)

| Sai lầm phổ biến (Anti-Pattern) | Hậu quả | Giải pháp thực chiến |
| --- | --- | --- |
| **"Sốc hóa đơn Cloud" (Cloud Bill Shock)** | Bị trừ hàng nghìn USD bất ngờ do lập trình viên bật máy chủ AI/Elasticsearch quên tắt. | Cài đặt **AWS/GCP Budget Alerts** tự động gửi cảnh báo qua Slack/Email khi chi phí chạm ngưỡng $50\%, 80\%$ và tự động ngắt dịch vụ khi chạm $100\%$. |
| **Chỉ đo "Tiền đã tiêu" mà không đo "Giá trị tạo ra"** | Nhìn thấy tiêu hết ít tiền thì tưởng là tốt, nhưng thực tế tiến độ không hoàn thành được gì. | Luôn tính toán **EV (Earned Value)** và **CPI**, không chỉ so sánh thô giữa AC (Actual Cost) và BAC. |
| **Bẫy Chi phí Chìm (Sunk Cost Fallacy)** | Tính năng làm dở dang nhưng không còn hiệu quả kinh doanh, vẫn cố đổ thêm tiền để làm vì "tiếc tiền đã bỏ ra". | Đánh giá lại ROI định kỳ; dũng cảm "hủy bỏ (Kill Feature)" các tính năng không mang lại giá trị để bảo toàn ngân sách. |
| **Không phân tách Quỹ dự phòng (Reserves Confusion)** | Chi tiêu vô tội vạ vào quỹ dự phòng cho những thay đổi phát sinh không chính đáng. | Tuân thủ nghiêm ngặt chuẩn PMP: **Contingency Reserve** do PM/PO duyệt cho *Known-Unknowns (rủi ro đã nhận diện)*; **Management Reserve** do Sponsor duyệt cho *Unknown-Unknowns (biến cố bất khả kháng)*. |

---

## 6. NGUỒN THAM KHẢO CHẤT LƯỢNG (BLOGS, BOOKS & YOUTUBE)

1. **Chuẩn quốc tế & Sách kinh điển:**
* *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) – 6th & 7th Edition* (Chương *Project Cost Management* & *Measurement Performance Domain*).
* *Practice Standard for Earned Value Management* – Project Management Institute (PMI).
* *Financial Intelligence for IT and Product Managers* – Karen Berman & Joe Knight.


2. **Blog chuyên ngành uy tín:**
* **ProjectManagement.com (PMI Portal):** Chuỗi bài viết *"EVM for Agile and Hybrid Projects: Practical Formulas & Case Studies"*.
* **Mind the Product:** *Financial Literacy for Product Managers: Managing Budgets & Unit Economics*.
* **AWS Architecture Blog:** *FinOps: Cloud Cost Management & Optimization Strategies*.


3. **Kênh YouTube tham khảo:**
* **Praizion Performance Management:** Video *Earned Value Management (EVM) Formulas Made Easy for PMP*.
* **ProjectManager:** Video *How to Track and Control Project Budget Effectively*.
* **Continuous Delivery:** *FinOps - Controlling Infrastructure Costs in Agile Delivery*.



---
