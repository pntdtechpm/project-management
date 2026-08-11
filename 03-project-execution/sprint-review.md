# 03-PROJECT-EXECUTION: BÀI 06 - SPRINT REVIEW (ĐÁNH GIÁ SPRINT DỰ ÁN)

## 1. KHUNG KIẾN THỨC CHUẨN PMP (PMBOK 6 & 7) & LIÊN HỆ THỰC TẾ

### A. Khái niệm theo chuẩn Quản trị Dự án Quốc tế (PMP)

* **PMBOK 6th Edition & Agile Practice Guide:**
* Sprint Review (hay còn gọi là Demonstration/Iteration Review) thuộc nhóm quy trình **Monitoring & Controlling** và quy trình nghiệm thu bàn giao (**Validate Scope**).
* Mục tiêu chính: Kiểm tra khối lượng công việc tăng trưởng (**Increment**) đã hoàn thành trong Sprint so với Định nghĩa Hoàn thành (**Definition of Done - DoD**) và nhận phản hồi trực tiếp từ các bên liên quan (Stakeholders).


* **PMBOK 7th Edition:**
* Thuộc **Stakeholder Performance Domain**, **Delivery Performance Domain** và **Measurement Performance Domain**.
* Nhấn mạnh tầm quan trọng của **Feedback Loops** (Vòng phản hồi nhanh). Trong môi trường Agile/Hybrid, Sprint Review đóng vai trò là điểm chốt điều chỉnh thích ứng (Adaptation Point), giúp đảm bảo sản phẩm luôn tạo ra giá trị thực sự (Value Delivery) thay vì chỉ chạy theo đúng tiến độ dự kiến ban đầu.



### B. Liên hệ Thực tế Quản lý Sản phẩm (Product Management)

* **Phân biệt cốt lõi:** Sprint Review **không phải là buổi báo cáo tiến độ bằng Slide** cho lãnh đạo xem.
* **Mục đích cốt lõi đối với Product Team:**
1. **Buổi cộng tác làm việc thực tế (Working Session):** Cho Stakeholders "sờ tận tay, thấy tận mắt" các tính năng đã hoạt động được trên môi trường Staging/Beta.
2. **Thu thập Phản hồi đa chiều:** Lắng nghe nhận xét trực tiếp từ Stakeholders, End-users, CSKH, Sales để điều chỉnh định hướng sản phẩm.
3. **Cập nhật Product Backlog:** Dựa trên kết quả thực tế của Sprint và phản hồi thu được, Product Owner (PO) cập nhật lại thứ tự ưu tiên hoặc bổ sung các yêu cầu mới vào Product Backlog cho các Sprint tiếp theo.



---

## 2. CẤU TRÚC BỘ CÔNG CỤ & KHUNG TÀI LIỆU SPRINT REVIEW (ARTIFACTS)

Để tổ chức buổi Sprint Review hiệu quả, bộ công cụ chia sẻ cần bao gồm 3 file/khung chuẩn sau:

### A. Khung Chương trình Họp (Sprint Review Agenda & Checklist)

* **Thời lượng:** Đóng khung thời gian (**Timebox**) 1 - 2 giờ cho Sprint kéo dài 2 tuần.
* **Cấu trúc Agenda chuẩn:**
1. *PO mở đầu (5 phút):* Tuyên bố Sprint Goal và danh sách User Stories đạt chuẩn DoD (Done) vs. chưa Done.
2. *Dev/QA Demo (30 - 45 phút):* Trình diễn trực tiếp các tính năng chạy thực tế trên môi trường Staging.
3. *Thảo luận & Feedback (20 - 30 phút):* Stakeholders đặt câu hỏi, trải nghiệm thử và đưa ra góp ý.
4. *PO Tổng kết & Nhìn về tương lai (10 phút):* Trình bày định hướng sơ bộ cho Sprint tiếp theo (Next Sprint Outlook) và ngân sách/tiến độ tổng thể còn lại.



### B. Mẫu Biểu mẫu Ghi nhận Phản hồi (Feedback Collection Form / Board)

Bảng ghi nhận ý kiến (trên Miro, Notion, Confluence hoặc FigJam) chia thành 4 ô đơn giản:

```
+------------------------------------+------------------------------------+
| 🟢 Điều Stakeholders Yêu thích     | 🔴 Điều cần Cải thiện / Chưa tốt   |
| (What worked well / Liked)         | (What needs improvement)           |
+------------------------------------+------------------------------------+
| ❓ Câu hỏi & Thắc mắc mới          | 💡 Ý tưởng / Đề xuất mới           |
| (Questions & Doubts)               | (New Ideas / Backlog Candidate)    |
+------------------------------------+------------------------------------+

```

---

## 3. QUY TRÌNH TRIỂN KHAI SPRINT REVIEW (STEP-BY-STEP WORKFLOW)

1. **Chuẩn bị (Pre-Review / Dry Run):**
* Đội Kỹ thuật và QA kiểm tra lần cuối, đảm bảo môi trường Staging ổn định, dữ liệu thử nghiệm (Test data) đã được chuẩn bị sẵn.
* PO rà soát danh sách User Stories: **Chỉ những Task đạt 100% Definition of Done mới được mang ra Review**.


2. **Thực thi (Run the Session):**
* Giữ không khí cởi mở, khuyến khích phản hồi mang tính xây dựng.
* Trình diễn tính năng dựa trên góc nhìn người dùng (User Journey/Use Case) thay vì giải thích dòng code hay thuật toán.


