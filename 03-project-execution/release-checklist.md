# 03-PROJECT-EXECUTION: BÀI 09 - RELEASE CHECKLIST (DANH MỤC KIỂM TRA PHÁT HÀNH)

## 1. KHUNG KIẾN THỨC CHUẨN PMP (PMBOK 6 & 7) & LIÊN HỆ THỰC TẾ

### A. Khái niệm theo chuẩn Quản trị Dự án Quốc tế (PMP)

Phát hành sản phẩm (**Release / Deployment**) là khoảnh khắc chuyển giao thành quả từ môi trường phát triển (Development/Staging) sang môi trường vận hành thực tế (Production) để phục vụ người dùng cuối. Đây là thời điểm rủi ro kỹ thuật và vận hành bị đẩy lên mức cao nhất.

* **PMBOK 6th Edition:**
* Hoạt động này thuộc giao điểm của quy trình **Control Quality** (Kiểm soát chất lượng), **Validate Scope** (Nghiệm thu phạm vi) và quy trình chuyển giao sản phẩm (**Transition Deliverable** trong *Close Project or Phase*).
* Đảm bảo rằng kết quả bàn giao đáp ứng đầy đủ các tiêu chuẩn chất lượng (Quality Metrics), tiêu chí chấp nhận (Acceptance Criteria) và có kế hoạch bàn giao vận hành trơn tru sang cho đội ngũ Operation/Support.


* **PMBOK 7th Edition & DevOps/Agile:**
* Thuộc **Delivery Performance Domain** (Miền hiệu suất bàn giao giá trị) và **Uncertainty Performance Domain**.
* Chuyển dịch từ việc phát hành theo từng khối lớn đầy rủi ro (Big-bang Release) sang phát hành liên tục, an toàn và có kiểm soát thông qua các cổng kiểm soát (**Release Gates**), cờ tính năng (**Feature Flags/Toggles**), và kế hoạch khôi phục khẩn cấp (**Rollback Strategy**).



### B. Liên hệ Thực tế Quản lý Sản phẩm (Product Management)

* **Bản chất:** Release Checklist **không chỉ là bảng danh mục kỹ thuật của riêng đội Lập trình (Dev/DevOps)**.
* **Mục đích cốt lõi đối với Product Team:**
1. **Bảo vệ Hệ thống & Khách hàng:** Đảm bảo phiên bản mới không làm gãy đổ các tính năng đang chạy ổn định cũ (Regression-free).
2. **Đồng bộ hóa 360 độ (Cross-functional Alignment):** Kết nối nhịp nhàng giữa *Kỹ thuật ➔ Thiết kế UI/UX ➔ Vận hành CSKH ➔ Marketing/Sales ➔ Pháp lý/Kế toán*.
3. **Quyết định Dừng/Chạy minh bạch (Go/No-Go Decision):** Cung cấp bộ tiêu chí rõ ràng để PM/PO và Tech Lead quyết định có nên bấm nút Deploy hay tạm dừng khi phát hiện rủi ro.



---

## 2. CẤU TRÚC BỘ CÔNG CỤ & KHUNG FILE RELEASE CHECKLIST (ARTIFACTS)

Một file **Release Checklist** chuẩn mực (quản lý trên Jira Release, Notion, Google Sheets hoặc Confluence) được chia làm 3 giai đoạn then chốt:

### Giai đoạn 1: Pre-Release (Trước khi bấm nút Deploy)

| Hạng mục kiểm tra | Người phụ trách | Trạng thái (`Pass`/`Fail`/`N/A`) | Ghi chú & Bằng chứng |
| --- | --- | --- | --- |
| **Code Freeze & Tagging:** Khóa nhánh code, tạo Git Release Tag (vd: `v2.4.0`). | Tech Lead | `Pass` | Đã khóa nhánh `release/v2.4.0` |
| **QA Regression Sign-off:** 100% test case hồi quy cốt lõi vượt qua trên Staging. | QA Lead | `Pass` | Không còn Bug Blocker/Critical nào mở |
| **Performance & Load Testing:** Kiểm tra tải chịu đựng (Stress test) đạt ngưỡng cam kết. | DevOps | `Pass` | Đạt 5,000 req/s, CPU server < 65% |
| **Database Migration Plan:** Script chuyển đổi dữ liệu, backup CSDL trước giờ G. | DBA / Backend | `Pass` | Đã chạy thử migration trên Staging |
| **Rollback Plan:** Kịch bản lùi về phiên bản cũ nếu gặp sự cố không thể khắc phục. | Tech Lead | `Pass` | Bản build cũ `v2.3.9` đã sẵn sàng |
| **App Store / Google Play Assets:** Screenshots UI mới, Release Notes, Metadata. | PO / UI/UX | `Pass` | Đã chuẩn bị đầy đủ ảnh tỉ lệ chuẩn |
| **Internal Training & CSKH Docs:** FAQ hướng dẫn tính năng mới, kịch bản trả lời khách. | PO / CSKH Lead | `Pass` | Đã đào tạo cho 15 nhân viên CSKH |

