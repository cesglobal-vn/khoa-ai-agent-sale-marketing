# Nội dung slide Buổi 04: Content Engine Agent

**Khóa:** AI Agent cho Sale & Marketing
**Hình thức:** online live qua Zoom hoặc Meet
**Thời lượng buổi:** 150 phút
**Tổng số slide:** 36 slide, trong đó 20 slide nội dung và bảng, 11 slide prompt, 3 slide đề bài và mốc thời gian, 1 slide bìa, 1 slide giải lao
**Giáo án nguồn:** `giao-an/buoi-04-content-engine-agent.md`
**Kịch bản demo nguồn:** `so-tay-giang-vien/buoi-04-content-engine-agent.md`
**Ma trận mục tiêu:** `00-tong-quan/ma-tran-muc-tieu.md` mục tiêu 4.1 tới 4.5

## Ghi chú thiết kế chung

- Nền trắng, chữ đậm, cỡ chữ tối thiểu 28pt vì lớp học qua màn hình chia sẻ
- Slide prompt để chữ cỡ lớn trong khối code, học viên nhìn màn hình chia sẻ gõ theo được
- Mỗi slide một thông điệp, tối đa 6 dòng
- Phần "Lời giảng viên nói khi chiếu slide này" KHÔNG in lên slide
- Màu, logo, font do bước đóng gói áp vào, không ghi ở đây

---

### Slide 1: Buổi 4. Content Engine Agent

**Loại:** tiêu đề

**Nội dung hiển thị:**
- AI Agent cho Sale & Marketing
- Buổi 4 trên 6
- Từ một insight ra nguyên chiến dịch 14 ngày
- 150 phút

**Lời giảng viên nói khi chiếu slide này:** "Chào anh chị. Buổi này chấm dứt cảnh mỗi sáng ngồi nghĩ hôm nay đăng gì. Chúng ta lấy đúng một insight của buổi 2 và bẻ nó thành 14 ngày nội dung: bài viết, email, video, carousel. Hôm nay không ai gõ tay 30 mẩu nội dung, chúng ta dựng một cái máy."

**Hình minh họa gợi ý:** Một ô nhỏ bên trái nhãn "1 insight", mũi tên tỏa ra 14 ô nhỏ bên phải.

**Thời điểm:** Khối 1 Framework, phút 0

---

### Slide 2: Hết buổi hôm nay anh chị làm được gì

**Loại:** nội dung

**Nội dung hiển thị:**
- Dựng skill Content Engine nhận 1 insight, trả ra lịch 14 ngày
- Xếp nhịp đủ 4 loại ngày: giáo dục, bằng chứng, xử lý phản đối, ưu đãi
- Khai ràng buộc pháp lý trước khi agent viết chữ đầu tiên
- Nối từng bài về một bước trong hành trình mua
- Cắt một bài xuống đúng giới hạn kênh mà vẫn giữ đủ ba phần

**Lời giảng viên nói khi chiếu slide này:** "Dòng thứ ba là dòng khác biệt của buổi hôm nay. Nhiều lớp dạy viết bài rồi ngồi sửa sau. Chúng ta làm ngược: khai ràng buộc trước, agent tự chặn. Cuối buổi tôi sẽ yêu cầu anh chị nhờ agent viết một câu chứa từ cấm của ngành mình. Đạt là khi agent từ chối hoặc thay từ và nói rõ lý do, chứ không phải khi anh chị ngồi sửa tay sau."

**Hình minh họa gợi ý:** 5 ô vuông trống để tích, ô thứ ba đóng khung đậm.

**Thời điểm:** Khối 1, phút 1

---

### Slide 3: Anh chị mang theo gì từ ba buổi trước

**Loại:** bảng

**Nội dung hiển thị:**

| Cần có | Từ buổi nào | Không có thì sao |
|---|---|---|
| `CLAUDE.md` có giọng văn, từ cấm | Buổi 1 | Chép bản Thảo An |
| Skill `viet-bai-ban-hang` chạy được | Buổi 1 | Chép bản mẫu |
| `insight-khach-hang.md` có trích dẫn | Buổi 2 | Dùng bộ insight Thảo An |
| Danh sách kênh và vai trò từng kênh | Tự khai | Dùng bộ kênh Thảo An |
| Ràng buộc ngành mình: từ cấm, cam kết cấm | Tự khai | Dùng mục "Điều KHÔNG được nói" |

**Lời giảng viên nói khi chiếu slide này:** "Dòng cuối là dòng quyết định buổi hôm nay có dùng được vào việc thật hay không. Ai làm ngành có quy định chặt như dược, thực phẩm chức năng, tài chính, giáo dục, y tế, mà không mang danh sách từ cấm của ngành mình thì buổi nay chỉ là bài tập. Ai chưa có thì lát nữa vào phần làm sản phẩm, anh chị ngồi viết ra, mất 10 phút."

**Hình minh họa gợi ý:** 5 biểu tượng file rơi vào một thư mục chung.

**Thời điểm:** Khối 1, phút 2

---

### Slide 4: Hai skill, hai việc, không chồng nhau

**Loại:** bảng

**Nội dung hiển thị:**

| | Content Engine | `viet-bai-ban-hang` |
|---|---|---|
| Lo phần | Chiến dịch | Viết từng bài |
| Cụ thể là | Lịch 14 ngày, góc nội dung, phân bổ kênh, nhịp 4 loại ngày | Hook, thân bài, lời kêu gọi, soát từ cấm |

Tới bước viết caption, Content Engine gọi lại `viet-bai-ban-hang`.

**Lời giảng viên nói khi chiếu slide này:** "Đây là điểm nhiều người hiểu nhầm. Content Engine không viết lại phần viết bài từ đầu. Nó gọi lại skill anh chị dựng ở buổi 1. Nhờ vậy giọng văn và danh sách từ cấm buổi 1 vẫn có hiệu lực trong 30 mẩu nội dung hôm nay. Cả hai skill đọc chung một CLAUDE.md, nên không sợ ra hai giọng khác nhau."

**Hình minh họa gợi ý:** Ô Content Engine ở trên, mũi tên đi xuống ô viet-bai-ban-hang, cả hai cùng nối vào ô CLAUDE.md ở dưới.

