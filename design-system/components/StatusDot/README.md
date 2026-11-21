# StatusDot

Chấm tròn 6px báo trạng thái công việc — đơn vị mang màu nhỏ nhất và phổ biến nhất của hệ.

- Lớp: `dq-dot dq-dot-<trạng thái>`; kèm chữ dùng `dq-status`.
- Luồng: backlog → todo → in-progress → (blocked | in-review) → done | canceled.
- `blocked` là **cam** (`status-blocked`), không đỏ — đỏ đã thuộc về thương hiệu.
- Không bao giờ tô chấm bằng `primary`.
- Chấm đứng một mình (không chữ) chỉ được dùng ở nơi có tooltip hoặc cột tiêu đề nói rõ nghĩa.
