# Interview guide — đọc trước câu hỏi đầu tiên

Bộ câu mẫu cho Bước 1–4 của `SKILL.md`. Không phải kịch bản đọc nguyên văn — đổi chữ cho khớp app của
người dùng, nhưng giữ đúng **ý** của từng câu.

---

## Bước 1 · Họ đã đưa gì sẵn?

### Họ mở đầu bằng bối cảnh theo 5W1H

Đọc kỹ, đối chiếu bảng dưới: mục nào **đã có** thì chỉ tóm lại cho họ xác nhận — **đừng hỏi lại**.
Dồn lượt hỏi vào những mục 5W1H **không lấp được**.

| 5W1H họ viết | Lấp mục nào của spec | Thường vẫn thiếu |
|---|---|---|
| **AI DÙNG** | 4 · vai | **ai được làm gì** — họ thường chỉ nói ai giao việc |
| **QUẢN LÝ CÁI GÌ** | 1 · hiện nay · 7 · thứ cần lưu (sơ bộ) | **một hay nhiều** · mỗi thứ gồm những mục gì |
| **VÌ SAO CẦN** | 1 · chỗ đau · ví dụ gần nhất | — |
| **KHI NÀO DÙNG** | 2 · mục tiêu (sơ bộ) · 5 | SC **kiểm được** |
| **DÙNG Ở ĐÂU** | 8 · thiết bị · 1 · dữ liệu đang có | dữ liệu cũ **đưa vào thế nào** |
| **LÀM THẾ NÀO** | 5 · luồng · dòng đời | **nhánh rẽ** (chưa đạt, giao nhầm) |
| *(không mục nào)* | **3 · 6 · 9** | phải hỏi gần như từ đầu |

**Cẩn thận chỗ tự suy:** họ viết *"tôi giao việc"* không có nghĩa là **chỉ họ** được thêm việc. Đây là
câu hỏi quyền — hỏi, đừng suy.

### Họ mở đầu bằng một câu ngắn

Có tệp trong project (nhất là `docs/`) thì đọc trước. Không có gì thì mở bằng chuyện thật:

> *"Kể tôi nghe một ngày làm việc của bạn đang vướng ở chỗ nào?"*

### Xét phạm vi và chốt khẩu phần

Họ kể nhiều hệ thống rời nhau (*"nhân sự, kho, kế toán và chăm khách"*) → chọn **một** trước:

> *"Bạn đang kể 4 app khác nhau. Ta chọn một cái làm trước — cái nào đang làm bạn mất nhiều thời
> gian nhất?"*

Rồi nói một lần, trước khi bàn tính năng:

> *"Vòng đầu phải đủ nhỏ để **dựng xong trong một buổi**. Thứ gì không vừa thì không mất — nó vào
> danh sách 'vòng sau'."*

---

## Bước 2a · Hỏi vì sao *(bỏ nếu họ đã viết VÌ SAO CẦN)*

> *"Nếu app chạy đúng, việc gì trong tuần của đội bạn sẽ khác đi?"*
> *"Lần gần nhất việc bị trễ hoặc bị quên là chuyện gì?"*

Họ đáp bằng tính năng (*"cần có Kanban"*) → hỏi tiếp *"cái đó giúp bạn tránh chuyện gì?"*

## Bước 2b · Tóm lại cho họ sửa

Sau vài câu đầu — hoặc **ngay lượt đầu** nếu họ đưa 5W1H — dừng và viết lại ngắn:

> *"Tôi hiểu thế này, bạn sửa giúp nếu sai:*
> - *App giúp **<ai>** <làm được gì>.*
> - *Hiện giờ <việc đang nằm ở đâu, đau ở đâu>.*
> - *Xong là khi: <họ thấy gì thì biết app chạy đúng>.*
> - *Chỗ tôi tự đoán: <…>."*

Bản này là **gốc** của cả spec — phương án và mọi mục sau phải khớp với nó.

---

## Bước 2c · Câu hỏi theo từng mục

### Mục 2 · Mục tiêu & tiêu chí thành công
> *"Dùng app một tuần, bạn nhìn vào đâu để biết nó đáng làm?"*

Họ nói *"làm việc hiệu quả hơn"* → đưa mẫu: *"Sáng thứ Hai mở app là thấy ngay việc nào sắp trễ, của ai"*.

### Mục 4 · Ai được làm gì *(app ≥2 vai — bắt buộc, mỗi lượt một câu)*
1. *"Ai được **thêm** `<thứ>` mới — và **giao** cho người khác?"*
2. *"Ai được đánh dấu **Xong** — hay phải qua duyệt?"*
3. *"Ai được **huỷ**?"*
4. *"`<vai 2>` có được **xem** — và **sửa** — `<thứ>` của người khác không?"*

Họ tự trả lời gộp nhiều ý một lượt → nhận luôn, đừng hỏi lại phần đã có. Mọi vai làm được như nhau →
ghi một dòng *"mọi vai làm được như nhau"*, bỏ bảng.

