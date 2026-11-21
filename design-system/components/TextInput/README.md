# TextInput

Ô nhập một dòng: nền trong suốt, viền 1px `input`, bo `radius-md`, cao 36px, lề 4px/12px.

- Lớp: `dq-input`; bọc nhãn bằng `dq-field`.
- Placeholder màu `muted-foreground`.
- Focus: viền đổi sang `primary` + vòng 3px `ring` (đỏ 40%).
- Luôn có `<label>` hiển thị — viền tóc quá nhạt để tự làm tín hiệu.
- Lỗi: hiện dòng chữ `destructive` 12px dưới ô; chưa có token viền lỗi riêng (xem Known gaps).
