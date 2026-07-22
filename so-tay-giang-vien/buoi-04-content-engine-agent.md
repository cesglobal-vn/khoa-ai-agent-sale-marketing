# Buổi 4 · Kịch bản demo 35 phút

> Demo chạy trên case Thảo An. Giảng viên gõ trực tiếp trước lớp, không dán kết quả soạn sẵn. Học viên phải thấy agent trả lời sai ở đâu và sửa thế nào.
>
> **Học viên gõ theo cùng lúc trên máy mình, không ngồi xem.** Bảng phân công học viên gõ gì ở từng mốc, cùng bốn điểm dừng chờ cả lớp, nằm ở mục "Khối 2 chạy kiểu làm theo" trong [../giao-an/buoi-04-content-engine-agent.md](../giao-an/buoi-04-content-engine-agent.md). Đọc mục đó trước khi vào lớp.
>
> Chuẩn bị trước: mở **thư mục làm việc** của buổi 1 bằng tab **Code** của Claude Desktop. Trong thư mục phải có sẵn `CLAUDE.md`, hai file `san-pham-thao-an.md` và `review-va-tin-nhan-khach.md` chép từ `demo/thao-an/`, và skill `viet-bai-ban-hang` ở `.claude/skills/viet-bai-ban-hang/SKILL.md`. Giao diện app có thể đổi theo phiên bản, giảng viên mở thử một lượt trước buổi.

| Mốc | Nội dung | Phút |
|---|---|---|
| A | Mở màn, tạo file skill Content Engine | 3 |
| B | Tra xu hướng bằng tikhub, rồi từ 1 insight ra campaign brief | 6 |
| C | Lịch 14 ngày, bảng thật | 7 |
| D | Hai bài social khác định dạng, cắt một bài xuống 280 ký tự | 7 |
| E | Bẫy vi phạm và khai báo ràng buộc | 6 |
| F | Kịch bản video và brief hình ảnh | 6 |

---

## A · 00:00 đến 03:00 · Mở màn và tạo file skill

**Thao tác:** Mở thư mục làm việc bằng tab **Code**. Gõ nguyên câu này cho Claude tạo file skill:

```
Tạo file .claude/skills/content-engine/SKILL.md trong thư mục làm việc này,
tạo luôn thư mục cha nếu chưa có. Nội dung như sau: [dán khối trong ../demo/buoi-04/skill-content-engine.md]
```

Claude xin phép ghi file thì bấm **Yes**. Mở file ra chiếu lên màn hình, chỉ cho lớp thấy hai chỗ: dòng `description` ở frontmatter trên cùng (đây là thứ Claude đọc để quyết định có gọi skill hay không), và khối ràng buộc nằm ngay **đầu** phần nội dung, không phải cuối.

Xong thì mở phiên mới và gõ đúng một câu tự nhiên, **không** nhắc tên skill:

```
Dựng cho tôi chiến dịch nội dung 14 ngày cho serum rau má B5.
```

**Nói với lớp:**

> "Hôm nay không ai gõ tay 30 mẩu nội dung. Chúng ta dựng một cái máy. Nhưng trước khi máy chạy, phải lắp phanh. Nhìn khối ràng buộc này: nó nằm trên cùng, trước cả phần mô tả nhiệm vụ. Lý do đơn giản, thứ đặt cuối file hay bị agent lướt qua khi output dài. Và để ý: mình không dán prompt vào đâu cả. Mình để nó thành một file trong thư mục, Claude tự tìm tới khi mình nói đúng việc."

**Kết quả mong đợi:** Claude báo đang dùng skill `content-engine`, rồi trả lời ngắn gọn kiểu "Đã sẵn sàng. Cần bạn cấp: insight xương sống, persona, danh sách kênh, mục tiêu bán hàng, danh sách từ cấm." Nếu nó không gọi skill thì lỗi ở dòng `description`, sửa cho giống câu người dùng thật sự gõ. Nếu nó tự nhảy vào viết bài ngay thì nội dung skill sai, sửa lại phần "Quy trình làm việc".

---

