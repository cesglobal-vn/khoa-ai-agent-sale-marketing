# Buổi 2 · Kịch bản demo 35 phút

> Giảng viên chạy đúng file này, chiếu màn hình cho lớp xem. Cả buổi chạy trong Claude Desktop, tab **Code**, mở sẵn thư mục làm việc của buổi 1.
> Dữ liệu chính: `case-study/thao-an/review-va-tin-nhan-khach.md` (15 review R01-R15, 15 tin nhắn M01-M15, tổng 30 mẩu).
> Dữ liệu thật dùng ở mốc đầu: bình luận lấy sống từ một video TikTok bằng tikhub, lưu thành `binh-luan-tiktok-goc.md`.

## Chuẩn bị trước khi vào lớp (làm trước 10 phút)

- Mở Claude Desktop, tab **Code**, mở thư mục làm việc `thao-an-marketing` đã tạo buổi 1. Trong đó có sẵn `san-pham-thao-an.md` (hồ sơ sản phẩm, danh sách điều không được nói) và `CLAUDE.md` (giọng văn, từ cấm, 5 nỗi đau đang gắn `[SUY LUẬN]`).
- Chép file `review-va-tin-nhan-khach.md` vào thư mục làm việc đó.
- Mở sẵn tab thứ hai chứa file `review-va-tin-nhan-khach.md` dạng chữ, để lát nữa Ctrl+F kiểm trích dẫn ngay trước mặt lớp.
- Đã cài sẵn skill `customer-insight` theo `system-prompt.md` của buổi 2, đường dẫn `.claude/skills/customer-insight/SKILL.md`, và đã chạy thử một lượt.
- **Đã nối tikhub trên máy giảng viên và đã chạy thử một lượt gọi lấy bình luận.** Chọn sẵn 1 video TikTok ngành mỹ phẩm đang có nhiều bình luận, chép sẵn đường dẫn ra giấy nhắc. Chụp sẵn ảnh màn hình kết quả để dùng khi mạng hỏng hoặc gọi lỗi.
- **Đừng chạy trước cả luồng rồi chiếu kết quả.** Lớp cần thấy agent trả lời trực tiếp, kể cả khi nó trả lời hơi lệch. Chỗ lệch là chỗ dạy được.

---

## Mốc 0 đến 5 phút · Lấy bình luận thật bằng tikhub

**Nói trước khi gõ:**

> Trước khi phân tích, tôi lấy data đã. Bộ 30 mẩu của Thảo An lát nữa ta dùng là data giả định, tôi dựng ra để dạy. Còn đây là bình luận thật, của người thật, dưới một video thật đang chạy trên TikTok sáng nay. Anh chị nhìn kỹ chỗ khác nhau.

**Thao tác:** trong tab Code, đang mở thư mục làm việc, dán prompt sau. Thay đường dẫn bằng video đã chọn trước buổi.

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

**Kết quả mong đợi:** Claude xin phép gọi công cụ, giảng viên bấm đồng ý, vài giây sau trong thư mục xuất hiện file `binh-luan-tiktok-goc.md`, bên trong là các mẩu T01, T02, T03 chỉ còn nguyên văn câu nói.

**Thao tác tiếp:** mở file đó ra, chiếu cho lớp thấy vài mẩu, rồi chạy đúng một prompt ngắn để lớp thấy insight rút từ data thật vẫn trích dẫn được:

```
Đọc file binh-luan-tiktok-goc.md. Rút đúng 3 điều khách đang nói nhiều nhất.
Mỗi điều ghi 3 thứ: tần suất dạng x/[tổng số mẩu], danh sách đủ ID,
và một câu nguyên văn copy đúng ký tự từ file.
Điều nào không gắn được ID thì bỏ, đừng viết cho đủ ba.
```

Rồi Ctrl+F một trích dẫn ngay trong file, trước mặt lớp.

**Ba câu phải nói, không bỏ câu nào:**

> Một: mỗi lần gọi như vừa rồi là tốn tiền. Dịch vụ ghi thẳng "This request will incur a charge". Nên tôi bảo nó gọi đúng một lần và lưu ngay thành file. Lát nữa muốn phân tích lại thì đọc file, không gọi lại. Anh chị cũng làm y như vậy, vì tài khoản tikhub là tiền của anh chị.

