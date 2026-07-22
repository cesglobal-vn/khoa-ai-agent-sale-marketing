# Buổi 4 · Workbook học viên

**Content Engine Agent.** 65 phút, làm ra một chiến dịch 14 ngày dùng được thật.

Làm theo thứ tự. Đừng nhảy cóc sang bước viết bài, vì bài viết ra từ lõi sai thì sửa lại cả loạt.

---

## Checklist chuẩn bị

Tick đủ 7 ô rồi mới bắt đầu bước 1.

- [ ] Thư mục làm việc của buổi 1 đang mở bằng tab **Code**, trong đó có `CLAUDE.md` đủ câu định vị, 3 thông điệp, giọng văn, danh sách từ cấm.
- [ ] Skill `viet-bai-ban-hang` của buổi 1 còn nguyên ở `.claude/skills/viet-bai-ban-hang/SKILL.md`. Bước 4 hôm nay gọi lại skill này.
- [ ] File `insight-khach-hang.md` của buổi 2 nằm trong thư mục làm việc, có phần trích dẫn nguyên văn.
- [ ] Đã chọn **một** insight xương sống cho chiến dịch này. Một thôi.
- [ ] Đã viết ra danh sách kênh và vai trò từng kênh.
- [ ] Đã điền xong **Bảng ràng buộc** ở cuối workbook này.
- [ ] Đã viết ra mục tiêu bán hàng bằng con số.

Chưa có dữ liệu thật thì nhảy xuống mục **"Chưa có insight thật thì làm gì"** ở cuối, lấy bộ Thảo An rồi quay lại đây.

---

## Bước 1 · Tạo file skill Content Engine (6 phút)

Mở `../demo/buoi-04/skill-content-engine.md`, copy toàn bộ khối skill. Sửa 4 chỗ: dòng `description` trong frontmatter (viết đúng những câu bạn thật sự sẽ gõ), tên thương hiệu, danh sách từ cấm của ngành mình, danh sách công dụng được phép nói.

Rồi gõ trong tab **Code**, ngay trong thư mục làm việc:

```
Tạo file .claude/skills/content-engine/SKILL.md trong thư mục làm việc này,
tạo luôn thư mục cha nếu chưa có. Nội dung như sau: [dán khối đã sửa]
```

Claude xin phép ghi file thì bấm **Yes**. Đừng tạo thư mục `.claude` bằng tay, Windows ẩn nó đi, tạo tay dễ sai chỗ.

Kiểm tra skill có được gọi không: mở **phiên mới**, gõ một câu tự nhiên, **không** nhắc tên skill.

```
Dựng cho tôi chiến dịch nội dung 14 ngày cho [sản phẩm của bạn].
Liệt kê giúp tôi cần cấp những gì trước khi viết, đừng viết nội dung vội.
```

Đúng khi Claude báo đang dùng skill `content-engine` và hỏi lại đầu vào còn thiếu. Không gọi skill thì lỗi ở dòng `description`, viết lại cho giống câu bạn vừa gõ. Gọi rồi mà viết bài ngay thì phần "Quy trình làm việc" trong file bị đặt sai chỗ, kiểm tra lại thứ tự.

---

## Bước 2 · Campaign brief (8 phút)

**Hai phút đầu, chỉ dành cho ai đã đăng ký tài khoản `tikhub` ở nhà.** Nhìn ra ngoài một lượt trước khi dựng chiến dịch: hashtag ngành mình đang chạy thế nào, đối thủ đang đăng gì. Gọi đúng ba công cụ: `tiktok_app_v3_fetch_hashtag_detail`, `tiktok_app_v3_fetch_hashtag_video_list`, `tiktok_ads_search_ads`.

**Mỗi lượt gọi tính tiền vào tài khoản của bạn.** Dịch vụ trả về nguyên chữ "This request will incur a charge". Nên gọi một lần, rồi lưu ngay:

```
Lưu kết quả vừa lấy được thành file xu-huong-hashtag.md trong thư mục làm việc.
Ghi rõ ngày lấy, hashtag nào, và 5 góc nội dung đang bị lặp nhiều nhất.
Chỉ lấy nội dung công khai, không ghi lại tên hay thông tin cá nhân của ai.
```

Lần sau cần thì đọc lại file đó, đừng gọi lại. Tra để biết góc nào đã bão hòa mà **tránh**, không phải để bắt chước. Insight xương sống vẫn lấy từ dữ liệu khách của bạn.

