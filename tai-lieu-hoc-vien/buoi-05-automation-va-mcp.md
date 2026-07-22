# Tài liệu học viên · Buổi 5: Automation và MCP

**Khóa:** AI Agent cho Sale & Marketing · CES Global
**Buổi:** 5 trên 6 · 150 phút · **Ngày học:** ______

Đây là bản mang về để tra và làm lại. Bản làm trong lớp là [../workbook/buoi-05-automation-va-mcp.md](../workbook/buoi-05-automation-va-mcp.md). Đặc tả đầy đủ của luồng post bài nằm ở [buoi-05-luong-post-bai.md](buoi-05-luong-post-bai.md), giữ file đó bên cạnh khi làm lại.

---

## 1. Buổi này anh chị đã làm gì

Hôm nay anh chị nối các việc lặp lại thành luồng tự chạy, và lần đầu tiên agent chạm ra bên ngoài thật.

- Liệt kê việc lặp lại, chấm theo 3 tiêu chí, tách rõ nhóm **nên tự động** và nhóm **không nên tự động**.
- Vẽ automation map 5 cột: kích hoạt, xử lý, đưa ra, ai duyệt, ghi log ở đâu.
- Dựng bảng quản lý trên Google Sheet, Airtable hoặc Notion, có cột trạng thái và cột người duyệt.
- Chạy trọn luồng post bài: lấy caption từ `lich-14-ngay.md`, soát giới hạn kênh, chuẩn bị ảnh, **dừng lại cho người duyệt**, rồi mới hẹn giờ đăng.
- Viết mẫu thông báo và checklist kiểm soát rủi ro.

**Buổi 1 chỉ cho Claude quyền đọc. Buổi 5 mở thêm hai quyền nặng hơn hẳn: ghi vào bảng, và gửi ra ngoài.** Đọc nhầm thì đọc lại. Ghi đè thì còn khôi phục được nếu có bản sao. Bài đã lên kênh thì có người đọc, có người chụp màn hình, không rút lại được.

**Lớp thứ ba của luồng có hai phanh, không phải một.** Phanh 1 là người duyệt. Phanh 2 là cửa sổ giữa lúc hẹn giờ và lúc bài lên. Hẹn giờ không phải để bài lên đúng khung giờ vàng; hẹn giờ là để còn kịp hủy.

---

## 2. Bộ prompt copy dùng ngay

### NHÓM A · Chọn việc và vẽ map

**A1. Liệt kê việc lặp lại và chấm điểm**

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

Dùng khi: đầu mỗi quý, hoặc khi thấy đội đang copy dữ liệu từ chỗ này sang chỗ kia quá 3 lần một tuần.

**A2. Điền automation map 5 cột**

```
Lấy 3 việc tôi vừa chọn ở trên. Với mỗi việc, điền thành bảng 5 cột:
Kích hoạt | Xử lý | Đưa ra | Ai duyệt | Ghi log ở đâu

Yêu cầu: kích hoạt phải cụ thể (sự kiện gì, hoặc mấy giờ ngày nào);
xử lý chia thành các bước đánh số, mỗi bước một việc; chỉ rõ chốt
duyệt nằm giữa bước nào và bước nào; ô "Ai duyệt" để trống, ghi
"[điền tên người]" để tôi tự điền; đề xuất tên bảng log và cột cần có.
```

Dùng khi: đã chọn được 3 việc. **Ô "Ai duyệt" phải là tên người, không ghi "trưởng phòng" hay "người phụ trách".** Không có tên là không có ai duyệt.

**A3. Thiết kế bảng quản lý**

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

Dùng khi: bắt đầu một luồng mới. Không có bảng log thì tuần sau không đo được gì.

### NHÓM B · Luồng post bài, chạy từng câu một

Đừng dán cả cụm. Chạy từng prompt, đọc kết quả rồi mới sang câu tiếp.

**B0. Soát kênh trước khi bắt đầu**

```
Liệt kê các kênh tôi đang nối và giới hạn của từng nền tảng:
caption tối đa bao nhiêu ký tự, mấy ảnh, mấy video,
có bắt tiêu đề không và tiêu đề dài tối đa bao nhiêu.
```

