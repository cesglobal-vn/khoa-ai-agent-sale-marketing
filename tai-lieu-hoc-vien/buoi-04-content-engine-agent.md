# Tài liệu học viên · Buổi 4: Content Engine Agent

**Khóa:** AI Agent cho Sale & Marketing · CES Global
**Buổi:** 4 trên 6 · 150 phút · **Ngày học:** ______

Đây là bản mang về để tra và làm lại. Bản làm trong lớp là [../workbook/buoi-04-content-engine-agent.md](../workbook/buoi-04-content-engine-agent.md).

---

## 1. Buổi này anh chị đã làm gì

Hôm nay anh chị lấy **một** insight và bẻ nó thành nguyên một chiến dịch 14 ngày.

- Cài skill `content-engine` vào thư mục làm việc, khai ràng buộc ngành **trước khi** agent viết chữ đầu tiên.
- Ra campaign brief 8 mục, rồi lịch 14 ngày theo nhịp 5 giáo dục, 4 bằng chứng, 3 xử lý phản đối, 2 ưu đãi. Hai ngày ưu đãi đặt ở ngày 7 và ngày 14.
- Sản xuất 10 bài social, 3 email nurturing, 1 khối landing page, 3 kịch bản video, 1 carousel, 5 brief hình ảnh.
- Content Engine lo phần **chiến dịch**; skill `viet-bai-ban-hang` của buổi 1 lo phần **viết từng bài**. Tới bước viết caption, Content Engine gọi lại skill kia chứ không viết từ đầu, nhờ vậy giọng văn và danh sách từ cấm buổi 1 vẫn có hiệu lực.

Dòng chảy phải nhớ: **biết, tin, hỏi, mua**. Ngày giáo dục làm khách biết. Ngày bằng chứng làm khách tin. Ngày xử lý phản đối làm khách hỏi. Ngày ưu đãi làm khách mua. Bài nào không nằm được vào một trong bốn ô này là bài thừa.

---

## 2. Bộ prompt copy dùng ngay

Nội dung skill copy từ [../demo/buoi-04/skill-content-engine.md](../demo/buoi-04/skill-content-engine.md). Sửa 4 chỗ trước khi dán: dòng `description`, tên thương hiệu, danh sách từ cấm của ngành mình, danh sách công dụng được phép nói.

### NHÓM A · Cài và kiểm skill

**A1. Tạo file skill Content Engine**

```
Tạo file .claude/skills/content-engine/SKILL.md trong thư mục làm việc này,
tạo luôn thư mục cha nếu chưa có. Nội dung như sau: [dán khối đã sửa]
```

**A2. Kiểm skill có được gọi ra không**

Mở **phiên mới**, gõ một câu tự nhiên, **không** nhắc tên skill.

```
Dựng cho tôi chiến dịch nội dung 14 ngày cho [sản phẩm của bạn].
Liệt kê giúp tôi cần cấp những gì trước khi viết, đừng viết nội dung vội.
```

Dùng khi: vừa cài xong skill. Đúng là Claude báo đang dùng skill `content-engine` và hỏi lại đầu vào còn thiếu. Không gọi skill thì lỗi ở dòng `description`. Gọi rồi mà viết bài ngay thì phần "Quy trình làm việc" trong file bị đặt sai chỗ.

### NHÓM B · Tra xu hướng bằng tikhub (bỏ qua nếu chưa có tài khoản)

Ba công cụ dùng ở đây: `tiktok_app_v3_fetch_hashtag_detail`, `tiktok_app_v3_fetch_hashtag_video_list`, `tiktok_ads_search_ads`. **Mỗi lượt gọi tính tiền vào tài khoản của anh chị.**

**B1. Lưu ngay kết quả tra được**

```
Lưu kết quả vừa lấy được thành file xu-huong-hashtag.md trong thư mục làm việc.
Ghi rõ ngày lấy, hashtag nào, và 5 góc nội dung đang bị lặp nhiều nhất.
Chỉ lấy nội dung công khai, không ghi lại tên hay thông tin cá nhân của ai.
```

Dùng khi: ngay sau khi gọi công cụ. Lần sau đọc lại file này, đừng gọi lại. Tra để biết góc nào đã bão hòa mà **tránh**, không phải để bắt chước. Insight xương sống vẫn lấy từ dữ liệu khách của anh chị.

### NHÓM C · Campaign brief và lịch 14 ngày

**C1. Campaign brief 8 mục**

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

Dùng khi: mở một chiến dịch mới. Dừng lại đọc to 5 lõi: chúng khác nhau thật hay chỉ khác chữ. Giống nhau thì sửa ngay, đừng viết tiếp.

**C2. Lịch nội dung 14 ngày**

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

