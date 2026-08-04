# 02-PROJECT-PLANNING: BÀI 12 - DEPENDENCY MAP (BẢN ĐỒ PHỤ THUỘC)

**Tên tài liệu:** `02-project-planning/dependency-map.md`  
**Chủ đề:** Lập Bản đồ và Quản lý Sự phụ thuộc Dự án (Project Dependency Map / Precedence Diagramming) theo chuẩn PMP & Agile/Hybrid  
**Đối tượng hướng tới:** Project Manager (PM), Product Owner (PO), Technical Lead, Solution Architect và Scrum Master.

---

## I. Khung kiến thức chuẩn PMP (PMBOK® Guide - 6th Edition) & Agile

### 1. Định nghĩa & bản chất của Dependency Map

Theo PMBOK® Guide 6th Edition, quy trình **Sequence Activities** (Process 6.3) là quá trình xác định và ghi nhận các mối quan hệ logic giữa các hoạt động dự án.

Trong thực hành quản lý dự án, **Dependency Mapping** (lập bản đồ sự phụ thuộc) giúp đội dự án nhìn rõ quan hệ phụ thuộc giữa activity, work package, deliverable, team hoặc hệ thống bên ngoài để tối ưu thứ tự thực thi, nhận diện rủi ro dây chuyền và kiểm soát các điểm nghẽn trên tiến độ.

Dependency Map đặc biệt quan trọng trong môi trường Agile/Hybrid, nơi nhiều team cùng chạy sprint song song nhưng vẫn phụ thuộc vào API, dữ liệu, môi trường, quyết định nghiệp vụ hoặc vendor bên ngoài.

### 2. Các loại phụ thuộc trong PMP

PMBOK phân loại các mối quan hệ phụ thuộc theo bốn nhóm chính:

1. **Mandatory Dependencies (Phụ thuộc bắt buộc / Hard Logic):** Các phụ thuộc mang tính bản chất kỹ thuật, quy trình, pháp lý hoặc quy luật tự nhiên, gần như không thể thay đổi. Ví dụ: phải hoàn thành eKYC trước khi cấp hạn mức giao dịch tài khoản; phải hoàn tất API trước khi kiểm thử tích hợp API thật.
2. **Discretionary Dependencies (Phụ thuộc tùy chọn / Soft Logic / Preferred Logic):** Do đội ngũ dự án chủ động lựa chọn dựa trên kinh nghiệm, best practice hoặc thói quen vận hành. Ví dụ: ưu tiên thiết kế UI mobile trước UI web dù kỹ thuật cho phép làm song song.
3. **External Dependencies (Phụ thuộc bên ngoài):** Quan hệ giữa công việc trong dự án với yếu tố hoặc bên thứ ba ngoài tầm kiểm soát trực tiếp của team. Ví dụ: chờ đối tác ngân hàng cấp quyền kết nối Sandbox API, chờ nhà cung cấp SDK xử lý lỗi, chờ cơ quan nhà nước cấp giấy phép an toàn thông tin.
4. **Internal Dependencies (Phụ thuộc nội bộ):** Mối quan hệ giữa các công việc nội bộ do chính team dự án kiểm soát. Ví dụ: backend cần hoàn tất API contract trước khi frontend bắt đầu tích hợp.

### 3. Phương pháp Sơ đồ Tiền nhiệm (Precedence Diagramming Method - PDM)

PDM sử dụng các khối (nodes) đại diện cho công việc và các mũi tên thể hiện quan hệ phụ thuộc logic giữa các công việc đó.

- **Finish-to-Start (FS - Hoàn thành để bắt đầu):** Công việc A phải hoàn thành thì công việc B mới được bắt đầu. Đây là quan hệ phổ biến nhất trong lập lịch.
- **Start-to-Start (SS - Bắt đầu để bắt đầu):** Công việc A phải bắt đầu thì công việc B mới được phép bắt đầu.
- **Finish-to-Finish (FF - Hoàn thành để hoàn thành):** Công việc A phải hoàn thành thì công việc B mới được hoàn thành.
- **Start-to-Finish (SF - Bắt đầu để hoàn thành):** Công việc A phải bắt đầu thì công việc B mới được hoàn thành. Quan hệ này rất hiếm gặp và thường chỉ xuất hiện trong các tình huống chuyển giao vận hành đặc thù.

