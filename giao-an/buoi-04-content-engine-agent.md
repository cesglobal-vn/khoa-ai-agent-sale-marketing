# Buổi 4 · Content Engine Agent

**Cỗ máy sản xuất chiến dịch đa kênh.**

Từ một insight, dựng nguyên chiến dịch 14 ngày: bài viết, email, video, carousel. Thôi cảnh mỗi sáng ngồi nghĩ hôm nay đăng gì.

---

## Mục tiêu buổi

Hết 2,5 giờ, học viên phải làm được 4 việc:

1. Lấy **một** insight và bẻ nó thành 14 ngày nội dung, nhiều góc, nhiều định dạng, không lặp lại chính mình.
2. Xếp 14 ngày đó thành một nhịp có logic: ngày giáo dục, ngày bằng chứng, ngày xử lý phản đối, ngày ưu đãi. Không phải danh sách bài rời.
3. Khai báo ràng buộc pháp lý và thương hiệu **trước khi** agent viết chữ đầu tiên, để agent tự chặn, không phải ngồi sửa sau.
4. Nối từng bài về mục tiêu bán hàng. Bài nào cũng phải trả lời được: bài này đẩy khách đi bước nào trong hành trình mua.

Sản phẩm đầu ra: 1 skill Content Engine chạy được, 1 campaign brief, 1 lịch 14 ngày, 10 bài social, 3 email, 1 khối landing page, 3 kịch bản video, 1 carousel, 5 brief hình ảnh.

---

## Học viên cần chuẩn bị gì

Mang theo, có sẵn trong **thư mục làm việc** dựng ở buổi 1, mở bằng tab **Code** của Claude Desktop:

| Cần có | Lấy từ đâu | Không có thì sao |
|---|---|---|
| `CLAUDE.md` có câu định vị, 3 thông điệp, giọng văn, danh sách từ cấm | Buổi 1 | Chép bản Thảo An trong `demo/buoi-01/claude-md-va-skill-mau.md` |
| Hồ sơ sản phẩm, file `san-pham-thao-an.md` hoặc file cùng dạng của thương hiệu mình | Buổi 1 | Dùng `demo/thao-an/san-pham-thao-an.md` |
| Skill `viet-bai-ban-hang` chạy được, nằm ở `.claude/skills/viet-bai-ban-hang/SKILL.md` | Buổi 1 | Chép bản mẫu trong `demo/buoi-01/claude-md-va-skill-mau.md` |
| File `insight-khach-hang.md` có trích dẫn nguyên văn, persona, góc nội dung | Buổi 2 | Dùng bộ insight Thảo An rút từ `review-va-tin-nhan-khach.md` |
| Danh sách kênh đang chạy và vai trò từng kênh | Học viên tự khai | Dùng bộ kênh Thảo An: Facebook đầu phễu tới chốt, Shopee cuối phễu, Website nền tin cậy |
| Ràng buộc ngành của mình: từ cấm, cam kết cấm, quy định pháp lý | Học viên tự khai | Dùng mục "Điều KHÔNG được nói" của Thảo An |
| Mục tiêu bán hàng đang chạy | Học viên tự khai | 30 đơn trong 30 ngày, 100% đơn gắn được nguồn kênh |
| Tài khoản `tikhub` riêng, đã đăng ký và nạp tiền ở nhà | Học viên tự đăng ký, tự trả phí | Bỏ bước tra xu hướng, dùng thẳng dữ liệu case Thảo An, vẫn làm đủ 9 hạng mục |

**Phân vai giữa Content Engine và skill `viet-bai-ban-hang`.** Hai thứ này không chồng nhau. Content Engine lo phần **chiến dịch**: lịch 14 ngày, góc nội dung, phân bổ kênh, nhịp bốn loại ngày. Skill `viet-bai-ban-hang` lo phần **viết từng bài**: hook, thân bài, CTA, soát từ cấm. Tới bước viết caption, Content Engine gọi lại skill `viet-bai-ban-hang` chứ không viết lại từ đầu, nhờ vậy giọng văn và danh sách từ cấm anh chị dựng ở buổi 1 vẫn có hiệu lực. Cả hai skill đọc chung một `CLAUDE.md`, nên không sợ ra hai giọng khác nhau.

