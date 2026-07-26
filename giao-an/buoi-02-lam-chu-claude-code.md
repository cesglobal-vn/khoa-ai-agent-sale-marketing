# BÀI SOẠN GIÁO VIÊN - BUỔI 2

## Dạy Claude hiểu việc của bạn, và biết dùng cả đội AI

> Bản script giảng được ngay. Đọc theo, không cần soạn thêm.
> Lớp: 10 đến 20 người làm sale và marketing. Chủ doanh nghiệp nhỏ, trưởng phòng marketing, nhân sự content, nhân sự ads, nhân sự CRM, người làm agency. Phần lớn KHÔNG biết code, chưa quen dòng lệnh. Nhiều người dù đã học buổi 1 vẫn CHƯA thực sự hiểu CLAUDE.md hay skill là gì. Đây là ràng buộc thiết kế quan trọng nhất của buổi này. Mỗi thao tác phải ghi rõ bấm gì, gõ gì, thấy gì thì biết đúng. Không giả định họ đã hiểu, giải thích lại từ đầu.
> Học online live qua Zoom hoặc Google Meet. Giảng viên chia sẻ màn hình, học viên làm trên máy mình và chia sẻ màn hình lại khi cần hỗ trợ.
> Công cụ học viên dùng: **Claude Desktop, tab Code**. Cả buổi làm ở tab Code.
> Case study xuyên suốt: **Thảo An**, thương hiệu mỹ phẩm thảo mộc giả định, 3 SKU, bán B2C qua Facebook và Shopee, bán sỉ B2B cho spa.
> Thời lượng: 150 phút, đã gồm 10 phút giải lao.
> Nguyên tắc thiết kế xuyên suốt: **đau trước, giải pháp sau.** Mỗi khối mở bằng một nỗi đau anh chị tự cảm, rồi khái niệm mới hiện ra như lời giải. Không định nghĩa khô trước. Không bày hết mọi thứ ra đầu buổi.
> Hai nửa buổi: nửa đầu (K1 tới K3) TỰ TAY LÀM, mang về dùng ngày mai. Nửa sau (K4) HIỂU ĐỂ DÙNG KHÔN, nghe và xem là chính, không luyện tay.

---

## BẢNG MỐC ĐỒNG HỒ CẢ BUỔI

Giả định giờ bắt đầu 08h00. Bắt đầu giờ khác thì cộng dồn tương ứng.

| Khối | Đồng hồ | Phút | Nội dung | Ai làm |
|---|---|---|---|---|
| K0 | 08:00 - 08:10 | 10 | Mở đầu: một nỗi đau chung | Giảng 6 + học viên thao tác 4 |
| K1 | 08:10 - 08:45 | 35 | CLAUDE.md: dạy Claude biết mình là ai | Giảng và demo 13 + thực hành 22 |
| K2 | 08:45 - 08:57 | 12 | Thêm mục lục để Claude tìm file nhanh | Giảng 2 + demo làm theo 4 + thực hành 6 |
| Giải lao | 08:57 - 09:07 | 10 | Nghỉ | |
| K3 | 09:07 - 09:45 | 38 | Skill: đóng gói một việc lặp lại thành nút bấm | Giảng và demo 13 + thực hành 25 |
| K4 | 09:45 - 10:20 | 35 | Đội quân AI: agent, trợ lý phụ, đội nhóm, token | Giảng và demo 28 + thực hành 7 |
| K5 | 10:20 - 10:30 | 10 | Chốt và giao bài | Giảng 10 |

**Cộng lại để tự kiểm:** 10 + 35 + 12 + 10 + 38 + 35 + 10 = **150 phút**, khớp thời lượng khai báo.

**Tay học viên đặt trên bàn phím:** K0 4 phút, K1 22 phút, K2 6 phút, K3 25 phút, K4 7 phút. Cộng khoảng 64 phút trên 140 phút học thật. Nửa đầu (K1 tới K3) là phần tự tay làm, nặng nhất là K3. Nửa sau (K4) gõ ít là có chủ ý: agent và token bản chất là hiểu chứ không phải gõ. Đừng ép biến K4 thành thực hành.

**Mốc phải bám cứng:** 08:45 xong K1. 09:45 xong K3. **Không cắt K1 và K3.** K1 là nền hiểu, K3 là sản phẩm chính học viên mang về.

**Lưu ý cho giảng viên về giao diện:** app Claude Desktop có thể đổi vị trí nút và tên lệnh theo phiên bản. Mọi chỗ bài này mô tả đường bấm hay lệnh gõ, trước buổi phải mở máy kiểm tra lại và ghi ra giấy nhắc. Đừng mô tả theo trí nhớ trước lớp. Các điểm cần kiểm được đánh dấu rõ trong từng khối.

---

## K0. MỞ ĐẦU: MỘT NỖI ĐAU CHUNG (10 phút, 08:00 - 08:10)

### LỜI GIẢNG (6 phút)

"Chào anh chị. Trước khi vào bài, tôi hỏi một câu, anh chị giơ tay thật lòng giúp tôi: ai từng nhận một bài AI viết ra, đọc xong thấy đúng ngữ pháp, câu chữ trơn tru, mà sai hẳn giọng thương hiệu của mình?"

*(Dừng 10 giây. Gần như cả lớp giơ tay. Đây là nỗi đau của buổi, để nguyên đó, chưa vội giải thích.)*

"Đúng rồi, gần như cả lớp. Đó chính là vấn đề của buổi hôm nay. Không phải AI kém. Anh chị đưa cho nó đúng một câu 'viết giúp tôi bài bán hàng', thì nó phải tự đoán. Đoán giọng, đoán khách, đoán công dụng sản phẩm. Mà đoán thì trật. Nó không biết anh chị là ai."

"Hôm nay tôi và anh chị làm đúng một việc: dạy cho Claude hiểu công việc của anh chị, để nó làm như một nhân viên đã quen việc, chứ không phải một người lạ vừa vào cửa. Và cuối buổi, anh chị còn biết một điều nữa: khi việc nhiều quá sức một mình nó, làm sao cho nó thuê thêm trợ lý, huy động cả một đội cùng làm."

"Cách chạy buổi online: tôi chia sẻ màn hình, anh chị vừa nghe vừa làm trên máy mình. Chỗ nào tôi bảo gõ cùng thì anh chị gõ cùng lúc, không ngồi xem. Ai vướng thì bật mic nói ngay hoặc gõ vào khung chat của Zoom, đừng ngồi im, vì các bước sau dựa vào bước trước. Cả buổi hôm nay chỉ dùng Claude Desktop, và chỉ tab **Code** ở trên cùng, không phải tab Chat."

### THAO TÁC HỌC VIÊN (4 phút)

Nói trước: "Bốn phút này ai cũng phải qua được. Ta chỉ mở lại chỗ làm việc của buổi trước, chưa làm gì nặng."

**Bước 1. Mở lại thư mục làm việc.** Đọc từng bước cho lớp làm theo:

1. Mở Claude Desktop.
2. Bấm tab **Code** ở hàng trên cùng.
3. Bấm nút mở thư mục làm việc, trỏ tới thư mục `thao-an-marketing` trên màn hình nền, chọn.

*Lưu ý cho giảng viên: tên nút mở thư mục có thể đổi theo phiên bản app. Kiểm tra trước buổi, ghi ra giấy nhắc.*

**Bước 2. Gõ một câu kiểm tra nhanh, bảo cả lớp gõ cùng.**

**PROMPT B2-0:**

```
Bạn đang mở thư mục nào, và trong thư mục này đang có những file gì?
Trả lời ngắn gọn, không phân tích thêm.
```

**Tiêu chí coi là xong:** mỗi máy mở được thư mục bằng tab Code, và Claude nêu đúng tên thư mục cùng danh sách file. Ai chưa mở được thì xử lý theo DỰ PHÒNG.

### DỰ PHÒNG

- **Máy không mở được thư mục buổi 1, hoặc app cũ không thấy tab Code:** bảo tải bản mới ở claude.ai/download. Trong lúc chờ, ghép nhóm xem chung màn hình một bạn bên cạnh qua Zoom breakout, không ngồi cài giữa giờ.
- **Có người nghỉ buổi 1, hoàn toàn mới:** phát bộ Thảo An mẫu (thư mục `thao-an-marketing` có sẵn `san-pham-thao-an.md`), tải về, mở bằng tab Code, cho bám theo. Họ vẫn theo được cả buổi, vì hôm nay ta viết lại từ đầu chứ không giả định đã hiểu.
- **Thư mục trống trơn, không còn file gì:** không sao, hôm nay K1 sẽ dựng lại. Cho họ tải file `san-pham-thao-an.md` bỏ vào thư mục để có dữ liệu làm việc.

---

## K1. CLAUDE.md: DẠY CLAUDE BIẾT MÌNH LÀ AI (35 phút, 08:10 - 08:45)

**Câu hỏi dẫn cả khối:** Vì sao cùng một câu lệnh, Claude viết cho người này hay, cho người kia dở?

**Mục tiêu khối:** mỗi học viên có một file `CLAUDE.md` viết cho đúng công việc THẬT của chính mình, do chính Claude phỏng vấn rồi viết ra.

**Cộng thời lượng khối:** giảng và demo 13 + thực hành 22 = **35 phút**.

### PHẦN 1: CHO GẶP NỖI ĐAU (demo giảng viên, 4 phút)

"Tôi làm một thí nghiệm trước mặt anh chị. Tôi mở một thư mục hoàn toàn trống, không có gì trong đó cả, và nhờ Claude viết một bài bán hàng cho Thảo An. Anh chị xem nó ra cái gì."

