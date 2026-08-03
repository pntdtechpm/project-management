# 02-PROJECT-PLANNING: BÀI 10 - QUALITY PLAN (KẾ HOẠCH QUẢN LÝ CHẤT LƯỢNG)

**Tên tài liệu:** `02-project-planning/quality-plan.md`  
**Chủ đề:** Kế hoạch Quản lý Chất lượng Dự án (Project Quality Management Plan) theo chuẩn PMP  
**Đối tượng hướng tới:** Project Manager (PM), Quality Assurance (QA) Lead, Product Owner (PO), Technical Lead và đội ngũ lập trình/kiểm thử.

---

## I. Khung kiến thức chuẩn PMP (PMBOK® Guide - 6th Edition)

### 1. Định nghĩa & bản chất của Quality Plan

Theo chuẩn *PMBOK® Guide - 6th Edition*, quy trình **8.1: Plan Quality Management**, **Quality Management Plan** là một cấu phần của kế hoạch tổng thể, mô tả cách thức tổ chức sẽ thực thi chính sách chất lượng (quality policy), xác định các tiêu chuẩn chất lượng (quality standards) áp dụng cho dự án và cách thức dự án sẽ chứng minh sự tuân thủ các tiêu chuẩn đó.

Quality Plan giúp PM và team trả lời các câu hỏi cốt lõi:

- Sản phẩm phải đạt tiêu chuẩn chất lượng nào?
- Tiêu chuẩn đó được đo bằng chỉ số cụ thể nào?
- Ai chịu trách nhiệm đảm bảo và kiểm soát chất lượng?
- Quality gates nào phải vượt qua trước khi release?
- Nếu chất lượng không đạt, quy trình xử lý và escalation ra sao?

### 2. Ba khái niệm cốt lõi về chất lượng trong PMP

#### a. Quality (Chất lượng) vs. Grade (Cấp độ/Hạng)

PMBOK phân biệt rõ hai khái niệm này để tránh hiểu nhầm trong thiết kế sản phẩm:

- **Quality (Chất lượng):** Mức độ mà một tập hợp các đặc tính vốn có đáp ứng các yêu cầu. Dự án **ít chất lượng (Low Quality)** luôn là vấn đề nghiêm trọng.
- **Grade (Cấp độ/Hạng):** Chỉ danh mục hoặc chỉ số phân loại thiết kế dành cho các sản phẩm bàn giao có cùng mục đích sử dụng nhưng khác nhau về đặc tính kỹ thuật. Sản phẩm **cấp độ thấp (Low Grade)** không phải là vấn đề, miễn là nó vận hành đúng yêu cầu, ổn định và ít lỗi.

Ví dụ: Một ứng dụng ngân hàng giao diện tối giản, ít chức năng nâng cao (Low Grade) nhưng chạy nhanh, ổn định và không sập (High Quality) vẫn tốt hơn một ứng dụng nhiều hiệu ứng, hàng trăm tính năng phức tạp (High Grade) nhưng liên tục treo hoặc xử lý sai giao dịch (Low Quality).

#### b. Quality Assurance (QA) vs. Quality Control (QC)

- **Quality Assurance - QA (Đảm bảo chất lượng):** Định hướng theo **quy trình (process-oriented)**. QA tập trung vào việc xây dựng quy trình chuẩn, kiểm toán quy trình (Quality Audit) và **phòng ngừa lỗi (Prevention)** ngay từ khâu sản xuất.
- **Quality Control - QC (Kiểm soát chất lượng):** Định hướng theo **sản phẩm (product-oriented)**. QC tập trung vào việc kiểm tra, test sản phẩm bàn giao thực tế để **phát hiện lỗi (Inspection)** trước khi giao cho khách hàng.

Trong dự án phần mềm Agile/Hybrid, QA tốt không chỉ ngồi cuối quy trình để test. QA nên tham gia từ refinement, góp ý acceptance criteria, xác định test strategy và giúp team chuyển chất lượng sang trái (Shift-left).

#### c. Cost of Quality (CoQ - Chi phí Chất lượng)

CoQ là tổng toàn bộ chi phí đầu tư để phòng ngừa sự không tuân thủ tiêu chuẩn, cộng với chi phí phát sinh do sản phẩm bị lỗi.