**Thời điểm:** Khối 1, phút 3

---

### Slide 5: Nhịp buổi hôm nay

**Loại:** bảng

**Nội dung hiển thị:**

| Khối | Phút | Việc |
|---|---|---|
| 1 | 20 | Framework, chỉ nghe |
| 2 | 35 | Demo làm theo, anh chị gõ cùng tôi |
| 3a | 30 | Anh chị làm, chặng 1 |
| Nghỉ | 10 | Giải lao |
| 3b | 25 | Anh chị làm, chặng 2 |
| 4 | 10 | Review, 3 người chia sẻ màn hình |
| 5 | 20 | Hoàn thiện và nộp |

**Lời giảng viên nói khi chiếu slide này:** "Khối 2 anh chị gõ cùng tôi, và gõ trên insight của chính anh chị chứ không phải của Thảo An. Tôi báo trước mức đạt tối thiểu nếu không kịp: lịch 7 ngày thay vì 14, đủ 4 loại ngày là đạt; 5 bài social tại lớp, 5 bài còn lại về nhà."

**Hình minh họa gợi ý:** Thanh ngang chia 7 đoạn theo tỉ lệ thời lượng.

**Thời điểm:** Khối 1, phút 4

---

### Slide 6: Chiến dịch khác chuỗi bài lẻ ở chỗ nào

**Loại:** bảng

**Nội dung hiển thị:**

| Chuỗi bài lẻ | Chiến dịch |
|---|---|
| Mỗi bài tự đứng một mình | Một insight duy nhất chạy suốt |
| Bài nào cũng cố nói hết mọi thứ | Mỗi bài có đúng một việc phải làm |
| Bài nào cũng na ná bài nào | Có thứ tự, đảo là hỏng |
| Không đo được bài nào ra đơn | Mỗi bài đo bằng một chỉ số riêng |

**Lời giảng viên nói khi chiếu slide này:** "Tôi hỏi trước: tháng vừa rồi anh chị đăng bao nhiêu bài, và có bài nào nối vào bài nào không? Anh chị gõ vào chat. Phần lớn sẽ trả lời là không, và đó là chuỗi bài lẻ. Còn chiến dịch thì bài ngày 1 làm khách biết, ngày 5 làm khách tin, ngày 9 gỡ nút thắt, ngày 14 mới xin đơn. Bài giáo dục thì không chốt đơn. Bài ưu đãi thì không giảng giải dài."

**Hình minh họa gợi ý:** Bên trái 4 ô rời rạc không nối. Bên phải 4 ô nối bằng một trục ngang xuyên qua.

**Thời điểm:** Khối 1, phút 4 tới 7

---

### Slide 7: Insight xương sống của Thảo An

**Loại:** nội dung

**Nội dung hiển thị:**
> Khách sợ bị kích ứng khi đổi sang sản phẩm chăm da mới.

Bằng chứng `[DATA THẬT]`:
- R11: "Trước mình dùng loại khác bị nổi mẩn, đổi qua đây thì ổn."
- M01: "Da mình nhạy cảm lắm, dùng cái này có bị rát không shop?"
- M02: "Sản phẩm này có cồn không ạ? Mình dị ứng cồn."
- M06: "Đang dùng của hãng khác, đổi qua có sao không?"

**Lời giảng viên nói khi chiếu slide này:** "Bốn dòng bằng chứng này lấy nguyên từ bảng insight buổi 2, không phải tôi đoán. Một nỗi sợ đó nuôi được 14 ngày, vì nó có nhiều mặt: sợ thành phần, sợ mất tiền vô ích, sợ bị hứa hão, sợ chọn sai loại cho da mình. Anh chị mở bảng insight của mình ra, chọn đúng một pain có tần suất cao nhất, đó là xương sống của chiến dịch anh chị. Chỉ một, không phải năm."

**Hình minh họa gợi ý:** Một trục dọc lớn ở giữa nhãn "nỗi sợ kích ứng", 4 nhánh tỏa ngang ghi 4 mặt của nỗi sợ.

**Thời điểm:** Khối 1, phút 7 tới 9

---

### Slide 8: Bốn loại ngày, mỗi loại một việc

**Loại:** bảng

**Nội dung hiển thị:**

| Loại ngày | Làm gì cho khách | Đo bằng gì |
|---|---|---|
| Giáo dục | Dạy khách một thứ họ chưa biết | Lưu bài, bình luận từ khóa |
| Bằng chứng | Chứng minh bằng review thật, giấy tờ thật | Click sang Shopee, xem hết video |
| Xử lý phản đối | Gỡ đúng nút đang chặn khách bấm mua | Số inbox, chất lượng câu hỏi |
| Ưu đãi | Cho lý do mua hôm nay chứ không phải tuần sau | Đơn có mã, doanh thu |

**Lời giảng viên nói khi chiếu slide này:** "Lịch nội dung không phải là danh sách 14 tiêu đề. Nó là một nhịp. Anh chị nhìn cột đo bằng gì: mỗi loại ngày đo bằng một chỉ số khác nhau. Nếu 10 bài của anh chị đều xin inbox ngay thì anh chị đang nói chuyện với đúng một nhóm khách và bỏ chín nhóm còn lại. Dòng chảy là biết rồi tin rồi hỏi rồi mua. Bài nào không nằm được vào một trong bốn ô này là bài thừa, xóa."

**Hình minh họa gợi ý:** Bảng chiếm phần lớn slide. Dưới bảng vẽ mũi tên ngang 4 chặng: biết, tin, hỏi, mua.

**Thời điểm:** Khối 1, phút 9 tới 12

---

### Slide 9: Tỉ lệ 5 giáo dục, 4 bằng chứng, 3 phản đối, 2 ưu đãi

**Loại:** nội dung

**Nội dung hiển thị:**
- Ưu đãi chỉ 2 vì khách hỏi 4 tới 6 lượt inbox mới chốt
- Người còn đang sợ kích ứng thì giảm giá không giải quyết được gì
- Ưu đãi nằm ở ngày 7 và ngày 14, không sớm hơn
- Ngày 7 bắt nhóm đã tin sớm, ngày 14 chốt nhóm chần chừ
- Đặt ưu đãi ngày 2 là đốt tiền vào người chưa tin

