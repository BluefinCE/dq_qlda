# App QLDA — Spec

## 1. Bối cảnh & vấn đề

> App QLDA giúp **nhân sự công ty tư vấn thiết kế** theo dõi mọi **văn bản đến, văn bản đi và thủ tục pháp lý của từng dự án** ở một chỗ, mà hiện nay đang **nằm rải rác trên Zalo cá nhân, không vào sổ, không đánh số**.

**Hiện nay:** công văn nhận qua Zalo của từng thành viên; sếp giao việc qua Zalo; chưa có quy trình phát hành công văn đi; hồ sơ thiết kế lưu trên NAS. Công ty tư vấn cho chủ đầu tư (CĐT) nhà nước — nhiều chuyên viên CĐT cần được tư vấn về thủ tục.
**Chỗ đau nhất:** *"Khâu làm việc pháp lý với các cơ quan dễ bị chậm trễ nhất."* · *"Các văn bản thu thập từ nhiều cơ quan và CĐT nhiều lần có thể rất dễ bị lạc mất, và biên bản bàn giao hồ sơ, biên bản hiện trường."* · Giai đoạn thi công *"rất nhiều văn bản công văn được nhận và phát đi nên rất dễ bị thất lạc."*
**Ví dụ:** dự án đường Bà Xán, bước TKCS — khảo sát, thiết kế → thẩm tra → lấy ý kiến điện lực, thông tin, Sở Xây dựng, Sở Nông nghiệp… → thẩm định tại Sở Xây dựng → bước BVTC → giám sát tác giả khi thi công. Một lần thất lạc cụ thể: `[CẦN LÀM RÕ]`
**Dữ liệu đang có:** nhập lại **toàn bộ** văn bản cũ của 5 dự án đang chạy; văn bản đi cũ giữ nguyên số cũ.
**Quy mô:** 5 dự án → 15 · 8 người → 30 · ~100 văn bản/tháng.

## 2. Mục tiêu & tiêu chí thành công

- **SC-01** · Mọi công văn đến/đi của các dự án đang chạy đều có trong app — không ai phải lục Zalo để tìm.
- **SC-02** · Sáng mở app là thấy ngay văn bản nào sắp hạn / quá hạn, của ai, dự án nào.
- **SC-03** · Trả lời ngay được *"thủ tục X của dự án Y đang chờ cơ quan nào, từ bao giờ"*.
- **SC-04** · Xuất tổng quan gửi CĐT trong vài phút.
- **SC-05** · Xuất được phần căn cứ pháp lý của dự án để đưa vào thuyết minh, không gõ tay.

## 3. Ngoài phạm vi

| Tính năng | Vì sao để vòng sau |
|---|---|
| PDF gộp toàn bộ văn bản dự án | P1 — vòng đầu đã có thuyết minh căn cứ pháp lý |
| Dashboard điểm nghẽn nhiều dự án | P1 — vòng đầu có danh sách dự án kèm số quá hạn / chờ cơ quan |
| Báo cáo, thống kê (cơ quan nào chậm…) | P1 — cần dữ liệu tích luỹ |
| Tìm kiếm trong nội dung PDF | P1 |
| Ký nháy / duyệt / ký số trong app | P2 — giữ trên giấy như hiện nay |
| Thông báo qua Zalo | P2 — cần tích hợp Zalo OA |
| Tài khoản hoặc link xem cho CĐT | P2 — vòng đầu xuất PDF gửi CĐT |
| Tải hồ sơ thiết kế lên app, phiên bản, khối lượng | P2 — vòng đầu chỉ lưu link NAS |

## 4. Người dùng & vai trò

| Vai | Ai | Mở app để hỏi điều gì |
|---|---|---|
| **Admin** | anh Thông (kiêm Leader) | Có số nào treo? Dự án nào có văn bản quá hạn? |
| **Sếp tổng** | 1 người | Các dự án đang tới đâu, tắc ở đâu? |
| **Leader** | anh Thông + 2 leader | Dự án tôi có văn bản gì mới, việc gì sắp hạn, thủ tục nào chờ cơ quan? |
| **Nhân sự** | các thành viên còn lại | Tôi đang giữ văn bản nào, hạn bao giờ? |