```text
                                  COST OF QUALITY (CoQ)
                                            |
           +--------------------------------+--------------------------------+
           |                                                                 |
           v                                                                 v
Cost of Conformance (Chi phí tuân thủ)                            Cost of Nonconformance (Chi phí không tuân thủ)
(Đầu tư để tránh thất bại)                                        (Chi phí phải trả vì thất bại)
  |-- Prevention Costs                                             |-- Internal Failure Costs
  |   |-- Sửa quy trình                                            |   |-- Sửa bug trước release
  |   |-- Đào tạo                                                  |   |-- Rework do kiểm thử fail
  |   |-- Code review                                              |
  |
  |-- Appraisal Costs                                              |-- External Failure Costs
      |-- Testing                                                  |   |-- Sửa bug trên Production
      |-- QA audit                                                 |   |-- Đền bù khách hàng
      |-- Security scanning                                        |   |-- Mất uy tín thương hiệu
```

---

## II. Ví dụ & minh họa thực tế

### Ví dụ: Thiết lập tiêu chí & kế hoạch chất lượng cho Module eKYC & Ví "Epic Center"

Một Quality Plan thực chiến phải biến các định nghĩa chung chung thành các **chỉ số chất lượng đo lường được (Quality Metrics)**.

### 1. Bảng chỉ số chất lượng (Quality Metrics Matrix)

| Đối tượng bàn giao | Tiêu chuẩn / tiêu chí chất lượng (Quality Metric) | Phương pháp QC / kiểm tra | Tần suất kiểm tra |
| --- | --- | --- | --- |
| **Module OCR Giấy tờ** | Tỷ lệ trích xuất chính xác thông tin CCCD >= 98.5%. Thời gian xử lý < 1.5 giây / hình ảnh. | Automation Test với bộ mẫu 10,000 ảnh CCCD thực tế. | Mỗi đợt build trong CI/CD Pipeline |
| **Luồng Face Matching** | Tỷ lệ nhận diện nhầm người (False Acceptance Rate - FAR) < 0.01%. | Security Testing và bộ test nhận diện chuyên sâu. | Trước mỗi đợt UAT |
| **Hệ thống Backend API** | Response Time < 200 ms ở mức tải 2,000 user đồng thời. | Load Testing / Performance Testing bằng JMeter hoặc công cụ tương đương. | Cuối mỗi Sprint |
| **Mã nguồn (Source Code)** | Unit Test Coverage >= 80%. Không có lỗi bảo mật mức Critical trên SonarQube. | Static Code Analysis, Peer Code Review và kiểm tra PR. | Khi Dev tạo Pull Request |

### 2. Ví dụ Quality Gates cho CI/CD

| Gate | Điều kiện pass | Người chịu trách nhiệm | Hành động nếu fail |
| --- | --- | --- | --- |
| Pull Request Gate | Code review xong, unit test pass, không có secret hardcode | Dev Lead | Không cho merge |
| Build Gate | Build thành công, lint pass, dependency scan không có lỗi Critical | DevOps / Tech Lead | Chặn deploy lên Staging |
| Staging Gate | Regression test pass, bug High/Critical = 0 | QA Lead | Không cho UAT |
| Release Gate | UAT sign-off, performance đạt ngưỡng, rollback plan sẵn sàng | PM / PO / QA Lead | Không Go-live hoặc giảm scope |

---

## III. Case study dẫn chứng thực tế

### Thảm họa 2 triệu USD do cắt giảm Prevention Cost để kịp deadline

**Bối cảnh:** Một công ty ví điện tử du lịch cố gắng chạy đua Go-live trước dịp nghỉ lễ lớn. Để kịp tiến độ, PM cắt giảm giai đoạn Code Review, bỏ qua Stress Test và rút ngắn thời gian UAT từ 2 tuần xuống 2 ngày.

**Vấn đề phát sinh:**

1. Khi lượng người dùng đặt phòng tăng đột biến trong ngày đầu lễ, một lỗi bất đồng bộ (Race Condition) trong module thanh toán bị kích hoạt.
2. Hệ thống bị trùng lặp giao dịch (Double Charge) trên 5,000 tài khoản khách hàng.
3. Hệ thống CSKH bị quá tải vì lượng cuộc gọi khiếu nại tăng mạnh.
4. Công ty phải tốn 200,000 USD chi phí đền bù voucher, 500,000 USD phạt hợp đồng từ ngân hàng đối tác và ước tính thiệt hại hơn 1.5 triệu USD giá trị thương hiệu do truyền thông tiêu cực.