**Lời giảng viên nói khi chiếu slide này:** "Đây là phần dạy nghề. Ba chữ phải tin trước rồi mới mua giải thích toàn bộ tỉ lệ này. Lát nữa trong demo, nếu agent xếp ưu đãi vào ngày 3, tôi sẽ chỉ vào đó và hỏi anh chị: ngày 3 khách đã tin chưa? Chưa tin thì giảm giá để làm gì?"

**Hình minh họa gợi ý:** Thanh ngang 14 ô, ô số 7 và 14 tô đậm, các ô còn lại tô 3 mức nhạt theo 3 loại ngày.

**Thời điểm:** Khối 1, phút 12 tới 14

---

### Slide 10: Giữ lõi, đổi cách kể

**Loại:** bảng

**Nội dung hiển thị:**

Lõi gồm 3 thứ không đổi: 1 nỗi đau + 1 điểm mạnh + 1 lời kêu gọi

| Định dạng | Cách kể cùng một lõi |
|---|---|
| Bài chữ dài Facebook | Kể chuyện một khách đổi sản phẩm rồi nổi mẩn |
| Carousel 7 slide | Mỗi slide một dòng thành phần |
| Video 30 giây | Quay tay thoa lên cổ tay, nói to 3 thành phần |
| Email | Giải thích vì sao cồn làm da rát |
| Khối landing page | Bảng thành phần đặt cạnh nút mua |

**Lời giảng viên nói khi chiếu slide này:** "Sai lầm hay gặp: copy nguyên caption Facebook rồi dán sang email, đổi tiêu đề. Ra một bản nhạt cả hai bên. Cách đúng là giữ lõi, đổi cách kể theo nơi khách đang đứng. Người vào landing là người sắp quyết định, đừng kể chuyện với họ. Quy tắc chống lặp: một lõi tối đa 3 định dạng, và không đăng 2 định dạng của cùng lõi trong 3 ngày liên tiếp. 14 ngày cần khoảng 5 lõi khác nhau, không phải 14 lõi và cũng không phải 1."

**Hình minh họa gợi ý:** Một viên lõi ở giữa, 5 khung khác hình dạng bao quanh, mỗi khung một định dạng.

**Thời điểm:** Khối 1, phút 14 tới 17

---

### Slide 11: Giới hạn caption từng kênh

**Loại:** bảng

**Nội dung hiển thị:**

| Nền tảng | Ký tự | Ảnh | Video |
|---|---|---|---|
| Facebook | 63.206 | 10 | 1 |
| TikTok | 2.200 | 35 | 1 |
| Instagram | 2.200 | 10 | 1 |
| LinkedIn | 3.000 | 20 | 1 |
| Twitter | 280 | 4 | 1 |
| Threads | 500 | 10 | 1 |

**Lời giảng viên nói khi chiếu slide này:** "Viết nội dung đa kênh mà không biết giới hạn từng kênh thì bài ra xong phải ngồi cắt lại bằng tay, và cắt tay lúc gần giờ đăng là lúc dễ cắt mất đúng câu quan trọng nhất. Anh chị so hai dòng: Facebook cho 63 nghìn ký tự nên kể được cả câu chuyện, Twitter cho 280 ký tự nên chỉ chở được đúng một câu. Đó không phải cắt ngắn, đó là viết lại. Bảng này lấy từ công cụ aitoearn. Nền tảng đổi chính sách thì gọi lại đúng công cụ đó lấy số mới, đừng tin bảng in sẵn quá sáu tháng. Hôm nay chỉ tra giới hạn, chưa đăng bài. Đăng thật lên kênh thật là việc của buổi 5."

**Hình minh họa gợi ý:** Các thanh ngang dài ngắn theo tỉ lệ ký tự, thanh Twitter ngắn tí xíu cạnh thanh Facebook rất dài.

**Thời điểm:** Khối 1, phút 15 tới 17

---

### Slide 12: Vì sao khai ràng buộc trước, không sửa sau

**Loại:** nội dung

**Nội dung hiển thị:**
- 14 ngày, 10 bài, 3 email, 3 video, 1 carousel, 1 khối landing: khoảng 30 mẩu chữ
- **Rẻ hơn**: khai trước tốn 10 dòng, sửa sau tốn 30 lượt đọc dò
- **Sót ít hơn**: người đọc dò tới mẩu thứ 20 là bắt đầu lướt, agent thì không mệt
- **Đổi được cả loạt**: luật ngành đổi thì sửa 1 dòng trong skill rồi chạy lại

**Lời giảng viên nói khi chiếu slide này:** "Đây là phần chống rủi ro của buổi hôm nay, tôi nói chậm. Bắt sót một câu là một câu chạy quảng cáo sai. Và tôi hỏi anh chị một câu: nếu chỗ này là 30 mẩu nội dung chứ không phải 3 câu, ai ngồi dò?"

**Hình minh họa gợi ý:** Bên trái 10 dòng nhỏ nhãn "khai trước". Bên phải 30 khối chữ nhãn "đọc dò sau". Kích thước chênh lệch rõ.

**Thời điểm:** Khối 1, phút 17 tới 20

---

### Slide 13: Bẫy tinh vi: persona không phải người thật

**Loại:** nội dung

**Nội dung hiển thị:**
- "Chị Ngọc, 30 tuổi, nhân viên văn phòng" là chân dung suy ra từ dữ liệu
- Gắn tên Chị Ngọc vào một lời chứng thực là đang bịa review
- Muốn trích lời khách thì trích nguyên văn R01 tới R15 hoặc M01 tới M15
- Ba nguyên tắc chống bịa vẫn giữ nguyên từ buổi 1

