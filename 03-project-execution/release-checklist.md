# Release Checklist

Checklist kiểm soát trước, trong và sau khi phát hành sản phẩm hoặc deliverable.

## Mục tiêu

- Giảm rủi ro lỗi production, thiếu tài liệu hoặc thiếu phê duyệt.
- Bảo đảm release có kế hoạch rollback, monitoring và owner rõ ràng.
- Tạo bằng chứng kiểm soát chất lượng cho PM, PO, QA, Tech Lead và Operations.

## Pre-release

- Scope release đã được chốt.
- Test cases quan trọng đã pass.
- Regression test đã hoàn tất.
- Security review đã hoàn tất nếu cần.
- Migration script đã được review.
- Release notes đã sẵn sàng.
- Rollback plan đã được phê duyệt.
- Stakeholder đã được thông báo.

## Release

- Người phụ trách release đã xác nhận.
- Thời gian triển khai đã được thông báo.
- Backup hoặc snapshot đã hoàn tất nếu cần.
- Monitoring dashboard đã bật.
- Smoke test sau deploy đã hoàn tất.

## Post-release

- Theo dõi lỗi trong hypercare window.
- Ghi nhận issue phát sinh vào Issue Log.
- Cập nhật trạng thái release cho stakeholder.
- Tổng kết bài học kinh nghiệm nếu có sự cố đáng kể.
