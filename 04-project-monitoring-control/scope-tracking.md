# 04-PROJECT-MONITORING-CONTROL: BÀI 08 - SCOPE TRACKING (KIỂM SOÁT PHẠM VI & CHỐNG PHÙ DUNG PHẠM VI)

## 1. KHUNG KIẾN THỨC CHUẨN PMP (PMBOK 6 & 7) & LIÊN HỆ THỰC TẾ

### A. Khái niệm theo chuẩn Quản trị Dự án Quốc tế (PMP)

Kiểm soát phạm vi (**Scope Tracking / Control Scope**) là quá trình giám sát hiện trạng của phạm vi dự án và sản phẩm, đồng thời quản lý các thay đổi đối với Đường cơ sở Phạm vi (**Scope Baseline**).

* **PMBOK 6th Edition:**
* Thuộc nhóm quy trình **Monitoring and Controlling Process Group**, trực tiếp là quy trình **Control Scope**.
* Dựa trên **Scope Baseline** bao gồm 3 thành tố: *Bản mô tả phạm vi dự án (Project Scope Statement), Cấu trúc phân chia công việc (WBS), và Từ điển WBS (WBS Dictionary)*.
* Phân biệt rõ hai hiểm họa lớn nhất của phạm vi dự án:
* **Scope Creep (Phù dung phạm vi):** Việc phạm vi dự án hoặc sản phẩm bị mở rộng một cách không kiểm soát, không được phê duyệt qua quy trình kiểm soát thay đổi, và không được điều chỉnh tương ứng về thời gian, chi phí và nguồn lực.
* **Gold Plating (Mạ vàng sản phẩm):** Hành động đội ngũ tự ý bổ sung thêm các chức năng, chi tiết "thú vị" hoặc tối ưu kỹ thuật vượt quá yêu cầu đã thỏa thuận với khách hàng/sponsor mà không mang lại giá trị gia tăng được công nhận.




* **PMBOK 7th Edition & Agile/Hybrid:**
* Nằm trong **Delivery Performance Domain** và **Development Approach and Life Cycle Performance Domain**.
* Agile xem sự tiến hóa của phạm vi (**Scope Evolution / Progressive Elaboration**) là tất yếu khi hiểu biết về người dùng ngày càng rõ nét. Tuy nhiên, sự linh hoạt này phải được quản lý chặt chẽ thông qua **Product Backlog Refinement** và nguyên tắc **Đánh đổi phạm vi (Scope Flexibility / Trade-off)**.



### B. Phân biệt Scope Tracking: Predictive (Truyền thống) vs. Adaptive (Agile/Hybrid)

| Khía cạnh so sánh | Dự án Truyền thống (Predictive) | Dự án Linh hoạt (Agile / Hybrid) |
| --- | --- | --- |
| **Cơ sở đối chiếu (Baseline)** | Scope Baseline cố định (Scope Statement + WBS). | Product Backlog được ưu tiên hóa liên tục. |
| **Công cụ kiểm soát chính** | Ma trận truy xuất nguồn gốc (RTM) & Change Control. | Backlog Refinement, Definition of Done (DoD), Sprint Goals. |
| **Cách ứng xử với Scope mới** | Phải nộp Change Request, họp CCB phê duyệt. | PO thẩm định giá trị (ROI), đưa vào Backlog, thực hiện **Swap Scope**. |
| **Tiêu chí nghiệm thu** | Formal Sign-off theo hợp đồng phạm vi ban đầu. | Khách hàng/Stakeholders nghiệm thu qua từng Sprint Review. |

---

## 2. CẤU TRÚC BỘ CÔNG CỤ THEO DÕI PHẠM VI (ARTIFACTS)

Một bộ công cụ Scope Tracking chuẩn quốc tế cần đảm bảo không có bất kỳ yêu cầu nào bị "bỏ rơi" hoặc tự ý phát sinh ngoài tầm kiểm soát:

### A. Ma trận Truy xuất Nguồn gốc Yêu cầu (Requirements Traceability Matrix - RTM)

RTM là chiếc "la bàn" liên kết từng dòng code và ca kiểm thử quay ngược về mục tiêu kinh doanh ban đầu:

| Req ID | Nhu cầu Kinh doanh (Business Need) | Mục tiêu Sản phẩm (Feature / Epic) | User Story ID | Thiết kế UI/UX (Figma Link) | Test Case ID (QA) | Trạng thái Nghiệm thu |
| --- | --- | --- | --- | --- | --- | --- |
| **REQ-01** | Tăng tỷ lệ hoàn tất đơn đặt phòng trực tuyến. | Module Thanh toán Đa kênh | `US-102` | `Screen_Checkout_v2` | `TC_Pay_001` to `005` | 🟢 Accepted (Sprint 6) |
| **REQ-02** | Giảm thiểu gian lận danh tính Chủ nhà. | Xác thực eKYC Căn cước công dân | `US-145` | `Screen_Host_KYC` | `TC_KYC_011` to `020` | 🟡 In Progress (Sprint 8) |
| **REQ-03** | Tối ưu thời gian tìm phòng theo vị trí. | Tìm kiếm Homestay theo Bán kính Bản đồ | `US-189` | `Screen_Map_Search` | `TC_Map_001` | 🔴 Deferred to Phase 2 |

---

### B. Biểu đồ Kiểm soát Biến động Phạm vi (Scope Burnup & Scope Delta)

```
Story Points
 200 ──┐                                         ┌─── [Total Scope Line] (Đường Tổng Scope)
 180   │                                   ┌─────┘ ◄── Scope phát sinh thêm (+20 SP)
 160   │ ──────────────────────────────────┘
 140   │                            ┌─────────── [Work Completed] (Công việc hoàn thành)
 120   │                     ┌──────┘
  80   │              ┌──────┘
   0 ──┴──────────────┴──────────────┴──────────────┴──────────────► Sprints
       Sprint 1       Sprint 2       Sprint 3       Sprint 4

```

* **Đường Total Scope Line tăng vọt:** Cho thấy dự án đang bị nhồi thêm tính năng (Scope Creep).
* **Khoảng cách giữa hai đường không thu hẹp:** Cảnh báo dự án sẽ không bao giờ về đích nếu không đóng băng phạm vi (Scope Freeze) hoặc bổ sung nguồn lực.

---

## 3. NGHỆ THUẬT QUẢN TRỊ THAY ĐỔI PHẠM VI: CƠ CHẾ "SWAP SCOPE"

Trong môi trường phát triển sản phẩm linh hoạt, thay vì cứng nhắc từ chối mọi ý tưởng mới của Ban Giám đốc hay Khách hàng, Product Owner áp dụng kỹ thuật **Hoán đổi Phạm vi (Swap Scope)** dựa trên bảo toàn Dung lượng (Capacity):

```
       KỸ THUẬT HOÁN ĐỔI PHẠM VI (SWAP SCOPE RULE)
       
  Yêu cầu Mới phát sinh: Tính năng Gamification Lắc Xu (Ước lượng: 13 SP)
  Dung lượng Sprint / Release: CỐ ĐỊNH (Không thể nhồi thêm)
  
  ┌────────────────────────────────────────────────────────────────────────┐
  │ NGUYÊN TẮC: "MUỐN THÊM VÀO THÌ PHẢI BỎ RA"                            │
  │                                                                        │
  │  [+13 SP Tính năng Mới]  <=======>  [-8 SP Module Đánh giá nâng cao]   │
  │                                     [-5 SP Bộ lọc tìm kiếm chi tiết]   │
  │                                     --------------------------------   │
  │                                     TỔNG BỎ RA: -13 SP                 │
  └────────────────────────────────────────────────────────────────────────┘

```

* **Thông điệp truyền thông của PO:** *"Chúng tôi hoàn toàn có thể đưa tính năng Gamification này vào Release tới. Đổi lại, hai tính năng có mức độ ưu tiên thấp hơn là Bộ lọc chi tiết và Đánh giá nâng cao sẽ được dời sang Phase sau để bảo đảm ngày ra mắt không bị trễ hạn"*.

---

## 4. CASE STUDY THỰC TẾ: DỰ ÁN "EPIC CENTER"

* **Bối cảnh:** Dự án Epic Center đang ở Sprint 9/12, chuẩn bị bước vào giai đoạn đóng gói phiên bản Release chính thức. Đội ngũ Marketing và Trưởng phòng Kinh doanh bất ngờ gửi một yêu cầu khẩn cấp: *"Cần bổ sung ngay tính năng 'Ví điểm thưởng tích lũy (Loyalty Points)' để kịp chạy chương trình kích cầu mùa hè"*.
* **Áp lực đè nặng lên Product Owner (Duy):**
* Đội Kỹ thuật (Dev Lead & QA Lead) phản ứng gay gắt: Nếu làm thêm tính năng Ví điểm thưởng (ước tính tốn khoảng 21 Story Points), toàn bộ kiến trúc Database thanh toán phải sửa đổi, đội ngũ chắc chắn vỡ tiến độ Release Target và phải làm thêm giờ (OT) liên tục.
* Marketing khẳng định: Không có tính năng này thì hiệu quả chiến dịch giảm 30%.