Nhắc học viên trước buổi 1 ngày: ai làm ngành có quy định chặt (dược, thực phẩm chức năng, tài chính, giáo dục, y tế) thì mang theo đúng danh sách từ bị cấm của ngành mình. Đây là thứ quyết định buổi hôm nay có dùng được vào việc thật hay không.

Nhắc luôn về `tikhub`: **mỗi lượt gọi công cụ đều tính tiền**, phản hồi của dịch vụ ghi thẳng "This request will incur a charge". Học viên tự đăng ký tài khoản riêng và tự trả phí, và phải đăng ký **trước buổi, ở nhà**, vì trong buổi không đủ thời gian. Ai không đăng ký vẫn học đủ, chỉ bỏ đúng bước tra xu hướng.

---

## Timeline 2,5 giờ

| Khối | Thời lượng | Nội dung | Giảng viên làm gì |
|---|---|---|---|
| 1. Framework | 20 phút | 4 ý: chiến dịch khác chuỗi bài lẻ; nhịp 14 ngày; một nội dung nhiều định dạng (gộp thêm bảng giới hạn độ dài từng kênh); khai báo ràng buộc trước khi viết | Nói, vẽ bảng lên màn hình, hỏi lớp 2 câu |
| 2. Demo **kiểu làm theo** | 35 phút | Chạy full trên case Thảo An theo `../so-tay-giang-vien/buoi-04-content-engine-agent.md`, có bước tra xu hướng bằng `tikhub` và bước cắt một bài xuống 280 ký tự | Gõ trực tiếp, không dán prompt soạn sẵn kiểu giấu bài. **Học viên gõ cùng lúc: 25 phút học viên tay trên bàn phím, 10 phút giảng viên nói và chỉ chỗ.** Xem mục "Khối 2 chạy kiểu làm theo" bên dưới |
| 3. Học viên làm, chặng 1 | 30 phút | Theo `../workbook/buoi-04-content-engine-agent.md`: bước 1 tạo file skill Content Engine (5 phút), bước 2 campaign brief (7 phút), bước 3 lịch 14 ngày (8 phút), bước 4 viết 5 trong 10 bài social (10 phút) | Đi từng bàn, mỗi bàn tối đa 5 phút. Ưu tiên bàn nào lịch 14 ngày chưa có nhãn loại ngày |
| **Giải lao** | **10 phút** | Nghỉ. Bắt buộc, không gộp vào khối khác. Cho nghỉ đúng sau khi mỗi người có tối thiểu 5 trong 10 bài social, đó là điểm dừng tự nhiên nhất | Gỡ cho máy nào chưa ra lịch 14 ngày, để họ vào chặng 2 không bị hụt |
| 3. Học viên làm, chặng 2 | 25 phút | Bước 4 nốt 5 bài social còn lại (5 phút), bước 5 ba email nurturing (5 phút), bước 6 khối landing page (4 phút), bước 7 ba kịch bản video (4 phút), bước 8 carousel (3 phút), bước 9 năm brief hình ảnh (4 phút) | Đủ 9 hạng mục |
| 4. Review | 10 phút | Gọi 3 học viên chiếu màn hình, chấm theo tiêu chí bên dưới | Chấm công khai, nói rõ đạt hay chưa đạt |
| 5. Hoàn thiện và nộp | 20 phút | Sửa theo góp ý, nộp file | Chốt danh sách nộp trước khi tan lớp |

**Cộng lại để tự kiểm:** 20 + 35 + 30 + 10 + 25 + 10 + 20 = **150 phút**, khớp thời lượng khai báo.

**Tay học viên đặt trên bàn phím:** demo làm theo 25 + chặng 1 là 30 + chặng 2 là 25 + hoàn thiện 20 = 100 phút trên 140 phút học thật, tức 71,4 phần trăm.

