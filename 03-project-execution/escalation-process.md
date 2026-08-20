# 03-PROJECT-EXECUTION: BÀI 10 - ESCALATION PROCESS (QUY TRÌNH LEO THANG & GIẢI QUYẾT XUNG ĐỘT)

## 1. KHUNG KIẾN THỨC CHUẨN PMP (PMBOK 6 & 7) & LIÊN HỆ THỰC TẾ

### A. Khái niệm theo chuẩn Quản trị Dự án Quốc tế (PMP)

Trong quá trình thực thi dự án (**Project Execution**), không phải rào cản hay xung đột nào cũng có thể tự giải quyết ở cấp độ Đội ngũ phát triển (Project Team). Khi một vấn đề vượt quá thẩm quyền hạn định hoặc ảnh hưởng nghiêm trọng tới các Đường cơ sở (Scope, Schedule, Cost), dự án cần một cơ chế chính thức để chuyển giao cấp độ xử lý. Đó là **Escalation Process** (Quy trình leo thang).

* **PMBOK 6th Edition:**
* Gắn liền mật thiết với quy trình **Manage Communications**, **Manage Stakeholder Engagement** và **Project Governance** (Quản trị dự án).
* Quy định rõ ràng các cấp bậc quyền hạn (Levels of Authority) và ranh giới chấp nhận sai lệch (**Tolerance / Thresholds**). Khi các chỉ số trễ hạn hoặc vượt chi phí chạm ngưỡng Thresholds, PM có trách nhiệm kích hoạt cơ chế leo thang lên Ban chỉ đạo dự án (Project Steering Committee / Sponsor).


* **PMBOK 7th Edition & Agile:**
* Thuộc **Project Team Performance Domain**, **Stakeholder Performance Domain** và **Uncertainty Performance Domain**.
* Chuyển hóa tư duy giải quyết xung đột (**Conflict Management**): Leo thang không phải là hành vi "méc sếp" hay thoái thác trách nhiệm, mà là một công cụ cộng tác văn minh nhằm đảm bảo **tính minh bạch (Transparency)** và nhận được sự hỗ trợ tài nguyên kịp thời từ lãnh đạo cấp cao.



### B. Liên hệ Thực tế Quản lý Sản phẩm (Product Management)

* **Bản chất:** Escalation Process là chiếc "phanh an toàn" ngăn chặn tình trạng team giấu lỗi, ôm đồm vấn đề quá lâu dẫn đến việc dự án sụp đổ bất ngờ vào phút chót.
* **Mục đích cốt lõi đối với Product Team:**
1. **Bảo vệ Thời gian & Năng lượng của Team:** Tránh việc team tốn hàng tuần tranh cãi bế tắc về quyền lợi hoặc kỹ thuật vượt quá quyền hạn nội bộ.
2. **Xác lập Kênh Phản Ứng Nhanh (Fast-track Resolution):** Có quy chuẩn rõ ràng về thời gian phản hồi (SLA) của cấp quản lý đối với các sự cố khẩn cấp.
3. **Hạ nhiệt xung đột liên phòng ban (Cross-functional Conflicts):** Cung cấp trọng tài khách quan để giải quyết bất đồng giữa Đội Kỹ thuật, Đội Vận hành (Ops), Marketing và Đối tác thứ ba.



---

## 2. CẤU TRÚC BỘ CÔNG CỤ & MA TRẬN LEO THANG (ESCALATION MATRIX)

Một **Ma trận Leo thang (Escalation Matrix)** chuẩn mực định nghĩa rõ 4 cấp độ xử lý, điều kiện kích hoạt, vai trò chịu trách nhiệm và cam kết thời gian phản hồi (SLA):

| Cấp độ (Level) | Điều kiện kích hoạt (Trigger Criteria) | Người chịu trách nhiệm xử lý (Owner) | Thời gian phản hồi tối đa (SLA) | Kênh trao đổi (Channel) |
| --- | --- | --- | --- | --- |
| **Level 1 (Team Level)** | • Vấn đề logic code, xung đột UI/UX nội bộ.<br>

<br>• Bug nhỏ không ảnh hưởng tiến độ Sprint.<br>

<br>• Blocker tự giải quyết được trong ngày. | **Dev, QA, UI/UX Designer, Scrum Master** | **Trong vòng 4 giờ** | Daily Standup, Slack/Teams channel nội bộ. |
| **Level 2 (Lead / PM Level)** | • Chậm tiến độ User Story > 2 ngày.<br>

<br>• Xung đột scope giữa PO và Stakeholder.<br>