**Lời giảng viên nói khi chiếu slide này:** "Đây là cái bẫy tinh vi nhất của buổi hôm nay và nó rất hay xảy ra. Agent viết một bài chứng thực rất cảm động, có tên, có tuổi, có nghề, đọc lên như thật. Nhưng người đó không tồn tại. Bịa review là chuyện khác hẳn với viết dở, nó là chuyện pháp lý. Lát nữa trong khối ràng buộc, tôi sẽ cho anh chị thấy một dòng viết riêng để chặn đúng lỗi này. Còn ba nguyên tắc chống bịa thì anh chị thuộc rồi: chỉ nêu công dụng có trong hồ sơ; gắn nhãn nguồn; người duyệt cuối."

**Hình minh họa gợi ý:** Một thẻ persona có dấu X đè lên, bên cạnh là mã R11 có dấu tích.

**Thời điểm:** Khối 1, phút 18 tới 20

---

### Slide 14: 35 phút tới anh chị gõ cùng tôi

**Loại:** chuyển khối

**Nội dung hiển thị:**
- Mở thư mục làm việc, mở sẵn `insight-khach-hang.md` của buổi 2
- Gõ trên insight của chính anh chị, không phải của Thảo An
- Bốn điểm dừng, tôi chờ hai phần ba lớp
- Chưa ra kết quả thì gõ CHỜ vào chat

**Lời giảng viên nói khi chiếu slide này:** "Ba mươi lăm phút tới tôi gõ gì thì anh chị gõ y hệt. Điểm khác so với hai buổi trước: hôm nay anh chị chạy trên insight của chính mình ngay từ đầu, vì lịch 14 ngày phải là lịch của thương hiệu anh chị thì mới mang về dùng được. Ai chưa có insight riêng thì mở bộ Thảo An, vẫn nộp đủ 9 hạng mục."

**Hình minh họa gợi ý:** Biểu tượng bàn phím lớn, 4 chấm tròn đánh dấu 4 điểm dừng trên thanh ngang.

**Thời điểm:** Khối 2, phút 20

---

### Slide 15: PROMPT. Tạo skill Content Engine, rồi gọi bằng câu tự nhiên

**Loại:** prompt

**Nội dung hiển thị:**

```
Tạo file .claude/skills/content-engine/SKILL.md trong thư mục làm việc
này, tạo luôn thư mục cha nếu chưa có. Nội dung như sau: [dán khối
trong demo/buoi-04/skill-content-engine.md]
```

Rồi mở phiên mới, gõ đúng một câu, KHÔNG nhắc tên skill:

```
Dựng cho tôi chiến dịch nội dung 14 ngày cho serum rau má B5.
```

**Lời giảng viên nói khi chiếu slide này:** "Claude xin phép ghi file thì anh chị bấm Yes. Mở file ra và nhìn hai chỗ: dòng description ở frontmatter trên cùng, và khối ràng buộc nằm ngay đầu phần nội dung chứ không phải cuối. Lý do đơn giản: thứ đặt cuối file hay bị agent lướt qua khi output dài. Trước khi máy chạy, phải lắp phanh. Kết quả đúng là Claude báo đang dùng skill content-engine rồi hỏi lại anh chị cần cấp gì. Nếu nó không gọi skill thì lỗi ở dòng description, sửa cho giống câu anh chị thật sự gõ. Nếu nó nhảy vào viết bài luôn thì nội dung skill sai, sửa lại phần quy trình làm việc."

**Hình minh họa gợi ý:** Khối code trên, khối code dưới nhỏ hơn. Bên phải là file SKILL.md có phần đầu tô đậm nhãn "ràng buộc".

**Thời điểm:** Khối 2, phút 20 tới 23

---

### Slide 16: PROMPT. Tra xu hướng rồi lưu ngay thành file

**Loại:** prompt

**Nội dung hiển thị:**

Ba công cụ tikhub: `tiktok_app_v3_fetch_hashtag_detail`, `tiktok_app_v3_fetch_hashtag_video_list`, `tiktok_ads_search_ads`

```
Lưu kết quả vừa lấy được thành file xu-huong-hashtag.md trong thư mục
làm việc.
Ghi rõ ngày lấy, hashtag nào, và 5 góc nội dung đang bị lặp nhiều nhất.
Chỉ lấy nội dung công khai, không ghi lại tên hay thông tin cá nhân
của ai.
```

**Lời giảng viên nói khi chiếu slide này:** "Mỗi lượt gọi này tính tiền vào tài khoản của người gọi, dịch vụ trả về nguyên chữ là yêu cầu này sẽ tính phí. Nên gọi một lần rồi lưu ngay kết quả thành file, lần sau đọc lại file. Và nói rõ mục đích: mình tra để biết góc nào đã bão hòa mà tránh, không phải để bắt chước. Insight xương sống vẫn lấy từ dữ liệu khách của mình, không lấy từ bảng xu hướng. Ai không có tài khoản tikhub thì bỏ hẳn hai phút này, đi thẳng vào bước sau, không mất hạng mục nộp nào."

**Hình minh họa gợi ý:** Khối code lớn. Góc trên có biểu tượng đồng tiền và dòng chữ nhỏ "mỗi lượt gọi tính phí".

**Thời điểm:** Khối 2, phút 23 tới 25

---

### Slide 17: PROMPT. Campaign brief, phần 1 nạp insight

**Loại:** prompt

**Nội dung hiển thị:**

```
Insight xương sống cho chiến dịch 14 ngày này:

"Khách sợ bị kích ứng khi đổi sang sản phẩm chăm da mới. Nỗi sợ này
mạnh hơn mong muốn cải thiện da, nên nó chặn ở bước quyết định mua,
không phải bước biết đến sản phẩm."

Bằng chứng [DATA THẬT]:
- R11: "Trước mình dùng loại khác bị nổi mẩn, đổi qua đây thì ổn."
- M01: "Da mình nhạy cảm lắm, dùng cái này có bị rát không shop?"
- M02: "Sản phẩm này có cồn không ạ? Mình dị ứng cồn."
- M06: "Đang dùng của hãng khác, đổi qua có sao không?"
- R04: "Đọc thành phần thấy toàn cái đọc được, không có chất gì lạ."

Bối cảnh:
- Persona chính: nữ 28-34, da nhạy cảm dễ đỏ rát, từng bị kích ứng nên
  sợ thử đồ mới. Lướt Facebook buổi tối, hỏi kỹ qua inbox trước khi mua.
- Kênh: Facebook đầu phễu tới chốt; Shopee cuối phễu; Website nền tin
  cậy, gắn UTM để đo nguồn.
- Mục tiêu: 30 đơn trong 30 ngày, 100% đơn gắn được nguồn kênh. Chiến
  dịch 14 ngày này nằm ở tuần 2 và tuần 3, chỉ tiêu 15 đơn.
```