CĐT, cơ quan nhà nước, đơn vị thẩm tra, nhà thầu **không mở app** — họ là **nơi gửi / nơi nhận** văn bản (mục 7).

**Ai được làm gì:**

| Việc | Admin | Sếp tổng | Leader | Nhân sự |
|---|---|---|---|---|
| Cài đặt chung (quy tắc số, số bắt đầu, loại dự án, quy trình mẫu, hiển thị dự án) | ✔ | ✘ | ✘ | ✘ |
| Tạo dự án | ✔ | ✘ | ✔ | ✘ |
| Thêm thành viên dự án | ✔ | ✘ | ✔ dự án mình | ✘ |
| Xem dự án được hiển thị | ✔ | ✔ | ✔ | ✔ |
| Tải văn bản đến · đăng ký số · tải bản scan văn bản đi | ✔ | ✘ | ✔ | ✔ dự án mình là thành viên |
| Giao / giao lại người xử lý, đặt hạn | ✔ | ✘ | ✔ dự án mình | ✘ |
| Đánh dấu văn bản Đã xong, mở lại | ✔ | ✘ | ✔ dự án mình | ✘ |
| Xác nhận trạng thái thủ tục | ✔ | ✘ | ✔ dự án mình | ✘ |
| Báo văn bản gắn nhầm | ✔ | ✘ | ✔ | ✔ |
| Chuyển văn bản gắn nhầm | ✔ | ✘ | ✔ dự án mình | ✘ |
| Nhắc số treo, huỷ số | ✔ | ✘ | ✘ | ✘ |
| Xuất tổng quan CĐT, xuất thuyết minh căn cứ pháp lý | ✔ | ✘ | ✔ dự án mình | ✘ |
| Khoá tài khoản nhân sự nghỉ việc | ✔ | ✘ | ✘ | ✘ |
| Nhận thông báo chung toàn công ty (số treo, quá hạn) | ✔ | ✔ | ✘ | ✘ |

**Chữ của app:** Dự án · Thủ tục · Quy trình mẫu · Văn bản đến · Văn bản đi · Admin · Sếp tổng · Leader · Nhân sự · trạng thái *Mới / Đang xử lý / Đã xong* · *Đã cấp số / Đã phát hành / Huỷ số* · *Chưa bắt đầu / Đang chuẩn bị / Chờ cơ quan / Có kết quả / Yêu cầu bổ sung / Hoàn thành* · cờ *Quá hạn*, *Sắp hạn*, *Treo số* — *dùng đúng các chữ này, không đổi qua lại.*

## 5. Luồng sử dụng chính

**Một vòng dùng app** *(Minh là tên ví dụ cho một nhân sự):*
Sáng thứ Hai Minh nhận qua Zalo văn bản góp ý của Sở Nông nghiệp về hồ sơ TKCS đường Bà Xán. Minh tải file lên ngay trên điện thoại; app điền sẵn số, ngày, cơ quan gửi, trích yếu, dự án — Minh sửa ngày, chọn thủ tục *"Lấy ý kiến Sở Nông nghiệp – TKCS"*, đánh dấu *pháp lý*, *Cần trả lời*, tag anh Thông. Anh Thông nhận thông báo trong app và email, giao Minh xử lý, hạn 5 ngày; app gợi ý thủ tục sang *Có kết quả*, anh Thông chọn *Yêu cầu bổ sung*. Minh chỉnh hồ sơ, đăng ký số văn bản đi trả lời và nhận số kế tiếp; anh Thông ký nháy, Sếp tổng ký; Minh scan, tải lên → *Đã phát hành*. Anh Thông đánh dấu văn bản đến *Đã xong*; app gợi ý thủ tục sang *Chờ cơ quan*. Cuối tháng anh Thông xuất tổng quan PDF gửi CĐT.

