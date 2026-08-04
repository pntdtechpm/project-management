# 03-PROJECT-EXECUTION: BÀI 03 - DECISION LOG (NHẬT KÝ QUYẾT ĐỊNH DỰ ÁN)

## 1. Khung kiến thức chuẩn PMP (PMBOK 6 & 7) & liên hệ thực tế

### A. Khái niệm theo chuẩn quản trị dự án quốc tế (PMP)

Trong suốt giai đoạn thực thi dự án (**Project Execution**), hàng trăm quyết định từ chiến lược đến kỹ thuật được đưa ra mỗi tuần. Bối cảnh dự án biến động liên tục khiến các quyết định nếu không được ghi vết sẽ dễ bị lãng quên hoặc tranh cãi lại.

**PMBOK 6th Edition:**

- Decision Log là một tài liệu lưu trữ thuộc **Project Documents**, đóng vai trò là cơ sở để duy trì tính nhất quán trong các quy trình **Direct and Manage Project Work** và **Manage Project Knowledge**.
- Decision Log giúp bảo đảm tri thức dự án (**Project Knowledge**) được tích lũy, không bị mất đi khi có thay đổi về nhân sự hoặc stakeholder.

**PMBOK 7th Edition & Agile:**

- Thuộc **Stakeholder Performance Domain**, **Project Work Performance Domain** và **Tailoring**.
- Trong môi trường Agile/Hybrid, việc ra quyết định mang tính phân tán (**Decentralized Decision Making**). Decision Log giúp tạo ra sự minh bạch (**Transparency**), tránh hội chứng "mất trí nhớ tổ chức" (**Organizational Amnesia**) - tình trạng đội ngũ quên mất lý do tại sao lại chọn một phương án kỹ thuật hoặc tính năng ở quá khứ.

### B. Liên hệ thực tế quản lý sản phẩm (Product Management)

**Tầm quan trọng:** Dự án kéo dài nhiều tháng, định hướng tính năng (Feature Scope), kiến trúc hạ tầng (System Architecture) hay giao diện UI/UX thường xuyên phải thay đổi theo phản hồi thị trường.

**Mục đích cốt lõi của Decision Log:**

1. **Chặn đứng việc tranh luận lặp lại:** Tránh việc team tốn hàng giờ họp hành chỉ để tranh cãi lại một vấn đề đã chốt từ 2 tháng trước.
2. **Bảo vệ đội ngũ & quá trình ra quyết định:** Minh bạch hóa bối cảnh, dữ liệu và giả định tại thời điểm ra quyết định để tránh việc đổ lỗi khi tình hình thay đổi.
3. **Onboarding nhân sự mới mượt mà:** Nhân sự mới vào team chỉ cần đọc Decision Log là hiểu rõ lịch sử tiến hóa của sản phẩm.

---

## 2. Cấu trúc bộ công cụ & khung file Decision Log (Artifacts)

Một file **Decision Log** chuẩn, dù đặt trên Confluence, Notion, Google Sheets hoặc Coda, nên có cấu trúc như bảng dưới đây:

| Trường thông tin | Ý nghĩa & mô tả | Ví dụ thực tế |
| --- | --- | --- |
| **Decision ID** | Mã định danh duy nhất của quyết định. | `DEC-015` |
| **Title / Topic** | Tiêu đề tóm tắt quyết định ngắn gọn. | *Lựa chọn cơ sở dữ liệu cho module Chat thời gian thực* |
| **Date & Decision Maker** | Ngày chốt và người chịu trách nhiệm quyết định chính (Approver). | `20/03/2026` - *Duy (Product Owner)* |
| **Key Stakeholders** | Những người tham gia thảo luận hoặc đóng góp ý kiến. | *Tấn (Tech Lead), QA Lead, UI/UX Designer* |
| **Context & Problem** | Bối cảnh và lý do tại sao cần ra quyết định này. | *Tính năng Chat CSKH cần xử lý 10,000 kết nối đồng thời. CSDL MySQL hiện tại bị nghẽn I/O.* |
| **Options Considered** | Danh sách phương án được cân nhắc, kèm ưu/nhược điểm và chi phí. | **Option A:** Tối ưu MySQL cũ - rẻ, nhưng trần hiệu năng thấp. **Option B:** Dùng Redis + MongoDB - nhanh, linh hoạt, tốn thêm chi phí AWS. |
| **Final Decision & Rationale** | Quyết định cuối cùng và lý do cốt lõi lựa chọn. | **Chọn Option B.** Lý do: đáp ứng tốc độ phản hồi dưới 100ms và khả năng mở rộng trong 2 năm tới. |
| **Impact / Trade-offs** | Tác động đến ngân sách, tiến độ, kỹ thuật hoặc tái cấu trúc. | Tăng `200 USD / tháng` chi phí Cloud AWS; đội Dev tốn thêm 3 ngày để config cluster. |
| **Status** | Trạng thái quyết định. | `Proposed`, `Approved`, `Superseded` |

---

## 3. Quy trình & mô hình ra quyết định trong dự án

### A. Quy trình 4 bước ghi nhận Decision Log

1. **Define Context (Xác định bối cảnh):** Nêu rõ bài toán/vấn đề cần giải quyết và các ràng buộc về thời gian, ngân sách, năng lực kỹ thuật.
2. **Evaluate Alternatives (Đánh giá phương án):** Đưa ra ít nhất 2-3 phương án khả thi. Phân tích rõ lợi ích, hạn chế và sự đánh đổi (Trade-offs).
3. **Formalize & Approve (Chốt & phê duyệt):** Người có thẩm quyền như Sponsor, PO hoặc Tech Lead đưa ra quyết định chính thức theo khung phân quyền RACI/DACI.
4. **Log & Communicate (Ghi nhật ký & truyền thông):** Cập nhật ngay vào Decision Log và thông báo trên kênh chung như Slack/Teams cho toàn bộ dự án.

