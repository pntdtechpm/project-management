# 02-PROJECT-PLANNING: BÀI 13 - COST ESTIMATION (ƯỚC TÍNH CHI PHÍ DỰ ÁN)

**Tên tài liệu:** `02-project-planning/cost-estimation.md`  
**Chủ đề:** Ước tính Chi phí Dự án (Project Cost Estimation) theo chuẩn PMP  
**Đối tượng hướng tới:** Project Manager (PM), Product Owner (PO), Business Analyst (BA), Technical Lead và Financial/Cost Analyst.

---

## I. Khung kiến thức chuẩn PMP (PMBOK® Guide - 6th Edition)

### 1. Định nghĩa & bản chất của Cost Estimation

Theo PMBOK® Guide 6th Edition, quy trình **Estimate Costs** (Process 7.2) là quá trình phát triển một giá trị ước tính gần đúng (*approximation*) về các nguồn lực tài chính cần thiết để hoàn thành toàn bộ công việc của dự án.

**Bản chất của ước tính:** Ước tính là dự đoán dựa trên thông tin hiện có tại một thời điểm nhất định. Khi thông tin dự án ngày càng chi tiết hơn thông qua **Progressive Elaboration** (phát triển lũy tiến), độ chính xác của ước tính chi phí sẽ tăng lên tương ứng.

Cost Estimation không chỉ là "đoán một con số". Đây là hoạt động phân tích có cơ sở, cần gắn với phạm vi, WBS, resource plan, schedule, risk register, quality plan và các giả định tài chính của tổ chức.

### 2. Mức độ chính xác của ước tính theo vòng đời dự án

PMBOK phân loại độ chính xác của ước tính theo từng giai đoạn triển khai:

- **Rough Order of Magnitude - ROM (Ước tính sơ bộ):** Thường được thực hiện ở giai đoạn Khởi tạo (Initiation), khi thông tin còn ít. Biên độ dao động thường nằm trong khoảng **-25% đến +75%**.
- **Budget Estimate (Ước tính ngân sách):** Thường được thực hiện ở giai đoạn lập kế hoạch sớm, khi phạm vi và cách tiếp cận đã rõ hơn. Biên độ dao động thường nằm trong khoảng **-10% đến +25%**.
- **Definitive Estimate (Ước tính xác định / chi tiết):** Được thực hiện khi đã có WBS, đặc tả kỹ thuật, resource plan và dữ liệu triển khai đủ chi tiết. Biên độ dao động thường hẹp nhất, khoảng **-5% đến +10%**.

### 3. Bốn kỹ thuật ước tính chi phí cốt lõi

#### 3.1. Analogous Estimating (Ước tính tương tự - Top-Down)

**Cách làm:** Dùng chi phí thực tế của các dự án tương tự trong quá khứ làm căn cứ ước tính cho dự án hiện tại.

**Đặc điểm:** Thực hiện nhanh, tốn ít chi phí nhưng độ chính xác thấp. Kỹ thuật này phù hợp với giai đoạn ROM hoặc khi tổ chức cần số liệu sơ bộ để quyết định có tiếp tục phân tích dự án hay không.

#### 3.2. Parametric Estimating (Ước tính tham số)

**Cách làm:** Sử dụng mối quan hệ thống kê giữa dữ liệu lịch sử và các tham số đo lường. Ví dụ: `50 USD / dòng code`, `100 USD / m2 xây dựng`, `500 USD / Story Point`.

**Đặc điểm:** Độ chính xác cao hơn Analogous nếu mô hình tham số đáng tin cậy, dữ liệu lịch sử đủ sạch và tham số đầu vào phản ánh đúng độ phức tạp thực tế.

#### 3.3. Bottom-Up Estimating (Ước tính từ dưới lên)

**Cách làm:** Phân rã dự án đến cấp nhỏ nhất có thể quản lý được, thường là Work Package trong WBS hoặc task chi tiết, sau đó ước tính từng phần và cộng dồn (*roll up*) lên cấp tổng thể.

**Đặc điểm:** Có độ chính xác cao nhất trong nhóm kỹ thuật phổ biến, phù hợp với Definitive Estimate, nhưng tốn nhiều thời gian và chi phí thực hiện nhất.

#### 3.4. Three-Point Estimating (Ước tính 3 điểm - PERT)

**Cách làm:** Tính toán chi phí dựa trên ba kịch bản để phản ánh rủi ro và độ biến động:

- **Optimistic (Co):** Kịch bản lạc quan, khi mọi việc thuận lợi nhất.
- **Most Likely (Cm):** Kịch bản khả thi nhất, trong điều kiện làm việc bình thường.
- **Pessimistic (Cp):** Kịch bản bi quan, khi các rủi ro chính xảy ra.

**Công thức PERT phân bố Beta (Weighted Average):**

```text
Ce = (Co + 4Cm + Cp) / 6
```

**Công thức phân bố tam giác (Triangular Distribution):**

```text
Ce = (Co + Cm + Cp) / 3
```

### 4. Cơ sở ước tính (Basis of Estimates - BoE)

Một sai lầm phổ biến của PM là chỉ đưa ra con số tổng mà không có tài liệu giải trình. PMBOK yêu cầu ước tính nên đi kèm **Basis of Estimates (BoE)** để mô tả:

- Các giả định (Assumptions) và hạn chế (Constraints) đã sử dụng.
- Phương pháp ước tính đã áp dụng.
- Dữ liệu đầu vào và nguồn tham chiếu.
- Mức độ tin cậy của con số ước tính (Confidence Level).
- Chi tiết các khoản dự phòng rủi ro đã tính toán.
- Các hạng mục bị loại trừ khỏi ước tính, nếu có.

BoE giúp Sponsor, Finance và Steering Committee hiểu vì sao con số được đưa ra, phạm vi con số bao gồm những gì và rủi ro tài chính nằm ở đâu.

---

## II. Ví dụ & minh họa thực tế

### Ví dụ: Áp dụng PERT 3 điểm cho module E-Coffer của dự án "Epic Center"

Giả định PM và Tech Lead cần ước tính chi phí phát triển module **Nạp tiền & Tích lũy E-Coffer**, bao gồm nhân sự, hạ tầng cloud API và chi phí kiểm toán an toàn thông tin.

- **Kịch bản lạc quan (Co):** `8,000 USD` - mọi API có sẵn, không phát sinh lỗi bảo mật.
- **Kịch bản khả thi nhất (Cm):** `12,000 USD` - tiến độ bình thường, có lỗi nhỏ nhưng xử lý được trong kế hoạch.
- **Kịch bản bi quan (Cp):** `22,000 USD` - lỗi kiến trúc, đối tác ngân hàng thay đổi API spec, phải kiểm thử lại từ đầu.

### 1. Tính chi phí dự kiến theo công thức Beta PERT

```text
Ce = (8,000 + 4 x 12,000 + 22,000) / 6
Ce = (8,000 + 48,000 + 22,000) / 6
Ce = 78,000 / 6
Ce = 13,000 USD
```

### 2. Tính độ lệch chuẩn để đo rủi ro biến động

```text
Standard Deviation (sigma) = (Cp - Co) / 6
sigma = (22,000 - 8,000) / 6
sigma = 14,000 / 6
sigma ≈ 2,333 USD
```

**Kết luận:** PM có thể báo cáo với Sponsor rằng chi phí ước tính cho module này là **13,000 USD**, với biên độ rủi ro khoảng **±2,333 USD**. Vùng tham chiếu một độ lệch chuẩn là khoảng **10,667 USD đến 15,333 USD**, tương ứng vùng tin cậy xấp xỉ **68%** nếu giả định phân bố phù hợp.

### 3. Ví dụ bảng Bottom-Up Estimate rút gọn

| Hạng mục | Cơ sở tính | Chi phí ước tính |
| --- | --- | ---: |
| Frontend Mobile | 12 man-day x 250 USD | 3,000 USD |
| Backend API | 18 man-day x 300 USD | 5,400 USD |
| Integration VietQR | 8 man-day x 320 USD | 2,560 USD |
| QA & Automation Test | 10 man-day x 220 USD | 2,200 USD |
| Cloud/Staging/API Gateway | Chi phí hạ tầng theo tháng | 1,200 USD |
| Security Review | Gói kiểm thử nội bộ/vendor | 2,500 USD |
| **Tổng trước dự phòng** |  | **16,860 USD** |

Bảng này có thể được dùng như dữ liệu đầu vào cho Budget, Cost Baseline và kế hoạch giải ngân theo milestone.

---

## III. Case study dẫn chứng thực tế

### Bài học vỡ quỹ 300% do bẫy Analogous Estimating rập khuôn