**Dòng đời** *(dạng A — có trạng thái nối tiếp):*
- **Văn bản đến:** Mới → Đang xử lý → Đã xong
  Loại *Cần trả lời*: chỉ Đã xong khi có **ít nhất một** văn bản đi trả lời *Đã phát hành*; Leader quyết định lần trả lời nào là cuối. Loại *Để biết*: Leader bấm là xong. Leader / Admin mở lại được, phải ghi lý do.
- **Văn bản đi:** Đã cấp số → Đã phát hành
  Nhánh rẽ: Đã cấp số → **Huỷ số** khi văn bản không phát hành; Admin bấm, ghi lý do; số đã huỷ không cấp lại.
- **Thủ tục:** Chưa bắt đầu → Đang chuẩn bị → Chờ cơ quan → Có kết quả → Hoàn thành
  Nhánh rẽ: Có kết quả → **Yêu cầu bổ sung** → Đang chuẩn bị. App gợi ý theo văn bản, Leader xác nhận. Thủ tục Hoàn thành **không** có nghĩa bước thiết kế hay dự án hoàn thành.
- *Quá hạn, Sắp hạn, Treo số là **cờ cảnh báo** app tự tính, không phải trạng thái.*

**Thử một vòng:** chạy lại đúng đoạn "Một vòng dùng app" — đi trọn không vướng là đạt.

## 6. Yêu cầu chức năng

> Dựng chia hai đợt: **Đợt 1** F1–F6, F9, F13 · **Đợt 2** F7, F8, F10–F12, F14.

### F1 · Cài đặt chung
Chỉ Admin. Đặt quy tắc số văn bản đi (mẫu ký hiệu, số bắt đầu, hậu tố **LD** cho liên danh), danh sách loại dự án, quy trình mẫu theo *loại dự án × bước thiết kế (BCKTKT / BCNCKT / BVTC) × có BIM*, và dự án nào được hiển thị.
- Admin đặt số bắt đầu 58 → đăng ký số đầu tiên → nhận 58.
- Khi đang là Leader hoặc Nhân sự → mở Cài đặt chung → không vào được.

### F2 · Tạo dự án
Admin hoặc Leader tạo dự án: loại, bước thiết kế, BIM, liên danh, leader, thành viên. App sinh danh sách thủ tục từ quy trình mẫu; người tạo thêm / bớt được.
- Tạo dự án BCKTKT không BIM → danh sách thủ tục đúng mẫu Admin khai.
- Để trống tên dự án hoặc leader → hiện lỗi, không lưu.
- Khi đang là Nhân sự → không tạo được dự án.

### F3 · Theo dõi thủ tục
Mỗi thủ tục có trạng thái và link NAS tới hồ sơ thiết kế. App gợi ý chuyển trạng thái khi có văn bản gắn vào; Leader xác nhận. Văn bản đi **gửi hồ sơ** (thẩm tra, xin ý kiến, trình thẩm định) được phát hành mà thủ tục chưa có link NAS → nhắc người đăng ký số và Leader.
- Văn bản đi gắn thủ tục được phát hành → app gợi ý *Chờ cơ quan* → Leader xác nhận → tải lại trang → vẫn *Chờ cơ quan*.
- Phát hành văn bản gửi hồ sơ khi thủ tục chưa có link NAS → người đăng ký số và Leader nhận nhắc.
- Khi đang là Nhân sự → không xác nhận được trạng thái thủ tục.

