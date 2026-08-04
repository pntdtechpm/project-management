# 03-PROJECT-EXECUTION: BÀI 02 - ISSUE LOG (NHẬT KÝ VẤN ĐỀ DỰ ÁN)

## 1. Khung kiến thức chuẩn PMP (PMBOK 6 & 7) & liên hệ thực tế

### A. Phân biệt cốt lõi: Risk (Rủi ro) vs. Issue (Vấn đề)

Một trong những nhầm lẫn lớn nhất của người làm dự án là không phân biệt được **Risk** và **Issue**:

- **Risk (Rủi ro):** Là sự kiện *chưa xảy ra* trong tương lai, có tính chất xác suất (`0% < xác suất < 100%`). Quản lý rủi ro là chủ động dự phòng (*proactive*).
- **Issue (Vấn đề):** Là sự kiện *đã và đang xảy ra* trong thực tế (`xác suất = 100%`), gây tác động trực tiếp đến tiến độ, chi phí, chất lượng hoặc phạm vi của dự án. Quản lý vấn đề là phản ứng và khắc phục (*reactive*).

### B. Khái niệm theo chuẩn PMP

**PMBOK 6th Edition:**

- **Issue Log** là một trong những đầu ra (Output) quan trọng của quy trình **Direct and Manage Project Work** và là đầu vào (Input) liên tục cho quy trình **Monitor and Control Project Work**.
- Issue Log được dùng để ghi nhận, theo dõi và bảo đảm mọi vấn đề phát sinh trong quá trình thực hiện dự án đều được phân công người chịu trách nhiệm và giải quyết dứt điểm.

**PMBOK 7th Edition & Agile:**

- Thuộc **Project Work Performance Domain** và **Delivery Performance Domain**.
- Trong dự án Agile/Scrum, các vấn đề nhỏ hằng ngày (*impediments/blockers*) được xử lý nhanh qua Daily Scrum. Tuy nhiên, với các vấn đề mang tính hệ thống như vướng mắc hợp đồng, sự cố tích hợp đối tác, thiếu hụt nhân sự cốt lõi hoặc thay đổi pháp lý, dự án bắt buộc phải ghi nhận vào **Issue Log** để có cơ chế theo dõi cấp quản lý (*management level tracking*).

---

## 2. Cấu trúc bộ công cụ & khung file Issue Log (Artifacts)

Một file **Issue Log** chuẩn, dù đặt trên Excel, Google Sheets, Jira Service Management hoặc Notion, cần bao gồm các trường thông tin cơ bản sau:

| Trường thông tin | Ý nghĩa & mô tả | Ví dụ thực tế |
| --- | --- | --- |
| **Issue ID** | Mã định danh duy nhất để truy vết. | `ISS-001`, `ISS-002` |
| **Raised Date & Raised By** | Ngày phát hiện và người phát hiện vấn đề. | `15/03/2026` - *Minh (QA Lead)* |
| **Issue Description** | Mô tả rõ ràng hiện trạng sự cố đang xảy ra. | *API cổng thanh toán MoMo bị gián đoạn kết nối do thay đổi cấu hình bảo mật từ đối tác.* |
| **Category** | Phân loại vấn đề. | `Technical`, `Vendor`, `Resource`, `Scope`, `Legal` |
| **Severity / Impact** | Mức độ nghiêm trọng. | `Critical` - chặn luồng đặt phòng chính |
| **Issue Owner** | Duy nhất một người chịu trách nhiệm thúc đẩy giải quyết. | *Tấn (Tech Lead)* |
| **Action Plan / Resolution** | Kế hoạch hoặc giải pháp khắc phục chi tiết. | *Tạm thời bật luồng thanh toán dự phòng chuyển khoản QR, liên hệ Lead Support MoMo xử lý IP Whitelist.* |
| **Target Resolution Date** | Hạn chót phải giải quyết xong. | `16/03/2026 - 12:00 PM` |
| **Status** | Trạng thái hiện tại. | `Open`, `In Progress`, `Escalated`, `Resolved`, `Closed` |

---

## 3. Quy trình quản lý vấn đề (Issue Life Cycle)

Một quy trình Issue Management tiêu chuẩn bao gồm 5 bước khép kín:

1. **Identify (Phát hiện & ghi nhận):** Bất kỳ ai trong team cũng có quyền phát hiện và khai báo issue vào Issue Log.
2. **Evaluate & Prioritize (Đánh giá & ưu tiên):** PM/PO cùng Tech Lead xác định mức độ ảnh hưởng (Impact) và độ khẩn cấp (Urgency) để xếp thứ tự ưu tiên.
3. **Assign Owner (Phân công trách nhiệm):** Gán chính xác một cá nhân làm chủ sở hữu issue.
4. **Execute Action Plan (Triển khai xử lý):** Owner phối hợp các bên liên quan để thực thi giải pháp.
5. **Review & Close (Nghiệm thu & đóng):** PM/PO xác nhận sự cố đã được khắc phục hoàn toàn, kiểm tra không phát sinh tác động phụ trước khi chuyển trạng thái sang `Closed`.

---

## 4. Case study thực tế: Dự án "Epic Center"

**Bối cảnh:** Dự án triển khai tính năng **Smart Check-in**, cho phép tự động mở khóa phòng homestay qua ứng dụng Epic Center.

**Sự cố phát sinh (Issue):** Vào chiều thứ Sáu, nhà cung cấp khóa thông minh bất ngờ cập nhật firmware hệ thống mà không báo trước, khiến toàn bộ khóa tại 50 căn homestay không nhận tín hiệu Bluetooth từ ứng dụng Epic Center. Khách hàng không thể nhận phòng.

**Đưa vào Issue Log & xử lý:**

- **Issue ID:** `ISS-089`
- **Category:** `Technical / External Partner`
- **Severity:** `Critical` - ảnh hưởng trực tiếp đến trải nghiệm người dùng cuối ngay thời điểm thực tế.
- **Issue Owner:** Duy (Product Owner) & Tech Lead.
- **Action Plan:**
  - **Giải pháp tình thế (Workaround):** Kích hoạt tự động gửi mã OTP mật khẩu số qua SMS/Zalo OA cho khách hàng để mở khóa thủ công trong thời gian chờ sửa code.
  - **Giải pháp gốc rễ (Root Cause Fix):** Đội Dev rollback SDK khóa về phiên bản stable và làm việc với bên cung cấp khóa để cấu hình lại cơ chế auto-update.
- **Kết quả:** Khách hàng vẫn check-in qua OTP dự phòng; issue được khắc phục hoàn toàn sau 4 giờ làm việc.

---

## 5. Các tips & điều lưu ý thực chiến (Anti-patterns & Solutions)

| Sai lầm phổ biến (Anti-Pattern) | Hậu quả | Giải pháp thực chiến |
| --- | --- | --- |
| **"Nghĩa địa Issue Log"** | Issue được ghi vào file nhưng không ai xem lại, file bị bỏ quên sau vài tuần. | Đưa Issue Log vào chương trình nghị sự định kỳ: review 10 phút trong các buổi họp tiến độ tuần hoặc Sprint Review. |
| **Ghi nhận mọi thứ thành Issue** | File Issue Log bị rác bởi hàng trăm bug nhỏ lẻ hoặc task tồn đọng. | Phân biệt rõ: bug giao diện/logic nhỏ đưa vào Product Backlog hoặc Jira Board. Chỉ những **sự cố nghẽn dòng chảy/nghiêm trọng** mới đưa vào Issue Log. |
| **Gán Issue cho nhiều người chung chung** | Không ai nhận trách nhiệm xử lý chính. | Áp dụng **nguyên tắc 1-1**: mỗi issue chỉ có duy nhất 1 owner. Owner có thể nhờ nhiều người hỗ trợ, nhưng phải là người chịu trách nhiệm cập nhật trạng thái cuối cùng. |
| **Sửa ngọn, không sửa gốc** | Sự cố lặp đi lặp lại nhiều lần trong các sprint tiếp theo. | Sau khi xử lý xong issue, luôn đặt câu hỏi *"Tại sao vấn đề này lại xảy ra?"* bằng 5 Whys và đưa bài học kinh nghiệm vào **Lessons Learned Register**. |

---

## 6. Nguồn tham khảo chất lượng (Blogs, Books & YouTube)

### 1. Chuẩn quốc tế & sách

- *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) - 6th & 7th Edition* (phần *Direct and Manage Project Work* & *Project Work Domain*).
- *Agile Extension to the BABOK® Guide* (quản lý các rào cản trong phát triển sản phẩm).

### 2. Blog chuyên ngành uy tín

- **ProjectManagement.com (PMI Portal):** *How to Maintain an Effective Issue Log*.
- **PM Majik:** Chuỗi hướng dẫn *Issue Management Process & Templates*.
- **Atlassian Blog:** *How to manage blockers and dependencies in Jira*.

### 3. Kênh YouTube tham khảo

- **ProjectManager:** *How to Manage Project Issues - Project Management Training*.
- **Praizion Performance Management:** *Risk Register vs Issue Log - PMP Exam Prep*.
