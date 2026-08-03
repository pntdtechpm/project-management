# 02-PROJECT-PLANNING: BÀI 06 - RESOURCE PLAN (KẾ HOẠCH NGUỒN LỰC)

**Tên tài liệu:** `02-project-planning/resource-plan.md`  
**Chủ đề:** Kế hoạch Quản lý Nguồn lực (Resource Management Plan) theo chuẩn PMP  
**Đối tượng hướng tới:** Project Manager (PM), Resource Manager, Tech Lead, PMO và bộ phận Tuyển dụng/Nhân sự (HR).

---

## I. Khung kiến thức chuẩn PMP (PMBOK® Guide - 6th Edition)

### 1. Định nghĩa & bản chất của Resource Plan

Theo chuẩn *PMBOK® Guide - 6th Edition* trong quy trình **9.1: Plan Resource Management**, **Resource Management Plan** là tài liệu cung cấp hướng dẫn về cách thức phân loại, phân bổ, quản lý và giải phóng các nguồn lực của dự án.

**Phạm vi nguồn lực rộng hơn nhân sự:** Trong PMP, nguồn lực (Resources) được chia làm hai loại lớn:

1. **Team Resources (Nguồn lực nhân sự):** Các thành viên trong đội ngũ dự án như Developers, Business Analysts, Testers, Project Manager, Product Owner, Tech Lead và DevOps.
2. **Physical Resources (Nguồn lực vật lý):** Vật liệu, thiết bị, máy móc, cơ sở hạ tầng, bản quyền phần mềm (Licenses), phòng làm việc, thiết bị mạng và môi trường cloud.

Resource Plan không chỉ trả lời câu hỏi "cần bao nhiêu người", mà còn xác định ai chịu trách nhiệm, khi nào cần tham gia, mức độ phân bổ bao nhiêu phần trăm, nguồn lực được lấy từ đâu và khi nào sẽ được giải phóng khỏi dự án.

### 2. Các công cụ định nghĩa vai trò & trách nhiệm

Để tránh tình trạng chồng chéo công việc, PMBOK khuyến nghị sử dụng các biểu đồ cấu trúc trực quan để phân định trách nhiệm.

**Hierarchical Charts (Biểu đồ phân cấp):**

- **OBS (Organizational Breakdown Structure):** Sắp xếp nguồn lực theo các phòng ban chức năng hiện tại của công ty, ví dụ Engineering, QA, Design, Infrastructure, Operations.
- **RBS (Resource Breakdown Structure):** Phân rã nguồn lực theo **loại (Type)** và **chủng loại (Category)**, ví dụ từ phần cứng như Server, PC đến nhân sự như Backend Developer, QA Engineer, Business Analyst.

**Matrix-based Charts (Biểu đồ dạng ma trận):**

- **RACI Matrix (Ma trận RACI):** Công cụ phổ biến nhất để định nghĩa mối quan hệ giữa các thành viên và các gói công việc (Work Packages).

Các ký hiệu trong RACI:

- **R - Responsible:** Người trực tiếp thực hiện công việc và tạo ra output.
- **A - Accountable:** Người chịu trách nhiệm tối cao về kết quả và có quyền phê duyệt. Mỗi gói công việc chỉ nên có duy nhất một chữ A.
- **C - Consulted:** Người cung cấp chuyên môn hoặc ý kiến tư vấn trước khi công việc được thực hiện.
- **I - Informed:** Người cần được cập nhật thông tin sau khi công việc hoàn thành hoặc có thay đổi quan trọng.

### 3. Chiến lược giải phóng nguồn lực (Resource Release Plan)

Một cấu phần thường bị bỏ quên trong Resource Plan là kế hoạch giải phóng nhân sự. Khi một cấu phần dự án kết thúc, ví dụ thiết kế UI/UX đã hoàn tất hoặc giai đoạn kiến trúc đã được phê duyệt, nhân sự cần được chuyển giao lại cho dự án khác hoặc phòng ban chức năng để tối ưu chi phí cho tổ chức.

Nếu không có Resource Release Plan, dự án dễ rơi vào hai vấn đề:

- **Bench time:** Nhân sự vẫn bị giữ trên dự án nhưng không còn đủ việc có giá trị.
- **Resource conflict:** Nhân sự bị kéo qua nhiều dự án cùng lúc vì không có ngày kết thúc phân bổ rõ ràng.

---

