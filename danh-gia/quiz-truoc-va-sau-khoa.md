# Quiz trước khóa và sau khóa: AI Agent cho Sale & Marketing

Kirkpatrick mức 2, đo học viên có thật sự biết thêm không.

| Mục | Nội dung |
|---|---|
| Dùng khi nào | Hai lần: 15 phút đầu buổi 1, và 15 phút đầu buổi 6 |
| Bộ câu hỏi | **Một bộ duy nhất, dùng cho cả hai lần.** Khác bộ câu là hai điểm số không so được với nhau |
| Số câu | 20 |
| Thang điểm | 20, mỗi câu 1 điểm |
| Thời gian làm | 15 phút |
| Ghi tên | Không. Chỉ ghi mã học viên là bốn số cuối số điện thoại |
| Nguồn mục tiêu | `00-tong-quan/ma-tran-muc-tieu.md`, 30 mục tiêu, mã B01-1 tới B06-5 |
| Cách xuất | Google Forms, bật thu mã học viên bằng một câu trả lời ngắn ở đầu form |

**Ba việc bắt buộc để phép đo không hỏng:**

1. **Không chữa đáp án quiz trước khóa.** Nói thẳng với lớp ở buổi 1: cuối khóa tôi chữa một thể. Chữa sớm là học viên nhớ đáp án, điểm sau khóa tăng ảo.
2. **Bản làm ở buổi 6 đảo thứ tự câu và đảo thứ tự phương án.** Nội dung câu giữ nguyên từng chữ.
3. **Quiz không tính điểm cá nhân.** Nói rõ điều này trước khi phát. Học viên bớt tâm lý phải làm đẹp, và số thu về mới dùng được.

---

## Lời mở đầu bản làm ở buổi 1

> Bài này 20 câu, làm trong 15 phút.
>
> Bài không tính điểm cá nhân, không ai trong lớp biết điểm của riêng anh chị. Tôi dùng để biết lớp đang đứng ở đâu, rồi cuối khóa đo lại xem sáu buổi đi được bao xa.
>
> Chỗ nào không biết thì bỏ trống, đừng đoán bừa. Đoán bừa làm tôi đọc sai trình độ lớp và soạn nhầm buổi sau.
>
> Anh chị ghi giúp tôi bốn số cuối số điện thoại vào ô mã học viên. Cuối khóa tôi cần ghép hai bài của cùng một người, mà vẫn không phải hỏi tên ai.

**Mã học viên:** bốn số cuối số điện thoại của anh chị: ______

Trong bài này tôi dùng ba từ theo nghĩa đã dạy trong khóa. "Prompt" là câu mình gõ cho AI. "Skill" là một quy trình đóng thành file để Claude gọi lại. "MCP" là kết nối cho Claude với tới dữ liệu bên ngoài thư mục làm việc.

---

## Bộ 20 câu

**Câu 1.** Anh chị có một quy trình 8 bước để viết bài bán hàng cho Facebook. Quy trình này nên đặt vào tầng nào trong bốn tầng ngữ cảnh? *Chọn một.*

```
Tầng 1, file CLAUDE.md, vì đây là thứ Claude cần đọc trước mọi việc
Tầng 2, một Skill riêng, vì nó chỉ được lấy ra khi đúng việc viết bài
Tầng 3, Memory, vì Claude cần nhớ quy trình này giữa các phiên
Tầng 4, MCP, vì quy trình cần với tới dữ liệu bên ngoài
```

**Câu 2.** Bốn cách mô tả giọng văn dưới đây cùng nằm trong mục giọng văn của `CLAUDE.md`. Cách nào viết đạt, tức là Claude đọc xong làm đúng và người khác kiểm được? *Chọn một.*

```
Giọng chuyên nghiệp, thân thiện, uy tín, gần gũi với khách hàng trẻ
Xưng "mình", gọi khách là "bạn". Câu tối đa 20 chữ. Tối đa 2 emoji một bài. Không dùng dấu chấm than quá 1 lần
Giọng viết cần hấp dẫn, cuốn hút, tạo được cảm xúc và thúc đẩy hành động mua
Viết theo phong cách thương hiệu, bám sát tinh thần sản phẩm thiên nhiên
```

**Câu 3.** Anh chị viết xong một Skill nhưng Claude không bao giờ tự gọi tới nó. Chỗ nào có khả năng sai nhất? *Chọn một.*

```
File đặt sai chỗ, hoặc dòng description trong frontmatter không mô tả đúng việc nào thì dùng skill này
Nội dung skill viết chưa đủ dài, cần thêm ví dụ
Máy chưa cài Git nên Claude không đọc được file
Tài khoản đang là gói miễn phí nên skill bị khóa
```

