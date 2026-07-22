# Buổi 2 · Customer Insight Agent

**Phụ đề:** Biến dữ liệu khách hàng thành insight và nội dung.

Buổi này dạy một việc rất cụ thể: đọc bình luận, review, tin nhắn khách để thấy điều họ thật sự quan tâm, rồi biến thành góc nội dung bám nỗi đau thật. Mọi insight phải trích được nguyên văn khách nói. Không trích được thì gắn `[SUY LUẬN]`.

---

## Mục tiêu buổi

- Học viên phân biệt được **dữ liệu thô** với **insight**, và biết insight nào dùng được để viết nội dung.
- Học viên xây xong **Customer Insight Agent** thành một skill trong thư mục làm việc của mình, agent này gom review và tin nhắn, phân nhóm chủ đề, rút pain kèm trích dẫn ID, dựng persona, xếp hạng pain theo tần suất.
- Học viên chuyển được insight thành **5 content angle** rồi ra **5 bài social**, **3 brief hình ảnh** và **3 visual** đăng được.
- Học viên thay được 5 nỗi đau `[SUY LUẬN]` trong `CLAUDE.md` của buổi 1 bằng 5 nỗi đau có trích dẫn thật.
- Học viên nhận ra ngay khi agent bịa: bịa trích dẫn, bịa tần suất, bịa persona.

---

## Đầu vào từ buổi 1

Học viên mở lại **thư mục làm việc** đã tạo buổi 1 (tên mẫu `thao-an-marketing`), mở bằng Claude Desktop, tab **Code**. Trong thư mục đó đã có sẵn:

- `san-pham-thao-an.md`: hồ sơ sản phẩm, giá, thành phần, danh sách điều không được nói
- `CLAUDE.md`: câu định vị, 3 thông điệp bán hàng, 5 nỗi đau khách (đang gắn nhãn `[SUY LUẬN]`), giọng văn, danh sách từ cấm
- `.claude/skills/viet-bai-ban-hang/SKILL.md`: skill viết bài bán hàng đã chạy được

Buổi 2 không tạo thư mục mới. Ta thêm một skill nữa vào chính thư mục đó, tên `customer-insight`. Claude tự đọc `CLAUDE.md` mỗi phiên, nên agent mới đọc được cả hồ sơ sản phẩm lẫn dữ liệu khách mà không phải dán lại gì.

**Lời hứa cuối buổi 1 phải trả trong buổi này.** Mục "5 nỗi đau khách" trong `CLAUDE.md` đang gắn nhãn `[SUY LUẬN]`, tức là buổi 1 mới chỉ đoán. Cuối buổi 2 học viên mở lại chính file đó, thay 5 dòng đoán bằng 5 nỗi đau rút từ data, đổi nhãn thành `[DATA THẬT]` kèm mã trích dẫn. Nói điều này ngay đầu buổi để lớp biết đích đến.

Ai vắng buổi 1 hoặc chưa có thư mục làm việc: tạo một thư mục mới trên màn hình nền, chép `demo/thao-an/san-pham-thao-an.md` vào, rồi nhờ Claude viết nhanh `CLAUDE.md` theo mẫu buổi 1. Mất 5 phút.

---

## Học viên cần chuẩn bị gì

**Bắt buộc mang tới lớp: dữ liệu khách hàng nguyên văn, tối thiểu 20 mẩu, tốt nhất 30 đến 60 mẩu.**

Một "mẩu" là một review, một câu hỏi inbox, hoặc một bình luận. Không cần dài. Câu "Có cồn không shop?" cũng là một mẩu, và là mẩu quý.

### Bắt buộc làm ở nhà trước buổi: đăng ký tài khoản tikhub

tikhub là dịch vụ cho Claude đọc dữ liệu công khai trên TikTok, Instagram, YouTube và một số nền tảng khác. Buổi này dùng nó để lấy bình luận thật dưới video, thay vì chỉ chép tay từ inbox. Ba điều nói thẳng với lớp trong email gửi trước buổi:

- **Mỗi lượt gọi đều tính tiền.** Phản hồi của dịch vụ ghi nguyên văn: "This request will incur a charge".
- **Mỗi học viên tự đăng ký tài khoản riêng và tự trả phí.** Lớp không cấp tài khoản dùng chung. Đăng ký và nạp phí phải xong trước buổi. Trong buổi không có thời gian ngồi đăng ký.
- **Không có tài khoản vẫn học được và vẫn nộp đủ sản phẩm.** Dùng file `demo/thao-an/review-va-tin-nhan-khach.md` là chạy trọn buổi.