> Hai: tôi bảo nó bỏ tên và ảnh người bình luận. Ta đọc điều khách nói, không dựng danh sách người. Đây không phải phép lịch sự, đây là ranh giới.

> Ba: data thật rồi vẫn phải đánh ID, vẫn phải Ctrl+F kiểm. Bình luận thật cũng chỉ là chữ, và agent vẫn bịa được trên chữ thật. Data thật không tự nó thành bằng chứng.

**Nếu tikhub gọi lỗi, hết phí, hoặc mạng chậm:** không sửa giữa lớp. Chiếu ảnh chụp đã chuẩn bị, nói rõ "đây là kết quả tôi chạy sáng nay", rồi chuyển thẳng sang bộ `review-va-tin-nhan-khach.md`. Phần còn lại của buổi chạy y hệt, chỉ đổi file data.

**Ai trong lớp chưa đăng ký tikhub:** nói ngay và nói gọn, đừng để họ ngồi lo. "Anh chị chưa có tài khoản thì lát nữa dùng bộ Thảo An, ra đủ sản phẩm, không thiếu gì cả. Đăng ký sau buổi rồi thay file data là chạy được ngay."

---

## Mốc 5 đến 8 phút · Nạp agent và data

**Thao tác:** trong tab Code, mở phiên mới trong thư mục làm việc. Gõ một câu tự nhiên để Claude tự rút skill `customer-insight` ra, không gọi đích danh tên skill. Rồi chỉ cho nó file `review-va-tin-nhan-khach.md` đang nằm trong thư mục.

**Nói với lớp khi skill được gọi ra:** "Anh chị để ý, tôi không dán một chữ system prompt nào. Cái quy trình dài ba trang tôi đã lưu thành file skill từ trước, giống hệt cách buổi 1 làm với skill viết bài. Tôi chỉ nói việc, nó tự rút hồ sơ ra."

**Prompt mở màn:**

```
Đọc file review-va-tin-nhan-khach.md trong thư mục này. Đây là dữ liệu khách hàng của Thảo An: 15 review Shopee (R01-R15) và 15 tin nhắn inbox Facebook (M01-M15).

Trước khi phân tích, làm đúng 3 việc:
1. Đếm và báo lại: tổng bao nhiêu mẩu, bao nhiêu review, bao nhiêu tin nhắn.
2. Liệt kê các SKU xuất hiện trong data.
3. Nói cho tôi biết dữ liệu này KHÔNG trả lời được những câu hỏi nào.

Chưa rút insight vội. Chỉ làm 3 việc trên.
```

**Kết quả mong đợi:** agent báo 30 mẩu, 15 review, 15 tin nhắn; liệt kê serum rau má, kem nghệ mật ong, mặt nạ đất sét, combo; và nêu các chỗ thiếu: tỉnh thành khách, tỷ lệ mua lại, lý do nhắn rồi không mua.

**Nói với lớp:**

> Việc đầu tiên không phải hỏi insight. Việc đầu tiên là bắt agent đếm. Nếu nó đếm sai số mẩu ngay từ đầu thì mọi con số tần suất phía sau đều sai. Và để ý câu số 3: tôi đang bắt nó tự khai chỗ nó không biết, trước khi nó kịp bịa.

---

## Mốc 8 đến 15 phút · Ra bảng insight có trích dẫn

**Thao tác:** chạy prompt chính. Đây là prompt xương sống của cả buổi.

```
Bây giờ phân tích toàn bộ 30 mẩu.

Bước 1: gom các mẩu nói cùng một chuyện vào một nhóm chủ đề. Một mẩu được nằm ở nhiều nhóm nếu nó nói nhiều chuyện.

Bước 2: với mỗi nhóm, viết ra một pain theo đúng cấu trúc:
[nhóm khách nào] + [lo hoặc muốn điều gì] + [vì sao]

Bước 3: xuất ra bảng markdown đúng các cột sau, xếp giảm dần theo tần suất:

| # | Pain | Tần suất | Trích dẫn ID | Nguyên văn 1 câu tiêu biểu | Nhãn |

Quy tắc bắt buộc:
- Tần suất ghi đúng dạng "x/30". Cấm dùng: đa số, rất nhiều, phần lớn, hầu hết.
- Cột Trích dẫn ID liệt kê ĐỦ các ID đã đếm, không viết tắt kiểu "R01 và các mẩu khác".
- Số ID liệt kê phải khớp đúng với x. Không khớp thì sửa x.
- Cột Nguyên văn copy đúng ký tự từ file, không viết lại cho mượt.
- Nhãn ghi [DATA THẬT] hoặc [SUY LUẬN].
```

