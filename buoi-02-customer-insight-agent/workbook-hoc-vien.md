# Buổi 2 · Workbook học viên

**Bạn có 65 phút. Cuối 65 phút bạn phải có 5 thứ:**

1. 1 Customer Insight Agent chạy được
2. Bảng insight tối thiểu 5 dòng, mỗi dòng có trích dẫn ID
3. 5 content angle rút từ data thật
4. 5 bài social
5. 3 brief hình ảnh và 3 visual đăng được

Làm theo đúng thứ tự 6 bước dưới. Đừng nhảy bước. Bước 2 hỏng thì mọi bước sau đều hỏng.

**Bước 7 nằm ở 20 phút cuối buổi, không nằm trong 65 phút này.** Đó là bước mang insight ngược về `CLAUDE.md`, thay 5 nỗi đau bạn đoán ở buổi 1 bằng 5 nỗi đau khách nói thật. Đọc trước cho biết, làm sau.

---

## Checklist chuẩn bị data (làm trong 10 phút đầu)

- [ ] Tôi có tối thiểu **20 mẩu** dữ liệu khách. Một mẩu là một review, một câu hỏi inbox, hoặc một bình luận.
- [ ] Mỗi mẩu đã có **ID**: review là R01, R02...; tin nhắn là M01, M02...; bình luận là C01, C02...
- [ ] Tôi giữ **nguyên văn** khách nói, kể cả sai chính tả. Không sửa cho đẹp.
- [ ] Tôi đã **xóa tên thật, số điện thoại, địa chỉ** của khách.
- [ ] Với review, tôi giữ thêm **số sao** và **tên sản phẩm**.
- [ ] Tôi đã mở lại **thư mục làm việc của buổi 1** bằng tab **Code**, trong đó có `san-pham-thao-an.md` (hoặc hồ sơ sản phẩm của tôi) và `CLAUDE.md`.
- [ ] File data của tôi đã nằm **trong thư mục làm việc đó**, không nằm ở Downloads hay Desktop.

**Bao nhiêu là đủ dùng?**

| Số mẩu | Dùng được không |
|---|---|
| Dưới 15 | Chưa đủ. Tần suất không nói lên gì. Gộp thêm nguồn, hoặc dùng bộ Thảo An. |
| 20 đến 30 | Đủ để làm bài hôm nay và ra 5 angle thật. |
| 50 trở lên | Tốt. Tần suất bắt đầu đáng tin. |
| Trên 200 | Chia theo tháng hoặc theo SKU rồi phân tích từng nhóm, đừng đổ hết một lần. |

**Mẹo gom nhanh khi thiếu:** đừng chỉ lấy review. Câu hỏi trước khi mua mới là nơi nỗi lo lộ ra rõ nhất. Mở lại inbox 30 ngày gần nhất, copy các câu khách hỏi. Thường 30 phút là ra 40 mẩu.

### Bước 0 · Lấy bình luận thật bằng tikhub (làm trong 10 phút chuẩn bị này, chỉ khi bạn đã có tài khoản)

Bước này không bắt buộc. Chưa đăng ký tikhub thì bỏ qua, đi thẳng xuống bước 1, bạn vẫn nộp đủ 5 sản phẩm.

Đã có tài khoản thì đây là cách lấy thêm vài chục mẩu data thật trong mười giây. Lấy bình luận dưới video của chính bạn, hoặc dưới video của đối thủ cùng ngành. Bình luận dưới video đối thủ thường thẳng thắn hơn, vì họ không biết bạn đọc.

**Đọc ba dòng này trước khi gõ:**

- **Mỗi lượt gọi tính tiền bạn trả.** Dịch vụ ghi thẳng "This request will incur a charge". Nghĩ kỹ rồi hãy gọi.
- **Gọi một lần rồi lưu ngay thành file.** Lần sau phân tích lại thì đọc file, không gọi lại. Đây là chỗ tiết kiệm nhiều tiền nhất.
- **Chỉ lấy nội dung công khai.** Bỏ tên tài khoản, ảnh đại diện, đường dẫn trang cá nhân. Chỉ giữ câu người ta viết. Đừng gom thành danh sách người để nhắn tin sau, đó là việc khác và không được làm ở đây.

**Prompt lấy bình luận TikTok:**

