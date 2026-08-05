# BÀI SOẠN GIÁO VIÊN - BUỔI 4

## Nắm xu hướng thị trường, để agent tự chạy ra content

> Bản script giảng được ngay. Đọc theo, không cần soạn thêm.
> Lớp: 10 đến 20 người làm sale và marketing. Chủ doanh nghiệp nhỏ, trưởng phòng marketing, nhân sự content, nhân sự ads. Phần lớn KHÔNG biết code, chưa quen dòng lệnh. Đây là ràng buộc thiết kế quan trọng nhất của buổi. Mỗi thao tác phải ghi rõ bấm gì, gõ gì, thấy gì thì biết đúng.
> Học online live qua Zoom hoặc Google Meet. Giảng viên chia sẻ màn hình, học viên làm trên máy mình và chia sẻ màn hình lại khi cần hỗ trợ.
> Công cụ học viên dùng: **Claude Desktop, tab Code**. Cả buổi làm ở tab Code.
> Case study xuyên suốt: **Thảo An**, thương hiệu mỹ phẩm thảo mộc giả định, 3 SKU, bán B2C qua Facebook và Shopee, bán sỉ B2B cho spa.
> Thời lượng: 150 phút, đã gồm 10 phút giải lao.
> Nguyên tắc thiết kế xuyên suốt: **đau trước, giải pháp sau.** Mỗi khối mở bằng một nỗi đau anh chị tự cảm, rồi công cụ mới hiện ra như lời giải. Mỗi phần có Lý thuyết ngắn rồi Thao tác có prompt.
> Nối tiếp buổi 2 và 3: buổi 2 anh chị hiểu MCP và lập được agent. Buổi 3 dùng agent làm ra ảnh. Buổi 4 cho agent một giác quan mới: nghe ngóng thị trường. KHÔNG giảng lại MCP hay agent từ đầu, chỉ nhắc một câu.
> Hình buổi: hai lần nối công cụ ở đầu (tikhub và last30days) chủ yếu XEM và HIỂU. Phần chính (K3, K4) TỰ TAY LÀM, mang về dùng ngày mai. Đừng dồn sức vào khâu cài mà cạn giờ cho K4.

---

## LƯU Ý LỚN NHẤT CHO GIẢNG VIÊN, ĐỌC TRƯỚC KHI DẠY

Buổi này nặng hơn buổi 3, vì có **hai lần nối công cụ** chứ không phải một: tikhub và last30days. Với lớp không biết code, phần lớn sẽ KHÔNG tự cài cả hai tại chỗ. Cách xử lý đã chốt:

1. **tikhub: học viên đăng ký tài khoản ở nhà trước buổi** (đã dặn từ buổi Customer Insight). Trong buổi chỉ nối vào Claude và cào, không ngồi đăng ký giữa giờ.
2. **last30days: giảng viên cài sẵn và demo. Học viên xem, mang hướng dẫn về nhà tự cài.** Đây là phần cài khó nhất khóa: cần Python 3.12 trở lên, và lần chạy đầu có bước thiết lập tự động. Ai máy đã có Python thì cài cùng tại lớp, càng tốt. Ai không, xem demo, vẫn học trọn buổi bằng file kết quả mẫu.
3. **Nói thẳng câu này với lớp ở đầu K1:** "Buổi nay có hai công cụ cần nối. Cái đầu, tikhub, anh chị đã đăng ký ở nhà rồi, giờ mình nối vào. Cái sau, last30days, cài hơi khó, tôi làm mẫu cho anh chị xem, ai làm được thì làm cùng, chưa được thì mang hướng dẫn về nhà. Không ai bị bỏ lại, vì tôi có sẵn file kết quả mẫu để cả lớp cùng làm phần chính."

**Ba con dao phải cầm chắc, nhắc lại cuối buổi:**
- **Mỗi lượt gọi tikhub tính tiền.** Nghĩ trước khi bấm, đừng gọi loạn.
- **Routine không tự đăng.** Nó chỉ chạy tới bản tin và nháp content. Người duyệt rồi mới đăng tay.
- **Chống bịa số.** Agent chỉ nói dựa trên dữ liệu hai nguồn trả về. Suy ra thì gắn `[SUY LUẬN]`.

**Ba việc giảng viên phải làm trước buổi (bắt buộc, vì giao diện và lệnh hay đổi):**
1. Tự nối tikhub vào Claude trên máy mình, chạy thử một lượt cào xu hướng, xem còn đúng đường bấm không. Ghi ra giấy các bước.
2. Cài sẵn last30days, chạy `/last30days` một chủ đề, chụp lại kết quả để có file mẫu phát cho lớp.
3. Lập sẵn agent nắm xu hướng và một routine trên máy mình, chạy thử, để lát demo trơn.

---

## BẢNG MỐC ĐỒNG HỒ CẢ BUỔI

Giả định giờ bắt đầu 08h00. Bắt đầu giờ khác thì cộng dồn tương ứng.