## B · 03:00 đến 09:00 · Tra xu hướng rồi ra campaign brief

Mốc này vẫn 6 phút: 2 phút tra xu hướng, 4 phút ra brief. Hai phút tra lấy từ phần bình luận cuối mốc, đừng để lấn sang mốc C.

**Thao tác bước 1, 2 phút:** Trước khi dựng chiến dịch, nhìn ra ngoài một lượt. Gọi MCP `tikhub`, đúng ba công cụ:

- `tiktok_app_v3_fetch_hashtag_detail` để xem một hashtag của ngành đang chạy thế nào.
- `tiktok_app_v3_fetch_hashtag_video_list` để lấy video đang lên theo hashtag đó.
- `tiktok_ads_search_ads` để tra thư viện quảng cáo đối thủ.

Nói to trước khi bấm gọi:

> "Mỗi lượt gọi này tính tiền vào tài khoản của người gọi. Dịch vụ nó trả về nguyên chữ 'This request will incur a charge'. Nên mình gọi một lần, rồi lưu ngay kết quả thành file. Lần sau đọc lại file, không gọi lại."

Gọi xong thì lưu ngay:

```
Lưu kết quả vừa lấy được thành file xu-huong-hashtag.md trong thư mục làm việc.
Ghi rõ ngày lấy, hashtag nào, và 5 góc nội dung đang bị lặp nhiều nhất.
Chỉ lấy nội dung công khai, không ghi lại tên hay thông tin cá nhân của ai.
```

Nói với lớp: mình tra để biết góc nào đã bão hòa mà **tránh**, không phải để bắt chước. Insight xương sống vẫn lấy từ dữ liệu khách của mình, không lấy từ bảng xu hướng.

**Ai không có tài khoản `tikhub` thì bỏ hẳn 2 phút này**, đi thẳng vào bước 2 với dữ liệu case Thảo An. Không mất hạng mục nộp nào.

**Thao tác bước 2, 4 phút:** Đưa một insight duy nhất, kèm bằng chứng trích dẫn. Nhấn mạnh với lớp: chỉ một, không phải năm.

**Prompt nguyên văn:**

```
Insight xương sống cho chiến dịch 14 ngày này:

"Khách sợ bị kích ứng khi đổi sang sản phẩm chăm da mới. Nỗi sợ này
mạnh hơn mong muốn cải thiện da, nên nó chặn ở bước quyết định mua,
không phải bước biết đến sản phẩm."

Bằng chứng [DATA THẬT]:
- R11: "Trước mình dùng loại khác bị nổi mẩn, đổi qua đây thì ổn. Sẽ mua lại."
- M01: "Da mình nhạy cảm lắm, dùng cái này có bị rát không shop?"
- M02: "Sản phẩm này có cồn không ạ? Mình dị ứng cồn."
- M06: "Đang dùng của hãng khác, đổi qua có sao không?"
- R04: "Đọc thành phần thấy toàn cái đọc được, không có chất gì lạ."

Bối cảnh:
- Persona chính: nữ 28-34, nhân viên văn phòng, da nhạy cảm dễ đỏ rát,
  từng bị kích ứng nên sợ thử đồ mới. Lướt Facebook buổi tối, hỏi kỹ
  qua inbox trước khi mua, thích chốt đơn trên Shopee.
- Kênh: Facebook (bài + ads + inbox) đầu phễu tới chốt; Shopee cuối phễu
  chốt đơn và chứng thực; Website nền tin cậy, gắn UTM để đo nguồn.
- Mục tiêu: 30 đơn trong 30 ngày, 100% đơn gắn được nguồn kênh.
  Chiến dịch 14 ngày này nằm ở tuần 2 và tuần 3, chỉ tiêu 15 đơn.

Viết campaign brief. Đúng 8 mục:
1. Tên chiến dịch
2. Insight xương sống (chép lại, không diễn giải thêm)
3. Khách mục tiêu, viết bằng lời khách nói
4. Ba thông điệp trụ cột, mỗi cái 1 câu
5. Năm lõi nội dung, mỗi lõi = 1 nỗi đau + 1 điểm mạnh sản phẩm
6. Vai trò từng kênh trong 14 ngày này
7. Chỉ số đo, tách rõ chỉ số đầu phễu và chỉ số đơn hàng
8. Điều tuyệt đối không nói

Mỗi dòng gắn nhãn [DATA THẬT] hoặc [SUY LUẬN]. Thiếu dữ liệu thì ghi
"chưa đủ dữ liệu", không tự điền.
```

