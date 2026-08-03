# 02-PROJECT-PLANNING: BÀI 08 - RISK PLAN (KẾ HOẠCH QUẢN LÝ RỦI RO)

**Tên tài liệu:** `02-project-planning/risk-plan.md`  
**Chủ đề:** Kế hoạch Quản lý Rủi ro (Project Risk Management Plan) theo chuẩn PMP  
**Đối tượng hướng tới:** Project Manager (PM), Risk Owner, Tech Lead, PMO và các thành viên chủ chốt trong dự án.

---

## I. Khung kiến thức chuẩn PMP (PMBOK® Guide - 6th Edition)

### 1. Định nghĩa & bản chất của Risk Plan

Theo chuẩn *PMBOK® Guide - 6th Edition*, Chapter 11: Project Risk Management, **Risk Management Plan** là một cấu phần của Project Management Plan nhằm mô tả cách thức các hoạt động quản lý rủi ro sẽ được cấu trúc và thực hiện trong suốt vòng đời dự án.

**Bản chất của rủi ro (Project Risk):** Rủi ro là một sự kiện hoặc điều kiện không chắc chắn (uncertain event), mà nếu xảy ra, sẽ mang lại tác động **tích cực (Opportunities - Cơ hội)** hoặc **tiêu cực (Threats - Thách thức)** đến ít nhất một mục tiêu của dự án như phạm vi, tiến độ, chi phí hoặc chất lượng.

Risk Plan không phải chỉ là danh sách các điều xấu có thể xảy ra. Đây là cơ chế quản trị giúp team chủ động nhận diện, ưu tiên, ứng phó và theo dõi cả rủi ro tiêu cực lẫn cơ hội tích cực.

### 2. Quy trình quản lý rủi ro tiêu chuẩn gồm 7 bước

Để làm chủ rủi ro, PM cần điều phối team đi qua chuỗi quy trình khép kín:

1. **Plan Risk Management (11.1):** Lập kế hoạch phương pháp luận, vai trò, lịch review và ngân sách dự phòng.
2. **Identify Risks (11.2):** Nhận diện tất cả các rủi ro có thể xảy ra và ghi nhận vào **Risk Register (Sổ đăng ký rủi ro)**.
3. **Perform Qualitative Risk Analysis (11.3):** Phân tích định tính bằng cách đánh giá xác suất (Probability) và tác động (Impact) để xếp hạng ưu tiên rủi ro.
4. **Perform Quantitative Risk Analysis (11.4):** Phân tích định lượng bằng cách số hóa tác động tài chính hoặc thời gian, ví dụ mô phỏng Monte Carlo, cây quyết định hoặc Expected Monetary Value.
5. **Plan Risk Responses (11.5):** Thiết lập các chiến lược ứng phó cụ thể cho từng rủi ro quan trọng.
6. **Implement Risk Responses (11.6):** Thực thi các hành động ứng phó khi rủi ro xuất hiện hoặc khi trigger đã được kích hoạt.
7. **Monitor Risks (11.7):** Theo dõi liên tục, săn tìm rủi ro mới và đánh giá hiệu quả của các biện pháp ứng phó.

### 3. Các chiến lược ứng phó rủi ro

PMBOK chia rõ hai bộ chiến lược tương ứng với tính chất của rủi ro.

#### Đối với rủi ro tiêu cực (Threats)

- **Escalate (Leo thang):** Chuyển rủi ro lên cấp quản lý cao hơn như Program, Portfolio hoặc Sponsor vì nó vượt quá thẩm quyền của PM hoặc ảnh hưởng ngoài phạm vi dự án.
- **Avoid (Né tránh):** Hành động nhằm loại bỏ hoàn toàn mối đe dọa hoặc bảo vệ dự án khỏi tác động của nó. Ví dụ: thay đổi công nghệ để tránh lỗi đã biết.
- **Transfer (Chuyển giao):** Chuyển trách nhiệm chịu tác động và chi phí xử lý cho bên thứ ba. Ví dụ: mua bảo hiểm, thuê ngoài hoặc ký hợp đồng fixed-price.
- **Mitigate (Giảm thiểu):** Thực hiện hành động sớm nhằm giảm xác suất xảy ra hoặc giảm mức độ thiệt hại của rủi ro. Ví dụ: làm prototype kiểm thử trước.
- **Accept (Chấp nhận):** Không chủ động thay đổi kế hoạch, ngoại trừ lập quỹ dự phòng (Contingency Reserve) hoặc chuẩn bị hành động nếu rủi ro thực sự xảy ra.

#### Đối với rủi ro tích cực (Opportunities)