**THAO TÁC DEMO:**

1. Giảng viên mở Claude Desktop, tab **Code**, mở thư mục `demo-trong` rỗng. Chia sẻ màn hình.
2. Nói: "Thư mục này trống trơn. Claude không biết Thảo An là ai, bán gì, giọng thế nào. Đúng như tình trạng máy anh chị lúc mới cài xong."
3. Dán **PROMPT B2-1**, bấm Enter.

**PROMPT B2-1:**

```
Viết cho tôi 1 bài đăng Facebook bán serum rau má B5 của thương hiệu Thảo An.
```

4. Chờ kết quả. Đọc lướt cho lớp nghe, rồi hỏi: "Anh chị soi giúp tôi, bài này sai chỗ nào, chung chung chỗ nào?"

*(Dừng chờ lớp nói. Gợi ý nếu lớp im: "nó có nói đúng giá không, giá đó ở đâu ra?", "nó gọi khách là gì?", "nó có hứa mấy ngày hết thâm không?")*

**Lỗi dự kiến, giảng viên chỉ ra:** bịa hoặc né giá; bịa thành phần; dùng từ cấm như "trị mụn", "trắng da cấp tốc"; hứa thời gian "7 ngày hết thâm"; xưng hô lung tung "chúng tôi", "quý khách"; và quan trọng nhất: thay tên Thảo An bằng tên bất kỳ hãng nào, bài vẫn dùng được. "Cái cuối cùng đó là phép thử tôi muốn anh chị nhớ mãi: một câu mà thay tên thương hiệu nào vào cũng đúng, thì câu đó chưa dùng được."

### PHẦN 2: KHÁI NIỆM HIỆN RA (3 phút)

"Vì sao nó viết dở như vậy? Không phải vì nó kém. Vì nó không có ai giới thiệu cho nó biết Thảo An là ai."

"Anh chị hình dung thế này. Có một bạn cộng tác viên rất giỏi, mới nhận việc sáng nay. Anh chị chưa nói gì đã bắt bạn ấy viết bài bán hàng ngay. Bạn ấy viết sai không phải vì dở, mà vì chưa ai đưa cho bạn ấy tờ giới thiệu: thương hiệu bán gì, bán cho ai, giọng viết thế nào, từ nào cấm dùng."

"**Cái tờ giới thiệu đó, trong Claude Code, chính là file `CLAUDE.md`.** Tên file viết hoa hết chữ CLAUDE, chấm md. Anh chị để nó ngay trong thư mục làm việc, thì mỗi lần mở phiên, việc đầu tiên Claude làm là đọc nó, y như nhân viên mới tới bàn là cầm tờ giới thiệu đọc trước. Không phải anh chị dán lại bối cảnh mỗi lần nữa."

"Chỉ một ý đó thôi. `CLAUDE.md` là tờ giới thiệu anh chị để sẵn cho Claude đọc trước khi làm việc. Giờ tôi cho anh chị thấy nó đổi khác thế nào."

### PHẦN 3: KHOẢNH KHẮC "À RA THẾ" (demo giảng viên, 3 phút)

**THAO TÁC DEMO:**

1. Giảng viên chuyển sang thư mục `demo-day-du`, trong đó đã có sẵn `san-pham-thao-an.md` và `CLAUDE.md` viết xong từ buổi 1.
2. Nói: "Vẫn là Claude đó. Vẫn là tôi gõ. Khác duy nhất: thư mục này có tờ giới thiệu."
3. Dán **PROMPT B2-2**, bấm Enter.

**PROMPT B2-2:**

```
Đọc file CLAUDE.md và file san-pham-thao-an.md trong thư mục này trước.
Sau đó viết cho tôi 1 bài đăng Facebook bán SKU-01 Serum rau má B5 của Thảo An,
nhắm nữ 25 đến 40 tuổi da nhạy cảm hoặc da sau mụn, mục tiêu là người đọc
nhắn tin hỏi thêm.

Chỉ dùng giá, thành phần và công dụng có trong hồ sơ. Không thêm con số nào
ngoài hồ sơ. Chỗ nào thiếu thì ghi "chưa đủ dữ liệu".
```

4. Đặt hai kết quả cạnh nhau. Chỉ vào ba chỗ khác biệt: giá đúng 320.000đ cho 30ml; không còn từ cấm; gọi khách là "bạn", gọi mình là "Thảo An". Nói câu chốt: "Cùng một Claude, cùng một người gõ. Khác nhau đúng một chỗ: có tờ giới thiệu hay không. Giờ tới lượt anh chị viết tờ giới thiệu cho công việc thật của chính mình."

### HOẠT ĐỘNG HỌC VIÊN (22 phút)

Mỗi người làm trên máy mình. Ai có thương hiệu thật thì làm cho thương hiệu mình. Ai chưa có thì làm trên Thảo An.

#### Việc 1 (18 phút): nhờ Claude phỏng vấn rồi viết CLAUDE.md cho công việc thật

**Đề bài đọc cho lớp:** "Đây là việc chính của khối, và tôi muốn anh chị làm theo một cách hơi lạ: anh chị KHÔNG tự ngồi gõ tờ giới thiệu. Anh chị bảo Claude phỏng vấn mình. Nó hỏi từng câu, anh chị trả lời, xong nó viết. Vì sao làm vậy? Vì anh chị hiểu việc của mình rõ nhất, còn Claude biết cần hỏi gì để đủ. Dán prompt B2-3. Ai làm cho thương hiệu thật thì trả lời bằng thông tin thật. Ai dùng Thảo An thì trả lời theo hồ sơ Thảo An."

**PROMPT B2-3:**

```
Tôi muốn bạn giúp tôi viết file CLAUDE.md cho công việc thật của tôi. Đây là
tờ giới thiệu bạn sẽ đọc trước mỗi việc tôi giao trong thư mục này.

Trước khi viết, hãy phỏng vấn tôi. Hỏi TỪNG CÂU MỘT, chờ tôi trả lời rồi mới
hỏi câu tiếp, đừng hỏi dồn một lúc. Hỏi đủ các ý sau:
1. Tôi là ai, làm ở đâu, phụ trách mảng gì.
2. Thương hiệu hoặc sản phẩm tôi phụ trách bán gì, bán cho ai.
3. Ba tới năm đầu việc tôi làm đi làm lại mỗi tuần.
4. Giọng văn: xưng hô thế nào, câu dài hay ngắn, có từ nào cấm dùng không.
5. Kênh tôi đăng hoặc gửi nội dung.

Hỏi xong hết, tóm tắt lại những gì tôi trả lời để tôi xác nhận. Tôi xác nhận
đúng rồi bạn mới viết file CLAUDE.md, đặt ngay trong thư mục làm việc này.

Yêu cầu file: viết ngắn, chỉ đưa vào những thứ LUÔN ĐÚNG cho mọi việc của tôi.
Phần giọng văn phải tả bằng HÀNH VI, ví dụ xưng hô ra sao, câu dài tối đa bao
nhiêu chữ, tối đa mấy emoji; không được chỉ ghi tính từ như "chuyên nghiệp",
"thân thiện", "uy tín". Cuối file thêm ba nguyên tắc chống bịa:
- Chỉ dùng dữ liệu tôi cấp, không tự chế số liệu, thành phần, giá, tên khách.
- Gắn nhãn [DATA THẬT] cho thông tin có thật, [SUY LUẬN] cho phần tự suy ra,
  thiếu hẳn thì ghi "chưa đủ dữ liệu".
- Mọi thứ là bản nháp, tôi là người duyệt cuối, bạn không tự đăng, không tự gửi.
```

**Cách giảng viên đi hỗ trợ (qua Zoom):** mời lần lượt vài người chia sẻ màn hình. Chỉ soi đúng ba thứ: (a) file có tên đúng `CLAUDE.md` và nằm trong thư mục làm việc; (b) mục giọng văn tả bằng hành vi, không phải chỉ liệt kê tính từ; (c) cuối file có đủ ba nguyên tắc chống bịa.

**Tiêu chí coi là xong Việc 1:** trong thư mục có `CLAUDE.md` viết cho đúng công việc của họ, mục giọng văn tả bằng hành vi, cuối file có ba nguyên tắc chống bịa.

#### Việc 2 (4 phút): kiểm tra Claude đã đọc được tờ giới thiệu chưa

**Đề bài:** "Anh chị gõ tiếp một câu để tự kiểm, xem nó đã thuộc việc của mình chưa."

Gõ đúng một câu ngắn (không cần đánh số prompt): `Theo tờ giới thiệu trong thư mục này, tôi phụ trách thương hiệu nào, giọng văn ra sao, và có từ nào cấm dùng?`

**Tiêu chí coi là xong Việc 2:** Claude nhắc lại đúng thương hiệu, giọng văn và từ cấm mà học viên vừa khai, không phải dán lại gì.

**Chốt khối, ghi một câu vào vở:** "`CLAUDE.md` chỉ chứa thứ LUÔN ĐÚNG cho MỌI việc của anh chị. Cái gì chỉ đúng cho một việc, ví dụ quy trình viết một loại bài, thì để dành cho khối sau. Đừng nhồi hết vào đây."

### DỰ PHÒNG