```
Dùng công cụ tikhub tên tiktok_app_v3_fetch_video_comments để lấy bình luận
của video này: [dán đường dẫn video TikTok]

Lấy tối đa 50 bình luận. Rồi làm đúng 3 việc:
1. Lưu kết quả thành file binh-luan-tiktok-goc.md ngay trong thư mục làm việc này.
2. Đánh ID cho từng bình luận theo dạng T01, T02, T03...
3. Bỏ tên tài khoản, ảnh đại diện và đường dẫn trang cá nhân của người bình luận.
   Chỉ giữ nguyên văn câu họ viết, giữ cả lỗi chính tả.

Gọi công cụ đúng MỘT lần. Gọi xong báo lại lấy được bao nhiêu bình luận.
Chưa phân tích gì cả.
```

Bài Instagram thì đổi tên công cụ thành `instagram_v3_get_post_comments` và đổi ID thành `I01, I02...`, phần còn lại giữ nguyên.

**Từ đây trở đi, mọi bước sau đọc file này thay vì gọi lại:**

```
Từ giờ dùng dữ liệu trong file binh-luan-tiktok-goc.md đã lưu.
Không gọi lại công cụ tikhub trừ khi tôi yêu cầu rõ ràng.
```

**Ghi lại:** số bình luận lấy được ______ · số lượt gọi đã dùng ______ · tên file đã lưu ______________

> Bình luận thật vẫn phải đánh ID và vẫn phải Ctrl+F kiểm được. Data thật không tự nó thành bằng chứng. Nó chỉ là chữ, và agent vẫn bịa được trên chữ thật.

---

## Chưa có data thật thì làm gì

Dùng nguyên bộ Thảo An: `case-study/thao-an/review-va-tin-nhan-khach.md`. Có sẵn 15 review (R01-R15) và 15 tin nhắn (M01-M15), đã đánh ID. Chép file đó vào thư mục làm việc của bạn trước khi bắt đầu.

Bạn vẫn làm đủ 6 bước và nộp đủ 5 sản phẩm. Kỹ thuật học được y hệt. Về công ty chỉ việc thay file data, giữ nguyên agent.

Nếu bạn có data thật nhưng ít (dưới 15 mẩu): làm hai lượt. Lượt một trên bộ Thảo An để nắm tay, lượt hai trên data của mình để thấy nó ra gì. So sánh hai bảng cũng là một bài học.

---

## Bước 1 · Nạp agent và bắt nó đếm (7 phút)

**1.1** Mở Claude Desktop, tab **Code**, mở thư mục làm việc của buổi 1.

**1.2** Cài skill `customer-insight`. Mở file `system-prompt.md` của buổi 2, copy toàn bộ phần trong code block (gồm cả ba dấu gạch và hai dòng `name`, `description`), rồi gõ vào ô nhập:

```
Tạo file .claude/skills/customer-insight/SKILL.md trong thư mục làm việc này,
tạo luôn thư mục cha nếu chưa có. Nội dung như sau: [dán nội dung vừa copy]
```

Claude xin phép ghi file thì bấm **Yes**. Làm một lần, dùng mãi. Buổi sau không phải dán lại.

**1.3** Kiểm tra file data của bạn đã nằm trong thư mục làm việc chưa. Chưa thì kéo thả vào.

**1.4** Chạy prompt này. Đừng bỏ qua, đây là bước bắt agent tự khai chỗ nó không biết:

```
Đọc file data khách hàng trong thư mục này. Trước khi phân tích, làm đúng 3 việc:
1. Đếm và báo lại: tổng bao nhiêu mẩu, chia theo từng loại nguồn.
2. Liệt kê các sản phẩm hoặc dịch vụ xuất hiện trong data.
3. Nói cho tôi biết dữ liệu này KHÔNG trả lời được những câu hỏi nào.

Chưa rút insight vội. Chỉ làm 3 việc trên.
```

**Ghi lại kết quả:**

- Tổng số mẩu agent đếm được: ______ (khớp với số bạn đếm tay chưa? ☐ khớp ☐ lệch)
- Ba chỗ data không trả lời được:
  1. ______________________________
  2. ______________________________
  3. ______________________________

> Agent đếm lệch số mẩu thì dừng lại, kiểm file data trước khi đi tiếp. Đếm sai ở đây là mọi tần suất phía sau sai.

---

## Bước 2 · Ra bảng insight (14 phút)

Đây là bước quan trọng nhất. Dành đủ thời gian.

**2.1** Chạy prompt:

```
Bây giờ phân tích toàn bộ data.

Bước 1: gom các mẩu nói cùng một chuyện vào một nhóm chủ đề. Một mẩu được nằm ở nhiều nhóm nếu nó nói nhiều chuyện.

Bước 2: với mỗi nhóm, viết một pain theo cấu trúc:
[nhóm khách nào] + [lo hoặc muốn điều gì] + [vì sao]

Bước 3: xuất bảng markdown đúng các cột sau, xếp giảm dần theo tần suất:

| # | Pain | Tần suất | Trích dẫn ID | Nguyên văn 1 câu tiêu biểu | Nhãn |

Quy tắc bắt buộc:
- Tần suất ghi dạng "x/[tổng số mẩu]". Cấm dùng: đa số, rất nhiều, phần lớn, hầu hết.
- Cột Trích dẫn ID liệt kê ĐỦ ID đã đếm, không viết tắt kiểu "và các mẩu khác".
- Số ID liệt kê phải khớp đúng với x. Không khớp thì sửa x, không sửa danh sách ID.
- Cột Nguyên văn copy đúng ký tự từ file, không viết lại cho mượt.
- Nhãn ghi [DATA THẬT] hoặc [SUY LUẬN].
```

**2.2** Kiểm ngay, đừng đi tiếp: chọn 2 dòng bất kỳ, lấy 1 ID mỗi dòng, Ctrl+F trong file data gốc. Không khớp nguyên văn 100% thì chạy prompt sửa:

```
Trích dẫn ở dòng số ... không khớp nguyên văn file gốc.
Rà lại toàn bộ cột Nguyên văn, copy đúng ký tự từ data, không diễn đạt lại.
Dòng nào không tìm được câu gốc thì xóa dòng đó.
```

**2.3** Chép bảng của bạn vào đây (tối thiểu 5 dòng):

| # | Pain | Tần suất | Trích dẫn ID | Persona liên quan | Nhãn |
|---|---|---|---|---|---|
| 1 |  | /  |  |  |  |
| 2 |  | /  |  |  |  |
| 3 |  | /  |  |  |  |
| 4 |  | /  |  |  |  |
| 5 |  | /  |  |  |  |
| 6 |  | /  |  |  |  |
| 7 |  | /  |  |  |  |

**2.4** Tách hai nhóm. Đánh dấu vào bảng trên:

- **Pain ra nội dung:** nỗi lo, thắc mắc, do dự trước mua. Những dòng này đi tiếp sang bước 4.
- **Pain vận hành:** giao hàng, đổi trả, thanh toán, kênh bán. Những dòng này **không viết bài**, ghi ra một danh sách riêng chuyển cho bộ phận liên quan.

Pain vận hành của tôi: ______________________________________

---

## Bước 3 · Dựng persona (7 phút)

```
Từ bảng insight trên, dựng tối đa 3 persona.

Mỗi persona ghi:
- Tên gọi ngắn, đặt theo nỗi lo, không đặt theo tuổi hay nghề nghiệp
- Nỗi lo chính, kèm ID
- Câu họ thật sự đang hỏi trong đầu (trích nguyên văn 1 mẩu)
- Cái họ cần thấy để yên tâm mua
- Sản phẩm hoặc gói phù hợp nhất và lý do

Ràng buộc:
- Không bịa tuổi, nghề, thu nhập, nơi ở. Data không có thì ghi "chưa đủ dữ liệu".
- Mỗi persona phải gắn được tối thiểu 3 ID.
```

**Ghi lại 3 persona:**

| Persona | Nỗi lo chính | ID | Cần thấy gì để mua |
|---|---|---|---|
| A. |  |  |  |
| B. |  |  |  |
| C. |  |  |  |

> Persona của bạn có tuổi, nghề, sở thích không? Nếu có mà data không nói tới thì xóa đi. Chi tiết bịa nghe sinh động và dẫn cả quý đi sai.

---

## Bước 4 · Năm content angle (10 phút)

```
Từ bảng insight và 3 persona trên, đề xuất 5 content angle.

Mỗi angle ghi đúng 4 dòng:
- Tên angle (1 câu, viết như tiêu đề khách sẽ đọc)
- Bám pain số mấy, tần suất bao nhiêu
- Trích dẫn ID làm bằng chứng
- Persona nhắm tới

Ràng buộc:
- 5 angle phải bám tối thiểu 4 pain KHÁC NHAU.
- Phép thử trước khi xuất: nếu thay tên thương hiệu tôi bằng tên đối thủ mà angle vẫn dùng được thì loại, viết lại angle khác.
- Đối chiếu mục "Điều KHÔNG được nói" trong hồ sơ sản phẩm của tôi. Không angle nào được hứa mốc thời gian có kết quả.
```