<br>• Vendor/Đối tác API phản hồi chậm trễ. | **Product Owner (PO), Technical Lead, Project Manager (PM)** | **Trong vòng 12 - 24 giờ** | Họp giải quyết Issue, cập nhật Issue Log, Jira Ticket. |
| **Level 3 (Department / Head Level)** | • Nhà cung cấp (Third-party) vi phạm SLA hoặc ngắt kết nối hệ thống.<br>

<br>• Xung đột phân bổ nhân sự chủ chốt giữa các dự án.<br>

<br>• Dự báo trễ tiến độ toàn bộ Sprint > 30%. | **Head of Product, CTO, Engineering Manager** | **Trong vòng 24 - 48 giờ** | Email Escalation chính thức, cuộc họp khẩn cấp (Ad-hoc meeting). |
| **Level 4 (Executive / Sponsor Level)** | • Tranh chấp hợp đồng/pháp lý có nguy cơ kiện tụng.<br>

<br>• Vượt ngân sách dự án (Cost overrun) > 15%.<br>

<br>• Sự cố rò rỉ dữ liệu bảo mật (Data breach), khủng hoảng truyền thông. | **C-Level (CEO, COO, CFO), Project Sponsor, Hội đồng Quản trị** | **Trong vòng 2 - 4 giờ (Khẩn cấp)** | Cuộc họp Ban điều hành, Hotline khẩn cấp, Thông cáo chính thức. |

---

## 3. NGUYÊN TẮC VÀNG KHI LEO THANG: "ĐỪNG CHỈ MANG ĐẾN VẤN ĐỀ, HÃY MANG THEO PHƯƠNG ÁN"

Một sai lầm kinh điển của các kỹ sư và quản lý trẻ là biến Escalation thành hành vi "ném bom thư" cho sếp. Một thông điệp leo thang chuyên nghiệp bắt buộc phải áp dụng cấu trúc **SCQA** hoặc **Mô hình 3 Điểm (3-Point Escalation Message)**:

```markdown
🚨 [ESCALATION - MỨC ĐỘ 2] - Chậm trễ Tích hợp API Cổng Thanh toán MoMo

1. BỐI CẢNH & HIỆN TRẠNG (The Problem & Impact):
- Đối tác MoMo đã quá hạn bàn giao API Production 3 ngày (Hạn chót là 15/03).
- Tác động: Nếu không có API trước ngày 18/03, toàn bộ tính năng Đặt phòng sẽ bị hoãn Release.

2. CÁC NỖ LỰC ĐÃ THỰC HIỆN (Actions Taken):
- PO và Tech Lead đã liên hệ qua kênh Zalo Support và gửi 02 email nhắc nhở nhưng chỉ nhận được câu trả lời chung chung từ Support cấp 1.

3. ĐỀ XUẤT PHƯƠNG ÁN XỬ LÝ (Proposed Solutions):
- Phương án A (Ưu tiên): Nhờ Head of Partnership can thiệp trực tiếp với Giám đốc Đối tác của MoMo trong sáng nay để cấp quyền truy cập ngay.
- Phương án B (Dự phòng): Tạm thời phát hành phiên bản chỉ dùng Chuyển khoản QR Ngân hàng (VietQR) và lùi MoMo lại 1 tuần.

```

---

## 4. CASE STUDY THỰC TẾ: DỰ ÁN "EPIC CENTER"

* **Bối cảnh:** Trước ngày Release phiên bản v2.0 của Epic Center 5 ngày, công ty bảo mật bên ngoài thực hiện đợt đánh giá ATTT (Penetration Testing) và bất ngờ gắn cờ đỏ (`Flag: Critical Vulnerability`): Phát hiện lỗ hổng có thể bị khai thác lộ số CCCD của Chủ nhà.
* **Xung đột nội bộ phát sinh:**
* Đội Dev & Tech Lead cho rằng: *"Lỗ hổng này chỉ xảy ra trên lý thuyết khi hacker có quyền Admin hệ thống, không đáng để hoãn ngày Launching"*.
* Đội An toàn thông tin (Security Lead) kiên quyết: *"Nếu không vá lỗi này, chúng tôi sẽ từ chối ký biên bản nghiệm thu bảo mật"*.
* Hai bên tranh cãi gay gắt suốt 24 giờ, buổi họp kỹ thuật đi vào ngõ cụt.