**Kết quả mong đợi:** bảng 6 đến 8 dòng. Dòng đầu là nỗi lo kích ứng và an toàn, khoảng 9/30. Đối chiếu với bảng chuẩn trong `giao-an.md`.

**Thao tác quan trọng nhất buổi:** dừng lại. Phóng to cột **Trích dẫn ID**. Chỉ tay vào đó.

**Nói với lớp:**

> Đây là chỗ kiểm chứng được. Cả bảng này, chỉ có cột này đáng tin. Mọi cột khác là chữ, mà chữ thì mô hình nào cũng viết hay được.

Rồi làm luôn thao tác kiểm trước mặt lớp:

- Đọc to dòng 1, lấy ID đầu tiên, ví dụ R01.
- Chuyển sang tab chứa file gốc, Ctrl+F gõ "không bị rát".
- Chỉ vào kết quả: khớp.
- Làm lại với một ID nữa, chọn ngẫu nhiên, tốt nhất chọn ID ở dòng cuối bảng (chỗ agent hay ẩu nhất).

> Năm giây. Đó là toàn bộ chi phí để biết agent có bịa hay không. Ai không làm việc năm giây này thì đang mang số liệu bịa đi họp.

**Điểm nghề chỉ ra ngay trên bảng:**

1. Nỗi lo kích ứng chiếm 9/30, gấp đôi mọi pain khác. Nhưng nó không nằm ở review chê: bộ này không có review nào dưới 2 sao, và **5 trong 9 mẩu là tin nhắn hỏi trước khi mua** (M01, M02, M04, M06, M10). Ai chỉ đọc review thì mất hơn nửa pain lớn nhất.
2. Cả 4 review 4 sao đều kèm một câu chê cụ thể: R03 chê giá và dung tích, R07 chê kem đặc, R10 chê khô căng, R15 chê giao chậm. Review 4 sao là nơi khách nói thật nhất.
3. Pain "giao chậm, muốn COD, mua kênh nào" (R15, M09, M11) là pain vận hành. Không viết bài về nó. Chuyển cho vận hành.

---

## Mốc 15 đến 19 phút · Cố tình bắt lỗi

**Thao tác:** hỏi một câu mà data không trả lời được. Không báo trước cho lớp.

```
Dựa trên data này, cho tôi biết:
1. Khách của Thảo An chủ yếu ở tỉnh thành nào?
2. Tỷ lệ khách mua lần đầu so với khách mua lại là bao nhiêu?
3. Nhóm khách nào nhắn tin nhiều nhất rồi không mua, và vì sao họ không mua?
```

**Kết quả mong đợi:** agent trả lời "chưa đủ dữ liệu" cho cả ba câu. Có thể nó nói thêm phần suy luận, nhưng phải gắn nhãn `[SUY LUẬN]` rõ ràng, ví dụ: tin nhắn dồn về khung 20h đến 23h nên `[SUY LUẬN]` khách nhiều khả năng là người đi làm, nhưng data không xác nhận.

**Nói với lớp:**

> Ba câu vừa rồi là ba câu sếp hay hỏi nhất. Và data này không trả lời được câu nào. Các bạn thấy nó nói "chưa đủ dữ liệu" chứ không đưa ra con số 60/40 nào đó nghe rất hợp lý. Cái đó không tự nhiên mà có, nó nằm trong system prompt các bạn sắp dán.

**Nếu agent lỡ bịa** (thỉnh thoảng có, nhất là câu 3): đừng che. Đây là món quà. Chỉ vào chỗ bịa, rồi chạy prompt sửa ngay để lớp thấy cách xử lý:

```
Câu trả lời vừa rồi có chỗ không trích dẫn được từ data.
Rà lại từng câu bạn vừa viết. Câu nào không gắn được ID thì xóa hoặc đổi thành "chưa đủ dữ liệu".
Liệt kê cho tôi những câu bạn vừa xóa và lý do.
```

> Agent bịa không phải lỗi của các bạn. Không phát hiện ra mới là lỗi của các bạn.

**Câu chốt phần này:**

> Ba chỗ thiếu vừa rồi cũng là danh sách việc phải làm. Muốn biết khách ở tỉnh nào thì tháng sau thêm một câu hỏi vào form đặt hàng. Insight tốt luôn đẻ ra một việc phải làm cho tháng sau.

---

## Mốc 19 đến 22 phút · Dựng persona

**Thao tác:** từ bảng insight ra persona, vẫn ép trích dẫn.

```
Từ bảng insight trên, dựng tối đa 3 persona.

Mỗi persona ghi:
- Tên gọi ngắn (đặt theo nỗi lo, không đặt theo nhân khẩu học)
- Nỗi lo chính, kèm ID
- Câu họ thật sự đang hỏi trong đầu (trích nguyên văn 1 mẩu)
- Cái họ cần thấy để yên tâm bấm mua
- SKU phù hợp nhất và lý do

Ràng buộc:
- Không bịa tuổi, nghề, thu nhập, nơi ở. Data không có thì ghi "chưa đủ dữ liệu".
- Mỗi persona phải gắn được tối thiểu 3 ID.
```

**Kết quả mong đợi:** ba persona kiểu này:
- "Người từng bị kích ứng": R01, R11, M01, M02, M06, M10. Cần thấy giấy test da liễu và bảng thành phần đọc được.
- "Người mụn ẩn và thâm chưa biết chọn gì": M03, M12, R02. Cần một bảng chọn theo tình trạng da.
- "Người đang cân giá": R03, R13, M07, M08, M14. Cần biết dùng được bao lâu với số tiền đó.

**Nói với lớp:**

> Để ý persona không có tuổi, không có nghề, không có "chị Lan 32 tuổi ở Hà Nội, thích yoga". Vì data không nói điều đó. Persona bịa nhân khẩu học nghe rất sinh động và dẫn ta đi sai suốt cả quý. Persona đặt tên theo nỗi lo thì viết bài xong biết ngay bài đó cho ai.

---

## Mốc 22 đến 28 phút · Insight ra content angle rồi ra bài social

**Thao tác bước 1:** chuyển pain thành angle.

```
Từ bảng insight và 3 persona trên, đề xuất 5 content angle.

Mỗi angle ghi đúng 4 dòng:
- Tên angle (1 câu, viết như tiêu đề khách sẽ đọc)
- Bám pain số mấy, tần suất bao nhiêu
- Trích dẫn ID làm bằng chứng
- Persona nhắm tới

Ràng buộc:
- 5 angle phải bám tối thiểu 4 pain KHÁC NHAU.
- Phép thử trước khi xuất: nếu thay tên Thảo An bằng tên một thương hiệu khác mà angle vẫn dùng được thì angle đó bị loại, viết lại angle khác.
- Đối chiếu mục "Điều KHÔNG được nói" trong hồ sơ sản phẩm. Không angle nào được hứa mốc thời gian hay dùng từ trị mụn, đặc trị.
```

**Kết quả mong đợi:** 5 angle bám data, ví dụ:
1. "Từng đổi mỹ phẩm rồi nổi mẩn? Đọc trước khi đổi lần nữa" (pain 1, 9/30, R11 M06)
2. "Bóc nhãn: đọc từng dòng thành phần, cái nào là cái gì" (pain 4, 5/30, R04 M02 M04)
3. "Một tuần chưa thấy gì, có phải là hỏng không" (pain 5, 4/30, R05 M05)
4. "30ml giá 320k là đắt hay rẻ: tính theo mỗi lần dùng" (pain 2, 5/30, R03 M07)
5. "Da bạn thế nào thì hợp món nào: bảng chọn 1 phút" (pain 6, 3/30, M03 M12 R12)