- **Escalate (Leo thang):** Chuyển cấp trên xử lý nếu cơ hội vượt tầm kiểm soát của dự án.
- **Exploit (Khai thác):** Đảm bảo 100% cơ hội sẽ xảy ra. Ví dụ: giao nhân sự giỏi nhất vào task để hoàn thành sớm nhằm nhận thưởng milestone.
- **Share (Chia sẻ):** Hợp tác với bên thứ ba để cùng khai thác cơ hội. Ví dụ: liên doanh, đối tác tích hợp hoặc chiến dịch đồng tài trợ.
- **Enhance (Nâng cao):** Gia tăng xác suất hoặc tác động tích cực của cơ hội.
- **Accept (Chấp nhận):** Sẵn sàng đón nhận nếu cơ hội tự đến, nhưng không chủ động theo đuổi.

---

## II. Ví dụ & minh họa thực tế

### Ví dụ: Trích lục Risk Register mẫu cho Module eKYC thuộc Dự án "Epic Center"

Dưới đây là cách cấu trúc một Risk Register thực chiến sử dụng **Ma trận Xác suất & Tác động (Probability and Impact Matrix)** tính điểm từ 1 đến 5.

| Mã Risk | Mô tả rủi ro (Sự kiện -> Hệ quả) | Xác suất (1-5) | Tác động (1-5) | Điểm rủi ro (P x I) | Chiến lược ứng phó | Hành động cụ thể (Mitigation Plan) | Risk Owner |
| --- | --- | ---: | ---: | ---: | --- | --- | --- |
| **RSK-01** | **[Threat]** API nhận diện khuôn mặt của đối tác gặp sự cố nghẽn mạch đột xuất trong giờ cao điểm, dẫn đến khách hàng không thể tạo tài khoản eKYC. | 3 | 5 | **15** (Cao) | **Mitigate** | Phát triển thêm module dự phòng kết nối song song với 1 nhà cung cấp API eKYC thứ 2 làm phương án fallback. | Tech Lead |
| **RSK-02** | **[Threat]** Apple cập nhật chính sách bảo mật hệ điều hành iOS mới làm xung đột với SDK chụp ảnh căn cước công dân hiện tại của dự án. | 2 | 4 | **8** (Trung bình) | **Avoid** | Đội Mobile cập nhật phiên bản iOS Beta mới nhất để chạy regression test trước khi Apple phát hành chính thức 1 tháng. | Mobile Lead |
| **RSK-03** | **[Opportunity]** Nhà mạng viễn thông tung ra chương trình tài trợ miễn phí data cho người dùng truy cập các app tài chính mới, giúp tăng 40% user đăng ký. | 4 | 3 | **12** (Cao) | **Enhance** | Phối hợp với Marketing đẩy ngân sách quảng cáo đúng vào tuần diễn ra chương trình để tối đa hóa lượng download. | PO |

### Thang điểm ưu tiên gợi ý

| Điểm P x I | Mức độ | Cách xử lý khuyến nghị |
| ---: | --- | --- |
| 1-4 | Thấp | Theo dõi định kỳ, chưa cần hành động lớn |
| 5-9 | Trung bình | Có owner và hành động ứng phó cơ bản |
| 10-15 | Cao | Cần mitigation plan rõ ràng, review mỗi Sprint |
| 16-25 | Rất cao | Escalation, contingency plan và theo dõi sát bởi PM/Sponsor |

---

## III. Case study dẫn chứng thực tế

### Thảm kịch sập hệ thống thanh toán và chiếc phao cứu sinh mang tên Contingency & Management Reserve

**Bối cảnh:** Một dự án tích hợp hệ thống Core ngân hàng cho cổng cho thuê phòng Epic Center. Trong giai đoạn Planning, PM xác định được rủi ro: *hệ thống có thể bị quá tải dữ liệu (Database Overload) khi đồng bộ hóa lịch phòng diện rộng*. PM đã lập quỹ dự phòng rủi ro đã nhận diện (**Contingency Reserve**) trị giá 5,000 USD và 3 ngày công để dự phòng nâng cấp RAM server.

**Vấn đề phát sinh:**

1. Khi Go-live, hệ thống không bị quá tải database, nhưng một sự kiện bất khả kháng hoàn toàn nằm ngoài dự tính (Unknown-Unknown) xảy ra: một cuộc tấn công từ chối dịch vụ (DDoS) quy mô lớn nhắm vào dải IP của máy chủ lưu trữ.
2. Hệ thống tê liệt hoàn toàn. Do đây là rủi ro không có trong Risk Register, PM không được phép tự ý dùng quỹ **Contingency Reserve** cho việc này.

**Giải pháp khắc phục:**

1. PM kích hoạt quy trình phê duyệt khẩn cấp để xin cấp quỹ **Management Reserve**, tức quỹ dự phòng quản lý dành cho rủi ro chưa nhận diện và do Ban Giám đốc kiểm soát.
2. Ngân sách được duyệt lập tức để thuê dịch vụ chống DDoS của Cloudflare cứu nguy cho hệ thống.

