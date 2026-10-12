# Spec template — 9 mục + phụ lục

Viết đúng 9 mục này, đúng tiêu đề, đúng thứ tự, cộng phụ lục. **Giữ đủ 9 tiêu đề** — mục không có gì
thì ghi một dòng *"Không có ở vòng này."*, đừng xoá (buổi sau tra theo số mục).

Viết **ngắn, cụ thể, bằng chữ nghiệp vụ**. Cả file **khoảng 2 trang** — dài hơn thường là chưa cắt.

**Không có mục màn hình, và không được tự thêm.** Spec nói app **làm được gì**, không nói app **trông
thế nào** — màn hình là việc của buổi thiết kế giao diện. Họ kể về màn hình → ghi nhu cầu đằng sau nó
thành một yêu cầu ở mục 6 (cần xem gì, cần làm gì).

---

## Khuôn

```markdown
# <Tên app> — Spec

## 1. Bối cảnh & vấn đề

> Một câu: app này giúp <ai> làm được <việc gì> mà hiện nay đang <khó ở đâu>.

**Hiện nay:** <việc đang làm bằng công cụ gì, ai cập nhật>
**Chỗ đau nhất:** <nguyên văn cách người dùng nói>
**Ví dụ gần nhất:** <một lần việc bị trễ / bị quên / bị sai — chuyện thật>
**Dữ liệu đang có:** <file/danh sách đang dùng phải đưa vào app — hoặc "bắt đầu từ trống">

## 2. Mục tiêu & tiêu chí thành công

- **SC-01** · <kết quả người dùng thấy được khi app chạy đúng>
- **SC-02** · <…>

## 3. Ngoài phạm vi

| Tính năng | Vì sao để vòng sau |
|---|---|
| <tên> | <lý do ngắn> |

## 4. Người dùng & vai trò

| Vai | Ai | Mở app để hỏi điều gì |
|---|---|---|
| <vai 1> | <tên/bộ phận> | <câu hỏi trong đầu họ> |
| <vai 2> | <tên/bộ phận> | <câu hỏi trong đầu họ> |

**Ai được làm gì:**

| Việc | <vai 1> | <vai 2> |
|---|---|---|
| <ví dụ: thêm <thứ> mới> | ✔ | ✔ |
| <ví dụ: chuyển sang Xong> | ✔ | ✘ |

**Chữ của app:** <thứ chính> · <các trạng thái> · <tên vai> — *dùng đúng các chữ này, không đổi qua lại.*

## 5. Luồng sử dụng chính

**Một vòng dùng app:**
<4–6 câu, kể bằng MỘT người có tên: lúc nào mở app, thấy gì, làm gì, việc đi tới đâu, ai nhận tiếp.>

**Dòng đời một <thứ>:** *(chọn MỘT dạng)*
- **Dạng A — có trạng thái nối tiếp:** <trạng thái 1> → <trạng thái 2> → <trạng thái 3>
  Nhánh rẽ: <trạng thái X> → **<nhánh>** khi <điều kiện>; <ai bấm / app tự>
- **Dạng B — ghi thẳng:** một <thứ> được ghi vào một trong các dạng: <dạng 1> · <dạng 2>

**Thử một vòng:** chạy lại đúng đoạn "Một vòng dùng app" — đi trọn không vướng là đạt.

## 6. Yêu cầu chức năng

### F1 · <việc app làm được — bắt đầu bằng động từ>
<1–2 câu: ai làm, làm gì, quy tắc riêng của việc này.>
- Khi đang <bối cảnh> → <làm gì> → <thấy gì>

### F2 · <…>
<…>
- Khi đang <…> → <…> → <…>

## 7. Mô hình dữ liệu

| Lưu hồ sơ của | Mỗi hồ sơ gồm | Nối với nhau thế nào | Vào app từ đâu | Chỗ tôi tự suy — cần bạn xác nhận |
|---|---|---|---|---|
| **<thứ 1>** `<tên_bảng>` | <mục 1> · <mục 2> | <một thứ 1 có nhiều thứ 2> | <người gõ / nhập một lần từ file / có sẵn cố định> | <hoặc để trống> |

*Chữ in mờ `<tên_bảng>` là tên kỹ thuật cho buổi dựng app — bạn không cần sửa.*

**App tự tính, không lưu:**
- **<tên con số>** = <cách tính>

## 8. Yêu cầu phi chức năng

- **Thiết bị:** <máy tính / điện thoại / cả hai — dùng lúc nào>
- **Ngôn ngữ:** <tiếng Việt / …>
- **Quy mô & tốc độ:** <bao nhiêu người · bao nhiêu <thứ> mỗi tháng>
- **Bảo mật & riêng tư:** <ai được xem gì — khớp mục 4 · có dữ liệu nhạy cảm không · đăng nhập ngay hay vòng sau>
- **Lưu giữ:** <giữ bao lâu>

## 9. Trường hợp biên & xử lý lỗi

- Nếu <tình huống> → app <xử lý thế nào>
- Nếu <…> → <…>

## Phụ lục: Câu hỏi còn mở

- `[CẦN LÀM RÕ]` <câu chưa có câu trả lời — cũng gắn đúng ký hiệu này tại chỗ trong spec>
- **Giả định:** <thứ tôi tự chọn mặc định vì không đáng hỏi>
```

