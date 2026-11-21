# dq-project

## 1. Dự án này là gì

**dq-project** (quản lý dự án) là web app **nội bộ** của công ty tư vấn thiết kế cầu đường / hạ tầng kỹ thuật, quản lý luồng thông tin và **thủ tục hồ sơ pháp lý** của các dự án đầu tư công mà công ty tư vấn cho chủ đầu tư nhà nước.

**Đã xác nhận (đang brainstorm, chưa có spec):**
*   **Who**: nhân sự nội bộ công ty (8 người → mục tiêu 30). Cần một góc nhìn **tổng quan cho chủ đầu tư** (không đi chi tiết).
*   **Why**: bảo đảm thủ tục pháp lý; văn bản từ nhiều cơ quan/CĐT, biên bản bàn giao, biên bản hiện trường dễ thất lạc; khâu làm việc pháp lý với cơ quan chậm nhất.
*   **What**: vòng đời dự án — TKCS (khảo sát → thiết kế → thẩm tra → lấy ý kiến cơ quan → thẩm định Sở XD) → BVTC + dự toán (thẩm tra → thẩm định) → phát hành hồ sơ → giám sát tác giả & công văn xử lý kỹ thuật khi thi công.
*   **Quy mô**: 5 dự án → 15; khoảng 100 văn bản/tháng.
*   **Căn cứ pháp lý**: Luật 135/2025 và các nghị định kèm theo.

Công nghệ: chưa chốt cho bài toán này.

## 2. Cấu trúc folder

| Folder | Dùng để |
|---|---|
| `.claude/skills/` | Skill riêng của project (hiện có: `brainstorm`) |
| `docs/1-discovery/` | Tư liệu đầu vào: bối cảnh, 5W1H, file/quy trình đang dùng |
| `docs/2-spec/` | `spec.md` — app làm được gì (đầu ra của skill `brainstorm`) |
| `design-system/` | DQHPC Design System: token màu/khoảng cách, CSS component (`dq-`), mẫu `preview.html` từng component. `globals.css` để tạm ở đây — chuyển vào `app/` khi dựng app |
| `docs/3-prototype/` | Bản thử giao diện |
| `docs/4-plan/` | Kế hoạch dựng app: chia việc, thứ tự làm |
| `docs/5-release/` | Ghi chú phát hành, hướng dẫn dùng, danh sách kiểm trước khi bàn giao |
| `app/` | Mã nguồn web app |
| `MEMORY.md` | Ghi nhớ quyết định và bối cảnh qua các buổi làm việc |

## 3. Quy ước làm việc

1. **Đi đúng thứ tự giai đoạn.** Chưa có `docs/2-spec/spec.md` được duyệt thì không viết code trong `app/`. Yêu cầu mới ngoài spec → cập nhật spec trước, rồi mới code.
2. **Spec là nguồn sự thật.** Code, giao diện, kế hoạch phải khớp spec; dùng đúng "Chữ của app" đã chốt trong spec (tên thứ chính, trạng thái, vai). Chỗ chưa rõ → hỏi, không tự đoán.
3. **Làm từng phần nhỏ, kiểm được.** Mỗi lần chỉ làm một chức năng (F) và kiểm theo tiêu chí chấp nhận của F đó trong spec trước khi sang phần sau. Quyết định quan trọng ghi vào `MEMORY.md`.

## 4. Quy tắc giao diện — BẮT BUỘC đọc trước khi viết UI

Dự án dùng **DQHPC Design System** trong thư mục `design-system/`. Trước khi tạo hay sửa bất kỳ màn hình/component nào:

1. Đọc `design-system/README.md` (nguyên tắc) và `design-system/components/<Tên>/README.md` của component liên quan.
2. Lấy màu, khoảng cách, bo góc từ token (`design-system/tokens.css`, map vào Tailwind qua `globals.css`). KHÔNG tự đặt mã hex mới.
3. Nếu component đã có mẫu trong `design-system/components/<Tên>/preview.html`, bám theo cấu trúc và số đo của mẫu đó.

**Luật cứng:**

- **Đỏ (`primary`) chỉ ở 4 chỗ**: nút chính (tối đa 1 nút/màn hình), vạch đứng ở header, mục sidebar đang chọn (`bg-primary-soft text-primary-text` + vạch trái 2px `bg-primary`), vòng focus. Không dùng đỏ cho chấm trạng thái, chip, biểu đồ, nền khối.
- **Màu = trạng thái**: chỉ dùng `status-*`, `label-*`, `schedule-*`. Không thêm màu trang trí.
- **Nút xoá** = outline chữ `text-destructive border-destructive`, không nền đặc, luôn có hộp xác nhận.
- **Chiều sâu bằng viền**: khối lớn = `bg-container border rounded-xl p-5`; thẻ con = `bg-background border rounded-lg p-4`. KHÔNG thêm `shadow-*`, trừ popover/dialog/dropdown (`shadow-xl`).
- **Mật độ cao**: chữ mặc định `text-xs` (12px) đậm `font-medium`; `text-sm` (14px) cho nội dung chính của hàng. Khoảng cách tối đa 24px.
- **Bo góc**: nút/input `rounded-md`; thẻ `rounded-lg`; khối lớn `rounded-xl`; chip/avatar/nút icon `rounded-full`.
- **Kích thước khung**: sidebar 248px, header 40px, hàng danh sách 44px, lưới Dashboard `grid-cols-[minmax(0,1fr)_340px_340px] gap-4` (≥1280px), 1 cột dưới 1280px.
- Không `transform: scale` trên hàng/thẻ. Animation quá hạn chạy trên box-shadow, tôn trọng `prefers-reduced-motion`.
- Mức ưu tiên phân biệt bằng hình icon, không bằng màu.
- Giao diện tiếng Việt, nhãn nút bắt đầu bằng động từ, không emoji, không dấu chấm than.