> **Lưu ý cho giảng viên:** con số phút ghi trong ngoặc ở từng bước của workbook tính theo nhịp cũ chưa có giải lao, cộng lại là 65 phút. Nhịp mới cho 55 phút gõ, chia hai chặng như bảng trên. Bám bảng trên. Ai không kịp thì áp mức đạt tối thiểu theo nhóm chậm: **lịch 7 ngày thay vì 14, đủ 4 loại ngày là đạt; 5 bài social tại lớp, 5 bài còn lại về nhà.**

---

## Khối 2 chạy kiểu làm theo, không phải ngồi xem

**Đây là điều kiện để buổi này đạt ngưỡng thực hành.** Giảng viên bấm nhanh cho kịp giờ thì 25 phút chuyển ngược sang cột lý thuyết và buổi tụt xuống dưới ngưỡng.

**Câu dặn đọc lên trước khi gõ chữ đầu tiên của khối 2:**

> "Anh chị mở thư mục làm việc ra, mở sẵn `insight-khach-hang.md` của buổi 2. Đặt tay lên bàn phím. Ba mươi lăm phút tới tôi gõ gì thì anh chị gõ y hệt trên máy mình, và gõ trên insight của chính anh chị chứ không phải của Thảo An. Tôi đi chậm, và sau mỗi prompt lớn tôi dừng lại hỏi ai chưa ra kết quả."

**Học viên gõ gì song song:**

| Giảng viên làm | Học viên gõ cùng lúc trên máy mình |
|---|---|
| Tra xu hướng bằng `tikhub` | Ai có tài khoản thì tra trên ngành của mình. Ai chưa có thì mở bảng insight của mình ra, chọn sẵn 1 insight để lát nữa nạp vào Content Engine |
| Cài skill Content Engine, nạp 1 insight | Cài skill đó vào thư mục của mình, nạp insight của chính mình |
| Ra campaign brief | Ra campaign brief của chính mình |
| Ra lịch 14 ngày đủ 4 loại ngày | Ra lịch của chính mình, tự đếm có đủ 4 loại và không có 3 ngày liền cùng loại không |
| Khai ràng buộc pháp lý rồi cố tình nhờ agent viết một câu chứa từ cấm | Khai đúng danh sách từ cấm của ngành mình, rồi thử đúng câu đó trên máy mình |
| Cắt một bài xuống 280 ký tự | Cắt một bài của chính mình xuống 280 ký tự, tự đếm còn đủ nỗi đau, điểm khác biệt, lời kêu gọi không |

**Bốn điểm dừng bắt buộc:**

1. **Sau khi skill Content Engine được gọi ra lần đầu:** "Ai chưa thấy Claude gọi đúng skill thì giơ tay." Chờ hai phần ba lớp.
2. **Sau khi ra lịch 14 ngày:** "Ai chưa ra đủ lịch thì giơ tay." Điểm dừng dài nhất, chờ tới 90 giây. Lịch là xương sống cả buổi và là đầu vào của buổi 5.
3. **Sau khi thử từ cấm:** "Trên máy anh chị, agent nó từ chối và nói rõ lý do, hay nó viết luôn rồi anh chị phải ngồi sửa tay?" Đếm bằng giơ tay. Ai phải sửa tay thì đó là dấu hiệu ràng buộc khai chưa đủ, sửa phần khai báo chứ không sửa bài.
4. **Sau khi cắt bài xuống 280 ký tự:** "Bài đã cắt trên máy anh chị còn đủ ba phần không: một nỗi đau, một điểm khác biệt, một lời kêu gọi?" Mất một phần là chưa đạt, cho làm lại ngay tại chỗ.

**Quy tắc cứng:** thà chạy chậm mà cả lớp gõ, còn hơn chạy đúng giờ mà nửa lớp ngồi xem. Thiếu giờ thì bỏ bước tra xu hướng bằng `tikhub`, không bỏ điểm dừng nào.

---

## Khối 1 · Framework 20 phút

### 1.1 Chiến dịch khác chuỗi bài lẻ ở chỗ nào (5 phút)

