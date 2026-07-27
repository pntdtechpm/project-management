# Success Criteria trong giai đoạn Khởi động

## Phần 1: Khung kiến thức chuyên sâu (Knowledge Framework)

Trong quản trị dự án theo chuẩn PMP, **Tiêu chí Thành công (Success Criteria)** là tập hợp các chỉ số định lượng và định tính được thống nhất và phê duyệt bởi Nhà tài trợ (Sponsor) và các bên liên quan cốt lõi ngay ở giai đoạn Khởi động. Việc xác định tiêu chí thành công trả lời cho câu hỏi quan trọng nhất: *"Làm thế nào để tất cả các bên cùng thừa nhận dự án này đã hoàn thành thành công?"*

PMP chia Tiêu chí Thành công thành **2 nhóm riêng biệt nhưng bổ trợ cho nhau**:

```text
┌────────────────────────────────────────────────────────────────────────┐
│                        THÀNH CÔNG TỔNG THỂ DỰ ÁN                       │
└────────────────────────────────────────────────────────────────────────┘
                                   │
         ┌─────────────────────────┴─────────────────────────┐
         ▼                                                   ▼
┌──────────────────────────────┐            ┌──────────────────────────────┐
│  Thành công về Quản lý Dự án │            │   Thành công về Sản phẩm /   │
│  (Project Management Success)│            │  Kinh doanh (Product Success)│
├──────────────────────────────┤            ├──────────────────────────────┤
│ • Tiến độ (Schedule)         │            │ • Lợi nhuận / ROI & Payback  │
│ • Ngân sách (Budget)         │            │ • Tỷ lệ sử dụng (Adoption)   │
│ • Bàn giao Phạm vi (Scope)   │            │ • Hiệu quả tự động hóa AI    │
│ • Chất lượng kỹ thuật        │            │ • Mức độ hài lòng (CSAT/NPS) │
└──────────────────────────────┘            └──────────────────────────────┘
   (Đo lường khi Đóng dự án)                  (Đo lường sau khi Go-live)
```

### Nguyên tắc SMART trong xây dựng Tiêu chí Thành công

- **S (Specific - Cụ thể):** Không viết mơ hồ như "Giao diện đẹp" hay "Hệ thống chạy nhanh", mà phải ghi rõ "Giao diện phong cách Luxury đạt chuẩn thiết kế Figma" hay "Thời gian tải trang <1.5s".
- **M (Measurable - Đo lường được):** Mỗi tiêu chí bắt buộc phải có một con số, tỷ lệ hoặc trạng thái kiểm tra có thể nghiệm thu được.
- **A (Achievable - Khả thi):** Phải khả thi đối với năng lực kỹ thuật và nguồn lực 2.5 tỷ VNĐ trong 6 tháng.
- **R (Relevant - Thực tế & Phù hợp):** Gắn liền với Tầm nhìn Dự án và Luận chứng Kinh doanh.
- **T (Time-bound - Có thời hạn):** Có mốc thời điểm đo lường rõ ràng (Go-live, sau 3 tháng, sau 12 tháng).

---

# Phần 2: Bảng Tiêu chí Thành công Dự án chi tiết (Project Success Criteria Matrix)

**Tên dự án:** Phát triển Nền tảng Kỹ thuật số Tích hợp Dịch vụ Toàn diện & Trợ lý Ảo AI

**Giai đoạn ban hành:** 01 Project Initiation

**Phiên bản:** 1.0

## 1. Nhóm Tiêu chí Quản lý Dự án (Project Management Success Criteria)

*Đo lường trực tiếp tại thời điểm nghiệm thu và đóng dự án (Kết thúc Tháng thứ 6)*

