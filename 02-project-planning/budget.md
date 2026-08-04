# 02-PROJECT-PLANNING: BÀI 14 - BUDGET (XÁC ĐỊNH NGÂN SÁCH DỰ ÁN)

**Tên tài liệu:** `02-project-planning/budget.md`  
**Chủ đề:** Xác định Ngân sách Dự án (Determine Budget) và Thiết lập Đường cơ sở Chi phí (Cost Baseline) theo chuẩn PMP  
**Đối tượng hướng tới:** Project Manager (PM), Product Owner (PO), CFO / Financial Controller, PMO và Nhà tài trợ dự án (Sponsor).

---

## I. Khung kiến thức chuẩn PMP (PMBOK® Guide - 6th Edition)

### 1. Định nghĩa & bản chất của quy trình Determine Budget

Theo PMBOK® Guide 6th Edition, quy trình **Determine Budget** (Process 7.3) là quá trình cộng dồn chi phí ước tính của từng hoạt động hoặc các gói công việc (Work Packages) để thiết lập một **Đường cơ sở Chi phí được phê duyệt (Authorized Cost Baseline)**.

**Bản chất cốt lõi:** Ngân sách dự án không đơn thuần là tổng chi phí ước tính. Nó là một thực thể tài chính được cấu trúc chặt chẽ, phân bổ theo thời gian (*time-phased*) nhằm giúp PM và doanh nghiệp quản lý dòng tiền (*cash flow*) và làm thước đo kiểm soát hiệu suất thông qua Earned Value Management (EVM).

Budget là bước nối giữa **Cost Estimation** và **Cost Control**. Nếu estimate trả lời câu hỏi "dự án có thể tốn bao nhiêu", thì budget trả lời câu hỏi "chi phí được phê duyệt là bao nhiêu, được cấp vào lúc nào và dùng để kiểm soát theo baseline nào".

### 2. Cấu trúc thành phần ngân sách dự án

PMBOK định nghĩa mô hình phân cấp ngân sách nhằm phân định rõ quyền hạn sử dụng tài chính:

1. **Activity Cost Estimates (Ước tính chi phí hoạt động):** Chi phí thô của từng task hoặc hoạt động cụ thể.
2. **Work Package Cost Estimates (Ước tính chi phí gói công việc):** Chi phí được cộng dồn từ các activity thuộc cùng một gói công việc trong WBS.
3. **Contingency Reserve (Quỹ dự phòng rủi ro đã nhận diện - Known-Unknowns):** Khoản dự phòng được tính toán dựa trên Risk Register. Khoản này **nằm trong Cost Baseline** và PM có thể sử dụng khi các rủi ro đã nhận diện xảy ra, theo ngưỡng thẩm quyền được phê duyệt.
4. **Cost Baseline (Đường cơ sở chi phí):** Ngân sách được phê duyệt theo thời gian, dùng để đo lường và giám sát hiệu suất chi phí của dự án. Công thức:

```text
Cost Baseline = Tổng chi phí Work Packages + Contingency Reserve
```

5. **Management Reserve (Quỹ dự phòng quản lý - Unknown-Unknowns):** Khoản dự phòng cho sự kiện bất khả kháng hoặc rủi ro chưa được nhận diện. Khoản này **nằm ngoài Cost Baseline** nhưng thuộc **Project Budget**. PM không được tự ý sử dụng mà phải xin phê duyệt từ Sponsor hoặc Ban Giám đốc.
6. **Project Budget (Tổng ngân sách dự án):** Tổng số tiền tổ chức cần chuẩn bị cho dự án. Công thức:

```text
Project Budget = Cost Baseline + Management Reserve
```

### 3. Đường cong S (S-Curve) trong phân bổ ngân sách

Do ngân sách được phân bổ theo thời gian, dòng tiền chi tiêu của dự án thường không đều nhau qua các tháng. Giai đoạn khởi đầu thường chi tiêu ít, giai đoạn thực thi code/test/mua sắm chi tiêu mạnh, và giai đoạn đóng dự án chi tiêu giảm dần.

Khi vẽ chi phí tích lũy theo thời gian, dự án thường tạo ra **Đường cong S (S-Curve)**. Đây là công cụ quan trọng để:

- Theo dõi Cost Baseline theo từng kỳ.
- So sánh Planned Value (PV), Earned Value (EV) và Actual Cost (AC).
- Phát hiện nguy cơ vượt ngân sách hoặc thiếu dòng tiền.
- Đối soát kế hoạch giải ngân với hạn mức cấp vốn của tổ chức.

### 4. Funding Limit Reconciliation

**Funding Limit Reconciliation** là kỹ thuật đối soát giữa nhu cầu chi tiêu tích lũy của dự án và hạn mức cấp vốn mà tổ chức có thể cung cấp tại từng thời điểm.

Nếu S-Curve của dự án vượt đường hạn mức cấp vốn, PM cần phối hợp với Finance và Sponsor để điều chỉnh kế hoạch. Các phương án thường gặp gồm giãn tiến độ mua sắm, chia nhỏ hợp đồng vendor, đổi milestone thanh toán hoặc xin phê duyệt cấp vốn bổ sung.

---

## II. Ví dụ & minh họa thực tế

### Ví dụ: Cấu trúc ngân sách dự án "Epic Center" - Phase 1 (Module eKYC & Ví)

Giả sử dự án được phê duyệt triển khai trong 4 tháng, từ tháng 08/2026 đến tháng 11/2026, với các thông số tài chính như sau.

### 1. Phân rã cấu phần tài chính (Budget Breakdown)

- **Tổng chi phí các gói công việc (Work Packages):** `40,000 USD`
  - Thiết kế UI/UX: `4,000 USD`
  - Dev Core: `24,000 USD`
  - Testing & Security Audit: `12,000 USD`
- **Contingency Reserve:** `4,000 USD`, tương đương 10% chi phí thô, dựa trên rủi ro nghẽn API và lỗi tích hợp ngân hàng.
- **Cost Baseline:** `44,000 USD`
- **Management Reserve:** `3,000 USD`, dành cho rủi ro bất khả kháng hoặc thay đổi chính sách pháp lý chưa nhận diện.
- **Total Project Budget:** `47,000 USD`

```text
Cost Baseline = 40,000 + 4,000 = 44,000 USD
Project Budget = 44,000 + 3,000 = 47,000 USD
```

### 2. Bảng phân bổ dòng tiền theo thời gian (Time-phased Budget)

| Gói công việc / Thành phần | Tháng 08/2026 | Tháng 09/2026 | Tháng 10/2026 | Tháng 11/2026 | Tổng cộng |
| --- | ---: | ---: | ---: | ---: | ---: |
| **WP-01: Thiết kế UI/UX** | 4,000 USD | 0 USD | 0 USD | 0 USD | **4,000 USD** |
| **WP-02: Phát triển Core Back-Frontend** | 6,000 USD | 12,000 USD | 6,000 USD | 0 USD | **24,000 USD** |
| **WP-03: Kiểm thử & An toàn thông tin** | 0 USD | 2,000 USD | 6,000 USD | 4,000 USD | **12,000 USD** |
| *Contingency Reserve (phân bổ)* | 1,000 USD | 1,000 USD | 1,000 USD | 1,000 USD | **4,000 USD** |
| **Chi phí hàng tháng (Periodic Target)** | **11,000 USD** | **15,000 USD** | **13,000 USD** | **5,000 USD** | **44,000 USD** |
| **Chi phí tích lũy (S-Curve Value)** | **11,000 USD** | **26,000 USD** | **39,000 USD** | **44,000 USD** | **Cost Baseline** |

Management Reserve `3,000 USD` không nằm trong bảng Cost Baseline ở trên. Khoản này vẫn thuộc tổng ngân sách dự án nhưng chỉ được giải ngân khi có phê duyệt quản lý phù hợp.

### 3. Diễn giải kiểm soát ngân sách

- Nếu đến cuối tháng 09/2026, chi phí thực tế là `28,000 USD` trong khi baseline tích lũy là `26,000 USD`, dự án đang có dấu hiệu vượt chi phí so với kế hoạch.
- Nếu phần vượt do rủi ro đã nhận diện trong Risk Register, PM có thể đề xuất dùng Contingency Reserve theo quy trình đã phê duyệt.
- Nếu phần vượt do thay đổi phạm vi hoặc sự kiện chưa từng được nhận diện, PM cần trình Change Request hoặc xin sử dụng Management Reserve.

---

## III. Case study dẫn chứng thực tế

### Khủng hoảng dòng tiền âm do lập ngân sách thiếu chiều thời gian