**Câu 4.** Anh chị muốn Claude tự đọc bảng đơn hàng đang nằm trên Google Sheet, thay vì phải copy từng dòng dán vào. Cần thêm cái gì? *Chọn một.*

```
Bật Memory, rồi dặn Claude nhớ nội dung bảng đó
Viết nội dung bảng vào CLAUDE.md, mỗi lần cập nhật thì sửa lại file
Nối một MCP tới Google Sheet, cấp quyền đọc cho đúng bảng đó
Dựng một Skill tên doc-don-hang, mô tả cấu trúc bảng trong skill
```

**Câu 5.** Anh chị hỏi Claude: "Ngân sách quảng cáo tháng trước của Thảo An là bao nhiêu?" Hồ sơ trong thư mục làm việc ghi rõ mục này còn trống. Claude trả về "khoảng 15 tới 20 triệu, mức phổ biến của thương hiệu mỹ phẩm quy mô tương tự". Việc đúng phải làm là gì? *Chọn một.*

```
Lấy tạm con số đó, vì nó là mức tham khảo hợp lý của ngành
Hỏi lại Claude lần nữa, nếu hai lần ra cùng con số thì tin
Mở hồ sơ dò ngược, xác nhận con số không có trong file, rồi thêm vào CLAUDE.md một dòng buộc trả lời "chưa đủ dữ liệu" cho mọi số không có trong thư mục, và chạy lại
Bỏ câu hỏi này, chuyển sang hỏi việc khác
```

**Câu 6.** Một khách viết trong tin nhắn: "Da mình nhạy cảm lắm, dùng cái này có bị rát không shop?" Câu này là dữ liệu thô hay insight, và vì sao? *Chọn một.*

```
Là insight, vì nó nói rõ nỗi lo của khách
Là dữ liệu thô. Nó thành insight khi có nhiều người cùng nói, có lý do đằng sau, và biết rồi thì viết khác đi bán khác đi
Là insight, vì nó trích được nguyên văn và có mã nguồn
Là dữ liệu thô, và không dùng được vào việc gì cho tới khi có ít nhất 100 mẩu
```

**Câu 7.** Trong bảng insight, cột tần suất nên ghi thế nào để giảng viên hoặc sếp kiểm lại được? *Chọn một.*

```
Ghi mức độ: cao, trung bình, thấp
Ghi tỉ lệ phần trăm làm tròn, ví dụ 30 phần trăm
Ghi dạng "9 trên 30 mẩu", tức số mẩu nhắc tới trên tổng số mẩu đã đọc
Không cần cột tần suất, chỉ cần cột trích dẫn là đủ
```

**Câu 8.** Anh chị nhận một bảng insight do agent của người khác sinh ra. Dấu hiệu nào cho biết bảng này có chỗ bịa, phải kiểm lại? *Chọn tất cả những dấu hiệu đúng.*

```
Có một dòng ghi mã trích dẫn R14, nhưng file gốc chỉ có tới R12
Cột tần suất ghi "12 trên 30 mẩu", đếm tay trong file gốc ra 5 mẩu
Bảng viết trôi chảy, câu chữ gọn gàng, đọc rất xuôi
Có một persona mô tả rất chi tiết về nghề nghiệp và thu nhập, mà trong 30 mẩu không ai nhắc tới nghề hay thu nhập
Một dòng ghi nhãn [SUY LUẬN] thay vì [DATA THẬT]
```

**Câu 9.** Anh chị dựng bộ tiêu chí chấm điểm lead cho việc bán sỉ của mình. Bộ nào dưới đây dùng được? *Chọn một.*

```
Bốn tiêu chí, mỗi tiêu chí thang 1 tới 5, trọng số lần lượt 25, 25, 30, 20, tổng 100. Mỗi trọng số nêu được lý do kinh doanh
Bốn tiêu chí, không đặt trọng số, cứ cộng điểm rồi xếp hạng
Để agent tự nghĩ ra tiêu chí, vì agent đọc được nhiều dữ liệu hơn mình
Hai tiêu chí là quy mô đơn và mức độ quan tâm, trọng số 50 và 50
```

**Câu 10.** Agent chấm xong 10 lead, mọi dòng đều ghi độ tin cậy "Cao", kể cả ba lead mà cột ghi chú trao đổi để trống. Điều này nói lên chuyện gì? *Chọn một.*

```
Bộ dữ liệu lead của anh chị đầy đủ, đây là dấu hiệu tốt
Agent đang chấm bằng suy luận từ loại hình cơ sở, cột độ tin cậy chưa có tác dụng. Lead thiếu ghi chú phải bị hạ độ tin cậy
Nên bỏ cột độ tin cậy vì nó không thêm thông tin gì
Nên chấm lại bằng thang 100 thay vì thang 1 tới 5
```

