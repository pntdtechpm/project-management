# 02-PROJECT-PLANNING: BÀI 05 - RELEASE PLAN (KẾ HOẠCH PHÁT HÀNH)

**Tên tài liệu:** `02-project-planning/release-plan.md`  
**Chủ đề:** Lập Kế hoạch Phát hành (Release Planning) chiến lược trong mô hình Agile/Hybrid theo chuẩn PMI  
**Đối tượng hướng tới:** Project Manager (PM), Product Owner (PO), Release Train Engineer (RTE), DevOps Lead và các khối vận hành liên quan như Operations và Marketing.

---

## I. Khung kiến thức chuẩn Agile (PMI-ACP® & PMBOK® Guide)

### 1. Định nghĩa & bản chất của Release Plan

Theo *Agile Practice Guide* của PMI, **Release Plan (Kế hoạch Phát hành)** vạch ra một lộ trình cấp trung hạn nhằm xác định khi nào các tính năng hoặc gói sản phẩm tăng trưởng (Increments) sẽ được triển khai tới người dùng cuối hoặc môi trường Production.

**Mối liên kết hệ thống:** Nếu *Product Roadmap* định hướng chiến lược dài hạn theo quý hoặc năm và *Sprint Plan* tập trung thực thi ngắn hạn theo 1-2 tuần, thì *Release Plan* chính là **cầu nối** kết hợp nhiều Sprint lại với nhau để tạo ra một phiên bản sản phẩm có giá trị sử dụng thực tế, chẳng hạn Minimum Viable Product (MVP) hoặc Marketable Feature Set.

```text
[ Strategic Level ]      Product Roadmap (Hàng quý / năm)
                                  |
[ Tactical Level ]       Release Plan (Sau 3-6 Sprints)  <- BÀI NÀY
                                  |
[ Operational Level ]    Sprint Plan (Hàng tuần / 2 tuần)
```

### 2. Các ràng buộc cấu thành một Kế hoạch Phát hành

Một kế hoạch phát hành tiêu chuẩn thường được tiếp cận theo hai cách, tùy thuộc vào yếu tố ràng buộc chủ đạo:

- **Feature-Driven Release (Định hướng tính năng):** Phát hành sẽ diễn ra khi một tập hợp các tính năng quan trọng được hoàn thành 100%. Ví dụ: "Hệ thống chỉ Go-live khi hoàn thiện xong lõi thanh toán".
- **Date-Driven Release (Định hướng thời gian):** Phát hành diễn ra vào một ngày cố định, và phạm vi tính năng sẽ được co giãn bằng Scope Buffer dựa trên những gì đã làm kịp. Ví dụ: "Đúng ngày 30/09 phải release phiên bản đón đầu mùa du lịch".

### 3. Mối quan hệ giữa PMP và Agile Release Planning

Trong mô hình PMP truyền thống, Release Plan tương đương với một phần của **Control Schedule (6.6)** và các hoạt động thuộc về chuyển giao trạng thái vận hành. Điểm khác biệt cốt lõi là Agile tách biệt rõ hai khái niệm:

- **Deploy to Production (Triển khai kỹ thuật):** Đưa code lên môi trường thật nhưng có thể ẩn bằng Feature Flags hoặc Feature Toggles.
- **Release to Users (Phát hành thương mại):** Bật tính năng cho người dùng sử dụng và bắt đầu tính toán giá trị kinh doanh (Business Value Assessment).

---

## II. Ví dụ & minh họa thực tế

### Ví dụ: Kế hoạch Phát hành phiên bản MVP V1.0 - Ứng dụng "Epic Center"

- **Tên đợt phát hành:** Release v1.0 - "Early Bird Launch"
- **Loại hình:** Date-Driven Release (thời gian cố định)
- **Ngày Go-live dự kiến:** 15/09/2026
- **Tổng thời gian tích lũy:** Gồm 4 Sprints, mỗi Sprint 2 tuần
- **Tổng sức chứa dự kiến:** Khoảng 160 Story Points