Dùng khi: mọi lần, trước mọi bài. Nhìn tên kênh nó trả về. Thấy tên fanpage công ty thì dừng lại, gỡ ra, nối lại kênh khác.

**B1. Lấy nội dung của một ngày trong lịch**

```
Mở lich-14-ngay.md trong thư mục làm việc. Lấy bài của Ngày [SỐ].
Cho tôi: góc nội dung, caption hoàn chỉnh đúng giọng văn trong CLAUDE.md,
và mô tả ảnh minh họa.

Ràng buộc: không dùng từ trong danh sách cấm ở CLAUDE.md,
không bịa thành phần hay công dụng, caption dưới 150 từ.
```

**B2. Cắt caption cho vừa kênh**

```
Tôi định đăng lên [TÊN KÊNH] trên [TÊN NỀN TẢNG].
Kiểm tra giới hạn của nền tảng đó rồi cắt caption cho vừa.
Nói rõ caption đang bao nhiêu ký tự, giới hạn kênh là bao nhiêu.
Kênh này có bắt tiêu đề không? Có thì viết tiêu đề luôn, đúng giới hạn.
Vượt giới hạn thì báo tôi, đừng tự đăng.
```

Ảnh thì anh chị tự soát bằng mắt, ba điều: đúng tỷ lệ kênh (Facebook feed 1:1 hoặc 4:5, story 9:16); logo không đè lên sản phẩm hay mặt người; số ảnh không vượt giới hạn kênh (Pinterest 1, Twitter 4, Facebook và Instagram 10).

**B3. Xin duyệt, KHÔNG bỏ bước này**

```
Dừng lại. Trình cho tôi duyệt, gồm: (1) caption đúng chữ sẽ đăng,
kèm số ký tự và giới hạn kênh; (2) ảnh cuối đã gắn logo, kèm tỷ lệ;
(3) tên kênh và giờ tôi muốn hẹn đăng; (4) tự soát: caption có từ cấm
nào không, có thông tin nào không tra được trong hồ sơ sản phẩm không,
bài này đã đăng hoặc đã nằm chờ chưa.

KHÔNG gọi bất kỳ công cụ đăng nào, kể cả công cụ hẹn giờ.
Chờ tôi trả lời "đồng ý đăng".
```

Dùng khi: mọi bài, mọi kênh, mọi lúc. **Hẹn giờ cũng tính là gửi ra ngoài**, nên duyệt phải đứng trước cả công cụ tạo luồng hẹn giờ.

**B4. Hẹn giờ đăng và ghi log**

```
Đồng ý đăng. Tạo luồng đăng lên [TÊN KÊNH],
HẸN GIỜ sau [SỐ] phút nữa, không đăng ngay.
Cho tôi mã task để còn hủy được nếu cần.

Sau đó ghi một dòng vào bảng log: ngày, mã bài, nền tảng, kênh,
góc nội dung, link ảnh, người duyệt, giờ duyệt, hẹn giờ hay đăng ngay,
giờ đăng, mã task, link bài.
Người duyệt điền là: [TÊN BẠN]
```

Dùng khi: sau khi đã đọc và đồng ý. Luật đề xuất: hẹn tối thiểu 15 phút.

**B5. Hai câu cứu bài, tập một lần cho quen tay**

```
Dời giờ đăng của task đó lùi thêm 30 phút.
```

```
Hủy task đó, và ghi lý do vào cột Ghi chú trong bảng log.
```

Dùng khi: đã duyệt xong mới phát hiện sai tên khách, sai giá, sai chính tả. Ai chưa thử thì đến lúc cần sẽ ngồi nhìn bài lên. Quá giờ đăng thì không hủy được nữa, phải vào tận kênh gỡ tay.

### NHÓM C · Hai mẫu thông báo, sửa lại theo đội của mình

**C1. Thông báo cho sale khi có lead mới**

