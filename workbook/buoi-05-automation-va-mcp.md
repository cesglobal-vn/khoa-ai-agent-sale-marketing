# Buổi 5 · Workbook học viên

**Bạn có 65 phút.** Hết 65 phút phải có 5 thứ: automation map, bảng quản lý, một luồng chạy được hoặc prototype, mẫu thông báo, checklist rủi ro.

**Đọc câu này trước khi bắt đầu:** luồng của bạn không cần chạy mượt. Nó cần có chốt duyệt đúng chỗ và có chỗ ghi log. Luồng thô mà đủ hai thứ đó thì đạt. Luồng mượt mà agent tự đăng thì chưa đạt. Chưa nối được công cụ thật thì nhảy xuống mục 7, làm prototype, vẫn tính đạt.

**Hai quy định cứng của buổi hôm nay, đọc kỹ:**

1. **Chỉ nối kênh demo hoặc kênh cá nhân.** Hôm nay agent đăng bài THẬT lên kênh THẬT được. Tuyệt đối không nối fanpage công ty đang chạy. Muốn dùng kênh công ty thì làm sau buổi, sau khi xin phép người phụ trách trang. Nối nhầm là bài nộp chưa đạt, và phải gỡ tại chỗ.
2. **Duyệt xong thì hẹn giờ, không đăng ngay.** Hẹn giờ để còn kịp hủy nếu phát hiện sai. Đây là cách kiểm soát rủi ro thực tế nhất của buổi này.

**Phân bổ:** 0-7 chuẩn bị · 7-21 bước 1 và 2 · 21-39 bước 3 · 39-54 bước 4 và 5 · 54-65 bước 6 và nộp.

---

## Checklist chuẩn bị

Tick hết trước khi bắt đầu bước 1. Thiếu cái nào thì làm bù ngay, đừng bỏ qua.

- [ ] Mở được Claude Desktop, tab Code, trỏ vào thư mục làm việc của mình. Mở được một Google Sheet trống, hoặc Notion, hoặc Airtable
- [ ] Trong thư mục làm việc có đủ 5 thứ: `CLAUDE.md` và hồ sơ sản phẩm (buổi 1), `insight-khach-hang.md` (buổi 2), bảng chấm điểm lead (buổi 3), `lich-14-ngay.md` (buổi 4)
- [ ] Có ảnh minh họa đã chuẩn bị sẵn và logo file PNG nền trong, nếu định làm luồng post bài
- [ ] **Kênh đang nối là kênh demo hoặc kênh cá nhân, không phải fanpage công ty đang chạy.** Mở ra nhìn tên kênh một lần cho chắc
- [ ] Đã ghi ra giấy ít nhất 5 việc tuần nào cũng phải làm lại

Chưa có dữ liệu thật của mình thì dùng bộ Thảo An trong [../demo/thao-an/](../demo/thao-an/), vẫn hoàn thành đủ 5 sản phẩm.

---

## Bước 1 · Liệt kê việc lặp lại và chấm điểm (7 phút)

Mở Claude Desktop, tab Code, trỏ vào thư mục làm việc của bạn. Dán prompt này.

```
Bạn là Automation Orchestrator của [TÊN THƯƠNG HIỆU].

Dựa trên các file trong thư mục làm việc, liệt kê những việc lặp lại mà đội
Sale & Marketing đang phải làm bằng tay. Với mỗi việc, chấm 3 tiêu chí
theo mức Cao/Trung bình/Thấp: tần suất lặp; mức độ rõ ràng của quy tắc
(viết ra được "gặp A thì làm B" không); mức thiệt hại nếu làm sai.

Xếp thành 2 nhóm:
A. Nên tự động: lặp nhiều, quy tắc rõ, sai thì sửa được
B. KHÔNG nên tự động: có tiền trong đó, gửi thẳng ra ngoài, quy trình
   còn loạn, hoặc mỗi lần một khác

Ràng buộc: chỉ dùng dữ liệu có trong thư mục làm việc, không bịa nhân sự
hay số liệu; gắn nhãn [DATA THẬT] / [SUY LUẬN] từng dòng; thiếu dữ liệu
thì ghi "chưa đủ dữ liệu".
```

**Ô điền: 3 việc chọn để tự động, và 2 việc quyết định KHÔNG tự động**

