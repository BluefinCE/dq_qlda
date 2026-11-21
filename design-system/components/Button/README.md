# Button

Nút hành động, 5 biến thể và 6 bậc cao; chỉ một nút `primary` đỏ mỗi màn hình.

- **primary** (`dq-btn dq-btn-primary`) — nền `primary`, chữ `primary-foreground`, hover `primary-hover`. Dành cho việc chính của trang: "Tạo việc", "Gửi duyệt".
- **secondary** — nền `muted`. Hành động phụ có trọng lượng.
- **outline** — nền `background` + viền `input`; hover `accent`.
- **ghost** — không nền, hover `accent`. Loại xuất hiện nhiều nhất trên thanh công cụ.
- **destructive** — outline chữ + viền `destructive` (đỏ sẫm). KHÔNG nền đặc để không trùng nút chính. Luôn đi kèm hộp xác nhận.
- **Cỡ**: xxs 24 · xs 28 (`dq-btn-xs`) · sm 32 (`dq-btn-sm`) · default 36 · lg 40 (`dq-btn-lg`) · icon 36 tròn (`dq-btn-icon`). xs/xxs chỉ dùng trên thanh công cụ desktop.
- **Focus**: vòng 3px `ring`. Chữ: `body` 14px đậm 500, bo `radius-md`.

Người dùng cung cấp: nhãn bắt đầu bằng động từ, icon 16px tuỳ chọn, `aria-label` cho nút chỉ có icon.