3. **Thu thập & Phân loại Phản hồi (Process Feedback):**
* Tất cả phản hồi, góp ý được ghi chép lại công khai trên Feedback Board.


4. **Cập nhật Product Backlog (Post-Review Adaption):**
* PO đánh giá các Feedback: Tính năng nào cần chỉnh sửa nhỏ ➔ Tạo Bug/Task vào Sprint sau. Ý tưởng nào lớn ➔ Đưa vào Product Backlog để xếp thứ tự ưu tiên.



---

## 4. CASE STUDY THỰC TẾ: DỰ ÁN "EPIC CENTER"

* **Bối cảnh:** Buổi Sprint Review cuối Sprint 7 cho dự án ứng dụng Epic Center. Mục tiêu Sprint Goal là: *"Cho phép Chủ nhà (Host) đăng tải thông tin và thiết lập bảng giá phòng Homestay theo mùa"*.
* **Diễn biến buổi Review:**
* **Thành phần tham dự:** Product Team (Duy - PO, Dev, UI/UX), Giám đốc Vận hành (COO), Trưởng phòng Kinh doanh (Sales Lead) và 2 Chủ nhà được mời trải nghiệm thử.
* **Phần Demo:** Dev trình diễn luồng tạo bài đăng Homestay mới trên app. Tất cả luồng chạy mượt mà theo đúng DoD.
* **Phản hồi phát sinh (Feedback Loop):**
* *Sales Lead nhận xét:* "Giao diện chọn giá theo từng ngày khá đẹp nhưng thao tác chọn từng ngày một rất lâu đối với các Host có 20 phòng. Họ cần tính năng **'Chọn giá theo dải ngày' (Bulk Date Pricing)**."
* *Chủ nhà tham dự góp ý:* "Tôi muốn hệ thống có nút 'Tạo bản sao' (Duplicate) từ phòng cũ để đỡ phải gõ lại thông tin tiện ích từ đầu."


* **Hành động xử lý của PO (Duy):**
* Duy xác nhận đây là 2 đóng góp cực kỳ giá trị nâng cao trải nghiệm người dùng (UX).
* Duy lập tức khởi tạo 2 User Stories mới trên Jira: `STORY-201: Bulk Date Pricing` và `STORY-202: Duplicate Room Listing`.
* Đưa `STORY-201` vào danh sách ưu tiên cao cho Sprint 8 ngay sau đó.




* **Kết quả:** Stakeholders cảm thấy ý kiến của mình được tôn trọng và lắng nghe; sản phẩm Epic Center ra mắt bám sát đúng nhu cầu thực tế của người dùng cuối.

---

## 5. CÁC TIPS & ĐIỀU LƯU Ý THỰC CHIẾN (ANTI-PATTERNS & SOLUTIONS)

| Sai lầm phổ biến (Anti-Pattern) | Hậu quả | Giải pháp thực chiến |
| --- | --- | --- |
| **Demo tính năng chưa hoàn thiện ("Sắp xong")** | Stakeholders thất vọng khi tính năng bị lỗi giữa chừng, mất niềm tin vào team. | **Tuyên ngôn thép:** Không đạt 100% Definition of Done = Không mang ra Demo. Chỉ demo những gì đã thực sự chạy được. |
| **Biến Sprint Review thành buổi "Sát phạt" / "Hỏi cung"** | Team phòng thủ, giấu giếm lỗi và ngại chia sẻ sự thật. | PO & Scrum Master quán xán tư duy: Buổi Review là để **tìm giải pháp hoàn thiện sản phẩm**, không phải để tìm người đổ lỗi. |
| **Chỉ nói bằng Slide Powerpoint** | Stakeholders không hình dung được sản phẩm thực tế, buổi họp trở nên nhàm chán. | Cấm dùng Slide để mô tả tính năng. **Bắt buộc thao tác trực tiếp trên giao diện thực tế (Live App / Staging)**. |
| **Gật đầu hứa hẹn mọi yêu cầu mới tại chỗ** | Phạm vi sản phẩm bị "vỡ trận" (Scope Creep), vỡ kế hoạch Sprint sau. | PO ghi nhận tất cả Feedback nhưng truyền thông rõ: *"Cảm ơn góp ý, PO sẽ đánh giá lại ROI & độ ưu tiên trên Product Backlog trước khi đưa vào Sprint tới"*. |

---

## 6. NGUỒN THAM KHẢO CHẤT LƯỢNG (BLOGS, BOOKS & YOUTUBE)

1. **Chuẩn quốc tế & Sách:**
* *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) – 6th & 7th Edition* (Phần *Validate Scope* & *Stakeholder Engagement*).
* *Agile Practice Guide* (PMI & Agile Alliance - Section 5.2.5 *Demonstrations/Reviews*).
* *Scrum Mastery* – Geoff Watts (Chương hướng dẫn tối ưu hóa các sự kiện Scrum).


2. **Blog chuyên ngành uy tín:**
* **Scrum.org:** Chuỗi bài viết *"Myth Busters: The Sprint Review is just a Demo"*.
* **Mountain Goat Software (Mike Cohn):** *How to Run an Effective Sprint Review Meeting*.
* **Roman Pichler Blog:** *Tips for Effective Sprint Reviews for Product Owners*.


3. **Kênh YouTube tham khảo:**
* **Scrum Master Series:** Video *Sprint Review Meeting Explained - Structure, Agenda & Anti-Patterns*.
* **Agile Academy:** *How to Facilitate a Successful Sprint Review*.
* **Development That Pays:** *Sprint Review vs Sprint Retrospective - What’s the difference?*.


