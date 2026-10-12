# Ghi nhận brainstorm — app QLDA

> Cập nhật: 2026-10-12. Chỉ ghi điều **đã xác nhận**; giả định và câu hỏi mở tách riêng ở cuối.

## Bối cảnh

- App **nội bộ** công ty tư vấn thiết kế cầu đường / hạ tầng kỹ thuật, tư vấn cho chủ đầu tư (CĐT) nhà nước. Mục tiêu: **bảo đảm thủ tục hồ sơ pháp lý**, không thất lạc văn bản.
- Quy mô: 5 dự án → 15; 8 người → 30; ~100 văn bản/tháng.
- Hiện trạng: công văn nhận qua Zalo cá nhân, không vào sổ, không đánh số; sếp giao việc qua Zalo; chưa có quy trình phát hành công văn đi.
- Chỗ đau: khâu pháp lý với cơ quan chậm nhất; văn bản từ nhiều cơ quan/CĐT, biên bản bàn giao, biên bản hiện trường dễ thất lạc (nhất là giai đoạn thi công).
- CĐT **không có tài khoản**; cần màn **tổng quan cho CĐT** (không chi tiết) để nội bộ dùng khi họp hoặc xuất gửi.

## Vai trò

| Vai | Ai | Quyền |
|---|---|---|
| Admin | anh Thông (kiêm leader) | cài đặt chung (quy tắc số, hiển thị dự án), nhận thông báo, nhắc số treo, có quyền đóng văn bản |
| Sếp tổng | 1 người | xem như Admin, không thao tác |
| Leader | anh Thông + 2 leader | quản lý dự án mình, giao việc, đóng văn bản, xác nhận trạng thái thủ tục |
| Nhân sự | còn lại | xem mọi dự án Admin cho hiển thị; thao tác (tải văn bản, đăng ký số) **chỉ trong dự án mình là thành viên** |

## Dự án & thủ tục

- Khi tạo dự án chọn: **loại dự án**, **bước thiết kế** (BCKTKT — 1 bước; BCNCKT — bước đầu dự án 2 bước; BVTC — bước cuối, khối lượng rất quan trọng), **có BIM hay không** (BIM thêm hạng mục + pháp lý BIM).
- Danh mục thủ tục khác nhau theo các lựa chọn trên (VD dự án 1 bước: thiết kế → thẩm tra → thẩm định ở Phòng KT-ĐT phường).
- **Văn bản gắn vào thủ tục** của dự án.
- Trạng thái thủ tục: **app gợi ý theo văn bản, leader xác nhận**.

## Văn bản đến

- Nhân sự tải PDF/ảnh/scan lên theo dự án → **app tự đọc, điền sẵn** (số, ngày, cơ quan, dự án, hạn…) → người tải **kiểm tra, sửa rồi mới lưu**.
- Người tải là leader → tự nhận xử lý; không phải leader → tag leader, mình phối hợp. Leader giao tiếp được cho nhân sự trong dự án.
- Hạn: theo văn bản nếu có ghi, không thì leader đặt.
- Chỉ **leader hoặc Admin** đánh dấu đã xử lý xong.

## Văn bản đi

- Người được giao soạn → **đăng ký số trên app** → điền số → leader ký nháy → sếp tổng ký (trên giấy) → scan, tải lên.
- **Mọi nhân sự** được đăng ký số; app **tự cấp số** theo quy tắc Admin đặt; đánh số **chung toàn công ty**; dự án liên danh thêm hậu tố **LD**; vẫn kiểm tra trùng.
- Số cấp quá **2 ngày làm việc** chưa có bản scan → báo Admin → **Admin nhắc** người đăng ký.

## Tổng quan cho CĐT, hồ sơ thiết kế, thông báo

- Màn **tổng quan cho CĐT** gồm: bước thiết kế hiện tại + thủ tục đã xong/còn lại · đang chờ cơ quan nào, bao lâu · việc CĐT cần làm · các mốc chính. **Xuất PDF** gửi CĐT.
- **Hồ sơ thiết kế không tải lên app** — chỉ lưu **đường link NAS**; thiếu link thì app nhắc.
- Thông báo qua **app + email**.

- Thiếu link NAS: khi văn bản đi **gửi hồ sơ** (thẩm tra, xin ý kiến, trình thẩm định) gắn thủ tục được phát hành mà thủ tục chưa có link → nhắc **người đăng ký số + leader**.
- **Sếp tổng nhận thông báo** như Admin.
- Số treo: Admin nhắc; vẫn không phát hành → **Admin huỷ số**.
- **Quy trình mẫu** (và danh mục thủ tục) do **Admin cung cấp / khai** trong app.

## Phạm vi MVP (đã duyệt)