**Kết quả mong đợi:** Brief 8 mục, khoảng một trang. Phần quan trọng nhất là mục 5, năm lõi nội dung. Agent thường ra đại loại:

- Lõi 1: Sợ thành phần lạ gây rát + không cồn, không hương liệu tổng hợp
- Lõi 2: Sợ đổi sản phẩm giữa chừng + đã test da liễu
- Lõi 3: Sợ bị hứa hão + không cam kết thời gian, nói thật về tốc độ
- Lõi 4: Không biết chọn SKU nào cho da mình + 3 SKU cho 3 nhóm da
- Lõi 5: Thấy 320k hơi cao + review người thật, mua thử được từng món

**Nói với lớp:**

> "Đây là chỗ ăn tiền của cả buổi. Năm lõi này quyết định 14 ngày có nhàm hay không. Agent trả về năm lõi mà đọc lên thấy giông giống nhau thì đừng viết tiếp, quay lại sửa lõi. Sửa 5 dòng ở đây rẻ hơn sửa 30 mẩu ở dưới."

Mục 7 mà agent ghi "tăng nhận diện thương hiệu" thì bắt sửa ngay: chỉ số phải đếm được, ví dụ số bình luận từ khóa, số inbox mới, số click có UTM, số đơn có mã.

---

## C · 09:00 đến 16:00 · Lịch 14 ngày

**Thao tác:** Yêu cầu bảng, ép rõ tỷ lệ loại ngày.

**Prompt nguyên văn:**

```
Dựa trên campaign brief vừa rồi, lên lịch nội dung 14 ngày.

Xuất ra dạng bảng markdown, đúng 8 cột:
Ngày | Kênh | Định dạng | Loại ngày | Góc nội dung | Pain | USP | Lời kêu gọi

Ràng buộc về nhịp:
- Đúng 4 loại ngày: giáo dục, bằng chứng, xử lý phản đối, ưu đãi.
- Tỷ lệ: 5 giáo dục, 4 bằng chứng, 3 xử lý phản đối, 2 ưu đãi.
- Hai ngày ưu đãi đặt ở ngày 7 và ngày 14, không sớm hơn.
- Ba ngày liên tiếp không được dùng cùng một lõi nội dung.

Ràng buộc về sản lượng, đếm cho khớp:
- 10 bài social (1 trong đó là carousel)
- 3 email nurturing
- 3 video 30 đến 60 giây
- 1 khối landing page

Cột "Lời kêu gọi" phải là hành động đo được: bình luận từ khóa cụ thể,
inbox từ khóa cụ thể, bấm link có UTM, dùng mã giảm giá riêng kênh.
Không được ghi "tương tác" hay "tìm hiểu thêm".

Cuối bảng, đếm lại và ghi rõ: số ngày mỗi loại, tổng số bài mỗi định dạng.
```

**Kết quả mong đợi:** Bảng 14 dòng. Chiếu nguyên bảng này lên màn hình, đọc to vài dòng.