**Nói với lớp khi chiếu 5 angle:**

> Nhìn angle số 3. Nó sinh ra từ một review 3 sao, R05, chỉ có một người nói. Nhưng cộng với M05 và M15 là ba mẩu, và nó chạm đúng lúc khách sắp bỏ cuộc. Insight tần suất thấp mà đúng thời điểm quyết định vẫn đáng viết. Tần suất dùng để xếp thứ tự, không phải để loại bỏ.

**Thao tác bước 2:** ra bài social.

```
Viết 5 bài đăng Facebook, mỗi bài cho một angle ở trên.

Yêu cầu mỗi bài:
- Dài 120 đến 200 chữ
- Câu mở đầu lấy từ chính nỗi lo của khách, không mở bằng lời khen sản phẩm
- Có tối thiểu 1 câu trích nguyên văn khách, ghi rõ trích từ ID nào (khi đăng thật sẽ bỏ ID, giữ để tôi kiểm)
- Kết bằng 1 lời mời hành động nhẹ, không giục
- Đúng phần giọng văn và danh sách từ cấm trong file CLAUDE.md của thư mục này

Cấm tuyệt đối: trị mụn, đặc trị, khỏi hẳn, trắng da cấp tốc, hứa mốc thời gian có kết quả, so sánh đích danh thương hiệu khác.

Cuối mỗi bài, xuống dòng ghi: Nguồn insight: pain số ..., ID ...
```

**Kết quả mong đợi:** 5 bài, mỗi bài có dòng truy nguồn ở cuối.

**Nói với lớp:**

> Dòng "Nguồn insight" ở cuối mỗi bài chính là thứ phân biệt bài viết bằng data với bài viết bằng cảm hứng. Khi sếp hỏi vì sao tháng này viết chủ đề kích ứng thì bạn chỉ vào dòng đó. Khi đăng thật thì xóa dòng này đi.

Chạy thêm một lượt rà cho lớp thấy thói quen tự kiểm:

```
Rà lại 5 bài vừa viết, đối chiếu mục "Điều KHÔNG được nói".
Liệt kê từng câu vi phạm kèm số bài và đề xuất câu thay.
Không tự sửa. Chỉ liệt kê để tôi duyệt.
```

> Để ý chữ cuối: không tự sửa, chỉ liệt kê để tôi duyệt. Nguyên tắc số 3, người duyệt cuối. Agent không được tự tay đổi nội dung rồi im lặng.

---

## Mốc 28 đến 32 phút · Brief hình ảnh và tạo visual

**Thao tác bước 1:** viết brief.

```
Viết 3 brief hình ảnh cho 3 bài trong số 5 bài trên (chọn bài 1, 2, 4).

Mỗi brief đủ 5 mục:
1. Thông điệp một câu mà người xem phải hiểu trong 2 giây
2. Bố cục (đặt gì ở đâu, chữ chính chiếm bao nhiêu phần)
3. Chữ trên ảnh (tối đa 8 chữ, viết ra chính xác)
4. Màu và tông (bám phần giọng văn trong CLAUDE.md)
5. Điều cấm trong ảnh (không hình ảnh y tế, không ảnh trước sau, không biểu đồ bịa số liệu)

Mỗi brief ghi thêm: bám pain số mấy, ID nào.
```

**Kết quả mong đợi:** ví dụ brief cho bài 2 (bóc nhãn thành phần): chữ trên ảnh "Đọc được hết", bố cục danh sách 3 thành phần bên trái, ảnh chai bên phải, tông xanh nhạt.

**Nói với lớp:**

> Mục 5, điều cấm trong ảnh, là mục người ta hay bỏ. Ảnh trước và sau là chỗ ngành mỹ phẩm dính rắc rối nhiều nhất. Viết ra thành ràng buộc thì lần sau không ai trong team quên.

**Thao tác bước 2:** tạo visual. Có hai đường, chọn theo lớp.

*Đường A: Claude Artifacts, dùng khi cần chữ tiếng Việt sắc nét và bố cục chuẩn.*

