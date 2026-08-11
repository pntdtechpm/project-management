# 03-PROJECT-EXECUTION: BÀI 04 - CHANGE REQUEST (YÊU CẦU THAY ĐỔI DỰ ÁN)

## 1. KHUNG KIẾN THỨC CHUẨN PMP (PMBOK 6 & 7) & LIÊN HỆ THỰC TẾ

### A. Khái niệm theo chuẩn Quản trị Dự án Quốc tế (PMP)

Thay đổi là điều tất yếu trong quản lý dự án. Sự khác biệt giữa một dự án thành công và thất bại nằm ở cách kiểm soát và ứng xử với sự thay đổi đó.

* **PMBOK 6th Edition:**
* Thay đổi được quản lý tập trung thông qua quy trình **Perform Integrated Change Control** (Thực hiện kiểm soát thay đổi tích hợp) thuộc nhóm quy trình *Monitoring & Controlling*.
* Bất kỳ yêu cầu thay đổi (**Change Request - CR**) nào ảnh hưởng đến các Đường cơ sở (**Baselines**: *Scope, Schedule, Cost*) đều phải được tài liệu hóa, đánh giá tác động và trình lên **Hội đồng Kiểm soát Thay đổi (Change Control Board - CCB)** phê duyệt trước khi thi hành.


* **PMBOK 7th Edition & Agile:**
* Thuộc **Development Approach and Life Cycle Performance Domain** và **Delivery Performance Domain**.
* Tuyên ngôn Agile nhấn mạnh: *"Đón nhận sự thay đổi hơn là tuân thủ nghiêm ngặt kế hoạch"* (Responding to change over following a plan).
* Trong dự án Agile/Hybrid, quản lý thay đổi không có nghĩa là loại bỏ thủ tục, mà là biến sự thay đổi thành cơ hội gia tăng giá trị cho sản phẩm. Thay đổi scope được thực hiện thông qua hoạt động **Product Backlog Refinement** và **Prioritization** (Sắp xếp ưu tiên Backlog) của Product Owner.



### B. Liên hệ Thực tế Quản lý Sản phẩm (Product Management)

* **Phân biệt ranh giới:** Cần phân biệt rõ giữa **Tư duy linh hoạt (Agile Adaptability)** và **Phù dung phạm vi (Scope Creep)**.
* *Agile Adaptability:* Thay đổi dựa trên dữ liệu người dùng, phản hồi thị trường, có tính toán ROI và đánh giá sự đánh đổi (Trade-off).
* *Scope Creep:* Thay đổi ngẫu hứng, liên tục thêm tính năng "nhỏ nhỏ" theo cảm tính của Stakeholder/Sponsor mà không đánh giá tác động, dẫn đến vỡ tiến độ và đuối sức cho team.


* **Mục đích cốt lõi của Change Request:**
1. **Bảo vệ Đội ngũ:** Tránh việc team phát triển bị xáo trộn kế hoạch liên tục giữa Sprint.
2. **Minh bạch sự đánh đổi (Trade-off):** Giúp Stakeholder hiểu rõ: *"Thêm tính năng A nghĩa là phải tăng Ngân sách, dời Deadline hoặc Cắt bỏ tính năng B"*.



---

## 2. CẤU TRÚC BỘ CÔNG CỤ & KHUNG FILE CHANGE REQUEST (ARTIFACTS)

Một quy trình Change Request chuyên nghiệp cần bao gồm 2 file công cụ chính:

### A. Mẫu phiếu Yêu cầu Thay đổi (Change Request Form)

Phiếu do bên yêu cầu (Stakeholder, Khách hàng hoặc PM/PO) lập khi muốn thay đổi Scope, Tech, Deadline hoặc Resource:

| Trường thông tin | Mô tả chi tiết |
| --- | --- |
| **CR ID & Title** | Mã CR (Ví dụ: `CR-012`) và Tiêu đề tóm tắt yêu cầu. |
| **Requester & Date** | Họ tên người yêu cầu & Ngày tạo yêu cầu. |
| **Change Description** | Mô tả chi tiết hiện trạng vs. Trạng thái mới mong muốn. |
| **Business Reason / Value** | Lý do kinh doanh & Giá trị mang lại (Tại sao phải làm thay đổi này?). |
| **Impact Analysis** | **Phần quan trọng nhất do PM/PO & Tech Lead phân tích:**<br>