**Bối cảnh:** PM của một dự án xây dựng hệ thống ERP nội bộ tính toán tổng chi phí dự án là `120,000 USD` cho 6 tháng. PM báo cáo con số tổng này và được duyệt. Công ty cam kết cấp tiền theo hạn mức chia đều `20,000 USD / tháng`.

**Vấn đề phát sinh:**

1. Vào tháng thứ 3, dự án bước vào giai đoạn mua sắm hạ tầng máy chủ vật lý và bản quyền phần mềm. Chi phí cần thanh toán ngay trong tháng tăng lên `60,000 USD`.
2. Vì ngân sách không được lập theo mô hình **Time-phased Budget**, bộ phận Kế toán từ chối giải ngân vượt hạn mức tháng do không nằm trong kế hoạch dòng tiền của doanh nghiệp.
3. Nhà cung cấp thiết bị từ chối bàn giao phần cứng do chậm thanh toán, khiến tiến độ code của team Dev đóng băng suốt 1 tháng.

**Bài học rút ra:**

1. Tổng ngân sách đúng là chưa đủ. PM phải lập kế hoạch chi tiêu chi tiết theo thời gian và milestone.
2. Các khoản mua sắm lớn, license, phí vendor và chi phí audit cần được đánh dấu sớm để Finance chuẩn bị dòng tiền.
3. Funding Limit Reconciliation cần được thực hiện trước khi baseline được phê duyệt, không chờ đến khi phát sinh hóa đơn.

---

## IV. Tips & điều lưu ý thực chiến cho PM/PO

1. **Kiểm soát chặt đường chặn Funding Limit:** Luôn so sánh chi phí tích lũy dự kiến với hạn mức cấp vốn tối đa của công ty tại từng thời điểm. Nếu S-Curve vượt hạn mức cấp vốn, PM phải điều chỉnh schedule, milestone thanh toán hoặc kế hoạch mua sắm.

2. **Không nhập nhằng Contingency Reserve và Management Reserve:** Contingency Reserve dùng cho rủi ro đã nhận diện và nằm trong Cost Baseline. Management Reserve dùng cho unknown-unknowns, nằm ngoài Cost Baseline và cần phê duyệt cấp quản lý. Team dev xin thêm tiền sửa bug thông thường không phải lý do tự động dùng Management Reserve.

3. **Theo dõi Burn Rate trong Agile:** Với dự án Scrum, ngân sách thường được tính dựa trên chi phí duy trì team trong một sprint, gồm lương, công cụ, môi trường và vận hành. PM/PO cần theo dõi burn rate để cảnh báo sớm nếu Product Backlog phình to trong khi ngân sách còn lại giảm nhanh.

4. **Gắn budget với milestone và acceptance criteria:** Đừng chỉ cấp ngân sách theo tháng. Với vendor hoặc team outsource, nên gắn thanh toán với deliverable rõ ràng, biên bản nghiệm thu và tiêu chí hoàn tất.

5. **Baseline phải được kiểm soát bằng Change Control:** Khi Cost Baseline đã được phê duyệt, mọi thay đổi làm tăng hoặc tái phân bổ ngân sách đáng kể cần đi qua Change Control Board (CCB) hoặc cơ chế phê duyệt tương đương.

6. **Tách ngân sách CAPEX và OPEX nếu cần:** Dự án công nghệ thường có chi phí đầu tư ban đầu như license, thiết bị, setup cloud và chi phí vận hành định kỳ như subscription, support, monitoring. Tách đúng giúp Finance xử lý kế toán và dòng tiền chính xác hơn.

---

## V. Tài liệu & nguồn tham khảo

### 1. Chuẩn quốc tế & sách gối đầu giường

- *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) - 6th Edition*, Chapter 7: Project Cost Management, Section 7.3 Determine Budget.
- *Project Finance for Business Development* - S. Shishido, John Wiley & Sons.

### 2. Blog & bài viết tài chính chuyên ngành

- PMI.org: *Establishing and Maintaining the Project Cost Baseline*.
- ProjectManager.com: *How to Create a Project Budget: Step-by-Step Guide*.

### 3. Video / YouTube hữu ích

- Search keyword: *"Determine Budget Process PMP - Cost Baseline vs Project Budget"* (Ricardo Vargas).
- Search keyword: *"How to draw a Project Cost S-Curve in Excel"*.