- **Claude hỏi dồn cả 5 câu một lúc thay vì hỏi từng câu:** bảo học viên gõ `Hỏi tôi từng câu một thôi, chờ tôi trả lời rồi hãy hỏi câu tiếp.` Lỗi nhẹ, không sao.
- **Học viên không có thương hiệu thật, ngập ngừng khi phỏng vấn:** cho dùng Thảo An, trả lời theo hồ sơ Thảo An, và giao bài về nhà là viết hồ sơ sản phẩm thật của mình sau theo cấu trúc file `san-pham-thao-an.md`.
- **Claude viết `CLAUDE.md` quá dài, dày đặc:** bảo học viên gõ `Rút gọn lại, chỉ giữ thứ luôn đúng cho mọi việc, bỏ hết quy trình chi tiết của từng việc.` Không viết lại từ đầu.
- **Mục giọng văn lại toàn tính từ như "chuyên nghiệp", "thân thiện":** bảo gõ `Viết lại mục giọng văn bằng hành vi cụ thể: xưng hô ra sao, câu dài tối đa mấy chữ, mở bài bằng gì, tối đa mấy emoji.`
- **Demo bài dở ở Phần 1 ra kết quả tình cờ khá tốt:** dùng phép thử đổi tên. "Bài này không sai hẳn, nhưng anh chị thử thay chữ Thảo An bằng tên hãng bất kỳ xem còn đúng không." Thường vẫn còn lỗi xưng hô và lỗi né giá.

---

## K2. THÊM MỤC LỤC ĐỂ CLAUDE TÌM FILE NHANH (12 phút, 08:45 - 08:57)

**Câu hỏi dẫn:** Thư mục có 20 file, anh chị nhờ "lấy bảng giá sỉ ra" mà không nói file nào, chuyện gì xảy ra?

**Cộng thời lượng khối:** giảng 2 + demo làm theo 4 + thực hành 6 = **12 phút**. Đây là phần mở rộng nhẹ của K1, cùng một file, nên ngắn.

### LỜI GIẢNG (2 phút)

"Hôm nay thư mục anh chị mới vài file thì Claude tìm dễ. Nhưng làm thật một thời gian, thư mục phình ra: hồ sơ sản phẩm, bảng giá lẻ, bảng giá sỉ, review khách, thư mục ảnh, thư mục bài đã đăng. Lúc đó anh chị nhờ 'lấy bảng giá sỉ' mà không nói file nào, Claude phải quét cả thư mục để đoán. Vừa chậm, đôi khi mở nhầm file."

"Nhiều người nghĩ giải pháp là tạo một file mục lục riêng, kiểu `index.md`. Tôi nói thẳng để anh chị khỏi mất công: **KHÔNG cần file mục lục riêng.** Vì file riêng thì Claude không tự đọc, chỉ đọc khi anh chị bảo. File mục lục riêng chủ yếu để con người mở ra xem, có cũng được, nhưng không giúp Claude."

"Cách đúng đơn giản hơn nhiều: **viết 5 tới 10 dòng mô tả thư mục ngay vào trong `CLAUDE.md`.** Vì `CLAUDE.md` là thứ nó đọc mỗi phiên, nên khi anh chị mô tả sẵn 'file bang-gia-si.md chứa chính sách sỉ, thư mục assets chứa ảnh sản phẩm', thì ngay đầu phiên nó đã biết đường. Anh chị nhờ lấy bảng giá sỉ, nó mở thẳng đúng file. Mục lục cho người thì để file riêng cũng được; mục lục cho Claude thì viết thẳng vào `CLAUDE.md`."

### THAO TÁC DEMO LÀM THEO (4 phút)

**Bốn phút này học viên gõ cùng lúc trên máy mình, không ngồi xem.** Giảng viên demo trên thư mục Thảo An, cả lớp làm song song trên thư mục của mình.

**Câu dặn:** "Anh chị đặt tay lên bàn phím. Tôi gõ gì anh chị gõ nấy. Tôi đi chậm và dừng chờ."

1. Giảng viên mở thư mục Thảo An bằng tab Code. Nhắc lớp mở thư mục của mình.
2. Dán **PROMPT B2-4**, bấm Enter. Nói to: "dán cùng tôi, bấm Enter cùng tôi."

**PROMPT B2-4:**

```
Quét giúp tôi thư mục làm việc này: có những file và thư mục con nào, mỗi cái
dùng cho việc gì. Chỉ liệt kê đúng những gì đang có thật, không bịa thêm file
chưa tồn tại.

Sau đó thêm vào file CLAUDE.md một mục mới tên "Cấu trúc thư mục". Trong mục
đó viết 5 tới 10 dòng, mỗi dòng ghi tên một file hoặc thư mục và một câu nói
nó chứa gì, dùng khi nào. Mục tiêu: lần sau tôi nhờ một việc, bạn biết ngay
phải mở file nào mà không phải quét lại cả thư mục.

Viết xong, đọc lại nguyên mục đó cho tôi xem.
```

3. **Điểm dừng bắt buộc:** dừng, hỏi "ai đã thấy Claude ghi thêm mục Cấu trúc thư mục vào file, khớp với thư mục thật của mình, thì giơ tay hoặc gõ chat". Chờ hai phần ba lớp.

*Lưu ý cho giảng viên: nếu thư mục Thảo An demo còn ít file, kết quả sẽ nghèo nàn. Trước buổi bỏ thêm vài file mẫu vào thư mục demo, ví dụ `bang-gia-si.md`, thư mục `assets`, để lớp thấy rõ ích lợi.*

### HOẠT ĐỘNG HỌC VIÊN (6 phút)

**Đề bài:** "Anh chị đã thêm mục Cấu trúc thư mục ở bước demo rồi. Giờ kiểm tra xem nó dùng được không. Gõ đúng câu này."

Gõ một câu thử (không cần đánh số): `Nếu bây giờ tôi nhờ bạn cập nhật hồ sơ sản phẩm, bạn sẽ mở file nào trong thư mục này, vì sao?`

"Anh chị thấy chưa, nó trả lời thẳng tên file, không quét lại. Đó là tác dụng của mấy dòng vừa thêm. Nó đọc `CLAUDE.md` mỗi phiên nên biết ngay."

**Tiêu chí coi là xong:** trong `CLAUDE.md` của mỗi học viên có mục "Cấu trúc thư mục" 5 tới 10 dòng, và Claude trả lời đúng tên file khi hỏi thử.

### DỰ PHÒNG

- **Có người hỏi lại "vậy file index.md có ích gì không":** trả lời ngắn "để người đọc thì tốt, để Claude thì không bắt buộc. Hôm nay ta không tạo, viết thẳng vào `CLAUDE.md` là đủ." Đừng vẽ ra tính năng không có.
- **Claude thêm nhầm cả file chưa tồn tại vào mục cấu trúc:** bảo học viên gõ `Chỉ liệt kê đúng file đang có thật trong thư mục, bỏ file nào bạn không thấy.`
- **Thư mục học viên chỉ có một file:** cho họ ghi mục cấu trúc dạng "hiện có 1 file X, sau này sẽ thêm bảng giá và ảnh", coi như khung để lần sau bổ sung. Không sao.

---

## GIẢI LAO (10 phút, 08:57 - 09:07)

**Việc giảng viên làm trong lúc lớp nghỉ:**

- Rà nhanh: máy nào chưa có `CLAUDE.md` cho việc thật thì ghi tên, đầu K3 hỗ trợ, đừng để họ vào K3 với thư mục trống.
- Kiểm tra máy giảng viên: thư mục Thảo An demo còn đủ file không, chạy thử được prompt K3 không.
- Chiếu sẵn lên màn hình: khung frontmatter 2 dòng và khung 6 phần của SKILL.md, để nguyên đó suốt K3.

---

## K3. SKILL: ĐÓNG GÓI MỘT VIỆC LẶP LẠI THÀNH NÚT BẤM (38 phút, 09:07 - 09:45, đỉnh của buổi)

**Câu hỏi dẫn:** Việc nào anh chị làm đi làm lại mỗi tuần mà lần nào cũng phải dặn Claude từ đầu?

**Mục tiêu khối:** mỗi học viên lập được một skill MỚI cho một việc thật của mình, đặt đúng chỗ trong thư mục làm việc, chạy thử ra kết quả, và biết sửa khi nó chưa đúng.

**Cộng thời lượng khối:** giảng và demo 13 + thực hành 25 = **38 phút**. Đây là phần quan trọng nhất buổi và cũng là phần anh chị mang về dùng được ngay. K3 được để ngay sau giải lao lúc não còn khỏe, và được nhiều thời gian nhất vì người lập skill lần đầu sẽ vấp, cần giờ sửa cùng nhau.

### PHẦN 1: NỖI ĐAU VÀ KHÁI NIỆM (5 phút)

"Tôi hỏi thật: có việc nào tuần nào anh chị cũng làm, mà lần nào mở Claude lên cũng phải dặn lại từ đầu không? Viết bài bán serum, mở ra dặn lại giọng. Soạn email chào spa, mở ra dặn lại chính sách sỉ. Mỗi lần dặn một kiểu, kết quả ra không đều. Mệt, và chán."

*(Dừng cho vài người gật hoặc kể việc của họ.)*

"Nỗi đau đó có một lời giải, gọi là **skill.** Tôi giải thích lại từ đầu, không giả định anh chị đã hiểu từ buổi 1."

"Anh chị hình dung skill như một **công thức nấu ăn** dán trong bếp. Món phở nhà anh chị nấu, nếu mỗi lần nấu lại nhớ mang máng thì hôm mặn hôm nhạt. Nhưng nếu anh chị viết ra công thức một lần cho chuẩn: bao nhiêu nước, hầm mấy tiếng, nêm mấy thìa, thì lần sau ai cầm công thức cũng nấu ra đúng vị đó. Skill là cái công thức đó, nhưng cho một đầu việc: viết bài bán hàng, soạn email chào sỉ, trả lời tin nhắn hỏi giá."