Mở bằng câu hỏi cho lớp: "Tháng vừa rồi anh chị đăng bao nhiêu bài? Có bài nào nối vào bài nào không?"

Phần lớn sẽ trả lời là không. Đó là chuỗi bài lẻ. Đặc điểm của nó:

- Mỗi bài tự đứng một mình, đọc bài 7 không cần biết bài 3 nói gì.
- Mỗi bài cố nói hết mọi thứ vì sợ khách chỉ đọc đúng bài này.
- Kết quả: bài nào cũng na ná bài nào, khách lướt qua vì thấy quen mắt.
- Không đo được. Bài này ra đơn hay bài kia ra đơn, không ai biết.

Chiến dịch thì khác. Ba dấu hiệu nhận biết:

1. **Có một xương sống.** Một insight duy nhất chạy suốt. Mọi bài đều là một mặt của cùng một nỗi đau.
2. **Có thứ tự.** Bài ngày 1 làm khách biết, ngày 5 làm khách tin, ngày 9 gỡ nút thắt, ngày 14 mới xin đơn. Đảo thứ tự là hỏng.
3. **Mỗi bài có một việc phải làm.** Không bài nào ôm hết. Bài giáo dục thì không chốt đơn. Bài ưu đãi thì không giảng giải dài.

Ví dụ để lớp thấy ngay, lấy Thảo An: insight xương sống là **nỗi sợ kích ứng khi đổi sang sản phẩm mới**. Bằng chứng có thật trong dữ liệu, không phải đoán:

- R11: "Trước mình dùng loại khác bị nổi mẩn, đổi qua đây thì ổn. Sẽ mua lại."
- M01: "Da mình nhạy cảm lắm, dùng cái này có bị rát không shop?"
- M02: "Sản phẩm này có cồn không ạ? Mình dị ứng cồn."
- M06: "Đang dùng của hãng khác, đổi qua có sao không?"

Một nỗi sợ đó nuôi được 14 ngày, vì nó có nhiều mặt: sợ thành phần, sợ mất tiền vô ích, sợ bị hứa hão, sợ chọn sai loại cho da mình.

### 1.2 Nhịp 14 ngày (5 phút)

Nói thẳng với lớp: lịch nội dung không phải là danh sách 14 tiêu đề. Nó là một nhịp.

Bốn loại ngày, mỗi loại làm một việc khác nhau:

| Loại ngày | Làm gì cho khách | Đo bằng gì |
|---|---|---|
| **Giáo dục** | Dạy khách một thứ họ chưa biết, để họ tự thấy vấn đề của mình | Lưu bài, bình luận từ khóa, thời gian đọc |
| **Bằng chứng** | Chứng minh bằng review thật, ảnh thật, giấy tờ thật | Click sang Shopee, xem hết video |
| **Xử lý phản đối** | Gỡ đúng cái nút đang chặn khách bấm mua | Số inbox, chất lượng câu hỏi trong inbox |
| **Ưu đãi** | Cho một lý do để mua hôm nay chứ không phải tuần sau | Đơn có mã, doanh thu |

Tỷ lệ đề xuất cho 14 ngày: 5 giáo dục, 4 bằng chứng, 3 xử lý phản đối, 2 ưu đãi.

Vì sao ưu đãi chỉ 2: khách của Thảo An hỏi trung bình 4 đến 6 lượt inbox mới chốt. Người còn đang sợ kích ứng thì giảm giá không giải quyết được gì. Phải tin trước rồi mới mua.

Vì sao ưu đãi phải nằm ở ngày 7 và ngày 14: cuối tuần 1 để bắt nhóm đã tin sớm; cuối tuần 2 để chốt nhóm chần chừ. Đặt ưu đãi ngày 2 là đốt tiền vào người chưa tin.

Vẽ lên bảng dòng chảy: **biết → tin → hỏi → mua**. Ngày giáo dục làm khách biết. Ngày bằng chứng làm khách tin. Ngày xử lý phản đối làm khách hỏi. Ngày ưu đãi làm khách mua. Bài nào không nằm được vào một trong bốn ô này là bài thừa, xóa.

