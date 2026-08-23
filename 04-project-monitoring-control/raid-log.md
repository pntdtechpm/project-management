

# 04-PROJECT-MONITORING-CONTROL: BÀI 01 - RAID LOG (QUẢN TRỊ RỦI RO, GIẢ ĐỊNH, VẤN ĐỀ VÀ PHỤ THUỘC)

## 1. KHUNG KIẾN THỨC CHUẨN PMP (PMBOK 6 & 7) & LIÊN HỆ THỰC TẾ

### A. Khái niệm theo chuẩn Quản trị Dự án Quốc tế (PMP)

Khi dự án bước vào giai đoạn kiểm soát (**Monitoring & Controlling**), việc quản lý rời rạc các yếu tố bất định qua nhiều file Excel/Jira khác nhau sẽ làm phân tán sự chú ý của người quản lý. **RAID Log** là công cụ quản trị tập trung ("Single Pane of Glass") giúp gom 4 khía cạnh sống còn của dự án về một nơi:

* **R - Risks (Rủi ro):** Các sự kiện *chưa xảy ra*, có xác suất ảnh hưởng (tiêu cực hoặc tích cực) đến mục tiêu dự án.
* **A - Assumptions (Giả định):** Những điều kiện, thông tin được xem là đúng hoặc chắc chắn sẽ diễn ra trong quá trình lập kế hoạch nhưng *chưa được kiểm chứng thực tế*.
* **I - Issues (Vấn đề):** Các sự cố *đã và đang xảy ra* trong thực tế, cần hành động khắc phục ngay lập tức.
* **D - Dependencies (Điểm phụ thuộc):** Các điều kiện ràng buộc giữa các công việc nội bộ dự án hoặc giữa dự án với bên thứ ba (Nếu A chưa xong thì B chưa thể bắt đầu).
* **PMBOK 6th Edition:**
* Nằm trong nhóm quy trình **Monitoring and Controlling Process Group**, trực tiếp phục vụ cho *Monitor and Control Project Work*, *Monitor Risks*, và *Manage Project Knowledge*.
* Đóng vai trò là một **Project Document** tổng hợp, giúp PM nắm quyền kiểm soát toàn diện mà không bị bất ngờ bởi các tác nhân ngoại cảnh.


* **PMBOK 7th Edition & Agile/Hybrid:**
* Thuộc **Uncertainty Performance Domain** (Xử lý sự mơ hồ, độ phức tạp và rủi ro) và **Measurement Performance Domain**.
* Trong mô hình phát triển Agile/Hybrid, RAID Log được sử dụng như một bảng điều khiển chiến lược (Strategic Dashboard) trong các buổi họp giao ban định kỳ với Ban chỉ đạo (Steering Committee) và các bên liên quan cấp cao (Key Stakeholders).



### B. Liên hệ Thực tế Quản lý Sản phẩm (Product Management)