*Lưu ý cho giảng viên: giao diện đăng ký và tên gói có thể đổi. Trước buổi phải tự chạy thử một lượt gọi trên máy mình, xem còn đúng đường bấm không.*

### Lấy data ở đâu

| Nguồn | Cách xuất |
|---|---|
| Review Shopee | Kênh Người Bán > Đánh giá > copy từng đánh giá vào Google Sheet. Nhớ lấy cả số sao và tên sản phẩm. |
| Review Lazada / TikTok Shop | Tương tự, vào mục đánh giá của gian hàng. |
| Inbox Facebook | Meta Business Suite > Hộp thư. Mở từng hội thoại, chỉ copy **câu khách hỏi**, bỏ phần shop trả lời. |
| Bình luận bài viết | Mở bài viết trên Page, copy bình luận có nội dung, bỏ các bình luận chỉ tag bạn bè. |
| Zalo OA, WhatsApp | Copy tay câu hỏi khách. |
| CRM hoặc Google Sheet có sẵn | Xuất CSV, giữ đúng cột nội dung. |
| Bình luận công khai dưới video TikTok | Nối tikhub, nhờ Claude gọi `tiktok_app_v3_fetch_video_comments`, lưu ngay kết quả thành file trong thư mục làm việc. Tốn phí mỗi lượt gọi. |
| Bình luận công khai dưới bài Instagram | Nối tikhub, nhờ Claude gọi `instagram_v3_get_post_comments`. Cũng tốn phí mỗi lượt gọi. |
| Không kịp gom | Chụp màn hình rồi cho Claude đọc ảnh cũng được, nhưng phải kiểm lại chữ trước khi dùng. |

### Ba việc phải làm trước khi đưa cho agent

1. **Xóa thông tin cá nhân.** Bỏ tên thật, số điện thoại, địa chỉ, ảnh đại diện. Giữ nguyên văn câu nói. Data lấy từ tikhub cũng vậy: chỉ giữ câu người ta viết công khai, bỏ tên tài khoản và đường dẫn trang cá nhân. Ta đọc điều khách nói, không dựng danh sách người.
2. **Đánh ID.** Review đánh R01, R02... Tin nhắn đánh M01, M02... Bình luận đánh C01, C02... Không có ID thì agent không trích dẫn được, cả buổi học sập.
3. **Giữ nguyên văn, kể cả sai chính tả.** "mụn ẩn" khách viết "mụn ẩnn" thì để nguyên. Sửa chữ là sửa bằng chứng.

Ai chưa có data thật: dùng nguyên bộ `demo/thao-an/review-va-tin-nhan-khach.md` (15 review + 15 tin nhắn, đã đánh ID sẵn). Vẫn làm ra đủ sản phẩm.

---

## Timeline 2,5 giờ

| Khối | Thời lượng | Giảng viên làm gì |
|---|---|---|
| 1. Framework | 20 phút | Giảng 4 ý: dữ liệu thô khác insight ở đâu (2 phút cuối ý này nói về nguồn data thật và tikhub); vì sao xếp hạng theo tần suất; vì sao mỗi insight phải có trích dẫn; content angle khác thông điệp thế nào. Chiếu bảng insight mẫu Thảo An ở cuối để lớp thấy đích đến. |
| 2. Demo trên Thảo An, **kiểu làm theo** | 35 phút | Chạy đúng `../so-tay-giang-vien/buoi-02-customer-insight-agent.md`, nhưng học viên gõ cùng lúc chứ không ngồi xem. Trong 35 phút: **25 phút học viên tay trên bàn phím, 10 phút giảng viên nói và chỉ chỗ.** Xem mục "Khối 2 chạy kiểu làm theo" ngay bên dưới bảng này. |
| 3. Học viên làm sản phẩm, chặng 1 | 30 phút | Học viên mở `../workbook/buoi-02-customer-insight-agent.md`. Chặng này làm: chuẩn bị data (8 phút), bước 1 nạp agent và bắt nó đếm (7 phút), bước 2 ra bảng insight (15 phút). Giảng viên đi vòng lớp. Ưu tiên bàn nào bảng insight chưa có cột trích dẫn, đó là bàn đang đi sai. **Hết 30 phút gọi cả lớp dừng, hỏi ai đã có bảng insight, ai chưa xong thì kéo về bộ Thảo An ngay**, rồi cho nghỉ. |
| **Giải lao** | **10 phút** | Nghỉ. Bắt buộc, không được gộp vào khối khác. Lớp online live không ngồi liền 150 phút. Giảng viên dùng 10 phút này gỡ cho máy nào chưa ra bảng insight, để họ vào chặng 2 không bị hụt. |
| 3. Học viên làm sản phẩm, chặng 2 | 25 phút | Làm tiếp workbook: bước 3 dựng persona (6 phút), bước 4 năm content angle (8 phút), bước 5 năm bài social (7 phút), bước 6 ba brief hình ảnh và ba visual (4 phút). Bước 7 để dành cho khối 5. |
| 4. Review nhanh | 10 phút | Gọi 3 học viên, mỗi người 2 phút. Xem tiêu chí review bên dưới. |
| 5. Hoàn thiện và nộp | 20 phút | Học viên sửa theo góp ý, làm **bước 7 của workbook**: lưu bảng insight thành file `insight-khach-hang.md` và cập nhật mục 5 nỗi đau trong `CLAUDE.md`. Rồi đóng gói nộp. Giảng viên chốt buổi bằng 1 câu: insight buổi này là nguyên liệu buổi 3 (cá nhân hóa email sale) và buổi 4 (chiến dịch 14 ngày). |

