
---

# PHẦN 1: KHUNG KIẾN THỨC CHUYÊN SÂU (KNOWLEDGE FRAMEWORK)

**Phân tích các bên liên quan (Stakeholder Analysis)** là quá trình thu thập và phân tích thông tin định tính, định lượng một cách có hệ thống để xác định lợi ích, kỳ vọng, mức độ ảnh hưởng và rủi ro từ tất cả các cá nhân/tổ chức có liên quan đến dự án.

### 1. Các mô hình phân loại & Công cụ phân tích cốt lõi

* **Ma trận Quyền hạn / Mức độ quan tâm (Power / Interest Grid):**
* **Quyền hạn Cao / Quan tâm Cao (Manage Closely):** Nhóm then chốt, cần quản lý chặt chẽ, tham vấn liên tục.
* **Quyền hạn Cao / Quan tâm Thấp (Keep Satisfied):** Cần đáp ứng tốt nhu cầu nhưng không làm họ bội thực thông tin.
* **Quyền hạn Thấp / Quan tâm Cao (Keep Informed):** Giữ cho họ luôn được cập nhật, họ là nguồn hỗ trợ tích cực.
* **Quyền hạn Thấp / Quan tâm Thấp (Monitor):** Theo dõi với nguồn lực tối thiểu.


* **Mô hình Nổi bật (Salience Model):**
Phân tích Stakeholders dựa trên 3 đặc tính sinh động:
1. *Quyền lực (Power):* Khả năng áp đặt ý chí lên dự án.
2. *Tính hợp pháp (Legitimacy):* Mức độ chính đáng của sự tham gia/yêu cầu.
3. *Tính cấp thiết (Urgency):* Đòi hỏi sự chú ý tức thì hoặc mức độ nhạy cảm về thời gian.


* **Ma trận Đánh giá Mức độ Tham gia (Stakeholder Engagement Assessment Matrix):**
Theo dõi sự dịch chuyển thái độ của từng bên qua 5 cấp độ:
`Chưa biết (Unaware)` ➔ `Kháng cự (Resistant)` ➔ `Trung lập (Neutral)` ➔ `Ủng hộ (Supportive)` ➔ `Dẫn dắt (Leading)`.
* **Hướng tác động (Directions of Influence):**
* *Upward (Hướng lên):* Ban lãnh đạo, Nhà tài trợ, CFO.
* *Downward (Hướng xuống):* Đội ngũ phát triển (Dev, UI/UX, QA).
* *Sideward (Hướng ngang):* Trưởng phòng Vận hành, Marketing, Pháp lý.
* *Outward (Hướng ra ngoài):* Khách hàng người dùng, Nhà cung cấp API eKYC/AI, Cơ quan quản lý.



---

# PHẦN 2: QUY TRÌNH 4 BƯỚC THỰC HIỆN PHÂN TÍCH

```
┌─────────────────────────────────┐
│ Bước 1: Thu thập & Định danh    │ ──> Phỏng vấn, Brainstorming, Phân tích tài liệu
└─────────────────────────────────┘
                 │
                 ▼
┌─────────────────────────────────┐
│ Bước 2: Định vị & Phân loại     │ ──> Xếp vào Ma trận Power/Interest & Salience
└─────────────────────────────────┘
                 │
                 ▼
┌─────────────────────────────────┐
│ Bước 3: Phân tích Xung đột      │ ──> Đánh giá khoảng cách C (Current) vs D (Desired)
└─────────────────────────────────┘
                 │
                 ▼
┌─────────────────────────────────┐
│ Bước 4: Lập Chiến lược tác động │ ──> Xây dựng Communication & Engagement Plan
└─────────────────────────────────┘

```

---

# PHẦN 3: BẢNG PHÂN TÍCH CÁC BÊN LIÊN QUAN CHI TIẾT (STAKEHOLDER ANALYSIS MATRIX)

**Tên dự án:** Phát triển Nền tảng Kỹ thuật số Tích hợp Dịch vụ Toàn diện & Trợ lý Ảo AI

**Giai đoạn:** 01 Project Initiation

**Phiên bản:** 2.0 (Bản nâng cấp chi tiết)

*Ký hiệu thái độ: **C** = Hiện tại (Current) | **D** = Mong muốn (Desired)*