**Câu 11.** Anh chị viết xong 10 email tiếp cận lead. Có một phép thử để biết email đó là cá nhân hóa thật hay chỉ là mẫu điền tên. Phép thử đó là gì, và kết quả thế nào thì gọi là chưa đạt?

*Trả lời ngắn, hai tới ba câu.*

**Câu 12.** Một lead hỏi: "Bên em cho tôi độc quyền khu vực quận 7 được không?" Chính sách giá của anh chị chưa có mục nào về độc quyền khu vực. Agent soạn proposal phải làm gì để tính là đạt? *Chọn một.*

```
Đề xuất một mức độc quyền hợp lý dựa trên thông lệ ngành, ghi chú là tham khảo
Để trống mục đó trong proposal và ghi rõ "cần xin ý kiến", không tự hứa một con số nào
Trả lời thẳng là không có độc quyền, để khỏi mất thời gian hai bên
Ghi mức độc quyền cao nhất có thể, rồi thương lượng xuống sau
```

**Câu 13.** Content Engine của anh chị sinh ra caption cho lịch 14 ngày. Làm sao để caption đó vẫn đúng giọng và vẫn sạch danh sách từ cấm đã khai ở buổi 1? *Chọn một.*

```
Chép nguyên phần giọng văn và từ cấm vào bên trong Content Engine
Tới bước viết caption thì Content Engine gọi lại skill viet-bai-ban-hang, và cả hai skill đọc chung một CLAUDE.md
Sau khi có caption thì ngồi soát tay từng bài, đối chiếu danh sách từ cấm
Dặn Claude trong prompt là nhớ giữ giọng thương hiệu
```

**Câu 14.** Lịch 14 ngày của anh chị có 14 ngày đều là bài giới thiệu sản phẩm kèm mã giảm giá. Vấn đề lớn nhất nằm ở đâu? *Chọn một.*

```
Đăng quá nhiều bài trong 14 ngày, nên rút xuống 7 bài
Lịch thiếu ba loại ngày còn lại: giáo dục, bằng chứng, xử lý phản đối. Khách chưa tin thì giảm giá không giải quyết được gì
Mã giảm giá nên đặt ở ngày 1 để bắt khách sớm
Không có vấn đề gì, miễn là mỗi bài viết khác nhau
```

**Câu 15.** Anh chị làm ngành có quy định chặt, ví dụ mỹ phẩm hoặc thực phẩm chức năng. Cách làm nào khiến agent tự chặn từ cấm, thay vì anh chị ngồi sửa tay sau? *Chọn một.*

```
Khai danh sách từ cấm và cam kết cấm vào CLAUDE.md trước khi agent viết chữ đầu tiên
Viết bài xong rồi dùng công cụ tìm kiếm để rà lại từng từ cấm
Nhắc trong prompt mỗi lần chạy là đừng dùng từ cấm
Chỉ đăng bài sau khi đã gửi cho luật sư đọc
```

**Câu 16.** Anh chị có một bài Facebook 900 ký tự, cần cắt xuống dưới 280 ký tự để đăng lên kênh khác. Cắt xong, ba thứ nào bắt buộc vẫn phải còn trong bài? *Chọn một.*

```
Hook mở đầu, hashtag, đường dẫn mua hàng
Một nỗi đau, một điểm khác biệt của sản phẩm, một lời kêu gọi hành động
Tên thương hiệu, giá, cam kết hoàn tiền
Câu chuyện khách hàng, bảng thành phần, ảnh sản phẩm
```

**Câu 17.** Việc nào KHÔNG được để chạy tự động rồi gửi thẳng ra ngoài mà không có người đọc lại? *Chọn tất cả những việc không được.*

```
Soạn bản nháp caption cho lịch đăng tuần sau
Duyệt mức chiết khấu cho một đơn sỉ
Đăng bài lên fanpage đang chạy thật
Gom bình luận trong tuần thành một bảng để mình đọc
Gửi email báo giá cho khách
```

**Câu 18.** Một luồng tự động gồm ba lớp: kích hoạt, xử lý, đưa ra. Chốt duyệt của người nằm ở đâu, và bảng quản lý phải có hai cột nào? *Chọn một.*

```
Chốt duyệt nằm ở đầu lớp kích hoạt. Bảng cần cột ngày và cột nội dung
Chốt duyệt nằm ở đầu lớp đưa ra, tức xử lý xong thì dừng chờ người đồng ý. Bảng cần cột trạng thái và cột người duyệt
Chốt duyệt nằm giữa lớp xử lý. Bảng cần cột kênh và cột giờ đăng
Không cần chốt duyệt nếu luồng đã chạy đúng vài lần. Bảng cần cột kết quả và cột ghi chú
```