| Khía cạnh | Chỉ số đo lường (KPI / Metric) | Ngưỡng mục tiêu (Target Threshold) | Phương pháp kiểm tra / Đo lường | Người đánh giá & Ký duyệt |
| --- | --- | --- | --- | --- |
| **Tiến độ (Schedule)** | Độ lệch thời gian so với Kế hoạch cơ sở | Hoàn thành và Go-live chính thức trong vòng **06 tháng** (Độ lệch tối đa: ±2 tuần) | So sánh ngày Go-live thực tế với Đường cơ sở tiến độ (Schedule Baseline) | Nhà tài trợ (Sponsor) & PM |
| **Chi phí (Budget)** | Tổng chi phí thực tế khi kết thúc dự án (Actual Cost) | Không vượt quá ngân sách **2.500.000.000 VNĐ** (Chỉ cho phép sử dụng trong phạm vi 10% ngân sách dự phòng) | Báo cáo kiểm toán tài chính dự án từ Ban Kế toán | Giám đốc Tài chính (CFO) |
| **Phạm vi (Scope)** | Tỷ lệ hoàn thành các Kết quả bàn giao (Deliverables) | **100%** các kết quả bàn giao thuộc phạm vi In-Scope được bàn giao (App iOS/Android, CMS, Module AI, eKYC) | Biên bản rà soát đối chiếu với Tài liệu Phạm vi cấp cao & SRS | Quản lý Dự án (PM) & Tech Lead |
| **Chất lượng (Quality)** | Số lượng lỗi hệ thống tại thời điểm nghiệm thu kỹ thuật (UAT) | **0 lỗi nghiêm trọng** (Severity 1 - Critical)<br>**0 lỗi cao** (Severity 2 - High)<br>Lỗi nhỏ (Severity 3/4) < 5 lỗi (có kế hoạch sửa bản sau) | Báo cáo tổng hợp kiểm thử chất lượng từ đội QA/QC | Tech Lead & Trưởng phòng QA |

---

## 2. Nhóm Tiêu chí Kỹ thuật & Hiệu năng Sản phẩm (Technical & Product Performance)

*Đo lường trong giai đoạn kiểm thử UAT và trong 30 ngày đầu sau Go-live*

| Khía cạnh | Chỉ số đo lường (KPI / Metric) | Ngưỡng mục tiêu (Target Threshold) | Phương pháp kiểm tra / Đo lường | Người đánh giá & Ký duyệt |
| --- | --- | --- | --- | --- |
| **Độ ổn định hệ thống** | Tỷ lệ hoạt động liên tục (Uptime) & Crash rate | Uptime hệ thống đạt **≥ 99.9%**.<br>Tỷ lệ ứng dụng bị văng (App Crash Rate) **< 0.5%**. | Hệ thống giám sát hạ tầng tự động (AWS CloudWatch / Firebase Analytics) | Tech Lead & DevOps |
| **Tốc độ phản hồi** | Thời gian phản hồi API (Latency) | Tốc độ tải dữ liệu trung bình **< 1.5 giây** trên mạng 4G/Wifi tiêu chuẩn | Công cụ đo kiểm tải và hiệu năng (JMeter / Postman) | Tech Lead |
| **Hiệu quả Trợ lý AI** | Tỷ lệ nhận diện đúng ý định & Tự động giải quyết | Độ chính xác nhận diện ý định khách hàng (Intent Accuracy) **≥ 85%**.<br>Tự động trả lời đúng kịch bản FAQs **≥ 75%** không cần con người can thiệp. | Nhật ký hội thoại AI (AI Log) & Báo cáo đánh giá ngẫu nhiên từ QA | Trưởng phòng Vận hành & BA |
| **Độ chính xác eKYC** | Tốc độ & Tỷ lệ định danh thành công | Quy trình định danh hoàn tất **< 1 phút**.<br>Tỷ lệ khớp khuôn mặt và OCR chính xác **≥ 98%**. | Nhật ký xác thực hệ thống eKYC (eKYC Verification Logs) | Tech Lead & Đơn vị Vendor eKYC |

---

## 3. Nhóm Tiêu chí Kinh doanh & Giá trị Thương mại (Business & Commercial Success)

*Đo lường theo các mốc 3 tháng, 6 tháng và 12 tháng sau khi Go-live (Thuộc Kế hoạch Quản lý Lợi ích)*