**Chưa có tài khoản `tikhub` thì bỏ hẳn hai phút này**, đi thẳng vào prompt bên dưới. Bạn vẫn nộp đủ 9 hạng mục, không mất điểm nào.

**Sáu phút còn lại, viết brief:**

```
Insight xương sống cho chiến dịch 14 ngày:
"[dán insight của bạn, 2 đến 3 câu]"

Bằng chứng [DATA THẬT]:
- [trích dẫn 1 nguyên văn]
- [trích dẫn 2 nguyên văn]
- [trích dẫn 3 nguyên văn]

Bối cảnh:
- Persona chính: [dán persona buổi 2]
- Kênh và vai trò: [kênh 1 làm gì, kênh 2 làm gì, kênh 3 làm gì]
- Mục tiêu bán hàng: [con số cụ thể, trong bao lâu]

Viết campaign brief đúng 8 mục:
1. Tên chiến dịch
2. Insight xương sống (chép lại, không diễn giải thêm)
3. Khách mục tiêu, viết bằng lời khách nói
4. Ba thông điệp trụ cột, mỗi cái 1 câu
5. Năm lõi nội dung, mỗi lõi = 1 nỗi đau + 1 điểm mạnh sản phẩm
6. Vai trò từng kênh trong 14 ngày này
7. Chỉ số đo, tách chỉ số đầu phễu và chỉ số đơn hàng
8. Điều tuyệt đối không nói

Gắn nhãn [DATA THẬT] hoặc [SUY LUẬN] cho mỗi dòng.
Thiếu dữ liệu thì ghi "chưa đủ dữ liệu", không tự điền.
```

**Điền vào đây:**

| Mục | Nội dung của bạn |
|---|---|
| Tên chiến dịch | |
| Insight xương sống | |
| Khách mục tiêu | |
| 3 thông điệp trụ cột | |
| Lõi 1 (pain + USP) | |
| Lõi 2 | |
| Lõi 3 | |
| Lõi 4 | |
| Lõi 5 | |
| Vai trò từng kênh | |
| Chỉ số đầu phễu | |
| Chỉ số đơn hàng | |
| Điều không được nói | |

**Dừng lại kiểm tra:** đọc to 5 lõi. Chúng khác nhau thật hay chỉ khác chữ? Giống nhau thì sửa ngay, đừng viết tiếp.

---

## Bước 3 · Lịch 14 ngày (9 phút)

```
Dựa trên campaign brief vừa rồi, lên lịch nội dung 14 ngày.
Xuất bảng markdown đúng 8 cột:
Ngày | Kênh | Định dạng | Loại ngày | Góc nội dung | Pain | USP | Lời kêu gọi

Nhịp bắt buộc: 5 ngày giáo dục, 4 ngày bằng chứng,
3 ngày xử lý phản đối, 2 ngày ưu đãi.
Hai ngày ưu đãi đặt ở ngày 7 và ngày 14, không sớm hơn.
Ba ngày liên tiếp không dùng cùng một lõi.

Sản lượng phải khớp: 10 bài social (1 là carousel), 3 email,
3 video 30-60 giây, 1 khối landing page.

Cột "Lời kêu gọi" phải là hành động đo được: bình luận từ khóa cụ thể,
inbox từ khóa cụ thể, bấm link có UTM, dùng mã giảm giá riêng kênh.
Cấm ghi "tương tác", "tìm hiểu thêm", "theo dõi trang".

Cuối bảng đếm lại: số ngày mỗi loại, số bài mỗi định dạng.
```

**Điền vào đây (14 dòng, không để trống ô nào):**

| Ngày | Kênh | Định dạng | Loại ngày | Góc nội dung | Pain | USP | Lời kêu gọi |
|---|---|---|---|---|---|---|---|
| 1 | | | | | | | |
| 2 | | | | | | | |
| 3 | | | | | | | |
| 4 | | | | | | | |
| 5 | | | | | | | |
| 6 | | | | | | | |
| 7 | | | | | | | |
| 8 | | | | | | | |
| 9 | | | | | | | |
| 10 | | | | | | | |
| 11 | | | | | | | |
| 12 | | | | | | | |
| 13 | | | | | | | |
| 14 | | | | | | | |

Đếm lại: giáo dục ___ ngày · bằng chứng ___ ngày · xử lý phản đối ___ ngày · ưu đãi ___ ngày.

---

## Bước 4 · 10 bài social (16 phút)

