# LabelChip

Chip nhãn mức độ gấp trên thẻ task: viền 1px, bo `radius-full`, lề 2px/10px, chấm 6px mang màu nhãn.

- Lớp: `dq-chip dq-chip-<urgent|important|normal|whenever>` chứa `<span class="dq-dot">` + chữ.
- Nhãn chia theo mức độ gấp, không theo loại việc: Gấp · Quan trọng · Thường · Khi rảnh.
- `label-urgent` là rose `#e11d48` — vẫn "nóng" nhưng khác sắc đỏ thương hiệu; luôn kèm chữ, không dùng chấm trơn.
- Giá trị lưu trong dữ liệu là khoá (`urgent`…), component ánh xạ sang token — đừng lưu hex.
- **count-chip** (`dq-count`): vòng 24px nền `muted`, chữ 12px đậm 600, đặt cạnh tên khối hoặc mục sidebar.