**Câu 19.** Luồng post bài của anh chị đã chạy được: lấy caption từ lịch 14 ngày, soát giới hạn kênh, chuẩn bị ảnh, người duyệt bấm đồng ý. Bước cuối cùng nên là đăng ngay hay hẹn giờ sau 30 phút? Nêu lý do.

*Trả lời ngắn, hai tới ba câu.*

**Câu 20.** Anh chị nghỉ phép hai tuần. Một đồng nghiệp chưa học khóa này mở thư mục làm việc của anh chị ra và cần viết một bài đăng đúng chuẩn. Nêu hai thứ anh chị phải bàn giao, nói rõ mỗi thứ khác nhau ở chỗ nào, và nêu một cách kiểm tra xem bàn giao đã đủ chưa.

*Trả lời đoạn, năm tới bảy câu.*

---

## Bản làm ở buổi 6

Cùng nội dung câu, đổi đúng hai thứ:

1. **Đảo thứ tự câu.** Thứ tự đề xuất: 11, 5, 17, 2, 20, 8, 14, 1, 19, 6, 12, 3, 16, 9, 18, 4, 13, 7, 15, 10.
2. **Đảo thứ tự phương án trong từng câu.**

Đổi lời mở đầu thành:

> Bài này giống hệt bài anh chị làm hôm buổi 1. Tôi so hai điểm để biết sáu buổi vừa rồi đi được tới đâu. Vẫn không tính điểm cá nhân. Anh chị nhớ ghi đúng bốn số cuối điện thoại như lần trước, nếu không tôi ghép không ra cặp.

**Không đổi nội dung câu hỏi.** Đổi nội dung là mất luôn phép đo.

---

## Bản đáp án

Chỉ dành cho giảng viên. Không phát cho học viên trước khi kết thúc buổi 6.

