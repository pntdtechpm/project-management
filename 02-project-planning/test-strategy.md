# 02-PROJECT-PLANNING: BÀI 11 - TEST STRATEGY (CHIẾN LƯỢC KIỂM THỬ)

**Tên tài liệu:** `02-project-planning/test-strategy.md`  
**Chủ đề:** Chiến lược Kiểm thử Dự án (Project Test Strategy) trong mô hình Agile/Hybrid và PMP  
**Đối tượng hướng tới:** Project Manager (PM), QA Lead / Test Manager, Product Owner (PO), Technical Lead và đội ngũ kiểm thử.

---

## I. Khung kiến thức chuẩn PMP (PMBOK® Guide - 6th Edition) & Agile

### 1. Định nghĩa & bản chất của Test Strategy

Theo chuẩn PMP trong *PMBOK® Guide - 6th Edition*, đặc biệt các quy trình **8.1 Plan Quality Management** và **8.2 Manage Quality**, **Test Strategy (Chiến lược Kiểm thử)** là tài liệu trục dọc, định hình phương pháp luận cấp cao để kiểm tra và đánh giá xem các sản phẩm bàn giao (Deliverables) có đạt tiêu chuẩn chất lượng và đáp ứng đúng kỳ vọng nghiệp vụ hay không.

**Sự khác biệt giữa Test Strategy và Test Plan:**

- **Test Strategy (Chiến lược):** Tài liệu mang tính **dài hạn và tổng quan**, xác định cách tiếp cận (Approach), tiêu chuẩn (Standards), các cấp độ kiểm thử (Test Levels), loại kiểm thử, công cụ và nguyên tắc áp dụng cho toàn bộ dự án hoặc tổ chức. Thường do QA Lead hoặc Test Manager xây dựng.
- **Test Plan (Kế hoạch):** Tài liệu mang tính **thực thi ngắn hạn**, phân bổ chi tiết ai test cái gì, lịch trình test khi nào, môi trường nào, dữ liệu nào và danh sách test cases cụ thể cho từng Sprint hoặc Release.

Nói ngắn gọn, Test Strategy trả lời câu hỏi "dự án sẽ kiểm thử theo triết lý và cấu trúc nào", còn Test Plan trả lời câu hỏi "đợt này kiểm thử những gì, bởi ai, vào lúc nào".

### 2. Kim tự tháp kiểm thử trong Agile/Hybrid

Trong phát triển phần mềm hiện đại, Test Strategy cần định hình cấu trúc kiểm thử theo mô hình **Testing Pyramid (Kim tự tháp Kiểm thử)** để tối ưu chi phí, tăng tốc phản hồi và phát hiện lỗi sớm (Shift-left Testing).

- **Unit Test (Kiểm thử đơn vị - đáy kim tự tháp):** Chiếm tỷ trọng lớn nhất, thường >= 70%. Developer tự viết code để test từng hàm, class hoặc module nhỏ. Chi phí rẻ, chạy tự động nhanh và phù hợp để phát hiện lỗi logic sớm.
- **Integration Test (Kiểm thử tích hợp - tầng giữa):** Chiếm khoảng 20%. Kiểm tra sự tương tác giữa các module độc lập, ví dụ API kết nối giữa eKYC Core, Backend App và webhook ngân hàng.
- **UI / End-to-End Test (Kiểm thử giao diện/toàn trình - đỉnh kim tự tháp):** Chiếm tỷ trọng nhỏ nhất, khoảng 10%. Giả lập hành vi thực tế của người dùng từ đầu đến cuối luồng. Loại test này có giá trị cao nhưng chi phí vận hành lớn, chạy chậm và dễ flaky nếu lạm dụng.

Một Test Strategy tốt không dồn toàn bộ trách nhiệm kiểm thử về cuối dự án. Nó phân bổ kiểm thử theo tầng, để lỗi rẻ được phát hiện ở tầng thấp trước khi trở thành lỗi đắt ở tầng UI/UAT.

### 3. Quy trình quản lý lỗi (Defect Lifecycle) chuẩn PMP

Một cấu phần bắt buộc trong Test Strategy là định nghĩa cách phân loại và xử lý vòng đời của lỗi (Defect/Bug).

**Mức độ nghiêm trọng (Severity):**

- **Critical:** Sập hệ thống, lộ dữ liệu, sai lệch tiền, mất khả năng giao dịch hoặc vi phạm bảo mật nghiêm trọng.
- **High:** Lỗi tính năng chính, không có giải pháp thay thế hợp lý, ảnh hưởng trực tiếp đến luồng nghiệp vụ quan trọng.
- **Medium:** Lỗi tính năng phụ hoặc có giải pháp thay thế tạm thời.
- **Low:** Lỗi giao diện, chính tả, căn chỉnh hoặc vấn đề nhỏ không ảnh hưởng nghiệp vụ chính.

