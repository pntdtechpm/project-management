# Project Scope trong giai đoạn Khởi động

## Khung kiến thức: Quan điểm về "Scope" trong giai đoạn Khởi động (Initiation)

Trong quản lý dự án chuẩn PMP, có một sự phân biệt rất rõ ràng về "Phạm vi" giữa hai giai đoạn Khởi động và Lập kế hoạch:

- **Tại giai đoạn Khởi động (Initiation):** Chúng ta **chưa** bóc tách công việc chi tiết, không tạo WBS (Work Breakdown Structure), không viết thẻ Task chi tiết. Thay vào đó, mục tiêu cốt lõi là xác định **Ranh giới dự án (Project Boundaries)**. Việc này nhằm trả lời câu hỏi: *"Chúng ta cam kết làm những gì và quan trọng hơn là chúng ta tuyệt đối không làm những gì?"*. Điều này giúp ngăn chặn tình trạng **Phình to phạm vi (Scope Creep)** ngay từ vạch xuất phát.
- **Phương pháp tiếp cận:** Sử dụng kỹ thuật phân tích sản phẩm (Product Analysis) và phân tích các bên liên quan để đưa ra một danh sách các **Kết quả bàn giao chính (Key Deliverables)** cấp cao nhất.

---

# Tài liệu Phạm vi Dự án cấp cao (High-Level Project Scope)

**Dự án:** Phát triển Nền tảng Kỹ thuật số Tích hợp Dịch vụ Toàn diện & Trợ lý Ảo AI

**Giai đoạn:** 01 Project Initiation (Khởi động dự án)

**Phiên bản:** 1.0

---

## 1. Mô tả Phạm vi Sản phẩm cấp cao (Product Scope Description)

Dự án sẽ tập trung xây dựng một hệ sinh thái công nghệ trọn gói bao gồm 3 cấu phần cốt lõi:

- **Ứng dụng di động (Mobile App):** Phát triển ứng dụng native hoặc cross-platform trên iOS và Android, sở hữu giao diện cao cấp (Luxury style), tối ưu luồng trải nghiệm người dùng (UI/UX) cho các dịch vụ tìm kiếm, đặt phòng/lưu trú, và tích lũy tài chính.
- **Hệ thống Quản trị trung tâm (Back-office CMS):** Cung cấp công cụ quản lý nội dung, duyệt phòng, theo dõi dòng tiền E-Coffer, cấu hình lịch nhắc tự động và hệ thống báo cáo thời gian thực cho nhân viên vận hành.
- **Module Trí tuệ nhân tạo & Tự động hóa (AI & Automation Hub):** Tích hợp mô hình ngôn ngữ lớn (LLM) thông qua API hoặc n8n để tự động hóa khâu tư vấn khách hàng 24/7 và cổng tích hợp eKYC (OCR + Face Matching).

---

## 2. Ranh giới Dự án: Những gì thuộc và không thuộc phạm vi (Project Boundaries)

Để đảm bảo nguồn lực dự án được tập trung tối đa, ranh giới công việc được phân định nghiêm ngặt như sau:

### 2.1. Nằm trong Phạm vi Dự án (In-Scope)

- **Nghiên cứu & Thiết kế:** Khảo sát hành vi người dùng, xây dựng User Persona, thiết kế Wireframe và mẫu UI hoàn chỉnh trên Figma cho cả App và CMS.
- **Phát triển Phần mềm:** Lập trình toàn bộ mã nguồn Frontend (App) và Backend (API, Cơ sở dữ liệu).
- **Tích hợp Hệ thống:** Kết nối thành công cổng thanh toán trực tuyến, API định danh eKYC từ bên thứ ba, và thiết lập luồng tự động hóa hội thoại với mô hình AI.
- **Kiểm thử & Đảm bảo chất lượng (QA/QC):** Thực hiện kiểm thử chức năng, kiểm thử hiệu năng (tải trang, chịu tải hệ thống), và kiểm thử chấp nhận người dùng (UAT).
- **Triển khai & Bàn giao:** Đưa ứng dụng lên App Store/Google Play, cấu hình hạ tầng Cloud (AWS/Google Cloud), đào tạo chuyển giao công nghệ và tài liệu hướng dẫn vận hành cho team nội bộ.

### 2.2. Nằm ngoài Phạm vi Dự án (Out-of-Scope)