**Cộng lại để tự kiểm:** 20 + 35 + 30 + 10 + 25 + 10 + 20 = **150 phút**, khớp thời lượng khai báo.

**Tay học viên đặt trên bàn phím:** demo làm theo 25 + chặng 1 là 30 + chặng 2 là 25 + hoàn thiện 20 = 100 phút trên 140 phút học thật, tức 71,4 phần trăm. Con số này chỉ đúng khi khối 2 chạy đúng kiểu làm theo.

> **Lưu ý cho giảng viên:** file workbook đang ghi tổng thời lượng từng bước cộng lại là 65 phút, tính theo nhịp cũ chưa có giải lao. Nhịp mới cho khối làm sản phẩm 55 phút gõ, chia hai chặng như bảng trên. Bám bảng trên, đừng bám con số trong ngoặc của workbook.

---

## Khối 2 chạy kiểu làm theo, không phải ngồi xem

**Đây là điều kiện để buổi này đạt ngưỡng thực hành.** Nếu giảng viên bấm nhanh cho kịp giờ và học viên chỉ ngồi nhìn, 25 phút chuyển ngược sang cột lý thuyết và buổi tụt xuống dưới ngưỡng bắt buộc.

**Câu dặn đọc lên trước khi gõ chữ đầu tiên của khối 2:**

> "Anh chị mở máy ra, mở đúng thư mục làm việc của buổi 1, đặt tay lên bàn phím. Ba mươi lăm phút tới không phải là tôi biểu diễn cho anh chị xem. Tôi gõ gì thì anh chị gõ y hệt trên máy mình. Tôi đi chậm hơn bình thường, và cứ sau mỗi prompt lớn tôi sẽ dừng lại hỏi ai chưa ra kết quả. Anh chị giơ tay ngay lúc đó, đừng ngại, vì tôi chạy tiếp là anh chị mất luôn khúc sau."

**Học viên gõ gì song song, ghi rõ theo từng mốc của sổ tay giảng viên:**

| Mốc trong sổ tay | Giảng viên làm | Học viên gõ cùng lúc trên máy mình |
|---|---|---|
| 0 tới 5 phút | Gọi tikhub lấy bình luận thật, lưu thành `binh-luan-tiktok-goc.md` | Ai đã có tài khoản tikhub thì gọi trên kênh của mình hoặc của đối thủ. Ai chưa có thì mở sẵn `review-va-tin-nhan-khach.md` trong thư mục của mình và đánh ID |
| 5 tới 8 phút | Nạp agent, dán prompt mở màn bắt agent đếm | Dán đúng prompt đó, đối chiếu máy mình có ra 30 mẩu không |
| 8 tới 15 phút | Dán prompt chính ra bảng insight, rồi Ctrl+F kiểm trích dẫn | Dán prompt chính, ra bảng insight của chính mình, rồi tự Ctrl+F kiểm một trích dẫn trên máy mình |
| 15 tới 19 phút | Hỏi ba câu data không trả lời được | Dán đúng ba câu đó, xem máy mình có nói "chưa đủ dữ liệu" không |
| 19 tới 22 phút | Dựng persona | Dựng persona trên bảng insight của mình |
| 22 tới 28 phút | Ra angle rồi ra bài social | Ra angle và bài social trên máy mình |
| 28 tới 32 phút | Brief hình ảnh và visual | Gõ theo, ra 1 brief là đủ ở khối này, ba brief để dành cho khối 3 |
| 32 tới 35 phút | Chốt sơ đồ, giao việc | Không gõ. Đây là phần thuộc 10 phút giảng viên nói |