**Luồng xử lý lỗi chuẩn:**

```text
New -> Assigned -> Fixed -> Verified -> Closed
```

Trong thực tế, có thể bổ sung các trạng thái như `Rejected`, `Duplicate`, `Cannot Reproduce`, `Deferred` hoặc `Reopened`, nhưng team cần thống nhất định nghĩa trước để tránh tranh cãi khi đo defect metrics.

---

## II. Ví dụ & minh họa thực tế

### Ví dụ: Thiết lập Test Strategy cho Dự án "Epic Center"

Dự án áp dụng cho Module eKYC và thanh toán VietQR.

### 1. Các cấp độ kiểm thử áp dụng (Test Levels)

- **Component / Unit Testing:** Bắt buộc 100% API xử lý tính toán dòng tiền của ví E-Coffer phải pass unit test trước khi tạo Pull Request.
- **API / Integration Testing:** QA dùng Postman/Newman để test tự động toàn bộ kịch bản kết nối webhook ngân hàng, gồm thanh toán thành công, sai số tiền, sai chữ ký bảo mật checksum, duplicate callback và timeout.
- **System Testing (E2E):** Test toàn trình luồng: tải app -> quét CCCD eKYC thành công -> nạp tiền ví E-Coffer -> quét mã VietQR đặt phòng.
- **User Acceptance Testing (UAT):** Khối vận hành và khách hàng thử nghiệm Alpha/Beta để ký biên bản nghiệm thu (Sign-off).

### 2. Tiêu chí bắt đầu và kết thúc kiểm thử (Entry & Exit Criteria)

| Tiêu chí | Điều kiện bắt buộc |
| --- | --- |
| **Entry Criteria** | 1. Môi trường Staging/Testing đã cấu hình xong, data test đã được chuẩn bị đầy đủ.<br>2. Code đã qua code review và pass >= 80% unit test coverage theo scope đã thống nhất.<br>3. Tài liệu đặc tả tính năng, SRS hoặc User Stories đã chốt acceptance criteria.<br>4. Build được deploy thành công và không có lỗi blocker ở smoke test. |
| **Exit Criteria** | 1. 100% test cases ưu tiên cao (Must-have) đã được thực hiện.<br>2. Tỷ lệ pass test cases >= 95%.<br>3. Không còn lỗi Critical và High chưa được sửa hoặc chưa có waiver được phê duyệt.<br>4. Báo cáo kiểm thử (Test Report) được QA Lead ký duyệt.<br>5. Các lỗi còn lại đã được phân loại, có owner và kế hoạch xử lý sau release nếu được chấp nhận. |

### 3. Ma trận truy vết yêu cầu kiểm thử (Traceability Matrix mẫu)

| User Story / Requirement | Test Case chính | Loại kiểm thử | Trạng thái |
| --- | --- | --- | --- |
| **US-01:** Người dùng quét CCCD để eKYC | TC-EKYC-001: OCR CCCD hợp lệ | Functional / OCR Accuracy | Pass |
| **US-02:** Người dùng xác thực khuôn mặt | TC-EKYC-014: Face matching đúng chủ tài khoản | Security / Biometric | Pass |
| **US-03:** Người dùng nạp tiền qua VietQR | TC-PAY-006: Webhook thanh toán thành công | Integration / API | Pass |
| **US-04:** Hệ thống xử lý callback trùng lặp | TC-PAY-011: Duplicate IPN callback | Integration / Idempotency | In Progress |
| **NFR-01:** API chịu tải 2,000 user đồng thời | TC-PERF-003: Load test checkout/payment | Performance | Pending |

---

## III. Case study dẫn chứng thực tế

### Hội chứng "Ice Cream Cone Anti-pattern" và cái kết đắng của dự án eKYC

**Bối cảnh:** Một dự án làm eKYC cho chuỗi căn hộ dịch vụ. QA Lead xây dựng một Test Strategy sai lầm: bỏ qua unit test vì cho rằng "tốn thời gian của Dev", giảm thiểu integration test và dồn 90% nguồn lực vào manual UI testing ở cuối dự án. Mô hình kim tự tháp bị đảo ngược thành "ice cream cone".

**Vấn đề phát sinh:**

1. Đến giai đoạn sát Go-live, khi QA Tester thực hiện test trên giao diện App, họ phát hiện hàng loạt lỗi logic: hệ thống nhận diện sai khuôn mặt, ví tính toán sai số dư cọc.
2. Do lỗi nằm sâu ở tầng Core Backend nhưng lại phát hiện ở tầng UI, Dev Team phải mất hàng tuần để truy vết nguyên nhân gốc rễ (Root Cause).
3. Dự án bị vỡ tiến độ, chậm 2 tháng, chi phí sửa bug tăng mạnh so với việc phát hiện sớm bằng unit test và integration test.

**Bài học rút ra:**