### 1.3 Một nội dung tái sử dụng qua nhiều định dạng (5 phút)

Đây là chỗ tiết kiệm nhiều thời gian nhất, và cũng là chỗ dễ làm ẩu nhất.

Sai lầm hay gặp: copy nguyên caption Facebook rồi dán sang email, đổi tiêu đề. Ra một bản nhạt cả hai bên.

Cách đúng: giữ **lõi**, đổi **cách kể**. Lõi gồm 3 thứ, không đổi: một nỗi đau, một điểm mạnh sản phẩm, một lời kêu gọi. Cách kể thì đổi theo nơi khách đang đứng.

Lấy một lõi của Thảo An làm ví dụ. Lõi: *sợ đổi sản phẩm bị kích ứng + không cồn, không hương liệu tổng hợp, đã test da liễu + đọc bảng thành phần trước khi mua*.

| Định dạng | Cách kể lõi này | Vì sao hợp |
|---|---|---|
| Bài chữ dài Facebook | Kể câu chuyện một khách đổi sản phẩm rồi nổi mẩn, rồi mới dẫn vào bảng thành phần | Buổi tối khách lướt chậm, chịu đọc |
| Carousel 7 slide | Mỗi slide một dòng thành phần, đọc là hiểu, không cần chú thích | Khách lướt nhanh, cần nhìn ra ngay |
| Video 30 giây | Quay tay thoa lên cổ tay, nói to 3 thành phần | Chứng minh bằng hình, không cần tin lời |
| Email | Viết dài hơn, giải thích vì sao cồn làm da rát, có chỗ để đọc kỹ | Người mở email là người đã quan tâm |
| Khối landing page | Bảng thành phần đặt cạnh nút mua, không kể chuyện | Người vào landing là người sắp quyết định |

Quy tắc chống lặp: **một lõi tối đa 3 định dạng, và không đăng 2 định dạng của cùng lõi trong 3 ngày liên tiếp.** 14 ngày cần khoảng 5 lõi khác nhau, không phải 14 lõi và cũng không phải 1.

**Giới hạn độ dài từng kênh.** Phần này gộp vào đúng 5 phút của ý 1.3, thay cho đoạn giảng thêm về tái sử dụng. Chiếu bảng lên, nói 1 phút, không giảng dài.

Viết nội dung đa kênh mà không biết giới hạn từng kênh thì bài ra xong phải ngồi cắt lại bằng tay. Cắt tay lúc gần giờ đăng là lúc dễ cắt mất đúng câu quan trọng nhất.

| Nền tảng | Giới hạn caption (ký tự) | Ảnh tối đa | Video tối đa | Ghi chú |
|---|---|---|---|---|
| Facebook | 63.206 | 10 | 1 | |
| TikTok | 2.200 | 35 | 1 | |
| Instagram | 2.200 | 10 | 1 | |
| LinkedIn | 3.000 | 20 | 1 | tiêu đề 200 |
| YouTube | 5.000 | 0 | 1 | tiêu đề 100 |
| Twitter | 280 | 4 | 1 | |
| Threads | 500 | 10 | 1 | |
| Pinterest | 800 | 1 | 1 | tiêu đề 100 |
| Douyin | 1.000 | 12 | 1 | tiêu đề 30 |
| Xiaohongshu | 1.000 | 9 | 1 | tiêu đề 20 |

Nói với lớp: cùng một lõi, Facebook cho 63.206 ký tự nên kể được cả câu chuyện; Twitter cho 280 ký tự nên chỉ chở được đúng một câu. Đó không phải cắt ngắn, đó là viết lại. Ai định đăng cùng một caption lên cả bốn kênh thì bốn kênh đều nhận một bài không hợp kênh nào.

Bảng này lấy từ MCP `aitoearn`, công cụ `listChannelPlatforms`. Nền tảng đổi chính sách thì gọi lại đúng công cụ đó để lấy số mới, đừng tin bảng in sẵn quá sáu tháng. Buổi hôm nay chỉ dùng `aitoearn` để **tra** giới hạn, chưa đăng bài. Đăng thật lên kênh thật là việc của buổi 5.