"Đóng gói một lần. Sau đó anh chị chỉ gõ một câu ngắn, nó chạy đúng theo công thức, ra đúng chuẩn, không phải dặn lại. Đó là 'nút bấm' trong tên khối này."

"Khác với `CLAUDE.md` thế nào? `CLAUDE.md` là tờ giới thiệu, nó đọc trước MỌI việc. Skill là công thức cho MỘT việc, chỉ lấy ra khi đúng việc đó. Vì chỉ lấy khi đúng việc, skill được phép dài, được phép chi tiết tới từng bước."

### PHẦN 2: NHỜ CLAUDE LÀM CỐ VẤN, NÊN ĐÓNG GÓI VIỆC NÀO (demo và thực hành, 8 phút)

"Câu khó là: trong đống việc của anh chị, cái nào đáng bỏ công đóng gói thành skill? Tin vui: anh chị không phải tự đoán. Người trả lời tốt nhất chính là Claude, vì nó vừa đọc tờ giới thiệu của anh chị, nó biết anh chị làm gì. Tôi demo cách hỏi trên Thảo An, rồi anh chị hỏi cho việc của mình."

**THAO TÁC DEMO (giảng viên, 3 phút):**

1. Mở thư mục Thảo An bằng tab Code.
2. Dán **PROMPT B2-5**, bấm Enter.

**PROMPT B2-5:**

```
Đọc file CLAUDE.md trong thư mục này để hiểu công việc của tôi.

Sau đó tư vấn cho tôi: trong các đầu việc tôi làm mỗi tuần, việc nào đáng
đóng gói thành skill nhất, việc nào chưa cần. Trả lời đúng 3 mục, ngắn gọn:

1. Việc đáng làm skill nhất là việc nào, vì sao. Việc nào chưa cần, vì sao.
2. Với việc đáng làm nhất, đề xuất tên skill (viết không dấu, nối bằng gạch
   nối) và viết sẵn giúp tôi dòng description thật rõ: nêu ba tình huống tôi
   sẽ gọi skill ra và một tình huống KHÔNG dùng.
3. Nếu chỉ làm một việc ngay hôm nay, bạn khuyên làm cái nào trước.

Chỗ nào phải suy đoán thì ghi [SUY LUẬN].
```

3. Chiếu kết quả. Nói: "Anh chị để ý, nó không nói chung chung. Nó chỉ ra việc soạn email chào sỉ đáng làm skill, đặt tên `soan-email-chao-si`, viết sẵn cả dòng description. Lát nữa tôi lấy đúng gợi ý này để lập skill thật. Đây là cách dùng Claude làm cố vấn: nó vạch việc, mình chọn."

**THỰC HÀNH (học viên, 5 phút):** "Giờ tới lượt anh chị. Dán prompt B2-5 y hệt, vì nó đã bảo Claude đọc tờ giới thiệu của chính anh chị rồi, không cần sửa. Đọc kỹ ba mục nó trả lời, nhất là mục 2, vì dòng description đó anh chị dùng ngay ở bước sau. Ai chưa ưng tên nó đề xuất thì gõ `Đề xuất tên khác cụ thể hơn và viết lại description tách bạch hẳn với các việc còn lại của tôi.`"

### PHẦN 3: LẬP SKILL MỚI (demo làm theo, 5 phút, và thực hành)

**Năm phút demo này học viên gõ cùng lúc.** Giảng viên lập skill `soan-email-chao-si` trên Thảo An. Học viên lập skill mà Claude vừa gợi ý cho mình.

**NHẤN MẠNH TRƯỚC KHI GÕ, đọc nguyên văn cho lớp:** "Anh chị nghe kỹ chỗ đặt skill, vì đây là điểm nhiều người làm sai. Skill của anh chị đặt ở `.claude/skills/<tên-skill>/SKILL.md`, và cái này quan trọng: **nó nằm NGAY TRONG thư mục làm việc hiện tại của anh chị**, tức trong thư mục `thao-an-marketing`, chứ không phải một chỗ chung nào đó trên máy."

"Vì sao phải nằm trong thư mục hiện tại? Hai lý do. Một, để skill chỉ áp cho đúng dự án này. Skill soạn email chào sỉ cho Thảo An thì chỉ nên bật ở thư mục Thảo An, không lẫn sang việc khác. Hai, để sau này đưa lên mạng chia cho đồng đội được. Skill nằm gọn trong thư mục dự án thì cả đội tải về là có ngay. Skill để lung tung ở bản cá nhân riêng máy anh chị thì không ai chia được, không gắn với dự án nào cả. Anh chị ghi vào vở: skill để trong thư mục làm việc, đường dẫn `.claude/skills/<tên>/SKILL.md`."

"Và tin mừng: anh chị KHÔNG phải tự tạo mấy thư mục lồng nhau đó bằng tay. Cứ bảo Claude tạo, nó tạo hết. Thư mục bắt đầu bằng dấu chấm như `.claude` bị Windows ẩn đi, tạo tay dễ sai, để Claude làm cho chắc."

1. Dán **PROMPT B2-6**, bấm Enter. Nói to "dán cùng tôi". Nhắc lớp đổi tên skill và mô tả cho đúng việc của mình.

**PROMPT B2-6:**

```
Tạo cho tôi một skill mới trong thư mục làm việc này.

Đường dẫn file: .claude/skills/soan-email-chao-si/SKILL.md
Đặt đúng trong thư mục làm việc hiện tại. Nếu thư mục .claude hoặc
.claude/skills chưa có thì tạo luôn.

File bắt đầu bằng phần frontmatter kẹp giữa hai dòng ba dấu gạch, bên trong
có đúng 2 dòng name và description.
- name: soan-email-chao-si
- description: viết thật kỹ. Nêu rõ đây là skill soạn email chào bán sỉ B2B
  cho spa và cửa hàng; ba tình huống gọi nó ra là chào sỉ lần đầu, gửi báo
  giá sỉ theo yêu cầu, nhắc lại sau khi khách im; và nói rõ KHÔNG dùng cho
  bài đăng bán lẻ Facebook.

Phần dưới frontmatter viết bằng markdown, đủ 6 mục:
1. Skill này làm gì: 3 dòng.
2. Đầu vào bắt buộc: gửi cho loại khách sỉ nào, họ quan tâm SKU nào, chính
   sách sỉ hiện có là gì, mục tiêu email là gì.
3. Các bước làm: đánh số. Bước 1 bắt buộc là kiểm tra đủ đầu vào, thiếu thì
   hỏi lại tôi, tuyệt đối không tự đoán. Trong các bước phải có: đọc CLAUDE.md
   lấy giọng và danh sách từ cấm; nêu lợi ích cho người bán sỉ chứ không chỉ
   tả sản phẩm; kết bằng một đề nghị hành động rõ ràng.
4. Ràng buộc: chép danh sách từ cấm và quy tắc giọng từ CLAUDE.md của thư mục
   này. Email dài 120 tới 200 chữ, có dòng tiêu đề email rõ ràng.
5. Định dạng đầu ra: dòng tiêu đề email, phần thân, câu kết đề nghị, rồi phần
   gắn nhãn [DATA THẬT] và [SUY LUẬN].
6. Ví dụ mẫu: viết luôn 1 email hoàn chỉnh chào sỉ SKU-01 Serum rau má B5 cho
   một spa, dùng đúng giá và thành phần trong hồ sơ sản phẩm.

Viết bằng tiếng Việt có dấu, câu ngắn, người không rành máy tính đọc là làm
theo được. Không dùng thuật ngữ lập trình.
```

2. **Điểm dừng bắt buộc 1:** hỏi "ai đã thấy Claude báo tạo xong file `SKILL.md` mới thì giơ tay hoặc gõ chat". Chờ hai phần ba lớp. Máy nào chưa ra, trợ giảng hoặc giảng viên xem màn hình người đó. Mở file ra, chỉ vào đường dẫn `.claude/skills/soan-email-chao-si/SKILL.md`, nhắc lại: "thấy chưa, nó nằm trong thư mục làm việc của mình."

### PHẦN 4: CHẠY THỬ, CỐ Ý BỎ TRỐNG, VÀ SỬA (thực hành, phần chính)

Đây là lý do K3 được nhiều giờ. Chia 25 phút thực hành như sau: lập và hoàn thiện skill 10 phút, chạy thử 8 phút, sửa lỗi 7 phút.

#### Việc 1 (10 phút): hoàn thiện skill của mình

**Đề bài:** "Anh chị hoàn thiện skill mình vừa lập theo gợi ý Claude đưa ở Phần 2. Ai làm skill trả lời tin nhắn, ai làm skill soạn báo giá, ai làm skill dựng kịch bản video, cứ theo việc mình chọn. Mở file `SKILL.md` ra đọc lại, sửa tay chỗ nào chưa đúng, hoặc bảo Claude sửa."

**Cách giảng viên đi hỗ trợ:** mời vài người chia sẻ màn hình, soi đúng một chỗ là dòng `description`. Hỏi: "nếu tuần sau anh chị lập thêm một skill khác, đọc dòng này Claude có phân biệt được hai cái không?" Nếu không, bảo gõ `Viết lại dòng description cho tách bạch hẳn với các skill khác của tôi.`

**Tiêu chí xong Việc 1:** có file `SKILL.md` mới đúng đường dẫn `.claude/skills/<tên>/SKILL.md` trong thư mục làm việc, frontmatter đủ 2 dòng, dòng description có nêu cả tình huống KHÔNG dùng.

#### Việc 2 (8 phút): chạy thử, cố ý bỏ trống để thấy nó hỏi lại