**Bài học rút ra:**

- **Contingency Reserve:** PM quản lý, nằm trong Cost Baseline, dùng cho rủi ro đã biết nhưng chưa chắc xảy ra (Known-Unknowns).
- **Management Reserve:** Cấp trên quản lý, nằm ngoài Cost Baseline nhưng thuộc Project Budget, dùng cho rủi ro chưa biết (Unknown-Unknowns).
- Risk Plan cần quy định rõ ngưỡng nào PM được quyền kích hoạt dự phòng, ngưỡng nào phải escalation lên Sponsor hoặc Steering Committee.

---

## IV. Tips & điều lưu ý thực chiến cho PM/PO

### 1. Tránh mô tả rủi ro mơ hồ

Đừng viết rủi ro kiểu: *"Thiếu nhân sự"*. Hãy viết theo cấu trúc:

```text
[Nguyên nhân] -> dẫn đến [Sự kiện] -> gây ra [Hệ quả]
```

Ví dụ chuẩn:

> "Do thị trường cạnh tranh gay gắt, dẫn đến lập trình viên Backend chủ chốt có thể nghỉ việc giữa chừng, gây ra việc chậm tiến độ bàn giao Module E-Coffer 2 tuần."

### 2. Cập nhật Risk Register trong mỗi Sprint Retrospective

Rủi ro không phải là tài liệu làm xong ở giai đoạn Planning rồi cất tủ. Sau mỗi Sprint, PM/SM nên cùng team review:

- Rủi ro nào đã qua đi và có thể đóng lại
- Rủi ro nào mới xuất hiện
- Trigger nào đã bị kích hoạt
- Biện pháp ứng phó có thực sự hiệu quả không
- Có cần cập nhật probability, impact, owner hoặc contingency plan không

### 3. Xây dựng văn hóa "không đổ lỗi" (Blameless Risk Culture)

Khuyến khích các thành viên chủ động báo cáo rủi ro kỹ thuật sớm. Nếu phạt nhân sự khi họ báo cáo rủi ro, họ sẽ che giấu nó cho đến khi dự án thực sự gặp sự cố lớn, lúc đó PM sẽ không còn thời gian để cứu vãn.

### 4. Phân biệt risk, issue và assumption

- **Risk:** Điều chưa chắc xảy ra, nhưng nếu xảy ra sẽ ảnh hưởng đến mục tiêu dự án.
- **Issue:** Vấn đề đã xảy ra và cần xử lý ngay.
- **Assumption:** Giả định đang được dùng để lập kế hoạch, cần theo dõi vì nếu sai có thể biến thành risk hoặc issue.

---

## V. Template Risk Plan nên dùng

| Trường thông tin | Nội dung cần có |
| --- | --- |
| Risk Methodology | Cách nhận diện, phân tích, xếp hạng và theo dõi rủi ro |
| Roles & Responsibilities | PM, Risk Owner, Sponsor, Tech Lead, QA, PO |
| Risk Categories | Technical, schedule, cost, vendor, compliance, security, operations |
| Probability Scale | Thang điểm xác suất, ví dụ 1-5 |
| Impact Scale | Thang điểm tác động theo tiến độ, chi phí, chất lượng, phạm vi |
| Probability-Impact Matrix | Cách tính điểm và ngưỡng ưu tiên |
| Risk Register | Danh sách rủi ro, owner, trigger, strategy, action plan |
| Risk Response Strategy | Escalate, avoid, transfer, mitigate, accept, exploit, share, enhance |
| Contingency Reserve | Quỹ/nguồn lực cho rủi ro đã nhận diện |
| Management Reserve | Cơ chế xin cấp quỹ cho rủi ro chưa nhận diện |
| Monitoring Cadence | Tần suất review, ví dụ mỗi Sprint Retrospective hoặc weekly project review |
| Escalation Path | Khi nào và báo cho ai nếu rủi ro vượt thẩm quyền PM |
| Reporting Format | Cách báo cáo top risks cho PMO, Sponsor và Steering Committee |

---

## VI. Tài liệu & nguồn tham khảo

### 1. Chuẩn quốc tế & sách gối đầu giường

- *A Guide to the Project Management Body of Knowledge (PMBOK® Guide) - 6th Edition*, Chapter 11: Project Risk Management.
- *Practical Project Risk Management: The ATOM Methodology* - David Hillson.

### 2. Blog quản trị dự án uy tín

- PMI.org: *The Risk Management Framework and Best Practices*.
- ProjectManager.com: *How to Create a Risk Management Plan (Template Included)*.

### 3. Video / YouTube hữu ích

- Search keyword: *"Project Risk Management Tutorial - PMP Exam Prep"*.
- Search keyword: *"Contingency Reserve vs Management Reserve Explained clearly"*.