### 1. Trục thời gian & mục tiêu các Sprint cấu thành

- **Sprint 05 (03/08 - 14/08):** Hoàn thiện Core Backend tích lũy E-Coffer và sinh mã VietQR động.
- **Sprint 06 (17/08 - 28/08):** Xây dựng luồng UI/UX Frontend trên iOS/Android cho chức năng nạp tiền và đặt chỗ.
- **Sprint 07 (31/08 - 11/09):** Tích hợp Webhook xử lý IPN ngân hàng, xử lý ngoại lệ như giao dịch lỗi và timeout.
- **Sprint 08 (14/09 - 18/09):** *Sprint Bug Hardening & Regression Testing*, chỉ tập trung fix bug và tối ưu, không thêm tính năng mới.

### 2. Ma trận Phạm vi Phát hành (Release Scope Matrix)

| Mã hạng mục | Tên tính năng (Epics / Stories) | Mức độ ưu tiên (MoSCoW) | Trạng thái kỹ thuật |
| --- | --- | --- | --- |
| **REQ-01** | Thanh toán tự động qua mã VietQR | **Must Have** (Bắt buộc) | Sẵn sàng triển khai |
| **REQ-02** | Hệ thống ví tích lũy E-Coffer nội bộ | **Must Have** (Bắt buộc) | Đang kiểm thử UAT |
| **REQ-03** | Gửi tin nhắn SMS OTP bảo mật khi rút tiền | **Should Have** (Nên có) | Đang phát triển |
| **REQ-04** | Trợ lý ảo AI Chatbot tư vấn giá phòng | **Could Have** (Có thể hoãn) | Chuyển sang Release v1.1 |

---

## III. Case study dẫn chứng thực tế

### Bài học đắt giá từ vụ rò rỉ dữ liệu do áp lực phát hành "Big Bang"

**Bối cảnh:** Một công ty công nghệ phát triển giải pháp SaaS quản lý đặt chỗ lưu trú lớn. Đến kỳ hạn Release cuối năm, PM quyết định phát hành toàn bộ 15 tính năng lớn tích lũy suốt 6 tháng cùng một lúc theo mô hình "Big Bang Release".

**Vấn đề phát sinh:**

1. Do khối lượng code thay đổi quá lớn (Massive Code Change), đội ngũ QA không thể kiểm thử hết toàn bộ các kịch bản tương tác chéo giữa các module.
2. Ngay đêm Go-live, hệ thống gặp lỗi nghẽn mạch cơ sở dữ liệu (Database Deadlock) do luồng đăng ký mới xung đột với cổng thanh toán.
3. Nghiêm trọng hơn, một lỗ hổng bảo mật trong module đối soát hóa đơn bị lộ, làm rò rỉ thông tin cá nhân của hơn 10,000 khách hàng.
4. Đội ngũ kỹ thuật phải thức trắng 48 giờ để rollback hệ thống về phiên bản cũ, gây thiệt hại lớn về uy tín và chi phí đền bù.

**Bài học rút ra:**

1. Đừng dồn tất cả các tính năng lớn vào một đợt phát hành duy nhất theo kiểu canh bạc.
2. Phải áp dụng chiến lược **Phát hành lũy tiến (Progressive/Canary Release)**: bật tính năng trước cho 5% lượng người dùng thử nghiệm, sau khi hệ thống ổn định mới nâng dần lên 100%.
3. Nếu release có rủi ro cao, PM/PO cần yêu cầu quality gates rõ ràng: regression pass, performance benchmark đạt ngưỡng, security scan không còn lỗi nghiêm trọng và rollback rehearsal đã được diễn tập.

---

## IV. Tips & điều lưu ý thực chiến cho PM/PO

### 1. Áp dụng mô hình phân loại ưu tiên MoSCoW

- **Must Have:** Các tính năng cốt lõi bắt buộc phải có; thiếu nó thì không thể release sản phẩm.
- **Should Have:** Quan trọng nhưng có thể dùng giải pháp tạm thời nếu thiếu hụt thời gian.
- **Could Have:** Tiện ích mở rộng, chỉ làm nếu team thừa thời gian và nguồn lực.
- **Won't Have:** Không làm trong đợt release này, chuyển hẳn vào Product Backlog dài hạn.