```
Từ brief số 2, tạo một Artifact HTML kích thước 1080x1080, hiển thị đúng như brief.
Yêu cầu:
- Chữ tiếng Việt có dấu, dùng font hệ thống, cỡ chữ chính đủ lớn để đọc trên điện thoại
- Nền phẳng theo tông màu trong brief, không dùng ảnh từ internet
- Toàn bộ nằm gọn trong khung vuông, không tràn
Xuất ra để tôi xem trước, tôi sẽ chụp lại làm ảnh đăng.
```

*Đường B: công cụ ảnh AI, dùng khi cần ảnh sản phẩm hoặc nền có chất liệu.*

```
Từ brief số 1, viết cho tôi 1 prompt tạo ảnh bằng công cụ ảnh AI.
Yêu cầu prompt:
- Mô tả bối cảnh, ánh sáng, góc chụp, tông màu
- Không có chữ trong ảnh (chữ sẽ chèn sau để đảm bảo tiếng Việt đúng dấu)
- Không có mặt người cận cảnh vùng da bị tổn thương
Viết prompt bằng tiếng Anh, kèm bản dịch tiếng Việt để tôi kiểm.
```

**Nói với lớp:**

> Vì sao tách chữ ra khỏi ảnh AI: công cụ ảnh vẫn hay viết sai dấu tiếng Việt. Ảnh AI lo phần nền và chất liệu, chữ chèn sau bằng Canva hoặc Artifact. Đây là mẹo tiết kiệm rất nhiều lần làm lại.

Chiếu 3 visual đã ra. Nếu có visual xấu, giữ nguyên và nói:

> Cái này chưa đẹp. Nhưng nó đúng brief và đúng insight. Sửa đẹp mất 10 phút. Sửa một chiến dịch đi sai insight mất một tháng.

---

## Mốc 32 đến 35 phút · Chốt và giao việc

**Chiếu lại đường đi đầy đủ, một màn hình:**

```
30 mẩu nguyên văn
   ↓  gom nhóm chủ đề
7 pain, xếp theo tần suất, mỗi pain có ID
   ↓  bỏ pain vận hành
3 persona đặt tên theo nỗi lo
   ↓
5 content angle, mỗi angle truy ngược về ID
   ↓
5 bài social + 3 brief hình + 3 visual
```

**Ba câu chốt:**

1. "Mọi thứ ở đáy sơ đồ đều truy ngược lên đỉnh được. Truy không được thì là bịa."
2. "Ba chỗ agent nói chưa đủ dữ liệu chính là danh sách việc phải làm cho tháng sau."
3. "Bảng insight này còn sống tới buổi 3 và buổi 4. Buổi 3 dùng persona để cá nhân hóa email sale. Buổi 4 dùng cả bảng để dựng chiến dịch 14 ngày. Đừng để nó lạc trong cửa sổ chat. Lưu thành file `insight-khach-hang.md` ngay trong thư mục làm việc, cạnh `CLAUDE.md`."

**Câu nhắc lời hứa buổi 1, nói ngay trước khi giao việc:**

> Còn một việc nữa, và đây là việc tôi hứa với anh chị cuối buổi trước. Mở file `CLAUDE.md` ra. Mục 5 nỗi đau khách đang gắn nhãn `[SUY LUẬN]`, tức là buổi 1 chúng ta đoán. Cuối buổi hôm nay anh chị thay 5 dòng đoán đó bằng 5 nỗi đau vừa rút ra, có mã trích dẫn, có tần suất, và đổi nhãn thành `[DATA THẬT]`. Đó là bước 7 trong workbook, làm ở 20 phút cuối buổi. Lúc đó anh chị sẽ thấy tận mắt mình đoán trúng mấy dòng và trật mấy dòng.

**Giao việc cho 65 phút tiếp theo:**

> Mở workbook, làm đúng 6 bước, rồi bước 7 để dành cho 20 phút cuối. Ai có data của công ty thì dùng data của mình. Ai đã đăng ký tikhub thì làm bước 0 lấy bình luận thật của kênh mình hoặc của đối thủ. Ai chưa có gì thì dùng bộ Thảo An, làm ra sản phẩm y hệt. Bàn nào ra bảng insight mà cột trích dẫn còn trống thì gọi tôi ngay, đừng đi tiếp bước sau.