| Khía cạnh | Chỉ số đo lường (KPI / Metric) | Ngưỡng mục tiêu (Target Threshold) | Phương pháp kiểm tra / Đo lường | Người đánh giá & Ký duyệt |
| --- | --- | --- | --- | --- |
| **Tối ưu chi phí Vận hành** | Tỷ lệ giảm chi phí xử lý yêu cầu CSKH | Cắt giảm **35% - 40%** chi phí vận hành bộ phận CSKH nhờ Trợ lý AI và eKYC tự động sau 6 tháng | So sánh chi phí vận hành CSKH thực tế so với giai đoạn trước khi có app | CFO & Trưởng phòng Vận hành |
| **Tỷ lệ chấp nhận (Adoption Rate)** | Số lượng người dùng kích hoạt & sử dụng ứng dụng | Đạt **20.000+** tài khoản người dùng đăng ký eKYC thành công sau 3 tháng.<br>Tỷ lệ duy trì hàng tháng (MAU) đạt **≥ 40%**. | Báo cáo phân tích dữ liệu ứng dụng (Google Analytics / AppsFlyer) | Product Manager & Marketing |
| **Chỉ số Tài chính (ROI & Payback)** | Thời gian hoàn vốn & Tỷ suất hoàn vốn | Thời gian hoàn vốn (Payback Period): **14 tháng**.<br>Tỷ suất hoàn vốn (ROI): **45%** sau 24 tháng vận hành. | Báo cáo tài chính doanh thu luân chuyển từ dịch vụ đặt phòng & E-Coffer | Ban Giám đốc (Sponsor) & CFO |

---

## 4. Nhóm Tiêu chí Trải nghiệm & Sự hài lòng (Stakeholder & User Satisfaction)

*Đo lường qua khảo sát thực tế người dùng và đội ngũ nội bộ*

| Khía cạnh | Chỉ số đo lường (KPI / Metric) | Ngưỡng mục tiêu (Target Threshold) | Phương pháp kiểm tra / Đo lường | Người đánh giá & Ký duyệt |
| --- | --- | --- | --- | --- |
| **Trải nghiệm Người dùng (UX)** | Chỉ số hài lòng của khách hàng (CSAT / NPS) | Điểm CSAT trải nghiệm app đạt **≥ 4.5/5 sao**.<br>Chỉ số NPS (Mức độ giới thiệu app) đạt **≥ 8.5/10**. | Khảo sát tự động ngay trên ứng dụng sau khi khách hàng trải nghiệm dịch vụ | Product Manager & UI/UX Designer |
| **Sự hài lòng Nội bộ** | Mức độ thuận tiện khi sử dụng hệ thống CMS | **≥ 80%** nhân viên vận hành và CSKH đánh giá giao diện CMS dễ thao tác, giúp tăng năng suất làm việc | Khảo sát nội bộ bộ phận Vận hành sau 1 tháng sử dụng | Trưởng phòng Vận hành |

---

## Phần 3: Nguyên tắc Giám sát và Báo cáo Tiêu chí Thành công

Để đảm bảo các tiêu chí thành công không bị lãng quên trong quá trình triển khai, Quản lý Dự án (PM) áp dụng cơ chế quản trị sau:

1. **Thiết lập Bảng theo dõi Chỉ số Thành công (Success Metrics Dashboard):** Cập nhật trạng thái của các chỉ số kỹ thuật và tiến độ theo thời gian thực (Real-time) trên công cụ quản lý dự án.
2. **Đánh giá tại các Cổng Phê duyệt (Quality Gates / Phase Gates):** Tại mỗi mốc Milestone lớn như Chốt thiết kế UI/UX, Hoàn thành bản MVP, Hoàn thành UAT, PM bắt buộc phải rà soát các tiêu chí thành công tương ứng trước khi trình Sponsor cho phép bước sang giai đoạn tiếp theo.
3. **Chuyển giao cho Kế hoạch Quản lý Lợi ích (Benefits Realization Plan):** Đối với các tiêu chí kinh doanh dài hạn (ROI, cắt giảm 40% chi phí CSKH), sau khi đóng dự án, PM sẽ chính thức bàn giao trách nhiệm theo dõi chỉ số này cho Trưởng phòng Vận hành và Giám đốc Sản phẩm (Product Owner) tiếp tục đo lường định kỳ.

---

*Tài liệu Tiêu chí Thành công này khép lại toàn bộ nền tảng định lượng cho **Giai đoạn 01 Project Initiation**. Bộ tiêu chí này sẽ là thước đo công bằng và minh bạch nhất để đánh giá năng lực quản lý dự án của PM cũng như giá trị thực tế mà sản phẩm mang lại cho doanh nghiệp.*