### 1.4 Vì sao khai báo ràng buộc trước khi viết, không sửa sau (5 phút)

Đây là phần chống rủi ro của buổi hôm nay. Nói chậm.

Cho lớp thấy con số: 14 ngày, 10 bài social, 3 email, 3 video, 1 carousel 7 slide, 1 khối landing. Tổng cộng khoảng 30 mẩu chữ. Nếu sửa sau, học viên phải đọc dò 30 mẩu và tự bắt lỗi. Bắt sót một câu là một câu chạy ads sai.

Ba lý do phải khai báo trước:

1. **Rẻ hơn.** Khai báo trước tốn 10 dòng. Sửa sau tốn 30 lượt đọc dò.
2. **Sót ít hơn.** Người đọc dò đến mẩu thứ 20 là bắt đầu lướt. Agent thì không mệt.
3. **Đổi được cả loạt.** Luật ngành đổi, sửa 1 dòng trong file skill rồi chạy lại, thay vì sửa tay 30 chỗ.

Danh sách cấm của Thảo An, đọc to cho lớp nghe: không dùng "trị mụn", "đặc trị", "khỏi hẳn", "trắng da cấp tốc"; không cam kết thời gian có kết quả kiểu "7 ngày hết thâm"; không nói sản phẩm là thuốc hay chữa bệnh; không so sánh trực tiếp bằng tên với thương hiệu khác; không bịa thành phần hoặc công dụng ngoài bảng.

Hỏi lớp: "Ngành của anh chị có danh sách tương tự chưa? Chưa có thì 10 phút nữa vào workbook viết ra."

Nhắc luôn **ba nguyên tắc chống bịa**, áp cho mọi agent trong khóa:

1. Chỉ nêu công dụng có trong hồ sơ sản phẩm. Không bịa thành phần, công dụng, review.
2. Gắn nhãn nguồn: `[DATA THẬT]` khi trích được, `[SUY LUẬN]` khi tự suy. Thiếu thì ghi thẳng "chưa đủ dữ liệu".
3. Người duyệt cuối. Mọi bài là nháp, agent không tự đăng.

Nguyên tắc 1 có một cái bẫy tinh vi, nói rõ ở đây: **persona không phải người thật.** "Chị Ngọc, 30 tuổi, nhân viên văn phòng" là chân dung suy ra từ dữ liệu, không phải một khách hàng có thật. Agent lấy tên Chị Ngọc gắn vào một lời chứng thực là đang bịa review. Muốn trích lời khách thì trích nguyên văn R01 đến R15 hoặc M01 đến M15.

---

## Bước tra xu hướng và đối thủ

**Không phải khối mới. Hai phút này gộp vào mốc B của demo (35 phút demo giữ nguyên), lấy từ phần bình luận của mốc B.** Trong phần học viên làm, nó nằm ở 2 phút đầu của Bước 2 trong workbook, tức trong chặng 1 của khối 3.

Trước khi dựng chiến dịch, nhìn ra ngoài một lượt: hashtag của ngành mình đang chạy thế nào, và đối thủ đang đăng gì. Không phải để bắt chước, mà để biết góc nào đã bão hòa và tránh.

Dùng MCP `tikhub`, đúng ba công cụ:

| Việc cần làm | Tên công cụ |
|---|---|
| Xem một hashtag đang chạy thế nào | `tiktok_app_v3_fetch_hashtag_detail` |
| Lấy video đang lên theo hashtag đó | `tiktok_app_v3_fetch_hashtag_video_list` |
| Tra thư viện quảng cáo đối thủ | `tiktok_ads_search_ads` |

Bốn ràng buộc, đọc to cho lớp trước khi ai bấm gọi:

1. **Mỗi lượt gọi đều tính tiền.** Dịch vụ trả về nguyên văn "This request will incur a charge". Nghĩ kỹ trước khi gọi, đừng gọi cho vui.
2. **Gọi một lần rồi lưu kết quả thành file** trong thư mục làm việc, đặt tên `xu-huong-hashtag.md`. Lần sau đọc lại file, không gọi lại.
3. **Chỉ lấy dữ liệu công khai.** Không lấy thông tin cá nhân của người bình luận ngoài phần họ viết công khai. Không dựng danh sách cá nhân từ bình luận.
4. **Ai không có tài khoản `tikhub` vẫn làm được đủ bài.** Bỏ hẳn hai phút này, dùng thẳng bộ dữ liệu case Thảo An trong `demo/thao-an/`. Không ai bị mất hạng mục nộp vì chuyện này.

Kết quả tra về là đầu vào bổ sung cho campaign brief, không thay thế insight. Insight xương sống vẫn lấy từ dữ liệu khách của mình.

---

## Điểm học viên hay vấp và cách xử lý

**1. Mười bài ra giống hệt nhau.**
Dấu hiệu: bài nào cũng mở bằng một câu hỏi, cũng kể một khách, cũng kết bằng "inbox ngay".
Nguyên nhân: học viên yêu cầu 10 bài trong một lượt, agent nhận cùng một lõi cho cả 10.
Cách chữa: bắt học viên khai 5 lõi khác nhau trước, mỗi lõi một nỗi đau riêng, rồi mới yêu cầu viết. Thêm vào prompt: "10 bài phải có 10 kiểu mở đầu khác nhau, liệt kê kiểu mở đầu ở đầu mỗi bài."

**2. Giọng văn nhạt, đọc như thông cáo báo chí.**
Dấu hiệu: nhiều tính từ, ít chi tiết. "Sản phẩm chất lượng cao, an toàn cho làn da của bạn."
Nguyên nhân: `CLAUDE.md` trong thư mục làm việc chưa có phần giọng văn, hoặc có mà học viên viết bài trong một thư mục khác nên Claude không đọc được file đó. Cũng có thể do bỏ qua skill `viet-bai-ban-hang` và bắt Content Engine tự viết caption từ đầu.
Cách chữa: yêu cầu mỗi bài phải chứa ít nhất một chi tiết cụ thể lấy từ dữ liệu: một câu nguyên văn của khách, một con số, một thành phần có tên. Cấm tính từ trống nghĩa. Chỉ vào bài của học viên và hỏi: "Câu này ai cũng viết được, đúng không?"

**3. Agent hứa quá lời.**
Dấu hiệu: xuất hiện "hết thâm", "sau 7 ngày", "đặc trị", "cam kết hiệu quả".
Nguyên nhân: chưa khai báo ràng buộc, hoặc khai rồi mà đặt cuối prompt nên bị chìm.
Cách chữa: đưa khối ràng buộc lên **đầu** file skill, ngay sau frontmatter, và bắt agent tự rà lại. Cho học viên chạy đúng câu này sau khi có bài: "Rà lại toàn bộ nội dung vừa viết, liệt kê mọi câu chạm vào danh sách từ cấm hoặc cam kết thời gian, kèm câu thay thế." Nếu agent trả về "không có câu nào" mà mắt thường vẫn thấy, tức là ràng buộc chưa vào đúng chỗ.

**4. Không nối được về mục tiêu bán hàng.**
Dấu hiệu: hỏi "bài này để làm gì" thì học viên trả lời "để tăng tương tác".
Cách chữa: bắt mỗi dòng trong lịch 14 ngày phải điền được ô "lời kêu gọi" bằng một hành động đo được: bình luận từ khóa, inbox, bấm link có gắn UTM, dùng mã giảm giá riêng kênh. "Tăng tương tác" không phải hành động đo được, gạch đi.

**5. Lịch 14 ngày ra thành 14 dòng cùng một loại ngày.**
Dấu hiệu: mở bảng ra thấy 14 dòng đều là bán hàng, hoặc 14 dòng đều là chia sẻ kiến thức.
Cách chữa: bắt thêm cột "loại ngày" và yêu cầu agent tự đếm cuối bảng: giáo dục mấy ngày, bằng chứng mấy ngày, phản đối mấy ngày, ưu đãi mấy ngày. Lệch tỷ lệ 5/4/3/2 quá xa thì bắt xếp lại.