### F4 · Nhận văn bản đến
Thành viên dự án tải PDF / ảnh / scan, **cả trên điện thoại**. App tự đọc và điền sẵn số, ngày, cơ quan gửi, trích yếu, dự án, hạn; người tải kiểm, sửa, chọn thủ tục (hoặc "khác"), loại *Cần trả lời / Để biết*, đánh dấu *pháp lý* rồi mới lưu. Không đọc được → nhập tay. Người tải không phải Leader → bắt buộc tag Leader.
- Tải ảnh chụp mờ, app không đọc được → vẫn nhập tay và lưu được.
- Tải văn bản trùng số + cơ quan gửi với văn bản **cùng dự án** → báo "đã trùng", không lưu.
- Đặt hạn vào ngày đã qua → cảnh báo, vẫn lưu, bật cờ Quá hạn.
- Lưu → tải lại trang → văn bản vẫn còn.

### F5 · Giao và xử lý văn bản đến
Leader nhận hoặc giao cho thành viên dự án, đặt hạn (lấy theo văn bản nếu có ghi). Leader / Admin đánh dấu Đã xong theo điều kiện ở mục 5; mở lại phải ghi lý do.
- Văn bản *Cần trả lời* chưa có văn bản đi Đã phát hành → không đánh dấu Đã xong được.
- Khi đang là Minh → mở văn bản mình đang giữ → không có lựa chọn Đã xong.
- Đánh dấu Đã xong một văn bản Quá hạn → số văn bản quá hạn của dự án giảm 1.

### F6 · Đăng ký số và phát hành văn bản đi
Thành viên dự án đăng ký số; app cấp số kế tiếp **chung toàn công ty** theo quy tắc F1, gắn văn bản đi vào thủ tục và vào một hoặc nhiều văn bản đến mà nó trả lời. Tải bản scan có chữ ký → Đã phát hành. Quá 2 ngày làm việc chưa có scan → cờ Treo số → báo Admin và Sếp tổng; Admin nhắc người đăng ký, vẫn không phát hành thì Admin huỷ số.
- Hai người đăng ký cùng lúc → nhận hai số liên tiếp, không trùng.
- Dự án liên danh → số có hậu tố LD.
- Admin huỷ số 60 → lần đăng ký sau nhận 61.
- Khi không phải thành viên dự án → không đăng ký số cho dự án đó được.

### F7 · Nhập văn bản cũ
Tải nhiều file một lần → app đọc → hàng chờ kiểm tra; người nhập kiểm từng văn bản, không cần liền một mạch. Văn bản đi cũ giữ nguyên số cũ. Văn bản cũ mặc định Đã xong, không gửi thông báo; văn bản còn dở thì bỏ đánh dấu.
- Nhập văn bản đi cũ số 45/2026 → app không đổi số, số cấp tiếp không bị ảnh hưởng.
- Nhập văn bản cũ trùng với văn bản đã có trong cùng dự án → báo trùng.
- Nhập 20 văn bản cũ → không ai nhận thông báo quá hạn.

### F8 · Báo và chuyển văn bản gắn nhầm
Ai cũng báo được văn bản gắn nhầm dự án / thủ tục → người nhập và Leader nhận thông báo. Leader / Admin chuyển văn bản đến đúng chỗ; app ghi nhật ký.
- Chuyển văn bản từ dự án A sang B → số liệu của cả hai dự án đổi theo.
- Khi đang là Nhân sự → không chuyển được.

### F9 · Thông báo trong app và email
Thông báo khi: được tag / được giao · văn bản sắp hạn (còn 2 ngày làm việc) hoặc quá hạn · số treo · thiếu link NAS · có báo gắn nhầm. Admin và Sếp tổng nhận thêm thông báo chung toàn công ty.
- Leader giao văn bản cho Minh → Minh thấy thông báo trong app và nhận email.

### F10 · Xem dự án và văn bản
Xem danh sách dự án kèm số văn bản quá hạn và số thủ tục Chờ cơ quan; xem văn bản theo dự án, theo thủ tục, theo người đang giữ, theo hạn.
- Leader xác nhận một thủ tục sang Chờ cơ quan → con số trên danh sách dự án tăng 1.