- **P0:** Dự án · Thủ tục (từ quy trình mẫu, link NAS) · Văn bản đến (tự đọc + kiểm, luôn cho nhập tay) · Văn bản đi (cấp số, LD, scan, treo số) · Thông báo app + email · Tổng quan CĐT + xuất PDF · Danh sách dự án kèm số quá hạn / chờ cơ quan · Nhật ký thay đổi.
- **P1:** Dashboard điểm nghẽn nhiều dự án · Báo cáo, thống kê · Tìm kiếm trong nội dung PDF.
- **P2:** Duyệt / ký số trong app · Thông báo Zalo · Tài khoản/link cho CĐT · Phiên bản hồ sơ thiết kế, khối lượng.

## Tiêu chí thành công (đã duyệt)

- **SC-01** Mọi công văn đến/đi của các dự án đang chạy đều có trong app — không lục Zalo.
- **SC-02** Sáng mở app thấy ngay văn bản sắp hạn / quá hạn, của ai, dự án nào.
- **SC-03** Trả lời ngay "thủ tục X của dự án Y đang chờ cơ quan nào, từ bao giờ".
- **SC-04** Xuất tổng quan cho CĐT trong vài phút.
- Thêm yêu cầu: **xuất PDF tổng hợp văn bản dự án** để đính kèm hồ sơ thiết kế; **xuất thuyết minh toàn bộ văn bản pháp lý** của dự án.

## Trường hợp biên (đã duyệt)

- Hai người tải cùng một văn bản → app báo **đã trùng**.
- Gắn nhầm dự án → báo người nhập / leader; **leader và Admin** được chuyển đến đúng chỗ; app ghi log.
- Nhân sự nghỉ việc còn giữ văn bản → bàn giao cho leader; **không khoá tài khoản** cho đến khi leader tiếp nhận hoặc giao người khác.
- Hạn đặt vào ngày đã qua → cảnh báo nhưng vẫn lưu.

## Dữ liệu cũ

- 5 dự án đang chạy: **nhập lại toàn bộ văn bản cũ**.
- Văn bản đi cũ đã có số → app **giữ nguyên số cũ, không cấp lại**; chỉ cấp số cho văn bản đi mới.

- Số văn bản đi mới: Admin nhập **số bắt đầu** trong Cài đặt (nối tiếp số cũ); sang năm mới app tự quay về 1.
- Chế độ **Nhập văn bản cũ**: tải nhiều file một lần → app đọc → hàng chờ kiểm tra; văn bản cũ mặc định **Đã xong**, **không gửi thông báo**; văn bản còn dở thì bỏ đánh dấu.
- **Thuyết minh căn cứ pháp lý → P0**; **PDF gộp văn bản → P1**.

- Thuyết minh căn cứ pháp lý: xuất **Word**, chỉ văn bản đánh dấu **pháp lý**, sắp theo thủ tục rồi ngày.
- **Tạo dự án:** Admin và Leader. **Xuất** tổng quan CĐT và thuyết minh: Admin và Leader.
- Spec nhóm 1 (mục 1–3), nhóm 2 (mục 4–5), nhóm 3 (mục 6 — 14 F) đã duyệt.
- "Sắp hạn" = còn **2 ngày làm việc**.
- Một văn bản đi trả lời được **nhiều** văn bản đến; một văn bản đến có thể cần **nhiều** văn bản đi.
- **Tải văn bản lên chạy được trên điện thoại**; phần còn lại dùng máy tính.
- **Được gửi file ra dịch vụ bên ngoài** để tự đọc văn bản.
- Một văn bản thuộc **một** dự án; công văn liên quan hai dự án thì **tải 2 lần**.
- Spec đã viết: `docs/2-spec/spec.md`.

## Giả định (chưa được xác nhận rõ)

- Bản nháp trạng thái: văn bản đến *Mới → Đang xử lý → Đã xong*; văn bản đi *Đã cấp số → Đã phát hành / Huỷ số*; thủ tục *Chưa bắt đầu → Đang chuẩn bị → Chờ cơ quan → Có kết quả → Hoàn thành* (nhánh *Yêu cầu bổ sung*). Quá hạn và treo số là **cờ cảnh báo**, không phải trạng thái.
- Văn bản đến chia "Cần trả lời" (đóng khi có văn bản đi đã phát hành) / "Để biết" (leader bấm xong).
- Mỗi văn bản thuộc đúng một dự án; mỗi dự án một leader.

## Câu hỏi mở

- Nội dung cụ thể danh sách loại dự án và quy trình mẫu (Admin cung cấp sau).
- Số lượng văn bản cũ ước tính.
- Một lần cụ thể văn bản bị thất lạc / trễ hạn (cho mục 1 spec).
- Admin làm được mọi việc Leader làm trên mọi dự án? (tự suy)