```
[LEAD MỚI - điểm {{điểm}}]
{{Tên cơ sở}} · {{Loại}} · {{Khu vực}}
Vào từ {{nguồn kênh}} lúc {{giờ}}. Nhu cầu: {{tóm tắt 1 dòng}}

Nháp phản hồi đã soạn sẵn: {{link dòng trong bảng}}
Việc của bạn: đọc nháp, sửa nếu cần, bấm gửi, trong {{số giờ}} giờ.
```

**C2. Email nội bộ báo cáo tuần**

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

Phép thử cho cả hai mẫu: người nhận đọc xong có biết phải làm gì tiếp không. Không biết thì viết lại.

---

## 3. Sản phẩm buổi 5 anh chị phải có

| # | Sản phẩm | Nằm ở đâu |
|---|---|---|
| 1 | `automation-map.md`: bảng 5 cột, tối thiểu 3 luồng | Ngay trong thư mục làm việc. **Buổi 6 dùng lại** |
| 2 | Bảng quản lý trên Sheet, Airtable hoặc Notion, có link mở được | Ngoài máy, ghi link vào `automation-map.md` |
| 3 | 1 automation chạy được, hoặc prototype có ảnh chụp từng bước | Thư mục làm việc |
| 4 | Bảng log bài đăng, tối thiểu 6 cột | Cùng chỗ với bảng quản lý |
| 5 | 1 mẫu thông báo hoặc email nội bộ | Thư mục làm việc |
| 6 | 1 checklist kiểm soát rủi ro đã điền theo luồng của mình | Thư mục làm việc |

**Chưa nối được công cụ thật vẫn tính là đạt.** Chọn một trong hai: vẽ luồng ra giấy đủ 6 ô rồi chụp ảnh; hoặc chạy tay từng bước ở nhóm B, lưu kết quả mỗi bước thành file, tự tick ô duyệt, tự điền dòng log. Luồng chạy tay đủ 6 bước có giá trị hơn luồng tự động thiếu bước duyệt.

---

## 4. Checklist tự kiểm

**Đủ sản phẩm**

- [ ] Automation map có ít nhất 3 luồng, điền đủ 5 cột
- [ ] Bảng quản lý đã dựng thật, có link mở được, có cột Trạng thái và cột Người duyệt
- [ ] Có 1 automation chạy được, hoặc prototype có ảnh chụp từng bước
- [ ] Có 1 mẫu thông báo và 1 checklist rủi ro đã điền

**Chốt duyệt**

- [ ] Mọi luồng có bước gửi ra ngoài đều có chốt duyệt trước bước đó, kể cả trước bước hẹn giờ
- [ ] Ô "Ai duyệt" ghi tên người thật, không ghi chức danh chung chung
- [ ] Tôi chỉ được ra bước nào trong luồng là bước có người dừng lại đọc

**An toàn riêng của buổi 5**

- [ ] Kênh tôi đang nối là kênh demo hoặc kênh cá nhân, **không phải fanpage công ty đang chạy**
- [ ] Luồng của tôi mặc định hẹn giờ, không đăng ngay
- [ ] Tôi đã thử một lần dời giờ và một lần hủy bài đã hẹn, và biết gõ câu gì để làm việc đó
- [ ] Tôi biết gỡ quyền ở cả hai chỗ: Settings > Connectors của Claude Desktop, **và** phần ứng dụng đã cấp quyền trên chính nền tảng

**Chống bịa và đo được**

- [ ] Dữ liệu có gắn nhãn `[DATA THẬT]` và `[SUY LUẬN]` ở phần suy ra
- [ ] Có ít nhất một chỗ ghi "chưa đủ dữ liệu", không điền bừa cho đầy
- [ ] Đã dò ngược 3 dòng bất kỳ về file gốc và cả 3 đều có thật
- [ ] Trả lời được 4 câu: luồng hỏng thì bao lâu tôi biết; hỏng thì làm tay theo bước nào; ai kiểm tra luồng và mấy ngày một lần; bài đã hẹn giờ mà phát hiện sai thì tôi gõ câu gì để hủy
- [ ] Đã lưu map thành `automation-map.md` trong thư mục làm việc

---

## 5. Việc làm ở nhà trước buổi 6