| Bên liên quan (Stakeholder) | Hướng tác động | Phân loại (Power / Interest) | Đánh giá Salience Model | Thái độ (C ➔ D) | Kỳ vọng / Điểm đau cốt lõi | Chiến lược tác động & Quản trị rủi ro |
| --- | --- | --- | --- | --- | --- | --- |
| **Ban Giám đốc (Sponsor)** | Upward | Quyền hạn: **Cao**<br>

<br>Quan tâm: **Cao** | Power + Legitimacy + Urgency *(Dominant)* | **C:** Supportive<br>

<br>**D:** **Leading** | • Go-live đúng hạn 6 tháng.<br>

<br>• Tối ưu chi phí CSKH.<br>

<br>• Mở rộng thị phần ứng dụng dịch vụ cao cấp. | • **Chiến lược:** Quản lý chặt chẽ.<br>

<br>• **Hành động:** Gửi báo cáo Executive Dashboard hàng tuần; Trình duyệt các mốc Milestones quan trọng. |
| **Giám đốc Tài chính (CFO)** | Upward | Quyền hạn: **Cao**<br>

<br>Quan tâm: **Thấp/Vừa** | Power + Legitimacy *(Dominant)* | **C:** Neutral<br>

<br>**D:** **Supportive** | • Kiểm soát tổng ngân sách 2.5 tỷ VNĐ.<br>

<br>• Minh bạch chi phí API duy trì (AI, eKYC, Cloud). | • **Chiến lược:** Giữ cho hài lòng.<br>

<br>• **Hành động:** Cung cấp báo cáo phân tích dòng tiền và ROI; Thống nhất hạn mức duyệt chi nhanh. |
| **Trưởng phòng Vận hành & CSKH** | Sideward | Quyền hạn: **Vừa**<br>

<br>Quan tâm: **Cao** | Legitimacy + Urgency *(Dependent)* | **C:** **Resistant**<br>

<br>**D:** **Supportive** | • Sợ AI trả lời sai ngữ cảnh làm mất khách.<br>

<br>• E ngại quy trình CMS mới phức tạp, xáo trộn nhân sự. | • **Chiến lược:** Tương tác & Lắng nghe.<br>

<br>• **Hành động:** Cam kết mô hình "Human-in-the-loop"; Đưa họ vào nhóm duyệt giao diện CMS và kịch bản thử nghiệm AI. |
| **Tech Lead / Kiến trúc sư Hệ thống** | Downward | Quyền hạn: **Cao**<br>

<br>Quan tâm: **Cao** | Power + Legitimacy + Urgency *(Definitive)* | **C:** Supportive<br>

<br>**D:** **Leading** | • Cần yêu cầu kỹ thuật (SRS) rõ ràng.<br>

<br>• Sợ Scope Creep làm trễ hạn Go-live 6 tháng. | • **Chiến lược:** Đồng hành & Trợ lực.<br>

<br>• **Hành động:** Bảo vệ team Dev trước các yêu cầu phát sinh; Trao quyền quyết định về kiến trúc hạ tầng và Framework. |
| **Chuyên gia UI/UX** | Downward | Quyền hạn: **Vừa**<br>

<br>Quan tâm: **Cao** | Legitimacy *(Discretionary)* | **C:** Supportive<br>

<br>**D:** **Supportive** | • Muốn trải nghiệm tinh tế, chuẩn Luxury.<br>

<br>• Cần phê duyệt thiết kế nhanh để chuyển giao sang Dev. | • **Chiến lược:** Giữ kết nối liên tục.<br>

<br>• **Hành động:** Duyệt cuốn chiếu từng luồng giao diện (eKYC, E-Coffer, Chat AI); Cân bằng giữa thẩm mỹ và tính khả thi kỹ thuật. |
| **Vendor cung cấp API (eKYC / AI)** | Outward | Quyền hạn: **Vừa**<br>

<br>Quan tâm: **Vừa** | Urgency + Power *(Dangerous nếu dừng service)* | **C:** Neutral<br>

<br>**D:** **Supportive** | • Cần tài liệu kỹ thuật chuẩn xác.<br>

<br>• Đảm bảo thanh toán chi phí duy trì đúng hợp đồng. | • **Chiến lược:** Hợp tác sòng phẳng.<br>

<br>• **Hành động:** Ký cam kết SLA >99.9%; Tích hợp kênh hỗ trợ kỹ thuật phản ứng nhanh (Zalo/Slack 24/7). |
| **Khách hàng / Người dùng cuối** | Outward | Quyền hạn: **Thấp**<br>