| Ngày | Kênh | Định dạng | Loại ngày | Góc nội dung | Pain | USP | Lời kêu gọi |
|---|---|---|---|---|---|---|---|
| 1 | Facebook | Bài chữ dài | Giáo dục | Đổi sản phẩm mới, ba ngày sau mặt đỏ rát | Sợ kích ứng | Không cồn, không hương liệu tổng hợp | Bình luận "THANHPHAN" nhận ảnh bảng thành phần |
| 2 | Facebook | Carousel 7 slide | Giáo dục | Đọc bảng thành phần trong 60 giây | Không biết đọc nhãn | Thành phần đọc là hiểu | Lưu bài, inbox "DOCNHAN" |
| 3 | Facebook | Ảnh review + caption ngắn | Bằng chứng | Trích nguyên văn R11 | Sợ đổi sản phẩm | Hợp da nhạy cảm | Bấm link Shopee gắn UTM xem đủ review |
| 4 | Email | Email 1 | Giáo dục | Vì sao da rát khi đổi sản phẩm | Sợ kích ứng | Đã test da liễu | Bấm link web đọc bảng thành phần |
| 5 | Facebook | Video 30 giây | Bằng chứng | Thử lên vùng cổ tay trước | Sợ thử đồ mới | Không cồn | Inbox "THUDA" nhận hướng dẫn thử |
| 6 | Facebook | Bài chữ hỏi đáp | Xử lý phản đối | "Bao lâu thấy hiệu quả?" trả lời thật | Sợ bị hứa hão | Nói thật, không cam kết thời gian | Inbox mô tả tình trạng da |
| 7 | Facebook + Shopee | Ảnh combo | Ưu đãi | Ưu đãi tuần 1, mã riêng kênh Facebook | Thấy 320k hơi cao | Combo tiết kiệm hơn mua lẻ | Dùng mã FB07 trên Shopee |
| 8 | Facebook | Bài chữ + ảnh so sánh | Giáo dục | Da bạn nhóm nào, chọn SKU nào | Không biết chọn | 3 SKU cho 3 nhóm da | Inbox "CHONSKU" mô tả da |
| 9 | Facebook + Email | Bài chữ + Email 2 | Xử lý phản đối | Ba câu inbox hỏi nhiều nhất | Còn phân vân | Tư vấn kỹ trước khi bán | Trả lời email kể tình trạng da |
| 10 | Facebook | Video 45 giây | Bằng chứng | Đọc to 3 review thật, để nguyên cả review 3 sao | Không tin quảng cáo | Review người thật, không cắt xén | Bấm link Shopee gắn UTM |
| 11 | Facebook | Bài chữ dài | Xử lý phản đối | Từng bị kích ứng thì đọc cái này trước khi mua bất cứ thứ gì | Sợ mất tiền vô ích | Hướng dẫn thử da trước khi dùng cả mặt | Inbox "ANTOAN" |
| 12 | Website + Facebook | Khối landing + bài dẫn link | Bằng chứng | Khối "Dành cho da đang dễ đỏ rát" | Cần chỗ đọc kỹ | Thành phần rõ, đã test da liễu | Bấm nút mua trên web hoặc Shopee |
| 13 | Facebook | Video 60 giây | Giáo dục | Một ngày chăm da tối giản cho da nhạy cảm | Không biết dùng thế nào | Ít bước, dễ theo | Inbox "ROUTINE" |
| 14 | Facebook + Shopee + Email | Ảnh + Email 3 | Ưu đãi | Ưu đãi đóng lúc 23h hôm nay | Chần chừ mãi | Combo tiết kiệm | Chốt đơn Shopee mã FB14 |

Đếm cuối bảng: giáo dục 5 (ngày 1, 2, 4, 8, 13), bằng chứng 4 (3, 5, 10, 12), xử lý phản đối 3 (6, 9, 11), ưu đãi 2 (7, 14). Social 10 (ngày 1, 2, 3, 6, 7, 8, 9, 11, 12, 14), email 3 (4, 9, 14), video 3 (5, 10, 13), carousel 1 (ngày 2), landing 1 (ngày 12).

**Nói với lớp:**

> "Nhìn cột 'Loại ngày'. Đây là cột giữ cho lịch không thành 14 bài bán hàng liên tiếp. Và nhìn ngày 10: agent để nguyên review 3 sao, không cắt đi. Đó là cố ý. Khách của mình hỏi kỹ 4 đến 6 lượt mới mua, họ nhận ra ngay khi thấy toàn 5 sao."

Nếu agent xếp ưu đãi vào ngày 3, chỉ vào đó và hỏi lớp: "Ngày 3 khách đã tin chưa? Chưa tin thì giảm giá để làm gì?"

