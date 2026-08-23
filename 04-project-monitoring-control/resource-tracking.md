# 04-PROJECT-MONITORING-CONTROL: BÀI 11 - RESOURCE TRACKING (THEO DÕI NGUỒN LỰC & CÂN BẰNG TẢI DỰ ÁN)

## 1. KHUNG KIẾN THỨC CHUẨN PMP (PMBOK 6 & 7) & LIÊN HỆ THỰC TẾ

### A. Khái niệm theo chuẩn Quản trị Dự án Quốc tế (PMP)

Quản trị nguồn lực là nghệ thuật cân bằng giữa khối lượng công việc cần làm và năng lực thực tế của đội ngũ nhằm tối ưu hóa hiệu suất mà không gây kiệt sức (Burnout). **Resource Tracking (Theo dõi & Cân bằng nguồn lực)** là hoạt động giám sát việc phân bổ, mức độ sử dụng và tính sẵn sàng của cả hai nhóm tài nguyên: **Team Resources (Con người)** và **Physical Resources (Hạ tầng, thiết bị, vật tư)**.

* **PMBOK 6th Edition:**
* Thuộc **Project Resource Management**, trực tiếp là hai quy trình:
* **Manage Team (Quản lý đội ngũ):** Theo dõi hiệu suất nhân sự, cung cấp phản hồi, xử lý xung đột và quản lý các biến động phân bổ nhân lực.
* **Control Resources (Kiểm soát nguồn lực vật lý):** Đảm bảo máy chủ, tài nguyên vật lý, bản quyền phần mềm và công cụ được cung cấp đúng lúc, đúng nơi và giải phóng đúng hạn.


* Sử dụng biểu đồ phân bổ nguồn lực (**Resource Histogram**) và Cơ cấu phân chia nguồn lực (**Resource Breakdown Structure - RBS**) để kiểm soát dung lượng.


* **PMBOK 7th Edition & Lean/Agile:**
* Nằm trong **Team Performance Domain** và **Project Work Performance Domain**.
* Thay đổi căn bản về mặt tư duy: **Chuyển từ "Tối đa hóa mức độ bận rộn" (Maximizing Utilization) sang "Tối ưu hóa dòng chảy giá trị" (Optimizing Value Flow)**.
* Trong môi trường Agile/Tech, quản trị nguồn lực không phải là vi mô theo dõi từng giờ làm việc của nhân viên, mà là quản lý **Dung lượng bền vững (Sustainable Pace / Capacity)** của cả đội ngũ qua các Sprint.



---

### B. Hai Nhóm Nguồn lực Cốt lõi trong Dự án Công nghệ

```
                           HỆ THỐNG NGUỒN LỰC DỰ ÁN
                                      │
        ┌─────────────────────────────┴─────────────────────────────┐
        ▼                                                           ▼
 [TEAM RESOURCES - CON NGƯỜI]               [PHYSICAL RESOURCES - CÔNG CỤ & HẠ TẦNG]
  • Product Owner / Business Analyst          • Máy chủ Cloud (AWS / GCP / Azure)
  • UI/UX Designer                            • Môi trường kiểm thử (Staging / Lab)
  • Frontend / Backend / Mobile Dev           • Bản quyền phần mềm (Figma, Jira, IDE)
  • QA / QC / Automation Tester               • Tài khoản thiết bị Test (iOS / Android)
  • DevOps / Security Engineer                • Hạn ngạch gọi API bên thứ ba (SMS, eKYC)

```

---

## 2. CẤU TRÚC BỘ CÔNG CỤ & KHUNG ĐO LƯỜNG NGUỒN LỰC (ARTIFACTS)

Một hệ thống **Resource Tracking & Capacity Matrix** chuẩn mực (trên Jira Resource Management, Tempo, Google Sheets hoặc Notion) cần định lượng được tính sẵn sàng và mức độ tải của từng vị trí:

### A. Ma trận Năng lực & Mức độ Tải Nhân sự (Team Capacity & Allocation Matrix)

* **Thời gian tính toán:** Chu kỳ Sprint 2 tuần (10 ngày làm việc = 80 giờ chuẩn/người).
* **Quy ước Giờ làm việc Hiệu dụng (Focus Hours):** Mỗi người chỉ có tối đa **$6\text{ giờ/ngày}$** làm việc tập trung (trừ $2\text{ giờ}$ cho họp hành, Daily Standup, email, trao đổi nội bộ). Dung lượng khả dụng chuẩn = **$60\text{ giờ/Sprint}$**.