**Đề bài:** "Giờ ta thử xem công thức có chạy không. Và tôi muốn anh chị làm một việc lạ: cố ý bỏ trống thông tin, xem nó phản ứng ra sao."

**Bước 1, cố ý thiếu.** Gõ một yêu cầu CỐ Ý thiếu (không đánh số prompt): `Dùng skill soan-email-chao-si soạn cho tôi một email.` (ai làm skill khác thì thay tên skill).

"Anh chị nhìn kỹ: nó có tự bịa ra một email không, hay nó hỏi ngược lại anh chị gửi cho khách nào, SKU nào, mục tiêu là gì? Nếu nó hỏi lại, tức là công thức chạy đúng: trong bước 1 anh chị đã bắt nó kiểm tra đủ đầu vào. Đây chính là thứ giúp anh chị yên tâm giao việc: nó không bịa, nó hỏi."

**Bước 2, chạy thật với đầy đủ đầu vào.** Gõ **PROMPT B2-7** (đầy đủ, để ra kết quả thật):

**PROMPT B2-7:**

```
Dùng skill soan-email-chao-si soạn cho tôi một email, làm đúng từng bước
trong skill, không bỏ bước nào.

- Loại khách sỉ: một spa vừa mở, chưa từng nhập hàng của tôi.
- SKU họ quan tâm: SKU-01 Serum rau má B5.
- Chính sách sỉ: [nếu hồ sơ chưa có thì để Claude tự ghi "chưa đủ dữ liệu"].
- Mục tiêu email: spa đồng ý nhận bảng giá sỉ và mẫu thử.

Chỉ dùng giá, thành phần, công dụng có trong hồ sơ sản phẩm. Không thêm con
số nào ngoài hồ sơ. Thiếu thì ghi "chưa đủ dữ liệu". Cuối email gắn nhãn
[DATA THẬT] và [SUY LUẬN].
```

"Anh chị để ý chỗ chính sách sỉ tôi để trống. Nó không được bịa ra mức chiết khấu. Nó phải ghi 'chưa đủ dữ liệu'. Đó là dấu hiệu skill và ba nguyên tắc chống bịa đang chạy đúng."

**Tiêu chí xong Việc 2:** skill hỏi lại khi thiếu đầu vào; và khi cấp đủ, ra được một kết quả thật, không dính từ cấm, có phần gắn nhãn nguồn ở cuối.

#### Việc 3 (7 phút): giờ sửa lỗi

**Đề bài:** "Skill không phải viết một lần là xong. Người lập lần đầu bao giờ cũng có chỗ mơ hồ. Ta sửa ngay bây giờ, cùng nhau."

"Ai gặp lỗi gì thì đây là lúc gỡ. Lỗi hay gặp: skill viết bài vẫn dính từ cấm; skill không hỏi lại mà viết luôn; email ra sai giọng. Cách sửa chung là **sửa công thức, không sửa kết quả.** Ví dụ nó dính từ cấm, đừng xóa tay từ đó trong email. Bảo nó: `Trong file SKILL.md, mục Ràng buộc, thêm nguyên danh sách từ cấm và thêm một bước bắt buộc dò lại toàn bài với danh sách đó trước khi trả kết quả.` Rồi chạy lại."

"Ai không gặp lỗi thì làm việc này cho chắc: bảo chính Claude soi lại skill của nó." Gõ (không đánh số): `Đóng vai người kiểm tra và soi lại file SKILL.md vừa tạo: bước nào còn chung chung khiến bạn phải tự đoán, đầu vào nào lẽ ra phải bắt buộc mà đang bỏ sót. Chỉ ra rồi sửa lại file, giữ nguyên cấu trúc 6 mục.`

**Câu chốt cuối K3:** "Anh chị vừa đi trọn một vòng của nghề: viết công thức, chạy thử, thấy chỗ hở, sửa. Trong marketing anh chị gọi vòng đó là tối ưu. Skill cũng vậy. Chạy ba lần trong tuần là anh chị biết ngay chỗ nào phải sửa. Và nhớ: skill này nằm trong thư mục làm việc của anh chị, nên nó gắn với đúng dự án này, và sau này chia cho đồng đội được."

### DỰ PHÒNG

- **Hết giờ Việc 1 chưa xong skill:** cho họ dùng luôn bản Claude vừa trả, không chau chuốt, chuyển ngay sang chạy thử. Thà chạy được một bản chưa hoàn hảo còn hơn ngồi mãi ở khâu viết.
- **Skill không hỏi lại mà viết luôn:** bảo gõ `Trong file SKILL.md, sửa bước 1 thành: bắt buộc kiểm tra đủ đầu vào, thiếu bất kỳ cái nào thì DỪNG và hỏi lại, tuyệt đối không tự đoán.` Rồi chạy lại. Bài học: sửa quy trình, không sửa kết quả.
- **Claude không nhận ra skill, viết kiểu chung chung:** kiểm tra đường dẫn có đúng `.claude/skills/<tên>/SKILL.md` trong thư mục làm việc không, bằng cách gõ `Liệt kê các skill đang có trong thư mục này kèm đường dẫn.` Gọi đích danh tên skill trong prompt.
- **Skill viết bài vẫn dính từ cấm:** không sửa tay kết quả. Sửa mục Ràng buộc trong SKILL.md như trên. Đây chính là bài học của khối.
- **Người xong sớm cả khối:** cho lập skill thứ hai cho một việc khác của họ, hoặc thêm mục "Khi nào KHÔNG dùng skill này" liệt kê 2 tình huống dễ nhầm.
- **Mạng chậm hoặc tài khoản báo hết lượt:** ghép chung máy với người bên cạnh qua Zoom, mỗi người giữ file của mình. Ghi tên để nhắc làm bù ở bài về nhà.

---

## K4. ĐỘI QUÂN AI: AGENT, TRỢ LÝ PHỤ, ĐỘI NHÓM, TOKEN (35 phút, 09:45 - 10:20)

Cả khối dùng MỘT ẩn dụ xuyên suốt: **một công ty thu nhỏ.** Bắt đầu từ cái anh chị đã biết, mở rộng dần. **Phần này nghe và xem là chính, chỉ có một hoạt động nhẹ ở cuối. Không luyện tay tạo agent.**

**Câu hỏi dẫn:** "Nãy giờ anh chị làm việc với Claude như giao việc cho đúng một nhân viên. Vậy khi việc phình to quá sức một người thì sao?"

**Cộng thời lượng khối:** giảng và demo 28 + thực hành 7 = **35 phút**.

### PHẦN 1: AGENT LÀ NHÂN VIÊN, SUBAGENT LÀ TRỢ LÝ PHỤ (giảng 8 phút)

"**Một, agent, cái anh chị đã dùng cả buổi mà chưa gọi tên.** Từ đầu khóa tới giờ, mỗi lần anh chị mở tab Code và làm việc với Claude, anh chị đang có một nhân viên: nó tự đọc tài liệu, tự làm, mang kết quả về. Cái đó gọi là **agent.** Anh chị đã dùng nó cả hai buổi rồi. Hôm nay chỉ đặt tên cho nó thôi. Một agent là một nhân viên anh chị đang giao việc."

"**Hai, khi việc phình to.** Anh chị nhờ nhân viên đó vừa đi nghiên cứu đối thủ, vừa viết bài, cùng một lúc. Nó làm thì rối, lẫn lộn, bàn làm việc đầy giấy tờ của cả hai việc. Cái này có thật, không phải tôi bịa ra, anh chị thử là gặp ngay."

"Ngoài đời anh chị làm gì? Anh chị bảo nhân viên đó thuê thêm một **trợ lý phụ**, giao bớt mảng nghiên cứu cho trợ lý. Trợ lý ngồi phòng riêng đọc tài liệu, xong chỉ mang về cho nhân viên chính một bản tóm tắt. Bàn của nhân viên chính vẫn gọn. Cái trợ lý phụ đó, trong Claude, gọi là **subagent.**"

"Ba điều về subagent, ghi vào vở:"

1. "Nó làm trong vùng riêng của nó, tách khỏi phần trò chuyện chính của anh chị. Giao cho nó đọc mười file dài, nó đọc trong phòng nó, phiên chính của anh chị vẫn sạch."
2. "Nó làm xong chỉ trả về phần kết luận, không đổ hết nội dung ra. Bảo nó đọc mười review rồi tóm tắt năm dòng, nó đưa anh chị đúng năm dòng."
3. "Các trợ lý phụ không nói chuyện với nhau. Mỗi trợ lý chỉ báo về sếp chính. Nhớ điểm này, vì lát nữa nó là chỗ khác với đội nhóm."

"**Cách gọi trợ lý phụ ra làm việc, đây là điểm tôi muốn anh chị nhớ kỹ vì nó dễ tới bất ngờ:** anh chị không phải cài gì, không phải gõ lệnh gì. Anh chị chỉ cần NÓI BẰNG LỜI. Ví dụ gõ cho Claude: 'Dùng một trợ lý phụ đọc giúp tôi các file trong thư mục này rồi tóm tắt 5 dòng.' Thế là xong. Claude tự lập trợ lý phụ, giao việc, nhận kết quả, đưa lại cho anh chị. Muốn nó làm hai việc song song thì nói 'làm việc A và việc B song song'. Nói bằng tiếng Việt bình thường, nó hiểu."

*(Ghi chú cho giảng viên: muốn tạo một trợ lý phụ chuyên biệt gọi bằng tên thì đó là custom agent, đặt ở `.claude/agents/<tên>.md` trong thư mục làm việc, cùng nguyên tắc như skill. Vị trí này kiểm trên máy trước buổi vì có thể đổi theo phiên bản. Lớp hôm nay chỉ dạy gọi bằng lời, không dạy tạo custom agent.)*