| # | Việc | Nộp gì | Hạn |
|---|---|---|---|
| 1 | Chạy luồng post bài thật thêm 3 lần trong tuần, trên kênh demo. Ghi đủ 3 dòng log | Bảng log 3 dòng, có cột người duyệt và cột hẹn giờ hay đăng ngay | Trước buổi 6 |
| 2 | **Gỡ quyền nếu không dùng tiếp**, ở cả hai chỗ. Ngắt ở Claude không thu hồi quyền đã cấp trên nền tảng | Ảnh chụp hai màn hình đã gỡ | Ngay tối nay |
| 3 | Điền nốt checklist rủi ro cho 3 dòng bắt buộc: kênh đang nối là kênh gì; duyệt xong có hẹn giờ không; học xong có gỡ quyền không | Checklist đã điền đủ | Trước buổi 6 |
| 4 | Nhìn cột "Hẹn giờ hay đăng ngay" trong log sau một tuần. Đăng ngay nhiều là dấu hiệu đội đang chạy ẩu | Một dòng nhận xét | Trước buổi 6 |
| 5 | **Chuẩn bị cho buổi 6:** mở lại đủ tài sản của cả 5 buổi trong thư mục làm việc. Thiếu buổi nào thì tối nay chạy lại prompt buổi đó | Đối chiếu theo [checklist-toan-khoa.md](checklist-toan-khoa.md), đánh dấu chỗ thiếu | Trước buổi 6 |
| 6 | **Chuẩn bị cho buổi 6:** tạo một thư mục trống trên máy, đặt tên `<ten-thuong-hieu>-ai-system` | Thư mục đã tạo | Trước buổi 6 |

Buổi 6 không tạo dữ liệu mới, nó gom cái đã có. Thiếu đầu vào là ngồi làm lại và mất thời gian của cả lớp.

---

## 6. Năm lỗi hay gặp khi làm lại ở nhà

| Lỗi | Dấu hiệu anh chị thấy | Cách xử lý |
|---|---|---|
| Tự động hóa quá sớm, khi quy trình còn loạn | Muốn nối form vào CRM mà chưa rõ ai nhận lead, xử lý trong bao lâu | Viết quy trình bằng tay trước, đúng 5 dòng: ai nhận, làm gì, trong bao lâu, chuyển cho ai, ghi vào đâu. Không viết được 5 dòng đó thì chưa tự động được. Tự động một mớ lộn xộn thì được một mớ lộn xộn chạy nhanh hơn |
| Duyệt rồi nhưng cho đăng ngay | Bấm `publishChannelTaskNow` cho gọn, thành thói quen | Đổi sang hẹn giờ tối thiểu 15 phút. Duyệt xong 2 phút mới thấy sai chính tả tên khách thì `updateChannelPublishAt` để dời giờ, hoặc `cancelChannelPublishTask` để hủy |
| Agent tự gọi công cụ đăng khi chưa được duyệt | Anh chị hỏi "chuẩn bị bài đi" và nó gọi luôn công cụ hẹn giờ | Viết ràng buộc cứng vào file skill, liệt kê đủ **cả hai**: công cụ đăng ngay và công cụ tạo luồng hẹn giờ. Trong prompt hàng ngày luôn tách riêng câu ở B3 |
| Không ghi log nên tuần sau không đo được gì | Luồng chạy đẹp, bài lên đều, nhưng hỏi "tuần rồi kênh nào ra đơn" thì không trả lời được | Thêm bảng log ngay, tối thiểu 6 cột: ngày, nội dung, kênh, ai duyệt, kết quả, ghi chú. Chưa có log thì chưa tính là luồng hoàn chỉnh |
| Nối quá nhiều bước ngay lần đầu | Sơ đồ 9 bước, 4 nhánh rẽ, chạy thử hỏng ở bước 3 mà không biết hỏng chỗ nào | Cắt xuống 3 bước, chạy cho thông từ đầu tới cuối, rồi mới thêm. Luồng đầu tiên phải chạy được trọn một lần, dù thô |

---

CES Global · Creative, Effective, Sustainable