---

## D · 16:00 đến 23:00 · Hai bài social khác định dạng, và một bản Twitter

Mốc này vẫn 7 phút: 5 phút cho hai bài, 2 phút cho bản Twitter 280 ký tự. Hai phút đó lấy từ phần đọc to nguyên văn bài B, chỉ chiếu bài B lên màn hình cho lớp tự đọc.

**Thao tác:** Yêu cầu viết hai bài đã có trong lịch, cố ý chọn hai bài khác loại ngày.

**Prompt nguyên văn:**

```
Viết đầy đủ 2 bài, nguyên văn caption, sẵn sàng đăng:

Bài A: ngày 1, Facebook, bài chữ dài, loại ngày giáo dục.
Bài B: ngày 6, Facebook, bài chữ hỏi đáp, loại ngày xử lý phản đối.

Gọi skill viet-bai-ban-hang để viết hai bài này, đừng tự viết từ đầu.
Truyền sang skill đó: SKU, nhóm khách, kênh, lõi nội dung của ngày đó,
số ký tự tối đa của kênh. Bài trả về thì bạn kiểm lại đúng lõi, đúng
loại ngày, và hai bài không trùng kiểu mở đầu.

Cấu trúc bắt buộc mỗi bài: 1 pain + 1 USP + 1 lời kêu gọi.
Mỗi bài phải chứa ít nhất một chi tiết trích được từ dữ liệu:
câu nguyên văn của khách, hoặc tên thành phần cụ thể.
Cấm tính từ trống nghĩa kiểu "chất lượng cao", "an toàn tuyệt đối".

Hai bài phải khác nhau ở: kiểu mở đầu, độ dài, lời kêu gọi.
Cuối mỗi bài ghi 1 dòng: bài này đẩy khách đi bước nào (biết / tin /
hỏi / mua) và đo bằng chỉ số gì.
```

**Kết quả mong đợi, chiếu nguyên văn lên màn hình:**

> **Bài A · Ngày 1**
>
> Đổi một lọ serum mới. Ba ngày sau hai bên má đỏ rát.
>
> Một chị viết trên Shopee: "Trước mình dùng loại khác bị nổi mẩn, đổi qua đây thì ổn. Sẽ mua lại."
>
> Nếu bạn cũng từng bị một lần rồi sợ luôn, đây là ba thứ nên nhìn trước khi mua bất cứ lọ nào, kể cả không phải của bên mình:
>
> 1. Bảng thành phần có cồn không.
> 2. Có hương liệu tổng hợp không.
> 3. Sản phẩm đã test da liễu chưa.
>
> Serum rau má B5 của Thảo An có ba thành phần chính: chiết xuất rau má, Panthenol B5, Glycerin. Không cồn, không hương liệu tổng hợp, đã test da liễu. Công dụng ghi trên nhãn: làm dịu da, hỗ trợ giảm thâm sau mụn, cấp ẩm.
>
> Mình không nói nó hợp với tất cả mọi người. Da mỗi người một khác.
>
> Bình luận "THANHPHAN" bên dưới, mình gửi ảnh bảng thành phần đầy đủ để bạn tự đọc trước khi quyết định.
>
> *Bước: biết. Đo bằng số bình luận từ khóa THANHPHAN và số lượt lưu bài.*

> **Bài B · Ngày 6**
>
> "Bao lâu thì thấy hiệu quả ạ?"
>
> Câu này inbox hỏi gần như mỗi tối. Trả lời thật:
>
> Mình không đưa được con số ngày. Ai nói chắc với bạn một mốc thời gian thì bạn nên nghi ngờ chỗ đó.
>
> Cái mình nói được:
>
> Thành phần là chiết xuất rau má, Panthenol B5, Glycerin. Không cồn, không hương liệu tổng hợp. Đã test da liễu. Công dụng ghi trên nhãn: làm dịu da, hỗ trợ giảm thâm sau mụn, cấp ẩm.
>
> Còn tốc độ thì để khách nói. Một chị sau 3 tuần: "Dùng 3 tuần thấy mấy vết thâm mụn cũ mờ đi chút." Một chị khác sau 1 tuần: "Dùng 1 tuần chưa thấy gì rõ lắm. Chắc phải kiên trì."
>
> Cả hai đều là review thật và mình để nguyên cả hai.
>
> Da bạn đang thế nào? Inbox mô tả giúp mình, không hợp thì mình nói thẳng là không hợp.
>
> *Bước: hỏi. Đo bằng số inbox mới và tỷ lệ inbox có mô tả tình trạng da.*