| Khối | Đồng hồ | Phút | Nội dung | Ai làm |
|---|---|---|---|---|
| K0 | 08:00 - 08:10 | 10 | Mở đầu: đăng theo cảm tính là đoán mò | Giảng 6 + học viên 4 |
| K1 | 08:10 - 08:40 | 30 | tikhub: nối vào Claude, cào xu hướng đúng ngành | Demo và thực hành |
| K2 | 08:40 - 09:05 | 25 | last30days: cài và nghe ngóng đa nền tảng | Demo 15 + thực hành hoặc xem 10 |
| Giải lao | 09:05 - 09:15 | 10 | Nghỉ | |
| K3 | 09:15 - 09:40 | 25 | Ghép hai nguồn thành bản tin xu hướng | Giảng và demo 8 + thực hành 17 |
| K4 | 09:40 - 10:10 | 30 | Lập trợ lý nắm xu hướng (đỉnh buổi) | Giảng và demo 10 + thực hành 20 |
| K5 | 10:10 - 10:25 | 15 | Routine: cho trợ lý tự chạy theo lịch | Giảng và demo 8 + thực hành 7 |
| K6 | 10:25 - 10:30 | 5 | Chốt và giao bài | Giảng 5 |

**Cộng lại để tự kiểm:** 10 + 30 + 25 + 10 + 25 + 30 + 15 + 5 = **150 phút**, khớp thời lượng khai báo.

**Tay học viên đặt trên bàn phím:** K0 4 phút, K1 tùy máy, K2 tùy máy (ai cài được thì 10, chưa thì xem), K3 17 phút, K4 20 phút, K5 7 phút. Đỉnh thực hành là K4 (lập agent nắm xu hướng). Đừng ép khâu cài thành thực hành cả lớp.

**Mốc phải bám cứng:** 08:40 xong K1. 09:40 xong K3. **Không cắt K4.** K4 là sản phẩm chính học viên mang về.

**Lưu ý về giao diện và lệnh:** app Claude Desktop, đường nối MCP, lệnh cài last30days, và cách bật routine có thể đổi theo phiên bản. Mọi chỗ bài này mô tả đường bấm hay lệnh gõ, trước buổi phải mở máy kiểm lại và ghi ra giấy nhắc. Các điểm cần kiểm đánh dấu **[KIỂM TRƯỚC BUỔI]** trong từng khối.

---

## K0. MỞ ĐẦU: ĐĂNG THEO CẢM TÍNH LÀ ĐOÁN MÒ (10 phút, 08:00 - 08:10)

### LỜI GIẢNG (6 phút)

"Chào anh chị. Ba buổi vừa rồi anh chị đã dạy Claude viết bài đúng giọng, đóng gói việc lặp thành nút bấm, và làm ra ảnh để đăng. Giờ tôi hỏi một câu, giơ tay thật lòng giúp tôi: tuần rồi anh chị đăng bài dựa vào đâu? Vào việc mình nghĩ khách sẽ thích, hay vào việc thị trường ngoài kia đang thật sự bàn?"

*(Dừng 10 giây. Phần lớn thừa nhận là tự nghĩ. Để nguyên đó.)*

"Đúng rồi. Phần lớn ta ngồi trong phòng kín tự nghĩ ra nội dung. Mà ngoài kia, trên TikTok, trên các diễn đàn, người ta đang bàn chủ đề khác, đang lên hashtag khác, đối thủ đang ăn với dạng bài khác. Mình không nghe được, nên mình đoán. Đoán trúng thì may, đoán trật thì phí cả buổi làm content."

"Hôm nay ta gỡ đúng chỗ đó. Cuối buổi, anh chị có một trợ lý có tai. Nó nghe thị trường qua hai nguồn, chỉ cho anh chị tuần này nên nói về cái gì, rồi tự làm việc đó mỗi tuần, để sẵn cho anh chị đọc khi mở máy. Từ chỗ đoán mò sang chỗ đăng theo cái thị trường đang quan tâm."

"Tôi kể một cảnh quen. Sáng thứ Hai, phải lên lịch content tuần. Ngồi nhìn màn hình trắng, không biết viết gì, bí quá lôi lại chủ đề tuần trước xào lại. Trong khi đúng lúc đó, trên TikTok đang nổi một trào lưu hợp sản phẩm mình mà mình không hề biết. Lỡ sóng chỉ vì không có cái tai nghe thị trường."

*(Dừng cho vài người gật.)*

"Buổi nay có hai công cụ cần nối. Tôi sẽ nói rõ cái nào làm cùng, cái nào xem tôi làm. Đừng lo cài đặt, phần chính là dạy trợ lý nghe thị trường, ai cũng làm được."

### THAO TÁC HỌC VIÊN (4 phút)

Nói trước: "Bốn phút này chỉ mở lại chỗ làm việc, chưa làm gì nặng."

**Bước 1. Mở lại thư mục làm việc.**

1. Mở Claude Desktop.
2. Bấm tab **Code** ở hàng trên cùng.
3. Mở thư mục làm việc của anh chị (`thao-an-marketing` hoặc thư mục thương hiệu thật, đã dựng từ buổi 2).

**Bước 2. Gõ một câu kiểm tra nhanh.**

**PROMPT B4-0:**

```
Bạn đang mở thư mục nào, và trong thư mục này đã có file CLAUDE.md chưa?
Trả lời ngắn gọn.
```