Chia làm 2 lượt, mỗi lượt 5 bài. Xin 10 bài một lượt là ra 10 bài giống nhau.

**Bước này không viết lại từ đầu.** Skill Content Engine lo phần chiến dịch, còn skill `viet-bai-ban-hang` của buổi 1 lo phần viết từng bài. Bắt Content Engine gọi lại skill kia, để giọng văn và danh sách từ cấm bạn dựng buổi 1 vẫn có hiệu lực.

```
Viết đầy đủ 5 bài social cho ngày [1, 2, 3, 6, 7], nguyên văn caption,
sẵn sàng đăng.

Gọi skill viet-bai-ban-hang để viết, đừng tự viết từ đầu. Truyền sang
skill đó: SKU, nhóm khách, kênh, lõi nội dung của ngày đó, số ký tự
tối đa của kênh. Bài trả về thì kiểm lại đúng lõi và đúng loại ngày
trong lịch chưa, và 5 bài có trùng kiểu mở đầu không.

Cấu trúc bắt buộc mỗi bài: 1 pain + 1 USP + 1 lời kêu gọi.
Mỗi bài phải chứa ít nhất một chi tiết trích được từ dữ liệu:
câu nguyên văn của khách, hoặc tên thành phần, hoặc con số có thật.
Cấm tính từ trống nghĩa: "chất lượng cao", "an toàn tuyệt đối",
"hiệu quả vượt trội".

Viết vừa khuôn kênh ngay từ đầu, đừng viết dài rồi để tôi tự cắt.
Cuối mỗi caption ghi kênh và số ký tự thực tế, ví dụ "(Twitter, 258/280)".

5 bài phải có 5 kiểu mở đầu khác nhau. Ghi rõ kiểu mở đầu ở đầu mỗi bài.
Cuối mỗi bài ghi 1 dòng: bài này đẩy khách đi bước nào
(biết / tin / hỏi / mua) và đo bằng chỉ số gì.
Áp đủ ràng buộc từ cấm.
```

Lượt 2: đổi thành ngày `[8, 9, 11, 12, 14]`, thêm câu: "5 bài này không được trùng kiểu mở đầu với 5 bài trước."

Nếu Claude không báo gọi skill `viet-bai-ban-hang`, kiểm tra file skill đó còn nằm trong thư mục làm việc không. Nó viết thẳng bằng giọng chung chung là dấu hiệu skill buổi 1 không được đọc.

Giới hạn ký tự của các kênh phổ biến: Facebook 63.206 · TikTok 2.200 · Instagram 2.200 · LinkedIn 3.000 · YouTube 5.000 (tiêu đề 100) · Twitter 280 · Threads 500 · Pinterest 800. Muốn số cập nhật thì gọi `listChannelPlatforms` của MCP `aitoearn`.

| # | Ngày | Kiểu mở đầu | Bước trong phễu | Đã dán bài chưa |
|---|---|---|---|---|
| 1 | | | | ☐ |
| 2 | | | | ☐ |
| 3 | | | | ☐ |
| 4 | | | | ☐ |
| 5 | | | | ☐ |
| 6 | | | | ☐ |
| 7 | | | | ☐ |
| 8 | | | | ☐ |
| 9 | | | | ☐ |
| 10 | | | | ☐ |

---

## Bước 5 · 3 email nurturing (6 phút)

```
Viết 3 email nurturing cho ngày [4, 9, 14] trong lịch.

Mỗi email gồm: dòng tiêu đề (tối đa 9 từ) | dòng xem trước |
thân email 150-250 từ | 1 lời kêu gọi duy nhất.

Vai trò từng email:
- Email 1: giáo dục, không bán, không nhắc giá.
- Email 2: xử lý phản đối, trả lời đúng câu khách hay hỏi nhất.
- Email 3: ưu đãi, có mã riêng kênh email, có hạn chót.

Email viết dài hơn và giải thích kỹ hơn caption, vì người mở email
là người đã quan tâm. Không copy caption dán sang.
Áp đủ ràng buộc từ cấm.
```

| Email | Ngày | Tiêu đề | Vai trò | Lời kêu gọi |
|---|---|---|---|---|
| 1 | | | Giáo dục | |
| 2 | | | Xử lý phản đối | |
| 3 | | | Ưu đãi | |

---

## Bước 6 · Khối landing page (5 phút)