<br>Quan tâm: **Cao** | Legitimacy + Urgency *(Demanding)* | **C:** Unaware<br>

<br>**D:** **Supportive** | • Muốn định danh eKYC siêu nhanh (<1 phút).<br>

<br>• Trợ lý AI phản hồi thông minh, bảo mật tuyệt đối dữ liệu. | • **Chiến lược:** Giữ cho được cập nhật thông tin.<br>

<br>• **Hành động:** Khảo sát nhóm trải nghiệm sớm (Beta Testers); Tối ưu hóa luồng UX đơn giản nhất có thể. |

---

# PHẦN 4: MA TRẬN GIẢI QUYẾT XUNG ĐỘT TRỌNG YẾU (CONFLICT RESOLUTION MATRIX)

Trong quá trình khởi động dự án, Quản lý Dự án (PM) phải chủ động xử lý 3 vùng xung đột lợi ích kinh điển sau:

```
[Xung đột 1: Tốc độ Go-live vs Độ hoàn hảo UI/UX]
  ✦ Tech Lead: Muốn giản lược hiệu ứng để kịp hạn 6 tháng.
  ✦ UI/UX Designer: Muốn giữ nguyên hiệu ứng Luxury tỉ mỉ.
  👉 Giải pháp của PM: Áp dụng tư duy MVP (Minimum Viable Product). Bản Go-live ưu tiên hiệu năng và tính năng cốt lõi; các hiệu ứng chuyển cảnh phức tạp chuyển sang giai đoạn nâng cấp tiếp theo.

[Xung đột 2: Tự động hóa AI vs An toàn vận hành]
  ✦ Kinh doanh/Sponsor: Muốn AI tự động chốt đơn đặt dịch vụ và tư vấn tài chính E-Coffer.
  ✦ Team Vận hành: Lo ngại AI tư vấn sai thông tin gây tổn hại uy tín thương hiệu.
  👉 Giải pháp của PM: Bán tự động hóa (Semi-automation). AI tư vấn các kịch bản chuẩn (FAQs, gợi ý danh mục); với các giao dịch tài chính E-Coffer hoặc phản hồi khiếu nại, AI sẽ soạn sẵn câu trả lời và yêu cầu Nhân viên Vận hành bấm duyệt (Confirm) trước khi gửi.

[Xung đột 3: Ngân sách API vs Tính năng hệ thống]
  ✦ CFO: Muốn khống chế chi phí duy trì API eKYC và AI theo lượt gọi (Pay-per-use).
  ✦ Team Sản phẩm: Muốn gọi API liên tục để tối ưu trải nghiệm người dùng.
  👉 Giải pháp của PM: Thiết lập cơ chế Caching dữ liệu thông minh ở phía Backend để giảm 30-40% số lượng truy vấn API lặp lại không cần thiết sang bên thứ ba.

```

---

# PHẦN 5: BẢNG KẾ HOẠCH TRUYỀN THÔNG & TƯƠNG TÁC (COMMUNICATION CADENCE)

| Nhóm đối tượng | Kênh truyền thông | Tần suất | Đầu ra / Mục tiêu |
| --- | --- | --- | --- |
| **Sponsor & CFO** | Executive Dashboard / Email Report | 2 tuần / lần | Báo cáo tiến độ Milestones, Ngân sách & Rủi ro vĩ mô |
| **Toàn bộ Stakeholders** | Báo cáo tình trạng dự án (Status Report) | 1 tháng / lần | Cập nhật bức toàn cảnh dự án cho toàn bộ hệ thống |
| **Core Team (Dev, UI/UX, BA)** | Daily Standup / Sprint Review (Hybrid) | Hàng ngày / 2 tuần | Tháo gỡ nghẽn kỹ thuật, rà soát Backlog và Demo sản phẩm |
| **Team Vận hành & Vendors** | Họp phối hợp nghiệp vụ & Sandbox Test | 1 tuần / lần | Đảm bảo chuẩn hóa dữ liệu đầu vào và tính sẵn sàng của API |

---

*Tài liệu **Phân tích các bên liên quan** hoàn chỉnh này cung cấp góc nhìn toàn diện từ chiến lược đến hành động, sẵn sàng để PM đưa vào bộ Hồ sơ Khởi động Dự án (Initiation Phase Package).*