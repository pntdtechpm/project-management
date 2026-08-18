# 03-PROJECT-EXECUTION: BÀI 08 - DEMO (BUỔI TRÌNH DIỄN SẢN PHẨM & TÍNH NĂNG)

## 1. KHUNG KIẾN THỨC CHUẨN PMP (PMBOK 6 & 7) & LIÊN HỆ THỰC TẾ

### A. Khái niệm theo chuẩn Quản trị Dự án Quốc tế (PMP)

Trong quản trị dự án, việc tạo ra kết quả bàn giao (**Deliverables**) chỉ là một nửa chặng đường; nửa còn lại là chứng minh được kết quả đó đáp ứng đúng kỳ vọng và mang lại giá trị thực tế cho các bên liên quan.

* **PMBOK 6th Edition:**
* Demo là kỹ thuật thanh tra và đánh giá trực quan (**Inspection**) cốt lõi trong quy trình **Validate Scope** (Nghiệm thu phạm vi dự án) và **Control Quality** (Kiểm soát chất lượng).
* Mục tiêu chính: Đưa Deliverables ra trước mắt Khách hàng/Sponsor để đạt được sự chấp thuận chính thức bằng văn bản (**Formal Acceptance**).


* **PMBOK 7th Edition & Agile Practice Guide:**
* Thuộc **Delivery Performance Domain**, **Stakeholder Performance Domain** và **Focus on Value**.
* Trong mô hình Agile/Hybrid, Demo không phải là sự kiện đơn lẻ diễn ra vào cuối dự án mà là chuỗi các buổi trình diễn lặp đi lặp lại (**Iterative Demonstrations**). Demo giúp rút ngắn khoảng cách giữa kỳ vọng trừu tượng trên tài liệu đặc tả và trải nghiệm thực tế của người dùng.



### B. Phân loại các buổi Demo trong Vòng đời Sản phẩm (Product Lifecycle)

Một Product Manager/PO chuyên nghiệp cần phân biệt rõ các loại hình Demo:

1. **Internal Demo / Sprint Demo:** Trình diễn trong nội bộ Scrum Team và các bên liên quan trực tiếp để kiểm tra tính sẵn sàng trước khi Release.
2. **Stakeholder / Executive Demo:** Trình diễn cho Ban điều hành, Nhà đầu tư (Sponsors) – Tập trung vào **Hiệu quả kinh doanh (ROI), Giá trị chiến lược**.
3. **Client / Sales Demo:** Trình diễn cho Khách hàng doanh nghiệp (B2B) hoặc Người dùng thử nghiệm (Beta Users) – Tập trung vào **Giải quyết nỗi đau (Pain points) & Trải nghiệm thực tế**.

---

## 2. CẤU TRÚC BỘ CÔNG CỤ & KHUNG KỊCH BẢN DEMO (ARTIFACTS)

Một buổi Demo thành công cần sự chuẩn bị kỹ lưỡng về mặt công cụ và kịch bản (tránh tình trạng người demo mở máy lên và thao tác ngẫu hứng):

### A. Kịch bản Trình diễn (Demo Script / Storyboard Template)

Khung tài liệu định hình toàn bộ dòng chảy buổi Demo:

| Cột mốc / Bước | Persona (Vai diễn) | Hành động trên màn hình (Action) | Thông điệp cốt lõi (Key Message / Value) | Thời lượng |
| --- | --- | --- | --- | --- |
| **01. Mở đầu (The Hook)** | PO / Presenter | Chiếu màn hình Dashboard rỗng. | Nêu bật nỗi đau: *"Chủ nhà mất 2 tiếng mỗi ngày để cập nhật giá phòng thủ công..."* | 2 phút |
| **02. Luồng chính (Happy Path)** | Chủ nhà (Host) | Thao tác chọn dải ngày ➔ Áp dụng giảm giá 20% ➔ Bấm "Lưu". | Giải pháp: *"Với tính năng Bulk Pricing mới, thao tác này chỉ tốn đúng 10 giây."* | 5 phút |
| **03. Tác động đa kênh (Sync)** | Khách đặt phòng | Mở app Epic Center trên điện thoại ➔ Giá mới hiển thị tức thì. | Giá trị: *"Dữ liệu đồng bộ Real-time, loại bỏ 100% rủi ro lệch giá."* | 3 phút |

### B. Danh mục Kiểm tra Trước Demo (Pre-Demo Checklist)

* **Environment (Môi trường):** Môi trường Demo (Staging/Demo Sandbox) đã được khóa code (Code Freeze), không có ai đang deploy ngầm.
* **Test Data (Dữ liệu thử nghiệm):** Dữ liệu mẫu phải sạch, thực tế và mang tính chuyên nghiệp (Tránh dùng tên test như: `test 123`, `abc xyz`, `ảnh lỗi 404`).
* **Hardware & Setup:** Sạc đầy pin, kiểm tra cáp chuyển đổi màn hình, tắt toàn bộ thông báo cá nhân (Slack, Zalo, Email, Telegram).
* **Backup Plan:** Luôn quay sẵn một video màn hình (**Pre-recorded Demo Video**) chất lượng cao để phòng sự cố mạng hoặc sập server.

---

## 3. QUY TRÌNH THỰC THI DEMO THEO NGHỆ THUẬT STORYTELLING

Một buổi Demo đỉnh cao không bao giờ là buổi "Đọc danh sách tính năng" (Feature dumping), mà là một câu chuyện giải quyết vấn đề gồm 4 bước:

1. **Context & Pain Point (Bối cảnh & Nỗi đau):** Bắt đầu bằng vấn đề thực tế mà người dùng đang gặp phải.
2. **The Hero’s Journey (Hành trình trải nghiệm giải pháp):** Thao tác mượt mà theo góc nhìn của người dùng mục tiêu (Persona). Trình diễn luồng chính mượt mà trước (Happy Path), sau đó mới lồng ghép khéo léo 1-2 trường hợp ngoại lệ (Edge Cases).
3. **The Value & Impact (Giá trị & Tác động):** Nhấn mạnh sản phẩm giúp tiết kiệm bao nhiêu thời gian, tăng bao nhiêu % doanh thu, hoặc giảm bớt bao nhiêu thao tác thừa.
4. **Q&A & Next Steps (Hỏi đáp & Cam kết tiếp theo):** Mở rộng thảo luận, giải đáp thắc mắc và công bố lộ trình bàn giao/phát hành chính thức.

---

## 4. CASE STUDY THỰC TẾ: DỰ ÁN "EPIC CENTER"

* **Bối cảnh:** Buổi Executive Demo tính năng *"Smart Booking & Flash Sale Automation"* cho Ban Giám đốc và các Đối tác vận hành Chuỗi Homestay lớn trước ngày Launching.
* **Sự cố bất ngờ ("The Demo Effect"):** Đúng phút thứ 7 của buổi Demo, mạng Wi-Fi tại văn phòng bất ngờ bị chập chờn, khiến trang thanh toán ví MoMo quay vòng tròn (Loading spinner) và không tải được mã QR thanh toán.
* **Cách PO (Duy) xử lý tình huống chuyên nghiệp:**
* **Bình tĩnh chuyển hướng:** Không cố bấm `F5 (Refresh)` liên tục trong hoang mang, Duy mỉm cười giải thích: *"Hệ thống mạng vừa có độ trễ nhẹ. Để không làm mất thời gian quý báu của các anh/chị, em xin phép chuyển sang bản ghi Demo 4K độ phân giải cao đã được thực hiện trực tiếp trên môi trường Production Sandbox sáng nay."*
* Duy bật ngay tab Video Backup, tua đúng đến đoạn quét mã QR và hoàn tất đơn hàng trong 3 giây.
* Duy tiếp tục dẫn dắt buổi thảo luận sang phần Dashboard báo cáo doanh thu của Chủ nhà.


* **Kết quả:** Hội đồng Giám đốc cực kỳ ấn tượng với sự chuẩn bị chu đáo và khả năng làm chủ tình huống của Product Team. Tính năng nhận được sự phê duyệt 100% (**Formal Sign-off**) để đưa lên App Store/Google Play.

---

## 5. CÁC TIPS & ĐIỀU LƯU Ý THỰC CHIẾN (ANTI-PATTERNS & SOLUTIONS)

| Sai lầm phổ biến (Anti-Pattern) | Hậu quả | Giải pháp thực chiến |
| --- | --- | --- |
| **"Hiệu ứng Demo" (The Demo Effect)** | Hệ thống lăn ra lỗi/sập đúng lúc đang chiếu màn hình cho Sếp hoặc Khách hàng xem. | **Nguyên tắc "Kế hoạch B":** Luôn chuẩn bị sẵn: 1 bộ dữ liệu sơ cua, 1 video quay sẵn màn hình, và phát mạng 4G/5G độc lập từ điện thoại. |
| **Demo kiểu "Liệt kê tính năng" (Feature Dumping)** | Nói quá nhiều về kỹ thuật (API, Database, Microservices) khiến Người nghe buồn ngủ và không hiểu giá trị. | Áp dụng công thức: **"Tính năng này (Feature) ➔ Giúp người dùng làm được gì (Benefit) ➔ Đem lại giá trị kinh doanh gì (Value)"**. |
| **Không chạy thử trước (No Dry Run)** | Người demo thao tác lúng túng, quên mật khẩu test, nhập sai dữ liệu gây lỗi logic. | **Bắt buộc tổ chức Dry Run (Tổng duyệt)** nội bộ trước buổi Demo chính thức ít nhất **3 - 4 giờ**. |
| **Sa đà vào việc sửa Bug tại chỗ** | Khi phát hiện 1 lỗi giao diện nhỏ, Dev/PO dừng buổi demo lại để kiểm tra code khiến thời gian bị trôi hết. | Bình tĩnh ghi nhận lỗi: *"Cảm ơn anh/chị đã phát hiện, em xin ghi nhận trường hợp này vào Bug Log để đội QA xử lý trước khi Release"* và tiếp tục kịch bản. |

---

## 6. NGUỒN THAM KHẢO CHẤT LƯỢNG (BLOGS, BOOKS & YOUTUBE)

1. **Chuẩn quốc tế & Sách kinh điển:**
* *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) – 6th & 7th Edition* (Phần *Validate Scope* & *Delivery Performance Domain*).
* *Demonstrating to Win!* – Robert Riefstahl (Cuốn sách kinh điển về phương pháp trình diễn phần mềm đỉnh cao).
* *Great Demo!* – Peter Cohan (Phương pháp tiếp cận Demo theo giá trị và giải pháp).


2. **Blog chuyên ngành uy tín:**
* **Mind the Product:** *How to deliver killer product demos that engage your stakeholders*.
* **Atlassian Blog:** *The Art of the Sprint Demo: How to showcase your team’s hard work*.
* **Gong.io Research:** *Data-backed tips on what makes a successful software demonstration*.


3. **Kênh YouTube tham khảo:**
* **Y Combinator:** Video *How to Pitch and Demo Your Product*.
* **Agile Academy:** *How to Deliver an Awesome Sprint Demo*.
* **Lenny's Podcast / Dan Martell:** *How to Demo Software Like a Pro*.