**Bài học rút ra:**

1. Chi phí khắc phục sự cố trên môi trường thật (**External Failure Cost**) thường đắt hơn rất nhiều so với chi phí đầu tư cho Code Review và Automated Testing (**Prevention Cost**).
2. Quality Plan phải là ranh giới kỹ thuật được thống nhất trước, không thể bị vi phạm chỉ vì áp lực tiến độ ngắn hạn.
3. Nếu bắt buộc rút ngắn thời gian, PM/PO nên giảm scope release thay vì cắt bỏ các quality gates cốt lõi.

---

## IV. Tips & điều lưu ý thực chiến cho PM/PO

### 1. Quality is built-in, not inspected-in

Đừng trông chờ QA/Tester tìm hết bug ở cuối quy trình. Hãy áp dụng tư duy **Shift-left Testing**: đưa kiểm thử vào ngay từ khâu viết User Story, xác định rõ acceptance criteria và yêu cầu Dev viết unit test trước khi đẩy code.

### 2. Dùng Definition of Done nghiêm ngặt

Đưa các tiêu chuẩn chất lượng vào **Definition of Done (DoD)** của Sprint. Một User Story chỉ được công nhận hoàn thành 100% khi:

- Code pass unit test
- Đã qua code review
- Không có lỗi SonarQube mức Critical
- QA xác nhận pass test case
- Không còn bug Severity High/Critical
- Tài liệu hoặc release note liên quan đã được cập nhật nếu cần

### 3. Áp dụng tự động hóa trong CI/CD Pipeline

Tích hợp công cụ kiểm tra chất lượng mã nguồn tự động như SonarQube, ESLint, dependency scanning và secret scanning trực tiếp vào quy trình đẩy code. Nếu code không đạt chỉ số chất lượng tối thiểu, hệ thống phải tự động chặn merge hoặc deploy.

### 4. Định nghĩa rõ ngưỡng chấp nhận lỗi

Không phải mọi bug đều có cùng mức độ nghiêm trọng. Quality Plan nên quy định rõ:

- Severity Critical: chặn release
- Severity High: chặn release trừ khi có waiver được Sponsor/PO phê duyệt
- Severity Medium: cần kế hoạch fix rõ ràng
- Severity Low: có thể đưa vào backlog nếu không ảnh hưởng trải nghiệm chính

---

## V. Template Quality Plan nên dùng

| Trường thông tin | Nội dung cần có |
| --- | --- |
| Quality Objectives | Mục tiêu chất lượng của dự án |
| Quality Standards | Tiêu chuẩn áp dụng: nội bộ, bảo mật, hiệu năng, compliance |
| Quality Metrics | Chỉ số đo lường cụ thể và ngưỡng pass/fail |
| QA Activities | Hoạt động đảm bảo chất lượng theo quy trình |
| QC Activities | Hoạt động kiểm soát chất lượng theo sản phẩm |
| Quality Gates | Các cổng kiểm soát trước merge, deploy, UAT và release |
| Definition of Done | Tiêu chí hoàn thành cho user story hoặc deliverable |
| Test Coverage Target | Mục tiêu unit test, integration test, regression test |
| Defect Management | Cách phân loại severity, priority, SLA fix bug |
| Tooling | SonarQube, ESLint, JMeter, test automation, CI/CD |
| Roles & Responsibilities | PM, PO, QA Lead, Tech Lead, Developer, DevOps |
| Reporting Cadence | Tần suất báo cáo quality metrics |
| Waiver Process | Quy trình ngoại lệ nếu phải release khi còn lỗi |

---

## VI. Tài liệu & nguồn tham khảo

### 1. Chuẩn quốc tế & sách gối đầu giường

- *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) - 6th Edition*, Chapter 8: Project Quality Management.
- *Continuous Delivery: Reliable Software Releases through Build, Test, and Deployment Automation* - Jez Humble & David Farley.

### 2. Blog chuyên môn toàn cầu

- PMI.org: *Understanding the Cost of Quality (CoQ) in Software Engineering*.
- Atlassian Agile Coach: *Quality Assurance vs Quality Control in Agile Teams*.

### 3. Video / YouTube hữu ích

- Search keyword: *"Cost of Quality PMP Explained - Conformance vs Non-Conformance"*.
- Search keyword: *"Shift Left Testing Strategy in Software Projects"*.