### F11 · Xuất tổng quan cho CĐT (PDF)
Admin / Leader. Gồm: bước thiết kế hiện tại và thủ tục đã xong / còn lại · đang chờ cơ quan nào, bao lâu · việc CĐT cần làm · các mốc chính.
- Xuất PDF → nội dung khớp trạng thái thủ tục đang có trong app.

### F12 · Xuất thuyết minh căn cứ pháp lý (Word)
Admin / Leader. Chỉ văn bản đánh dấu *pháp lý*, sắp theo thủ tục rồi theo ngày; mỗi văn bản một dòng *"Căn cứ Văn bản số … ngày … của … về việc …;"*.
- Bỏ đánh dấu pháp lý một văn bản → xuất lại → văn bản đó không còn trong file.

### F13 · Nhật ký thay đổi
App tự ghi ai · lúc nào · làm gì · lý do cho mọi lần đổi trạng thái, giao, chuyển, huỷ số, mở lại; xem được ngay trong từng văn bản và thủ tục.
- Admin huỷ một số → nhật ký của văn bản đó có dòng ghi người huỷ, thời điểm và lý do.

### F14 · Bàn giao khi nhân sự nghỉ việc
Admin chỉ khoá được tài khoản khi người đó không còn giữ văn bản nào; Leader tiếp nhận hoặc giao lại trước.
- Minh còn giữ 2 văn bản → Admin bấm khoá → app chặn và liệt kê 2 văn bản đó.

## 7. Mô hình dữ liệu

| Lưu hồ sơ của | Mỗi hồ sơ gồm | Nối với nhau thế nào | Vào app từ đâu | Chỗ tôi tự suy — cần bạn xác nhận |
|---|---|---|---|---|
| **Người dùng** `users` | họ tên · email · vai · đang làm / đã nghỉ | một người ở nhiều dự án | Admin tạo | chỉ Admin tạo tài khoản |
| **Loại dự án, quy trình mẫu** `project_types` `procedure_templates` | loại dự án · với mỗi *loại × bước × BIM*: danh sách thủ tục mẫu (tên, thứ tự, có cần link NAS) | một mẫu sinh thủ tục cho nhiều dự án | Admin khai | |
| **Dự án** `projects` | mã · tên · CĐT · loại · bước thiết kế · BIM · liên danh · leader · ngày bắt đầu · hiển thị | một dự án có một leader, nhiều thành viên `project_members`, nhiều thủ tục | Admin / Leader gõ | thêm *mã dự án*, *CĐT* |
| **Thủ tục** `procedures` | tên · thứ tự · trạng thái · link NAS | thuộc một dự án; có nhiều văn bản | sinh từ mẫu, sửa tay | |
| **Văn bản đến** `incoming_docs` | số · ngày · cơ quan gửi · trích yếu · file · loại · pháp lý · hạn · trạng thái · người giữ · người phối hợp · người tải · văn bản cũ | thuộc **một** dự án; gắn một thủ tục hoặc "khác" | người tải lên, app điền sẵn | |
| **Văn bản đi** `outgoing_docs` | số · ngày · nơi nhận · trích yếu · file scan · pháp lý · gửi hồ sơ · trạng thái · người đăng ký · lý do huỷ · văn bản cũ | thuộc **một** dự án; gắn một thủ tục hoặc "khác" | người đăng ký số | văn bản đi cũng đánh dấu pháp lý được |
| **Mối nối trả lời** `doc_replies` | văn bản đi · văn bản đến | một văn bản đi trả lời **nhiều** văn bản đến; một văn bản đến có **nhiều** văn bản đi | người đăng ký số chọn | |
| **Cơ quan / đơn vị** `organizations` | tên · loại (CĐT, cơ quan nhà nước, thẩm tra, nhà thầu…) | gửi / nhận nhiều văn bản | danh mục, thêm khi gặp mới | là danh mục, không gõ tự do |
| **Nhật ký** `audit_log` | ai · lúc nào · làm gì · lý do | gắn văn bản hoặc thủ tục | app tự ghi | |