| Nhân sự | Vai trò chuyên môn | Năng lực khả dụng (Available Capacity) | Giờ được giao việc (Allocated Hours) | Tỷ lệ sử dụng (Utilization Rate) | Mức độ rủi ro tải | Biện pháp điều hòa |
| --- | --- | --- | --- | --- | --- | --- |
| **Duy** | Product Owner / UI/UX | $60\text{ giờ}$ | $52\text{ giờ}$ | **86.7%** | 🟢 **An toàn** | Tải tối ưu, duy trì nhịp độ |
| **Tấn** | Tech Lead / Backend | $60\text{ giờ}$ | $84\text{ giờ}$ | **140.0%** | 🔴 **Quá tải nghiêm trọng** | Chuyển bớt task DB sang Dev 2 |
| **Huy** | Senior Frontend Dev | $60\text{ giờ}$ | $48\text{ giờ}$ | **80.0%** | 🟢 **An toàn** | Sẵn sàng nhận thêm task |
| **Lan** | QA Lead / Tester | $60\text{ giờ}$ | $72\text{ giờ}$ | **120.0%** | 🔴 **Quá tải** | Tự động hóa kiểm thử hồi quy |
| **Tuấn** | DevOps Engineer (Share) | $20\text{ giờ}$ (Bán thời gian) | $18\text{ giờ}$ | **90.0%** | 🟡 **Chú ý** | Theo sát lịch trực hệ thống |

---

### B. Các Công thức Toán học Đo lường Hiệu suất Nguồn lực

#### 1. Tỷ lệ Sử dụng Nguồn lực (Resource Utilization Rate - $U$)

$$U = \frac{\text{Allocated Hours (Số giờ phân bổ công việc)}}{\text{Available Capacity (Số giờ khả dụng thực tế)}} \times 100\%$$

* **Thang chuẩn đoán sức khỏe tải nhân sự:**
* $U < 70\%$ 🟡: **Thừa công suất (Under-utilized)** – Nguồn lực chưa được khai thác hiệu quả, có thể gánh thêm công việc.
* $75\% \le U \le 85\%$ 🟢: **Vùng hiệu suất tối ưu (Optimal Zone)** – Đội ngũ làm việc tập trung nhưng vẫn có $15\% - 25\%$ "dung lượng đệm" (**Slack Time**) để nghiên cứu, cải tiến quy trình và xử lý rủi ro đột xuất.
* $U > 100\%$ 🔴: **Quá tải (Over-allocated / Burnout Risk)** – Năng suất bị tụt dốc, tỷ lệ lỗi phần mềm tăng vọt, nguy cơ nhân sự nghỉ việc.



---

## 3. CÁC KỸ THUẬT TỐI ƯU HÓA NGUỒN LỰC CHUẨN PMP (RESOURCE OPTIMIZATION)

Khi phát hiện sự mất cân bằng về nguồn lực giữa các giai đoạn hoặc các thành viên, Quản lý Dự án áp dụng 2 kỹ thuật nền tảng:

### 1. Resource Leveling (San phẳng nguồn lực)

* **Cơ chế:** Điều chỉnh ngày bắt đầu và kết thúc của các hoạt động dựa trên sự giới hạn cứng về nguồn lực (ví dụ: một lập trình viên duy nhất không thể làm 2 task cùng một lúc).
* **Đặc tính cốt lõi:** **Thường làm kéo dài thời gian hoàn thành của dự án** hoặc thay đổi Đường găng (Critical Path) để bảo vệ nguồn lực không bị quá tải.

### 2. Resource Smoothing (Làm mịn nguồn lực)

* **Cơ chế:** Điều chỉnh phân bổ nguồn lực của các công việc chỉ trong phạm vi độ trễ cho phép (**Total Float / Free Float**).
* **Đặc tính cốt lõi:** **Tuyệt đối không làm thay đổi ngày kết thúc dự án** và không làm biến đổi Critical Path. Công việc nào có thể lùi mà không ảnh hưởng hạn chót thì sẽ được dời sang thời điểm nhân sự rảnh rỗi hơn.

---

## 4. CASE STUDY THỰC TẾ: DỰ ÁN "EPIC CENTER"

* **Bối cảnh:** Ở Sprint 10, dự án Epic Center bước vào giai đoạn tăng tốc hoàn thiện module *"Tự động Xuất hóa đơn VAT & Báo cáo Doanh thu cho Chủ nhà"*.
* **Tín hiệu cảnh báo từ Resource Tracking Sheet:**
* **Tech Lead (Tấn)** đang bị gán tới **84 giờ** công việc (tương đương mức tải $140\%$). Anh phải đồng thời: Viết Core API phức tạp, hỗ trợ 2 Junior Devs sửa bug, và phụ trách trực hạ tầng Cloud server.
* **Hậu quả nhãn tiền:** Tấn thường xuyên làm việc đến 23:00 đêm, bắt đầu có dấu hiệu mệt mỏi, phản hồi tin nhắn chậm và làm lọt 2 lỗi logic nghiêm trọng trong đợt merge code gần nhất.


