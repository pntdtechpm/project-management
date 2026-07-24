# Stakeholder Analysis trong giai đoạn Khởi động

## Khung kiến thức: Kỹ thuật Phân tích Các bên liên quan (Stakeholder Analysis)

Trong quản lý dự án, nếu **Sổ đăng ký các bên liên quan (Stakeholder Register)** giúp chúng ta *liệt kê và nhận diện* "Ai là ai", thì **Phân tích các bên liên quan (Stakeholder Analysis)** là kỹ thuật định lượng và định tính nhằm *đào sâu tâm lý, mức độ ủng hộ và nguy cơ rủi ro* của từng đối tượng để đưa ra chiến lược ứng xử phù hợp.

### 1. Ma trận Đánh giá Mức độ Tham gia (Stakeholder Engagement Assessment Matrix)

PMP định nghĩa 5 mức độ thái độ/hành vi của Stakeholder đối với dự án:

- **Unaware (Chưa biết):** Không biết gì về dự án cũng như tác động tiềm ẩn của nó.
- **Resistant (Kháng cự/Phản đối):** Biết về dự án nhưng phản đối do lo ngại mất lợi ích, tăng khối lượng công việc hoặc sợ thay đổi.
- **Neutral (Trung lập):** Biết về dự án nhưng không ủng hộ cũng không phản đối.
- **Supportive (Ủng hộ):** Biết về dự án và ủng hộ các kết quả đạt được.
- **Leading (Dẫn dắt):** Biết về dự án và chủ động tham gia điều hướng để đảm bảo dự án thành công.

**Mục tiêu của PM:** Xác định vị trí **Hiện tại (C - Current)** và dịch chuyển họ về vị trí **Mong muốn (D - Desired)**.

### 2. Mô hình Nổi bật Salience Model (Ưu tiên hóa Stakeholders)

Để phân tích sâu hơn ngoài ma trận Quyền hạn/Quan tâm, PMP khuyến nghị đánh giá dựa trên 3 yếu tố:

- **Quyền lực (Power):** Mức độ ảnh hưởng đến quyết định của dự án.
- **Tính cấp thiết (Urgency):** Đòi hỏi sự chú ý tức thì hoặc mức độ nhạy cảm về mặt thời gian.
- **Tính hợp pháp (Legitimacy):** Mức độ hợp lý/đúng đắn trong sự tham gia của họ.

---

# Tài liệu Phân tích Các bên liên quan (Stakeholder Analysis)

**Dự án:** Phát triển Nền tảng Kỹ thuật số Tích hợp Dịch vụ Toàn diện & Trợ lý Ảo AI

**Giai đoạn:** 01 Project Initiation

**Phiên bản:** 1.0

---

## 1. Bảng Phân tích Mức độ Tham gia & Chiến lược Tác động

*Ký hiệu: **C** = Mức độ tham gia hiện tại (Current) | **D** = Mức độ tham gia mong muốn (Desired)*

| Bên liên quan (Stakeholder) | Mức độ tham gia (Unaware -> Leading) | Tác động tiềm ẩn & Xung đột lợi ích có thể xảy ra | Chiến lược dịch chuyển & Kế hoạch hành động cụ thể của PM |
| --- | --- | --- | --- |
| **1. Ban Giám đốc (Sponsor)** | **C:** Supportive<br>**D:** **Leading** | Lo ngại dự án bị trễ Go-live làm lỡ cơ hội kinh doanh.<br>Có thể thay đổi ưu tiên chiến lược giữa chừng. | Cung cấp báo cáo Dashboard tóm tắt hàng tuần (KPIs/Milestones).<br>Mời phát biểu chỉ đạo tại phiên Kick-off để công khai cam kết hỗ trợ toàn diện cho dự án. |
| **2. Giám đốc Tài chính (CFO)** | **C:** Neutral<br>**D:** **Supportive** | Lo ngại vượt ngân sách R&D và chi phí API duy trì hàng tháng (Cloud/AI/eKYC).<br>Siết chặt quy trình giải ngân gây chậm tiến độ mua sắm. | Trình bày mô hình ROI & phân tích điểm hòa vốn rõ ràng trong Business Case.<br>Thống nhất trước quy trình duyệt chi nhanh cho các gói hạ tầng dưới 50 triệu VNĐ. |
| **3. Trưởng bộ phận Vận hành & CSKH** | **C:** **Resistant**<br>**D:** **Supportive** | E ngại Trợ lý AI sẽ thay thế nhân sự hoặc quy trình CMS mới phức tạp làm gián đoạn công việc.<br>Ngại phải thay đổi thói quen làm việc cũ. | Làm rõ AI là **công cụ hỗ trợ** giảm tải tác vụ lặp lại, không phải thay thế nhân sự.<br>Mời tham gia thiết kế luồng CMS ngay từ đầu để đảm bảo giao diện thuận tiện nhất cho họ. |
| **4. Kiến trúc sư hệ thống / Tech Lead** | **C:** Supportive<br>**D:** **Leading** | Bị áp lực về mặt thời gian 6 tháng đối với các bài toán kỹ thuật khó (eKYC, AI LLM).<br>Xung đột với bộ phận Phân tích nghiệp vụ về yêu cầu tính năng. | Trao quyền chủ động cho Tech Lead lựa chọn công nghệ/Framework phù hợp.<br>Đảm bảo chốt Scope rõ ràng, chống Scope Creep để bảo vệ team kỹ thuật khỏi quá tải. |
| **5. Chuyên gia UI/UX** | **C:** Supportive<br>**D:** **Supportive** | Muốn tối ưu thẩm mỹ cao cấp (Luxury) nhưng có thể làm tăng độ phức tạp khi Lập trình viên triển khai. | Tổ chức các phiên Review thiết kế sớm (Design Review) giữa UI/UX và Lập trình viên Frontend để cân bằng giữa thẩm mỹ và tính khả thi kỹ thuật. |
| **6. Đơn vị cung cấp API eKYC & Cloud** | **C:** Neutral<br>**D:** **Supportive** | Tốc độ hỗ trợ kỹ thuật chậm nếu gặp sự cố tích hợp API.<br>Rủi ro thay đổi chính sách giá API theo lượng Request. | Đưa các chỉ số cam kết chất lượng dịch vụ (SLA) rõ ràng vào hợp đồng thương mại.<br>Thiết lập nhóm trao đổi kỹ thuật phản ứng nhanh (Slack/Zalo 24/7). |
| **7. Khách hàng / Người dùng cuối** | **C:** Unaware<br>**D:** **Supportive** | Ngại sử dụng app mới nếu quy trình eKYC phức tạp hoặc sợ lộ thông tin cá nhân. | Thiết kế luồng eKYC siêu ngắn gọn (<1 phút), hiển thị rõ các cam kết bảo mật thông tin trên giao diện.<br>Tổ chức thử nghiệm nghiệm thu người dùng (UAT) trên nhóm khách hàng thân thiết. |