**Bối cảnh:** Một công ty dịch vụ tài chính bất động sản triển khai dự án nâng cấp core ứng dụng đặt phòng tích hợp ví tích lũy. PM sử dụng phương pháp **Analogous Estimating** dựa trên một dự án cũ đã làm hai năm trước: "Dự án trước làm module thanh toán mất 30,000 USD, dự án này chắc cũng khoảng 30,000 USD".

**Vấn đề phát sinh:**

1. PM bỏ qua thay đổi về tiêu chuẩn pháp lý. Luật và tiêu chuẩn an toàn thông tin mới yêu cầu eKYC phải có Liveness Detection chống deepfake.
2. Chi phí nhân sự kỹ thuật cao tăng mạnh, đặc biệt là Senior AI Engineer, DevOps và Security Specialist.
3. Dự án không xây dựng **Basis of Estimates (BoE)** nên khi chi phí đội lên 90,000 USD, Ban Giám đốc từ chối giải ngân thêm vì không thấy cơ sở giải trình rõ ràng.
4. Dự án bị đóng băng giữa chừng vì kiệt quệ tài chính và mất niềm tin từ Sponsor.

**Bài học rút ra:**

1. **Analogous Estimating** chỉ nên dùng ở vòng duyệt chủ trương ban đầu hoặc khi cần ROM.
2. Ngay khi có WBS và đặc tả kỹ thuật, PM nên chuyển sang **Bottom-Up Estimating** kết hợp **Three-Point Estimating** cho các hạng mục có rủi ro cao.
3. Mọi con số chi phí quan trọng cần có **Basis of Estimates** để bảo vệ logic ước tính, phạm vi bao gồm, giả định và khoản dự phòng.

---

## IV. Tips & điều lưu ý thực chiến cho PM/PO

1. **Phân biệt Direct Costs và Indirect Costs:** Direct Costs là chi phí gắn trực tiếp với dự án như lương lập trình viên, server AWS riêng, license kiểm thử hoặc phí vendor. Indirect Costs là chi phí dùng chung được phân bổ cho dự án như văn phòng, điện nước, kế toán, HR hoặc công cụ quản trị chung.

2. **Luôn tính Cost of Quality (CoQ):** Đừng chỉ ước tính chi phí viết code. Cần tính đủ chi phí code review, test case, automated testing, security review và UAT. Đây là chi phí tuân thủ (*cost of conformance*) giúp giảm chi phí sửa lỗi muộn (*cost of non-conformance*).

3. **Quy đổi Story Point / Man-day thành chi phí tiền tệ:** Với Agile/Hybrid, PM nên thống nhất burn rate theo vai trò hoặc theo team. Ví dụ: `1 Story Point = 0.75 man-day`, `burn rate team = 2,000 USD / ngày`, từ đó quy đổi backlog thành chi phí dự kiến.

4. **Tách Contingency Reserve và Management Reserve:** Contingency Reserve dùng cho rủi ro đã biết và có thể phân tích trong risk register. Management Reserve dùng cho rủi ro chưa biết, thường do Sponsor hoặc Steering Committee kiểm soát.

5. **Không ước tính chi phí nếu phạm vi chưa rõ:** Nếu scope, assumption hoặc acceptance criteria còn mơ hồ, PM nên ghi rõ mức độ tin cậy thấp và dùng ROM thay vì trình bày như một con số chắc chắn.

6. **Cập nhật estimate theo thay đổi phạm vi:** Khi Change Request được phê duyệt, cost estimate và cost baseline phải được cập nhật. Nếu không, báo cáo variance sẽ mất ý nghĩa vì đang so sánh chi phí thực tế với một baseline lỗi thời.

---

## V. Tài liệu & nguồn tham khảo

### 1. Chuẩn quốc tế & sách gối đầu giường

- *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) - 6th Edition*, Chapter 7: Project Cost Management, Section 7.2 Estimate Costs.
- *Project Cost Estimating Tools and Techniques* - Association for the Advancement of Cost Engineering (AACE).

### 2. Blog & bài viết chuyên ngành

- PMI.org: *Estimating Cost: Analogous, Parametric, Bottom-Up, and Three-Point Estimating*.
- ProjectManagement.com: *How to Write a Solid Basis of Estimates (BoE)*.

### 3. Video / YouTube hữu ích

- Search keyword: *"Cost Estimation Techniques PMP Exam - PERT, Bottom-Up, Parametric"* (Ricardo Vargas hoặc ProjectManager).
- Search keyword: *"How to estimate software development costs accurately"*.