**Tiêu chí coi là xong:** mỗi máy mở đúng thư mục, Claude xác nhận có `CLAUDE.md`. File này quan trọng cho cả buổi, vì lát nữa trợ lý nắm xu hướng sẽ đọc nó để biết ngành và giọng thương hiệu, gợi ý content mới hợp với mình.

### DỰ PHÒNG

- **Máy chưa có `CLAUDE.md`:** phát bộ Thảo An mẫu (`thao-an-marketing` có sẵn `san-pham-thao-an.md` và `CLAUDE.md`), tải về mở bằng tab Code. Vẫn theo được cả buổi.
- **App cũ không thấy tab Code:** tải bản mới ở claude.ai/download. Trong lúc chờ, xem chung màn hình một bạn.

---

## K1. TIKHUB: NỐI VÀO CLAUDE, CÀO XU HƯỚNG ĐÚNG NGÀNH (30 phút, 08:10 - 08:40)

**Câu hỏi dẫn:** Claude không tự vào TikTok đọc số liệu được. Vậy làm sao nó biết trên TikTok đang nổi cái gì trong ngành mình?

**Mục tiêu khối:** nối tikhub vào Claude, cào được một mẻ xu hướng KHÓA ĐÚNG NGÀNH của mình, lưu thành file. Không cào chung chung.

### PHẦN 1: LÝ THUYẾT (4 phút)

"Buổi 2 anh chị biết MCP là cái thẻ cho Claude với tới công cụ ngoài. Nhắc một câu thôi. Hôm nay cái thẻ đó cắm vào **tikhub**, một dịch vụ đọc dữ liệu công khai trên TikTok, Instagram, YouTube. Buổi Customer Insight sắp tới ta dùng nó đọc bình luận để hiểu nỗi đau khách. Buổi nay dùng theo hướng khác: **đọc cái đang nóng của cả ngành.**"

"Hai điều ghi vào vở ngay:"
- "**Mỗi lượt gọi tính tiền.** Phản hồi của dịch vụ ghi thẳng câu 'This request will incur a charge'. Nên nghĩ kỹ mình muốn hỏi gì rồi mới bấm, đừng gọi loạn mười mấy lần."
- "**Cào đúng ngành mới có giá trị.** Bảo nó 'cho tôi xu hướng' chung chung thì ra rác, toàn chuyện không dính dáng. Phải khóa theo từ khóa ngành, hashtag ngành, hoặc đối thủ cụ thể. Ví dụ Thảo An thì khóa vào 'dưỡng da thảo mộc', 'trị mụn', 'serum', chứ không phải 'làm đẹp' chung."

**Nói rõ tikhub làm gì trong buổi này, để lớp không kỳ vọng sai. Chiếu bảng:**

| tikhub trong buổi này | Dùng để |
|---|---|
| Xem cái đang tìm kiếm và hashtag đang lên trên TikTok | Biết trào lưu chung đang nổi gì |
| Tìm video đang lên theo từ khóa ngành | Biết trong ngành mình đang nóng chủ đề nào |
| Xem bài mới và bình luận của một đối thủ | Biết đối thủ đang làm dạng nội dung gì, khách phản ứng ra sao |

### PHẦN 2: THAO TÁC NỐI TIKHUB (giảng viên demo, 8 phút)

**[KIỂM TRƯỚC BUỔI]** Đường nối tikhub vào Claude Desktop tùy phiên bản app. Trước buổi mở máy làm lại, ghi đúng đường bấm ra giấy.

**Giảng viên làm trên màn hình, đọc to từng bước. Học viên đã đăng ký tikhub thì làm cùng.**

Bước nối, mô tả theo ý niệm (đường bấm cụ thể xem màn hình giảng viên):

1. **Lấy khóa từ tikhub.** Vào `user.tikhub.io`, đăng nhập tài khoản đã tạo ở nhà. Vào mục API Keys, tạo một khóa, bấm copy. Khóa này như mật khẩu, không đưa cho ai.
2. **Dán khóa vào Claude.** Trong Claude Desktop, mở phần kết nối công cụ ngoài (Connectors hoặc phần cấu hình MCP), thêm tikhub, dán khóa vào. Lưu lại.
3. **Bật lại cho Claude nhận công cụ** nếu app yêu cầu.

**Kiểm tra đã nối được chưa. PROMPT B4-1 (prompt kiểm tra kết nối):**

```
Bạn có đang thấy công cụ tikhub không? Liệt kê ngắn gọn vài việc bạn làm được
với tikhub liên quan tới TikTok. Chưa thấy thì nói thẳng là chưa thấy.
```

**Tiêu chí coi là xong:** Claude trả lời có thấy tikhub và kể được vài việc (tìm video, đọc bình luận, xem hashtag). Nếu nó nói chưa thấy, kết nối chưa xong, kiểm lại bước 2.

### PHẦN 3: THAO TÁC CÀO XU HƯỚNG ĐÚNG NGÀNH (thực hành, 18 phút)

"Giờ cào thật. Ba mẻ, từ rộng tới hẹp. Anh chị thay chủ đề Thảo An bằng ngành của mình."

**Mẻ 1. Cái đang nóng chung trên TikTok. PROMPT B4-2 (prompt chạy test lần đầu, nhẹ):**

