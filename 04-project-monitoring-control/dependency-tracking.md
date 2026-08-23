# 04-PROJECT-MONITORING-CONTROL: BÀI 10 - DEPENDENCY TRACKING (QUẢN TRỊ & THEO DÕI ĐIỂM PHỤ THUỘC DỰ ÁN)

## 1. KHUNG KIẾN THỨC CHUẨN PMP (PMBOK 6 & 7) & LIÊN HỆ THỰC TẾ

### A. Khái niệm theo chuẩn Quản trị Dự án Quốc tế (PMP)

Trong các dự án phức tạp hoặc phát triển sản phẩm quy mô lớn, hầu như không có công việc nào tồn tại độc lập. **Dependency Tracking (Theo dõi điểm phụ thuộc)** là quy trình nhận diện, lập sơ đồ logic, giám sát và gỡ bỏ các ràng buộc liên kết giữa các tác vụ nội bộ hoặc giữa dự án với các yếu tố bên ngoài.

* **PMBOK 6th Edition:**
* Nằm trong **Project Schedule Management**, trọng tâm tại quy trình **Sequence Activities** (Xác định trình tự hoạt động) và **Control Schedule**.
* Sử dụng phương pháp vẽ sơ đồ mạng (**Precedence Diagramming Method - PDM**) với 4 mối quan hệ logic cơ bản:
* **Finish-to-Start (FS):** Hoạt động A phải kết thúc thì hoạt động B mới được bắt đầu (phổ biến nhất).
* **Start-to-Start (SS):** Hoạt động A phải bắt đầu thì hoạt động B mới có thể bắt đầu.
* **Finish-to-Finish (FF):** Hoạt động A phải kết thúc thì hoạt động B mới có thể kết thúc.
* **Start-to-Finish (SF):** Hoạt động A phải bắt đầu thì hoạt động B mới được kết thúc (hiếm gặp).


* Phân loại 4 nguồn gốc phụ thuộc cốt lõi:
1. **Mandatory Dependencies (Phụ thuộc bắt buộc / Hard logic):** Ràng buộc mang tính chất tự nhiên hoặc hợp đồng pháp lý (vd: Phải thiết kế kiến trúc DB xong mới tạo bảng dữ liệu).
2. **Discretionary Dependencies (Phụ thuộc tùy ý / Soft logic):** Ràng buộc dựa trên kinh nghiệm hoặc thông lệ tốt nhất (vd: Nên xong toàn bộ UI mới bắt đầu test tổng thể).
3. **External Dependencies (Phụ thuộc bên ngoài):** Ràng buộc giữa công việc của dự án với một thực thể ngoài tầm kiểm soát (vd: Chờ cơ quan nhà nước cấp phép, chờ Apple duyệt app).
4. **Internal Dependencies (Phụ thuộc nội bộ):** Ràng buộc giữa các nhóm hoặc các thành viên trong cùng tổ chức dự án (vd: Team Frontend đợi Team Backend cung cấp API).




* **PMBOK 7th Edition & Agile Scaling (SAFe, LeSS):**
* Thuộc **Planning Performance Domain**, **Project Work Performance Domain**, và **Uncertainty Performance Domain**.
* Các mô hình Agile mở rộng xem **Điểm phụ thuộc chéo (Cross-team Dependencies)** là "kẻ thù số 1" bóp nghẹt dòng chảy phân phối giá trị (Flow of Value). Quản trị hiện đại tập trung vào việc **Khử phụ thuộc (Decoupling)** bằng kiến trúc phần mềm và trực quan hóa qua **Program Board / Dependency Matrix**.



---

## 2. CẤU TRÚC BỘ CÔNG CỤ THEO DÕI ĐIỂM PHỤ THUỘC (ARTIFACTS)

Để kiểm soát chặt chẽ các mắt xích liên kết, Product Team cần duy trì một file **Dependency Log / Matrix** (trên Jira Advanced Roadmaps, Miro, Google Sheets hoặc Notion):

### A. Ma trận Theo dõi Điểm Phụ thuộc (Cross-team Dependency Matrix)

| Dependency ID | Hạng mục bị khóa (Downstream - Consumer) | Hạng mục cung cấp (Upstream - Producer) | Loại phụ thuộc | Mức độ ảnh hưởng (Criticality) | Người đầu mối phía cung cấp (Contact) | Ngày cam kết bàn giao (Committed Date) | Trạng thái (RAG) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **DEP-01** | *UI/UX Checkout* (Epic Center App) | *API Khuyến mãi & Voucher* (Core Promo Team) | `Internal Cross-team` | 🔴 **High (Critical)** | Hoàng (Lead Promo Service) | `10/04/2026` | 🟡 **At Risk** (Chậm 2 ngày) |
| **DEP-02** | *Smart Check-in* (Mobile Team) | *Firmware Bluetooth SDK* (Vendor Khóa Thông Minh) | `External Vendor` | 🔴 **High (Critical)** | Mr. Chen (Kỹ sư Đối tác) | `15/04/2026` | 🟢 **On Track** |
| **DEP-03** | *Xuất Hóa đơn VAT* (Web Host) | *Cổng Hóa đơn điện tử* (Bộ phận Kế toán / Thuế) | `External Legal/Dept` | 🟡 **Medium** | Chị Mai (Trưởng phòng KT) | `25/04/2026` | 🟢 **On Track** |
| **DEP-04** | *Push Notification* (Marketing App) | *Cụm Kafka Service* (DevOps / Infra Team) | `Internal Infra` | 🟢 **Low** | Tuấn (DevOps Lead) | `05/04/2026` | 🟢 **Delivered** |