* **Bản chất:** RAID Log là công cụ giúp Product Manager/PO **bảo vệ bức tranh toàn cảnh (Bird's-eye view)**, không để các chi tiết kỹ thuật vi mô (Tasks/Bugs hàng ngày) che khuất các nguy cơ chiến lược.
* **Mục đích cốt lõi đối với Product Team:**
1. **Nhận diện Giả định ẩn (Hidden Assumptions):** Nhiều dự án Product thất bại vì xây dựng tính năng dựa trên những giả định sai lầm về hành vi người dùng hoặc năng lực hạ tầng đối tác.
2. **Quản lý Nghẽn phụ thuộc chéo (Cross-team Dependencies):** Giúp PO nhìn thấy rõ điểm tắc nghẽn giữa các Team (Ví dụ: Team UI/UX xong nhưng phải đợi Team Core Backend mở API, Team Core Backend lại đợi đối tác Ngân hàng duyệt bảo mật).
3. **Truyền thông minh bạch cho Ban Giám đốc (Sponsors):** Cung cấp 1 trang tóm tắt ngắn gọn về "Sức khỏe rủi ro" của sản phẩm thay vì bắt Sếp đọc toàn bộ hàng trăm tickets trên Jira.



---

## 2. CẤU TRÚC BỘ CÔNG CỤ & KHUNG FILE RAID LOG (ARTIFACTS)

Một file **RAID Log** chuẩn chỉnh (trên Notion, Confluence, Google Sheets hoặc Airtable) được tổ chức thành 4 tab/phần riêng biệt với các trường thông tin tiêu chuẩn:

### 1. Tab R - Risk Register (Sổ đăng ký rủi ro)

* **ID:** `RSK-001`
* **Mô tả Rủi ro:** *Khả năng Apple App Store từ chối duyệt app do chính sách thu phí in-app mới.*
* **Xác suất (Probability - P) x Mức độ ảnh hưởng (Impact - I):** $High \times High = Critical (Đỏ)$.
* **Chiến lược ứng phó:** *Mitigate (Giảm thiểu)* - Liên hệ chuyên gia tư vấn App Review để chỉnh sửa luồng thanh toán trước khi submit.
* **Owner:** Duy (Product Owner).

### 2. Tab A - Assumption Log (Nhật ký giả định)

* **ID:** `ASM-001`
* **Mô tả Giả định:** *Giả định rằng 100% Chủ nhà (Host) đều sở hữu điện thoại thông minh hỗ trợ Bluetooth 5.0 trở lên để sử dụng Smart Check-in.*
* **Cách thức kiểm chứng (Validation Action):** Thực hiện khảo sát nhanh trên 200 Chủ nhà mẫu trong tuần này.
* **Hạn chót kiểm chứng:** `15/04/2026`.
* **Trạng thái:** `Validated (Đúng)` / `Invalidated (Sai - Chuyển thành Issue/Risk)`.

### 3. Tab I - Issue Log (Nhật ký vấn đề)

* **ID:** `ISS-001`
* **Mô tả Vấn đề:** *Máy chủ Test của bên thứ ba bị sập, Dev không thể test luồng gọi Webhook.*
* **Mức độ khẩn cấp:** `High`.
* **Hành động khắc phục (Action):** Dựng Mock API nội bộ để tiếp tục phát triển.
* **Owner & Deadline:** Tech Lead - `18/04/2026`.

### 4. Tab D - Dependency Matrix (Ma trận phụ thuộc)

* **ID:** `DEP-001`
* **Nội dung phụ thuộc:** *Tính năng "Xuất hóa đơn điện tử tự động" phụ thuộc vào việc Bên Thuế cấp tài khoản API chính thức.*
* **Phân loại:** *External Inbound* (Phụ thuộc vào đối tác bên ngoài bàn giao cho dự án).
* **Đầu mối liên hệ (Contact):** Trưởng phòng Kế toán.
* **Ngày bàn giao cam kết:** `25/04/2026`.

---

## 3. QUY TRÌNH QUẢN TRỊ & NHỊP ĐIỆU CẬP NHẬT RAID LOG (CADENCE)

```
       [Đầu tuần: Rà soát & Cập nhật]
                     │
                     ▼
  ┌─────────────────────────────────────┐
  │  1. Kiểm chứng các Giả định (A)     │
  │  2. Đánh giá lại Rủi ro (R)         │
  │  3. Cập nhật tiến độ giải quyết (I) │
  │  4. Đôn đốc các mốc Phụ thuộc (D)   │
  └─────────────────────────────────────┘
                     │
                     ▼
  [Cuộc họp Review với Stakeholders / Sponsor]
                     │
                     ▼
  [Kích hoạt Escalation nếu có cảnh báo Đỏ]

```

* **Nhịp điệu hàng tuần (Weekly RAID Review):** Dành **20 - 30 phút** trước buổi họp tiến độ tuần để PM/PO rà soát toàn bộ các mục:
* *Giả định nào đến hạn kiểm chứng?* Nếu giả định sai ➔ Chuyển ngay thành Risk hoặc Issue.
* *Rủi ro nào đã trở thành sự thật?* ➔ Chuyển trạng thái sang Issue.
* *Điểm phụ thuộc nào sắp trễ hạn cam kết?* ➔ Kích hoạt cảnh báo sớm.



---

## 4. CASE STUDY THỰC TẾ: DỰ ÁN "EPIC CENTER"

* **Bối cảnh:** Epic Center chuẩn bị tung ra tính năng *"Thanh toán Quốc tế dành cho Khách nước ngoài thuê Homestay"* (Tích hợp Stripe/Visa/Mastercard).
* **Ứng dụng RAID Log trong thực tế:**
* **Assumption (A):** Đội ngũ giả định rằng cổng thanh toán Stripe tại Việt Nam đã hỗ trợ rút tiền trực tiếp về tài khoản ngân hàng nội địa bằng tiền VNĐ với mức phí < 2%.
* **Hành động kiểm chứng:** PO (Duy) đưa mục này vào RAID Log với mã `ASM-014` và giao cho Business Analyst đối soát hợp đồng pháp lý của Stripe.
* **Phát hiện bước ngoặt:** Sau khi đối soát tài liệu, BA phát hiện tài khoản Stripe Việt Nam vẫn chưa mở tính năng rút trực tiếp tiền VNĐ nếu không đăng ký pháp nhân tại Singapore (Giả định bị sai - **Invalidated**).
* **Chuyển hóa sang Risk & Action:**
* Duy lập tức chuyển giả định này thành rủi ro nghiêm trọng: `RSK-029: Rủi ro gián đoạn luồng giải ngân tiền cho Chủ nhà do vướng mắc pháp nhân Stripe`.
* **Chiến lược ứng phó:** Đổi phương án tích hợp sang cổng **Onepay / VNPAY Quốc tế** đã có sẵn giấy phép thanh toán tại Việt Nam.




* **Kết quả:** Nhờ kiểm chứng giả định từ sớm qua RAID Log, dự án đã kịp thời đổi hướng kỹ thuật trước khi đội Dev bắt tay vào viết code, tránh lãng phí 4 tuần phát triển vô ích và tiết kiệm hàng ngàn USD chi phí tái cấu trúc hệ thống.

---

## 5. CÁC TIPS & ĐIỀU LƯU Ý THỰC CHIẾN (ANTI-PATTERNS & SOLUTIONS)

| Sai lầm phổ biến (Anti-Pattern) | Hậu quả | Giải pháp thực chiến |
| --- | --- | --- |
| **"Tài liệu viết một lần rồi quên" (Write & Forget)** | RAID Log trở thành tài liệu "chết", không phản ánh thực tế dự án. | Đưa RAID Log vào **Chương trình nghị sự bắt buộc (Mandatory Agenda)** của cuộc họp giao ban hàng tuần. |
| **Bỏ quên phần Giả định (Ignoring Assumptions)** | Dự án xây dựng trên "lâu đài cát" của những niềm tin chủ quan, dễ sụp đổ khi thử nghiệm thực tế. | Mỗi khi lập kế hoạch cho 1 Epic/Feature mới, luôn đặt câu hỏi: *"Chúng ta đang ngầm coi điều gì là hiển nhiên?"* và ghi ngay vào Assumption Log. |
| **Nhầm lẫn giữa Risk và Issue** | Hành động lúng túng, áp dụng kế hoạch dự phòng cho sự cố đã xảy ra hoặc ngược lại. | **Ghi nhớ câu thần chú:** *Risk là 'Nếu... thì...' (Chưa xảy ra); Issue là 'Bởi vì... đang bị...' (Đang diễn ra)*. |
| **Ghi nhận Dependency nhưng không có ngày cam kết** | Phụ thuộc vào bên thứ ba bị thả nổi vô thời hạn, khiến dự án bị động chờ đợi. | Mọi Dependency đều bắt buộc phải có: **01 Người liên hệ đối tác (Contact Person)** và **01 Ngày bàn giao cam kết (Committed Delivery Date)**. |

---

## 6. NGUỒN THAM KHẢO CHẤT LƯỢNG (BLOGS, BOOKS & YOUTUBE)

1. **Chuẩn quốc tế & Sách kinh điển:**
* *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) – 6th & 7th Edition* (Phần *Monitor and Control Project Work* & *Uncertainty Performance Domain*).
* *Managing Successful Projects with PRINCE2®* (Nguồn gốc chuẩn mực của phương pháp luận quản trị RAID).


2. **Blog chuyên ngành uy tín:**
* **ProjectManagement.com (PMI Portal):** Chuỗi bài viết *"The Power of RAID Logs in Project Governance"*.
* **PM Majik:** *How to Create and Manage an Effective RAID Log (Excel & Cloud Templates)*.
* **Atlassian Confluence Guides:** *How to run a RAID analysis for cross-functional teams*.


3. **Kênh YouTube tham khảo:**
* **ProjectManager:** Video *What is a RAID Log in Project Management? (Definitions & Templates)*.
* **Praizion Performance Management:** Video *Managing Risks, Assumptions, Issues, Dependencies (RAID) for PMP*.
* **Agile Academy:** *Managing Dependencies Across Agile Teams*.



---