<br>• *Scope Impact:* Thêm/bớt bao nhiêu Story Points/Tasks?<br>

<br>• *Schedule Impact:* Trễ tiến độ bao nhiêu ngày/Sprint?<br>

<br>• *Cost Impact:* Chi phí phát sinh (AWS, API 3rd party, nhân sự)?<br>

<br>• *Risk Impact:* Phát sinh rủi ro kỹ thuật hay bảo mật nào? |
| **Proposed Action** | Phương án đề xuất (Làm ngay / Dời sang Phase sau / Swap Scope). |

### B. Nhật ký Kiểm soát Thay đổi (Change Log)

File tổng hợp theo dõi toàn bộ trạng thái CR của dự án (trên Excel, Google Sheets hoặc Jira Service Management):

```
[CR ID] | [Tiêu đề] | [Người yêu cầu] | [Mức ưu tiên] | [Tác động Tiến độ/Chi phí] | [Trạng thái] | [Người duyệt]

```

*Trạng thái CR:* `Draft` ➔ `Under Review` ➔ `Approved` ➔ `Rejected` ➔ `Deferred` (Hoãn).

---

## 3. QUY TRÌNH QUẢN LÝ THAY ĐỔI (CHANGE CONTROL PROCESS)

Một quy trình xử lý Change Request tiêu chuẩn trải qua 5 bước:

1. **Submit (Gửi CR):** Người yêu cầu điền phiếu CR Form nêu rõ mong muốn và lý do.
2. **Impact Analysis (Đánh giá tác động 360 độ):** * PM/PO đánh giá ảnh hưởng tới Business Value và Timeline.
* Tech Lead đánh giá ảnh hưởng tới Architecture, Tech Debt và Security.
* QA Lead đánh giá ảnh hưởng tới thời gian Testing và Regression.


3. **Review & Decision (Review & Ra quyết định):**
* *Mô hình Waterfall/PMP traditional:* Họp **CCB** (gồm Sponsor, PM, Key Stakeholders) để bỏ phiếu Approved / Rejected.
* *Mô hình Agile:* Product Owner cùng Stakeholder xem xét. Sử dụng cơ chế **Swap Scope** (Đổi tính năng có độ ưu tiên thấp hơn ra khỏi Backlog để nhường chỗ cho CR mới có giá trị cao hơn).


4. **Implement & Update Baseline (Triển khai & Cập nhật Đường cơ sở):**
* Nếu được duyệt, PM cập nhật lại Project Plan / Product Backlog.
* Truyền thông cho toàn đội ngũ về Scope mới.


5. **Close & Log (Đóng & Lưu trữ):** Cập nhật trạng thái cuối cùng vào **Change Log**.

---

## 4. CASE STUDY THỰC TẾ: DỰ ÁN "EPIC CENTER"

* **Bối cảnh:** Dự án đang ở giữa Sprint 6/10 (Triển khai tính năng quản lý danh sách Homestay). Sponsor dự án đột ngột yêu cầu: *"Bổ sung gấp tính năng eKYC (Xác thực Căn cước công dân gắn chip) khi chủ nhà đăng ký niêm yết Homestay để tuân thủ quy định pháp lý mới vừa ban hành"*.
* **Xử lý theo Quy trình Change Request:**
* **Bước 1 (Lập CR):** PO khởi tạo `CR-012: Tích hợp eKYC xác thực Căn cước công dân`.
* **Bước 2 (Đánh giá tác động - Impact Analysis):**
* *Kỹ thuật:* Cần mua SDK eKYC của FPT/VNPT và tích hợp luồng OCR + Face Matching.
* *Tiến độ:* Tốn thêm **02 Sprints (4 tuần làm việc)** của đội Dev & QA.
* *Chi phí:* Phát sinh $300/tháng chi phí gọi API eKYC.
* *Tác động vỡ kế hoạch:* Nếu làm ngay, ngày Launching dự án sẽ bị trễ 3 tuần.