```
Dùng tikhub, cho tôi xem hiện trên TikTok đang có những từ khóa tìm kiếm
và hashtag nào đang lên. Chỉ cần một danh sách ngắn, kèm con số nếu có.
```

*(Giảng viên: Claude sẽ gọi các lệnh dạng trending searchwords và trends hashtag list của tikhub. Đây là mẻ nhẹ để lớp thấy tikhub chạy thật, ra số thật.)*

**Điểm dừng bắt buộc (sau mẻ 1):** "Ai đã thấy tikhub trả về danh sách thật thì giơ tay." Chờ tối thiểu hai phần ba lớp. Máy nào chưa ra, kiểm kết nối ở PHẦN 2.

**Mẻ 2. Cái đang nóng ĐÚNG NGÀNH mình. PROMPT B4-3:**

```
Dùng tikhub, tìm trên TikTok những video đang có nhiều lượt xem gần đây
về chủ đề [dưỡng da thảo mộc, trị mụn, serum thiên nhiên].
Với mỗi video cho tôi: tiêu đề hoặc mô tả ngắn, lượt xem, hashtag chính.
Lưu kết quả thành file xu-huong-tikhub.md trong thư mục làm việc.
KHÔNG lấy tên tài khoản người dùng, chỉ giữ nội dung công khai.
```

Nhắc học viên: **thay cụm trong ngoặc vuông bằng đúng ngành của mình.** Ai bán đồ ăn thì để món ăn, ai làm nội thất thì để nội thất.

**Mẻ 3. Đối thủ đang làm gì (tùy chọn, nếu còn giờ). PROMPT B4-4:**

```
Dùng tikhub, xem vài bài đăng gần đây của tài khoản TikTok [tên hoặc @ đối thủ],
và đọc một ít bình luận dưới đó. Tóm cho tôi: họ đang làm dạng nội dung gì,
khách khen chê điều gì. Ghi thêm vào cuối file xu-huong-tikhub.md.
```

**Tiêu chí coi là xong khối K1:** mỗi máy (hoặc máy nào nối được tikhub) có file `xu-huong-tikhub.md` chứa vài video đang lên đúng ngành. Máy chưa nối được tikhub: phát file `xu-huong-tikhub-mau.md` mẫu để dùng ở K3.

### DỰ PHÒNG K1

- **Chưa nối được tikhub trong 8 phút:** dừng, không kéo cả lớp chờ. Phát file xu hướng mẫu, cho làm bù ở nhà theo hướng dẫn.
- **tikhub báo hết lượt hoặc lỗi phí:** tài khoản chưa nạp đủ. Dùng file mẫu, nạp sau.
- **Ra kết quả nhưng lệch ngành:** do từ khóa quá rộng. Sửa cụm trong ngoặc vuông cho hẹp lại, cào lại một lần (nhắc: tốn thêm phí).

---

## K2. LAST30DAYS: CÀI VÀ NGHE NGÓNG ĐA NỀN TẢNG (25 phút, 08:40 - 09:05)

**Câu hỏi dẫn:** tikhub nghe được TikTok. Nhưng người ta còn bàn tán trên Reddit, YouTube, tin tức, diễn đàn. Làm sao nghe luôn mấy chỗ đó?

**Mục tiêu khối:** lớp HIỂU last30days làm gì, thấy nó chạy ra kết quả thật. Ai cài được thì có công cụ; ai chưa, biết đường làm bù ở nhà.

### PHẦN 1: LÝ THUYẾT (4 phút)

"tikhub mạnh ở TikTok, Instagram. Nhưng xu hướng còn nằm ở Reddit, YouTube, tin tức. **last30days** là một công cụ chuyên trả lời đúng một câu: '30 ngày qua người ta nói gì về [chủ đề]'. Nó gom bài và lượt tương tác từ nhiều nền tảng, rồi tóm lại: cái gì đang nóng, ai đang khen, ai đang chê."

"Tôi nói thẳng để anh chị không sốt ruột: **đây là công cụ cài khó nhất khóa.** Nó cần Python 3.12 trở lên trên máy, và lần chạy đầu nó tự cài thêm vài thứ nền. Tôi đã cài sẵn trên máy tôi. Bây giờ tôi làm mẫu cho anh chị thấy nó chạy ra gì. Ai máy có sẵn Python thì cài cùng. Ai chưa, cứ xem, tôi có sẵn file kết quả để lát cả lớp cùng làm phần chính."

### PHẦN 2: THAO TÁC CÀI (giảng viên demo, 11 phút)

**[KIỂM TRƯỚC BUỔI]** Cài sẵn last30days, chạy thử một chủ đề, lưu kết quả làm file mẫu. Ghi lại đúng lệnh còn chạy được.

**Bước 1. Kiểm máy đã có Python 3.12 chưa.** last30days cần cái này. Prompt hỏi Claude kiểm hộ.

**PROMPT B4-5 (prompt để AI kiểm điều kiện cài):**

```
Kiểm giúp tôi máy này đã có Python phiên bản 3.12 trở lên chưa.
Nếu chưa có, chỉ cho tôi một lệnh để cài trên Windows. Nói ngắn gọn.
```