* **Hành động can thiệp của PO thông qua Scope Tracking & RTM:**
1. **Đối soát lại RTM và Mục tiêu Cốt lõi (Core Business Need):** Mục tiêu tối thượng của phiên bản này là: *Luồng đặt phòng ổn định và Thanh toán bảo mật tuyệt đối*.
2. **Phân loại theo Ma trận MoSCoW:**
* **Must-have (Bắt buộc phải có):** Đặt phòng, Thanh toán MoMo/VietQR, Smart Check-in mở khóa.
* **Could-have (Có thì tốt, chưa gấp):** Ví điểm thưởng tích lũy.


3. **Đưa ra giải pháp tình thế (Workaround / Lean Scope):** Thay vì xây dựng cả một hệ thống Ví điểm thưởng phức tạp (21 SP), Duy đề xuất giải pháp tinh gọn: Sử dụng cơ chế **"Mã Voucher giảm giá trực tiếp (Direct Discount Codes)"** – tính năng đã có sẵn trong hệ thống – để Marketing phát hành mã ưu đãi cho khách mà không cần viết thêm dòng code nào.


* **Kết quả:** Marketing đạt được mục tiêu kích cầu bằng mã voucher; đội ngũ Kỹ thuật giữ vững phạm vi cam kết, không phát sinh nợ kỹ thuật (Tech Debt); sản phẩm ra mắt đúng ngày với tỷ lệ lỗi phát sinh trên môi trường Production bằng 0.

---

## 5. CÁC TIPS & ĐIỀU LƯU Ý THỰC CHIẾN (ANTI-PATTERNS & SOLUTIONS)

| Sai lầm phổ biến (Anti-Pattern) | Hậu quả | Giải pháp thực chiến |
| --- | --- | --- |
| **"Hội chứng Chiều lòng tất cả" (The Yes-Man PO)** | PO gật đầu với mọi yêu cầu của Stakeholders, khiến Backlog phình to vô hạn, team kiệt sức. | Rèn luyện kỹ năng **"Say NO with Data"**: Từ chối dựa trên dữ liệu dung lượng (Capacity) và bài toán ROI, không từ chối theo cảm tính cá nhân. |
| **"Mạ vàng sản phẩm" (Gold Plating)** | Lập trình viên/Designer tự thêm các hiệu ứng, tính năng thừa thãi mà khách hàng không cần, gây trễ tiến độ. | Bám sát **Acceptance Criteria (Tiêu chuẩn chấp nhận)** trong từng User Story; QA chỉ kiểm thử đúng những gì đã được định nghĩa. |
| **Thêm việc qua tin nhắn/trò chuyện miệng (Shadow Scope)** | Tính năng được sửa trực tiếp không qua ghi nhận, gây mất dấu vết khi xảy ra lỗi hệ thống. | Thực thi quy tắc: **"No Ticket, No Work"**. Mọi công việc phải được xuất hiện trên Jira/Backlog mới được thực thi. |
| **Định nghĩa Hoàn thành mơ hồ (Vague DoD)** | Mỗi người hiểu một kiểu về độ hoàn thiện của tính năng, dẫn đến việc phải làm đi làm lại (Rework). | Xây dựng **Definition of Done (DoD)** rõ ràng: Đã viết Unit Test > 80% coverage, đã qua kiểm thử QA trên Staging, đã cập nhật tài liệu kỹ thuật. |

---

## 6. NGUỒN THAM KHẢO CHẤT LƯỢNG (BLOGS, BOOKS & YOUTUBE)

1. **Chuẩn quốc tế & Sách kinh điển:**
* *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) – 6th & 7th Edition* (Chương *Project Scope Management* & *Delivery Performance Domain*).
* *User Story Mapping: Discover the Whole Story, Build the Right Product* – Jeff Patton (Phương pháp trực quan hóa và cắt tỉa phạm vi sản phẩm).
* *BABOK® Guide v3 (A Guide to the Business Analysis Body of Knowledge)* – IIBA (Phần *Requirements Life Cycle Management*).


2. **Blog chuyên ngành uy tín:**
* **ProjectManagement.com (PMI Portal):** *How to Prevent Scope Creep in Agile and Hybrid Projects*.
* **Roman Pichler Product Management Blog:** *The Art of Saying No to Stakeholders*.
* **Mind the Product:** *Scope Management: How to Balance Flexibility and Delivery*.


3. **Kênh YouTube tham khảo:**
* **Praizion Performance Management:** Video *Control Scope Process Explained for PMP Exam*.
* **Agile Academy:** Video *User Story Splitting Techniques to Control Scope*.
* **Product School:** Video *How to Manage Scope Creep and Stakeholder Expectations*.



---