| # | Việc | Tần suất | Quy tắc rõ? | Sai thì sao? | Tự động? |
|---|---|---|---|---|---|
| 1 |  |  |  |  | Có |
| 2 |  |  |  |  | Có |
| 3 |  |  |  |  | Có |
| 4 |  |  |  |  | Không, vì... |
| 5 |  |  |  |  | Không, vì... |

---

## Bước 2 · Vẽ automation map của bạn (7 phút)

Điền tay bảng dưới. Đây là sản phẩm nộp số 1.

**Quy tắc điền:** ô "Ai duyệt" phải là tên người, không ghi "trưởng phòng" hay "người phụ trách"; không có tên là không có ai duyệt. Ô "Ghi log ở đâu" phải là tên bảng hoặc tên sheet cụ thể. Luồng có bước gửi ra ngoài mà ô "Ai duyệt" trống thì luồng đó chưa dùng được.

| # | Kích hoạt | Xử lý (AI làm gì) | Đưa ra (kết quả đi đâu) | Ai duyệt | Ghi log ở đâu |
|---|---|---|---|---|---|
| 1 |  |  |  |  |  |
| 2 |  |  |  |  |  |
| 3 |  |  |  |  |  |
| 4 |  |  |  |  |  |

Muốn Claude gợi ý trước rồi bạn sửa lại thì dùng prompt này:

```
Lấy 3 việc tôi vừa chọn ở trên. Với mỗi việc, điền thành bảng 5 cột:
Kích hoạt | Xử lý | Đưa ra | Ai duyệt | Ghi log ở đâu

Yêu cầu: kích hoạt phải cụ thể (sự kiện gì, hoặc mấy giờ ngày nào);
xử lý chia thành các bước đánh số, mỗi bước một việc; chỉ rõ chốt
duyệt nằm giữa bước nào và bước nào; ô "Ai duyệt" để trống, ghi
"[điền tên người]" để tôi tự điền; đề xuất tên bảng log và cột cần có.
```

**Chọn 1 luồng để làm thật trong 44 phút còn lại.** Chọn luồng đơn giản nhất, đừng chọn luồng oai nhất. Luồng tôi chọn: ______________________

---

## Bước 3 · Dựng bảng quản lý (18 phút)

Sản phẩm nộp số 2. Dùng Google Sheet, Airtable hoặc Notion, cái nào bạn quen hơn.

```
Thiết kế cấu trúc bảng quản lý cho luồng [TÊN LUỒNG] của [TÊN THƯƠNG HIỆU].

Bắt buộc có: cột Trạng thái kèm sẵn các giá trị chọn được; cột Người
duyệt và Ngày duyệt; cột Nguồn kênh để tuần sau đo việc đến từ đâu;
cột Nháp cho agent để nội dung chờ duyệt; cột Kết quả để đối chiếu.

Trả về:
1. Bảng tên cột kèm 1 dòng giải thích cột đó đo cái gì
2. Ba dòng dữ liệu mẫu lấy từ file trong thư mục làm việc
3. Chỗ nào chưa có dữ liệu thì để trống và ghi "chưa đủ dữ liệu"
```

### Cột đề xuất cho bảng quản lý lead

| Cột | Dùng để làm gì |
|---|---|
| Mã lead, Ngày vào | Tra ngược nhanh, đo tốc độ phản hồi |
| Tên khách, Loại khách, Khu vực | Nhận diện và chia vùng cho sale |
| Nguồn kênh, Nhu cầu tóm tắt, Điểm lead | Form / inbox / Zalo / email; nhu cầu 1 dòng; điểm theo bảng buổi 3 |
| Nháp phản hồi | Agent ghi vào đây, chưa gửi |
| Trạng thái | Mới / Đang xử lý / Chờ duyệt / Đã gửi / Đã chốt / Không theo nữa |
| Người phụ trách, Người duyệt, Ngày duyệt | Trách nhiệm rõ, đo thời gian nằm chờ |
| Kết quả | Có đơn / Chưa / Từ chối, kèm lý do |

**Bảng log bài đăng:** dùng nguyên bảng trong [../tai-lieu-hoc-vien/buoi-05-luong-post-bai.md](../tai-lieu-hoc-vien/buoi-05-luong-post-bai.md). Tối thiểu phải có ngày đăng, mã bài, kênh, góc nội dung, link ảnh, người duyệt, giờ đăng, link bài, kết quả sau 7 ngày, ghi chú.