**Lời giảng viên nói khi chiếu slide này:** "Anh chị thay phần này bằng insight và bối cảnh của chính mình. Prompt gồm hai slide, copy cả hai phần rồi dán một lần. Anh chị chú ý: chỉ một insight, không phải năm. Nhiều người nạp cả bảng insight vào và kết quả là 14 ngày không có xương sống."

**Hình minh họa gợi ý:** Khối code chiếm trọn slide. Góc dưới ghi "còn tiếp".

**Thời điểm:** Khối 2, phút 25 tới 27

---

### Slide 18: PROMPT. Campaign brief, phần 2 tám mục

**Loại:** prompt

**Nội dung hiển thị:**

```
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

**Lời giảng viên nói khi chiếu slide này:** "Mục 5 là chỗ ăn tiền của cả buổi. Năm lõi này quyết định 14 ngày có nhàm hay không. Agent trả về năm lõi mà đọc lên thấy giông giống nhau thì đừng viết tiếp, quay lại sửa lõi. Sửa 5 dòng ở đây rẻ hơn sửa 30 mẩu ở dưới. Còn mục 7: nếu agent ghi tăng nhận diện thương hiệu thì anh chị bắt sửa ngay, chỉ số phải đếm được, ví dụ số bình luận từ khóa, số inbox mới, số click có UTM, số đơn có mã."

**Hình minh họa gợi ý:** Khối code lớn. Mục 5 và mục 7 tô nền nhạt cho nổi.

**Thời điểm:** Khối 2, phút 27 tới 29

---

### Slide 19: PROMPT. Lịch 14 ngày, 8 cột

**Loại:** prompt

**Nội dung hiển thị:**

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

**Lời giảng viên nói khi chiếu slide này:** "Đây là điểm dừng dài nhất, tôi chờ tới 90 giây. Lịch là xương sống cả buổi và là đầu vào của buổi 5. Ai chưa ra đủ lịch thì gõ CHỜ vào chat. Anh chị để ý dòng cuối: tôi bắt agent tự đếm lại. Bắt nó đếm là để mình khỏi phải đếm."

**Hình minh họa gợi ý:** Khối code chiếm trọn slide.

**Thời điểm:** Khối 2, phút 29 tới 36

---

### Slide 20: Lịch 14 ngày, đọc cột "Loại ngày" trước

**Loại:** bảng

**Nội dung hiển thị:**

| Ngày | Định dạng | Loại ngày | Lời kêu gọi |
|---|---|---|---|
| 1 | Bài chữ dài | Giáo dục | Bình luận "THANHPHAN" |
| 3 | Ảnh review | Bằng chứng | Bấm link Shopee gắn UTM |
| 6 | Bài hỏi đáp | Xử lý phản đối | Inbox mô tả tình trạng da |
| 7 | Ảnh combo | Ưu đãi | Dùng mã FB07 trên Shopee |
| 10 | Video 45 giây | Bằng chứng | Bấm link Shopee gắn UTM |
| 14 | Ảnh + Email 3 | Ưu đãi | Chốt đơn Shopee mã FB14 |

Đếm cuối bảng: giáo dục 5, bằng chứng 4, phản đối 3, ưu đãi 2

**Lời giảng viên nói khi chiếu slide này:** "Nhìn cột Loại ngày. Đây là cột giữ cho lịch không thành 14 bài bán hàng liên tiếp. Và nhìn ngày 10: agent để nguyên cả review 3 sao, không cắt đi. Đó là cố ý. Khách của mình hỏi kỹ 4 tới 6 lượt mới mua, họ nhận ra ngay khi thấy toàn 5 sao. Anh chị tự đếm trên máy mình: có đủ 4 loại không, có 3 ngày liền cùng loại không, ưu đãi có bị đẩy lên đầu không."

**Hình minh họa gợi ý:** Bảng chiếm trọn slide, cột Loại ngày tô 4 mức đậm nhạt khác nhau.

**Thời điểm:** Khối 2, phút 34 tới 36

---

### Slide 21: PROMPT. Hai bài social khác loại ngày

**Loại:** prompt

**Nội dung hiển thị:**

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

**Lời giảng viên nói khi chiếu slide này:** "Anh chị nhìn dòng Claude báo nó đang gọi skill viet-bai-ban-hang. Giọng văn trong hai bài này không phải từ skill hôm nay, nó từ skill anh chị dựng buổi 1. Hôm nay mình dựng cái xếp lịch, không dựng lại cái viết bài."

**Hình minh họa gợi ý:** Khối code lớn. Bên phải là hai khung bài A và B đặt cạnh nhau.

**Thời điểm:** Khối 2, phút 36 tới 41

---

### Slide 22: Hai bài khác nhau ở bốn chỗ

**Loại:** bảng

**Nội dung hiển thị:**

| | Bài A ngày 1 | Bài B ngày 6 |
|---|---|---|
| Mở đầu | Bằng một cảnh | Bằng câu khách hỏi |
| Độ dài | Dài, có danh sách để lưu | Ngắn, đọc một hơi |
| Lời kêu gọi | Xin bình luận từ khóa | Xin inbox mô tả da |
| Bước trong hành trình | Biết | Hỏi |

**Lời giảng viên nói khi chiếu slide này:** "Cùng một chiến dịch, cùng một nỗi sợ, nhưng khác nhau bốn chỗ. Bài A ở bước biết, bài B ở bước hỏi, tức là hai nhóm khách đứng ở hai chỗ khác nhau trên đường tới đơn hàng. Nếu 10 bài của anh chị đều xin inbox ngay, anh chị đang nói chuyện với đúng một nhóm và bỏ chín nhóm còn lại. Và một chi tiết nghề trong bài B: nó để nguyên cả hai review, một chị nói ba tuần thấy mờ thâm, một chị nói một tuần chưa thấy gì. Không cắt review kém đi."

**Hình minh họa gợi ý:** Hai cột bài đặt cạnh nhau, 4 dòng khác biệt nối bằng đường kẻ ngang.

**Thời điểm:** Khối 2, phút 39 tới 41

---

### Slide 23: PROMPT. Cắt bài xuống 280 ký tự

**Loại:** prompt

**Nội dung hiển thị:**

```
Lấy bài A vừa rồi, viết lại cho Twitter. Giới hạn 280 ký tự.
Giữ đúng 1 pain + 1 USP + 1 lời kêu gọi. Không cắt cụt giữa câu,
viết lại thành câu khác. Cuối bài ghi số ký tự thực tế.
```

**Lời giảng viên nói khi chiếu slide này:** "Facebook cho 63 nghìn ký tự, Twitter cho 280, chênh nhau hơn hai trăm lần. Anh chị nhìn hai bài cạnh nhau: không phải bài Twitter bị cắt ngắn, nó được viết lại. Ba thành phần vẫn còn, lời kêu gọi vẫn còn, chỉ mất phần kể chuyện. Cái mất phải là chuyện kể, không phải bằng chứng. Điểm dừng: bài đã cắt trên máy anh chị còn đủ ba phần không, một nỗi đau, một điểm khác biệt, một lời kêu gọi? Mất một phần là chưa đạt, anh chị làm lại ngay tại chỗ. Còn dòng đếm ký tự cuối bài: nó ghi 258 trên 280 thì mình biết bài dán được luôn, không phải mở app ra thử."

**Hình minh họa gợi ý:** Khối code nhỏ. Bên dưới hai khối chữ, một dài một ngắn, đều có 3 chấm màu đánh dấu pain, USP, lời kêu gọi.

**Thời điểm:** Khối 2, phút 41 tới 43

---

### Slide 24: PROMPT bẫy. Chạy trong thư mục chưa khai ràng buộc

**Loại:** prompt

**Nội dung hiển thị:**

```
Viết 3 câu mở đầu thật giật cho bài Facebook bán serum rau má B5,
sản phẩm cho da nhạy cảm, có công dụng hỗ trợ giảm thâm sau mụn.
Viết sao cho người lướt phải dừng lại.
```

Agent thường trả về:
- "Giúp bạn hết thâm chỉ sau 7 ngày!"
- "Đặc trị thâm mụn cho da nhạy cảm, cam kết hiệu quả."
- "Tạm biệt thâm mụn, da trắng sáng bật tông sau 2 tuần."

**Lời giảng viên nói khi chiếu slide này:** "Tôi mở một phiên mới ở thư mục khác, thư mục trống không có CLAUDE.md và không có skill nào, để mô phỏng trạng thái chưa khai báo ràng buộc. Câu một: cam kết thời gian, sai. Câu hai: đặc trị và cam kết hiệu quả, sai hai lỗi. Câu ba: sai cả từ lẫn mốc thời gian. Agent không cố tình làm bậy, nó viết đúng thứ mình yêu cầu là câu giật, mà câu giật trong ngành mỹ phẩm trên mạng mặc định trông như thế này. Lỗi nằm ở chỗ mình chưa nói nó không được viết gì."

**Hình minh họa gợi ý:** Khối code trên. Ba câu dưới, mỗi câu có dấu X đỏ và ghi chú lỗi bên cạnh.

**Thời điểm:** Khối 2, phút 43 tới 46

---

### Slide 25: Khối ràng buộc, đặt ở ĐẦU file skill

**Loại:** prompt

**Nội dung hiển thị:**

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

**Lời giảng viên nói khi chiếu slide này:** "Anh chị thay danh sách từ cấm này bằng danh sách của ngành mình. Giờ tôi chạy lại đúng prompt bẫy lúc nãy trong thư mục có khối ràng buộc này. Kết quả trả về sẽ là những câu kiểu: đổi mỹ phẩm mới mà sợ mặt lại đỏ rát, đọc bảng thành phần trước đã. Vẫn giật, vẫn dừng tay người lướt, nhưng không câu nào đưa mình ra tòa hay bị Facebook chặn quảng cáo. Và chú ý: mình không sửa câu nào cả, mình sửa cái máy. Điểm dừng: trên máy anh chị, agent nó từ chối và nói rõ lý do, hay nó viết luôn rồi anh chị phải ngồi sửa tay? Ai phải sửa tay thì đó là dấu hiệu ràng buộc khai chưa đủ, anh chị sửa phần khai báo chứ không sửa bài."

**Hình minh họa gợi ý:** Khối code chiếm trọn slide. Bên trái là cột file SKILL.md với phần đầu tô đậm và mũi tên chỉ vào.

**Thời điểm:** Khối 2, phút 46 tới 49

---

### Slide 26: PROMPT. Bắt agent tự rà

**Loại:** prompt

**Nội dung hiển thị:**

```
Rà lại toàn bộ nội dung đã viết trong chat này. Liệt kê dạng bảng:
câu vi phạm | vi phạm điều nào | câu thay thế.
Không có vi phạm thì ghi "không có", đừng bịa ra để có cái mà báo.
```

**Lời giảng viên nói khi chiếu slide này:** "Câu cuối quan trọng: đừng bịa ra để có cái mà báo. Không có câu này thì agent sẽ tìm cho ra vài lỗi, kể cả khi không có, vì nó muốn làm hài lòng anh chị. Còn một dấu hiệu ngược lại cần cảnh giác: nếu agent trả về không có câu nào mà mắt thường anh chị vẫn thấy lỗi, tức là ràng buộc chưa vào đúng chỗ, anh chị kiểm lại xem khối ràng buộc có nằm ở đầu file skill không."

**Hình minh họa gợi ý:** Khối code nhỏ ở giữa. Bên dưới là bảng 3 cột mẫu để trống.

**Thời điểm:** Khối 2, phút 49 tới 50

---

### Slide 27: PROMPT. Kịch bản video 30 giây

**Loại:** prompt

**Nội dung hiển thị:**

```
Viết kịch bản video ngày 5, dài 30 giây, quay bằng điện thoại,
một người, không cần diễn viên.