*(Trên Windows lệnh cài thường là `winget install Python.Python.3.12`. Giảng viên demo. Ai chưa có Python thì đây là lý do để về nhà cài, đừng cài giữa buổi vì mất thời gian.)*

**Bước 2. Cài last30days vào Claude.** Với Claude Desktop tab Code, đường gọn là thêm bộ cài qua marketplace.

**PROMPT B4-6 (prompt để AI cài đặt công cụ):**

```
Cài giúp tôi bộ công cụ last30days từ marketplace mvanhorn/last30days-skill,
rồi nói cho tôi biết đã cài xong chưa và tôi gọi nó bằng cách nào.
```

*(Nếu app không cài qua prompt được thì làm tay: lệnh `/plugin marketplace add mvanhorn/last30days-skill`. Giảng viên [KIỂM TRƯỚC BUỔI] xem đường nào chạy trên máy mình.)*

**Bước 3. Chạy kiểm tra sức khỏe.** Xem nguồn nào đã nối, nguồn nào chưa.

**PROMPT B4-7:**

```
Chạy last30days ở chế độ kiểm tra sức khỏe (doctor) để tôi xem
nguồn dữ liệu nào đã sẵn sàng, nguồn nào chưa.
```

### PHẦN 3: CHẠY THẬT MỘT LẦN (demo, ai cài được thì làm cùng, 10 phút)

**Chạy đúng ngành. PROMPT B4-8 (prompt chạy test last30days):**

```
Chạy last30days cho chủ đề: [dưỡng da thảo mộc trị mụn].
Cho tôi biết 30 ngày qua người ta đang bàn gì, khen gì, chê gì về chủ đề này.
```

Nhắc thay cụm trong ngoặc theo ngành mình.

**Chỉ thêm chế độ bắt xu hướng. PROMPT B4-9:**

```
Chạy last30days ở chế độ tìm xu hướng cho ngành [làm đẹp, chăm sóc da]:
đang nổi lên những chủ đề gì đáng làm nội dung.
```

*(Đây là chế độ discovery của last30days: nó tự gợi ý chủ đề đang lên, kèm góc nội dung. Rất hợp việc lên lịch content.)*

**Tiêu chí coi là xong khối K2:** lớp thấy last30days chạy ra một bản tóm xu hướng thật. Ai cài được thì có file kết quả của mình. Ai chưa, cầm file mẫu của giảng viên để dùng ở K3.

### DỰ PHÒNG K2

- **Máy không có Python 3.12:** không cài giữa buổi. Xem demo, cài ở nhà theo hướng dẫn, dùng file mẫu.
- **Lần chạy đầu đứng lâu:** bình thường, lần đầu nó cài thêm vài thứ và quét nhiều nguồn, mất vài phút. Đừng bấm lại liên tục.
- **Một vài nguồn báo chưa nối (X, TikTok qua last30days):** không sao, các nguồn miễn phí như Reddit, YouTube, web vẫn chạy. Đủ để thấy xu hướng.

---

## GIẢI LAO (10 phút, 09:05 - 09:15)

Bắt buộc, không gộp. Giảng viên dùng 10 phút này gỡ máy nào chưa cào tikhub được, và bảo đảm mọi người có ít nhất file xu hướng (của mình hoặc file mẫu) để vào K3.

---

## K3. GHÉP HAI NGUỒN THÀNH BẢN TIN XU HƯỚNG (25 phút, 09:15 - 09:40)

**Câu hỏi dẫn:** Có hai đống dữ liệu rồi, tikhub một bên, last30days một bên. Nhìn riêng thì rối. Làm sao gộp thành một tờ giấy đọc là biết tuần này nên làm gì?

**Mục tiêu khối:** ra một file `ban-tin-xu-huong.md` gọn: 5 chủ đề đang nóng, mỗi chủ đề kèm một góc content làm được.

### PHẦN 1: LÝ THUYẾT (5 phút)

"Hai nguồn nhìn hai góc. tikhub thấy cái đang lên trên video ngắn. last30days thấy cái đang bàn trên diễn đàn và tin tức. Ghép lại mới đủ. Và đây là mẹo quan trọng: **một chủ đề nóng ở CẢ HAI nơi là chủ đề đáng làm ngay tuần này.** Nóng một nơi thì cân nhắc, nóng cả hai thì làm liền."

"Nhắc nguyên tắc chống bịa, lần này áp cho xu hướng: agent chỉ được nói dựa trên dữ liệu hai file trả về. Nó KHÔNG được tự chế con số 'chủ đề này tăng 300 phần trăm' nếu số đó không có trong dữ liệu. Cái gì nó suy ra thì bắt nó ghi `[SUY LUẬN]`."

### PHẦN 2: THAO TÁC GHÉP (thực hành, 20 phút)

**Prompt ghép hai nguồn. PROMPT B4-10:**