Dùng khi: đã có brief. Lưu bảng này thành `lich-14-ngay.md` ngay trong thư mục làm việc, buổi 5 đọc thẳng từ file đó.

### NHÓM D · Sản xuất nội dung

**D1. Mười bài social, chia hai lượt mỗi lượt 5 bài**

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

Dùng khi: đã có lịch. Xin 10 bài một lượt là ra 10 bài giống nhau.

**D2. Ba email nurturing**

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

**D3. Khối landing page**

```
Viết 1 khối landing page cho ngày 12, tiêu đề khối hướng tới người
đang sợ [nỗi sợ chính của bạn].

Gồm: tiêu đề khối | 1 câu dẫn | 3 gạch đầu dòng bằng chứng
(mỗi gạch phải kiểm chứng được, không phải lời khen) |
1 bảng thành phần hoặc thông số | 1 nút bấm với chữ trên nút.

Người vào landing là người sắp quyết định. Không kể chuyện dài,
đặt bằng chứng cạnh nút mua. Áp đủ ràng buộc từ cấm.
```

**D4. Ba kịch bản video 30 tới 60 giây**

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

**D5. Carousel 6 tới 8 slide**

```
Viết carousel cho ngày 2, từ 6 đến 8 slide.
Mỗi slide: chữ trên slide (tối đa 12 từ) | mô tả hình.
Slide 1 phải làm người ta dừng lại. Slide cuối là lời kêu gọi.
Mỗi slide chỉ chở đúng một ý. Đọc lướt hết carousel trong 15 giây
vẫn hiểu được.
Áp đủ ràng buộc từ cấm.
```

**D6. Năm brief hình ảnh**

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

### NHÓM E · Rà soát trước khi nộp hoặc đăng

**E1. Rà vi phạm và đếm sản lượng**

```
Rà lại toàn bộ nội dung đã viết trong chat này. Xuất bảng 3 cột:
câu vi phạm | vi phạm điều nào | câu thay thế.
Không có vi phạm thì ghi "không có", đừng bịa ra để có cái mà báo.
Sau đó đếm giúp tôi: bao nhiêu bài social, bao nhiêu email,
bao nhiêu video, bao nhiêu slide carousel, bao nhiêu brief hình ảnh.
```

Dùng khi: cuối mỗi đợt sản xuất nội dung. Agent trả về "không có câu nào" mà mắt thường vẫn thấy vi phạm, tức là khối ràng buộc chưa nằm đúng chỗ: đưa nó lên **đầu** file skill, ngay sau frontmatter.

---

## 3. Sản phẩm buổi 4 anh chị phải có trên máy

| # | Sản phẩm | Nằm ở đâu |
|---|---|---|
| 1 | Skill Content Engine đã chỉnh cho ngành của mình | `.claude/skills/content-engine/SKILL.md` |
| 2 | Campaign brief 8 mục | Trong thư mục làm việc |
| 3 | `lich-14-ngay.md`: bảng 14 dòng, 8 cột, không ô nào trống | Ngay trong thư mục làm việc. **Buổi 5 đọc thẳng từ file này** |
| 4 | 10 bài social, trong đó 1 là carousel | Trong thư mục làm việc |
| 5 | 3 email nurturing, 1 khối landing page, 3 kịch bản video | Trong thư mục làm việc |
| 6 | Carousel 6 tới 8 slide và 5 brief hình ảnh | Trong thư mục làm việc |
| 7 | `xu-huong-hashtag.md`, chỉ ai dùng tikhub | Trong thư mục làm việc |

Giới hạn caption từng kênh để đối chiếu nhanh: Facebook 63.206 · TikTok 2.200 · Instagram 2.200 · LinkedIn 3.000 · YouTube 5.000 (tiêu đề 100) · Twitter 280 · Threads 500 · Pinterest 800. Muốn số cập nhật thì gọi `listChannelPlatforms` của MCP `aitoearn`.

---

## 4. Checklist tự kiểm