## II. Ví dụ & minh họa thực tế

### Ví dụ: Ma trận RACI và RBS cho Module eKYC thuộc Dự án "Epic Center"

### 1. Bảng phân rã nguồn lực (Resource Breakdown Structure - RBS mẫu)

```text
Hệ thống Epic Center V1.0
|
|-- Nhân sự (Team Resources)
|   |-- Đội phát triển (Engineering)
|   |   |-- 1 Backend Lead
|   |   |-- 2 Backend Developers
|   |   |-- 2 Mobile Developers
|   |
|   |-- Đội đảm bảo chất lượng (QA/QC)
|   |   |-- 1 QA Lead
|   |   |-- 2 Automation Testers
|   |
|   |-- Đội thiết kế
|       |-- 1 UI/UX Designer
|
|-- Vật lý (Physical Resources)
    |-- Hạ tầng đám mây (Cloud)
    |   |-- AWS Staging Environment
    |   |-- AWS Production Environment
    |   |-- AWS Rekognition License
    |
    |-- Phần cứng
        |-- 1 Mac mini M4 cho build và deploy ứng dụng iOS
```

### 2. Ma trận RACI cho các sản phẩm bàn giao chính

| Deliverables (từ WBS) | Project Manager (PM) | Product Owner (PO) | Tech Lead / Dev | QA Lead / Tester |
| --- | --- | --- | --- | --- |
| **Kế hoạch Dự án & Ngân sách** | **A** | C | I | I |
| **Tài liệu Nghiệp vụ (BRD/SRS)** | C | **A** | C | I |
| **Kiến trúc Hệ thống (Architecture)** | I | I | **A** | C |
| **Mã nguồn Module OCR & Core eKYC** | I | I | **A** (Lead) / **R** (Dev) | I |
| **Kịch bản & Báo cáo Kiểm thử UAT** | C | C | I | **A** (Lead) / **R** (Tester) |

### 3. Ví dụ lịch phân bổ nguồn lực theo giai đoạn

| Nguồn lực | Giai đoạn phân tích | Giai đoạn thiết kế | Giai đoạn phát triển | Giai đoạn kiểm thử/UAT | Giai đoạn Go-live |
| --- | ---: | ---: | ---: | ---: | ---: |
| PM | 50% | 60% | 70% | 80% | 100% |
| PO / BA | 100% | 80% | 50% | 80% | 60% |
| UI/UX Designer | 60% | 100% | 30% | 20% | 0% |
| Backend Lead | 30% | 80% | 100% | 80% | 100% |
| Backend Developers | 0% | 40% | 100% | 80% | 60% |
| QA Lead / Testers | 20% | 30% | 60% | 100% | 80% |
| DevOps | 20% | 50% | 60% | 80% | 100% |

---

## III. Case study dẫn chứng thực tế

### Khủng hoảng tranh giành nguồn lực tại tập đoàn công nghệ và bài học về quản trị ma trận

**Bối cảnh:** Một công ty công nghệ vận hành theo mô hình Ma trận yếu (Weak Matrix Organization). Dự án Core Banking Onboarding đang bước vào giai đoạn nước rút để kết nối hệ thống. PM của dự án cần sự hỗ trợ của chuyên gia tối ưu dữ liệu (Database Administrator - DBA) thuộc Phòng Hạ tầng của công ty.

**Vấn đề phát sinh:**

1. Do Resource Plan không được ký duyệt rõ ràng với Functional Manager, Trưởng phòng Hạ tầng đã điều động DBA đi xử lý một sự cố khẩn cấp của dự án khác mà không thông báo cho PM.
2. Dự án Core Banking bị đình trệ 1 tuần vì không có chuyên gia cấu hình database.
3. PM không thể ép buộc nhân sự làm việc vì quyền đánh giá lương thưởng và KPI của DBA nằm trong tay Functional Manager.
4. Xung đột leo thang làm mối quan hệ giữa PM và các phòng ban trở nên căng thẳng.

**Giải pháp khắc phục:**

1. Khi lập Resource Plan trong mô hình ma trận, PM cần ký kết thỏa thuận cung cấp nguồn lực nội bộ như **SLA / Resource Assignment** với Functional Manager.
2. Thiết lập **Escalation Path (Đường leo thang)** rõ ràng: nếu xung đột nguồn lực không thể tự thỏa thuận, vụ việc sẽ được đưa lên PMO hoặc Sponsor để phân định thứ tự ưu tiên dựa trên lợi ích chiến lược của công ty.
3. Đưa lịch phân bổ nguồn lực chủ chốt vào baseline kế hoạch, có owner, thời gian cam kết, phần trăm allocation và điều kiện thay đổi.