**Nói với lớp, chỉ vào từng chỗ khác nhau:**

> "Cùng một chiến dịch, cùng một nỗi sợ, nhưng khác nhau bốn chỗ. Bài A mở bằng cảnh, bài B mở bằng câu khách hỏi. Bài A dài, có danh sách để lưu lại; bài B ngắn, đọc một hơi. Bài A xin bình luận, bài B xin inbox, hai chỉ số khác nhau. Bài A ở bước 'biết', bài B ở bước 'hỏi', tức là hai nhóm khách đứng ở hai chỗ khác nhau trên đường tới đơn hàng. Nếu 10 bài của anh chị đều xin 'inbox ngay', anh chị đang nói chuyện với đúng một nhóm và bỏ chín nhóm còn lại."

Chỉ luôn cho lớp thấy dòng Claude báo nó đang gọi skill `viet-bai-ban-hang`. Nói: "Giọng văn trong hai bài này không phải từ skill hôm nay. Nó từ skill anh chị dựng buổi 1. Hôm nay mình dựng cái xếp lịch, không dựng lại cái viết bài."

**Thao tác cuối mốc, 2 phút:** Cùng một nội dung, đổi sang kênh chật hơn.

```
Lấy bài A vừa rồi, viết lại cho Twitter. Giới hạn 280 ký tự.
Giữ đúng 1 pain + 1 USP + 1 lời kêu gọi. Không cắt cụt giữa câu,
viết lại thành câu khác. Cuối bài ghi số ký tự thực tế.
```

**Kết quả mong đợi:** một bài dài hơn 1.500 ký tự rút xuống còn dưới 280, kiểu:

> Đổi serum mới, ba ngày sau má đỏ rát. Trước khi mua bất cứ lọ nào, nhìn 3 thứ: có cồn không, có hương liệu tổng hợp không, đã test da liễu chưa. Rau má B5 của Thảo An: không, không, rồi. Bình luận THANHPHAN để xem bảng thành phần.
>
> *(Twitter, 258/280)*

**Nói với lớp, chiếu hai bài cạnh nhau:**

> "Facebook cho 63.206 ký tự. Twitter cho 280. Chênh nhau hơn hai trăm lần. Nhìn hai bài này: không phải bài Twitter bị cắt ngắn, nó được viết lại. Ba thành phần vẫn còn, lời kêu gọi vẫn còn, chỉ mất phần kể chuyện. Cái mất phải là chuyện kể, không phải bằng chứng. Ai đang dán cùng một caption lên bốn kênh thì bốn kênh đều nhận một bài không hợp kênh nào."

Chỉ vào dòng đếm ký tự cuối bài: "Bắt agent tự đếm là để mình khỏi phải đếm. Nó ghi 258/280 thì mình biết bài dán được luôn, không phải mở app ra thử."

---

## E · 23:00 đến 29:00 · Bẫy vi phạm và khai báo ràng buộc

Đây là đoạn quan trọng nhất buổi. Làm chậm, đừng vội.

**Thao tác bước 1:** Mở một phiên mới **ở thư mục khác**, thư mục trống không có `CLAUDE.md` và không có skill nào, để mô phỏng trạng thái chưa khai báo ràng buộc.

**Prompt nguyên văn:**

```
Viết 3 câu mở đầu thật giật cho bài Facebook bán serum rau má B5,
sản phẩm cho da nhạy cảm, có công dụng hỗ trợ giảm thâm sau mụn.
Viết sao cho người lướt phải dừng lại.
```