**Bốn điểm dừng bắt buộc, đọc đúng câu này:**

1. **Sau prompt bắt agent đếm (mốc 8 phút):** "Ai chưa ra kết quả thì giơ tay." Chờ tới khi tối thiểu hai phần ba lớp giơ tay báo đã ra. Máy nào chưa ra thì kiểm ngay: file data đã nằm trong thư mục làm việc chưa.
2. **Sau prompt chính ra bảng insight (mốc 15 phút):** "Ai chưa ra bảng thì giơ tay." Đây là điểm dừng dài nhất, chờ được thì chờ tới 90 giây. Bảng insight là xương sống cả buổi, ai hụt ở đây là hụt tới cuối.
3. **Sau ba câu bắt lỗi (mốc 19 phút):** "Máy anh chị nó nói chưa đủ dữ liệu mấy trên ba câu?" Đếm bằng giơ tay. Máy nào ra khác thì chiếu lên cho cả lớp xem, đó là tình huống dạy được.
4. **Sau khi ra 5 angle (mốc 28 phút):** "Ai đã có đủ 5 angle trên máy mình thì giơ tay." Chưa đủ thì cho dùng tạm 3 angle, làm nốt ở khối 3.

**Quy tắc cứng:** thà chạy chậm mà cả lớp gõ, còn hơn chạy đúng giờ mà nửa lớp ngồi xem. Nếu tới mốc 28 phút mà mới chạy được nửa kịch bản, bỏ phần visual của mốc 28 tới 32, chuyển thẳng sang phần chốt. Đừng bù giờ bằng cách bấm nhanh hơn.

---

## Nội dung 20 phút framework

### Ý 1 · Dữ liệu thô khác insight ở chỗ nào (7 phút)

Mở đầu bằng câu hỏi cho lớp: "Câu này là dữ liệu hay insight? Khách nói: Da mình nhạy cảm lắm, dùng cái này không bị rát gì hết."

Đó là **dữ liệu thô**. Một người, một câu, một lần.

Nó thành **insight** khi đủ ba thứ:

1. **Lặp lại.** Không phải một người nói mà nhiều người nói, ở nhiều chỗ khác nhau.
2. **Có lý do đằng sau.** Vì sao họ nói vậy. Ở đây: họ từng bị kích ứng nên sợ, chứ không phải họ thích cảm giác mát.
3. **Đổi được hành vi bán hàng.** Biết rồi thì viết khác đi, bán khác đi.

Công thức viết một insight cho gọn:

```
[Nhóm khách nào] + [lo hoặc muốn điều gì] + [vì sao] + [bằng chứng ID] + [tần suất trên tổng]
```

Ví dụ thật từ data Thảo An:

> Nhóm khách da nhạy cảm sợ sản phẩm mới làm rát và nổi mẩn, vì họ đã từng bị với sản phẩm khác. Bằng chứng: R01, R11, M01, M02, M06, M10. Tần suất: 9 trên 30 mẩu nhắc trực tiếp nỗi lo an toàn.

So sánh với câu thường thấy trong các báo cáo: "Khách hàng quan tâm đến chất lượng sản phẩm." Câu này đúng, nhưng vô dụng. Nó đúng với mọi ngành, mọi thương hiệu, mọi thời điểm. Insight tốt phải sai được. Nếu một câu không thể sai thì nó không phải insight.

**Chốt ý:** dữ liệu thô là khách nói gì; insight là vì sao họ nói vậy và ta phải làm gì.

#### Dữ liệu thật lấy ở đâu (2 phút cuối của ý 1, không cộng thêm giờ)

Hai đường vào, nói cả hai:

**Đường 1, chép tay.** Review sàn, inbox Facebook, bình luận bài viết. Chậm, nhưng ai cũng làm được và không tốn phí.