| Câu | Đáp án | Mục tiêu | Bậc Bloom | Vì sao đáp án này đúng |
|---|---|---|---|---|
| 1 | Tầng 2, một Skill riêng | B01-1 | Hiểu | `CLAUDE.md` là thứ Claude đọc trước mọi việc, nên chỉ chứa thứ luôn đúng cho mọi việc. Nhét quy trình viết bài Facebook vào đó thì lúc soạn email chào sỉ Claude cũng phải đọc 8 bước không liên quan |
| 2 | Xưng "mình", gọi khách là "bạn", câu tối đa 20 chữ, tối đa 2 emoji | B01-2 | Vận dụng | Ba phương án kia toàn tính từ. "Chuyên nghiệp" hay "hấp dẫn" thì mỗi người hiểu một kiểu, Claude cũng vậy. Mô tả bằng hành vi thì đếm được, kiểm được |
| 3 | File đặt sai chỗ, hoặc dòng `description` không mô tả đúng việc | B01-3 | Vận dụng | Claude không đọc hết nội dung mọi skill. Nó chỉ lướt dòng `description` để chọn skill nào hợp việc. Mô tả sai thì skill nằm đó không ai gọi |
| 4 | Nối MCP tới Google Sheet, cấp quyền đọc | B01-4 | Vận dụng | Memory là chỗ ghi thói quen làm việc, không phải chỗ chứa dữ liệu đổi hằng ngày. Chép bảng vào `CLAUDE.md` thì hôm sau số cũ đã sai |
| 5 | Dò ngược hồ sơ, thêm dòng ràng buộc vào `CLAUDE.md`, chạy lại | B01-5 | Phân tích | Đây là nguyên tắc chống bịa thứ nhất: chỉ dùng dữ liệu người dùng cấp. Con số "phổ biến của ngành" nghe hợp lý nhưng không có trong hồ sơ, mang đi báo cáo là sai thật |
| 6 | Là dữ liệu thô, thành insight khi đủ ba điều kiện | B02-1, B02-2 | Phân tích | Một người, một câu, một lần thì mới là dữ liệu. Insight cần lặp lại, có lý do đằng sau, và đổi được cách bán |
| 7 | Ghi dạng "9 trên 30 mẩu" | B02-2 | Vận dụng | Ghi "cao" thì không ai kiểm được. Ghi phần trăm làm tròn thì mất mẫu số. Ghi số trên tổng thì giảng viên đếm tay lại được trong hai phút |
| 8 | Ba dấu hiệu: mã trích dẫn không tồn tại; tần suất đếm lại không khớp; persona chi tiết mà data không có căn cứ | B02-5 | Đánh giá | Đúng đủ ba mới tính điểm. "Viết trôi chảy" là bẫy, câu hay không liên quan tới đúng sai. Nhãn `[SUY LUẬN]` không phải lỗi, đó là agent tự khai đúng chỗ nó đoán |
| 9 | Bốn tiêu chí, trọng số tổng 100, mỗi trọng số nêu được lý do | B03-1 | Sáng tạo | Không trọng số thì tiêu chí nào cũng nặng như nhau, xếp hạng ra sai. Để agent tự nghĩ tiêu chí thì mỗi lần chạy một kiểu, sếp hỏi không giải thích được |
| 10 | Agent đang chấm bằng suy luận, lead thiếu ghi chú phải bị hạ độ tin cậy | B03-2 | Phân tích | Điểm 51 độ tin cậy Cao là một việc, điểm 51 độ tin cậy Thấp là việc khác hẳn. Với lead tin cậy thấp thì việc cần làm là đi tìm đúng người, không phải gửi proposal |
| 11 | Chấm theo mô tả bên dưới | B03-3 | Vận dụng | |
| 12 | Để trống mục đó và ghi rõ "cần xin ý kiến" | B03-4, B03-5 | Vận dụng | Agent hứa một con số chưa có chính sách là hứa thay chủ doanh nghiệp. Sai ở đây tốn tiền thật, không phải tốn công sửa bài |
| 13 | Content Engine gọi lại skill `viet-bai-ban-hang`, hai skill đọc chung `CLAUDE.md` | B04-1 | Vận dụng | Chép trùng nội dung sang hai chỗ thì sửa một chỗ quên chỗ kia. Soát tay từng bài là công việc lặp lại mà khóa này đang tìm cách bỏ đi |
| 14 | Thiếu ba loại ngày còn lại | B04-2 | Sáng tạo | Nhịp 14 ngày cần đủ bốn loại: giáo dục, bằng chứng, xử lý phản đối, ưu đãi. Đặt ưu đãi vào người chưa tin là đốt tiền |
| 15 | Khai từ cấm và cam kết cấm vào `CLAUDE.md` trước khi agent viết | B04-4 | Vận dụng | Chặn trước thì agent tự từ chối hoặc tự thay từ. Rà sau thì mỗi bài mất thêm thời gian, và bài thứ mười mấy là bắt đầu sót |
| 16 | Một nỗi đau, một điểm khác biệt, một lời kêu gọi | B04-3, B04-5 | Phân tích | Đây là lõi của một bài. Cắt mất một trong ba thì bài còn chữ mà không còn tác dụng bán hàng |
| 17 | Ba việc: duyệt chiết khấu; đăng bài lên fanpage thật; gửi email báo giá | B05-1, B05-5 | Phân tích | Đúng đủ ba mới tính điểm. Ba việc này đều có tiền hoặc có người ngoài đọc, sai là không rút lại được. Soạn nháp và gom bảng cho mình đọc thì sai sửa được |
| 18 | Chốt duyệt ở đầu lớp đưa ra; bảng cần cột trạng thái và cột người duyệt | B05-2, B05-3 | Vận dụng | Lớp đưa ra là lớp duy nhất dùng quyền ghi và quyền gửi ra ngoài. Không có hai cột đó thì không ai biết bài nào đã duyệt, ai duyệt |
| 19 | Chấm theo mô tả bên dưới | B05-4 | Đánh giá | |
| 20 | Chấm theo mô tả bên dưới | B06-1, B06-2, B06-3, B06-4 | Đánh giá | |

### Cách chấm ba câu trả lời viết

Mỗi câu 1 điểm, chấm ba nấc 0 / 0,5 / 1.

**Câu 11, phép thử email cá nhân hóa.** Mục tiêu B03-3.

- 1 điểm: nêu được phép thử đổi tên, tức là thay tên lead này bằng tên lead khác. Và nêu đúng kết quả chưa đạt: email vẫn dùng được nguyên si cho lead khác thì đó là mẫu điền tên, không phải cá nhân hóa.
- 0,5 điểm: nêu được ý phải bám ghi chú trao đổi thật của từng lead, nhưng không nêu được phép thử cụ thể.
- 0 điểm: bỏ trống, hoặc trả lời chung chung kiểu "đọc lại xem có tự nhiên không".

**Câu 19, đăng ngay hay hẹn giờ.** Mục tiêu B05-4.

- 1 điểm: chọn hẹn giờ, và nêu được lý do đúng: hẹn giờ để lại một cửa sổ còn hủy hoặc còn sửa được. Người duyệt là phanh thứ nhất, hẹn giờ là phanh thứ hai. Đăng ngay là bỏ mất phanh thứ hai.
- 0,5 điểm: chọn hẹn giờ nhưng lý do chung chung, ví dụ "cho an toàn hơn", không nói được cửa sổ hủy.
- 0 điểm: chọn đăng ngay, hoặc bỏ trống.