**Kết quả mong đợi:** Agent trả về những câu kiểu:

- "Giúp bạn hết thâm chỉ sau 7 ngày!"
- "Đặc trị thâm mụn cho da nhạy cảm, cam kết hiệu quả."
- "Tạm biệt thâm mụn, da trắng sáng bật tông sau 2 tuần."

**Nói với lớp:**

> "Câu một: cam kết thời gian, sai. Câu hai: 'đặc trị' và 'cam kết hiệu quả', sai hai lỗi. Câu ba: sai cả từ lẫn mốc thời gian. Agent không cố tình làm bậy, nó viết đúng thứ mình yêu cầu là câu giật; mà câu giật trong ngành mỹ phẩm trên mạng mặc định trông như thế này. Lỗi nằm ở chỗ mình chưa nói nó không được viết gì."

Hỏi lớp: "Nếu chỗ này là 30 mẩu nội dung chứ không phải 3 câu, ai ngồi dò?"

**Thao tác bước 2:** Quay lại phiên trong thư mục làm việc, nơi skill `content-engine` đang chạy. Chiếu đúng khối ràng buộc trong file `SKILL.md` lên màn hình cho lớp nhìn, rồi chạy lại đúng prompt cũ.

```
KHÔNG ĐƯỢC VIẾT, ưu tiên cao nhất, áp cho mọi output:

Từ cấm tuyệt đối:
trị mụn · đặc trị · khỏi hẳn · trắng da cấp tốc · bật tông ·
cam kết hiệu quả · hết thâm · dứt điểm

Cấm cam kết thời gian có kết quả: không viết "sau 7 ngày", "sau 2 tuần",
"chỉ 1 tháng" gắn với bất kỳ kết quả nào trên da.

Cấm nói sản phẩm là thuốc hoặc có tác dụng chữa bệnh.
Cấm so sánh trực tiếp bằng tên với thương hiệu khác.
Cấm nêu thành phần hoặc công dụng ngoài bảng trong hồ sơ sản phẩm.
Cấm gắn tên persona vào lời chứng thực. Persona là suy luận, không phải
người thật. Muốn trích lời khách thì trích nguyên văn R01-R15 hoặc M01-M15.

Chỉ được dùng đúng cụm công dụng ghi trên nhãn:
"làm dịu da", "hỗ trợ giảm thâm sau mụn", "cấp ẩm".

Trước khi xuất bất kỳ nội dung nào: tự rà một lượt. Nếu một câu chạm
danh sách trên, viết lại câu đó rồi mới xuất. Không xuất kèm ghi chú
xin lỗi, chỉ xuất bản đã sạch.
```

**Kết quả mong đợi:** Cùng một yêu cầu, agent trả về những câu kiểu:

- "Đổi mỹ phẩm mới mà sợ mặt lại đỏ rát? Đọc bảng thành phần trước đã."
- "Không cồn, không hương liệu tổng hợp, đã test da liễu. Ba dòng, tự kiểm tra được."
- "Chị nào từng bị kích ứng một lần rồi sợ luôn, bài này viết cho chị."

**Nói với lớp:**

> "Vẫn giật, vẫn dừng tay người lướt, nhưng không câu nào đưa mình ra tòa hay bị Facebook chặn quảng cáo. Và chú ý: mình không sửa câu nào cả, mình sửa cái máy. Từ giờ tới cuối chiến dịch, 30 mẩu nội dung đều đi qua bộ lọc này."

**Thao tác bước 3:** Chạy prompt tự rà, cho lớp thấy cách kiểm tra lại:

```
Rà lại toàn bộ nội dung đã viết trong chat này. Liệt kê dạng bảng:
câu vi phạm | vi phạm điều nào | câu thay thế.
Không có vi phạm thì ghi "không có", đừng bịa ra để có cái mà báo.
```

---

## F · 29:00 đến 35:00 · Kịch bản video và brief hình ảnh

**Thao tác:** Xin video trước, brief hình ảnh sau.

**Prompt nguyên văn:**