- [ ] Lịch 14 ngày đủ 14 dòng, không ô nào trống
- [ ] Nhịp đúng: 5 giáo dục, 4 bằng chứng, 3 xử lý phản đối, 2 ưu đãi. Ưu đãi ở ngày 7 và ngày 14
- [ ] Đủ số lượng: 10 bài social, 3 email, 3 video, 1 carousel 6 tới 8 slide, 1 khối landing, 5 brief
- [ ] Đọc lướt 3 bài bất kỳ, phân biệt được bài nào ra bài nào
- [ ] Không bài nào chứa từ cấm hoặc cam kết thời gian có kết quả
- [ ] Không có review, thành phần, con số nào bịa ra. Trích dẫn nào cũng chỉ được về nguồn
- [ ] **Không gắn tên persona vào lời chứng thực.** Persona là chân dung suy ra, không phải khách có thật. Muốn trích lời khách thì trích nguyên văn ID trong `insight-khach-hang.md`
- [ ] Mỗi bài có ít nhất một chi tiết cụ thể lấy từ dữ liệu, không toàn tính từ
- [ ] Mọi lời kêu gọi đều là hành động đo được, không có "tương tác" hay "tìm hiểu thêm"
- [ ] Chỉ vào một dòng bất kỳ, trả lời được: bài này đẩy khách đi bước nào, đo bằng gì, nối về mục tiêu bán hàng ra sao
- [ ] Đã lưu `lich-14-ngay.md` vào thư mục làm việc, giữ nguyên dạng bảng và đúng thứ tự cột

---

## 5. Việc làm ở nhà trước buổi 5

| # | Việc | Nộp gì | Hạn |
|---|---|---|---|
| 1 | Chạy thật 3 ngày đầu của lịch 14 ngày trên kênh của mình. Ghi lại số liệu từng bài | Bảng 3 dòng: ngày, bài, kênh, kết quả sau 48 giờ | Trước buổi 5 |
| 2 | Điền xong Bảng ràng buộc của ngành mình nếu buổi học còn để trống: từ cấm, cam kết bị cấm, quy định ngành, cụm công dụng được phép nói, ai duyệt cuối | Bảng ràng buộc đã điền, dán vào đầu file skill | Trước buổi 5 |
| 3 | **Lập một kênh demo hoặc dùng kênh cá nhân** để buổi 5 đăng bài thật. Tuyệt đối không dùng fanpage công ty đang chạy | Tên kênh, mở ra nhìn một lần cho chắc | Trước buổi 5 |
| 4 | **Đăng ký tài khoản aitoearn và nối sẵn kênh demo đó.** Trong buổi 5 không đủ thời gian đăng ký và duyệt quyền | Ảnh chụp màn hình kênh đã nối | Trước buổi 5 |
| 5 | Chuẩn bị ảnh minh họa và **logo file PNG nền trong**, để buổi 5 chạy trọn luồng post bài | Thư mục ảnh, tối thiểu 3 ảnh | Trước buổi 5 |
| 6 | Ghi ra giấy ít nhất 5 việc tuần nào cũng phải làm lại. Càng chán càng tốt | Danh sách 5 dòng, mang vào buổi 5 | Trước buổi 5 |

---

## 6. Năm lỗi hay gặp khi làm lại ở nhà

| Lỗi | Dấu hiệu anh chị thấy | Cách xử lý |
|---|---|---|
| Mười bài ra giống hệt nhau | Bài nào cũng mở bằng câu hỏi, cũng kể một khách, cũng kết bằng "inbox ngay" | Nguyên nhân là xin 10 bài trong một lượt. Khai 5 lõi khác nhau trước, mỗi lõi một nỗi đau riêng, rồi chia hai lượt, mỗi lượt 5 bài |
| Giọng văn nhạt như thông cáo báo chí | Nhiều tính từ, ít chi tiết: "sản phẩm chất lượng cao, an toàn cho làn da của bạn" | Kiểm hai chỗ: đang làm việc đúng thư mục có `CLAUDE.md` chưa, và Content Engine có gọi lại skill `viet-bai-ban-hang` không. Nó viết thẳng bằng giọng chung chung là dấu hiệu skill buổi 1 không được đọc |
| Agent hứa quá lời | Xuất hiện "hết thâm", "sau 7 ngày", "đặc trị", "cam kết hiệu quả" | Đưa khối ràng buộc lên **đầu** file skill, ngay sau frontmatter, rồi chạy prompt E1. Ràng buộc để cuối prompt là bị chìm |
| Lịch 14 ngày ra 14 dòng cùng một loại | Mở bảng ra thấy 14 dòng đều là bán hàng, hoặc đều là chia sẻ kiến thức | Bắt agent tự đếm cuối bảng: giáo dục mấy ngày, bằng chứng mấy ngày, phản đối mấy ngày, ưu đãi mấy ngày. Lệch tỷ lệ 5/4/3/2 quá xa thì bắt xếp lại |
| Brief hình ảnh chung chung, người thiết kế không làm được | "Ảnh sản phẩm đẹp, nền sáng, cảm giác tự nhiên" | Brief phải đủ 6 mục, trong đó có chữ trên ảnh viết nguyên văn, tỷ lệ khung, và mục "không được xuất hiện". Phép thử: đưa cho người chưa biết gì về sản phẩm, họ vẫn làm ra được |

---

CES Global · Creative, Effective, Sustainable