```
Viết 1 khối landing page cho ngày 12, tiêu đề khối hướng tới người
đang sợ [nỗi sợ chính của bạn].

Gồm: tiêu đề khối | 1 câu dẫn | 3 gạch đầu dòng bằng chứng
(mỗi gạch phải kiểm chứng được, không phải lời khen) |
1 bảng thành phần hoặc thông số | 1 nút bấm với chữ trên nút.

Người vào landing là người sắp quyết định. Không kể chuyện dài,
đặt bằng chứng cạnh nút mua. Áp đủ ràng buộc từ cấm.
```

| Thành phần khối | Nội dung của bạn |
|---|---|
| Tiêu đề khối | |
| Câu dẫn | |
| Bằng chứng 1 | |
| Bằng chứng 2 | |
| Bằng chứng 3 | |
| Bảng thông số | |
| Chữ trên nút | |

---

## Bước 7 · 3 kịch bản video (6 phút)

```
Viết 3 kịch bản video cho ngày [5, 10, 13], mỗi video 30 đến 60 giây,
quay bằng điện thoại, một người, không cần diễn viên.

Bảng 4 cột: Giây | Hình | Lời thoại | Chữ trên màn hình. Chia block 5 giây.
3 giây đầu phải nói được nỗi sợ. Lời kêu gọi ở 5 giây cuối kèm từ khóa.
3 video phải khác nhau về kiểu: 1 hướng dẫn, 1 đọc review thật,
1 kể một ngày dùng sản phẩm.
Áp đủ ràng buộc từ cấm. Được nói cách dùng theo thời gian,
không được hứa kết quả theo thời gian.
```

| Video | Ngày | Độ dài | Kiểu | Câu 3 giây đầu | Từ khóa lời kêu gọi |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |

---

## Bước 8 · Carousel 6 đến 8 slide (4 phút)

```
Viết carousel cho ngày 2, từ 6 đến 8 slide.
Mỗi slide: chữ trên slide (tối đa 12 từ) | mô tả hình.
Slide 1 phải làm người ta dừng lại. Slide cuối là lời kêu gọi.
Mỗi slide chỉ chở đúng một ý. Đọc lướt hết carousel trong 15 giây
vẫn hiểu được.
Áp đủ ràng buộc từ cấm.
```

| Slide | Chữ trên slide | Mô tả hình |
|---|---|---|
| 1 | | |
| 2 | | |
| 3 | | |
| 4 | | |
| 5 | | |
| 6 | | |
| 7 | | |
| 8 | | |

---

## Bước 9 · 5 brief hình ảnh (5 phút)

```
Viết 5 brief hình ảnh hoặc video cho 5 ngày: [chọn 5 ngày].

Mỗi brief đúng 6 mục:
1. Mục đích: người xem hiểu gì trong 1 giây
2. Bố cục
3. Chủ thể trong khung
4. Chữ trên ảnh, nguyên văn, tối đa 8 từ
5. Tỷ lệ khung và nơi đăng
6. Không được xuất hiện (viết cụ thể)

Viết sao cho người thiết kế chưa từng nghe tên thương hiệu này
vẫn làm ra được.
```

| Brief | Ngày | Mục đích 1 giây | Chữ trên ảnh | Tỷ lệ | Cấm xuất hiện |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |

---

## Bảng ràng buộc riêng của bạn

Điền bảng này **trước** bước 1. Nó là thứ quyết định agent có dùng được vào việc thật hay không.

| Loại ràng buộc | Của bạn |
|---|---|
| Từ cấm tuyệt đối (liệt kê hết) | |
| Cam kết bị cấm (thời gian, kết quả, hoàn tiền) | |
| Quy định ngành, ghi rõ tên văn bản nếu có | |
| Nội dung phải có nếu ngành yêu cầu (cảnh báo, mã số công bố) | |
| Cụm công dụng được phép nói, chép nguyên từ nhãn hoặc hồ sơ | |
| Không được so sánh với ai, nhắc tên ai | |
| Ai là người duyệt cuối trước khi đăng | |

Ngành có quy định chặt thì mở `../demo/buoi-04/skill-content-engine.md`, mục "Chỉnh cho ngành khác", có bảng từ cấm gợi ý cho 6 ngành.

---

## Chưa có insight thật thì làm gì

Dùng nguyên bộ Thảo An, vẫn nộp đủ 9 hạng mục. Chưa có tài khoản `tikhub` cũng vậy: bỏ phần tra xu hướng ở Bước 2, dùng thẳng bộ dữ liệu dưới đây, không mất điểm nào.

**Insight xương sống, copy dán được:**