* **Chiến lược Cân bằng tải của Product Owner (Duy):**
1. **Áp dụng Resource Smoothing cho các tác vụ không nằm trên Đường găng:** Duy rà soát lại Backlog, nhận thấy tác vụ *"Tối ưu hóa định dạng file PDF xuất hóa đơn"* có độ trễ tự do (Free Float = 4 ngày). Duy quyết định dời tác vụ này sang tuần tiếp theo khi áp lực công việc giảm bớt.
2. **Tái phân bổ theo mô hình Kỹ năng chữ T (T-shaped Skills):**
* Tách bỏ các task cấu hình Database cơ bản khỏi Tấn và chuyển giao cho một Senior Frontend Dev có hiểu biết về Backend (Huy - người đang có mức tải $80\%$).
* Duy (PO) tự mình đứng ra phụ trách việc kiểm thử sơ bộ dữ liệu hóa đơn (User Acceptance Testing) để giảm tải cho QA Lead.


3. **Bảo vệ Vùng tập trung (Focus Shielding):** Cắt giảm 50% các cuộc họp không cần thiết trong tuần của Tấn; mọi yêu cầu hỗ trợ từ các phòng ban khác bắt buộc phải đi qua PO làm đầu mối tiếp nhận.


* **Kết quả:** Mức độ tải của Tech Lead hạ từ $140\%$ xuống **$83\%$** (về vùng an toàn); toàn bộ module Hóa đơn được phát hành đúng kế hoạch với độ chính xác tài chính $100\%$.

---

## 5. CÁC TIPS & ĐIỀU LƯU Ý THỰC CHIẾN (ANTI-PATTERNS & SOLUTIONS)

| Sai lầm phổ biến (Anti-Pattern) | Hậu quả | Giải pháp thực chiến |
| --- | --- | --- |
| **"Bẫy Tận dụng 100%" (100% Utilization Trap)** | Lên kế hoạch ép team kín lịch $100\%$ ($8\text{h/ngày}$), biến quy trình thành "đường cao tốc tắc nghẽn", chỉ cần 1 sự cố nhỏ là sụp đổ dây chuyền. | Luôn duy trì **Dung lượng đệm $15\% - 20\%$ (Slack Time)** trong mỗi Sprint để hấp thụ các biến số bất định. |
| **"Hội chứng Người Hùng" (Hero Culture)** | Phụ thuộc hoàn toàn vào 1 nhân sự "siêu sao" gánh cả dự án; khi người này ốm hoặc nghỉ việc, dự án lập tức tê liệt. | Xóa bỏ **"Chỉ số Xe buýt" (Bus Factor = 1)** bằng cách chia sẻ kiến thức liên tục qua Code Review, Pair Programming và chuẩn hóa tài liệu kỹ thuật. |
| **"Nhảy việc liên tục" (Context Switching)** | Bắt 1 nhân sự phụ trách đồng thời 3 - 4 dự án khác nhau; năng suất não bộ bị suy giảm tới $40\%$ do phân tán chú ý. | **Nguyên tắc "Tập trung Đơn nhiệm"**: Hạn chế tối đa việc phân bổ nhân sự làm việc đa nhiệm chéo dự án; ưu tiên Squad chuyên trách cố định. |
| **"Định luật Brooks" (Brooks' Law)** | Thêm người vào một dự án phần mềm đang trễ hạn chỉ làm cho nó trễ hạn hơn (do tốn thời gian đào tạo và chi phí giao tiếp). | Khi dự án trễ hạn, ưu tiên **Cắt giảm Phạm vi (De-scoping)** hoặc **Tối ưu Quy trình**, hạn chế nhồi thêm nhân sự mới vào giai đoạn nước rút. |

---

## 6. NGUỒN THAM KHẢO CHẤT LƯỢNG (BLOGS, BOOKS & YOUTUBE)

1. **Chuẩn quốc tế & Sách kinh điển:**
* *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) – 6th & 7th Edition* (Chương *Project Resource Management* & *Team Performance Domain*).
* *The Mythical Man-Month: Essays on Software Engineering* – Frederick P. Brooks Jr. (Cuốn sách kinh điển về quản trị nguồn lực phần mềm và Định luật Brooks).
* *Peopleware: Productive Projects and Teams* – Tom DeMarco & Timothy Lister (Tác phẩm chuẩn mực về tâm lý học và quản trị con người trong dự án công nghệ).


2. **Blog chuyên ngành uy tín:**
* **Martin Fowler Blog:** *Slack Time in Software Engineering and Agile Teams*.
* **Atlassian Team Playbook:** *Capacity Planning for High-Performing Agile Teams*.
* **Spotify Engineering Culture:** *Managing Autonomous Squads and Shared Resources*.


3. **Kênh YouTube tham khảo:**
* **Praizion Performance Management:** Video *Resource Leveling vs Resource Smoothing for PMP Exam*.
* **Continuous Delivery (Dave Farley):** Video *Why 100% Resource Utilization Is a Terrible Idea*.
* **Agile Academy:** *Team Capacity Planning and Velocity Management in Scrum*.



---