**Ghi lại 5 angle:**

| # | Tên angle | Bám pain số | Tần suất | ID bằng chứng | Persona |
|---|---|---|---|---|---|
| 1 |  |  | / |  |  |
| 2 |  |  | / |  |  |
| 3 |  |  | / |  |  |
| 4 |  |  | / |  |  |
| 5 |  |  | / |  |  |

**Tự thử ngay:** đọc to angle số 1, thay tên thương hiệu bạn bằng tên đối thủ. Vẫn dùng được không?
☐ Vẫn dùng được, phải viết lại  ☐ Không dùng được, angle đạt

---

## Bước 5 · Năm bài social (10 phút)

```
Viết 5 bài đăng cho kênh chính của tôi, mỗi bài cho một angle ở trên.

Yêu cầu mỗi bài:
- Dài 120 đến 200 chữ
- Câu mở đầu lấy từ chính nỗi lo của khách, không mở bằng lời khen sản phẩm
- Có tối thiểu 1 câu trích nguyên văn khách, ghi rõ trích từ ID nào
- Kết bằng 1 lời mời hành động nhẹ, không giục
- Đúng phần giọng văn và danh sách từ cấm trong file CLAUDE.md của thư mục này

Cấm: hứa mốc thời gian có kết quả, so sánh đích danh thương hiệu khác, và mọi từ trong mục "Điều KHÔNG được nói".

Cuối mỗi bài, xuống dòng ghi: Nguồn insight: pain số ..., ID ...
```

**Rà lại trước khi tính là xong:**

```
Rà 5 bài vừa viết, đối chiếu mục "Điều KHÔNG được nói" trong hồ sơ sản phẩm.
Liệt kê từng câu vi phạm kèm số bài, đề xuất câu thay thế.
Không tự sửa. Chỉ liệt kê để tôi duyệt.
```

**Đánh dấu khi xong:**

| Bài | Angle | Có trích nguyên văn khách? | Có dòng nguồn insight? | Đã rà từ cấm? |
|---|---|---|---|---|
| 1 |  | ☐ | ☐ | ☐ |
| 2 |  | ☐ | ☐ | ☐ |
| 3 |  | ☐ | ☐ | ☐ |
| 4 |  | ☐ | ☐ | ☐ |
| 5 |  | ☐ | ☐ | ☐ |

> Khi đăng thật thì xóa dòng "Nguồn insight" đi. Giữ trong bản nộp để giảng viên kiểm.

---

## Bước 6 · Ba brief hình ảnh và ba visual (7 phút)

**6.1** Viết brief:

```
Viết 3 brief hình ảnh cho 3 bài trong số 5 bài trên. Chọn 3 bài bám 3 pain khác nhau.

Mỗi brief đủ 5 mục:
1. Thông điệp một câu mà người xem phải hiểu trong 2 giây
2. Bố cục (đặt gì ở đâu, chữ chính chiếm bao nhiêu phần)
3. Chữ trên ảnh (tối đa 8 chữ, viết ra chính xác)
4. Màu và tông (bám phần giọng văn trong CLAUDE.md)
5. Điều cấm trong ảnh

Mỗi brief ghi thêm: bám pain số mấy, ID nào.
```

**Ghi lại 3 brief:**

| # | Bài số | Thông điệp 2 giây | Chữ trên ảnh (tối đa 8 chữ) | Điều cấm trong ảnh | Pain / ID |
|---|---|---|---|---|---|
| 1 |  |  |  |  |  |
| 2 |  |  |  |  |  |
| 3 |  |  |  |  |  |

**6.2** Tạo visual. Chọn một trong hai đường:

*Đường A: Claude Artifacts (chọn khi cần chữ tiếng Việt sắc nét)*

```
Từ brief số 1, tạo một Artifact HTML kích thước 1080x1080, hiển thị đúng brief.
Yêu cầu:
- Chữ tiếng Việt có dấu, cỡ chữ chính đủ lớn để đọc trên điện thoại
- Nền phẳng theo tông màu trong brief, không dùng ảnh từ internet
- Toàn bộ nằm gọn trong khung vuông, không tràn
```