```
Viết kịch bản video ngày 5, dài 30 giây, quay bằng điện thoại,
một người, không cần diễn viên.

Format bảng 4 cột: Giây | Hình | Lời thoại | Chữ trên màn hình.
Chia theo block 5 giây.
Câu đầu tiên phải nói được nỗi sợ trong 3 giây đầu.
Lời kêu gọi đặt ở 5 giây cuối, kèm từ khóa inbox.
Áp đủ ràng buộc từ cấm.
```

**Kết quả mong đợi:**

| Giây | Hình | Lời thoại | Chữ trên màn hình |
|---|---|---|---|
| 0-5 | Cận mặt, tay chỉ vào vùng má | "Từng đổi mỹ phẩm rồi mặt đỏ rát chưa?" | TỪNG BỊ MỘT LẦN LÀ SỢ LUÔN |
| 5-12 | Cận chai serum, xoay nhãn cho thấy bảng thành phần | "Trước khi bôi cả mặt, thử lên cổ tay đã." | THỬ TRƯỚC Ở CỔ TAY |
| 12-20 | Nhỏ 2 giọt lên mặt trong cổ tay, thoa nhẹ | "Rau má, B5, Glycerin. Không cồn, không hương liệu tổng hợp." | 3 THÀNH PHẦN, ĐỌC LÀ HIỂU |
| 20-25 | Cổ tay sau khi thoa, giữ yên khung hình | "Đã test da liễu. Để 24 tiếng xem da phản ứng thế nào." | ĐÃ TEST DA LIỄU |
| 25-30 | Cầm chai, nhìn thẳng camera | "Muốn hướng dẫn thử da đầy đủ thì inbox chữ THUDA." | INBOX: THUDA |

**Nói với lớp:**

> "Để ý giây 20 đến 25: 'để 24 tiếng xem da phản ứng thế nào'. Đây là mốc thời gian nhưng không phải cam kết kết quả, nó là hướng dẫn sử dụng. Ranh giới nằm ở chỗ đó. Cấm hứa kết quả theo thời gian, không cấm nói cách dùng."

**Prompt tiếp theo:**

```
Viết 5 brief hình ảnh cho 5 ngày sau: 1, 2, 3, 7, 12.

Mỗi brief đúng 6 mục:
1. Mục đích (bài này cần người xem hiểu gì trong 1 giây)
2. Bố cục
3. Chủ thể trong khung
4. Chữ trên ảnh, viết nguyên văn, tối đa 8 từ
5. Tỷ lệ khung và nơi đăng
6. Không được xuất hiện

Mục 6 phải cụ thể, ví dụ: không dùng ảnh trước và sau, không dùng ảnh
da người khác không phải khách thật, không ghi con số ngày.

Viết sao cho người thiết kế chưa từng nghe tên Thảo An vẫn làm ra được.
```

**Kết quả mong đợi, đọc 1 brief làm mẫu cho lớp:**

> **Brief ngày 3 · Ảnh review**
> 1. Mục đích: người xem hiểu ngay đây là lời của khách thật, không phải lời quảng cáo.
> 2. Bố cục: nền trơn màu kem, ảnh chụp màn hình review Shopee đặt lệch trái, chai serum đặt góc dưới phải, nhỏ, không che chữ.
> 3. Chủ thể: ảnh chụp màn hình review R11 giữ nguyên giao diện Shopee, còn thấy số sao và ngày đăng.
> 4. Chữ trên ảnh: "Đổi qua đây thì ổn."
> 5. Tỷ lệ 4:5, đăng Facebook.
> 6. Không được xuất hiện: ảnh da mặt cận cảnh, ảnh trước và sau, con số ngày, logo thương hiệu khác, chữ tiếng Anh.

**Chốt demo, nói với lớp:**

> "Ba mươi lăm phút, một insight, ra được brief, lịch 14 ngày, bài viết, video, brief hình ảnh. Sáu mươi lăm phút tới anh chị làm y hệt trên sản phẩm của mình. Ai chưa có dữ liệu thật thì dùng nguyên bộ Thảo An, vẫn nộp đủ bài."