```
Đọc hai nguồn xu hướng của tôi:
1. File xu-huong-tikhub.md trong thư mục làm việc.
2. Kết quả last30days về ngành của tôi (dán vào đây, hoặc đọc file nếu đã lưu).

Lập cho tôi một BẢN TIN XU HƯỚNG tuần này, đúng 5 chủ đề đang nóng.
Mỗi chủ đề trình bày:
- Tên chủ đề
- Nóng ở đâu: chỉ TikTok, chỉ diễn đàn, hay cả hai
- Vì sao đang nóng (dựa trên dữ liệu, ghi rõ)
- Một góc content tôi có thể làm cho thương hiệu của tôi

Đọc CLAUDE.md để gợi ý góc content hợp ngành và giọng của tôi.
Chủ đề nào chỉ thấy ở một nguồn thì ghi rõ. Số liệu nào không có trong dữ liệu
thì đừng bịa, ghi "chưa đủ dữ liệu". Phần suy luận gắn nhãn [SUY LUẬN].
Lưu kết quả thành file ban-tin-xu-huong.md.
```

**Kiểm nhanh chất lượng. Nói với lớp:** "Mở file `ban-tin-xu-huong.md`, tìm xem có chủ đề nào ghi 'nóng ở cả hai' không. Đó là chủ đề đáng làm nhất. Và soi thử một con số: nó có ghi nguồn không, hay bịa ra."

**Ra 2 bài từ bản tin (nếu còn giờ). PROMPT B4-11:**

```
Từ bản tin xu hướng vừa rồi, chọn 2 chủ đề nóng nhất.
Dùng skill viết bài bán hàng đã có của tôi, viết cho mỗi chủ đề một bài đăng
Facebook bám đúng xu hướng đó, đúng giọng thương hiệu.
```

**Tiêu chí coi là xong khối K3:** mỗi máy có `ban-tin-xu-huong.md` với 5 chủ đề, mỗi chủ đề có góc content. Điểm phải thấy: ít nhất một chủ đề ghi rõ nóng ở nguồn nào, và không có số bịa.

### DỰ PHÒNG K3

- **Bản tin chung chung, không dính ngành:** do dữ liệu nguồn quá rộng. Nhắc quay lại K1 cào hẹp hơn, hoặc bảo Claude "bám sát ngành [X] trong CLAUDE.md, bỏ chủ đề không liên quan".
- **Agent bịa số tăng trưởng:** đây là tình huống dạy được, chiếu lên cho cả lớp. Nhắc lại: bắt nó ghi nguồn, không có thì ghi "chưa đủ dữ liệu".

---

## K4. LẬP TRỢ LÝ NẮM XU HƯỚNG (30 phút, 09:40 - 10:10, ĐỈNH BUỔI)

**Câu hỏi dẫn:** Làm tay từng bước như nãy thì mỗi tuần lặp lại mệt. Có cách nào gói cả quy trình thành một trợ lý, chỉ gõ một câu là nó chạy trọn?

**Mục tiêu khối:** lập một agent nắm xu hướng trong `.claude/agents/`, chạy thử ra bản tin.

### PHẦN 1: LÝ THUYẾT (5 phút)

"Buổi 2 anh chị lập trợ lý viết bài. Buổi 3 lập trợ lý tạo ảnh. Hôm nay lập **trợ lý nắm xu hướng.** Anh chị chỉ nói 'xem tuần này ngành mình có gì', nó tự cào tikhub, tự chạy last30days, tự tổng hợp bản tin, tự gợi ý góc content. Giống một bạn chuyên viên nghiên cứu thị trường ngồi sẵn trong máy, sáng nào cũng đọc thị trường hộ mình."

"Trợ lý này nằm trong `.claude/agents/` của thư mục làm việc, đúng chỗ anh chị đặt agent buổi 2 và 3. Nó đọc `CLAUDE.md` để biết ngành, sản phẩm, giọng, nên gợi ý hợp mình chứ không chung chung. Điểm khác agent trước: agent này được phép gọi tikhub và chạy last30days."

### PHẦN 2: THAO TÁC LẬP AGENT (thực hành, 22 phút)

**Không tự gõ file. Bảo Claude tạo hộ. PROMPT B4-12 (prompt xây dựng agent):**

```
Tạo cho tôi một agent mới, đặt file trong thư mục .claude/agents/ của thư mục
làm việc này. Tên agent: nam-xu-huong.

Việc của agent này, mỗi khi tôi gọi:
1. Đọc CLAUDE.md để biết ngành, sản phẩm, giọng thương hiệu và danh sách từ cấm.
2. Dùng tikhub tìm trên TikTok các video và hashtag đang lên đúng ngành của tôi.
3. Chạy last30days cho chủ đề ngành của tôi để lấy xu hướng đa nền tảng.
4. Tổng hợp thành một bản tin xu hướng đúng 5 chủ đề. Mỗi chủ đề ghi: nóng ở đâu,
   vì sao nóng, và một góc content hợp thương hiệu tôi.
5. Lưu bản tin thành file ban-tin-xu-huong.md, ghi kèm ngày.

Ba quy tắc bắt buộc ghi vào agent:
- Chỉ nói dựa trên dữ liệu tikhub và last30days trả về. Không bịa số. Không có số
  thì ghi "chưa đủ dữ liệu". Phần suy ra gắn nhãn [SUY LUẬN].
- Không tự đăng bài. Chỉ ra bản tin và bản nháp, người duyệt sau.
- Nhắc tôi mỗi lần gọi tikhub đều tốn phí, nên gọi gọn.

Viết xong cho tôi xem nội dung file agent, giải thích ngắn từng phần
để tôi hiểu nó sẽ làm gì.
```