**Câu 20, bàn giao cho đồng nghiệp.** Mục tiêu B06-1, B06-2, B06-3, B06-4.

Ba phần cần có trong câu trả lời:

- Hai thứ phải bàn giao: một Claude Skill và một Playbook.
- Khác nhau ở đâu: Skill là thứ Claude đọc, chứa quy trình các bước, tiêu chuẩn đầu ra, ranh giới không được vượt, cách xử lý khi thiếu dữ liệu. Playbook là thứ người đọc, chứa mục đích, ai dùng, quy trình từng bước, tiêu chuẩn đầu ra, ranh giới, chỉ số đo, cách xử lý khi agent ra sai. Nêu được ý "một cái cho máy đọc, một cái cho người đọc" là tính đúng phần này.
- Cách kiểm: đưa cho một người chưa học khóa, để họ chạy trên một yêu cầu chưa từng làm, xem kết quả có đạt đúng bảng tiêu chuẩn đầu ra do chính mình viết không, và họ có phải gọi điện hỏi lại không.

Chấm:
- 1 điểm: có đủ ba phần trên.
- 0,5 điểm: có hai trong ba phần.
- 0 điểm: chỉ nêu được một phần, hoặc trả lời chung chung kiểu "bàn giao tài liệu hướng dẫn".

### Ghi chú chấm câu chọn nhiều

Câu 8 và câu 17 là câu chọn nhiều. **Đúng hết mới tính 1 điểm**, không có nửa điểm. Chọn thiếu một ý hoặc chọn thừa một ý đều tính 0.

---

## Bảng đối chiếu mục tiêu

Bảng bắt buộc. Nhìn một cái là thấy mục tiêu nào bị bỏ quên.

| Mục tiêu | Nội dung rút gọn | Câu hỏi | Số câu |
|---|---|---|---|
| B01-1 | Phân biệt bốn tầng ngữ cảnh | 1 | 1 |
| B01-2 | Viết `CLAUDE.md` đủ 9 mục, giọng văn mô tả bằng hành vi | 2 | 1 |
| B01-3 | Dựng skill `viet-bai-ban-hang` đúng đường dẫn và frontmatter | 3 | 1 |
| B01-4 | Cấu hình Memory và một kết nối MCP | 4 | 1 |
| B01-5 | Chẩn đoán Claude bịa số và sửa `CLAUDE.md` chặn lần sau | 5 | 1 |
| B02-1 | Dựng skill `customer-insight`, mọi dòng có mã nguồn và trích dẫn | 6 | 1 |
| B02-2 | Xếp hạng pain theo tần suất, tách dữ liệu thô khỏi insight | 6, 7 | 2 |
| B02-3 | Chuyển insight thành 5 content angle truy được về trích dẫn | 8 | 1 |
| B02-4 | Viết 5 bài social, 3 brief hình ảnh, 3 visual | 8 | 1 |
| B02-5 | Thẩm định bảng insight có bịa hay không | 8 | 1 |
| B03-1 | Thiết kế bộ tiêu chí chấm lead, trọng số tổng 100 | 9 | 1 |
| B03-2 | Áp bộ tiêu chí lên 10 lead, có cột lý do và độ tin cậy | 10 | 1 |
| B03-3 | Viết 10 email và 10 tin nhắn cá nhân hóa bằng ghi chú thật | 11 | 1 |
| B03-4 | Dựng proposal, agent dừng khi khách hỏi điều chưa có chính sách | 12 | 1 |
| B03-5 | Kịch bản gọi và 10 kịch bản xử lý từ chối, không hứa quá chính sách | 12 | 1 |
| B04-1 | Dựng Content Engine, gọi lại skill `viet-bai-ban-hang` | 13 | 1 |
| B04-2 | Nhịp 14 ngày đủ 4 loại ngày, mỗi bài nối vào hành trình mua | 14 | 1 |
| B04-3 | 10 bài social không trùng ý, mỗi bài 1 pain, 1 USP, 1 CTA | 16 | 1 |
| B04-4 | Khai ràng buộc pháp lý và thương hiệu trước khi agent viết | 15 | 1 |
| B04-5 | Cắt bài xuống giới hạn ký tự mà vẫn giữ đủ ba phần | 16 | 1 |
| B05-1 | Vẽ automation map, loại ra việc không nên tự động kèm lý do | 17 | 1 |
| B05-2 | Bảng quản lý có cột trạng thái và cột người duyệt | 18 | 1 |
| B05-3 | Chạy luồng có đủ 5 phần, hoặc prototype | 18 | 1 |
| B05-4 | Chạy trọn luồng post bài, có điểm dừng chờ người duyệt | 19 | 1 |
| B05-5 | Thẩm định ranh giới ba quyền đọc, ghi, gửi ra ngoài | 17 | 1 |
| B06-1 | Nâng skill buổi 1 thành Skill bàn giao được, đủ 4 phần | 20 | 1 |
| B06-2 | Thẩm định Skill chạy đúng ngoài bối cảnh gốc | 20 | 1 |
| B06-3 | Viết AI Agent Playbook đủ 4 câu trả lời | 20 | 1 |
| B06-4 | Sắp xếp tài sản 5 buổi, tìm được trong 10 giây | 20 | 1 |
| B06-5 | Trình bày 5 phút bằng kết quả, nộp kế hoạch 14 ngày 4 cột | Không có câu quiz. Đo bằng rubric | 0 |