### PHẦN 2: DEMO TRỢ LÝ PHỤ (demo giảng viên, 6 phút)

**Giảng viên demo, cả lớp xem. Không phải demo làm theo. Mục tiêu là thấy khái niệm chạy thật, không luyện tay.**

1. Mở thư mục Thảo An bằng tab Code.
2. Dán **PROMPT B2-8**, bấm Enter.

**PROMPT B2-8:**

```
Dùng một trợ lý phụ (subagent) để làm việc này, giữ cho phần trò chuyện chính
của chúng ta gọn gàng.

Giao cho trợ lý phụ: đọc toàn bộ các file trong thư mục làm việc này, rồi trả
về đúng một đoạn tóm tắt 5 dòng: thư mục này đang có gì, dùng cho việc gì.
Chỉ trả về bản tóm tắt 5 dòng, không đổ hết nội dung file ra đây.
```

3. Chiếu kết quả. Chỉ vào hai chỗ: chỗ Claude báo đang dùng một trợ lý phụ, và chỗ nó chỉ trả về đúng 5 dòng. Nói: "Anh chị thấy chưa, nó không đổ hết nội dung file ra màn hình. Trợ lý phụ đọc trong phòng riêng, chỉ mang về cho tôi phần kết luận. Nếu tôi tự đọc, cả đống nội dung sẽ chất vào phiên chính, vừa rối vừa tốn tiền. Đó là ích lợi thật của trợ lý phụ, và tôi chỉ cần nói bằng lời là nó chạy."

*Lưu ý cho giảng viên: cách Claude báo đang dùng subagent hiển thị khác nhau theo phiên bản. Chạy thử trước buổi để biết trên máy mình nó hiện ra sao, chỉ đúng chỗ đó cho lớp. Trên màn hình người dùng thường thấy tên trợ lý phụ và phần tóm tắt nó mang về.*

### PHẦN 3: ĐỘI NHÓM AGENT TEAM (giảng 6 phút, chỉ hiểu)

"Mở rộng thêm một bước. Trợ lý phụ là một người giúp việc, chỉ báo về sếp. Nhưng có việc lớn cần cả một **đội** nhiều người, và họ phải nói chuyện với nhau, không chỉ báo về sếp. Cái đó gọi là **agent team**, đội nhiều agent."

"Khác trợ lý phụ ở đâu? Trợ lý phụ chỉ báo về sếp chính. Còn đội nhóm thì các thành viên nhắn tin trực tiếp cho nhau, chia chung một bảng việc, bàn với nhau rồi ra một kết luận chung."

"Ví dụ trong nghề anh chị: soát một chiến dịch lớn trước khi tung, từ ba góc cùng lúc. Một người soi đúng luật, ngành mỹ phẩm có phạm từ cấm không. Một người soi đúng brand, có sai giọng thương hiệu không. Một người soi đúng insight, có trúng nỗi đau khách không. Ba góc đó bàn với nhau, rồi ra một bản kết luận chung. Việc kiểu đó đội nhóm hợp hơn một trợ lý phụ."

"**Nhưng đây là chỗ tôi phải nói rõ, lần thứ nhất: đội nhóm agent team hiện là tính năng THỬ NGHIỆM.** Nó chưa ổn định, còn phải bật một cờ đặc biệt mới chạy. Vì vậy hôm nay chúng ta CHỈ hiểu khái niệm và biết khi nào cần, KHÔNG thực hành. Anh chị ghi vào vở: đội nhóm là thứ để dành, biết trước để sau này khi nó ổn định thì mình dùng."

"**Nhắc lại lần thứ hai cho chắc:** hôm nay không ai mở đội nhóm ra chạy. Đây là phần để hiểu, không phải để làm. Ai về nhà tự bật thử mà gặp lỗi thì đó là bình thường, vì tính năng chưa ổn định."

### PHẦN 4: TOKEN LÀ TIỀN CÔNG (giảng 8 phút, gồm dẫn vào hoạt động)

"Khép lại ẩn dụ công ty. Nhân viên, trợ lý, cả đội, ai làm cũng phải trả công. Công tính theo số chữ họ đọc và viết. Đó là **token.**"

"**Token là mẩu nhỏ của chữ.** Không phải một chữ, không phải một câu, mà là mẩu nhỏ hơn. Tiếng Anh trung bình khoảng 4 ký tự là một token. Anh chị hình dung như tính tiền taxi theo từng đoạn ngắn: đi càng xa càng nhiều đoạn, trả càng nhiều. Chữ càng nhiều, token càng nhiều, tiền càng nhiều."

"Hai điều nên nhớ. **Một, tính tiền cả hai chiều.** Thứ anh chị gửi đi và thứ Claude trả lại đều tính token. Và thứ Claude trả lại thường đắt hơn thứ anh chị gửi, khoảng bốn tới năm lần. Nên phần đắt là khi anh chị bảo nó viết dài, không phải câu lệnh ngắn anh chị gõ. **Hai, mỗi phiên có sức chứa giới hạn, khoảng 200 nghìn token.** Anh chị hình dung như mặt bàn: để được chừng đó giấy tờ. Gần đầy thì Claude tự dọn bớt, nén lại phần lịch sử cũ để lấy chỗ, và lúc đó nó có thể quên vài chi tiết đầu buổi. Đó là lý do đừng kéo một phiên chạy cả ngày, đừng nhồi hàng chục file vào một phiên."

"**Và điều này quan trọng riêng cho anh chị: tiếng Việt tốn token hơn tiếng Anh.** Vì tiếng Việt có dấu, dấu làm mỗi chữ bị chẻ thành nhiều mẩu hơn. Cùng một ý, viết tiếng Việt tốn nhiều hơn, thường khoảng gấp rưỡi tới gấp đôi. Anh chị không cần vì thế mà viết tiếng Anh, khách anh chị là người Việt. Nhưng anh chị hiểu vì sao phải giữ `CLAUDE.md` ngắn và đừng nhồi file thừa: mỗi chữ tiếng Việt đắt hơn anh chị tưởng."

"**Xem token ở đâu?** Anh chị ghi mấy lệnh này vào vở, gõ ngay trong tab Code:"

*(Chiếu bảng, đọc từng dòng.)*

| Gõ lệnh | Nó cho anh chị thấy |
|---|---|
| `/context` | Một lưới màu, cho biết mục nào đang chiếm nhiều token, gợi ý chỗ tối ưu |
| `/usage` hoặc `/cost` | Chi phí và tổng token đã dùng |
| `/compact` | Nén lịch sử cũ lại để lấy lại chỗ khi phiên gần đầy |

*Lưu ý cho giảng viên: tên và cách hoạt động của các lệnh `/context`, `/usage`, `/cost`, `/compact` có thể khác theo phiên bản app. Trước buổi phải mở tab Code gõ thử từng lệnh, xác nhận nó chạy và nó hiện ra gì, ghi ra giấy nhắc. Nếu một lệnh không có trên phiên bản của lớp thì bỏ lệnh đó, đừng dạy lệnh không chạy.*

"**Bốn mẹo tiết kiệm, ghi vào vở:** một, giữ `CLAUDE.md` ngắn, nó đọc lại mỗi phiên nên mỗi dòng thừa là tiền thừa mỗi lần. Hai, đừng nhồi file thừa, chỉ mở đúng file cần, đây cũng là lý do khối 2 ta viết mô tả cấu trúc thư mục. Ba, việc phụ nặng thì giao trợ lý phụ, để nó đọc trong phòng riêng. Bốn, phiên dài quá thì gõ `/compact` hoặc mở phiên mới cho việc mới."

### HOẠT ĐỘNG HỌC VIÊN (7 phút)

**Đây là hoạt động nhẹ duy nhất của K4. Cho Claude ước lượng token một đoạn thật, để lớp thấy con số, rồi thôi.**

**Đề bài đọc cho lớp:** "Anh chị làm việc này để thấy token bằng con số, không phải lý thuyết. Dán prompt B2-9. Chỗ đoạn văn, anh chị dán một đoạn tiếng Việt khoảng một trăm chữ của chính mình, ví dụ một bài anh chị từng đăng."

**PROMPT B2-9:**

```
Tôi muốn hiểu về token bằng con số. Làm giúp tôi 3 việc:

1. Ước lượng đoạn văn tiếng Việt sau tốn khoảng bao nhiêu token:
[dán một đoạn tiếng Việt khoảng 100 chữ của anh chị vào đây]

2. Dịch đoạn đó sang tiếng Anh, rồi ước lượng lại token của bản tiếng Anh.
   So sánh hai con số và giải thích ngắn vì sao khác nhau.

3. Ước lượng file CLAUDE.md hiện tại của tôi tốn khoảng bao nhiêu token mỗi
   phiên, và gợi ý một chỗ có thể rút gọn để tiết kiệm.
```

**Điểm giảng viên nói to giữa hoạt động:** "Anh chị nhìn hai con số ở mục 2. Bản tiếng Việt tốn nhiều token hơn bản tiếng Anh cùng nội dung. Đó không phải lỗi, đó là do dấu. Và mục 3 cho anh chị thấy `CLAUDE.md` của mình tốn bao nhiêu mỗi phiên. Giờ anh chị hiểu vì sao tôi bảo giữ nó ngắn."

**Tiêu chí coi là xong:** mỗi học viên thấy được ba con số ước lượng token, và đọc được gợi ý rút gọn `CLAUDE.md` của chính mình.