*(Giảng viên: Claude sẽ tạo file `.claude/agents/nam-xu-huong.md` có phần đầu khai báo tên, mô tả, công cụ được dùng, rồi phần hướng dẫn việc. Mở file đó cho lớp xem, chỉ vào từng dòng, để lớp hiểu agent chỉ là một tờ mô tả việc, không phải phép thuật.)*

**Chạy thử agent. PROMPT B4-13 (prompt chạy test agent):**

```
Gọi agent nam-xu-huong: xem tuần này ngành mình đang có xu hướng gì,
làm cho tôi bản tin xu hướng.
```

**Điểm dừng bắt buộc:** "Ai đã thấy agent chạy và ra bản tin thì giơ tay." Đây là điểm dừng dài nhất khối, chờ tới 90 giây. Agent chạy được là sản phẩm chính buổi. Máy nào chưa ra, kiểm: file agent đã nằm trong `.claude/agents/` chưa, tikhub còn nối không.

**Tiêu chí coi là xong khối K4:** mỗi máy có file agent `nam-xu-huong` trong `.claude/agents/`, gọi một câu thì nó ra bản tin xu hướng. Máy chưa nối được công cụ: vẫn tạo được file agent và hiểu nó làm gì, chạy đủ ở nhà sau.

### DỰ PHÒNG K4

- **Agent chạy nhưng bỏ qua tikhub hoặc last30days:** mở file agent, kiểm phần công cụ được phép dùng có hai cái đó chưa. Bảo Claude "sửa agent để nó được dùng tikhub và last30days".
- **Agent ra bản tin nhưng lệch giọng:** nhắc nó đọc kỹ `CLAUDE.md`, thêm câu "bám giọng và từ cấm trong CLAUDE.md" vào agent.
- **Chưa nối được công cụ:** tạo file agent trước, phần chạy để làm ở nhà. Không bỏ bước lập agent, vì đó là thứ mang về.

---

## K5. ROUTINE: CHO TRỢ LÝ TỰ CHẠY THEO LỊCH (15 phút, 10:10 - 10:25)

**Câu hỏi dẫn:** Trợ lý ngon rồi, nhưng vẫn phải mở máy gõ tay mỗi lần. Có cách nào nó tự chạy, sáng thứ Hai để sẵn bản tin cho mình đọc?

**Mục tiêu khối:** hiểu routine là gì, bật thử một routine chạy trợ lý theo lịch, và nhớ ranh giới người duyệt cuối.

### PHẦN 1: LÝ THUYẾT (5 phút)

"**Routine** là hẹn giờ cho trợ lý tự chạy. Ví dụ 7 giờ sáng mỗi thứ Hai, nó tự làm bản tin xu hướng tuần, để sẵn cho anh chị đọc khi mở máy. Giống hẹn báo thức, nhưng cái báo thức này làm việc thay mình."

"Hai điều nói thẳng, ghi vào vở, quan trọng hơn cả cách bật:"
- "**Người duyệt cuối, luôn luôn.** Routine chỉ chạy tới bước ra bản tin và bản nháp content. Nó KHÔNG tự đăng. Anh chị đọc, sửa, rồi mới đăng tay. Đây là nguyên tắc chống bịa số 3 của cả khóa, giờ áp cho tự động hóa: máy chuẩn bị, người quyết định."
- "**Chạy nền có giới hạn.** tikhub và last30days cần thiết lập trên máy anh chị. Routine chạy tự động lúc anh chị không ngồi máy có thể không với tới hết mấy thiết lập đó. Nên bản đầu, để routine làm phần chắc chạy được, ví dụ phần last30days. Phần cào tikhub thì mình kiểm tay. Đừng kỳ vọng nó hoàn hảo ngay lần đầu. Cứ để chạy một tuần rồi xem nó ra gì."

### PHẦN 2: THAO TÁC BẬT ROUTINE (demo và thực hành, 10 phút)

**[KIỂM TRƯỚC BUỔI]** Cách bật routine tùy phiên bản app. Trước buổi tự lập một routine, chạy thử, ghi đúng đường bấm. Nếu bản app của lớp chưa có tính năng này, chuyển khối K5 thành "giới thiệu ý niệm, hướng dẫn bật khi có", và dồn thời gian cho K4.

**Bảo Claude lập routine. PROMPT B4-14 (prompt lập lịch tự chạy):**

```
Tôi muốn agent nam-xu-huong tự chạy mỗi tuần một lần, sáng thứ Hai,
để sẵn bản tin xu hướng cho tôi. Giúp tôi đặt lịch chạy tự động (routine) cho việc đó.
Nhắc rõ trong routine: chỉ ra bản tin và bản nháp, KHÔNG tự đăng bài.
```

**Chạy thử ngay một lần để thấy kết quả. PROMPT B4-15:**

```
Chạy thử routine đó ngay bây giờ một lần, để tôi xem nó ra bản tin thế nào,
đừng chờ tới thứ Hai.
```