**Ba chỗ phải nói thẳng về bảng này:**

1. Cả 30 mục tiêu đều có câu quiz, trừ **B06-5**. Mục tiêu đó là trình bày miệng có bấm giờ và nộp kế hoạch 14 ngày, không có cách nào đo bằng câu hỏi giấy. Nó đo bằng tiêu chí 6 của `danh-gia/rubric-san-pham-cuoi-khoa.md`.
2. Quiz chỉ là **một nửa** phép đo mức 2 của khóa này. Nửa còn lại, và là nửa nặng hơn, là 40 hơn tài sản học viên nộp bằng file thật, chấm theo `00-tong-quan/chuan-dau-ra.md` và theo rubric cuối khóa. Khi làm báo cáo phải trình bày cả hai, đừng chỉ đưa điểm quiz.
3. Một số mục tiêu bậc Vận dụng chỉ có một câu trắc nghiệm đứng sau. Một câu không đủ để kết luận về một cá nhân. Nó đủ để nhìn ra xu hướng của cả lớp, và đó là mục đích của bộ quiz này.

**Phân bố bậc Bloom:** Hiểu 1 câu, Vận dụng 8 câu, Phân tích 5 câu, Đánh giá 4 câu, Sáng tạo 2 câu. Bậc Nhớ và Hiểu chiếm 1 trên 20, tức 5 phần trăm. Luật tối đa 30 phần trăm ở bậc Nhớ và Hiểu: đạt.

**Phân bố theo buổi:** buổi 1 có 5 câu, buổi 2 có 3 câu, buổi 3 có 4 câu, buổi 4 có 4 câu, buổi 5 có 3 câu, buổi 6 có 1 câu. Mỗi buổi tối thiểu 2 câu: buổi 6 chỉ có 1 câu vì câu 20 là câu tổng hợp bốn mục tiêu và chấm theo đoạn viết, nặng bằng ba câu trắc nghiệm. Xem ghi chú ở mục "Điểm cần biết trước khi đọc kết quả" bên dưới.

**Câu về ba nguyên tắc chống bịa:** câu 5 (chỉ dùng dữ liệu người dùng cấp), câu 8 (gắn nhãn nguồn và bắt lỗi bịa trích dẫn), câu 12 (agent dừng khi chưa có chính sách), câu 17 và câu 19 (người duyệt cuối). Năm câu trên 20, tức 25 phần trăm bộ đề. Đây là chủ ý: ba nguyên tắc chống bịa là điểm khác biệt của khóa này so với các khóa dạy mẹo prompt.

---

## Cách tính điểm và cách so trước với sau

### Tính điểm một bài

Tổng 20 điểm. Mười bảy câu trắc nghiệm mỗi câu 1 điểm, chấm bằng máy. Ba câu viết mỗi câu 1 điểm, chấm tay theo mô tả ba nấc ở trên.

Bỏ trống tính 0, không trừ điểm. Nói rõ điều này với lớp để họ dám bỏ trống thay vì đoán bừa.

### So điểm trước với sau

Báo cáo **hai** con số cho mỗi học viên, không phải một:

| Chỉ số | Công thức |
|---|---|
| Mức tăng thô | điểm sau trừ điểm trước |
| Mức tăng chuẩn hóa | (điểm sau trừ điểm trước) chia cho (20 trừ điểm trước) |

Vì sao cần con số thứ hai. Người vào khóa đã được 15 trên 20 thì dù học rất tốt cũng chỉ còn 5 điểm để lấy. Người vào khóa được 5 trên 20 tăng 8 điểm là bình thường. Nhìn mức tăng thô thì người thứ hai trông giỏi hơn hẳn. Nhìn mức tăng chuẩn hóa mới biết ai lấy được nhiều phần hơn của khoảng còn thiếu.