* **Kích hoạt Quy trình Leo thang (Escalation to Level 3 - CTO & Head of Product):**
* PO (Duy) không để cuộc tranh cãi tiếp diễn làm tiêu hao năng lượng của team. Duy lập tức kích hoạt phiếu **Escalation Level 3** triệu tập cuộc họp ngắn 30 phút giữa CTO, Security Lead, Tech Lead và Duy.
* **Tại cuộc họp:** Duy trình bày rõ rủi ro kinh doanh (nếu rò rỉ dữ liệu sẽ bị phạt hành chính và mất uy tín thương hiệu) song hành cùng phương án kỹ thuật.
* **Quyết định từ CTO:**
1. Yêu cầu Tech Lead dừng toàn bộ các Task phụ, tập trung 2 Senior Dev giỏi nhất viết bản vá (Patch) cho lỗ hổng bảo mật trong vòng 24 giờ.
2. Đội Security cam kết Test lại ngay trong đêm khi nhận được bản vá.
3. Giữ nguyên mốc Launching của Epic Center.




* **Kết quả:** Xung đột được dập tắt nhanh gọn nhờ sự can thiệp của cấp có thẩm quyền; bản vá hoàn tất trong 18 giờ và sản phẩm được phê duyệt ATTT tuyệt đối trước ngày ra mắt.

---

## 5. CÁC TIPS & ĐIỀU LƯU Ý THỰC CHIẾN (ANTI-PATTERNS & SOLUTIONS)

| Sai lầm phổ biến (Anti-Pattern) | Hậu quả | Giải pháp thực chiến |
| --- | --- | --- |
| **"Hội chứng Cậu bé chăn cừu" (Crying Wolf)** | Mọi chuyện nhỏ nhặt đều leo thang lên Sếp/Sponsor, làm loãng tính nghiêm trọng của các vấn đề sống còn thực sự. | Tuân thủ nghiêm ngặt **Điều kiện kích hoạt (Triggers)** của Ma trận Leo thang. Chỉ leo thang khi đã cạn kiệt giải pháp ở cấp hiện tại. |
| **"Giấu rác dưới thảm" (Sweeping under the rug)** | Sợ bị đánh giá năng lực nên giấu lỗi, đến khi sát deadline vỡ trận thì không ai cứu kịp. | Xây dựng văn hóa **"Phát hiện lỗi sớm là dũng cảm"**. Đặt quy tắc: *"Nếu một Issue bị kẹt > 48h mà không tiến triển, bắt buộc phải leo thang lên cấp trên"*. |
| **"Vượt cấp bừa bãi" (Skipping Levels)** | Nhân viên Dev nhảy cóc qua PM/Tech Lead để phàn nàn thẳng với CEO, gây hỗn loạn cấu trúc quản trị. | Thiết lập quy định: Mọi Escalation phải đi tuần tự theo từng tầng bậc (L1 ➔ L2 ➔ L3 ➔ L4), trừ các sự cố thảm họa cấp bách được quy định sẵn. |
| **Leo thang cảm tính, không có số liệu** | Đưa ra các câu phàn nàn chung chung (*"Bên A làm việc chán lắm", "Team kia không hợp tác"*), làm gia tăng xung đột cá nhân. | Bắt buộc phải có **Dữ liệu & Bằng chứng cụ thể** (Số ngày trễ hạn, log tin nhắn, email cảnh báo, bảng phân tích tác động tài chính). |

---

## 6. NGUỒN THAM KHẢO CHẤT LƯỢNG (BLOGS, BOOKS & YOUTUBE)

1. **Chuẩn quốc tế & Sách kinh điển:**
* *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) – 6th & 7th Edition* (Phần *Manage Stakeholder Engagement* & *Conflict Management*).
* *Crucial Conversations: Tools for Talking When Stakes Are High* – Kerry Patterson, Joseph Grenny, Ron McMillan & Al Switzler (Nghệ thuật giao tiếp trong những tình huống rủi ro cao).
* *Coaching Agile Teams* – Lyssa Adkins (Chương về *Navigating Conflict - 5 Levels of Conflict in Agile*).


2. **Blog chuyên ngành uy tín:**
* **ProjectManagement.com (PMI Portal):** *Designing an Effective Project Escalation Path*.
* **Mind the Product:** *Managing Conflict and Alignment Across Cross-functional Product Teams*.
* **Harvard Business Review (HBR):** *How to Escalate a Problem to Your Boss (Without Sounding Like a Whiner)*.


3. **Kênh YouTube tham khảo:**
* **Harvard Business Review:** Video *How to Resolve Conflict at Work*.
* **Praizion Performance Management:** Video *Conflict Resolution Techniques for PMP Exam*.
* **Agile Academy:** *Managing Team Conflicts in Agile Projects*.



---