**Đường 2, để Claude tự lấy.** Nối tikhub, rồi nhờ Claude gọi công cụ `tiktok_app_v3_fetch_video_comments` để lấy nguyên bình luận dưới một video TikTok. Một lượt gọi ra vài chục mẩu trong mười giây. Bài Instagram thì dùng `instagram_v3_get_post_comments`.

Ba điều phải nói với lớp, đừng bỏ điều nào:

1. **Mỗi lượt gọi tính tiền.** Nghĩ kỹ rồi hãy gọi. Gọi một lần xong thì lưu ngay kết quả thành file trong thư mục làm việc. Lần sau đọc file đó, đừng gọi lại.
2. **Data thật rồi vẫn phải đánh ID và vẫn phải trích dẫn được.** Bình luận lấy về từ TikTok cũng chỉ là mấy chục dòng chữ. Agent vẫn bịa được trên chữ thật, nếu ta không ép nó chỉ ra dòng nào.
3. **Chỉ lấy nội dung công khai.** Câu người ta viết công khai thì lấy được. Gom tên tài khoản, ảnh đại diện, đường dẫn trang cá nhân của người bình luận thành một danh sách thì không. Đó là dựng danh sách cá nhân, không phải đọc khách hàng.

### Ý 2 · Vì sao xếp hạng theo tần suất chứ không theo cảm giác (5 phút)

Ai làm marketing lâu cũng có "linh cảm" về khách. Linh cảm thường sai theo một kiểu rất cụ thể: ta nhớ mẩu gây cảm xúc mạnh nhất, không nhớ mẩu lặp nhiều nhất.

Một review 1 sao chửi rát mặt sẽ ám cả tuần. Trong khi 9 câu hỏi "có cồn không shop" rải rác cả tháng thì không ai nhớ. Nhưng 9 câu kia mới là thứ đang chặn đơn hàng.

Quy tắc: **xếp hạng pain theo số mẩu nhắc tới, ghi dạng x trên tổng.** Không ghi "đa số khách", "rất nhiều khách", "phần lớn". Ba chữ đó là chỗ agent và người đều hay bịa.

Ghi "9 trên 30" thì kiểm được. Ghi "đa số khách" thì không kiểm được, và thường là 3 trên 30.

Lưu ý nghề: tần suất trong data chỉ phản ánh **người đã nói**. Người bỏ đi im lặng không nằm trong đó. Nên tần suất dùng để xếp thứ tự ưu tiên, không dùng để suy ra thị phần.

### Ý 3 · Vì sao mỗi insight phải có trích dẫn (5 phút)

Đây là phần quan trọng nhất buổi.

Mô hình ngôn ngữ rất giỏi viết câu nghe đúng. Nó cũng rất giỏi viết câu nghe đúng mà không có thật. Hai loại này nhìn giống nhau khi đọc lướt.

Cách duy nhất tách được: **ép agent chỉ ra mẩu nào.**

Khi agent phải ghi "R01, M02" bên cạnh mỗi insight, ba việc xảy ra:
- Insight bịa lộ ra ngay, vì không có ID nào để gắn.
- Bạn Ctrl+F kiểm được trong 5 giây.
- Sếp hoặc khách hàng hỏi "dựa vào đâu" thì có câu trả lời.

Nhắc lại **ba nguyên tắc chống bịa** áp cho mọi agent trong khóa:

1. **Chỉ dùng dữ liệu người dùng cấp.** Không tự chế số liệu, thành phần, công dụng, giá, tên khách.
2. **Gắn nhãn nguồn.** `[DATA THẬT]` khi trích được, `[SUY LUẬN]` khi tự suy ra. Thiếu thì ghi thẳng "chưa đủ dữ liệu".
3. **Người duyệt cuối.** Mọi thứ gửi khách đều là nháp. Agent không tự bấm gửi.

Điểm cần nói rõ với lớp: `[SUY LUẬN]` không xấu. Suy luận là việc có ích. Cái xấu là suy luận đội lốt dữ liệu.

### Ý 4 · Content angle là gì, khác thông điệp ra sao (3 phút)

**Thông điệp** là điều thương hiệu muốn nói. Thảo An: "Da khỏe từ thảo mộc Việt". Một thương hiệu có một hoặc hai thông điệp, giữ nguyên cả năm.

**Content angle** là góc vào để khách chịu đọc. Nó bắt đầu từ nỗi lo của khách, không từ ưu điểm của sản phẩm. Một thông điệp đẻ ra được mười angle.

Đặt cạnh nhau cho dễ thấy:

| Thông điệp | Content angle |
|---|---|
| Da khỏe từ thảo mộc Việt | "Từng đổi serum rồi nổi mẩn? Đọc cái này trước khi đổi lần nữa" |
| Không cồn, đã test da liễu | "Bóc nhãn thành phần: đọc từng dòng, cái nào là gì" |
| Hỗ trợ giảm thâm sau mụn | "1 tuần chưa thấy gì có phải là hỏng không" |

Nhận ra angle yếu bằng một phép thử: **đọc angle lên, nếu thay tên thương hiệu bằng đối thủ mà vẫn dùng được thì angle đó chưa bám data.** "Chất lượng tốt, giá hợp lý" dùng được cho mọi shop, nên nó không phải angle.

Angle mạnh luôn truy ngược được về một insight, insight đó truy ngược được về một ID. Trong workbook có cột bắt học viên ghi rõ đường truy ngược này.

---

## Bảng insight mẫu Thảo An (giảng viên có sẵn đáp án)

Chiếu bảng này cuối phần framework, hoặc giữ để đối chiếu khi demo. Đây là kết quả rút từ 30 mẩu trong `review-va-tin-nhan-khach.md`.

| # | Pain | Tần suất | Trích dẫn ID | Nhãn |
|---|---|---|---|---|
| 1 | Sợ sản phẩm mới gây rát, nổi mẩn, dị ứng; muốn bằng chứng an toàn trước khi thử | 9/30 | R01, R02, R04, R11, M01, M02, M04, M06, M10 | [DATA THẬT] |
| 2 | Băn khoăn giá và dung tích, sợ mua hớ, muốn size nhỏ dùng thử | 5/30 | R03, R13, M07, M08, M14 | [DATA THẬT] |
| 3 | Kết cấu và cảm giác dùng chưa vừa ý, kem đặc khó thấm, mặt nạ gây khô căng | 5/30 | R06, R07, R08, R10, M13 | [DATA THẬT] |
| 4 | Cần bằng chứng để tin: giấy test da liễu, hàng chuẩn, xem hàng rồi mới trả | 5/30 | R04, R14, M04, M09, M14 | [DATA THẬT] |
| 5 | Sốt ruột vì chưa thấy kết quả, không biết bao lâu và dùng tới khi nào | 4/30 | R02, R05, M05, M15 | [DATA THẬT] |
| 6 | Không biết tình trạng da của mình thì chọn SKU nào | 3/30 | M03, M12, R12 | [DATA THẬT] |
| 7 | Vướng ở khâu mua: giao chậm, chọn kênh nào, muốn COD | 3/30 | R15, M09, M11 | [DATA THẬT] |

Ba nhận xét đáng nói khi chiếu bảng này:

1. **Pain số 1 gấp đôi mọi pain khác.** Nỗi lo an toàn là thứ chặn đơn nhiều nhất, nhưng nó gần như không nằm ở phần review chê. Bộ này không có review nào dưới 2 sao, và 5 trong 9 mẩu của pain số 1 là tin nhắn hỏi trước khi mua (M01, M02, M04, M06, M10). Ai chỉ đọc review sẽ bỏ lỡ hơn nửa pain lớn nhất.
2. **Cả 4 review 4 sao đều kèm một câu chê cụ thể** (R03 giá và dung tích, R07 kem đặc, R10 khô căng, R15 giao chậm). Review 4 sao là mỏ vàng, khách hài lòng nên nói thật, không giận nên nói rõ.
3. **Pain số 3 chỉ nằm ở kem nghệ và mặt nạ** (R07, R08 là kem; R10 là mặt nạ). Serum rau má không có mẩu nào chê kết cấu. Đây là insight cấp SKU, không phải cấp thương hiệu, và nó đổi cách viết bài cho từng dòng sản phẩm.

**Pain số 7 là pain vận hành, không phải pain nội dung.** Giao chậm thì không viết bài, mà chuyển cho bộ phận vận hành. Nhắc lớp phân tách chỗ này, nhiều người viết bài xin lỗi về giao hàng rồi tự làm yếu thương hiệu.

**Chỗ agent phải trả lời "chưa đủ dữ liệu":** khách chủ yếu ở tỉnh thành nào, tỷ lệ mua lần đầu so với mua lại, lý do khách nhắn rồi không mua. File data ghi rõ ba chỗ này còn thiếu.

---

## Điểm học viên hay vấp và cách xử lý