### 4. Khái niệm Lead và Lag

- **Lead (Thời gian vượt trước):** Cho phép đẩy sớm công việc kế tiếp khi công việc tiền nhiệm chưa hoàn thành 100%. Ví dụ: khi đã có 50% tài liệu SRS hoặc API contract ổn định, team dev có thể bắt đầu dựng khung database hoặc mock service.
- **Lag (Thời gian trễ):** Khoảng thời gian bắt buộc phải chờ giữa hai công việc. Ví dụ: sau khi deploy code lên môi trường staging, phải chờ 4 giờ để hệ thống đồng bộ dữ liệu trước khi QA bắt đầu kiểm thử.

---

## II. Ví dụ & minh họa thực tế

### Ví dụ: Dependency Map cho dự án "Epic Center" - Module E-Coffer & Thanh toán

Dưới đây là mô hình ma trận phụ thuộc cross-team giữa các đội ngũ kỹ thuật và đối tác:

```text
[Đội UI/UX] ──(FS)──> [Đội Frontend Mobile] ──(SS)──┐
                                                    ├──(FS)──> [E2E Testing & Go-Live]
[Đội Core Backend] ──(SS)──> [Đội Integration API] ──┘
                                     │
                             (External Dependency)
                                     ▼
                        [Ngân hàng Cung cấp VietQR API]
```

### Bảng phân tích chi tiết mối quan hệ phụ thuộc (Dependency Log)

| Mã công việc | Tên công việc | Công việc tiền nhiệm (Predecessor) | Loại phụ thuộc (Dependency Type) | Ràng buộc / Tác động |
| --- | --- | --- | --- | --- |
| **DEP-01** | **Code luồng nạp tiền ví E-Coffer** | Thiết kế UI/UX màn hình Ví | **Mandatory & Internal (FS)** | Dev không thể code frontend nếu chưa chốt Figma design. |
| **DEP-02** | **Tích hợp Webhook VietQR** | Cấp tài khoản Sandbox từ ngân hàng | **External & Mandatory (FS + Lag 2 days)** | Phụ thuộc tốc độ duyệt hồ sơ của ngân hàng đối tác. Trễ 1 ngày có thể làm trễ toàn bộ luồng thanh toán. |
| **DEP-03** | **Viết test script tự động** | Thiết kế API Spec (Swagger) | **Discretionary & Internal (SS + Lead 1 day)** | QA viết kịch bản test ngay khi có Swagger Spec, không cần chờ dev code xong mới bắt đầu. |

---

## III. Case study dẫn chứng thực tế

### Hiệu ứng domino làm đổ bể tiến độ dự án Super App do phụ thuộc ẩn (Hidden Dependency)

**Bối cảnh:** Một dự án chuyển đổi số Super App đặt phòng và di chuyển được chia thành ba team độc lập:

- **Team A:** User Profile & eKYC.
- **Team B:** Core Đặt phòng.
- **Team C:** Cổng Thanh toán.

Mỗi team chạy Agile/Scrum riêng và chủ yếu theo dõi Sprint Backlog của team mình.

**Vấn đề phát sinh:**

1. Đến tuần thứ 8, Team B hoàn thành toàn bộ tính năng đặt phòng và sẵn sàng cho UAT. Tuy nhiên, luồng đặt phòng bắt buộc user phải có trạng thái `Verified` từ module eKYC của Team A.
2. Team A gặp rủi ro kỹ thuật với nhà cung cấp SDK OCR nên chủ động lùi tính năng eKYC sang sprint tiếp theo, nhưng không thông báo sớm cho Team B.
3. Kết quả: Team B bị tắc nghẽn, không thể test hay nghiệm thu sản phẩm. Team C cũng bị ảnh hưởng vì không thể kiểm thử đầy đủ luồng thanh toán gắn với booking đã xác thực.