---

## Luật cho từng mục

### 1 · Bối cảnh & vấn đề
Câu mở đầu đọc to lên được thành **một câu** — chưa nói được thành một câu là đặc tả còn mờ ở gốc.
**Chỗ đau** và **ví dụ gần nhất** ghi **nguyên văn** cách họ kể, đừng viết lại cho "chuyên nghiệp".

### 2 · Mục tiêu & tiêu chí thành công
SC là **kết quả người dùng thấy được**, không phải nút bấm — nút bấm để mục 6. **2–4 SC** là đủ.

| Nhận | Không nhận |
|---|---|
| SC · Sáng thứ Hai mở app là thấy ngay việc nào sắp trễ, của ai | Nhóm làm việc hiệu quả hơn |
| SC · Không ai phải nhắn hỏi "việc này tới đâu rồi" | App dễ dùng |

Phép thử: **đọc lên là biết cách kiểm** sau một tuần dùng thì nhận; chỉ là mong muốn thì không.

### 3 · Ngoài phạm vi
Không phải phụ lục cho đủ. Đây là chỗ chứng minh vòng đầu là kết quả của việc **cắt có lý do** — và
là kế hoạch nâng cấp sau này. Thứ được **tách đôi** thì ghi nửa để sau ở đây, nửa làm ngay ở mục 6.
Lý do ghi **nguyên văn của họ** khi họ tự nói.

### 4 · Người dùng & vai trò
App cho **nhóm** thì nên có ≥2 vai, và hai vai phải hỏi **hai câu khác nhau**. App cho **một người** →
một vai là đủ, **bỏ bảng "Ai được làm gì"**, đừng bịa vai thứ hai cho đủ khuôn.

Ai **không tự mở app** (khách, bệnh nhân, người ngoài nhóm) → họ là **dữ liệu** (mục 7), không phải vai.

**Ai được làm gì** — mỗi dòng là một việc **làm thay đổi dữ liệu** (thêm · sửa · đổi trạng thái ·
huỷ) hoặc **xem dữ liệu của người khác**. Chữ nghiệp vụ, không viết *"quyền admin"*.
Buổi này chỉ **ghi quy tắc**, chưa dựng đăng nhập — nhưng không ghi thì app cho ai cũng làm được mọi thứ.

**Chữ của app** — đúng những chữ đã chốt với người dùng, dùng lại y nguyên ở mọi mục khác.

### 5 · Luồng sử dụng chính
Kể bằng **người có tên** lấy từ mục 4, đúng thứ tự thời gian, có chỗ **chuyển tay** giữa hai vai nếu
app nhiều vai. Không nhắc tới màn hình hay nút — kể việc người ta làm.

Dạng A: **một đường thẳng có mũi tên**, nhánh rẽ ghi rõ ai bấm. Dạng B: **đừng vẽ mũi tên** — các dạng
là lựa chọn song song. App **một người** thường là dạng B, không có bước duyệt.