Có ai **không tự mở app** không? *(khách, người ngoài nhóm → là dữ liệu, không phải vai)*

### Mục 5 · Luồng sử dụng chính
Họ chưa kể luồng → xin kể bằng **một người có tên**:
> *"Giả sử app đã chạy. Kể tôi nghe một lần `<tên một người trong đội>` dùng nó — sáng mở ra thấy gì,
> làm gì, việc đi tới đâu, ai nhận tiếp?"*

Hỏi **lúc không ổn** — chỗ người ta hay quên:
> *"`<thứ>` gửi duyệt mà chưa đạt thì sao — trả về, hay có trạng thái riêng?"*
> *"Giao nhầm thì sao?"*

Có trạng thái nối tiếp không — đừng giả định là có:
> *"Một `<thứ>` sau khi xuất hiện thì **đi qua các trạng thái** nào, hay được **ghi thẳng vào một dạng**
> rồi ở đó luôn?"*

### Mục 6 · Yêu cầu chức năng
Gom các việc họ đã kể thành danh sách F, đọc lại cho họ xác nhận:
> *"Từ những gì bạn kể, app cần làm được những việc này: … Thiếu việc nào không?"*

Hỏi **cần xem theo cách nào** — đây là F, không phải màn hình:
> *"Bạn cần xem `<thứ>` theo những cách nào — theo người, theo dự án, theo ngày hạn, hay cách khác?"*

Tiêu chí chấp nhận — hỏi *"bạn bấm gì"*, đừng hỏi *"tiêu chí là gì"*:
> *"Ngày mai app xong, bạn **làm gì đầu tiên** để biết nó chạy đúng?"*

Người dùng gần như chỉ tự nghĩ ra loại **nhập sai**. Ba loại kia bạn đưa mẫu để họ sửa:
- **Quyền:** *"Lan mở việc của mình đang Chờ duyệt → không có lựa chọn Xong"*
- **Còn sau tải lại:** *"Thêm việc → tải lại trang → vẫn còn"*
- **Con số tự đúng:** *"Huỷ một việc quá hạn → con số Quá hạn tự giảm"*

Họ kể **màn hình** (*"trang đầu có 3 ô số, bên phải có lịch"*) → **đừng ghi bố cục**. Hỏi nhu cầu đằng sau:
> *"Ba con số đó giúp bạn biết điều gì?"*

…rồi ghi điều đó thành một F (*"xem ngay số việc quá hạn, đến hạn hôm nay, đang làm"*).

### Mục 7 · Mô hình dữ liệu
> *"Mỗi `<thứ>` cần ghi lại những gì?"*

Rồi chạy **phép thử MỘT hay NHIỀU** và **LƯU hay TÍNH** — xem dưới.

Dữ liệu đang có → *"40 việc trong Excel: bắt đầu từ trống, nhập tay lại, hay đưa vào một lần lúc dựng app?"*

### Mục 8 · Yêu cầu phi chức năng
**Không hỏi từng dòng** — điền mặc định. Chỉ hỏi khi 5W1H chưa nói:
> *"Mọi người mở app chủ yếu trên **máy tính** hay **điện thoại**? Mỗi tháng cỡ bao nhiêu `<thứ>`?"*
> *"Có gì trong đây không nên để ai cũng thấy — lương, sức khoẻ, thông tin khách?"* *(app một người thì bỏ)*

### Mục 9 · Trường hợp biên & xử lý lỗi
Đưa **2–3 tình huống mẫu** đúng app của họ, hỏi app nên làm gì:
> *"Nếu `<thứ>` đặt hạn vào ngày đã qua thì sao?"*
> *"Nếu xoá một người đang còn giữ việc thì việc của họ đi đâu?"*
> *"Nếu trả lại mà không ghi lý do thì sao?"*

---

## Ba phép thử — chạy với mọi app

### 1 · MỘT hay NHIỀU *(khi bàn tới dữ liệu)*

Người không kỹ thuật gần như luôn gộp hai thứ thành một. Họ nói *"lưu hồ sơ khách"* rồi kể *tên ·
điện thoại · ngày mua · mua gì · tiền* — ba mục cuối thuộc **đơn hàng**, không thuộc khách.

Với từng mục họ kể:

> *"`<một người/thứ cụ thể>` có **MỘT** cái này, hay **NHIỀU** cái?"*

App quản lý công việc — ba câu hay đổi cả thiết kế:
*"Một việc có **một** hay **nhiều** người làm?"* · *"Một việc thuộc **một** hay **nhiều** dự án?"* ·
*"Bình luận là **một** ô ghi chú, hay **nhiều** dòng trao đổi?"*
Mỗi câu *"nhiều"* là thêm **một thứ cần lưu** — nói rõ cái giá đó ra.