### 2. Luôn có Hardening Sprint

Đừng lập kế hoạch phát hành theo kiểu code sát nút đến ngày cuối cùng. Hãy dành riêng từ 0.5 đến 1 Sprint cuối trước ngày Release cho các việc:

- Kiểm thử hồi quy (Regression Testing)
- Tối ưu hiệu năng (Performance Tuning)
- Quét lỗ hổng bảo mật (Vulnerability Scanning)
- Viết tài liệu hướng dẫn sử dụng và Release Notes
- Chuẩn bị dữ liệu, dashboard giám sát và runbook vận hành

### 3. Thiết lập kế hoạch dự phòng Rollback

Luôn tự hỏi bản thân và đội ngũ DevOps:

> "Nếu hệ thống sập sau 10 phút Go-live, quy trình khôi phục lại trạng thái cũ mất bao lâu và cần những bước nào?"

Một Release Plan không có phương án rollback là một kế hoạch có rủi ro vận hành rất cao. Tối thiểu, kế hoạch cần nêu rõ:

- Điều kiện kích hoạt rollback
- Người có quyền ra quyết định rollback
- Thời gian khôi phục mục tiêu (RTO)
- Điểm khôi phục dữ liệu chấp nhận được (RPO)
- Cách truyền thông với khách hàng, Sales, CS và Operations

### 4. Tách Deploy khỏi Release

Trong các hệ thống hiện đại, không nên đồng nhất việc đưa code lên Production với việc bật tính năng cho toàn bộ người dùng. PM/PO nên làm việc với DevOps và Tech Lead để áp dụng:

- Feature flags cho tính năng rủi ro cao
- Canary release theo nhóm người dùng nhỏ
- Blue/green deployment nếu downtime không được chấp nhận
- Monitoring theo error rate, latency, conversion và business KPI sau release

---

## V. Template Release Plan nên dùng

| Trường thông tin | Nội dung cần có |
| --- | --- |
| Release ID / Name | Mã và tên đợt phát hành, ví dụ Release v1.0 - Early Bird Launch |
| Release Type | Date-driven, feature-driven, canary, phased rollout hoặc big bang |
| Business Objective | Giá trị kinh doanh cần đạt sau release |
| Target Users | Nhóm người dùng được bật tính năng |
| Scope Matrix | Must/Should/Could/Won't Have theo MoSCoW |
| Sprint Coverage | Các Sprint đóng góp vào release và mục tiêu từng Sprint |
| Entry Criteria | Điều kiện để bắt đầu release hardening hoặc release window |
| Exit Criteria | Điều kiện để Go-live hoặc mở rộng rollout |
| Quality Gates | Regression, performance, security, UAT, compliance |
| Deployment Plan | Lịch deploy, môi trường, owner, runbook |
| Rollback Strategy | Điều kiện rollback, bước rollback, RTO/RPO |
| Communication Plan | Thông báo nội bộ, khách hàng, Operations, Marketing và Support |
| Release Notes | Tính năng mới, thay đổi hành vi, lỗi đã sửa, hạn chế còn tồn tại |
| Post-release Review | Cách đo lường thành công và bài học sau release |

---

## VI. Tài liệu & nguồn tham khảo

### 1. Chuẩn quốc tế & sách gối đầu giường

- *Project Management Institute (PMI) - Agile Practice Guide* (2017), Section 5.2.4: Agile Release Planning.
- *Agile Estimating and Planning* - Mike Cohn.

### 2. Blog công nghệ & quản trị uy tín

- LeadingAgile: *Introduction to Agile Release Planning*.
- Scaled Agile Framework (SAFe): *PI Planning / Release Management*.

### 3. Video / YouTube hữu ích

- Search keyword: *"Agile Release Planning Masterclass - Step by Step"*.
- Search keyword: *"How to create a Release Plan in Jira Software"*.
