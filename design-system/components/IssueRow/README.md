# IssueRow

Hàng việc trong danh sách: cao 44px (đạt ngưỡng chạm), lề ngang 24px, chữ 14px đậm 600; không viền, không bo — tách bằng khoảng cách và hover.

- Lớp: `dq-row` trong `dq-list`; phần tử con: `dq-row-id`, `dq-dot`, `dq-row-title`, chip, `dq-row-date`.
- Hover: nền `sidebar` 50%. Đang chọn (`is-selected`): nền `primary-soft`.
- Co lại theo màn hình, bỏ dần từ ngoài vào: nhãn (<1024px), avatar, ngày hạn, mã việc (<640px).
- Không animate scale.