**Ô điền:** tên bảng ______________ · đường dẫn ______________

---

## Bước 4 · Chạy luồng (11 phút)

Làm luồng post bài thì theo đúng 6 bước trong [../tai-lieu-hoc-vien/buoi-05-luong-post-bai.md](../tai-lieu-hoc-vien/buoi-05-luong-post-bai.md). Dán chuỗi prompt này, chạy từng cái một, đừng dán cả cụm.

**4.0 Soát kênh trước khi bắt đầu.** Một câu, đừng bỏ.

```
Liệt kê các kênh tôi đang nối và giới hạn của từng nền tảng:
caption tối đa bao nhiêu ký tự, mấy ảnh, mấy video,
có bắt tiêu đề không và tiêu đề dài tối đa bao nhiêu.
```

Nhìn tên kênh nó trả về. **Đúng kênh demo hoặc kênh cá nhân của bạn thì đi tiếp. Nếu thấy tên fanpage công ty thì dừng lại, gỡ ra, nối lại kênh khác.**

**4.1 Lấy nội dung**

```
Mở lich-14-ngay.md trong thư mục làm việc. Lấy bài của Ngày [SỐ].
Cho tôi: góc nội dung, caption hoàn chỉnh đúng giọng văn trong CLAUDE.md,
và mô tả ảnh minh họa.

Ràng buộc: không dùng từ trong danh sách cấm ở CLAUDE.md,
không bịa thành phần hay công dụng, caption dưới 150 từ.
```

**4.2 Cắt caption cho vừa kênh, rồi soát ảnh.**

```
Tôi định đăng lên [TÊN KÊNH] trên [TÊN NỀN TẢNG].
Kiểm tra giới hạn của nền tảng đó rồi cắt caption cho vừa.
Nói rõ caption đang bao nhiêu ký tự, giới hạn kênh là bao nhiêu.
Kênh này có bắt tiêu đề không? Có thì viết tiêu đề luôn, đúng giới hạn.
Vượt giới hạn thì báo tôi, đừng tự đăng.
```

Ảnh thì bạn tự soát bằng mắt, ba điều: đúng tỷ lệ kênh (Facebook feed 1:1 hoặc 4:5, story 9:16); logo không đè lên sản phẩm hay mặt người; số ảnh không vượt giới hạn kênh (Twitter 4, Pinterest 1, Facebook và Instagram 10).

**4.3 Xin duyệt, KHÔNG bỏ bước này**

```
Dừng lại. Trình cho tôi duyệt, gồm: (1) caption đúng chữ sẽ đăng,
kèm số ký tự và giới hạn kênh; (2) ảnh cuối đã gắn logo, kèm tỷ lệ;
(3) tên kênh và giờ tôi muốn hẹn đăng; (4) tự soát: caption có từ cấm
nào không, có thông tin nào không tra được trong hồ sơ sản phẩm không,
bài này đã đăng hoặc đã nằm chờ chưa.

KHÔNG gọi bất kỳ công cụ đăng nào, kể cả công cụ hẹn giờ.
Chờ tôi trả lời "đồng ý đăng".
```

**4.4 Hẹn giờ đăng và ghi log.** Chú ý: hẹn giờ, không đăng ngay.

```
Đồng ý đăng. Tạo luồng đăng lên [TÊN KÊNH],
HẸN GIỜ sau [SỐ] phút nữa, không đăng ngay.
Cho tôi mã task để còn hủy được nếu cần.

Sau đó ghi một dòng vào bảng log: ngày, mã bài, nền tảng, kênh,
góc nội dung, link ảnh, người duyệt, giờ duyệt, hẹn giờ hay đăng ngay,
giờ đăng, mã task, link bài.
Người duyệt điền là: [TÊN BẠN]
```

**4.5 Thử phanh thứ hai.** Bắt buộc làm một lần cho biết, dù bài không sai.

```
Dời giờ đăng của task đó lùi thêm 30 phút.
```

```
Hủy task đó, và ghi lý do vào cột Ghi chú trong bảng log.
```

Chạy được hai câu này là bạn biết đường cứu một bài sai. Ai chưa thử thì đến lúc cần sẽ ngồi nhìn bài lên.

**Ô điền: nhật ký chạy thử**

