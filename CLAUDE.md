# app-QLDA

## 1. Dự án này là gì

**QLDA (Quản lý dự án)** là web app **nội bộ** của công ty tư vấn thiết kế cầu đường / hạ tầng kỹ thuật, quản lý luồng thông tin và **thủ tục hồ sơ pháp lý** của các dự án đầu tư công mà công ty tư vấn cho chủ đầu tư nhà nước.

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
| `docs/3-prototype/` | Bản thử giao diện, quy ước hình thức (`DESIGN.md`) |
| `docs/4-plan/` | Kế hoạch dựng app: chia việc, thứ tự làm |
| `docs/5-release/` | Ghi chú phát hành, hướng dẫn dùng, danh sách kiểm trước khi bàn giao |
| `app/` | Mã nguồn web app |
| `MEMORY.md` | Ghi nhớ quyết định và bối cảnh qua các buổi làm việc |

## 3. Quy ước làm việc

1. **Đi đúng thứ tự giai đoạn.** Chưa có `docs/2-spec/spec.md` được duyệt thì không viết code trong `app/`. Yêu cầu mới ngoài spec → cập nhật spec trước, rồi mới code.
2. **Spec là nguồn sự thật.** Code, giao diện, kế hoạch phải khớp spec; dùng đúng "Chữ của app" đã chốt trong spec (tên thứ chính, trạng thái, vai). Chỗ chưa rõ → hỏi, không tự đoán.
3. **Làm từng phần nhỏ, kiểm được.** Mỗi lần chỉ làm một chức năng (F) và kiểm theo tiêu chí chấp nhận của F đó trong spec trước khi sang phần sau. Quyết định quan trọng ghi vào `MEMORY.md`.