**Kết khối, đọc nguyên văn:** "Chốt lại cả đội quân AI cho gọn. **Việc thường thì một nhân viên**, tức một agent, anh chị đã dùng cả khóa. **Việc phụ nặng thì thêm trợ lý phụ**, tức subagent, nhờ bằng lời là chạy, dùng được ngay hôm nay. **Việc lớn nhiều góc thì cả đội**, tức agent team, để dành vì còn thử nghiệm. **Và cái gì cũng tốn công, tính bằng token, nên viết gọn.**"

### DỰ PHÒNG

- **Có người hỏi con số token có chính xác tuyệt đối không:** trả lời thẳng "đây là ước lượng, không phải hóa đơn. Mục tiêu là cảm được cái gì tốn, không phải tính tiền tới từng đồng."
- **Lớp đòi thực hành agent team:** từ chối nhẹ nhàng, nhắc lại "đây là tính năng thử nghiệm, phải bật cờ đặc biệt, chưa ổn định, hôm nay chỉ hiểu khái niệm." Không mở ra làm giữa giờ.
- **Có người lẫn lộn trợ lý phụ với skill:** chốt một câu: "Skill là công thức dạy nó LÀM cho đúng. Trợ lý phụ là một người làm bớt việc cho nó. Hai cái khác nhau, dùng cùng nhau được."
- **Demo trợ lý phụ chạy lâu hoặc không hiện rõ:** không sao, chuyển sang giải thích bằng bảng và ví von. Phần token vẫn chạy độc lập.
- **Lệnh `/context` hoặc `/usage` không chạy trên máy học viên:** giảng viên demo trên máy mình, lớp xem. Nếu lệnh không có trên phiên bản của lớp thì chỉ dạy ý niệm token và mẹo tiết kiệm, bỏ phần lệnh.
- **Thiếu giờ tới K4:** giữ Phần 1 (agent và trợ lý phụ) và Phần 4 (token), vì hai thứ này dùng được ngay. Rút Phần 3 (đội nhóm) xuống còn một câu: "có tính năng đội nhiều agent bàn với nhau, đang thử nghiệm, buổi sau kể kỹ." Bỏ demo trợ lý phụ nếu cần, thay bằng mô tả.

---

## K5. CHỐT VÀ GIAO BÀI (10 phút, 10:20 - 10:30)

### LỜI GIẢNG

"Hai tiếng rưỡi vừa rồi anh chị đi được một quãng xa. Tôi chốt lại theo đúng hai nửa buổi: ba thứ anh chị TỰ TAY LÀM mang về, và một thứ HIỂU để dùng sau."

*(Chiếu bảng, đọc to, bảo lớp tự đối chiếu máy mình.)*

**Ba thứ tự tay làm, mang về dùng ngay:**

| # | Sản phẩm | Ở đâu |
|---|---|---|
| 1 | `CLAUDE.md` viết cho công việc THẬT của mình, có mục cấu trúc thư mục | Trong thư mục làm việc |
| 2 | Một skill MỚI do chính mình lập, đã chạy thử được | `.claude/skills/<tên>/SKILL.md` trong thư mục làm việc |
| 3 | Một mẹo tiết kiệm token | Trong đầu và trong vở |

**Một thứ hiểu để dùng sau:** khi nào cần một trợ lý phụ, khi nào cần cả một đội.

"Ai thiếu mục nào giơ tay hoặc gõ chat ngay bây giờ, tôi ghi lại để hỗ trợ trước buổi sau."

"Và tôi nhắc lại điểm quan trọng nhất kỹ thuật của buổi: skill anh chị vừa lập nằm NGAY TRONG thư mục làm việc, ở `.claude/skills/`. Nhờ vậy nó chỉ áp cho đúng dự án này, và sau này chia cho đồng đội được. Đây là chỗ nối sang buổi sau, tôi nói ở cuối."

"Ba nguyên tắc chống bịa vẫn nguyên, đây là thứ theo anh chị suốt sáu buổi. **Một:** chỉ dùng dữ liệu anh chị cấp, không tự chế số liệu, thành phần, giá, tên khách. **Hai:** gắn nhãn nguồn, `[DATA THẬT]` cho thông tin có thật, `[SUY LUẬN]` cho phần nó tự suy ra, thiếu thì ghi 'chưa đủ dữ liệu'. **Ba:** người duyệt cuối, mọi thứ gửi khách đều là nháp, Claude không tự bấm đăng, không tự bấm gửi. Cả buổi hôm nay anh chị thấy nó xuất hiện lại: lúc để trống chính sách sỉ, nó ghi 'chưa đủ dữ liệu' chứ không bịa mức chiết khấu."

"Giới hạn của hôm nay, nói thẳng để anh chị không kỳ vọng sai. Skill anh chị vừa lập đang nằm trên máy anh chị. Chưa cất lên mạng, chưa chia cho ai được. Và đội nhóm agent team hôm nay mới hiểu khái niệm, chưa chạy thật. Hai chuyện đó có chỗ của nó ở các buổi sau."

"**Bài tập về nhà, ba việc. Việc một:** chạy thật skill mới của anh chị ít nhất ba lần trong tuần, ghi lại chỗ nào phải sửa tay, đó là danh sách sửa cho lần sau, buổi sau tôi hỏi. **Việc hai:** rà lại `CLAUDE.md` của mình, kiểm mục cấu trúc thư mục có khớp thư mục thật không. **Việc ba:** ai dùng Thảo An hôm nay thì viết hồ sơ sản phẩm của chính thương hiệu mình theo cấu trúc file `san-pham-thao-an.md`, rồi bảo Claude viết lại `CLAUDE.md` cho thương hiệu mình."

"**Mồi cho buổi sau.** Anh chị để ý: skill của anh chị đang nằm trên máy. Máy hỏng là mất, và cả phòng chưa dùng chung được. Buổi sau ta học cách cất nó lên mạng, một chỗ tên là GitHub, để không sợ mất và chia cho đồng đội tải về dùng chung. Đúng lúc anh chị đã có skill trong tay để mà tiếc nếu mất. Cảm ơn anh chị, hẹn gặp buổi sau."

---

## CHECKLIST CHUẨN BỊ TRƯỚC BUỔI

### Làm trước buổi ít nhất 3 ngày

- [ ] Xác nhận danh sách học viên đã qua buổi 1, có thư mục làm việc và file `san-pham-thao-an.md`. Ai nghỉ buổi 1 thì chuẩn bị bộ Thảo An mẫu để phát.
- [ ] Chuẩn bị bộ Thảo An mẫu đầy đủ để phát cho người thiếu nền: thư mục `thao-an-marketing` có `san-pham-thao-an.md`, một `CLAUDE.md` mẫu, một skill `viet-bai-ban-hang` mẫu, và vài file như `bang-gia-si.md`, thư mục `assets` để phần mô tả cấu trúc thư mục ở K2 có nội dung phong phú.
- [ ] Nhắc lại với lớp: KHÔNG mang dữ liệu khách hàng thật tới lớp.

### Làm trước buổi 1 ngày

- [ ] Máy giảng viên có sẵn 2 thư mục demo: `demo-trong` rỗng, và `demo-day-du` có `san-pham-thao-an.md` và `CLAUDE.md` viết xong. Đã chạy thử PROMPT B2-1 và B2-2, xác nhận bài dở rõ và bài đúng rõ. K1 phụ thuộc hoàn toàn vào cặp demo này.
- [ ] Thư mục Thảo An demo có nhiều file để phần mô tả cấu trúc thư mục ở K2 chạy ra kết quả phong phú. Đã chạy thử PROMPT B2-4.
- [ ] Đã chạy thử toàn bộ prompt B2-0 tới B2-9 trên máy giảng viên, xác nhận chạy đúng. Riêng PROMPT B2-6 (lập skill) chạy trọn một lần, xác nhận file nằm đúng `.claude/skills/soan-email-chao-si/SKILL.md` trong thư mục làm việc.
- [ ] **Kiểm tra các lệnh token trên máy:** mở tab Code gõ thử `/context`, `/usage`, `/cost`, `/compact`. Ghi lại lệnh nào chạy, hiện ra gì. Bỏ lệnh nào không có trên phiên bản của lớp.
- [ ] Chạy thử PROMPT B2-8 (trợ lý phụ) để biết trên phiên bản hiện tại Claude báo đang dùng subagent ra sao, chỉ đúng chỗ đó cho lớp.
- [ ] Chạy thử PROMPT B2-9 để biết trước con số token tiếng Việt so với tiếng Anh, chuẩn bị một câu bình luận. Con số tỉ lệ (gấp rưỡi tới gấp đôi) nên tự kiểm bằng chính đoạn văn demo, vì chưa có số chính thức.
- [ ] **Kiểm tra vị trí custom agent** nếu định nhắc tới: `.claude/agents/<tên>.md` trong thư mục làm việc. Vị trí này có thể đổi theo phiên bản, kiểm trên máy trước buổi. Với lớp hôm nay chỉ cần dạy gọi trợ lý phụ bằng lời.
- [ ] Kiểm tra lại đường bấm: nút mở thư mục ở tab Code. Ghi ra giấy nhắc.
- [ ] Chuẩn bị bảng hoặc slide vẽ sẵn: ví von tờ giới thiệu người mới (K1), ví von công thức nấu ăn (K3), ẩn dụ công ty thu nhỏ với nhân viên, trợ lý phụ, đội nhóm (K4), ví von token theo taxi và mặt bàn (K4), bảng lệnh token.

### Mang tới lớp hoặc gửi qua Zoom