1. Test Strategy phải giữ vững mô hình Testing Pyramid, với tầng unit và integration test đủ mạnh.
2. Lỗi phát hiện càng muộn, chi phí sửa đổi càng tăng theo cấp số nhân.
3. PM/PO không nên xem unit test là "việc kỹ thuật tùy chọn"; đây là quality gate giúp bảo vệ tiến độ release.
4. Kiểm thử tự động cần được tích hợp vào CI/CD pipeline để feedback đến team ngay sau mỗi thay đổi.

---

## IV. Tips & điều lưu ý thực chiến cho PM/PO

### 1. Non-functional Testing là bắt buộc với dữ liệu cá nhân và tài chính

Với các dự án chứa thông tin cá nhân như CCCD và dữ liệu tài chính như ví điện tử, Test Strategy bắt buộc phải có:

- **Security Testing:** Quét lỗ hổng OWASP, kiểm tra phân quyền, mã hóa dữ liệu, bảo vệ token/session và kiểm thử rò rỉ dữ liệu.
- **Performance / Load Testing:** Giả lập tải cao khi hàng nghìn khách cùng đặt phòng hoặc thanh toán vào khung giờ cao điểm.
- **Reliability Testing:** Kiểm tra retry, timeout, idempotency và recovery khi vendor API hoặc ngân hàng phản hồi chậm.

### 2. Quản lý Test Data là điểm nghẽn cần xử lý sớm

Test Data Management là điểm nghẽn của nhiều dự án. QA thường không có đủ dữ liệu sạch để test hoặc không được phép dùng dữ liệu thật vì lý do bảo mật. PM cần có kế hoạch:

- Tạo mock data đủ bao phủ happy path và edge cases
- Ẩn danh dữ liệu thật bằng data masking nếu cần dùng dữ liệu Production
- Quản lý dữ liệu test cho CCCD, tài khoản, giao dịch, lỗi checksum và timeout
- Làm sạch dữ liệu sau test để tránh ảnh hưởng các vòng kiểm thử tiếp theo

### 3. Dùng Traceability Matrix để tránh bỏ sót kiểm thử

Mỗi User Story hoặc Requirement quan trọng phải tương ứng với ít nhất một Test Case. Traceability Matrix giúp PM/QA Lead trả lời nhanh:

- Requirement nào đã có test case?
- Test case nào đang fail?
- Tính năng nào chưa được test trước release?
- Nếu requirement thay đổi, test case nào cần cập nhật?

### 4. Định nghĩa rõ tiêu chí waiver khi còn lỗi

Trong thực tế, không phải release nào cũng sạch 100% bug. Test Strategy nên quy định rõ lỗi nào được phép waiver, ai có quyền phê duyệt và cần ghi nhận rủi ro gì. Lỗi Critical liên quan đến tiền, dữ liệu cá nhân hoặc bảo mật không nên được waiver.

---

## V. Template Test Strategy nên dùng

| Trường thông tin | Nội dung cần có |
| --- | --- |
| Test Objectives | Mục tiêu kiểm thử và tiêu chuẩn chất lượng cần chứng minh |
| Scope of Testing | Phạm vi kiểm thử và phạm vi không kiểm thử |
| Test Levels | Unit, integration, system, E2E, UAT |
| Test Types | Functional, regression, performance, security, usability, compatibility |
| Testing Pyramid | Tỷ trọng unit/integration/E2E và nguyên tắc automation |
| Entry Criteria | Điều kiện để bắt đầu kiểm thử |
| Exit Criteria | Điều kiện để dừng kiểm thử hoặc đề xuất release |
| Test Environment | Staging, test data, accounts, vendor sandbox, monitoring |
| Test Data Management | Mock data, masking, refresh, cleanup |
| Defect Lifecycle | New, assigned, fixed, verified, closed, reopened |
| Severity / Priority Rules | Cách phân loại lỗi và SLA xử lý |
| Traceability Matrix | Mapping requirement -> test case -> result |
| Tools | Jira, TestRail, Zephyr, Postman/Newman, JMeter, Cypress, Playwright |
| Reporting | Test report, defect trend, coverage, pass rate |
| Roles & Responsibilities | QA Lead, Tester, Dev, Tech Lead, PO, PM |

---

## VI. Tài liệu & nguồn tham khảo

### 1. Chuẩn quốc tế & sách gối đầu giường

- *International Software Testing Qualifications Board (ISTQB) - Certified Tester Foundation Level (CTFL) Syllabus*.
- *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) - 6th Edition*, Section 8.3: Control Quality.

### 2. Blog chuyên ngành uy tín

- Ministry of Testing: *Modern Software Testing Strategies*.
- Atlassian Agile Coach: *Different Types of Testing in Agile Frameworks*.

### 3. Video / YouTube hữu ích

- Search keyword: *"Software Testing Pyramid Explained - Unit vs Integration vs E2E"*.
- Search keyword: *"How to write an effective Test Strategy Document"*.