- **Nội dung & Dữ liệu:** Dự án này không bao gồm việc trực tiếp đi chụp ảnh, viết bài mô tả hay nhập liệu thủ công hàng nghìn danh sách phòng/hành trình lưu trú lên hệ thống. Team Vận hành/Đối tác sẽ tự thực hiện trên CMS sau khi bàn giao.
- **Hạ tầng Vật lý:** Không bao gồm việc mua sắm, lắp đặt máy chủ vật lý (Data Center) tại văn phòng công ty. Dự án sử dụng 100% hạ tầng điện toán đám mây Cloud thuê ngoài.
- **Pháp lý & Thủ tục:** Không chịu trách nhiệm xin giấy phép hoạt động kinh doanh tài chính cho module E-Coffer hoặc các chứng nhận pháp lý về lưu trú của doanh nghiệp.
- **Tiếp thị thương mại:** Không bao gồm việc lên kế hoạch, chi phí và chạy các chiến dịch Marketing, quảng cáo thu hút người dùng tải app (User Acquisition).

---

## 3. Các Kết quả Bàn giao chính (Key Deliverables)

| STT | Kết quả bàn giao (Deliverables) | Mô tả định dạng / Yêu cầu cốt lõi |
| --- | --- | --- |
| 1 | **Bộ hồ sơ Thiết kế UI/UX** | Link Figma hoàn chỉnh bao gồm: Design System, Prototype tương tác của 40+ màn hình App và 15+ màn hình CMS. |
| 2 | **Tài liệu Kỹ thuật Hệ thống** | Tài liệu Đặc tả Yêu cầu Hệ thống (SRS), Tài liệu kiến trúc phần mềm, và Tài liệu đặc tả API (Swagger). |
| 3 | **Gói mã nguồn & Ứng dụng** | Toàn bộ mã nguồn trên GitHub; Ứng dụng đã được phê duyệt và sẵn sàng tải về trên App Store & Google Play. |
| 4 | **Module AI & eKYC hoạt động** | Hệ thống Chatbot AI chạy thực tế trên môi trường Production; luồng eKYC trả kết quả chính xác. |
| 5 | **Bộ tài liệu Vận hành & Nghiệm thu** | Video/Tài liệu hướng dẫn sử dụng CMS; Biên bản nghiệm thu kỹ thuật (UAT Sign-off) có chữ ký của các bên. |

---

## 4. Tiêu chí Nghiệm thu cấp cao (High-Level Acceptance Criteria)

Sản phẩm của dự án khi bàn giao phải thỏa mãn các tiêu chuẩn chất lượng sau để được ký duyệt:

- **Hiệu năng (Performance):** Tốc độ phản hồi trung bình của API dưới 1.5 giây. Tỷ lệ crash của ứng dụng di động dưới 0.5%.
- **Độ chính xác của AI:** Trợ lý ảo AI nhận diện đúng ý định (Intent) của khách hàng đạt tỷ lệ trên 85% đối với các bộ dữ liệu mẫu đã huấn luyện.
- **Bảo mật (Security):** Toàn bộ dữ liệu cá nhân của khách hàng và dữ liệu eKYC phải được mã hóa (HTTPS, AES-256). Hệ thống vượt qua bài kiểm tra quét lỗ hổng bảo mật cơ bản trước khi Go-live.

---

## 5. Ràng buộc và Giả định về Phạm vi (Scope Constraints & Assumptions)

- **Ràng buộc (Constraints):** Đội ngũ phát triển phải tuân thủ nghiêm ngặt các quy định về bảo mật dữ liệu người dùng theo pháp luật hiện hành. Phạm vi công nghệ phải gói gọn trong các nền tảng đám mây và framework đã thống nhất để đảm bảo tiến độ 6 tháng.
- **Giả định (Assumptions):** Giả định rằng các bên thứ ba cung cấp dịch vụ API (eKYC, Cổng thanh toán, OpenAI/Anthropic API) cung cấp tài liệu kỹ thuật đầy đủ và môi trường Sandbox (thử nghiệm) ổn định ngay trong tháng thứ 2 của dự án.

---

*Tài liệu Phạm vi cấp cao này sẽ là căn cứ trực tiếp để Quản lý Dự án và Đội ngũ thực hiện tiến hành bóc tách thành **Kế hoạch Quản lý Phạm vi (Scope Management Plan)** và **Đường cơ sở phạm vi (Scope Baseline)** ở giai đoạn Lập kế hoạch tiếp theo.*