**6. Brief hình ảnh viết chung chung, người thiết kế không làm được.**
Dấu hiệu: "ảnh sản phẩm đẹp, nền sáng, cảm giác tự nhiên."
Cách chữa: brief phải có đủ 5 mục: bố cục, chủ thể, chữ trên ảnh, tỷ lệ khung, thứ được phép và không được phép xuất hiện. Nói với lớp: brief đúng là brief mà đưa cho người chưa biết gì về sản phẩm họ vẫn làm ra được.

---

## Khối 4 · Review 10 phút

Gọi 3 học viên chiếu màn hình, mỗi người 2 phút. Chấm tại chỗ theo 6 câu, trả lời có hoặc không:

1. **Một xương sống:** đọc 14 dòng lịch có thấy rõ chỉ một insight chạy suốt không, hay là 14 chủ đề rời?
2. **Nhịp đủ 4 loại:** có đủ giáo dục, bằng chứng, xử lý phản đối, ưu đãi không? Ưu đãi có bị dồn lên đầu không?
3. **Không lặp:** đọc lướt 3 bài bất kỳ, có phân biệt được bài nào ra bài nào không?
4. **Ràng buộc có hiệu lực:** hỏi thẳng học viên "agent của bạn chặn được câu nào?", rồi thử ngay một prompt bẫy.
5. **Nối về mục tiêu:** chỉ vào một dòng bất kỳ, hỏi "bài này đẩy khách đi bước nào, đo bằng gì?"
6. **Chi tiết thật:** mỗi bài có ít nhất một chi tiết trích được từ dữ liệu, hay toàn tính từ?

Câu nào "không" thì nói rõ sửa thế nào trong 20 phút cuối. Không nói chung chung kiểu "làm kỹ hơn nhé".

---

## Sản phẩm nộp và cách chấm

Nộp một thư mục hoặc một tài liệu gộp, gồm đủ 9 hạng mục:

| # | Hạng mục | Số lượng | Điểm |
|---|---|---|---|
| 1 | Skill Content Engine, file `.claude/skills/content-engine/SKILL.md` đã chỉnh cho ngành của mình | 1 | 15 |
| 2 | Campaign brief | 1 | 10 |
| 3 | Lịch nội dung 14 ngày, đủ 7 cột | 1 bảng 14 dòng | 20 |
| 4 | Bài social | 10 | 20 |
| 5 | Email nurturing | 3 | 8 |
| 6 | Khối landing page | 1 | 7 |
| 7 | Kịch bản video 30 đến 60 giây | 3 | 8 |
| 8 | Carousel | 6 đến 8 slide | 7 |
| 9 | Brief hình ảnh hoặc video | 5 | 5 |

**Điểm trừ, áp sau khi cộng:**

- Còn một câu chạm danh sách từ cấm: trừ 10. Còn từ hai câu trở lên: trừ 20.
- Bịa review, bịa thành phần, hoặc gắn tên persona vào lời chứng thực: trừ 20.
- Có ô nào trong lịch 14 ngày để trống: trừ 5 mỗi ô.

Đạt: từ 70 điểm. Dưới 70 thì nộp lại trong 3 ngày.

---

## Nối sang buổi 5

Nói câu này trước khi tan lớp: "Lịch 14 ngày anh chị vừa làm không nằm yên trong file. Buổi sau chúng ta nối nó vào luồng đăng bài tự động: đến ngày là bài lên hàng chờ, có ảnh kèm, chỉ chờ người bấm duyệt. Buổi này làm cẩu thả thì buổi sau tự động hóa cái cẩu thả đó nhanh gấp mười lần."

Nhắc học viên lưu lịch 14 ngày thành file `lich-14-ngay.md` ngay trong thư mục làm việc, ở dạng bảng, mỗi dòng một ngày, các cột đúng thứ tự trong workbook. Buổi 5 sẽ đọc thẳng từ file đó.
