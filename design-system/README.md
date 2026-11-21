# DQHPC — Design System

Hệ giao diện cho các webapp nội bộ của CTCP Đại Quang HPC (quản lý việc, hồ sơ thiết kế, dashboard dự án). Phát triển từ hệ Taskory (clone giao diện Linear), giữ nguyên tinh thần **mật độ cao, chiều sâu bằng viền tóc, màu = thông tin**, nhưng thêm một màu thương hiệu: **đỏ DQHPC**.

> Đỏ là hành động. Mọi màu khác là trạng thái.

## 1. Thay đổi so với Taskory

| Hạng mục | Taskory | DQHPC | Lý do |
|---|---|---|---|
| `primary` | màu mực (#18181b / #fafafa) | đỏ `#c8102e` / `#dc2626` | yêu cầu màu chủ đạo đỏ |
| Vạch đứng ở header | `orange-500` (ngoại lệ ngoài token) | `primary` | xoá ngoại lệ duy nhất của luật "màu = trạng thái" |
| `status-blocked` | đỏ `#eb5757` | cam `#f97316` | tránh lẫn với đỏ thương hiệu |
| `label-urgent` | đỏ | rose `#e11d48`, luôn kèm chữ "Gấp" | vẫn đọc là "nóng", nhưng khác sắc độ nút chính |
| `destructive` | nút nền đỏ đặc | nút outline chữ đỏ sẫm `#991b1b` | nút chính đã là đỏ đặc — hai nút không được giống nhau |
| Mục đang chọn | nền `sidebar-accent` xám | `primary-soft` + chữ `primary-text` | thương hiệu xuất hiện ở điểm định hướng |
| Biến thể giao diện | pure-light, magic-blue, classic-dark | chỉ Sáng / Tối | rút gọn cho bản đầu; thêm sau bằng cách ghi đè token |

## 2. Nguyên tắc màu

**Đỏ chỉ ở bề mặt hành động và định hướng.** `primary` được phép xuất hiện ở đúng 4 chỗ:

1. Nền nút chính (`button-primary`) — tối đa **một** nút chính mỗi màn hình.
2. Vạch đứng `|` ở `page-header` và vạch trái 2px của mục sidebar đang chọn.
3. Nền `primary-soft` + chữ `primary-text` cho mục đang chọn (sidebar, tab, hàng được chọn).
4. Vòng focus (`ring`).

**Không** dùng `primary` cho: chấm trạng thái, chip nhãn, khối lịch, biểu đồ, icon trang trí, nền khối lớn. Một màn hình có quá 5% diện tích đỏ là sai.

**Màu = trạng thái.** Ba nhóm ngữ nghĩa giữ nguyên vai trò:

- `status-*` (7) — luồng backlog → to-do → in-progress → (blocked | in-review) → done | canceled. Hiển thị bằng `status-dot` 6px.
- `label-*` (4) — mức độ gấp: Gấp · Quan trọng · Thường · Khi rảnh. Luôn chấm + chữ.
- `schedule-*` (5) — tone khối lịch, xoay vòng sky → violet → amber → pink → emerald. Sọc chéo = nền × 0.95.

Mức ưu tiên (Urgent/High/Medium/Low) phân biệt bằng **hình icon**, không bằng màu.

## 3. Chiều sâu

| Tầng | Cách làm | Dùng ở |
|---|---|---|
| 0 — flat | `background` | nền trang |
| 1 — raised | `container` + viền 1px `border`, bo `radius-xl` | khối lớn Dashboard |
| 2 — inset | `background` + viền 1px trên nền container, bo `radius-lg` | thẻ task trong khối |
| 3 — overlay | `popover` + `shadow-overlay` | dialog, dropdown — tầng DUY NHẤT có bóng |
| focus | vòng 3px `ring` | nút, input đang focus |

Ở theme sáng, tầng 2 tối hơn tầng 1 (thẻ #f7f7f7 trong khối #ffffff) — cố ý, giữ cách của Linear.

## 4. Chữ

Một font: **Montserrat** (Google Fonts, subset latin + vietnamese), fallback `system-ui, sans-serif`. Cỡ chủ đạo `body-sm` 12px; `body` 14px chỉ cho nội dung chính của hàng. Độ đậm mặc định **500** (đọc được ở 12px), 600 cho tiêu đề, 700 rất dè (tên app, tên khối). Tracking âm chỉ ở tiêu đề; duy nhất `eyebrow` dùng +0.14em.

## 5. Khoảng cách, bo góc, bố cục

- Thang 4px: `space-xxs` 4 · `xs` 6 · `sm` 8 · `md` 12 · `lg` 16 · `xl` 20 · `xxl` 24. Không bậc nào lớn hơn 24px — khoảng trống để tách tầng, không để "thở".
- Bo góc: `radius-md` 8px cho nút/input, `radius-lg` 10px cho thẻ, `radius-xl` 14px cho khối lớn, `radius-full` cho mọi thứ nhỏ và tròn. Không có bậc 20–24px.
- Khung app: sidebar 248px (thu gọn 48px, mobile sheet 260px) · header 40px · hàng danh sách 44px · lề nội dung 16px.
- Lưới Dashboard: `minmax(0,1fr) 340px 340px`, gap 16px; dưới 1280px rời về một cột.

## 6. Chuyển động

- `color-shift`: color, background, box-shadow 150ms — mặc định nút/input/badge.
- `overdue-pulse`: 5s, `cubic-bezier(0.4,0,0.6,1)`, chạy trên **box-shadow** (spread tối đa 4px), không dùng scale.
- `prefers-reduced-motion`: tắt animation, thay bằng viền tĩnh 3px `overdue-border`.

## 7. Giọng văn giao diện

Tiếng Việt, ngắn, động từ đứng đầu: "Tạo việc", "Gửi duyệt", "Xuất báo cáo". Thuật ngữ chuyên ngành giữ nguyên khi rõ nghĩa hơn (WBS, KPI, BVTC). Không dấu chấm than, không emoji trong giao diện.

## 8. Do / Don't

**Do**
- Một nút `primary` mỗi màn hình, cho việc mà trang đó tồn tại để làm.
- Dùng `container` + viền cho mọi khối lớn mới.
- Lấy màu trạng thái/nhãn từ token — đừng chọn màu mới.
- Kiểm cả theme Sáng và Tối, và mốc 1280px, khi sửa số đo Dashboard.

**Don't**
- Đừng dùng đỏ `primary` làm chấm trạng thái, nền khối, hay màu biểu đồ.
- Đừng làm nút xoá nền đỏ đặc — dùng `destructive` dạng outline + hộp xác nhận.
- Đừng thêm `shadow` vào thẻ hay khối để "cho nổi".
- Đừng animate `transform: scale` trên hàng danh sách.
- Đừng phân biệt mức ưu tiên bằng màu.

## 9. Dùng hệ này

- Token: `project/tokens.json` (trang tự sinh `tokens.css`, biến CSS dạng `--primary`, `--space-lg`, `--radius-md`…; theme qua `data-theme="light|dark"` trên `<html>`).
- Lớp CSS component: `project/components/bundle.css`, tiền tố `dq-`. Bản đầu là HTML + CSS thuần, chưa có bundle React.
- Mỗi component có `README.md` (hướng dẫn) và `preview.html` (mẫu chạy được) trong `components/<Tên>/`.

## 10. Còn thiếu (Known gaps)

- **Chưa có logo DQHPC** — header đang dùng chữ. Khi anh cấp file logo (SVG), thêm vào nhóm tài sản `Logos` và cập nhật màu đỏ theo đúng mã màu nhận diện chính thức.
- Mã đỏ `#c8102e` là đề xuất, chưa đối chiếu bộ nhận diện thương hiệu của công ty.
- Chưa có component: Calendar, Schedule column, Dialog, Dropdown, Avatar group, Hero banner.
- Chưa có token trạng thái lỗi form (`aria-invalid`) ngoài `destructive`.