**1. Data quá ít, dưới 15 mẩu.**
Dấu hiệu: bảng insight chỉ ra được 2 đến 3 dòng, tần suất toàn 1/12.
Xử lý: gộp thêm nguồn (bình luận bài viết, tin nhắn cũ, review sàn khác). Vẫn thiếu thì cho học viên chạy song song: dùng bộ Thảo An để học kỹ thuật, đồng thời ghi lại cách gom data về công ty làm tiếp. Đừng để học viên ngồi không.

**2. Data toàn khen, không có chê.**
Rất hay gặp ở shop mới hoặc shop có lọc review.
Xử lý: nói với lớp rằng **câu hỏi trước mua chính là pain**. Người hỏi "có cồn không" đang lo dị ứng. Người hỏi "bao lâu thấy hiệu quả" đang sợ mất tiền vô ích. Chuyển toàn bộ trọng tâm sang tin nhắn và bình luận. Thêm nữa: đọc review 4 sao thay vì 5 sao, chỗ chê nằm ở đó.

**3. Agent phóng đại tần suất.**
Dấu hiệu: agent viết "đa số khách lo về kích ứng", "rất nhiều khách phàn nàn giá".
Xử lý: bắt agent ghi dạng x/tổng và liệt kê đủ ID. Rồi tự đếm tay một dòng bất kỳ. Prompt sửa nhanh:
```
Bỏ mọi từ định lượng mơ hồ: đa số, rất nhiều, phần lớn, hầu hết.
Mỗi pain ghi đúng dạng "x/30" và liệt kê đủ ID đã đếm.
Nếu số ID liệt kê không khớp với x thì sửa lại x, không sửa danh sách ID.
```

**4. Agent bịa trích dẫn hoặc ghép chữ.**
Dấu hiệu tinh vi hơn: ID có thật, nhưng câu trích bị agent viết mượt lại cho hay.
Xử lý: dạy lớp thao tác kiểm 5 giây. Copy đoạn agent trích, Ctrl+F trong file gốc. Không khớp 100% ký tự là hỏng. Nhắc: agent làm mượt câu chê của khách là đang làm hỏng bằng chứng.

**5. Nhầm pain vận hành với pain nội dung.**
Dấu hiệu: trong 5 content angle có một angle về giao hàng nhanh.
Xử lý: chia bảng insight làm hai nhóm ngay từ đầu. Nhóm ra nội dung, nhóm chuyển vận hành. Chỉ nhóm đầu đi tiếp sang bước angle.

**6. Năm angle thật ra là một angle viết năm kiểu.**
Dấu hiệu: cả 5 angle đều xoay quanh "lành tính, an toàn".
Xử lý: ép mỗi angle map tới một pain **khác nhau** trong bảng. Pain số 1 mạnh nhất thì cho phép 2 angle, còn lại mỗi pain một angle.

**7. Bài social vi phạm danh sách điều không được nói.**
Dấu hiệu: xuất hiện "trị mụn", "hết thâm sau 7 ngày", "đặc trị", so sánh đích danh thương hiệu khác.
Xử lý: nhắc hồ sơ sản phẩm và mục từ cấm trong `CLAUDE.md` của buổi 1 đã liệt kê rõ. Cho học viên chạy một lượt rà cuối:
```
Rà 5 bài trên, đối chiếu mục "Điều KHÔNG được nói" trong hồ sơ sản phẩm.
Liệt kê từng câu vi phạm kèm số bài, đề xuất câu thay thế.
Không tự sửa, chỉ liệt kê để tôi duyệt.
```

---

## Tiêu chí review 10 phút

Gọi 3 học viên, mỗi người 2 phút, 4 phút còn lại giảng viên chốt điểm chung cả lớp.

Với mỗi người, làm đúng ba thao tác này, không giảng lý thuyết:

1. **Chỉ vào một dòng insight bất kỳ, hỏi: mẩu nào?** Học viên phải mở được file data và chỉ ra đúng câu. Ấp úng là insight chưa chắc.
2. **Đọc to angle số 3, hỏi: angle này bám pain nào, tần suất bao nhiêu?** Trả lời được thì đường truy ngược thông.
3. **Đọc lướt một bài social, tìm từ cấm và tìm chỗ hứa kết quả.** Có thì sửa tại chỗ.

Ghi bảng ba lỗi phổ biến nhất vừa thấy để cả lớp sửa trong 20 phút cuối.