---

## 2. Phân tích Các mối Xung đột Lợi ích trọng yếu & Phương án Xử lý (Risk & Conflict Resolution)

```text
[Xung đột 1: Tiến độ vs Chất lượng UX]
Tech Lead (Muốn đơn giản) <---> UI/UX Designer (Muốn tỉ mỉ)
=> Giải pháp: PM ưu tiên phát triển MVP trước, tối ưu hiệu ứng ở bản sau.

[Xung đột 2: Chi phí vs Tính năng]
CFO (Muốn tiết kiệm) <---> Team Vận hành (Muốn mua thêm API xịn)
=> Giải pháp: PM dùng dữ liệu Business Case chứng minh hiệu quả giảm chi phí lâu dài.
```

### Xung đột 1: Team Kỹ thuật (Dev) vs Team Vận hành/Kinh doanh về Yêu cầu tính năng

- **Bản chất:** Team Kinh doanh muốn thêm nhiều tính năng mới, ví dụ tính năng thưởng giới thiệu hoặc báo cáo nâng cao, trong khi Tech Lead muốn giữ phạm vi tối giản để kịp hạn Go-live 6 tháng.
- **Phương án xử lý của PM:** Sử dụng phương pháp phân loại ưu tiên **MoSCoW** (Must have, Should have, Could have, Won't have). Chỉ đưa các tính năng thuộc nhóm *Must have* vào bản Go-live đầu tiên. Các yêu cầu còn lại đưa vào Backlog sản phẩm cho giai đoạn 2.

### Xung đột 2: Bộ phận CSKH e ngại Trợ lý AI (Lo ngại tâm lý & Vận hành)

- **Bản chất:** Nhân viên CSKH lo lắng AI trả lời sai ngữ cảnh gây phàn nàn từ khách hàng cao cấp, hoặc lo ngại nguy cơ giảm biên chế.
- **Phương án xử lý của PM:** Lập cơ chế **Human-in-the-loop (Con người giám sát)**. Trợ lý AI chỉ tự động trả lời các câu hỏi chuẩn hóa (FAQs). Đối với các giao dịch tài chính hoặc phàn nàn phức tạp, AI sẽ tự động chuyển luồng (Escalate) sang cho nhân viên CSKH xử lý kèm theo toàn bộ lịch sử trò chuyện.

---

## 3. Kế hoạch Tương tác Thường niên (Stakeholder Engagement Cadence)

Để duy trì sự đồng thuận xuyên suốt dự án, PM thiết lập tần suất giao tiếp cho từng nhóm đối tượng như sau:

| Nhóm đối tượng | Hình thức tương tác | Tần suất |
| --- | --- | --- |
| **Nhóm Quản lý Cấp cao (Sponsor, CFO)** | Báo cáo quản trị (Dashboard / Executive Summary) & Họp Steering Committee | 1 lần/tháng hoặc ngay khi phát sinh rủi ro cấp độ 1 |
| **Nhóm Thực thi Cốt lõi (Tech Lead, UI/UX, BA)** | Họp kế hoạch Sprint/Daily Standup theo Agile/Hybrid | Hàng ngày 15 phút và hàng tuần review tiến độ |
| **Nhóm Vận hành Nội bộ & Đối tác (Ops Head, Vendors)** | Họp cập nhật tiến độ tích hợp & Demo sản phẩm thử nghiệm | 2 tuần/lần |

---

*Bản Phân tích các bên liên quan này khép lại toàn bộ bộ tài liệu chuẩn cho **Giai đoạn 01 Project Initiation (Khởi động dự án)**. Bạn đã có đủ: Business Case -> Project Vision -> High-Level Scope -> Project Charter -> Stakeholder Register -> Stakeholder Analysis.*
