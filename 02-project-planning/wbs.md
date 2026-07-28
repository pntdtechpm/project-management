# 02-PROJECT-PLANNING: BÀI 01 - WORK BREAKDOWN STRUCTURE (WBS)

**Tên tài liệu:** `02-project-planning/wbs.md`  
**Chủ đề:** Cấu trúc Phân chia Công việc (Work Breakdown Structure - WBS) chuẩn PMP trong giai đoạn Project Planning  
**Đối tượng hướng tới:** Project Manager (PM), Product Owner (PO), Business Analyst (BA) và các thành viên Quản lý Dự án.

---

## I. Khung kiến thức chuẩn PMP (PMBOK® Guide - 6th Edition)

### 1. Định nghĩa & bản chất WBS

Theo PMBOK® Guide 6th Edition, quy trình **Create WBS** (Process 5.4) phân chia các sản phẩm bàn giao (*deliverables*) và công việc của dự án thành những thành phần nhỏ hơn, dễ quản lý hơn.

WBS là sự phân rã theo thứ bậc (*hierarchical decomposition*) của toàn bộ phạm vi công việc đội ngũ dự án phải thực hiện để đạt mục tiêu dự án và tạo ra các sản phẩm bàn giao được yêu cầu.

- **Work Package (Gói công việc):** Nằm ở cấp thấp nhất của WBS. Ở cấp này, chi phí và thời gian có thể được ước tính, quản lý một cách đáng tin cậy.
- **Lưu ý quan trọng:** Từ *work* trong WBS đại diện cho kết quả công việc hoặc sản phẩm bàn giao (*deliverables/work products*), **không phải** các hoạt động thực hiện (*activities*).

### 2. Các quy tắc vàng khi lập WBS

- **Quy tắc 100% (The 100% Rule):** WBS phải bao hàm 100% phạm vi trong Project Scope Statement, kể cả công việc quản lý dự án. Tổng công việc ở các cấp con bằng chính xác 100% công việc ở cấp cha: không thừa, không thiếu phạm vi.
- **Tính tương hỗ loại trừ (Mutually Exclusive):** Các thành phần cùng cấp không được trùng lặp phạm vi để tránh nhân đôi chi phí hoặc chồng chéo trách nhiệm.
- **Tập trung vào bàn giao (Deliverable-Oriented):** Mỗi node nên là một danh từ đại diện cho sản phẩm/kết quả bàn giao, thay vì động từ đại diện cho hành động.

### 3. Các thành phần trong Scope Baseline

WBS là một trong ba thành phần cốt lõi của **Scope Baseline**:

1. **Project Scope Statement:** Mô tả chi tiết phạm vi dự án, các bàn giao chính, giả định và hạn chế.
2. **WBS:** Biểu đồ phân rã phạm vi.
3. **WBS Dictionary:** Tài liệu mô tả chi tiết từng thành phần WBS, gồm Code of Account, mô tả công việc, tiêu chí nghiệm thu, chi phí ước tính, người chịu trách nhiệm và các thông tin liên quan.

### 4. Mối quan hệ giữa WBS, Control Account và Planning Package

- **Control Account (Tài khoản kiểm soát):** Điểm kiểm soát quản lý tích hợp Scope, Budget và Schedule để đo lường hiệu suất dự án bằng Earned Value Management (EVM). Mỗi Control Account chứa một hoặc nhiều Work Package; mỗi Work Package chỉ thuộc một Control Account duy nhất.
- **Planning Package:** Nằm dưới Control Account và trên Work Package. Dùng cho phần việc đã biết phạm vi nhưng chưa đủ thông tin để chi tiết thành Work Package tại thời điểm hiện tại.

```text
                [ Dự án: Hệ thống Ngân hàng Số ]
                               |
                [ Control Account 1.0: eKYC ]
                     /                   \
      [Work Package 1.1: OCR Module]  [Planning Package 1.2: Deepfake Check]
```

---

## II. Ví dụ & minh họa thực tế

### Ví dụ: WBS dự án phát triển hệ thống Onboarding & eKYC ngân hàng số

Cây WBS dưới đây được phân rã theo các sản phẩm bàn giao chính (*major deliverables*):