### Giai đoạn 2: During Release (Trong quá trình Deploy - Giờ G)

| Hạng mục kiểm tra | Người phụ trách | Trạng thái | Ghi chú |
| --- | --- | --- | --- |
| **Database Backup:** Tạo bản Snapshot CSDL Production ngay trước khi chạy migration. | DevOps | `Pass` | Lưu snapshot AWS RDS `prod-backup-20260818` |
| **Deploy Backend & Services:** Triển khai các API services theo cơ chế Blue/Green hoặc Canary. | DevOps | `Pass` | Lưu lượng traffic chuyển đổi an toàn |
| **Run Migrations:** Chạy script cập nhật schema và dữ liệu mới. | Backend Dev | `Pass` | Thời gian chạy: 45 giây, không lỗi |
| **Smoke Testing (Live Check):** QA kiểm tra nhanh các luồng nghiệp vụ sống còn trên Production. | QA Lead / PO | `Pass` | Đăng ký, Đăng nhập, Đặt phòng, Thanh toán OK |
| **Turn on Feature Flag:** Bật cờ tính năng cho nhóm người dùng nội bộ/Beta trước. | PO / Dev | `Pass` | Đã mở cho 10% User đầu tiên |

### Giai đoạn 3: Post-Release (Sau khi phát hành - 24h - 48h)

| Hạng mục kiểm tra | Người phụ trách | Trạng thái | Ghi chú |
| --- | --- | --- | --- |
| **System Monitoring & APM:** Theo dõi đồ thị lỗi (Crash rate, Sentry error logs, Latency). | DevOps / Tech Lead | `Pass` | Crash-free rate > 99.8%, API Response < 200ms |
| **CSKH Ticket Monitoring:** Theo dõi số lượng khiếu nại, phản ánh từ người dùng. | CSKH Lead | `Pass` | 0 khiếu nại nghiêm trọng về giao dịch |
| **Release Announcement:** Gửi thông báo Push Notification, Email marketing, Post MXH. | Marketing / PO | `Pass` | Bắn push app lúc 10:00 AM |
| **Post-Release Review (Sign-off):** Họp nhanh 10 phút xác nhận đợt Release thành công mỹ mãn. | PO & Tech Lead | `Pass` | Đóng đợt Release `v2.4.0` |

---

## 3. QUY TRÌNH HỌP RA QUYẾT ĐỊNH GO / NO-GO (GO/NO-GO MEETING)

Trước giờ phát hành chính thức 2 đến 4 tiếng, một cuộc họp ngắn (**Go/No-Go Meeting** - 15 phút) bắt buộc phải diễn ra với sự có mặt của: **Product Owner (Chủ tọa), Tech Lead, QA Lead, DevOps Lead, và CSKH Lead**.

```
[Mở đầu: PO tóm tắt phạm vi Release]
               │
               ▼
[Rà soát Pre-Release Checklist từng người]
               │
       ┌───────┴───────┐
       ▼               ▼
[TẤT CẢ ĐỀU PASS]   [CÒN 1 VẤN ĐỀ CRITICAL]
       │               │
       │               ▼
       │         [NO-GO: Tạm hoãn Release]
       │         - Kích hoạt kế hoạch dự phòng
       │         - Thông báo dời lịch cho các bên
       ▼
 [GO: DUYỆT PHÁT HÀNH]
 - DevOps tiến hành Deploy
 - QA trực chiến Smoke Test

```

* **Quy tắc Vàng của Go/No-Go:** Chỉ cần **01 thành viên cốt lõi (QA Lead, Tech Lead hoặc PO) bỏ phiếu NO-GO** do phát hiện rủi ro nghiêm trọng chưa được kiểm soát, đợt Release phải lập tức tạm dừng. Tuyệt đối không release trong sự thỏa hiệp hay phỏng đoán may rủi.

---

## 4. CASE STUDY THỰC TẾ: DỰ ÁN "EPIC CENTER"

* **Bối cảnh:** Phát hành phiên bản lớn **Epic Center v2.0** (Tích hợp tính năng *Smart Check-in mở khóa phòng tự động* và *Cổng thanh toán MoMo nâng cao*). Thời gian dự kiến Deploy: 23:00 tối thứ Ba.
* **Tình huống tại buổi họp Go/No-Go (20:00 tối):**
* Tech Lead & DevOps: Hệ thống Cloud và kịch bản Rollback đã sẵn sàng (`Pass`).
* CSKH Lead: Đội ngũ trực đêm đã nắm rõ tài liệu xử lý sự cố khách không mở được khóa (`Pass`).
* QA Lead giơ cờ vàng: *"Trong đợt Test tải cuối cùng lúc 18:30, khi giả lập 2,000 khách đồng thời bấm mở khóa Bluetooth, có 3% trường hợp API trả về lỗi Timeout 504 và Token xác thực bị treo."*