Ví dụ điền vào bảng ở mục 3 của `danh-gia/diem-danh.md`:

| Mã học viên | Điểm trước | Điểm sau | Tăng thô | Tăng chuẩn hóa |
|---|---|---|---|---|
| 4821 | 6 | 15 | 9 | 0,64 |
| 3907 | 14 | 19 | 5 | 0,83 |
| 1264 | 5 | 11 | 6 | 0,40 |

Học viên 3907 có mức tăng thô thấp nhất nhưng mức tăng chuẩn hóa cao nhất. Báo cáo chỉ đưa cột tăng thô là làm người đọc hiểu nhầm người này học kém nhất lớp.

### Mốc tự kiểm độ khó của bộ đề

**Điểm trung bình trước khóa nên rơi vào khoảng 6 tới 10 trên 20, tức 30 tới 50 phần trăm.**

| Điểm trung bình trước khóa | Nghĩa là | Phải làm gì |
|---|---|---|
| Trên 14 trên 20 | Bộ câu quá dễ, không còn chỗ để tăng | Làm khó lên, và sửa **cả hai bản** để giữ nguyên tắc cùng bộ câu. Không được chỉ sửa bản sau khóa |
| Từ 6 tới 10 | Bộ câu vừa | Giữ nguyên |
| Dưới 4 trên 20 | Quá khó, hoặc câu hỏi diễn đạt rối nên học viên đoán bừa | Đọc lại phần đông người sai cùng một câu, xem câu đó có gài bẫy không |

Khóa này có 5 câu ở buổi 1 và phần lớn học viên chưa từng dùng Claude Code, nên điểm trước khóa dự kiến sẽ thấp, khoảng 5 tới 8. Đó là bình thường, không phải dấu hiệu đề khó.

---

## Điểm cần biết trước khi đọc kết quả

**Buổi 6 chỉ có một câu, và đó là chủ ý.** Buổi 6 là buổi đóng gói, không dạy khái niệm mới. Đo nó bằng trắc nghiệm không đúng bản chất: sản phẩm của buổi 6 là một Skill và một Playbook mà người khác cầm lên dùng được, chuyện đó chỉ đo được bằng rubric và bằng phép thử đưa cho người khác chạy. Câu 20 giữ lại để đo phần hiểu, phần làm được nằm ở rubric.

**Số cặp ghép được luôn nhỏ hơn số phiếu thu về.** Học viên ghi nhầm bốn số cuối, hoặc vắng một trong hai buổi. Ghi rõ trong báo cáo: thu về bao nhiêu phiếu trước, bao nhiêu phiếu sau, ghép được bao nhiêu cặp. Chỉ tính mức tăng trên số cặp ghép được, không tính trên trung bình lớp của hai lần khác nhau về sĩ số.

**Đây là khóa mở.** Học viên không thuộc cùng một công ty, không ai bắt buộc họ làm quiz. Muốn tỉ lệ làm bài cao thì phải làm ba việc: phát quiz **trong giờ học** chứ không gửi link sau buổi; nói rõ không tính điểm cá nhân; và ở buổi 6 nói thẳng là bài này chỉ mất 15 phút và nó quyết định con số duy nhất chứng minh khóa có tác dụng.

---

## Xuất sang Google Forms

1. Mở `forms.new`, đặt tên form là "Quiz đầu khóa: AI Agent cho Sale và Marketing". Bản buổi 6 đặt tên "Quiz cuối khóa".
2. Câu đầu tiên của form là câu trả lời ngắn: "Mã học viên: bốn số cuối số điện thoại của anh chị". Đặt là câu bắt buộc.
3. **Tắt thu thập email.** Mã học viên là đủ để ghép cặp, và ẩn danh thì học viên bớt làm đẹp.
4. Với câu trắc nghiệm: chọn kiểu Multiple choice, dán nội dung câu, rồi dán nguyên khối phương án vào ô lựa chọn đầu tiên. Forms tự tách mỗi dòng thành một lựa chọn.
5. Câu 8 và câu 17 chọn kiểu Checkboxes, không phải Multiple choice.
6. Câu 11, 19, 20 chọn kiểu Paragraph.
7. Bật chế độ Quiz trong phần Settings, gán đáp án và điểm cho 17 câu trắc nghiệm để máy chấm. Ba câu viết để chấm tay.
8. **Tắt hiển thị đáp án ngay sau khi nộp** ở bản đầu khóa. Bật lại ở bản cuối khóa nếu muốn chữa bài tại lớp.
9. Lấy link rút gọn, dựng mã QR, dán vào slide và vào khung chat của Zoom hoặc Meet. Lớp online thì dán link vào khung chat là chính, mã QR chỉ dành cho người học bằng điện thoại.