### 6 · Yêu cầu chức năng
Mỗi **F** là một việc app làm được, **bắt đầu bằng động từ** *(thêm việc · đổi trạng thái · xem việc
theo dự án…)*. **Không nói màn hình, nút, bố cục hay công nghệ.**

- **Nhu cầu xem cũng là một F** — *"xem việc theo dự án"*, *"xem việc theo lịch hạn"*. Đây là chỗ giữ
  nhu cầu thật của đội cho buổi thiết kế giao diện.
- Mỗi F có **ít nhất 1 tiêu chí chấp nhận**, đúng khuôn **khi đang `<…>` → `<làm gì>` → `<thấy gì>`**.
  Vế đầu được bỏ khi bối cảnh hiển nhiên.
- F nào dính tới bảng **"Ai được làm gì"** thì có một tiêu chí **kiểm quyền**.
- **Khoảng 5–8 F** cho vòng đầu. Nhiều hơn là chưa cắt.

| Nhận | Không nhận |
|---|---|
| Thêm việc mà để trống tên → hiện lỗi, không lưu | Giao diện dễ dùng |
| Khi đang chọn là Lan → mở việc của mình đang Chờ duyệt → không có lựa chọn Xong | Có nút Xong màu xanh ở góc phải |
| Đổi việc sang Đang làm → tải lại trang → vẫn là Đang làm | App chạy nhanh |

**Cả spec phải có đủ 4 loại tiêu chí** *(rải trong các F và mục 9)*:

| Loại | Kiểm điều gì |
|---|---|
| **Quyền** | vai này **không** làm được việc của vai kia *(app một người bỏ loại này)* |
| **Còn sau tải lại** | dữ liệu thật sự được lưu |
| **Con số tự đúng** | con số tính ra đổi đúng khi dữ liệu đổi |
| **Nhập sai** | app chặn dữ liệu hỏng |

### 7 · Mô hình dữ liệu
Chữ **của người dùng**. Tên bảng tiếng Anh để mờ, đứng sau. Chỉ ghi thứ **phải còn lại** sau khi tắt máy.

**Cột "Nối với nhau thế nào"** viết bằng câu thường: *"một khách hàng có nhiều đơn"* — không viết
`foreign key`. **Cột "Vào app từ đâu"**: người gõ · nhập một lần từ file đang có · có sẵn cố định.
Thứ *có sẵn cố định* thường là lý do vòng đầu không cần chức năng quản lý nó.

Thứ **tính ra được** thì **không lưu** — ghi vào *"App tự tính, không lưu"* kèm cách tính, và nói câu này
cho họ nghe: *lưu con số tính được là lý do sổ hay lệch.*

Mọi chỗ bạn tự suy → **cột cuối**, đừng lẫn vào cột "mục".

### 8 · Yêu cầu phi chức năng
Phần lớn là **mặc định bạn tự điền** (xem *"Đừng hỏi"* trong SKILL.md) — **không hỏi người dùng từng
dòng**. Mỗi dòng một câu. Thứ bạn tự điền → ghi thêm vào **Giả định** ở phụ lục.

**Bảo mật & riêng tư** chỉ nói **ai được xem gì** và **có dữ liệu nhạy cảm không** — khớp bảng mục 4.
Không viết về mã hoá hay công nghệ.

### 9 · Trường hợp biên & xử lý lỗi
**3–5 tình huống**, mỗi dòng **"Nếu … → app …"**. Hay gặp: nhập thiếu hoặc sai · trùng · làm nhầm
*(huỷ nhầm, trả lại mà không ghi lý do)* · xoá một thứ đang được dùng *(xoá người còn đang giữ việc)* ·
hạn đặt vào ngày đã qua.

Lỗi **chung** cho nhiều F ghi ở đây. Quy tắc **riêng** của một F thì ghi trong F đó — đừng ghi hai lần.

### Phụ lục: Câu hỏi còn mở
Chỗ chưa rõ gắn `[CẦN LÀM RÕ]` **ngay tại chỗ** trong spec, và liệt kê lại ở đây. Hết giờ mà còn câu
chưa hỏi → cũng ghi ở đây. **Giả định** = những thứ bạn tự chọn để họ đọc lại và gạt đi nếu sai.
Không có gì thì ghi *"Không có."*