*Đường B: công cụ ảnh AI (chọn khi cần ảnh sản phẩm hoặc nền có chất liệu)*

```
Từ brief số 1, viết cho tôi 1 prompt tạo ảnh bằng công cụ ảnh AI.
Yêu cầu prompt:
- Mô tả bối cảnh, ánh sáng, góc chụp, tông màu
- KHÔNG có chữ trong ảnh (chữ sẽ chèn sau để đảm bảo tiếng Việt đúng dấu)
Viết prompt bằng tiếng Anh, kèm bản dịch tiếng Việt để tôi kiểm.
```

**6.3** Đánh dấu: ☐ visual 1 ☐ visual 2 ☐ visual 3 (mở xem được, chữ không tràn, đọc được trên điện thoại)

---

## Bước 7 · Trả lời hứa của buổi 1: thay 5 nỗi đau đoán bằng 5 nỗi đau thật

**Bước này làm ở 20 phút cuối buổi, không nằm trong 65 phút thực hành.**

Buổi 1 bạn nhờ Claude viết `CLAUDE.md`, trong đó có mục 5 nỗi đau khách. Lúc đó bạn chưa có một dòng review nào, nên cả 5 dòng đều gắn nhãn `[SUY LUẬN]`. Đó là chủ ý, không phải thiếu sót. Giờ bạn đã có bảng insight rút từ data thật. Đây là lúc thay.

**7.1** Lưu bảng insight thành file, đừng để nó nằm trong cửa sổ chat:

```
Lưu bảng insight, danh sách pain vận hành, 3 persona và 5 content angle vừa làm
thành file insight-khach-hang.md ngay trong thư mục làm việc này.

Giữ nguyên cột Trích dẫn ID và cột Nguyên văn. Không rút gọn, không bỏ ID.
Đầu file ghi 3 dòng: ngày phân tích, tên file data nguồn, tổng số mẩu.
Cuối file giữ nguyên mục "Chỗ còn thiếu dữ liệu".
```

**7.2** Cập nhật `CLAUDE.md`. Chạy đúng prompt này:

```
Mở file CLAUDE.md trong thư mục này, tìm mục 5 nỗi đau khách (hoặc mục chân dung
khách). Cả 5 dòng đang gắn nhãn [SUY LUẬN] vì buổi trước tôi chưa có data.

Giờ đọc file insight-khach-hang.md vừa lưu, rồi viết lại mục đó theo đúng quy tắc sau:

1. Mỗi nỗi đau lấy từ bảng insight, ưu tiên theo tần suất giảm dần.
2. Mỗi dòng ghi đủ 4 phần: nỗi đau viết bằng lời khách; tần suất dạng x/tổng;
   danh sách đủ mã trích dẫn; nhãn [DATA THẬT].
3. Kèm một câu nguyên văn khách nói, copy đúng ký tự, đặt trong ngoặc kép.
4. Nỗi đau nào KHÔNG gắn được mã trích dẫn thì GIỮ NGUYÊN nhãn [SUY LUẬN].
   Không đổi nhãn cho đủ 5 dòng.
5. Nỗi đau vận hành (giao hàng, thanh toán, đổi trả) không đưa vào mục này.
   Ghi riêng thành một dòng ở cuối, đánh dấu là việc của bộ phận vận hành.

Trước khi ghi đè, cho tôi xem bảng so sánh 2 cột: bên trái là 5 dòng cũ tôi đoán,
bên phải là dòng mới từ data. Dòng nào tôi đoán trật thì ghi rõ trật ở chỗ nào.
Tôi duyệt xong bạn mới ghi vào file.
```

**7.3** Đọc bảng so sánh trước khi bấm duyệt. Đây là chỗ đáng tiền nhất của cả buổi. Ghi lại ngay:

| | Số dòng |
|---|---|
| Nỗi đau tôi đoán ở buổi 1 mà data xác nhận đúng | ______ |
| Nỗi đau tôi đoán mà data không hề nhắc tới | ______ |
| Nỗi đau data chỉ ra mà tôi chưa từng nghĩ tới | ______ |

Dòng cuối cùng là dòng quan trọng nhất. Đó là thứ bạn đang bỏ lỡ suốt thời gian qua.

**7.4** Mở lại `CLAUDE.md`, đọc mục vừa sửa, kiểm đúng ba thứ:

- [ ] Không còn dòng nào gắn `[SUY LUẬN]` mà lại có mã trích dẫn (mâu thuẫn, sửa lại)
- [ ] Không còn dòng nào gắn `[DATA THẬT]` mà cột mã trích dẫn để trống (đây là bịa)
- [ ] Ctrl+F thử 2 câu nguyên văn trong file data gốc, cả 2 phải khớp từng ký tự

> Từ giờ, mọi bài viết Claude làm trong thư mục này đều đọc `CLAUDE.md` trước. Tức là mọi bài từ hôm nay trở đi đều bám nỗi đau thật, không phải nỗi đau bạn tưởng. Bạn không phải nhắc lại lần nào nữa.

---

## Checklist tự kiểm trước khi nộp

Đọc từng dòng, đánh dấu thật. Dòng nào chưa tick thì sửa trong 20 phút cuối.

**Về bảng insight**

- [ ] Bảng có tối thiểu 5 dòng
- [ ] **Mỗi insight có trích dẫn ID chưa?** Không dòng nào để trống cột này
- [ ] Mỗi dòng có tối thiểu 2 ID
- [ ] Tần suất ghi dạng x/tổng, không có chữ "đa số", "rất nhiều", "phần lớn"
- [ ] Tôi đã tự Ctrl+F kiểm ít nhất 3 trích dẫn ngẫu nhiên, tất cả khớp nguyên văn
- [ ] Có ít nhất 1 chỗ agent ghi "chưa đủ dữ liệu"
- [ ] Phần agent tự suy ra đều có nhãn `[SUY LUẬN]`
- [ ] Tôi đã tách riêng pain vận hành ra khỏi pain ra nội dung

**Về persona**

- [ ] Tối đa 3 persona, mỗi persona gắn tối thiểu 3 ID
- [ ] Không persona nào có tuổi, nghề, thu nhập bịa ra từ hư không

**Về content angle**

- [ ] Đủ 5 angle
- [ ] Bám tối thiểu 4 pain khác nhau
- [ ] Mỗi angle truy ngược được về ID cụ thể
- [ ] Không angle nào thay được tên thương hiệu mà vẫn dùng được

**Về bài social**

- [ ] Đủ 5 bài
- [ ] Mỗi bài có tối thiểu 1 câu trích nguyên văn khách
- [ ] Đã rà một lượt đối chiếu "Điều KHÔNG được nói", không còn câu vi phạm
- [ ] Không bài nào hứa mốc thời gian có kết quả
- [ ] Đọc lên nghe ra đúng thương hiệu mình, không phải giọng chung chung

**Về hình ảnh**

- [ ] Đủ 3 brief, mỗi brief đủ 5 mục
- [ ] Đủ 3 visual, mở xem được
- [ ] Chữ trên visual đúng chính tả tiếng Việt, không tràn khung

**Cuối cùng**

- [ ] Tôi đã lưu bảng insight, persona và 5 angle thành file **`insight-khach-hang.md`** ngay trong thư mục làm việc, cạnh `CLAUDE.md`
- [ ] Skill `customer-insight` nằm đúng chỗ: `.claude/skills/customer-insight/SKILL.md`
- [ ] Tôi đã làm bước 7: mục 5 nỗi đau trong `CLAUDE.md` không còn nhãn `[SUY LUẬN]`, mỗi dòng có mã trích dẫn và tần suất
- [ ] Ai lấy data bằng tikhub: file `binh-luan-tiktok-goc.md` đã lưu trong thư mục, và tôi không gọi lại công cụ nữa

> Vì sao phải lưu thành file trong thư mục: buổi 3 dùng persona để cá nhân hóa email sale, buổi 4 dùng cả bảng insight để dựng chiến dịch 14 ngày. File nằm trong thư mục thì buổi sau mở tab Code lên là Claude đọc được ngay, không phải dán lại. Để rời trong cửa sổ chat thì hai buổi sau phải làm lại từ đầu.

---

## Ba câu hỏi tự trả lời trước khi rời lớp

1. Pain số 1 của tôi có tần suất bao nhiêu, và tôi có dám nói con số đó trước mặt sếp không?
2. Ba chỗ data không trả lời được là gì, và tháng sau tôi thêm câu hỏi nào để lấp?
3. Nếu ai đó hỏi "dựa vào đâu bạn viết bài này", tôi mở file nào ra để trả lời trong 10 giây?