* **Xử lý tình huống:**
* Nếu là đội ngũ thiếu kinh nghiệm, họ có thể "tặc lưỡi" bấm GO vì nghĩ 3% là tỷ lệ nhỏ và ban đêm ít người dùng.
* Tuy nhiên, căn cứ theo Release Checklist, lỗi liên quan đến cửa phòng khách hàng là **Critical Severity** (nếu xảy ra thực tế, khách sẽ phải đứng ngoài đường ban đêm).
* PO (Duy) và Tech Lead ra quyết định: **NO-GO cho tính năng Smart Check-in**.
* **Giải pháp thích ứng:** Sử dụng **Feature Flag** để tạm tắt tính năng Mở khóa thông minh trên bản v2.0; các tính năng khác (Giao diện UI mới, Thanh toán MoMo) vẫn được bấm **GO** để phát hành đúng hẹn. Đội Backend có thêm 3 ngày để tối ưu lại Pool kết nối Redis cho tính năng Khóa thông minh trước khi bật cờ mở lại.


* **Kết quả:** Đợt Release v2.0 diễn ra an toàn tuyệt đối, không có bất kỳ sự cố khách hàng nào bị kẹt ngoài phòng trong đêm; hệ thống duy trì độ ổn định 99.9%.

---

## 5. CÁC TIPS & ĐIỀU LƯU Ý THỰC CHIẾN (ANTI-PATTERNS & SOLUTIONS)

| Sai lầm phổ biến (Anti-Pattern) | Hậu quả | Giải pháp thực chiến |
| --- | --- | --- |
| **"Friday Release" (Phát hành vào chiều/tối thứ Sáu)** | Hệ thống lỗi vào thứ Bảy/Chủ Nhật; đội Dev kiệt sức trực xuyên cuối tuần, khách hàng bị gián đoạn dịch vụ. | **Luật bất thành văn:** Chỉ Release từ **Thứ Ba đến sáng Thứ Năm**. Tuyệt đối không Release vào chiều Thứ Sáu, cuối tuần hoặc trước kỳ nghỉ Lễ lớn. |
| **Không có Kịch bản Lùi bước (No Rollback Plan)** | Khi xảy ra lỗi nghiêm trọng trên Production, team hoảng loạn sửa code trực tiếp (Hotfix live), dẫn đến "chữa lợn lành thành lợn què". | **Không có Rollback Plan = Không duyệt Release.** Kịch bản khôi phục phiên bản cũ phải được thử nghiệm trước và thời gian Rollback phải < 15 phút. |
| **Quên thông báo đội Vận hành / CSKH** | App đổi luồng giao diện UI, khách hàng gọi lên tổng đài thắc mắc nhưng nhân viên CSKH hoàn toàn không biết gì. | Đội CSKH phải nhận được **Product Release Notes** và tài liệu hướng dẫn (Internal User Guide) trước ngày Release ít nhất **48 giờ**. |
| **Mở tính năng 100% cùng một lúc (All-at-once)** | Lỗi tiềm ẩn lập tức tác động đến toàn bộ hàng trăm nghìn người dùng, gây khủng hoảng truyền thông. | Áp dụng chiến lược **Phát hành theo giai đoạn (Phased Rollout / Canary Release)**: Mở cho 5% ➔ 20% ➔ 50% ➔ 100% trong vòng 3-5 ngày. |

---

## 6. NGUỒN THAM KHẢO CHẤT LƯỢNG (BLOGS, BOOKS & YOUTUBE)

1. **Chuẩn quốc tế & Sách kinh điển:**
* *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) – 6th & 7th Edition* (Phần *Control Quality* & *Delivery Performance Domain*).
* *The DevOps Handbook* – Gene Kim, Jez Humble, Patrick Debois & John Willis (Cuốn sách tiêu chuẩn về quy trình tích hợp và phát hành phần mềm an toàn).
* *Continuous Delivery: Reliable Software Releases through Build, Test, and Deployment Automation* – Jez Humble & David Farley.


2. **Blog chuyên ngành uy tín:**
* **Atlassian DevOps Guides:** *Software Release Management: Best Practices & Checklist*.
* **LaunchDarkly Blog:** *Why Feature Flags are essential for modern Release Management*.
* **GitLab Handbook:** *Release Management and Deployment Strategies*.


3. **Kênh YouTube tham khảo:**
* **Continuous Delivery (Dave Farley):** Video *How to Safely Release Software into Production*.
* **IBM Technology:** Video *What is Blue-Green Deployment? / Canary Deployments Explained*.
* **Agile Academy:** *Release Planning and Definition of Done in Agile*.