---

## IV. Tips & điều lưu ý thực chiến cho PM/PO

### 1. Tránh bẫy "một task có nhiều chữ A" trong ma trận RACI

Khi giao việc, nếu một công việc có tới 2 người cùng chịu trách nhiệm phê duyệt (Accountable), kết quả thường là không ai thật sự chịu trách nhiệm. Chỉ nên có duy nhất một người giữ chữ A cho mỗi deliverable hoặc work package.

### 2. Quản lý quá tải bằng Resource Histograms

Hãy sử dụng biểu đồ cột thể hiện số giờ làm việc của mỗi nhân sự theo tuần để phát hiện sớm hiện tượng **Over-allocation (Quá tải nguồn lực)**. Nếu một Developer bị xếp lịch làm việc 14 tiếng/ngày liên tục trong 2 tuần, dự án chắc chắn sẽ tăng nguy cơ bug lớn, giảm chất lượng review hoặc mất nhân sự.

### 3. Có kế hoạch dự phòng cho nhân sự chủ chốt

Luôn có phương án dự phòng cho trường hợp Tech Lead, Solution Architect, DBA hoặc DevOps Lead đột ngột nghỉ việc giữa chừng. Resource Plan nên quy định rõ cách giảm **Key-person Risk** thông qua:

- Pair programming
- Documentation bắt buộc cho kiến trúc, API và runbook
- Cross-training giữa các thành viên
- Backup owner cho các module quan trọng
- Review định kỳ các điểm phụ thuộc vào một cá nhân duy nhất

### 4. Phân biệt Resource Leveling và Resource Smoothing

- **Resource Leveling:** Điều chỉnh lịch dự án để giải quyết xung đột hoặc thiếu hụt nguồn lực, có thể làm thay đổi ngày hoàn thành.
- **Resource Smoothing:** Tối ưu phân bổ nguồn lực trong giới hạn schedule baseline hiện có, không làm thay đổi mốc hoàn thành đã cam kết.

Trong môi trường deadline cố định, PM nên ưu tiên Resource Smoothing trước. Nếu vẫn không đủ nguồn lực, cần escalation sớm thay vì âm thầm ép team làm quá tải.

---

## V. Template Resource Plan nên dùng

| Trường thông tin | Nội dung cần có |
| --- | --- |
| Resource Categories | Team resources và physical resources |
| RBS | Cấu trúc phân rã nguồn lực theo loại và nhóm |
| Role Description | Vai trò, trách nhiệm chính và kỹ năng yêu cầu |
| RACI Matrix | Responsible, Accountable, Consulted, Informed cho từng deliverable |
| Resource Calendar | Lịch làm việc, nghỉ phép, ngày lễ, availability |
| Allocation Plan | Tỷ lệ phân bổ theo tuần, Sprint hoặc phase |
| Acquisition Plan | Cách lấy nguồn lực: nội bộ, tuyển mới, vendor, contractor |
| Training Plan | Nhu cầu đào tạo, onboarding, chuyển giao kiến thức |
| Physical Resource Plan | Thiết bị, license, môi trường, cloud, phòng họp |
| Escalation Path | Quy trình xử lý thiếu hụt hoặc xung đột nguồn lực |
| Release Plan | Thời điểm giải phóng nguồn lực khỏi dự án |
| Key-person Risk Plan | Phương án dự phòng cho nhân sự chủ chốt |

---

## VI. Tài liệu & nguồn tham khảo

### 1. Chuẩn quốc tế & sách gối đầu giường

- *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) - 6th Edition*, Chapter 9: Project Resource Management.
- *Human Resource Management in Projects* - Brien Keegan.

### 2. Blog chuyên môn toàn cầu

- ProjectManagement.com: *Effective Resource Allocation and Management in Matrix Organizations*.
- PMI Today: *Mitigating Key-Person Risk in Complex Project Architectures*.

### 3. Video / YouTube hữu ích

- Search keyword: *"RACI Matrix Explained with Examples - PMBOK Framework"*.
- Search keyword: *"Resource Leveling vs Resource Smoothing in Project Management"*.