```text
1.0 Hệ thống Onboarding & eKYC Ngân hàng Số
├── 1.1 Quản lý Dự án
│   ├── 1.1.1 Báo cáo Khởi động & Kế hoạch Dự án
│   ├── 1.1.2 Báo cáo Tiến độ & Quản lý Rủi ro
│   └── 1.1.3 Tài liệu Nghiệm thu & Đóng dự án
├── 1.2 Nền tảng eKYC
│   ├── 1.2.1 Module OCR Giấy tờ tùy thân (Work Package)
│   │   ├── 1.2.1.1 Trích xuất thông tin CCCD / CMND
│   │   └── 1.2.1.2 Module kiểm tra tính thật/giả của giấy tờ
│   └── 1.2.2 Module Nhận diện & So khớp Khuôn mặt (Work Package)
│       ├── 1.2.2.1 Face Matching (1:1 & 1:N)
│       └── 1.2.2.2 Liveness Detection (Chống giả mạo hình ảnh/video)
├── 1.3 Ứng dụng Di động
│   ├── 1.3.1 Luồng Onboarding iOS App (Work Package)
│   └── 1.3.2 Luồng Onboarding Android App (Work Package)
├── 1.4 Tích hợp & Kiểm thử
│   ├── 1.4.1 Hệ thống Tích hợp Core Banking (Work Package)
│   └── 1.4.2 Bộ Test Case & Báo cáo Kiểm thử An toàn Bảo mật (Work Package)
└── 1.5 Triển khai & Đào tạo
    ├── 1.5.1 Môi trường Production & Infrastructure
    └── 1.5.2 Tài liệu Hướng dẫn Vận hành & Đào tạo Operations
```

---

## III. Case study dẫn chứng thực tế

### Cạm bẫy biến WBS thành danh sách task dẫn đến trượt tiến độ dự án Super App

**Bối cảnh:** Dự án chuyển đổi số phát triển Super App đặt phòng và dịch vụ trễ hạn ba tháng. PM dùng WBS như một danh sách 200 việc phải làm, với các hành động như *"Viết code API"*, *"Họp với bên Design"* và *"Fix bug đăng nhập"*.

**Vấn đề phát sinh:**

1. **Thiếu ownership:** Thành viên không biết khi nào một sản phẩm bàn giao hoàn thành triệt để vì các task hành động diễn ra liên tục.
2. **Scope creep:** Không tuân thủ quy tắc 100% theo deliverables nên bỏ sót các phần quan trọng, như tài liệu bảo mật và tích hợp cổng thanh toán phụ; công việc phát sinh nằm ngoài tầm kiểm soát.
3. **Không ước tính được EVM:** Cấp thấp nhất là các task nhỏ thay vì Work Package, làm mất khả năng theo dõi tiến độ tổng thể.

**Giải pháp khắc phục:**

1. Tái cấu trúc WBS dựa trên deliverables (danh từ): chuyển *"Viết code API"* thành *"Work Package: API Cổng Thanh toán VNPAY"*.
2. Bổ sung **WBS Dictionary** với Acceptance Criteria rõ ràng cho từng Work Package.

**Kết quả:** Tiến độ được quản lý rõ ràng hơn, phạm vi được kiểm soát 100% và số yêu cầu thay đổi không hợp lý từ stakeholder giảm 80%.

---

## IV. Tips & điều lưu ý thực chiến cho PM/PO

1. **Phân biệt WBS và Backlog / Task List**
   - **WBS:** Phân rã sản phẩm bàn giao (**WHAT**); không chứa thứ tự thời gian hoặc phụ thuộc.
   - **Activity List / Backlog:** Phân rã Work Package thành các hành động hoặc User Stories (**HOW & WHEN**) để đưa vào Sprint hoặc Schedule.

2. **Quy tắc 8/80 khi xác định độ sâu Work Package**
   - Không nên dưới 8 giờ công để tránh micro-management.
   - Không nên trên 80 giờ công hoặc quá 1–2 tuần vì khó kiểm soát tiến độ và chi phí.

3. **Dùng WBS chống scope creep:** Khi stakeholder yêu cầu thêm tính năng, đối chiếu Scope Baseline/WBS: nếu tính năng không thuộc WBS đã phê duyệt, cần thực hiện Change Request.

4. **Luôn bao gồm Project Management:** Đưa các công việc quản lý, báo cáo và nghiệm thu vào WBS để bảo đảm đủ ngân sách và nguồn lực cho hoạt động quản lý dự án.

---

## V. Tài liệu & nguồn tham khảo

### 1. Sách & chuẩn quốc tế

- *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) – 6th Edition*, Chapter 5: Project Scope Management, Section 5.4 Create WBS.
- *Practice Standard for Work Breakdown Structures – 2nd Edition* (PMI).

### 2. Bài viết & blog uy tín

- PMI.org: *Work Breakdown Structure Practice Standard*.
- ProjectManagement.com: *How to Create a Deliverable-Oriented WBS*.

### 3. Video / YouTube chia sẻ chuyên sâu

- Search keyword: *"How to Create a Work Breakdown Structure - PMBOK Framework"* (Ricardo Vargas hoặc ProjectManager).
- Search keyword: *"WBS vs Product Backlog vs Activity List Explained"*.