**Không được tự suy ở đây.** Tách cha/con là quyết định nghiệp vụ. Tự tách rồi dán `[tôi tự suy]` thì
họ gật mà không hiểu, và app dựng sai kiến trúc.

Một người có thể ở **hai trạng thái cùng lúc** không? → có = trạng thái thuộc *thứ con* (đơn hàng, ca
điều trị), không thuộc người.

Hai thứ con **dính nhau** (buổi học trừ vào gói · đơn trừ vào tồn kho):
> *"Bạn cần biết `<cái này>` nào thuộc `<cái kia>` nào, hay chỉ cần **đếm tổng**?"*

### 2 · LƯU hay TÍNH *(với mọi con số họ kể)*

> *"Con số này bạn **ghi vào một chỗ**, hay **cộng trừ ra** mỗi lần cần?"*

Cộng trừ ra được → **không lưu**, ghi vào *"App tự tính, không lưu"* ở mục 7. Nói với họ: *"lưu con số
tính được là lý do sổ giấy hay lệch — app tự đếm thì không lệch."*

### 3 · CẮT *(khi họ muốn quá nhiều thứ)*

Đừng chỉ hỏi *"bỏ cái nào?"* — họ sẽ đáp *"cái nào cũng cần"*. Hỏi ba câu theo thứ tự:

| Phép cắt | Câu hỏi | Cắt được gì |
|---|---|---|
| Chỉ xem | *"Có ai NHẬP gì vào cái này không, hay chỉ để xem?"* | chỉ xem → bảng tính làm được |
| Ra ngoài app | *"Cái này xảy ra trong app, hay là gửi ra ngoài?"* | gửi ra ngoài → việc của luồng tự động |
| Thiếu thì chết | *"Thiếu cái này thì app còn dùng được không?"* | còn dùng được → để vòng sau |

Họ vẫn giữ sau cả ba câu → **họ đúng, đừng cãi** — nhưng thử tách làm hai nửa trước khi hoãn:

| Họ muốn | Nửa làm ngay (mục 6) | Nửa để sau (mục 3) |
|---|---|---|
| Gửi tin nhắn nhắc | danh sách "cần nhắc hôm nay" | app tự bấm gửi |
| Đồng bộ Excel | xuất một lần | tự đồng bộ hai chiều |
| Biểu đồ báo cáo | vài con số tổng | trang biểu đồ riêng |

---

## Bước 3 · Mẫu đưa phương án

> *"Có ba cách làm app này:*
> - ***A** — `<mô tả>`. Được: `<…>`. Mất: `<…>`*
> - ***B** — `<mô tả>`. Được: `<…>`. Mất: `<…>`*
> - ***C** — `<mô tả>`. Được: `<…>`. Mất: `<…>`*
>
> *Tôi khuyên **A**, vì `<lý do gắn với việc của họ>`. Bạn thấy sao?"*

Phương án phải khác nhau ở chỗ **đáng khác** — về **cách làm việc**, không về bố cục màn hình:
- **dữ liệu vào app bằng cách nào** — nhập tay từng lần, nhập một lần từ file, hay app sinh sẵn theo
  lịch/mẫu *(trục quyết định nhất)*
- **khai trước hay dùng được ngay** — phải khai 25 hồ sơ mới chạy, hay mở là dùng
- **thủ công hay tự động** — ai bấm, hay app tự đánh dấu
- *(nhiều vai)* **ai thấy gì** — cả nhóm xem chung, hay mỗi người chỉ thấy phần mình

Nêu rõ **cái mất** của từng cách — nghe cái giá cụ thể, họ mới bật ra ràng buộc thật. Họ ghép hai cách
là chuyện tốt — đọc lại bản ghép cho họ xác nhận.

---

## Bước 4 · Khi họ đòi "code luôn đi"

| Lần | Cách đáp |
|---|---|
| 1 | *"Chưa — còn `<n>` phần nữa. Có spec rồi thì code mới đúng ý."* |
| 2 | *"Tôi code được ngay, nhưng phải tự đoán `<chỗ họ chưa nói>`. Đoán sai thì bạn dựng lại."* |
| 3+ | *"Được — cho tôi 2 câu cuối, không thì app sẽ thiếu `<X>` và `<Y>`."* → hỏi 2 câu rồi viết spec với phần đang có |

Đừng cãi tới lần thứ tư. Thà spec thiếu còn hơn họ bỏ giữa buổi.

## Bước 6 · Xác nhận chỗ tự suy

Đừng đọc tên bảng/cột cho họ nghe — họ sẽ gật cho qua:

| Đừng nói | Nói thế này |
|---|---|
| *"`tasks.assignee_id` nối sang `members.id`, đúng không?"* | *"Mỗi việc thuộc về đúng một người, và một người có nhiều việc. Đúng không?"* |
| *"`comments.task_id` là khoá ngoại"* | *"Mỗi dòng trao đổi gắn với đúng một việc — không có trao đổi chung. Đúng không?"* |