---

### B. Bảng Trực quan hóa Phụ thuộc Đa nhóm (Cross-Team Program Board)

```
 Sprint 01                Sprint 02                Sprint 03
┌──────────────────────┐ ┌──────────────────────┐ ┌──────────────────────┐
│ [Team Mobile App]    │ │ [Team Mobile App]    │ │ [Team Mobile App]    │
│  Story: UI Đặt phòng │ │  Story: Tích hợp Pay │ │  Story: Bật Check-in │
└──────────┬───────────┘ └──────────▲───────────┘ └──────────▲───────────┘
           │                        │ (Chờ API)              │ (Chờ SDK)
           │ Phụ thuộc chéo         │                        │
           ▼                        │                        │
┌──────────────────────┐ ┌──────────┴───────────┐ ┌──────────┴───────────┐
│ [Team Core Backend]  │ │ [Team Core Backend]  │ │ [Đối tác Khóa Ngoài] │
│  Task: DB Schema     │ │  Task: API Payment   │ │  Task: Cung cấp SDK  │
└──────────────────────┘ └──────────────────────┘ └──────────────────────┘

```

* **Quy tắc đọc trực quan:** Mũi tên đỏ nối giữa các Sprint cảnh báo sự chậm trễ dây chuyền: Nếu thẻ gốc (Producer) bị trượt sang Sprint sau, thẻ đích (Consumer) lập tức bị nghẽn (Blocked).

---

## 3. CHIẾN LƯỢC QUẢN TRỊ & "KHỬ" ĐIỂM PHỤ THUỘC (DEPENDENCY DECOUPLING)

Thay vì chỉ thụ động ngồi chờ bên khác bàn giao, một Product Manager/PO chuyên nghiệp cần chủ động áp dụng 4 chiến lược giải phóng phụ thuộc:

```
                      4 CHIẾN LƯỢC LÀM CHỦ PHỤ THUỘC
                      
  ┌────────────────────────────────────────────────────────────────────────┐
  │ 1. Thiết kế theo Hợp đồng giao tiếp (Contract-First Design)           │
  │    • Chốt sớm định dạng dữ liệu (OpenAPI / Swagger Schema).            │
  │    • Cả 2 team phát triển song song dựa trên bản Contract đã chốt.    │
  ├────────────────────────────────────────────────────────────────────────┤
  │ 2. Sử dụng Môi trường Giả lập (Mock API / Virtualization)             │
  │    • Frontend dựng Mock Data giả lập phản hồi của Backend/Vendor.     │
  │    • Không bị đứng hình chờ đợi khi đối tác bảo trì hoặc chậm trễ.    │
  ├────────────────────────────────────────────────────────────────────────┤
  │ 3. Cờ tính năng & Phát hành linh hoạt (Feature Flags / Toggles)       │
  │    • Đóng gói code và deploy trước lên Production.                    │
  │    • Chỉ bật cờ (Toggle ON) khi bên phụ thuộc đã sẵn sàng 100%.       │
  ├────────────────────────────────────────────────────────────────────────┤
  │ 4. Tái cấu trúc Đội ngũ (Team Topologies - Cross-functional Squads)   │
  │    • Gom nhân sự chuyên trách vào cùng 1 Squad tự chủ (End-to-End).   │
  │    • Triệt tiêu hoàn toàn nhu cầu phải phụ thuộc vào phòng ban khác.  │
  └────────────────────────────────────────────────────────────────────────┘

```

---

## 4. CASE STUDY THỰC TẾ: DỰ ÁN "EPIC CENTER"

* **Bối cảnh:** Ở Sprint 8, team ứng dụng Epic Center phát triển tính năng *"Thanh toán Tách dòng Tiền tự động (Split Payment)"* – Khi khách thanh toán gói Combo, tiền phòng tự động chuyển về ví Chủ nhà, tiền Tour chuyển về đối tác Tour, phần hoa hồng chuyển về tài khoản công ty.
* **Mạng lưới phụ thuộc đa tầng (Multi-tier Dependencies):**
* `Nhánh 1 (Nội bộ):` Team Mobile của Duy phụ thuộc vào API chia sẻ dòng tiền từ *Team Core Billing nội bộ*.
* `Nhánh 2 (Bên ngoài):` Team Core Billing lại phụ thuộc vào *Cổng thanh toán Ngân hàng* kích hoạt tính năng tài khoản trung gian (Escrow Account).