**Tiêu chí coi là xong khối K5:** lớp hiểu routine là hẹn lịch cho agent, và thấy một lần chạy thử ra kết quả. Ai app chưa có tính năng: hiểu ý niệm, biết sẽ bật khi có.

### DỰ PHÒNG K5

- **App chưa có routine:** không sao, đây là phần "biết để dùng sau". Nhấn mạnh phần agent ở K4 mới là thứ mang về dùng ngay, gọi tay mỗi tuần cũng được.
- **Routine chạy nhưng thiếu phần tikhub:** đúng như đã cảnh báo. Để nó làm phần last30days, phần tikhub kiểm tay. Không phải lỗi.

---

## K6. CHỐT VÀ GIAO BÀI (5 phút, 10:25 - 10:30)

### LỜI GIẢNG

"Tổng lại buổi nay. Anh chị mang về ba thứ. Một, tikhub đã nối, cào được xu hướng đúng ngành. Hai, một trợ lý nắm xu hướng nằm trong `.claude/agents/`, gọi một câu là ra bản tin. Ba, biết cách cho nó tự chạy theo lịch bằng routine."

"Ba con dao nhắc lại lần cuối. Một, mỗi lượt tikhub tốn phí, gọi gọn. Hai, routine không tự đăng, người duyệt rồi mới đăng. Ba, không bịa số xu hướng, không có thì ghi chưa đủ dữ liệu."

"Bài về nhà:"
1. "Ai chưa cài last30days thì cài theo file hướng dẫn tôi gửi."
2. "Để routine chạy một tuần, sáng thứ Hai mở máy xem nó để sẵn bản tin gì."
3. "Chọn một chủ đề nóng nhất trong bản tin, ra một bài đăng thật, đăng lên trang của anh chị."

"Buổi sau ta quay lại chính khách hàng của mình: đọc review, tin nhắn, bình luận để tìm nỗi đau thật, rồi nối nỗi đau đó với xu hướng hôm nay để ra nội dung vừa trúng người vừa hợp trào lưu. Hẹn anh chị buổi tới."

### ĐÓNG GÓI NỘP

Nói học viên gom vào thư mục làm việc để nộp:
- `xu-huong-tikhub.md`
- `ban-tin-xu-huong.md`
- File agent `.claude/agents/nam-xu-huong.md`
- Một bài đăng bám xu hướng (nếu đã làm ở K3)

---

## PHỤ LỤC A: DANH SÁCH LỆNH TIKHUB HAY DÙNG TRONG BUỔI (cho giảng viên)

Học viên không cần gõ tên lệnh, chỉ nói tiếng Việt, Claude tự chọn. Bảng này để giảng viên hiểu Claude đang gọi gì, và gỡ khi cần.

| Muốn gì | Nhóm lệnh tikhub Claude thường gọi |
|---|---|
| Từ khóa tìm kiếm đang lên trên TikTok | trending searchwords |
| Hashtag đang lên trên TikTok | trends hashtag list / detail |
| Tìm video theo từ khóa ngành | general search result |
| Video dưới một hashtag | hashtag video list |
| Bình luận dưới một video | video comments |
| Bài đăng của một đối thủ | user post videos |
| Hashtag và bài trên Instagram | search hashtags / hashtag posts |

---

## PHỤ LỤC B: BỐN LỖI HAY GẶP VÀ CÁCH GỠ NHANH (cho giảng viên)

| Lỗi | Dấu hiệu | Gỡ |
|---|---|---|
| tikhub chưa nối | Claude nói không thấy tikhub | Kiểm lại khóa API đã dán đúng chưa, bật lại app |
| tikhub hết lượt | Báo lỗi phí hoặc quota | Tài khoản chưa nạp đủ, dùng file mẫu, nạp sau |
| last30days đòi Python | Báo cần Python 3.12+ | Không cài giữa buổi, cài ở nhà, dùng file mẫu |
| Cào ra lệch ngành | Bản tin toàn chuyện lạ | Từ khóa quá rộng, khóa hẹp lại theo CLAUDE.md |

---

## PHỤ LỤC C: TÓM TẮT PROMPT CẢ BUỔI (bảng tra nhanh)

| Mã | Dùng để |
|---|---|
| B4-0 | Kiểm mở đúng thư mục và có CLAUDE.md |
| B4-1 | Kiểm tikhub đã nối chưa |
| B4-2 | Cào thử xu hướng chung (nhẹ) |
| B4-3 | Cào xu hướng đúng ngành, lưu file |
| B4-4 | Xem đối thủ đang làm gì |
| B4-5 | Kiểm máy có Python 3.12 chưa |
| B4-6 | Cài last30days |
| B4-7 | Chạy kiểm tra sức khỏe last30days |
| B4-8 | Chạy last30days một chủ đề |
| B4-9 | Chế độ tìm xu hướng của last30days |
| B4-10 | Ghép hai nguồn ra bản tin xu hướng |
| B4-11 | Ra 2 bài từ bản tin |
| B4-12 | Lập agent nắm xu hướng |
| B4-13 | Chạy thử agent |
| B4-14 | Lập routine tự chạy |
| B4-15 | Chạy thử routine ngay |

---

CES Global · Creative · Effective · Sustainable