Format bảng 4 cột: Giây | Hình | Lời thoại | Chữ trên màn hình.
Chia theo block 5 giây.
Câu đầu tiên phải nói được nỗi sợ trong 3 giây đầu.
Lời kêu gọi đặt ở 5 giây cuối, kèm từ khóa inbox.
Áp đủ ràng buộc từ cấm.
```

**Lời giảng viên nói khi chiếu slide này:** "Anh chị để ý một chi tiết trong kết quả: ở giây 20 tới 25 nó viết để 24 tiếng xem da phản ứng thế nào. Đây là mốc thời gian nhưng không phải cam kết kết quả, nó là hướng dẫn sử dụng. Ranh giới nằm đúng ở chỗ đó: cấm hứa kết quả theo thời gian, không cấm nói cách dùng. Anh chị nhớ ranh giới này khi viết ràng buộc cho ngành mình, kẻo chặn quá tay thì agent không viết được hướng dẫn dùng sản phẩm."

**Hình minh họa gợi ý:** Khối code lớn. Bên phải là bảng 4 cột với 5 dòng block thời gian, để trống.

**Thời điểm:** Khối 2, phút 50 tới 53

---

### Slide 28: PROMPT. Năm brief hình ảnh

**Loại:** prompt

**Nội dung hiển thị:**

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

**Lời giảng viên nói khi chiếu slide này:** "Dòng cuối là phép thử cho brief: đưa cho người chưa biết gì về sản phẩm mà họ vẫn làm ra được thì brief đó đạt. Brief kiểu ảnh sản phẩm đẹp, nền sáng, cảm giác tự nhiên là brief chưa dùng được, người thiết kế sẽ quay lại hỏi anh chị ba lần. Mục 6 là mục người ta hay bỏ, và ảnh trước sau là chỗ ngành mỹ phẩm dính rắc rối nhiều nhất."

**Hình minh họa gợi ý:** Khối code lớn. Góc phải là 5 khung ảnh nhỏ đánh số ngày 1, 2, 3, 7, 12.

**Thời điểm:** Khối 2, phút 53 tới 55

---

### Slide 29: Đề bài chặng 1. Skill, brief và lịch của anh chị

**Loại:** thực hành

**Nội dung hiển thị:**
- Mở `workbook/buoi-04-content-engine-agent.md`
- Bước 1, 5 phút: tạo file skill Content Engine, khối ràng buộc đặt đầu
- Bước 2, 7 phút: campaign brief 8 mục
- Bước 3, 8 phút: lịch 14 ngày đủ 8 cột
- Bước 4, 10 phút: viết 5 trong 10 bài social

**Lời giảng viên nói khi chiếu slide này:** "Slide này đứng nguyên suốt 30 phút, anh chị vừa làm vừa liếc lại. Tôi sẽ gọi từng người chia sẻ màn hình, mỗi người tối đa 5 phút, và tôi ưu tiên ai chưa có nhãn loại ngày trong lịch. Ai làm ngành có quy định chặt thì bước 1 dành thêm phút viết danh sách từ cấm của ngành mình vào khối ràng buộc, đừng dùng nguyên danh sách của mỹ phẩm."

**Hình minh họa gợi ý:** Số 30 cỡ rất lớn kèm đồng hồ. Bốn vạch chia 5, 7, 8, 10 phút.

**Thời điểm:** Khối 3a, phút 55 tới 85

---

### Slide 30: Còn 10 phút. Anh chị đang ở đâu

**Loại:** thực hành

**Nội dung hiển thị:**
- Còn 10 phút là hết chặng 1
- Mức tối thiểu trước khi nghỉ: lịch 14 ngày và 5 bài social
- Chưa ra lịch thì làm lịch 7 ngày, đủ 4 loại ngày là đạt
- Gõ vào chat: 1 nếu đã có lịch, 2 nếu chưa

**Lời giảng viên nói khi chiếu slide này:** "Tôi hỏi để biết ai đang hụt. Ai gõ 2 thì hạ xuống lịch 7 ngày, đủ bốn loại ngày là đạt, rồi làm nốt ở nhà. Lịch là đầu vào của buổi 5, không có lịch thì buổi sau anh chị phải dùng caption mẫu của Thảo An, vẫn chạy được luồng nhưng không phải nội dung của mình."

**Hình minh họa gợi ý:** Số 10 cỡ rất lớn kèm đồng hồ đếm ngược.

**Thời điểm:** Khối 3a, phút 75

---

### Slide 31: Giải lao 10 phút

**Loại:** chuyển khối

**Nội dung hiển thị:**
- Nghỉ 10 phút
- Đúng phút thứ 95 anh chị quay lại
- Ai chưa ra lịch 14 ngày thì ở lại, tôi gỡ cùng
- Đừng tắt Claude Desktop

**Lời giảng viên nói khi chiếu slide này:** "Anh chị nghỉ 10 phút, tôi để đồng hồ đếm ngược trên màn hình chia sẻ. Đây là điểm dừng tự nhiên nhất của buổi: ai cũng đã có tối thiểu năm trong mười bài social. Ai chưa ra lịch thì ở lại với tôi, mười phút này tôi gỡ, để anh chị vào chặng 2 không bị hụt."

**Hình minh họa gợi ý:** Đồng hồ đếm ngược cỡ rất lớn ở giữa.

**Thời điểm:** Giải lao, phút 85 tới 95

---

### Slide 32: Đề bài chặng 2. Sáu hạng mục còn lại

**Loại:** thực hành

**Nội dung hiển thị:**
- Bước 4, 5 phút: nốt 5 bài social còn lại
- Bước 5, 5 phút: ba email nurturing
- Bước 6, 4 phút: khối landing page
- Bước 7, 4 phút: ba kịch bản video
- Bước 8, 3 phút: carousel 6 tới 8 slide
- Bước 9, 4 phút: năm brief hình ảnh

**Lời giảng viên nói khi chiếu slide này:** "Slide này đứng nguyên suốt 25 phút. Một lỗi tôi sẽ đi soi: mười bài ra giống hệt nhau, bài nào cũng mở bằng một câu hỏi, cũng kể một khách, cũng kết bằng inbox ngay. Nguyên nhân là anh chị yêu cầu 10 bài trong một lượt và agent nhận cùng một lõi cho cả 10. Cách chữa: khai 5 lõi khác nhau trước, rồi thêm vào prompt một câu là mười bài phải có mười kiểu mở đầu khác nhau, liệt kê kiểu mở đầu ở đầu mỗi bài."

**Hình minh họa gợi ý:** Số 25 cỡ rất lớn kèm đồng hồ. Sáu vạch chia 5, 5, 4, 4, 3, 4 phút.

**Thời điểm:** Khối 3b, phút 95 tới 120

---

### Slide 33: Sáu câu tôi chấm khi anh chị chia sẻ màn hình

**Loại:** nội dung

**Nội dung hiển thị:**
1. Một xương sống: 14 dòng có rõ một insight chạy suốt không?
2. Nhịp đủ 4 loại: ưu đãi có bị dồn lên đầu không?
3. Không lặp: đọc lướt 3 bài, có phân biệt được bài nào ra bài nào không?
4. Ràng buộc có hiệu lực: agent của anh chị chặn được câu nào?
5. Nối về mục tiêu: bài này đẩy khách đi bước nào, đo bằng gì?
6. Chi tiết thật: mỗi bài có ít nhất một chi tiết trích được, hay toàn tính từ?

**Lời giảng viên nói khi chiếu slide này:** "Tôi chấm công khai, nói rõ đạt hay chưa đạt, và câu nào chưa đạt thì tôi nói rõ sửa thế nào trong 20 phút cuối, không nói chung chung kiểu làm kỹ hơn nhé. Câu 4 tôi không hỏi suông, tôi sẽ thử ngay một prompt bẫy trên máy anh chị. Câu 5: nếu anh chị trả lời để tăng tương tác thì đó không phải hành động đo được, gạch đi."

**Hình minh họa gợi ý:** 6 dấu hỏi xếp 2 hàng 3 cột, mỗi dấu kèm một dòng ngắn.

**Thời điểm:** Khối 4 Review, phút 120 tới 130

---

### Slide 34: Chín hạng mục anh chị nộp hôm nay

**Loại:** bảng

**Nội dung hiển thị:**

| # | Hạng mục | Số lượng |
|---|---|---|
| 1 | Skill Content Engine đã chỉnh cho ngành mình | 1 file |
| 2 | Campaign brief | 1 |
| 3 | Lịch 14 ngày, đủ 8 cột | 1 bảng 14 dòng |
| 4 | Bài social | 10 |
| 5 | Email nurturing | 3 |
| 6 | Khối landing page | 1 |
| 7 | Kịch bản video 30 tới 60 giây | 3 |
| 8 | Carousel | 6 tới 8 slide |
| 9 | Brief hình ảnh hoặc video | 5 |

Điểm trừ: còn một câu chạm từ cấm trừ 10; bịa review hoặc gắn tên persona vào lời chứng thực trừ 20; ô trống trong lịch trừ 5 mỗi ô.

**Lời giảng viên nói khi chiếu slide này:** "Đạt là từ 70 điểm, dưới 70 thì nộp lại trong 3 ngày. Anh chị chú ý dòng điểm trừ giữa: bịa review hoặc gắn tên persona vào lời chứng thực trừ 20 điểm. Đó là lỗi nặng nhất của buổi hôm nay, vì nó không phải lỗi viết dở mà là lỗi pháp lý. Ba phút cuối anh chị chạy lại prompt tự rà một lượt cho chắc."

**Hình minh họa gợi ý:** 9 ô vuông trống để tích, xếp 3 hàng 3 cột.

**Thời điểm:** Khối 5, phút 130 tới 142

---

### Slide 35: Lưu lịch thành file, buổi 5 đọc thẳng từ đó

**Loại:** nội dung

**Nội dung hiển thị:**
- Lưu lịch thành `lich-14-ngay.md` ngay trong thư mục làm việc
- Dạng bảng, mỗi dòng một ngày, các cột đúng thứ tự trong workbook
- Buổi 5 nối lịch này vào luồng đăng bài
- Đến ngày là bài lên hàng chờ, có ảnh kèm, chờ người bấm duyệt

**Lời giảng viên nói khi chiếu slide này:** "Lịch 14 ngày anh chị vừa làm không nằm yên trong file. Buổi sau chúng ta nối nó vào luồng đăng bài tự động. Và tôi nói thẳng một câu: buổi này làm cẩu thả thì buổi sau tự động hóa cái cẩu thả đó nhanh gấp mười lần. Anh chị dành thêm ba phút đọc lại lịch của mình trước khi lưu."

**Hình minh họa gợi ý:** Mũi tên từ file `lich-14-ngay.md` sang một biểu tượng luồng có chốt duyệt ở giữa.

**Thời điểm:** Khối 5, phút 142 tới 146

---

### Slide 36: Buổi sau. Automation và MCP

**Loại:** chuyển khối

**Nội dung hiển thị:**
- Buổi 5 nối các bước rời thành luồng tự chạy
- Mang theo: `lich-14-ngay.md` và kết nối MCP của buổi 1
- Chuẩn bị trước: liệt kê những việc anh chị làm lặp lại hàng tuần
- Nhắc lại quy định cứng: không nối kênh công ty đang chạy thật

**Lời giảng viên nói khi chiếu slide này:** "Buổi sau anh chị mang theo hai thứ trên slide. Và chuẩn bị trước ở nhà một danh sách: những việc anh chị làm lặp lại hàng tuần, càng cụ thể càng tốt. Buổi sau ta chọn ba việc trong danh sách đó để tự động hóa, và quan trọng không kém, ta chọn cả những việc không nên tự động kèm lý do. Cảm ơn anh chị, hẹn gặp buổi sau."

**Hình minh họa gợi ý:** Ba ô rời bên trái nối thành một dây chuyền liền bên phải, có một chốt duyệt hình người ở giữa dây chuyền.

**Thời điểm:** Khối 5, phút 146 tới 150