* **Sự cố phát sinh (Week 2 của Sprint):**
* Phía Ngân hàng thông báo dời lịch bàn giao môi trường thử nghiệm chậm **10 ngày** do nâng cấp hệ thống core nội bộ.
* Nguy cơ: Nếu chờ ngân hàng, cả Team Core Billing và Team Mobile của Duy sẽ phải ngồi chơi xơi nước suốt 2 tuần, vỡ toàn bộ kế hoạch Sprint.


* **Hành động can thiệp của Product Owner (Duy) & Tech Lead:**
1. **Kích hoạt Contract-First & Mock Data:** Duy cùng Tech Lead 2 team nội bộ ngồi lại 2 giờ để chốt cứng cấu trúc dữ liệu JSON API (Request/Response) cho luồng Split Payment.
2. **Tách đôi quy trình phát triển:**
* Team Mobile sử dụng **Postman Mock Server** để hoàn thiện toàn bộ giao diện UI/UX và logic giỏ hàng (không cần API thật).
* Team Core Billing viết sẵn toàn bộ logic phân bổ tài chính và Unit Test, sẵn sàng kết nối API ngân hàng ngay khi có môi trường.


3. **Tổ chức Sync hàng tuần (Scrum of Scrums):** Duy duy trì buổi họp nhanh 15 phút vào sáng thứ Ba và thứ Năm với PO của Team Core Billing và Quản lý Đối tác phía Ngân hàng để cập nhật tiến độ gỡ nghẽn.


* **Kết quả:** Khi Ngân hàng bàn giao môi trường sandbox, việc ghép nối (Integration) giữa các bên chỉ tốn đúng **01 ngày** do định dạng contract đã chuẩn hóa từ trước. Dự án không bị trễ hạn bàn giao tổng thể.

---

## 5. CÁC TIPS & ĐIỀU LƯU Ý THỰC CHIẾN (ANTI-PATTERNS & SOLUTIONS)

| Sai lầm phổ biến (Anti-Pattern) | Hậu quả | Giải pháp thực chiến |
| --- | --- | --- |
| **"Niềm tin mù quáng" (Blind Trust)** | Mặc định rằng bên thứ ba/đối tác sẽ giao hàng đúng hạn mà không có cơ chế theo dõi định kỳ. | Áp dụng nguyên tắc: **"Tin tưởng nhưng phải kiểm chứng (Trust but Verify)"**. Thiết lập các mốc kiểm tra tiến độ trung gian (Checkpoints). |
| **Phụ thuộc kiểu "Dây chuyền đổ Domino"** | Team A đợi Team B, Team B đợi Team C, Team C đợi Vendor ➔ Toàn bộ dự án tê liệt khi 1 mắt xích gãy. | Tối ưu kiến trúc: Áp dụng **Microservices Decoupling** và chia nhỏ tính năng độc lập (Vertical Slicing) thay vì làm theo lớp ngang (Horizontal Layering). |
| **Ghi nhận phụ thuộc nhưng thiếu ngày cam kết** | Phụ thuộc bị thả nổi vô thời hạn, hai bên đùn đẩy trách nhiệm khi bị hỏi đến tiến độ. | Bắt buộc phải có **01 Đầu mối liên hệ (Point of Contact)** và **01 Hard Deadline bàn giao** được xác nhận bằng văn bản/ticket. |
| **Ghép nối hệ thống vào phút chót (Big-Bang Integration)** | Đến tuần cuối cùng của dự án mới ráp nối các API với nhau, phát sinh hàng loạt lỗi không thể cứu vãn. | Thực hiện **Tích hợp liên tục (Continuous Integration)** từ tuần đầu tiên bằng Mock API và Contract Testing tự động (vd: dùng Pact.io). |

---

## 6. NGUỒN THAM KHẢO CHẤT LƯỢNG (BLOGS, BOOKS & YOUTUBE)

1. **Chuẩn quốc tế & Sách kinh điển:**
* *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) – 6th & 7th Edition* (Phần *Sequence Activities*, *Schedule Network Analysis* và *Planning Domain*).
* *Team Topologies: Organizing Business and Technology Teams for Fast Flow* – Matthew Skelton & Manuel Pais (Cuốn sách kinh điển thế giới về cấu trúc tổ chức và khử điểm phụ thuộc giữa các team công nghệ).
* *Scaled Agile Framework (SAFe 6.0)* – Quản lý Program Board và Cross-team Dependencies.


2. **Blog chuyên ngành uy tín:**
* **Martin Fowler Blog:** *Contract Tests and Decoupling Architectures in Distributed Systems*.
* **Atlassian Agile Coach:** *Managing Dependencies Across Multiple Agile Teams in Jira Advanced Roadmaps*.
* **Spotify Engineering Culture:** *How Spotify Manages Dependencies Across Autonomous Squads*.


3. **Kênh YouTube tham khảo:**
* **Continuous Delivery (Dave Farley):** Video *How to Decouple Dependencies in Software Projects*.
* **Praizion Performance Management:** Video *Precedence Diagramming Method (PDM) & Dependencies for PMP*.
* **Scaled Agile:** Video *Program Board: Visualizing Cross-Team Dependencies*.



---