```
Khách sợ bị kích ứng khi đổi sang sản phẩm chăm da mới. Nỗi sợ này mạnh
hơn mong muốn cải thiện da, nên nó chặn ở bước quyết định mua, không phải
bước biết đến sản phẩm.
```

**Bằng chứng [DATA THẬT], lấy từ `demo/thao-an/review-va-tin-nhan-khach.md`:**

- R11: "Trước mình dùng loại khác bị nổi mẩn, đổi qua đây thì ổn. Sẽ mua lại."
- M01: "Da mình nhạy cảm lắm, dùng cái này có bị rát không shop?"
- M02: "Sản phẩm này có cồn không ạ? Mình dị ứng cồn."
- M06: "Đang dùng của hãng khác, đổi qua có sao không?"
- R04: "Đọc thành phần thấy toàn cái đọc được, không có chất gì lạ."

**Persona:** nữ 28-34, nhân viên văn phòng, da nhạy cảm dễ đỏ rát, từng bị kích ứng nên sợ thử đồ mới. Muốn da dịu lại, bớt thâm mụn, không cần trắng nhanh. Tin review người thật, bảng thành phần rõ, đã test da liễu. Lướt Facebook buổi tối, hỏi kỹ qua inbox trước khi mua, thích chốt đơn trên Shopee.

**Kênh:** Facebook (bài + ads + inbox) đầu phễu tới chốt; Shopee cuối phễu chốt đơn và chứng thực; Website nền tin cậy, gắn UTM để đo nguồn.

**Mục tiêu:** 30 đơn trong 30 ngày, 100% đơn gắn được nguồn kênh. Chiến dịch 14 ngày này nằm ở tuần 2 và tuần 3, chỉ tiêu 15 đơn.

**Ràng buộc, copy vào bảng ràng buộc:** không dùng "trị mụn", "đặc trị", "khỏi hẳn", "trắng da cấp tốc"; không cam kết thời gian có kết quả; không nói là thuốc; không so sánh trực tiếp bằng tên với thương hiệu khác; không bịa thành phần hoặc công dụng ngoài hồ sơ; không gắn tên persona vào lời chứng thực.

---

## Checklist tự kiểm trước khi nộp

Chạy prompt này trước, rồi tự soi 10 ô bên dưới.

```
Rà lại toàn bộ nội dung đã viết trong chat này. Xuất bảng 3 cột:
câu vi phạm | vi phạm điều nào | câu thay thế.
Không có vi phạm thì ghi "không có", đừng bịa ra để có cái mà báo.
Sau đó đếm giúp tôi: bao nhiêu bài social, bao nhiêu email,
bao nhiêu video, bao nhiêu slide carousel, bao nhiêu brief hình ảnh.
```

- [ ] Lịch 14 ngày đủ 14 dòng, không ô nào trống.
- [ ] Nhịp đúng: 5 giáo dục, 4 bằng chứng, 3 xử lý phản đối, 2 ưu đãi. Ưu đãi ở ngày 7 và 14.
- [ ] Đủ số lượng: 10 bài social, 3 email, 3 video, 1 carousel 6-8 slide, 1 khối landing, 5 brief.
- [ ] Đọc lướt 3 bài bất kỳ, phân biệt được bài nào ra bài nào.
- [ ] Không bài nào chứa từ cấm hoặc cam kết thời gian có kết quả.
- [ ] Không có review, thành phần, con số nào bịa ra. Trích dẫn nào cũng chỉ được về nguồn.
- [ ] Không gắn tên persona vào lời chứng thực.
- [ ] Mỗi bài có ít nhất một chi tiết cụ thể lấy từ dữ liệu, không toàn tính từ.
- [ ] Mọi lời kêu gọi đều là hành động đo được, không có "tương tác" hay "tìm hiểu thêm".
- [ ] Chỉ vào một dòng bất kỳ, trả lời được: bài này đẩy khách đi bước nào, đo bằng gì, nối về mục tiêu bán hàng ra sao.

Đủ 10 ô thì nộp. Thiếu ô nào sửa ô đó, đừng nộp trước rồi bổ sung sau.

---

**Buổi sau dùng lại gì:** lịch 14 ngày ở Bước 3. Lưu nó thành file `lich-14-ngay.md` ngay trong thư mục làm việc, giữ nguyên dạng bảng, đúng thứ tự cột. Buổi 5 sẽ đọc thẳng từ file đó để nối vào luồng đăng bài tự động.