### B. Áp dụng khung tư duy Bezos (Amazon Decision Framework)

- **One-Way Door Decisions (Quyết định một chiều - khó đảo ngược):** Các quyết định lớn như đổi core architecture, đổi cổng thanh toán chính, ký hợp đồng vendor dài hạn. Nhóm quyết định này cần phân tích kỹ, ghi chép chi tiết trong Decision Log và yêu cầu phê duyệt cấp cao.
- **Two-Way Door Decisions (Quyết định hai chiều - dễ đảo ngược/thử nghiệm):** Thay đổi màu nút báo cáo, chỉnh sửa văn bản thông báo, thử nghiệm luồng UI. Nhóm quyết định này có thể quyết định nhanh, triển khai A/B Testing và ghi log tóm tắt để học hỏi.

---

## 4. Case study thực tế: Dự án "Epic Center"

**Bối cảnh:** Phát triển tính năng **Tìm kiếm & Gợi ý Homestay theo ngân sách tự động** cho ứng dụng Epic Center.

**Tình huống ra quyết định:** Team cần lựa chọn giải pháp công nghệ cho Search Engine.

**Ghi nhận vào Decision Log:**

- **Decision ID:** `DEC-038`
- **Title:** Lựa chọn giải pháp Search Engine cho tính năng Tìm kiếm Homestay.
- **Date:** `10/02/2026`
- **Decision Maker:** Duy (Product Owner) & Tech Lead.
- **Options Considered:**
  - **Option 1:** Dùng tính năng `LIKE / FULLTEXT SEARCH` sẵn có của CSDL PostgreSQL. Chi phí `0 USD`, triển khai nhanh 2 ngày, nhưng chậm khi dữ liệu lớn.
  - **Option 2:** Tích hợp dịch vụ **Elasticsearch / OpenSearch** trên Cloud. Tìm kiếm nhanh dưới 50ms, hỗ trợ tìm kiếm mờ (Fuzzy Search), nhưng tăng `120 USD / tháng` và tốn 7 ngày tích hợp.
- **Final Decision:** Chọn **Option 2 (Elasticsearch)**.
- **Rationale:** Trải nghiệm tìm kiếm là xương sống của ứng dụng đặt phòng. Tốc độ phản hồi nhanh giúp tăng tỷ lệ chuyển đổi (Conversion Rate) đặt phòng lên ước tính 15%.
- **Tác động thực tế:** 8 tháng sau, khi CFO mới vào họp và thắc mắc "Tại sao hằng tháng ứng dụng lại phát sinh thêm khoản chi phí Cloud cho Elasticsearch?", Duy chỉ cần dẫn liên kết file `DEC-038`. Mọi lý do, dữ liệu đo lường và bài toán ROI trước đó hiển thị rõ ràng, giúp chấm dứt nghi ngại của stakeholder.

---

## 5. Các tips & điều lưu ý thực chiến (Anti-patterns & Solutions)

| Sai lầm phổ biến (Anti-Pattern) | Hậu quả | Giải pháp thực chiến |
| --- | --- | --- |
| **"Thỏa thuận miệng trong góc bãi xe / tin nhắn ẩn"** | Quyết định xong không ghi chép, 2 tuần sau mỗi người nhớ một kiểu và đổ lỗi cho nhau. | Áp dụng nguyên tắc kỷ luật: **"Chưa nằm trong Decision Log = Chưa được phê duyệt"**. |
| **Chỉ ghi kết quả, không ghi lý do (Missing Rationale)** | Team nhìn lại quyết định cũ nhưng không hiểu "Tại sao ngày xưa lại làm như vậy?". | Bắt buộc có cột **Context** và **Options Considered**, ghi rõ ít nhất 1 phương án bị loại bỏ và lý do. |
| **Thay đổi quyết định nhưng xóa bối cảnh cũ** | Mất dấu vết tiến hóa của sản phẩm. | Khi có quyết định mới thay thế quyết định cũ, **không xóa log cũ**. Chuyển trạng thái log cũ sang `Superseded by DEC-xxx` và tạo log mới. |
| **Mọi quyết định nhỏ nhặt đều bắt ghi log** | Gây tắc nghẽn quy trình, tạo ra thủ tục hành chính vô ích (Bureaucracy). | Áp dụng quy tắc Bezos: chỉ bắt buộc ghi Decision Log chi tiết cho các quyết định **One-Way Door** hoặc có tác động lớn đến Scope/Cost/Tech. |

---

## 6. Nguồn tham khảo chất lượng (Blogs, Books & YouTube)

### 1. Chuẩn quốc tế & sách

- *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) - 6th & 7th Edition* (phần *Manage Project Knowledge* & *Tailoring*).
- *Architecture Decision Records (ADR)* - tiêu chuẩn tài liệu hóa quyết định kiến trúc phần mềm (Michael Nygard).

### 2. Blog chuyên ngành uy tín

- **ThoughtWorks Technology Radar:** Các bài viết hướng dẫn thực hành *Architecture Decision Records (ADRs)*.
- **Atlassian Team Playbook:** Khung bài viết *DACI Framework for Decision Making* (Driver, Approver, Contributor, Informed).
- **Figma Engineering Blog:** *How we document decisions across product and engineering teams*.

### 3. Kênh YouTube tham khảo

- **Continuous Delivery (Dave Farley):** *Architecture Decision Records (ADR) - How To Document Decisions*.
- **Harvard Business Review:** Chuỗi video *How to Make Faster, Better Decisions in Agile Projects*.