**Giải pháp khắc phục:**

1. Ban quản lý dự án thiết lập **Program Dependency Board** họp hàng tuần trong cơ chế Scrum of Scrums.
2. Mọi dependency giữa các team phải được định danh thành hạng mục ưu tiên trong **Dependencies Backlog**.
3. Mỗi dependency có **Dependency Owner**, ngày cần hoàn thành, mức độ rủi ro và phương án thay thế nếu bị trễ.
4. Các team thống nhất dùng API contract và mock response để không bị chặn hoàn toàn khi module phụ thuộc chưa hoàn thành.

**Kết quả:** Dự án giảm được tình trạng phụ thuộc ẩn, PM có dữ liệu sớm hơn để escalate vendor risk, còn các team có thể tiếp tục phát triển và kiểm thử một phần thay vì chờ hoàn toàn.

---

## IV. Tips & điều lưu ý thực chiến cho PM/PO

1. **Luôn chú ý External Dependencies:** Các bên thứ ba như đối tác, ngân hàng, nhà cung cấp SDK hoặc cơ quan nhà nước không chịu sự quản lý trực tiếp của PM. Vì vậy, phụ thuộc bên ngoài thường có xác suất trễ hạn cao nhất. Hãy cộng thêm buffer hoặc lag hợp lý trong kế hoạch.

2. **Dùng kỹ thuật Dependency Decoupling để gỡ nút thắt:** Nếu Team B phải chờ API của Team A mới làm việc được, PM/Tech Lead nên yêu cầu Team A viết trước API Contract/Swagger và tạo Mock API. Team B có thể dùng Mock API để phát triển giao diện ngay, sau đó chỉ cần đấu nối lại khi API thật sẵn sàng.

3. **Cập nhật Dependency Map vào Critical Path:** Những công việc có nhiều phụ thuộc hội tụ (Merge Dependency) thường là mắt xích yếu trên đường găng. Nếu một mắt xích này trễ, toàn bộ tiến độ dự án có thể bị trượt.

4. **Đưa dependency vào backlog, không chỉ để trong biên bản họp:** Trong Agile/Hybrid, dependency cần có owner, trạng thái, deadline và acceptance criteria như một backlog item. Nếu chỉ ghi trong meeting note, dependency rất dễ bị quên.

5. **Theo dõi lead indicator thay vì chỉ báo cáo trễ hạn:** Với dependency quan trọng, PM nên theo dõi tín hiệu sớm như vendor chưa phản hồi, API contract chưa được review, môi trường test chưa tạo, hoặc security chưa approve. Các tín hiệu này giúp xử lý trước khi milestone bị ảnh hưởng.

6. **Phân biệt blocker và dependency:** Dependency là quan hệ phụ thuộc có thể được lên kế hoạch trước. Blocker là tình trạng công việc đang bị chặn tại thời điểm hiện tại. Một dependency không được quản lý tốt sẽ dễ biến thành blocker.

---

## V. Tài liệu & nguồn tham khảo

### 1. Chuẩn quốc tế & sách gối đầu giường

- *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) - 6th Edition*, Chapter 6: Project Schedule Management, Section 6.3 Sequence Activities.
- *Scaled Agile Framework (SAFe) 6.0*: Managing Dependencies on the Program Board.

### 2. Blog & bài viết chuyên sâu

- Atlassian Agile Coach: *Managing dependencies in Jira Software and Agile Teams*.
- ProjectManagement.com: *Precedence Diagramming Method (PDM) in Modern Project Management*.

### 3. Video / YouTube hữu ích

- Search keyword: *"Precedence Diagramming Method PDM Explained - PMP Exam Prep"* (Ricardo Vargas).
- Search keyword: *"How to manage Cross-Team Dependencies in Agile/SAFe"*.
