# RACI trong giai đoạn Khởi động

## Phần 1: Khung kiến thức chuyên sâu về Ma trận RACI

Trong quản lý dự án theo chuẩn PMP, **Ma trận RACI** (hay còn gọi là Ma trận phân bổ trách nhiệm - Responsibility Assignment Matrix - RAM) là công cụ được sử dụng để xác định rõ ràng vai trò và trách nhiệm của các thành viên hoặc phòng ban đối với từng đầu việc, gói công việc (Work Package) hoặc kết quả bàn giao (Deliverables).

RACI là viết tắt của 4 dung lượng trách nhiệm:

- **R - Responsible (Người thực hiện):** Người trực tiếp bắt tay vào làm công việc. Phải có ít nhất một chữ **R** cho mỗi đầu việc. Có thể có nhiều người cùng làm (nhiều chữ R).
- **A - Accountable (Người chịu trách nhiệm tối cao / Người duyệt):** Người sở hữu kết quả cuối cùng, có quyền quyết định và phê duyệt. **Quy tắc vàng của PMP: Chỉ có duy nhất một chữ A cho mỗi hàng việc.** Nếu có hơn một chữ A, quyền lực bị chồng chéo, dễ dẫn đến đổ lỗi khi xảy ra sự cố.
- **C - Consulted (Người được tham vấn):** Các chuyên gia, cố vấn hoặc bên liên quan có chuyên môn sâu. Họ cung cấp ý kiến, dữ liệu đầu vào *trước* khi công việc được thực hiện hoặc phê duyệt. Tương tác 2 chiều.
- **I - Informed (Người được thông báo):** Những người cần biết kết quả hoặc tiến độ sau khi công việc đã hoàn thành. Tương tác 1 chiều, không cần lấy ý kiến.

---

# Phần 2: Bảng Ma trận RACI Dự án (Project RACI Matrix)

**Tên dự án:** Phát triển Nền tảng Kỹ thuật số Tích hợp Dịch vụ Toàn diện & Trợ lý Ảo AI

**Giai đoạn:** 01 Project Initiation (Bao gồm các kết quả bàn giao cốt lõi của cả giai đoạn)

**Phiên bản:** 1.0

| Các hoạt động & Kết quả bàn giao chính (Activities / Deliverables) | Nhà tài trợ (Sponsor) | Giám đốc Tài chính (CFO) | Quản lý Dự án (PM / PO) | Trưởng phòng Vận hành (Ops Head) | Kiến trúc sư hệ thống (Tech Lead) | Chuyên gia UI/UX | Đối tác bên thứ 3 (Vendors) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **1. Xây dựng Luận chứng Kinh doanh (Business Case)** | **A** | **C** | **R** | **C** | **I** | **I** | **I** |
| **2. Tuyên bố Tầm nhìn Dự án (Project Vision)** | **C** | **I** | **A / R** | **C** | **I** | **C** | **I** |
| **3. Xây dựng & Phê duyệt Điều lệ Dự án (Project Charter)** | **A** | **C** | **R** | **I** | **I** | **I** | **I** |
| **4. Xác định & Phân tích các bên liên quan (Stakeholder Analysis)** | **I** | **I** | **A / R** | **C** | **C** | **I** | **I** |
| **5. Thiết lập Ma trận Truyền thông (Communication Matrix)** | **I** | **I** | **A / R** | **I** | **C** | **I** | **C** |
| **6. Phân rã Yêu cầu Hệ thống cấp cao (High-Level Scope)** | **I** | **I** | **A** | **C** | **R** | **R** | **C** |
| **7. Đánh giá tính khả thi kỹ thuật (AI Integration, n8n, eKYC)** | **I** | **I** | **C** | **I** | **A / R** | **I** | **R** |
| **8. Ký kết hợp đồng thương mại & cam kết dịch vụ (SLA)** | **A** | **R** | **C** | **I** | **C** | **I** | **R** |
| **9. Tổ chức họp khởi động dự án chính thức (Kick-off Meeting)** | **I** | **I** | **A / R** | **I** | **I** | **I** | **I** |

---

## Phần 3: Nguyên tắc Rà soát và Kiểm tra Ma trận RACI (Analysis Rules)

Để đảm bảo ma trận RACI không chỉ nằm trên giấy mà có tính thực thi cao, PM cần dùng kỹ thuật rà soát theo hai chiều dọc và ngang:

### 1. Rà soát theo Hàng Ngang (Phát hiện lỗ hổng quy trình)

- **Hàng không có chữ A:** Cực kỳ nguy hiểm. Đầu việc này không có người chịu trách nhiệm tối cao, khi trễ hạn hoặc lỗi sẽ không ai giải quyết. *Sửa: Phải bổ sung ngay 1 chữ A.*
- **Hàng có nhiều chữ A:** Gây xung đột quyền lực trong việc đưa ra quyết định. *Sửa: Rút gọn lại chỉ để 1 người nắm chữ A.*
- **Hàng có quá nhiều chữ R:** Có quá nhiều người thực hiện cùng một việc dễ dẫn đến tình trạng "cha chung không ai khóc". *Sửa: Cần chia nhỏ đầu việc ra thành các tác vụ cụ thể hơn.*
- **Hàng không có chữ R:** Có người duyệt (A) nhưng không có người làm. *Sửa: Chỉ định nhân sự thực thi.*

### 2. Rà soát theo Cột Dọc (Phát hiện quá tải nhân sự)

- **Cột có quá nhiều chữ A hoặc R đối với một người:** Nhân sự đó đang bị quá tải (Overloaded) hoặc đang ôm đồm việc vi mô. Đặc biệt nếu PM có quá nhiều chữ R, PM đang sa đà vào làm kỹ thuật thay vì quản lý. *Sửa: Ủy quyền (Delegate) bớt chữ R cho các thành viên trong nhóm.*
- **Cột không có chữ nào hoặc quá ít:** Nhân sự đó đang bị lãng phí nguồn lực hoặc bị gạt ra khỏi các hoạt động cốt lõi của dự án. *Sửa: Xem xét lại vai trò của họ.*

---

*Ma trận RACI này là mảnh ghép hoàn chỉnh tiếp theo giúp chốt lại sơ đồ tổ chức, quyền lực và trách nhiệm cốt lõi, loại bỏ hoàn toàn sự mập mờ về trách nhiệm giữa team Sản phẩm (Product), Kỹ thuật (Tech) và Vận hành (Operations) ngay từ vạch xuất phát.*