**Trong 20 phút cuối, giảng viên đi vòng và kiểm thêm đúng hai thứ của bước 7:**

- Mở `CLAUDE.md` của học viên, xem mục 5 nỗi đau đã đổi nhãn từ `[SUY LUẬN]` sang `[DATA THẬT]` chưa, và mỗi dòng có mã trích dẫn kèm tần suất chưa. Còn dòng nào không gắn được ID thì giữ nguyên nhãn `[SUY LUẬN]`, đừng cho đổi bừa.
- Xem trong thư mục làm việc đã có file `insight-khach-hang.md` chưa. Bảng insight còn nằm trong cửa sổ chat là chưa tính hoàn thành.

---

## Sản phẩm nộp

Học viên nộp chính thư mục làm việc của mình, trong đó có đúng 6 phần:

1. **1 Customer Insight Agent** đóng thành file skill `.claude/skills/customer-insight/SKILL.md`, đã chỉnh cho ngành của mình, có frontmatter `name` và `description`
2. **Bảng insight** lưu thành file `insight-khach-hang.md` trong thư mục làm việc, tối thiểu 5 dòng, có đủ cột pain / tần suất / trích dẫn ID / persona
3. **5 content angle** rút từ data thật, mỗi angle ghi rõ bám pain nào
4. **5 bài social** viết theo phần giọng văn và từ cấm trong `CLAUDE.md` của buổi 1
5. **3 brief hình ảnh** và **3 visual** đăng được
6. **`CLAUDE.md` đã cập nhật:** mục 5 nỗi đau khách không còn nhãn `[SUY LUẬN]`, mỗi nỗi đau kèm mã trích dẫn và tần suất

### Chấm đạt / chưa đạt

| | Đạt | Chưa đạt |
|---|---|---|
| Bảng insight | Từ 5 dòng trở lên, mỗi dòng có tối thiểu 2 ID, tần suất ghi dạng x/tổng | Dưới 5 dòng, hoặc có dòng không ID, hoặc tần suất ghi bằng chữ "đa số" |
| Chống bịa | Có ít nhất 1 chỗ agent ghi "chưa đủ dữ liệu"; phần suy ra có nhãn `[SUY LUẬN]` | Bảng điền kín, không chỗ nào thiếu, không nhãn nào. Đây là dấu hiệu agent đang bịa |
| Kiểm chứng | Giảng viên bốc 2 trích dẫn ngẫu nhiên, cả 2 khớp nguyên văn file gốc | Có 1 trích dẫn không khớp |
| Content angle | 5 angle, map tới ít nhất 4 pain khác nhau, không angle nào thay được tên thương hiệu | Angle chung chung, hoặc 5 angle cùng một pain |
| Bài social | 5 bài, đúng brand voice, không từ cấm, không hứa mốc thời gian | Có từ cấm, hoặc bài không nhận ra được là của thương hiệu nào |
| Hình ảnh | 3 brief đủ 5 mục và 3 visual mở xem được | Chỉ có brief, chưa có visual |
| `CLAUDE.md` cập nhật | Mục 5 nỗi đau đã đổi sang `[DATA THẬT]`, mỗi dòng có mã trích dẫn và tần suất dạng x/tổng | Vẫn nguyên 5 nỗi đau `[SUY LUẬN]` của buổi 1, hoặc đã đổi nhãn nhưng không có mã trích dẫn |

Đạt tối thiểu 6 trên 7 dòng thì tính là hoàn thành buổi 2. Riêng dòng `CLAUDE.md` cập nhật là bắt buộc, thiếu dòng này thì chưa xong buổi.

---

## Nối sang buổi sau

Nói câu này trước khi kết thúc, để học viên giữ file cẩn thận:

- **Buổi 3 (Sales Agent):** persona và bảng pain của hôm nay là thứ dùng để cá nhân hóa email sale. Email viết cho "người từng bị kích ứng" khác hẳn email viết cho "người đang so giá".
- **Buổi 4 (Content Engine):** bảng insight và 5 angle là nguyên liệu dựng chiến dịch 14 ngày. Không có bảng này thì buổi 4 phải bịa lịch nội dung.

Yêu cầu học viên lưu bảng insight thành file `insight-khach-hang.md` ngay trong thư mục làm việc, cạnh `CLAUDE.md`. Để rời trong cửa sổ chat là buổi sau mất. File nằm trong thư mục thì buổi sau mở tab Code lên là Claude đọc được ngay.