| Bước | Chạy được? | Hỏng ở đâu và sửa thế nào |
|---|---|---|
| Soát kênh và giới hạn |  |  |
| Lấy nội dung |  |  |
| Cắt caption cho vừa kênh |  |  |
| Xin duyệt |  |  |
| Hẹn giờ đăng và ghi log |  |  |
| Dời giờ và hủy task |  |  |

---

## Bước 5 · Viết mẫu thông báo hoặc email (4 phút)

Sản phẩm nộp số 4. Người nhận đọc xong phải hành động được ngay, không phải đi tra thêm.

**Mẫu thông báo cho sale khi có lead mới:**

```
[LEAD MỚI - điểm {{điểm}}]
{{Tên cơ sở}} · {{Loại}} · {{Khu vực}}
Vào từ {{nguồn kênh}} lúc {{giờ}}. Nhu cầu: {{tóm tắt 1 dòng}}

Nháp phản hồi đã soạn sẵn: {{link dòng trong bảng}}
Việc của bạn: đọc nháp, sửa nếu cần, bấm gửi, trong {{số giờ}} giờ.
```

**Mẫu email nội bộ báo cáo tuần**

```
Tiêu đề: Báo cáo tuần {{tuần}} · nháp chờ duyệt

Số liệu tuần {{tuần}}, tất cả lấy từ bảng {{tên bảng}}:
- Lead mới: {{số}} ({{chia theo kênh}})
- Bài đã đăng: {{số}} trên {{số}} theo lịch
- Đơn gắn được nguồn: {{số}} · so với tuần trước: {{tăng/giảm}}

Chỗ thiếu dữ liệu: {{liệt kê thẳng, không ước lượng thay}}
Việc cần quyết tuần sau: {{liệt kê}}

Đây là bản nháp. Chưa gửi cho ai ngoài nhóm này.
```

**Ô điền:** dán mẫu bạn viết vào file nộp. Kiểm một câu: người nhận đọc xong có biết phải làm gì tiếp không.

## Bước 6 · Checklist kiểm soát rủi ro (7 phút)

Sản phẩm nộp số 5. Điền cụ thể vào luồng của bạn, không chép nguyên bảng này.

| # | Rủi ro | Có xảy ra với luồng của tôi không | Cách chặn | Ai chịu trách nhiệm |
|---|---|---|---|---|
| 1 | Agent gửi ra ngoài mà không ai duyệt |  |  |  |
| 2 | Nội dung chứa từ cấm của ngành |  |  |  |
| 3 | Agent bịa số liệu, giá, tên khách |  |  |  |
| 4 | Đăng nhầm kênh, hoặc đăng trùng bài |  |  |  |
| 5 | Caption vượt giới hạn ký tự, hoặc thiếu tiêu đề kênh bắt buộc |  |  |  |
| 6 | Ảnh sai tỷ lệ, sai số lượng, bị cắt mất nội dung |  |  |  |
| 7 | **Đang nối kênh thật của công ty thay vì kênh demo** |  |  |  |
| 8 | **Duyệt xong đăng ngay, không còn cửa sổ để hủy** |  |  |  |
| 9 | **Học xong để nguyên quyền, không gỡ kết nối** |  |  |  |
| 10 | Công cụ hỏng giữa chừng, không ai biết |  |  |  |
| 11 | Kết nối được cấp quyền rộng hơn mức cần |  |  |  |
| 12 | Không ghi log, hoặc người duyệt nghỉ không ai thay |  |  |  |

Ba dòng in đậm là dòng riêng của buổi 5, vì đây là buổi agent chạm ra ngoài thật. Không được để trống.

**Bốn câu bắt buộc trả lời được:** luồng hỏng thì bao lâu tôi biết ____ ; hỏng thì làm tay theo bước nào ____ ; ai kiểm tra luồng, mấy ngày một lần ____ ; bài đã hẹn giờ mà phát hiện sai thì tôi gõ câu gì để hủy ____

**Gỡ quyền sau buổi học.** Không dùng tiếp thì gỡ, đừng để kết nối nằm đó. Hai chỗ, làm cả hai mới sạch:

1. Trong Claude Desktop: Settings, mục Connectors, tìm kết nối aitoearn, bấm ngắt kết nối.
2. Trên chính nền tảng (Facebook, TikTok, LinkedIn...): vào phần ứng dụng đã cấp quyền trong cài đặt tài khoản, gỡ ứng dụng ra. Bước này quan trọng hơn, vì ngắt ở Claude không thu hồi quyền đã cấp trên nền tảng.

*Giao diện hai chỗ này có thể đổi theo phiên bản. Không thấy đúng như mô tả thì hỏi giảng viên, đừng bỏ qua.*

---

## 7 · Chưa nối được công cụ thật thì làm gì

Không có quyền fanpage, chưa mở được Make hay Zapier, công ty chưa cho nối API. Chuyện bình thường. **Làm prototype vẫn tính là đạt.** Chọn một trong hai cách.

**Cách 1 · Prototype trên giấy.** Vẽ luồng ra giấy hoặc slide, đủ 6 ô, mỗi ô ghi ai làm hoặc công cụ nào, đầu vào là gì, đầu ra là gì. Chụp ảnh nộp.

```
[Kích hoạt] -> [Bước 1] -> [Bước 2] -> [CHỐT DUYỆT] -> [Đưa ra] -> [Ghi log]
```

**Cách 2 · Chạy tay từng bước.** Điểm cao hơn, vì cuối cùng bạn có sản phẩm thật. Chạy từng prompt ở bước 4 một cách thủ công; lưu kết quả mỗi bước thành file trong thư mục làm việc; đến bước duyệt thì tự đọc và tự tick vào ô duyệt trong bảng; tự đăng bằng tay, hoặc chụp màn hình nội dung đã sẵn sàng nếu không được đăng; tự điền dòng log. Ghép ảnh chụp từng bước vào một file, đó là bài nộp.

Chưa nối được kênh thì vẫn hỏi Claude giới hạn của nền tảng bạn định đăng, và vẫn cắt caption cho vừa. Đó là phần học được mà không cần quyền gì cả.

**Nói thẳng:** luồng chạy tay đủ 6 bước có giá trị hơn luồng tự động thiếu bước duyệt. Cái bạn học ở buổi này là thiết kế luồng, không phải là bấm nút trên Make.

---

## Checklist tự kiểm trước khi nộp

Tick hết mới nộp. Còn ô trống thì sửa, đừng nộp trước rồi sửa sau.

**Đủ 5 sản phẩm**

- [ ] Automation map có ít nhất 3 luồng, điền đủ 5 cột
- [ ] Bảng quản lý đã dựng thật, có link mở được
- [ ] Có 1 automation chạy được, hoặc prototype có ảnh chụp từng bước
- [ ] Có 1 mẫu thông báo hoặc email, và 1 checklist rủi ro đã điền

**Chốt duyệt**

- [ ] Mọi luồng có bước gửi ra ngoài đều có chốt duyệt trước bước đó, kể cả trước bước hẹn giờ
- [ ] Ô "Ai duyệt" ghi tên người thật, không ghi chức danh chung chung
- [ ] Bảng quản lý có cột Người duyệt và cột Ngày duyệt
- [ ] Tôi chỉ được ra bước nào trong luồng là bước có người dừng lại đọc

**An toàn của buổi 5**

- [ ] Kênh tôi đang nối là kênh demo hoặc kênh cá nhân, không phải fanpage công ty đang chạy
- [ ] Luồng của tôi mặc định hẹn giờ, không đăng ngay
- [ ] Tôi đã thử một lần dời giờ và một lần hủy bài đã hẹn, và biết gõ câu gì để làm việc đó
- [ ] Tôi biết gỡ quyền ở cả hai chỗ: trong Claude Desktop và trên chính nền tảng

**Chống bịa và đo được**

- [ ] Dữ liệu có gắn nhãn `[DATA THẬT]` / `[SUY LUẬN]` ở phần suy ra
- [ ] Có ít nhất một chỗ ghi "chưa đủ dữ liệu", không điền bừa cho đầy
- [ ] Đã dò ngược 3 dòng bất kỳ về file gốc và cả 3 đều có thật
- [ ] Có bảng log tối thiểu 6 cột, cột tôi định đo đang có dữ liệu chảy vào
- [ ] Trả lời được 4 câu ở cuối bước 6
- [ ] Map đã lưu thành file `automation-map.md` trong thư mục làm việc, buổi 6 dùng lại

---

CES Global · Creative, Effective, Sustainable