- [ ] Phiếu copy 10 prompt (B2-0 tới B2-9), gửi bản mềm qua chat Zoom và để trên Drive lớp, link rút gọn viết sẵn.
- [ ] Chụp sẵn ảnh màn hình kết quả PROMPT B2-1, B2-2, B2-8, B2-9 để dùng khi mạng chậm.
- [ ] Một trợ giảng trực khung chat Zoom, xử lý người tụt lại, nhất là ở K3 (lập skill).

---

## XỬ LÝ TÌNH HUỐNG LỚP HỌC

### Tình huống về kỹ thuật

| Tình huống | Xử lý ngay |
|---|---|
| Máy không mở được thư mục hoặc app cũ, không thấy tab Code | Tải bản mới ở claude.ai/download. Trong lúc chờ ghép xem chung màn hình qua Zoom, không cài giữa giờ. |
| Máy trống, không còn file buổi 1 | Phát bộ Thảo An mẫu, tải về mở bằng tab Code. Hôm nay viết lại từ đầu nên vẫn theo được. |
| Claude viết `CLAUDE.md` quá dài | Gõ `Rút gọn lại, chỉ giữ thứ luôn đúng cho mọi việc, bỏ hết quy trình chi tiết.` Không viết lại từ đầu. |
| Mục giọng văn chỉ toàn tính từ | Gõ `Viết lại mục giọng văn bằng hành vi cụ thể: xưng hô ra sao, câu dài tối đa mấy chữ, tối đa mấy emoji.` |
| Claude thêm nhầm file chưa tồn tại vào mục cấu trúc thư mục | Gõ `Chỉ liệt kê đúng file đang có thật, bỏ file bạn không thấy.` |
| Skill mới không hỏi lại đầu vào mà viết luôn | Sửa bước 1 trong SKILL.md thành bắt buộc kiểm tra đủ đầu vào, thiếu thì dừng và hỏi. Chạy lại. Sửa quy trình, không sửa kết quả. |
| Claude không nhận ra skill vừa lập | Kiểm tra đường dẫn đúng `.claude/skills/<tên>/SKILL.md` trong thư mục làm việc. Gọi đích danh tên skill trong prompt. Kiểm frontmatter đủ hai dòng ba dấu gạch. |
| Skill viết bài vẫn dính từ cấm | Không sửa tay kết quả. Sửa mục Ràng buộc trong SKILL.md, thêm danh sách từ cấm và bước dò lại. Chạy lại. |
| Lệnh `/context` hoặc `/usage` không chạy | Demo trên máy giảng viên. Không có trên phiên bản của lớp thì bỏ, chỉ dạy ý niệm token và mẹo. |
| Demo trợ lý phụ không hiện rõ | Chuyển sang giải thích bằng bảng và ví von. Không cố đợi. |
| Mạng chậm, Claude quay lâu | Chiếu ảnh chụp màn hình kết quả đã chuẩn bị sẵn. Không chờ quá 45 giây. |

### Tình huống về lớp

| Tình huống | Xử lý ngay |
|---|---|
| Có người nói "buổi 1 tôi làm theo mà chưa hiểu CLAUDE.md là gì" | Tốt, đúng đối tượng của buổi này. Trấn an "hôm nay ta làm lại từ đầu, không cần nhớ buổi 1." Bám ví von tờ giới thiệu. |
| Lớp mất tập trung ở K4 (nhiều lý thuyết) | Dừng, hỏi một câu về nghề: "ở đây ai từng phải soát một chiến dịch từ nhiều góc cùng lúc?" để dẫn vào đội nhóm cho gần thực tế. |
| Có người hỏi "khi nào tôi thật sự cần đội nhóm agent team" | Trả lời bằng ví dụ soát chiến dịch ba góc. Nhắc lại đó là tính năng thử nghiệm, biết trước để sau này dùng. |
| Có người hỏi "AI có thay người làm content không" | Trả lời thẳng ngắn: "Người vẫn viết tờ giới thiệu, viết công thức, duyệt và bấm đăng. Cái nó thay là gõ lại và dò từ cấm. Ai viết tờ giới thiệu và công thức giỏi thì càng có giá." |
| Có người muốn thực hành đội nhóm agent team | Từ chối nhẹ nhàng. Nêu lý do: tính năng thử nghiệm, chưa ổn định. Hẹn buổi riêng khi nó ổn định. |
| Người xong sớm cả khối | Cho lập skill thứ hai cho một việc khác của họ, hoặc thêm mục "Khi nào KHÔNG dùng skill này". |
| Có người không theo kịp phần thực hành | Ghép xem chung màn hình một bạn khác qua Zoom breakout, hoặc bám màn hình giảng viên. Đừng để ai ngồi xem suốt. |
| Có người bảo "bài AI viết chưa hay bằng tôi viết" | Đồng ý luôn: "Đúng, và hôm nay mục tiêu không phải hay hơn anh chị. Mục tiêu là bản nháp thứ nhất mất 30 giây thay vì 30 phút, và nó không bao giờ quên danh sách từ cấm." |

---

## ƯU TIÊN KHI THIẾU GIỜ

Thứ tự giữ lại, từ quan trọng nhất: **K3 (lập skill) > K1 (CLAUDE.md cho việc thật) > K2 (cấu trúc thư mục) > K4 (đội quân AI, token) > K5 > K0.**

- **Thiếu 5 phút:** rút giờ sửa lỗi ở K3 (Việc 3) xuống còn nhờ Claude tự soi, chuyển phần sửa tay sang bài về nhà.
- **Thiếu 10 phút:** rút K4 xuống còn Phần 1 (agent và trợ lý phụ) và Phần 4 (token) kèm hoạt động token. Bỏ demo trợ lý phụ, rút Phần 3 (đội nhóm) xuống một câu.
- **Thiếu 15 phút trở lên:** gộp K2 vào cuối K1 (thêm mục cấu trúc thư mục ngay trong hoạt động viết CLAUDE.md), và trong K4 chỉ giữ phần token kèm hoạt động, phần agent chuyển thành đọc bảng và hẹn buổi sau. Giữ nguyên K1 và K3.
- **Không bao giờ cắt:** cặp demo bài dở và bài đúng ở K1; phần lập và chạy thử skill ở K3; câu nhấn skill nằm trong thư mục làm việc; và câu chốt đội nhóm agent team là tính năng thử nghiệm ở K4.

---

## GHI CHÚ CUỐI

- **Đau trước, giải pháp sau là xương sống buổi này.** Mỗi khối phải mở bằng nỗi đau học viên tự cảm, rồi mới nêu khái niệm. Không được đảo ngược thành định nghĩa khô trước. Cặp demo bài dở rồi bài đúng ở K1 là hình mẫu, giữ đúng thứ tự đó.
- **Không giả định lớp đã hiểu CLAUDE.md hay skill từ buổi 1.** Nhiều người buổi 1 chỉ làm theo cho xong. Buổi 2 giải thích lại từ đầu bằng ví von tờ giới thiệu và ví von công thức nấu ăn. Ai đã hiểu thì nghe lại vài phút không hại gì; ai chưa hiểu thì đây là lần đầu thật sự thông.
- **Ba điểm kỹ thuật phải nhấn cho rõ trong bài.** Một, skill và custom agent nằm NGAY TRONG thư mục làm việc hiện tại ở `.claude/skills/` và `.claude/agents/`, để gắn với đúng dự án và chia cho đồng đội được, khác bản cá nhân không chia được. Hai, cách gọi trợ lý phụ hay agent làm việc là NÓI BẰNG LỜI, không phải cài đặt hay gõ lệnh. Ba, cách tính và xem token: lệnh `/context`, `/usage` hoặc `/cost`, `/compact`, và mẹo tiếng Việt tốn hơn tiếng Anh.
- **Đội nhóm agent team là tính năng thử nghiệm.** Phải nói rõ ít nhất hai lần trong K4. Không demo, không bắt lớp thực hành. Ghi rõ để giảng viên khác không lỡ tay biến nó thành bài thực hành.
- **File index riêng không bắt buộc cho Claude.** Đừng để lớp hiểu nhầm phải tạo `index.md`. Cách đúng là viết mô tả cấu trúc thư mục thẳng vào `CLAUDE.md`. Nói rõ ở K2.
- **Token là ước lượng, không phải hóa đơn.** Con số ở hoạt động K4 là để cảm độ lớn, không phải tính tiền chính xác. Tỉ lệ token tiếng Việt (gấp rưỡi tới gấp đôi) chưa có số chính thức, giảng viên tự kiểm bằng đoạn văn demo trước buổi. Các điểm chưa chắc khác (vị trí `.claude/agents/`; lệnh `/context`, `/usage`, `/cost`, `/compact`; cách Claude hiển thị trợ lý phụ; nút mở thư mục) đã liệt kê ở CHECKLIST, kiểm trên máy trước buổi, đừng mô tả theo trí nhớ.
- **Mười prompt B2-0 tới B2-9 phải khớp nguyên văn với phiếu copy phát cho học viên.** Cần sửa thì sửa đồng thời ở cả giáo án, phiếu copy và bản mềm trên Drive lớp.
- **Feed sang buổi 3.** `CLAUDE.md` cho việc thật và skill mới là nền để buổi sau dạy cất skill lên GitHub và chia cho đồng đội. Giảng viên ghi lại danh sách người chưa xong ngay cuối K5.
- **Buổi 2 KHÔNG dạy:** đẩy skill lên GitHub (dời buổi sau); chạy đội nhóm agent team thật (tính năng thử nghiệm); phân tích review khách thành insight (buổi Customer Insight); viết quảng cáo trả tiền; tự động hóa nhiều bước và luồng đăng bài; đóng gói skill thành bộ bàn giao hoàn chỉnh.