*Chữ in mờ `<tên_bảng>` là tên kỹ thuật cho buổi dựng app — bạn không cần sửa.*

**App tự tính, không lưu:**
- **Quá hạn** = đã qua hạn mà chưa Đã xong
- **Sắp hạn** = còn ≤ 2 ngày làm việc tới hạn
- **Treo số** = ở Đã cấp số quá 2 ngày làm việc
- **Đã chờ cơ quan bao lâu** = hôm nay − ngày thủ tục sang Chờ cơ quan (lấy từ nhật ký)
- **Số văn bản quá hạn**, **số thủ tục Chờ cơ quan** của mỗi dự án
- **Số kế tiếp** = số lớn nhất đã cấp trong năm + 1, hoặc số bắt đầu Admin đặt; sang năm mới quay về 1

## 8. Yêu cầu phi chức năng

- **Thiết bị:** máy tính; riêng **tải văn bản đến lên** phải dùng được trên điện thoại.
- **Ngôn ngữ:** tiếng Việt.
- **Quy mô & tốc độ:** 30 người · 15 dự án · ~100 văn bản/tháng + toàn bộ văn bản cũ.
- **Bảo mật & riêng tư:** đăng nhập ngay vòng đầu; ai thấy gì theo bảng mục 4; file công văn **được gửi ra dịch vụ đọc văn bản bên ngoài** (công ty đã đồng ý).
- **Lưu giữ:** giữ mãi; văn bản không xoá được, chỉ chuyển / huỷ số / mở lại.

## 9. Trường hợp biên & xử lý lỗi

- Nếu hai người tải cùng một văn bản vào cùng dự án → app báo **đã trùng**, không lưu bản thứ hai.
- Nếu một công văn liên quan hai dự án → tải lên **hai lần**, mỗi dự án một bản; app nhắc "văn bản này đã có ở dự án X" nhưng vẫn cho lưu.
- Nếu gắn nhầm dự án / thủ tục → báo người nhập và Leader; Leader / Admin chuyển; app ghi nhật ký.
- Nếu nhân sự nghỉ việc còn giữ văn bản → bàn giao cho Leader; không khoá tài khoản tới khi Leader tiếp nhận hoặc giao lại.
- Nếu hạn đặt vào ngày đã qua → cảnh báo, vẫn lưu.
- Nếu đổi Leader dự án → văn bản Leader cũ đang giữ chuyển sang Leader mới.
- Nếu dự án đã có văn bản → không xoá được, chỉ ẩn.

## Phụ lục: Câu hỏi còn mở

- `[CẦN LÀM RÕ]` Danh sách loại dự án và quy trình mẫu — Admin cung cấp **trước khi chạy thử**.
- `[CẦN LÀM RÕ]` Mẫu ký hiệu số văn bản đi và số cũ cuối cùng năm 2026.
- `[CẦN LÀM RÕ]` Một lần cụ thể văn bản bị thất lạc / trễ hạn (mục 1).
- `[CẦN LÀM RÕ]` Số lượng văn bản cũ ước tính.
- **Giả định:**
  - G1 Admin làm được mọi việc Leader làm, trên mọi dự án.
  - G2 Chỉ Admin tạo tài khoản người dùng.
  - G3 Dự án có thêm *mã dự án* và *CĐT*.
  - G4 Cơ quan / đơn vị là danh mục.
  - G5 Văn bản đi cũng đánh dấu pháp lý và vào thuyết minh căn cứ pháp lý.
  - G6 Văn bản không xoá được.
  - G7 Ngày làm việc = thứ Hai – thứ Sáu, chưa trừ ngày lễ.
  - G8 Đổi Leader → văn bản Leader cũ đang giữ chuyển sang Leader mới.
  - G9 Dự án đã có văn bản chỉ ẩn, không xoá.
  - G10 Email thông báo gửi từ một địa chỉ email của công ty.
  - G11 Tốc độ, sao lưu, công nghệ quyết định ở buổi dựng app.