* **Bước 3 (Thương lượng & Ra quyết định với Sponsor):** Duy (Product Owner) đưa ra 2 lựa chọn cho Sponsor:
* *Option A:* Tăng budget, dời ngày Launching dự án thêm 3 tuần.
* *Option B (Swap Scope):* Giữ nguyên ngày Launching, nhưng tạm thời hoãn tính năng *"Chương trình Khuyến mãi & Vouchers"* (chưa gấp) sang Phase 2 để dồn lực làm eKYC ngay trong Sprint 7 & 8.


* **Kết quả:** Sponsor đồng ý **Option B (Swap Scope)**. CR-012 được đánh dấu `Approved`. Tiến độ tổng thể của dự án Epic Center giữ vững được mốc Release Target ban đầu mà vẫn đảm bảo tuân thủ pháp lý.



---

## 5. CÁC TIPS & ĐIỀU LƯU Ý THỰC CHIẾN (ANTI-PATTERNS & SOLUTIONS)

| Sai lầm phổ biến (Anti-Pattern) | Hậu quả | Giải pháp thực chiến |
| --- | --- | --- |
| **"Nhận lời thay đổi qua trò chuyện/tin nhắn chat"** | Dev sửa code theo lời nói miệng, cuối cùng bị bug, trễ Deadline mà không ai chịu trách nhiệm. | Áp dụng quy tắc thép: **"No CR, No Do"** (Không có file CR được duyệt = Không sửa code/design). |
| **Sợ thay đổi, từ chối cứng nhắc mọi yêu cầu** | Sản phẩm ra mắt đúng tiến độ nhưng bị thị trường đào thải vì lỗi thời/không đúng nhu cầu thực tế. | Chuyển tư duy từ "Kiểm soát ngăn chặn" sang "Cố vấn giá trị". Giải thích cho Stakeholder bài toán ROI thay vì chỉ nói "Không làm được". |
| **Đánh giá tác động hời hợt (Chỉ tính Dev time)** | Quên mất thời gian cho QA Test, thời gian chỉnh sửa UI/UX, viết Tài liệu hướng dẫn hay config Hạ tầng AWS ➔ Trễ Deadline. | Checklist Impact Analysis phải luôn phủ đủ 5 khía cạnh: **Design ➔ Dev ➔ QA ➔ Infra/Ops ➔ Documentation/Training**. |
| **Sự thay đổi liên tục làm vỡ Sprint đang chạy** | Đội ngũ bị xáo trộn tâm lý, xé lẻ tập trung (Context switching). | Thiết lập nguyên tắc **"Sprint Backlog là Bất khả xâm phạm"** (trừ sự cố sập hệ thống). Mọi CR mới sẽ được xếp hàng vào Product Backlog để làm ở Sprint kế tiếp. |

---

## 6. NGUỒN THAM KHẢO CHẤT LƯỢNG (BLOGS, BOOKS & YOUTUBE)

1. **Chuẩn quốc tế & Sách:**
* *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) – 6th Edition* (Quy trình *Perform Integrated Change Control*).
* *Agile Practice Guide* (Phần *Managing Change in Agile Projects*).
* *Software Extension to the PMBOK® Guide Fifth Edition* (Quản lý thay đổi trong dự án phần mềm).


2. **Blog chuyên ngành uy tín:**
* **ProjectManagement.com:** *Managing Change Requests Without Destroying Stakeholder Relationships*.
* **ProductPlan Blog:** *Scope Creep: Definition & How Product Managers Can Avoid It*.
* **Atlassian Agile Coach:** *Managing change in agile development*.


3. **Kênh YouTube tham khảo:**
* **Praizion Performance Management:** Video *Perform Integrated Change Control - PMP Exam Prep*.
* **ProjectManager:** Video *How to Control Change Requests in Project Management*.
* **Agile Academy:** *How to Handle Scope Changes in Scrum*.


