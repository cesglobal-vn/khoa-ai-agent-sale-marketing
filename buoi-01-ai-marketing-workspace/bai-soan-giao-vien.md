# BÀI SOẠN GIÁO VIÊN - BUỔI 1

## Đóng gói ngữ cảnh và năng lực cho Claude: CLAUDE.md, Skill, Memory và MCP

> Bản script giảng được ngay. Đọc theo, không cần soạn thêm.
> Lớp: 10 đến 20 người làm sale và marketing. Chủ doanh nghiệp nhỏ, trưởng phòng marketing, nhân sự content, nhân sự ads, nhân sự CRM, người làm agency. Phần lớn KHÔNG biết code, chưa từng mở cửa sổ dòng lệnh. Đây là ràng buộc thiết kế quan trọng nhất của buổi này.
> Máy: Windows 11. Mỗi người 1 máy, ai thiếu thì ghép cặp.
> Công cụ học viên dùng: **Claude Desktop, tài khoản trả phí (Pro trở lên)**. Trong app có 3 tab ở trên: Chat, Cowork, Code. Cả buổi hôm nay làm ở tab **Code**. Không cài thêm gì qua dòng lệnh, không cần Node.js.
> Cài đặt chi tiết nằm ở file riêng: [huong-dan-cai-dat.md](huong-dan-cai-dat.md). Bài soạn này không lặp lại phần đó.
> Case study xuyên suốt: **Thảo An**, thương hiệu mỹ phẩm thảo mộc giả định, 3 SKU, bán B2C qua Facebook và Shopee, bán sỉ B2B cho spa.
> Thời lượng: 150 phút, đã gồm 10 phút giải lao.
> Nguyên tắc xuyên suốt: LÝ THUYẾT trước, DEMO giữa, THỰC HÀNH sau.

---

## BẢNG MỐC ĐỒNG HỒ CẢ BUỔI

Giả định giờ bắt đầu 08h00. Nếu bắt đầu giờ khác thì cộng dồn tương ứng.

| Khối | Đồng hồ | Phút | Nội dung | Ai làm |
|---|---|---|---|---|
| K0 | 08:00 - 08:15 | 15 | Mở đầu, kiểm tra cài đặt, tạo thư mục làm việc, ra đề bài | Giảng 5 + học viên thao tác 6 + viết tay 4 |
| K1 | 08:15 - 08:45 | 30 | Lý thuyết 4 tầng + demo so sánh có và không có ngữ cảnh | Giảng 20 + demo 10 |
| K2 | 08:45 - 09:10 | 25 | Tầng 1 viết CLAUDE.md, tầng 3 bật Memory | Giảng 3 + demo 7 + thực hành 15 |
| Giải lao | 09:10 - 09:20 | 10 | Nghỉ | |
| K3 | 09:20 - 09:55 | 35 | Tầng 2 viết Skill đầu tiên, chạy thật, sửa 1 vòng | Giảng 2 + demo 5 + thực hành 28 |
| K4 | 09:55 - 10:20 | 25 | Tầng 4 nối MCP đọc dữ liệu thật | Giảng 7 + demo 6 + thực hành 12 |
| K5 | 10:20 - 10:30 | 10 | Tổng kết, bài tập, mở đường Buổi 2 | Giảng 10 |

**Mốc phải bám cứng:** 08:45 xong lý thuyết. 09:55 xong K3.
Nếu trễ, cắt K4 xuống còn phần demo của giảng viên và chuyển phần nối MCP sang bài tập về nhà. **Không cắt K1 và K3.** K1 là nền hiểu, K3 là sản phẩm chính học viên mang về.

---

## K0. MỞ ĐẦU, KIỂM TRA CÀI ĐẶT VÀ RA ĐỀ BÀI (15 phút, 08:00 - 08:15)

### LỜI GIẢNG (5 phút)

"Chào anh chị. Trước khi vào bài, tôi hỏi một câu và anh chị giơ tay thật lòng giúp tôi: ai ở đây từng gõ lại đoạn giới thiệu thương hiệu của mình vào một ô chat AI, quá năm lần rồi?"

*(Dừng 10 giây. Gần như cả lớp giơ tay. Nếu ít người giơ thì hỏi thêm: "vậy ai từng nhận một bài AI viết ra, đọc xong thấy đúng ngữ pháp mà sai hẳn giọng thương hiệu mình?")*

"Đó chính là vấn đề của buổi hôm nay. Không phải AI kém. Anh chị đưa cho nó đúng một câu 'viết giúp tôi bài bán hàng' thì nó phải tự đoán, mà đoán thì trật. Nó đoán giọng, đoán khách, đoán công dụng sản phẩm. Có khi nó đoán ra một con số nghe rất hợp lý mà thương hiệu anh chị chưa bao giờ có. Hôm nay chúng ta không học mẹo gõ lệnh. Chúng ta đóng gói ngữ cảnh và năng lực cho Claude, gồm bốn tầng. Xong buổi này, anh chị có một chỗ để cả đội đứng chung, và bạn nhân sự mới vào tuần sau mở ra là dùng được."

"Về cách chạy buổi: 30 phút đầu anh chị chỉ nghe và ghi vở, không ai phải gõ gì. Tôi biết ngồi nghe 30 phút hơi lâu, nhưng bỏ qua phần này thì lúc mở máy anh chị sẽ làm mà không hiểu mình đang làm gì. Từ khối thứ ba trở đi là gõ liên tục tới hết buổi. Một lưu ý về công cụ: cả buổi hôm nay chỉ dùng Claude Desktop, và chỉ dùng tab **Code** ở trên cùng, không phải tab Chat. Ai đang mở sẵn ChatGPT hay công cụ khác thì đóng lại giúp tôi, để lát nữa không bấm nhầm cửa sổ."

### THAO TÁC HỌC VIÊN (6 phút)

Nói trước: "Sáu phút này ai cũng phải làm được. Ai vướng thì giơ tay ngay, đừng ngồi im, vì cả buổi sau dựa vào bước này."

**Bước 1. Kiểm tra ba thứ bằng cách giơ tay,** đếm số người: ai đã cài Claude Desktop và đăng nhập được; ai đang dùng tài khoản trả phí (Pro trở lên); ai đã cài Git for Windows theo hướng dẫn gửi trước buổi.

Nói thật với lớp về Git: "Git không bắt buộc tuyệt đối. Thiếu Git thì Claude Code vẫn chạy được bằng PowerShell có sẵn trong Windows. Nhưng cả lớp cài để mọi máy giống nhau, tôi hướng dẫn một đường là đúng cho tất cả. Ai chưa cài thì cứ làm tiếp, giờ nghỉ trợ giảng cài giúp."

**Bước 2. Tạo thư mục làm việc.** Đọc từng bước cho lớp làm theo:

1. Bấm chuột phải lên màn hình nền, chọn **New** rồi chọn **Folder**.
2. Gõ tên thư mục là `thao-an-marketing`. Viết không dấu, không khoảng trắng, dùng gạch nối. Bấm Enter.
3. Mở Claude Desktop.
4. Bấm tab **Code** ở hàng trên cùng.
5. Bấm nút mở thư mục làm việc, trỏ tới màn hình nền, chọn thư mục `thao-an-marketing` vừa tạo, bấm chọn.
6. Gõ vào ô nhập ở dưới cùng đúng một câu: `Bạn đang mở thư mục nào?` rồi bấm Enter. Claude phải trả lời đúng tên thư mục đó.

*Lưu ý cho giảng viên: tên nút mở thư mục có thể đổi theo phiên bản app. Trước buổi phải mở máy kiểm tra lại đúng đường bấm và ghi ra giấy nhắc. Đừng mô tả theo trí nhớ trước lớp.*

**Bước 3. Chép dữ liệu case study vào thư mục.** Giảng viên đã để sẵn file `san-pham-thao-an.md` trên Drive lớp và trên USB dự phòng.

1. Tải file `san-pham-thao-an.md` về máy.
2. Kéo file đó thả vào thư mục `thao-an-marketing`.
3. Gõ vào Claude: `Trong thư mục này có file gì?` Claude phải kể được tên file vừa bỏ vào.

**Tiêu chí coi là xong:** mỗi máy có thư mục `thao-an-marketing`, mở được bằng tab Code, và Claude kể đúng tên file có trong thư mục.

### HOẠT ĐỘNG HỌC VIÊN (4 phút)

**Đề bài:** Mỗi người viết tay ra tờ giấy phát sẵn: 3 đầu việc nội dung hoặc bán hàng mà mình phải làm đi làm lại hàng tuần.

**Cách giảng viên đọc đề:** "Anh chị lấy tờ giấy tôi vừa phát. Viết ra ba đầu việc mà tuần nào anh chị cũng phải làm lại, liên quan tới nội dung hoặc bán hàng. Mỗi việc một dòng, không cần viết dài. Ví dụ: viết bài bán hàng cho Facebook, trả lời tin nhắn hỏi giá, soạn email chào sỉ cho spa, viết kịch bản video ngắn, dựng caption cho ảnh sản phẩm. Anh chị có 4 phút."

**Giảng viên đi hỗ trợ:** đi một vòng, đọc lướt giấy từng người, vừa đi vừa hỏi nhỏ "việc này tuần làm mấy lần?" để lọc ra việc tần suất cao. Ghi lên bảng 3 việc phổ biến nhất mà nhiều người cùng nêu.

**Tiêu chí coi là xong:** trên bảng có đúng 3 việc, mỗi việc có ít nhất 3 người trong lớp cũng làm. Nói rõ với lớp: đây là đề bài chính thức của K3, lát nữa anh chị viết skill cho một trong ba việc này.

### DỰ PHÒNG

- **Có người chưa cài được Claude Desktop, hoặc không bấm thấy tab Code:** ghép cặp ngay với người bên cạnh, không ngồi cài giữa giờ. Nguyên nhân thường là app cũ, phải tải bản mới ở claude.ai/download. Ghi tên lại, giờ nghỉ trợ giảng xử lý.
- **Có người dùng tài khoản miễn phí:** nói thẳng và không giấu: "gói miễn phí sẽ hết lượt giữa buổi, không đủ cho 150 phút thực hành." Cho ghép cặp với người có tài khoản trả phí, hai người thay phiên cầm chuột. Nhắc nâng cấp sau buổi.
- **Lớp viết chậm hoặc ngại viết:** giảng viên đọc luôn 5 ví dụ ở trên và nói "anh chị chỉ cần khoanh cái nào đúng với mình, thêm 1 việc riêng nữa là được".
- **Ba việc trên bảng quá giống nhau, cả ba đều là viết bài:** giữ 2 việc, thêm 1 việc khác loại như trả lời tin nhắn hoặc soạn email chào sỉ, để K3 có sự đa dạng giữa các nhóm.

---

## K1. LÝ THUYẾT: BỐN TẦNG NGỮ CẢNH VÀ NĂNG LỰC (30 phút, 08:15 - 08:45)

**Mục tiêu khối:** học xong khối này học viên đủ vốn để làm K2, K3, K4 mà không phải dừng lại hỏi thêm.

**Cách giữ lớp tỉnh:** khối này chia 4 phần nhỏ, mỗi phần 3 đến 8 phút, cuối mỗi phần có 1 câu hỏi nhanh cho lớp. Demo đặt cuối khối để kéo lại chú ý trước khi vào thực hành.

---

### Phần 1. Bốn tầng (8 phút)

#### LỜI GIẢNG

"Trước hết, từ 'ngữ cảnh'. Ngữ cảnh là những thứ AI cần biết trước khi bắt tay vào việc. Giống một bạn content mới nhận việc: trước khi giao bài, anh chị phải cho bạn ấy biết thương hiệu bán gì, bán cho ai, giọng viết thế nào, từ nào cấm dùng. Nếu không nói, bạn ấy viết sai không phải vì kém, mà vì không biết. Claude có bốn tầng. Tôi sẽ ví bốn tầng này bằng bốn thứ mà phòng marketing nào cũng có."

*(Chiếu bảng lên màn hình, đọc từng dòng, dừng lại ở từng ví von.)*

| Tầng | Trong Claude Code là gì | Ví như trong nghề marketing | Nội dung nên đưa vào |
|---|---|---|---|
| Tầng 1 | File `CLAUDE.md` trong thư mục làm việc | Bản brief thương hiệu mà ai vào team cũng phải đọc trước ngày đầu tiên | Thương hiệu bán gì, bán cho ai, giọng văn thế nào, từ nào cấm dùng, tên kênh |
| Tầng 2 | Skill, là thư mục `.claude/skills/<tên>/SKILL.md` | Quy trình chuẩn cho từng đầu việc, ví dụ quy trình viết bài bán hàng dán trong phòng content | Từng bước làm một việc cụ thể |
| Tầng 3 | Memory | Sổ bàn giao giữa các phiên làm việc, như file bàn giao khi bạn content nghỉ phép | Thói quen làm việc của tôi, điều đã dặn và không muốn dặn lại |
| Tầng 4 | MCP | Thẻ ra vào có phân quyền, để Claude tự vào lấy đúng file được phép | Nối vào Google Drive hoặc Google Sheet chứa dữ liệu thật |

"**Tầng 1, bản brief thương hiệu.** Ai vào team cũng đọc, không phân biệt hôm đó làm bài Facebook hay làm email sỉ. Vì ai cũng phải đọc, nên anh chị chỉ ghi vào đó những thứ luôn đúng cho mọi việc: bán gì, bán cho ai, giọng nào, từ nào cấm. Anh chị không nhét cả quy trình 12 bước viết bài vào bản brief, đúng không? Vì đâu phải việc nào cũng là viết bài. **Tầng 2, quy trình từng việc.** Chỉ khi nào đúng việc thì mới lấy ra. Vì chỉ lấy khi đúng việc, nên nó được phép dài, được phép chi tiết tới từng bước. Không ai chê quy trình dài. Người ta chỉ chê quy trình mơ hồ, kiểu 'viết cho hấp dẫn'. Hấp dẫn là cái gì thì mỗi người hiểu một kiểu."

"**Tầng 3, sổ bàn giao.** Phiên làm việc sau mở ra là biết phiên trước đã dặn gì, không phải dặn lại từ đầu. Tiện thì rất tiện. Nhưng phải kiểm tra định kỳ. Nếu nó nhớ sai một điều thì nó áp cái sai đó vào mọi bài viết sau, mà anh chị không biết là đang sai. **Tầng 4, thẻ ra vào.** Tới đây Claude mới thôi là người ngồi trong phòng kín. Ba tầng trên rất giỏi, nhưng muốn nó đọc cái gì thì anh chị vẫn phải bê tài liệu vào tận nơi: copy từ Google Sheet, dán vào Claude, lấy kết quả, dán ngược ra. Mệt. MCP là cái thẻ cho nó tự đi lấy, nhưng chỉ đi được vào đúng chỗ anh chị cho phép."

**Bốn câu chốt, bảo lớp ghi vào vở:**

1. CLAUDE.md là thứ Claude đọc trước mọi việc, nên chỉ ghi thứ luôn đúng cho mọi việc.
2. Skill chỉ được lấy ra khi đúng việc, nên ghi càng chi tiết càng tốt, không sợ dài.
3. Memory là thứ Claude tự ghi lại và tự dùng lại ở phiên sau, nên phải kiểm tra định kỳ.
4. MCP cho Claude với tới dữ liệu thật, nên phải cấp quyền có kiểm soát và biết đường gỡ quyền.

"Còn một câu tôi nói qua thôi, anh chị không cần làm hôm nay: file CLAUDE.md có thể đặt ngay trong thư mục làm việc, tức là `./CLAUDE.md`, hoặc đặt trong thư mục con `.claude` thành `./.claude/CLAUDE.md`. Cả hai chỗ Claude đều tự đọc, anh chị không phải đính kèm gì cả. Hôm nay ta dùng cách đầu tiên cho gọn."

#### CÂU HỎI CHỐT PHẦN 1

"Tôi hỏi nhanh một câu. Cái quy trình 8 bước để viết một bài bán hàng cho Facebook, anh chị nên đặt vào tầng mấy?"

*(Dừng chờ. Đáp án: tầng 2, skill. Nếu ai trả lời tầng 1, hỏi lại: "nếu đặt vào bản brief thì lúc anh chị nhờ nó soạn email chào sỉ, nó cũng phải đọc 8 bước viết bài Facebook. Có cần không?")*

#### DỰ PHÒNG

- Lớp im lặng không trả lời: giảng viên tự trả lời và giải thích lý do, đừng chờ quá 15 giây làm không khí nặng nề.
- Có người hỏi "dùng cả bốn tầng cùng lúc được không?": trả lời "được, và đó chính là cách nên làm. Hôm nay ta dựng đủ cả bốn."

---

### Phần 2. Cơ chế skill chạy 4 bước (4 phút)

#### LỜI GIẢNG

"Bây giờ tôi giải thích Claude tìm và dùng cái quy trình đó như thế nào. Đúng 4 bước, anh chị vẽ vào vở thành 4 ô nối mũi tên."

*(Vừa nói vừa vẽ 4 ô lên bảng.)*

"**Bước 1.** Anh chị nêu yêu cầu. Ví dụ: viết bài Facebook bán serum rau má B5. **Bước 2.** Claude nhìn qua tất cả skill đang có, nhưng nó KHÔNG đọc hết. Nó chỉ đọc đúng một dòng mô tả của mỗi skill, giống anh chị lướt mắt qua nhãn dán trên gáy từng tập tài liệu trong tủ. Nó tìm cái nhãn nào ghi là dùng cho việc viết bài bán hàng."

"**Bước 3.** Tìm được rồi thì nó mới rút tập đó ra, mở file SKILL.md bên trong, nạp toàn bộ nội dung vào phiên làm việc hiện tại. **Bước 4.** Nó làm đúng từng bước ghi trong đó. Và cái này quan trọng: kể cả việc hỏi ngược lại anh chị khi thiếu thông tin bắt buộc. Nếu trong quy trình anh chị viết 'bước 1 là kiểm tra đủ thông tin, thiếu thì hỏi lại' thì nó sẽ hỏi thật, chứ không tự bịa con số."

"Hai điểm tôi muốn anh chị nhớ kỹ. **Thứ nhất:** chất lượng kết quả phụ thuộc vào chất lượng quy trình anh chị viết, KHÔNG phụ thuộc anh chị gõ câu lệnh hay hay dở. Nhiều người cứ nghĩ phải học cách gõ lệnh thần thánh. Không phải. Viết quy trình tốt thì gõ câu lệnh xoàng cũng ra kết quả tốt. **Thứ hai:** Claude chọn skill dựa vào cái nhãn, tức dòng `description`. Nhãn viết mơ hồ thì nó rút nhầm tập tài liệu. Nên lát nữa khi viết skill, dòng mô tả là dòng anh chị phải viết kỹ nhất trong cả file."

#### CÂU HỎI CHỐT PHẦN 2

"Nếu phòng anh chị có hai skill, một cái tên là 'viết nội dung' và một cái tên là 'viết bài bán hàng Facebook', chuyện gì xảy ra khi anh chị nhờ viết bài bán hàng?"

*(Đáp án: Claude có thể rút nhầm cái 'viết nội dung' vì nhãn quá rộng, trùm lên cả việc kia.)*

---

### Phần 3. Cấu trúc file SKILL.md (5 phút)

#### LỜI GIẢNG

"Giờ ta xem cái quy trình đó trông thế nào. Một skill trong Claude là một THƯ MỤC, chứ không phải một file lẻ. Đường dẫn đúng là như thế này, anh chị chép vào vở:"

```
.claude/skills/viet-bai-ban-hang/SKILL.md
```

"Đọc từ phải sang cho dễ hiểu: file tên đúng là `SKILL.md`, viết hoa cả chữ SKILL. Nó nằm trong thư mục mang tên skill. Thư mục đó nằm trong `skills`. `skills` nằm trong `.claude`. Và `.claude` nằm ngay trong thư mục làm việc của anh chị."

"Có một biến thể tôi nói cho anh chị biết mà chưa dùng hôm nay: nếu anh chị đặt skill ở `~/.claude/skills/` thì nó dùng được cho MỌI thư mục trên máy, không riêng thư mục này. Dấu ngã đó là thư mục người dùng của Windows. Hôm nay ta đặt trong thư mục làm việc thôi, để dễ mang đi và dễ chia cho đồng nghiệp. Còn nội dung file. Mở đầu file có một phần đặc biệt gọi là frontmatter, nghe lạ nhưng đơn giản: đó là mấy dòng khai báo tên và mô tả, kẹp giữa hai dòng ba dấu gạch. Trông thế này:"

```
---
name: viet-bai-ban-hang
description: Viết bài bán hàng cho Facebook và Shopee của Thảo An. Dùng khi
  cần bài giới thiệu một SKU, bài xử lý lo ngại kích ứng của khách da nhạy cảm,
  hoặc bài đẩy đơn dịp khuyến mãi. Không dùng cho email chào sỉ B2B.
---

Rồi từ đây trở xuống viết bằng chữ thường như viết Word.
```

"Hai dòng trong khung đó thôi. `name` là tên skill, viết không dấu, nối bằng gạch nối, trùng với tên thư mục. `description` chính là cái nhãn dán trên gáy hồ sơ tôi vừa nói ở phần trước. Đây là dòng Claude đọc để QUYẾT ĐỊNH có dùng skill này hay không. Viết kỹ nhất ở đây. Đừng viết 'skill này viết nội dung'. Hãy viết như trong ví dụ: nói rõ viết cho kênh nào, ba tình huống nào thì gọi ra, và một câu nói rõ khi nào KHÔNG dùng."

"Phần dưới frontmatter là hướng dẫn, viết bằng chữ thường như viết Word. Sáu phần, anh chị chép vào vở vì lát nữa K3 dùng ngay:"

**1. Skill này làm gì.** Một đoạn ngắn.
**2. Đầu vào bắt buộc.** Viết cho SKU nào, đăng kênh nào, người đọc là ai, mục tiêu bài là gì.
"Đây là chỗ hay bị bỏ sót nhất. Thiếu ở đây thì Claude tự đoán, mà nó đoán thì bài ra chung chung."
**3. Các bước làm.** Đánh số, mỗi bước một việc. Bước 1 LUÔN là kiểm tra đủ đầu vào, thiếu thì hỏi lại.
**4. Ràng buộc.** Từ cấm, độ dài, xưng hô, số emoji tối đa.
**5. Định dạng đầu ra.** Bài trông ra sao, có mấy phần.
**6. Ví dụ mẫu.** Một bài hoàn chỉnh đã viết xong.
"Cái này là mẹo hay nhất. Claude bắt chước một bài mẫu đã viết xong nhanh hơn nhiều so với đọc lời tả. Giống anh chị đào tạo bạn content mới: đưa họ đọc ba bài đã đăng và đúng giọng, họ hiểu ngay. Còn tả bằng miệng thì họ vẫn mơ hồ."

#### CÂU HỎI CHỐT PHẦN 3

"Trong cả file SKILL.md, dòng nào Claude đọc để quyết định có dùng skill này hay không?"

*(Đáp án: dòng `description` trong frontmatter.)*

---

### Phần 4. Ba nguyên tắc chống bịa (3 phút)

#### LỜI GIẢNG

"Phần cuối lý thuyết, ngắn nhưng là phần tách khóa này khỏi các khóa dạy mẹo prompt. Ba nguyên tắc, anh chị ghi vào vở, và lát nữa ta ghi luôn vào file CLAUDE.md."

"**Một: chỉ dùng dữ liệu người dùng cấp.** Không tự chế số liệu, thành phần, công dụng, giá, tên khách. Cái này quan trọng gấp đôi trong ngành mỹ phẩm, vì bịa một công dụng là chạm vào chuyện pháp lý, không chỉ là chuyện viết sai."

"**Hai: gắn nhãn nguồn.** Thông tin lấy được từ file mình đưa vào thì ghi `[DATA THẬT]`. Phần nó tự suy ra thì ghi `[SUY LUẬN]`. Thiếu hẳn thì ghi thẳng 'chưa đủ dữ liệu'. Vì sao nguyên tắc này quan trọng nhất? Vì AI không biết là nó đang bịa. Nó chỉ đang chọn từ nghe hợp lý tiếp theo. Bắt nó gắn nhãn là bắt nó tự khai chỗ nào chắc, chỗ nào đoán. Anh chị chỉ phải soi kỹ phần `[SUY LUẬN]`, bỏ qua phần `[DATA THẬT]`. Tiết kiệm nửa thời gian duyệt bài."

"**Ba: người duyệt cuối.** Mọi thứ gửi khách đều là nháp. Claude không tự bấm đăng, không tự bấm gửi. Người vẫn là người bấm."

"Báo trước cho anh chị: ở khối sau, tôi sẽ cố tình hỏi Claude một con số mà hồ sơ Thảo An ghi rõ là chưa có. Anh chị nhìn kỹ nó trả lời thế nào."

---

### DEMO GIÁO VIÊN: SO SÁNH CÓ NGỮ CẢNH VÀ KHÔNG CÓ NGỮ CẢNH (10 phút)

**Chuẩn bị trước buổi:** giảng viên có sẵn 2 thư mục trên máy mình.
- Thư mục `demo-trong`: rỗng, không có gì cả.
- Thư mục `demo-day-du`: có `san-pham-thao-an.md`, có `CLAUDE.md` đã viết xong, có skill `.claude/skills/viet-bai-ban-hang/SKILL.md` đã chạy thử.

#### THAO TÁC DEMO - Bước 1 (3 phút): chạy KHÔNG có ngữ cảnh

1. Mở Claude Desktop trên máy giảng viên, chiếu lên màn hình lớn. Bấm tab **Code**.
2. Mở thư mục `demo-trong`.
3. Nói với lớp: "Thư mục này hoàn toàn trống. Không có brief, không có skill, không có hồ sơ sản phẩm. Đúng như tình trạng máy anh chị lúc mới cài xong."
4. Gõ prompt sau vào ô nhập ở dưới cùng, bấm Enter.

**PROMPT 1:**

```
Viết cho tôi 1 bài đăng Facebook bán serum rau má B5 của thương hiệu Thảo An.
```

5. Chờ Claude trả kết quả, để nguyên trên màn hình.

#### THAO TÁC DEMO - Bước 2 (2 phút): cùng lớp soi kết quả

"Anh chị nhìn cái này giúp tôi. Nhìn lướt thì trông cũng được đấy chứ, đúng ngữ pháp, có emoji, có kêu gọi mua. Nhưng nếu anh chị là người duyệt bài của Thảo An, anh chị sẽ trả lại. Vì sao? Anh chị chỉ giúp tôi những chỗ sai và những chỗ chung chung."

*(Dừng chờ lớp nói. Ghi lên bảng từng ý lớp nêu. Nếu lớp nêu chậm thì gợi ý bằng câu hỏi: "nó có nói giá không, giá đó ở đâu ra?", "nó gọi khách là gì?", "nó có hứa bao nhiêu ngày hết thâm không?")*

**Danh sách lỗi dự kiến, ghi lên bảng:**
- Bịa hoặc né giá, trong khi giá thật là 320.000đ cho 30ml.
- Bịa thành phần ngoài bảng, hoặc nói chung chung "chiết xuất thiên nhiên".
- Dùng từ cấm: "trị mụn", "đặc trị", "trắng da cấp tốc".
- Hứa thời gian: "7 ngày hết thâm", "2 tuần da sáng bật tông".
- Xưng hô lung tung: "chúng tôi", "quý khách", trong khi Thảo An gọi mình là "Thảo An" và gọi khách là "bạn".
- Bài đúng ngữ pháp nhưng thay tên thương hiệu nào vào cũng dùng được.

"Cái gạch cuối cùng là phép thử tôi muốn anh chị mang về dùng mãi. Lấy một câu trong bài, thay tên Thảo An bằng tên đối thủ. Nếu câu đó vẫn đúng thì câu đó chưa dùng được."

#### THAO TÁC DEMO - Bước 3 (3 phút): chạy CÓ ngữ cảnh

1. Chuyển Claude Code sang thư mục `demo-day-du`.
2. Nói: "Vẫn là Claude đó. Vẫn là tôi gõ. Khác duy nhất: lần này thư mục có bản brief và có quy trình viết bài."
3. Dán prompt sau, bấm Enter.

**PROMPT 2:**

```
Dùng skill viet-bai-ban-hang để viết 1 bài đăng Facebook bán SKU-01 Serum
rau má B5 của Thảo An.

Đầu vào:
- Người đọc: nữ 25 đến 40 tuổi, da nhạy cảm hoặc da sau mụn, ngân sách
  200 đến 500 nghìn cho một sản phẩm dưỡng da.
- Kênh đăng: Facebook, bài thường, không phải quảng cáo trả tiền.
- Mục tiêu của bài: người đọc nhắn tin hỏi thêm.

Chỉ dùng thông tin có trong file san-pham-thao-an.md và CLAUDE.md của thư mục
này. Không thêm thành phần, công dụng, giá hay con số nào ngoài hồ sơ.
Chỗ nào thiếu dữ liệu thì ghi "chưa đủ dữ liệu", đừng đoán.

Cuối bài, liệt kê riêng thành 2 nhóm: câu nào là [DATA THẬT], câu nào là
[SUY LUẬN].
```

#### THAO TÁC DEMO - Bước 4 (2 phút): chốt

1. Mở hai cửa sổ đặt hai kết quả cạnh nhau, hoặc chia đôi màn hình.
2. Chỉ vào ba chỗ khác biệt rõ nhất: giá đúng 320.000đ cho 30ml; không còn từ cấm; có phần gắn nhãn nguồn ở cuối.
3. Nói câu chốt: "Cùng một Claude. Cùng một người gõ. Khác nhau duy nhất ở chỗ có ngữ cảnh hay không. Ba mươi phút vừa rồi anh chị đã hiểu ngữ cảnh là gì. Một trăm phút còn lại chúng ta tự tay dựng nó."

### HOẠT ĐỘNG HỌC VIÊN (K1)

**Không ai gõ máy ở khối này.** Chỉ ghi vở.

**Tiêu chí coi là xong K1:** vở mỗi học viên có đủ 4 thứ.

1. Bảng 4 tầng, kèm ví von marketing.
2. Sơ đồ 4 bước skill chạy.
3. Đường dẫn `.claude/skills/<ten-skill>/SKILL.md` và khung frontmatter 2 dòng.
4. Ba nguyên tắc chống bịa.

Giảng viên đi nhanh một vòng cuối khối, liếc vở, ai chưa chép đủ đường dẫn skill thì nhắc chép ngay vì K3 cần.

### DỰ PHÒNG

- **Demo bước 1 ra kết quả quá tốt, không thấy lỗi rõ:** đừng cố cãi. Chuyển hướng sang phép thử đổi tên: "bài này không sai, nhưng anh chị thử thay chữ Thảo An bằng tên bất kỳ hãng mỹ phẩm nào xem bài có còn đúng không?" Rồi so tiếp với bước 3. Thường vẫn còn ít nhất lỗi xưng hô và lỗi không có phần gắn nhãn nguồn.
- **Mạng chậm, Claude quay lâu:** giảng viên chuẩn bị sẵn 2 ảnh chụp màn hình kết quả của cả hai lần chạy, dán vào slide. Mạng chậm thì chiếu ảnh và nói rõ "đây là kết quả tôi chạy sáng nay", không ngồi chờ quá 45 giây.
- **Lớp mất tập trung giữa chừng:** dừng lại, hỏi một câu về nghề chứ không phải về AI, ví dụ "ở đây ai đang phải viết bài cho quá ba kênh cùng lúc?" để kéo lại rồi giảng tiếp.

---

## K2. TẦNG 1 VIẾT CLAUDE.md VÀ TẦNG 3 BẬT MEMORY (25 phút, 08:45 - 09:10)

### LỜI GIẢNG (3 phút)

"Giờ anh chị gõ máy. Chúng ta làm tầng 1, tầng dễ nhất, bản brief thương hiệu."

"Nhắc lại một câu, không dạy mới: CLAUDE.md là bản brief, chỉ ghi thứ luôn đúng cho MỌI việc. Đừng nhét quy trình viết bài vào đây, quy trình để dành cho skill ở khối sau. Và đây là tin mừng cho anh chị: **anh chị KHÔNG phải mở Notepad, không phải nhớ chỗ Save as, không phải sợ file lưu nhầm thành đuôi chấm txt.** Anh chị bảo Claude tạo file, nó tạo. Anh chị bảo nó sửa, nó sửa. Đó là điểm khác biệt của tab Code so với tab Chat: ở tab Chat nó chỉ nói cho anh chị nghe, ở tab Code nó ghi được file thẳng vào thư mục."

"Một câu về vị trí file: đặt tên đúng là `CLAUDE.md`, chữ CLAUDE viết hoa hết, và để ngay trong thư mục `thao-an-marketing` anh chị vừa tạo. Claude tự đọc, không phải đính kèm gì cả."

### THAO TÁC DEMO (7 phút)

#### Bước 1 (3 phút): dựng CLAUDE.md trước mặt lớp

1. Mở Claude Desktop, tab Code, mở thư mục demo có sẵn `san-pham-thao-an.md`.
2. Dán PROMPT 3 (nội dung đầy đủ ở phần thực hành bên dưới), bấm Enter.
3. Khi Claude báo đã tạo file, mở thư mục trên màn hình nền cho lớp thấy file `CLAUDE.md` vừa xuất hiện. Nói: "Anh chị thấy chưa, tôi không mở Notepad lần nào."
4. Mở file ra, chiếu nội dung, dừng lại đọc to 3 phần quan trọng nhất.

**Ba phần giảng viên phải đọc to và bình luận, đây là phần lõi của cả buổi:**

```
## Câu định vị
Thảo An là mỹ phẩm dưỡng da từ thảo mộc, sản xuất tại Việt Nam, dành cho
phụ nữ 25 đến 40 tuổi có da nhạy cảm hoặc da sau mụn, giá 180 đến 320 nghìn
một sản phẩm; khác ở chỗ không cồn, không hương liệu tổng hợp và đã test
da liễu. [DATA THẬT]

## Giọng văn, mô tả bằng hành vi
- Nói như dược sĩ tư vấn ở quầy thuốc: giải thích thành phần trước, mời mua sau.
- Gọi mình là "Thảo An". Gọi khách là "bạn". Không dùng "chúng tôi",
  không dùng "quý khách".
- Mở bài bằng một tình huống da cụ thể, không mở bằng lời chào.
- Câu dưới 20 chữ.
- Tối đa 1 dấu chấm than mỗi bài. Tối đa 2 emoji mỗi bài.

## Từ cấm và điều không được nói
- Cấm từ: trị mụn, đặc trị, khỏi hẳn, trắng da cấp tốc.
- Không cam kết thời gian có kết quả, ví dụ "7 ngày hết thâm".
- Không nói sản phẩm là thuốc hay có tác dụng chữa bệnh.
- Không so sánh trực tiếp bằng tên với thương hiệu khác.
- Không bịa thành phần hoặc công dụng ngoài hồ sơ sản phẩm.
```

Nói khi chiếu phần giọng văn: "Anh chị để ý, ở đây không có chữ 'chuyên nghiệp', không có chữ 'thân thiện', không có chữ 'uy tín'. Ba từ đó ai cũng viết được và AI không dùng được. Cái viết ở đây là hành vi: câu dài bao nhiêu chữ, gọi khách bằng gì, tối đa mấy emoji. Đọc một câu là biết đúng hay sai ngay." Nói khi chiếu phần từ cấm: "Danh sách này tôi không tự nghĩ ra. Nó nằm nguyên trong mục 'Điều KHÔNG được nói' của hồ sơ sản phẩm. Với ngành mỹ phẩm, đây là ràng buộc bắt buộc, không phải gợi ý."

#### Bước 2 (2 phút): cho lớp thấy Claude đọc được file

1. Gõ một câu ngắn vào ô nhập: `Thảo An cấm dùng những từ nào, và gọi khách hàng bằng gì?`
2. Chiếu kết quả.
3. Nói: "Nó nhắc lại đúng danh sách từ cấm và đúng cách xưng hô. Từ giờ mọi việc tôi giao trong thư mục này, nó đều đọc cái này trước. Tôi không phải dán lại lần nào nữa."

#### Bước 3 (2 phút): THỬ PHÉP CHỐNG BỊA

Nói trước khi gõ: "Giờ tới đoạn tôi hứa với anh chị ở khối trước. Tôi sẽ hỏi nó ba con số mà hồ sơ Thảo An ghi rõ là chưa có. Anh chị nhìn kỹ."

1. Dán PROMPT 4, bấm Enter.
2. Chiếu kết quả, đọc to từng câu trả lời.

**PROMPT 4:**

```
Dựa trên các file trong thư mục này, trả lời 3 câu sau.

Quy tắc trả lời: câu nào hồ sơ không có dữ liệu thì trả lời đúng một câu
"chưa đủ dữ liệu". Không ước lượng. Không đưa con số tham khảo của ngành.
Không nói "thường thì các thương hiệu tương tự...".

1. Tháng này Thảo An chi bao nhiêu tiền cho quảng cáo?
2. Giá trị đơn trung bình của Thảo An là bao nhiêu?
3. Serum rau má B5 hiện có bao nhiêu đánh giá của khách?

Trả lời xong 3 câu, liệt kê thêm: trong hồ sơ còn mục dữ liệu nào đang trống
mà tôi nên bổ sung trước khi chạy quảng cáo?
```

3. Kết quả đúng: cả 3 câu đều là "chưa đủ dữ liệu". Mục còn trống thứ tư mà nó phải chỉ ra: ai trực inbox Facebook và thời gian phản hồi trung bình.
4. Nói câu chốt: "Đây là thứ đắt giá nhất của buổi hôm nay. Một AI nói 'chưa đủ dữ liệu' có ích hơn nhiều một AI đưa cho anh chị con số nghe rất hợp lý mà sai. Vì con số sai đó anh chị sẽ mang đi báo cáo sếp."

### HOẠT ĐỘNG HỌC VIÊN (15 phút)

Mỗi người làm trên máy của mình. Ai ghép cặp thì hai người thay phiên, mỗi người một lượt.

#### Việc 1 (9 phút): nhờ Claude viết CLAUDE.md

**Đề bài đọc cho lớp:** "Anh chị lấy phiếu copy prompt tôi phát, mở prompt số 3. Bản mềm nằm trên Drive lớp, link tôi đã viết lên bảng. Copy nguyên cả đoạn dán vào ô nhập của tab Code, bấm Enter. Ai có thương hiệu thật của mình thì thay hồ sơ Thảo An bằng hồ sơ của mình, nhưng giữ nguyên cấu trúc prompt."

**PROMPT 3:**

```
Trong thư mục này có file san-pham-thao-an.md. Đọc kỹ file đó trước khi làm.

Sau đó tạo giúp tôi file CLAUDE.md đặt ngay trong thư mục này. Đây là bản brief
thương hiệu mà bạn sẽ đọc trước MỌI việc tôi giao trong thư mục này.

Viết đủ 9 mục sau, mỗi mục một tiêu đề riêng:

1. Thương hiệu này là ai: viết 1 câu định vị duy nhất, có đủ 4 phần: bán cho ai,
   giải quyết chuyện gì, khác đối thủ ở đâu, bằng chứng nào.
2. Bán gì: liệt kê 3 SKU, mỗi SKU ghi giá, thành phần chính, công dụng ghi
   trên nhãn, hợp với loại da nào. Lấy đúng số trong hồ sơ, không làm tròn.
3. Bán cho ai: chân dung khách B2C và chân dung khách B2B.
4. Ba thông điệp bán hàng, mỗi thông điệp 1 dòng.
5. Năm nỗi đau của khách. Vì hôm nay tôi chưa đưa bạn review khách thật,
   phần này bạn phải đánh dấu [SUY LUẬN] và ghi rõ cần kiểm chứng lại.
6. Giọng văn, mô tả bằng HÀNH VI chứ không phải bằng tính từ. Cấm dùng các từ
   "chuyên nghiệp", "thân thiện", "uy tín", "trẻ trung". Thay vào đó hãy viết
   rõ: xưng hô thế nào, mở bài bằng gì, câu dài tối đa bao nhiêu chữ, tối đa
   mấy dấu chấm than, tối đa mấy emoji.
7. Từ cấm và điều không được nói: chép nguyên danh sách trong mục
   "Điều KHÔNG được nói" của hồ sơ, không bớt dòng nào.
8. Ba nguyên tắc chống bịa, ghi nguyên văn như sau:
   - Chỉ dùng dữ liệu trong các file của thư mục này. Không tự chế số liệu,
     thành phần, công dụng, giá, tên khách.
   - Gắn nhãn nguồn: [DATA THẬT] cho thông tin trích được từ file,
     [SUY LUẬN] cho phần tự suy ra. Thiếu thì ghi "chưa đủ dữ liệu".
   - Mọi thứ gửi khách đều là bản nháp. Bạn không tự bấm đăng, không tự bấm gửi.
9. Chỗ còn thiếu dữ liệu: chép nguyên mục "Chỗ còn thiếu dữ liệu" của hồ sơ.
   Khi tôi hỏi những mục này, câu trả lời duy nhất được phép là "chưa đủ dữ liệu".

Viết gọn trong khoảng 60 dòng. Tiếng Việt có dấu, câu ngắn.
Đừng đưa quy trình chi tiết của từng việc vào đây, phần đó tôi để riêng ở skill.
```

**Sau khi Claude tạo xong file:** học viên mở file ra đọc lại, sửa tay chỗ nào chưa đúng, hoặc gõ tiếp cho Claude sửa.

**Giảng viên đi hỗ trợ:** đi một vòng, mỗi người khoảng 40 giây. Chỉ kiểm tra đúng 3 thứ:
(a) file có tên đúng `CLAUDE.md` và nằm ngay trong thư mục làm việc;
(b) mục giọng văn có phải là hành vi không, hay lại là danh sách tính từ;
(c) mục từ cấm có đủ 5 dòng lấy từ hồ sơ không.
Trợ giảng đi vòng ngược lại để phủ hết lớp.

**Tiêu chí coi là xong Việc 1:** trong thư mục có file `CLAUDE.md`, mở ra thấy đủ 9 mục, câu định vị có đủ 4 phần, mục giọng văn không chứa từ "chuyên nghiệp", "thân thiện", "uy tín".

#### Việc 2 (6 phút): bật Memory và kiểm tra Claude nhớ đúng

**Đề bài:** "Anh chị vào Cài đặt bật Memory lên trước. Bấm vào biểu tượng tài khoản, chọn Settings, tìm mục Memory hoặc Trí nhớ, gạt công tắc sang bật. Chỗ đó cũng có nút để xem lại và xóa những gì Claude đã nhớ, anh chị nhớ đường vào, vì sổ bàn giao ghi sai thì mọi bài sau sai theo. Bật xong thì dán prompt số 5."

*Lưu ý cho giảng viên: vị trí menu Memory có thể đổi theo phiên bản app. Trước buổi phải mở máy kiểm tra lại và ghi ra giấy nhắc.*

**PROMPT 5:**

```
Từ giờ trở đi hãy ghi nhớ 3 điều sau về cách tôi làm việc, và tự áp dụng lại
ở những lần trò chuyện sau mà tôi không phải dặn lại:

1. Tôi làm marketing cho Thảo An, thương hiệu mỹ phẩm dưỡng da từ thảo mộc,
   3 SKU, bán B2C qua Facebook và Shopee, bán sỉ B2B cho spa. Tên SKU luôn ghi
   đúng là SKU-01 Serum rau má B5, SKU-02 Kem nghệ mật ong,
   SKU-03 Mặt nạ đất sét trà xanh.
2. Mỗi khi tôi nhờ viết bài bán hàng, luôn hỏi tôi đủ 4 thông tin trước khi
   viết: viết cho SKU nào, đăng kênh nào, người đọc là ai, mục tiêu của bài
   là gì (nhắn tin, bấm link, hay lưu bài).
3. Mọi bài viết trả về đều phải có phần cuối liệt kê câu nào [DATA THẬT],
   câu nào [SUY LUẬN]. Và mọi bài đều là bản nháp, tôi là người bấm đăng.

Ghi nhớ xong, đọc lại cho tôi nghe bạn đã nhớ những gì, để tôi kiểm tra
có nhớ sai chỗ nào không.
```

**Bước kiểm tra bắt buộc:** mở một cuộc trò chuyện MỚI rồi gõ đúng một câu:

`Tôi làm marketing cho thương hiệu nào, và bạn cần hỏi tôi những gì trước khi viết bài bán hàng?`

"Nếu ở cuộc trò chuyện mới nó vẫn trả lời đúng, tức là sổ bàn giao đã hoạt động. Nếu nó ngơ ngác không biết anh chị là ai, tức là Memory chưa bật thật, anh chị gọi tôi."

**Tiêu chí coi là xong Việc 2:** ở cuộc trò chuyện mới, Claude nêu đúng tên Thảo An và liệt kê đủ 4 thông tin cần hỏi trước khi viết bài.

### DỰ PHÒNG

- **Claude vẫn bịa số ở bước 3 của demo, tức là nó đưa ra con số ngân sách hoặc số review:** đừng che giấu, đây là tình huống dạy được. Xử lý theo đúng thứ tự này trước lớp.
  1. Nói thẳng: "Đây, nó vừa bịa. Anh chị mở file hồ sơ ra dò giúp tôi, tìm xem con số này nằm ở dòng nào." Cả lớp không tìm ra. Đó là bài học.
  2. Mở `CLAUDE.md`, thêm một dòng cứng vào mục 9: `Khi tôi hỏi một con số không có trong file của thư mục này, câu trả lời duy nhất được phép là "chưa đủ dữ liệu, cần bổ sung từ [tên nguồn]". Không ước lượng, không dùng số trung bình ngành.`
  3. Chạy lại PROMPT 4. Lần này nó thường trả đúng.
  4. Nếu vẫn bịa: thêm câu ràng buộc ngay trong prompt, và nói với lớp: "Đây là lý do nguyên tắc thứ ba tồn tại. Người vẫn phải rà. Không có cách nào bỏ được bước rà."
- **Claude tạo file nhưng học viên không thấy file đâu:** bảo họ mở thư mục `thao-an-marketing` trên màn hình nền và bấm F5 để làm mới. Nếu vẫn không thấy, gõ vào Claude: `Liệt kê tất cả file trong thư mục này kèm đường dẫn đầy đủ.`
- **Claude trả CLAUDE.md quá dài, hơn 100 dòng:** bảo học viên gõ thêm đúng một câu `Rút gọn còn khoảng 60 dòng, bỏ hết phần quy trình chi tiết của từng việc.` Không cần viết lại từ đầu.
- **Máy không tìm thấy Memory trong Cài đặt:** cho người đó bỏ qua Việc 2, thay bằng cách đưa 3 điều đó vào luôn mục cuối file `CLAUDE.md`. Nói với lớp: "cách này kém tiện hơn vì chỉ đúng trong thư mục này, nhưng ra kết quả tương đương, không sao cả."
- **Học viên dùng thương hiệu thật của mình và hồ sơ quá sơ sài:** cho họ dùng Thảo An cho hôm nay, và giao bài tập về nhà là viết hồ sơ sản phẩm của mình theo đúng cấu trúc file `san-pham-thao-an.md`.

---

## GIẢI LAO (10 phút, 09:10 - 09:20)

**Việc giảng viên làm trong lúc lớp nghỉ:**

- Đi kiểm tra nhanh: máy nào chưa có file `CLAUDE.md` thì làm giúp ngay, đừng để họ bước vào K3 với thư mục rỗng.
- Trợ giảng cài Git for Windows cho ai chưa cài.
- Kiểm tra máy giảng viên: tài khoản Google demo còn đăng nhập không, thư mục lớp trên Drive còn đủ 2 file không.
- Chiếu sẵn khung frontmatter và khung 6 phần của SKILL.md lên màn hình, để nguyên đó suốt K3.

---

## K3. TẦNG 2 VIẾT SKILL ĐẦU TIÊN (35 phút, 09:20 - 09:55)

### LỜI GIẢNG (2 phút)

"Xong bản brief. Giờ ta viết quy trình, tức là skill. Đây là phần quan trọng nhất buổi hôm nay, và cũng là phần anh chị mang về dùng được ngay từ chiều nay."

*(Chiếu lại khung frontmatter và khung 6 phần từ K1 lên màn hình và ĐỂ NGUYÊN đó suốt 28 phút thực hành, đừng tắt đi.)*

"28 phút thực hành chia 4 chặng, tôi bấm giờ báo chuyển chặng. Chặng một 11 phút: nhờ Claude viết skill. Chặng hai 8 phút: chạy skill đó ra 3 bài bán hàng thật. Chặng ba 4 phút: chạy tiếp ra 10 hook và 10 CTA. Chặng bốn 5 phút: nhờ chính Claude soi lại skill của mình và sửa. Nhắc lại đường dẫn, anh chị nhìn lên màn hình: skill là một THƯ MỤC nằm ở `.claude/skills/`, bên trong có file tên đúng là `SKILL.md`. Anh chị không phải tự tạo mấy thư mục lồng nhau đó, cứ bảo Claude tạo, nó tạo hết."

### THAO TÁC DEMO (5 phút)

#### Bước 1 (2 phút): dựng skill trước mặt lớp

1. Dán PROMPT 6 (nội dung đầy đủ ở phần thực hành bên dưới), bấm Enter.
2. Khi Claude báo xong, gõ: `Cho tôi xem nội dung file SKILL.md vừa tạo.`
3. Chiếu nội dung, dừng lâu nhất ở đúng 2 chỗ.
   - Dòng `description`: đọc to lên và nói "Đây là cái nhãn. Anh chị nghe kỹ nó viết gì: viết bài bán hàng cho Facebook và Shopee, dùng khi cần bài giới thiệu SKU, bài xử lý lo ngại kích ứng, bài đẩy đơn khuyến mãi, và KHÔNG dùng cho email chào sỉ. Bốn ý trong một dòng. Đó là lý do lát nữa nó không rút nhầm việc."
   - Mục "Đầu vào bắt buộc": nói "Đây là chỗ hay bị bỏ sót nhất. Tôi liệt kê ra đây: SKU nào, kênh nào, người đọc là ai, mục tiêu bài là gì. Thiếu một cái là Claude tự đoán, mà nó đoán thì bài ra chung chung."

#### Bước 2 (2 phút): chạy thử và cố tình bỏ trống thông tin

1. Gõ một yêu cầu CỐ Ý thiếu: `Dùng skill viet-bai-ban-hang viết cho tôi một bài.`
2. Chỉ vào màn hình khi Claude hỏi ngược lại bốn thông tin đầu vào: "Anh chị thấy chưa, nó không tự đoán. Nó hỏi lại tôi viết cho SKU nào, đăng kênh nào. Vì tôi đã viết trong quy trình rằng bước 1 phải kiểm tra đủ đầu vào. Đây chính là thứ giúp anh chị yên tâm giao việc cho nó."

#### Bước 3 (1 phút): sửa skill ngay tại chỗ

1. Chỉ ra 1 chỗ trong skill viết còn mơ hồ. Ví dụ mục ràng buộc chỉ ghi "viết ngắn gọn" mà không nói bao nhiêu chữ.
2. Gõ cho Claude sửa ngay: `Trong file SKILL.md, sửa mục Ràng buộc: thay "viết ngắn gọn" bằng "bài dài 120 đến 180 chữ, câu dưới 20 chữ".`
3. Nói: "Skill không phải viết một lần là xong. Nó là quy trình, mà quy trình nào cũng có bản sửa lần 1, lần 2. Lát nữa chính anh chị sẽ sửa bản của mình ở chặng cuối."

### HOẠT ĐỘNG HỌC VIÊN (28 phút)

Ai có thương hiệu thật thì làm cho thương hiệu mình. Ai chưa có thì làm trên Thảo An. Ai muốn làm skill cho một trong ba việc ghi trên bảng ở K0 thì đổi phần "việc cần chuẩn hóa" trong prompt, giữ nguyên phần còn lại.

#### Chặng 1 (11 phút): nhờ Claude viết file SKILL.md

**PROMPT 6:**

```
Tạo cho tôi một skill mới trong thư mục làm việc này.

Đường dẫn file: .claude/skills/viet-bai-ban-hang/SKILL.md
Nếu thư mục .claude hoặc .claude/skills chưa có thì tạo luôn.

File bắt đầu bằng phần frontmatter kẹp giữa hai dòng ba dấu gạch, bên trong
có đúng 2 dòng: name và description.
- name: viet-bai-ban-hang
- description: viết thật kỹ dòng này, vì đây là dòng bạn dùng để quyết định
  có gọi skill này ra hay không. Trong một dòng phải nói được: skill viết bài
  bán hàng cho kênh nào của Thảo An, ba tình huống cụ thể khiến nó được gọi ra,
  và một tình huống rõ ràng KHÔNG dùng nó.

Phần dưới frontmatter viết bằng markdown, đủ 6 mục sau:

1. Skill này làm gì: 3 dòng.
2. Đầu vào bắt buộc: 4 thứ tôi phải cấp trước khi bạn viết, gồm viết cho
   SKU nào, đăng kênh nào, người đọc là ai, mục tiêu bài là gì.
3. Các bước làm: đánh số 8 bước, mỗi bước một việc. Bước 1 bắt buộc là kiểm
   tra đủ 4 đầu vào, thiếu thì hỏi lại tôi, tuyệt đối không tự đoán. Trong
   8 bước phải có: chọn 1 nỗi đau cụ thể để mở bài; nêu thành phần trước rồi
   mới nêu công dụng; đối chiếu toàn bài với danh sách từ cấm trong CLAUDE.md;
   bước cuối gắn nhãn [DATA THẬT] hoặc [SUY LUẬN] cho từng ý.
4. Ràng buộc: chép danh sách từ cấm và quy tắc giọng văn từ CLAUDE.md của
   thư mục này. Thêm: bài dài 120 đến 180 chữ, câu dưới 20 chữ, tối đa
   1 dấu chấm than, tối đa 2 emoji.
5. Định dạng đầu ra: bài gồm 4 phần theo thứ tự là hook mở bài, phần thân,
   câu kêu gọi hành động, rồi phần gắn nhãn nguồn đặt cuối cùng.
6. Ví dụ mẫu: viết luôn 1 bài hoàn chỉnh cho SKU-01 Serum rau má B5, đăng
   Facebook, người đọc là nữ 25 đến 40 tuổi da nhạy cảm, mục tiêu là nhắn tin.
   Dùng đúng giá và đúng thành phần trong file san-pham-thao-an.md.

Viết bằng tiếng Việt có dấu, câu ngắn, người không rành máy tính đọc là làm
theo được. Không dùng thuật ngữ lập trình.
```

**Giảng viên đi hỗ trợ:** đi vòng, chỉ soi đúng 1 chỗ ở mỗi người là dòng `description`. Hỏi họ: "nếu tuần sau anh chị viết thêm một skill soạn email chào sỉ cho spa, thì đọc dòng này Claude có phân biệt được hai cái không?" Nếu không phân biệt được thì bảo họ gõ: `Viết lại dòng description cho tách bạch hẳn với skill soạn email chào sỉ B2B.`

**Tiêu chí xong chặng 1:** có file `SKILL.md` đúng đường dẫn, mở ra thấy frontmatter đủ 2 dòng, dòng description có nêu cả tình huống KHÔNG dùng, và mục 6 có 1 bài mẫu đã viết xong.

#### Chặng 2 (8 phút): chạy skill ra 3 bài bán hàng

**Đề bài:** "Giờ ta thử xem cái quy trình anh chị vừa viết có chạy được không. Anh chị dán prompt số 7. Ba bài cho ba SKU, ba mục tiêu khác nhau, để thấy skill nó bám theo đầu vào chứ không viết một kiểu."

**PROMPT 7:**

```
Dùng skill viet-bai-ban-hang để viết 3 bài đăng, làm đúng từng bước trong
skill, không bỏ bước nào.

Bài 1:
- SKU: SKU-01 Serum rau má B5
- Kênh: Facebook, bài thường
- Người đọc: nữ 25 đến 40 tuổi, da sau mụn còn thâm, đã từng dùng sản phẩm
  mạnh và bị kích ứng
- Mục tiêu: người đọc nhắn tin hỏi thêm

Bài 2:
- SKU: SKU-02 Kem nghệ mật ong
- Kênh: Facebook, bài thường
- Người đọc: nữ 25 đến 40 tuổi, da khô, mùa hanh bị bong tróc
- Mục tiêu: người đọc lưu bài lại

Bài 3:
- SKU: SKU-03 Mặt nạ đất sét trà xanh
- Kênh: Shopee, phần mô tả sản phẩm
- Người đọc: nữ 25 đến 40 tuổi, da dầu, lỗ chân lông to vùng chữ T
- Mục tiêu: người đọc bấm mua

Chỉ dùng giá, thành phần và công dụng có trong file san-pham-thao-an.md.
Không thêm bất kỳ con số nào ngoài hồ sơ. Thiếu thì ghi "chưa đủ dữ liệu".
Mỗi bài kết thúc bằng phần gắn nhãn [DATA THẬT] và [SUY LUẬN].
```

**Điểm giảng viên phải nói to giữa chặng này:** "Anh chị dừng tay 30 giây, làm giúp tôi phép thử đổi tên. Lấy câu mở bài của bài 1, thay chữ Thảo An bằng tên một hãng mỹ phẩm bất kỳ. Câu đó còn đúng không? Nếu vẫn đúng thì bài đó chưa dùng được, anh chị bảo Claude viết lại kèm chi tiết chỉ Thảo An mới có, ví dụ đã test da liễu, hoặc không cồn và không hương liệu tổng hợp."

**Tiêu chí xong chặng 2:** có đủ 3 bài, không bài nào chứa từ trong danh sách cấm, mỗi bài có phần gắn nhãn nguồn ở cuối.

#### Chặng 3 (4 phút): 10 hook và 10 CTA

**PROMPT 8:**

```
Vẫn dùng skill viet-bai-ban-hang và file CLAUDE.md của thư mục này.

Viết cho tôi:
- 10 hook mở bài cho Thảo An. Mỗi hook 1 dòng, dưới 20 chữ, mở bằng một
  tình huống da cụ thể, không mở bằng lời chào. Ghi rõ mỗi hook dùng cho
  SKU nào.
- 10 câu kêu gọi hành động. Chia rõ: 4 câu cho mục tiêu nhắn tin,
  3 câu cho mục tiêu bấm mua trên Shopee, 3 câu cho mục tiêu lưu bài.

Ràng buộc: không dùng từ trong danh sách cấm ở CLAUDE.md. Không hứa thời gian.
Sau khi viết xong, tự kiểm tra lại giúp tôi: hook nào thay tên Thảo An bằng
tên thương hiệu khác mà vẫn đúng thì đánh dấu YẾU và viết lại câu đó.
```

**Tiêu chí xong chặng 3:** có 10 hook và 10 CTA, không câu nào chứa từ cấm, và có ít nhất vài câu đã bị chính Claude đánh dấu YẾU rồi viết lại.

#### Chặng 4 (5 phút): nhờ Claude tự soi và sửa skill

**Đề bài:** "Giờ ta làm việc ít người nghĩ tới: bảo chính Claude soi lại cái quy trình mà nó vừa dùng. Nó biết chỗ nào nó phải tự đoán, vì chính nó đoán."

**PROMPT 9:**

```
Bạn vừa chạy skill viet-bai-ban-hang để viết 3 bài và bộ hook, CTA cho
Thảo An. Giờ đóng vai người kiểm tra quy trình và soi lại chính file
.claude/skills/viet-bai-ban-hang/SKILL.md đó.

Trả lời tôi đúng 4 mục, ngắn gọn:

1. Bước nào trong skill viết còn chung chung khiến bạn phải tự đoán?
   Nêu rõ bạn đã đoán gì.
2. Đầu vào nào lẽ ra phải liệt kê là bắt buộc nhưng skill đang bỏ sót?
3. Dòng description đã đủ rõ để phân biệt skill này với một skill soạn email
   chào sỉ B2B chưa? Nếu chưa thì viết lại giúp tôi.
4. Sửa lại file SKILL.md theo đúng những gì bạn vừa chỉ ra, giữ nguyên
   cấu trúc 6 mục. Ghi thêm một dòng cuối file:
   "Sửa lần 1, ngày [điền ngày hôm nay], lý do: ..." kèm lý do ngắn.
```

**Câu chốt cuối K3:** "Anh chị vừa đi trọn một vòng: viết quy trình, chạy thật, soi lại, sửa. Trong nghề marketing anh chị gọi vòng đó là gì? Đúng, là tối ưu. Skill cũng vậy. Chạy ba lần trong tuần là anh chị biết ngay chỗ nào phải sửa."

### DỰ PHÒNG

- **Hết 11 phút chưa xong chặng 1:** cho họ dùng luôn bản Claude vừa trả, không sửa gì, chuyển ngay sang chặng 2. Thà chạy thử được một bản chưa hoàn hảo còn hơn ngồi mãi ở chặng 1.
- **Claude viết bài vẫn dính từ cấm:** không sửa tay bài viết. Bảo học viên gõ: `Trong file SKILL.md, mục Ràng buộc, thêm nguyên danh sách từ cấm và thêm bước bắt buộc dò lại toàn bài với danh sách đó trước khi trả kết quả.` Rồi chạy lại. Đây chính là bài học của khối: **sửa quy trình chứ không sửa kết quả.**
- **Claude không nhận ra skill, viết bài kiểu chung chung:** bảo học viên gõi rõ tên skill trong prompt, ví dụ `Dùng skill viet-bai-ban-hang để...`. Nếu vẫn không nhận, kiểm tra đường dẫn file có đúng `.claude/skills/viet-bai-ban-hang/SKILL.md` không, bằng cách gõ `Liệt kê các skill đang có trong thư mục này kèm đường dẫn.`
- **Người làm quá nhanh, xong sớm 5 phút:** giao thêm việc: viết thêm mục "Khi nào KHÔNG dùng skill này" vào cuối file, liệt kê 2 tình huống dễ nhầm. Hoặc viết skill thứ hai cho một việc khác ghi trên bảng ở K0.
- **Mạng chậm hoặc tài khoản báo hết lượt:** người đó ghép chung máy với người bên cạnh, mỗi người giữ file của mình trong một thư mục riêng. Ghi tên lại để nhắc làm bù ở bài tập về nhà.

---

## K4. TẦNG 4 NỐI MCP ĐỌC DỮ LIỆU THẬT (25 phút, 09:55 - 10:20)

### LỜI GIẢNG (7 phút)

"Anh chị ngồi xuống. Khối này là khối nhiều người chờ nhất, và cũng là khối tôi phải dặn kỹ nhất về an toàn."

"Từ đầu buổi tới giờ, Claude vẫn là một người ngồi trong phòng kín. Nó rất giỏi, nó có brief, nó có quy trình, nó có trí nhớ. Nhưng muốn nó đọc cái gì thì anh chị vẫn phải bê tài liệu vào tận nơi. Copy từ Google Sheet, dán vào Claude, lấy kết quả, dán ngược ra. Mệt."

"MCP là cách mở cửa cái phòng đó. MCP viết tắt của Model Context Protocol, tạm hiểu là chuẩn cắm nối cho AI. Anh chị hình dung như cái thẻ ra vào của tòa nhà: một cái thẻ, nhưng quẹt được đúng những tầng công ty cho phép, không phải tầng nào cũng vào. Có MCP rồi thì Claude đọc thẳng file trên Drive, đọc thẳng bảng đơn hàng trên Google Sheet, không phải copy dán nữa."

*(Vẽ lên bảng hai cột: KHÔNG MCP và CÓ MCP.)*

"Anh chị đừng nhầm skill với MCP, hai cái khác hẳn nhau. **Skill dạy Claude LÀM một việc cho đúng chuẩn. MCP cho Claude TAY CHÂN để với tới dữ liệu thật.** Có skill mà không có MCP thì vẫn phải copy dán. Có MCP mà không có skill thì nó với tới được dữ liệu nhưng viết ra bài không đúng giọng thương hiệu, y như demo đầu buổi. Phải có cả hai."

*(Hỏi lớp: "Vậy nếu tôi chỉ có MCP mà không có skill, tôi bảo nó viết bài bán hàng, nó viết thế nào?" Dừng chờ. Đáp án: viết chung chung, sai giọng, dính từ cấm, y như demo K1 bước 1.)*

"Cách cài rất đơn giản, không phải gõ dòng lệnh gì hết. Anh chị vào **Settings** của Claude Desktop, tìm mục **Connectors**, chọn Google Drive, rồi làm theo màn hình đăng nhập Google hiện ra."

"Nhưng tới màn hình cấp quyền của Google thì tôi phải nói rõ, vì chỗ này rất hay hiểu nhầm. **Google hiện ra một màn hình liệt kê nguyên một nhóm quyền mà ứng dụng xin. Anh chị chỉ có hai lựa chọn: đồng ý cả nhóm, hoặc hủy. KHÔNG có ô bật tắt từng quyền một.** Nhiều người tưởng vào đó tích chọn được cái nào cho cái nào không. Không phải vậy. Nên việc anh chị phải làm là đọc kỹ danh sách quyền trước khi bấm. Thấy quyền nào không chấp nhận được thì bấm hủy, không cắm nối nữa."

"**Và đây là quy định cứng của lớp hôm nay, tôi nói lần thứ nhất:** chỉ nối vào tài khoản Google demo tôi phát, hoặc tài khoản Google cá nhân của anh chị. **TUYỆT ĐỐI không nối tài khoản công ty thật có dữ liệu khách hàng.** Trong Drive công ty anh chị có danh sách khách, số điện thoại, lịch sử đơn hàng. Đó là dữ liệu cá nhân của người khác, không phải của anh chị, và hôm nay là buổi học chứ không phải triển khai chính thức. Lát nữa trước khi anh chị bấm cấp quyền tôi sẽ nói lại lần thứ hai."

"**Cách gỡ quyền sau buổi, anh chị ghi vào vở luôn:** mở trình duyệt, vào trang quản lý tài khoản Google, mục Bảo mật, tìm phần các ứng dụng bên thứ ba có quyền truy cập tài khoản. Tìm dòng Claude, bấm xóa quyền truy cập. Ngoài ra vào luôn Settings của Claude Desktop, mục Connectors, bấm ngắt kết nối. Làm cả hai chỗ. Tôi có in hướng dẫn phát cho anh chị. **Và ranh giới an toàn, câu này cũng ghi vào vở:** Claude ĐỌC và SOẠN NHÁP. Người vẫn là người duyệt và người bấm đăng. Không bao giờ để nó tự bấm đăng bài lên trang thật."

### THAO TÁC DEMO (6 phút)

**Chuẩn bị trước buổi:** tài khoản Google demo của lớp có sẵn một thư mục tên `LOP-AI-MARKETING`, bên trong có 2 file.
- `san-pham-thao-an` dạng Google Docs, nội dung y hệt file hồ sơ sản phẩm.
- `thao-an-don-hang-demo` dạng Google Sheet, 40 dòng đơn hàng mô phỏng, 5 cột: Ngày, Kênh, Mã SKU, Số lượng, Thành tiền. Mỗi đơn đúng 1 sản phẩm để số cộng khớp.

#### Bước 1 (3 phút): nối Google Drive trên máy giảng viên

1. Mở Claude Desktop, vào **Settings**, tìm mục **Connectors**.
2. Chọn thêm connector Google Drive, bấm kết nối.
3. Cửa sổ đăng nhập Google hiện ra. Chọn tài khoản demo.
4. **Dừng lại ở màn hình cấp quyền. Phóng to màn hình.** Đọc TO từng dòng quyền mà nó xin cho cả lớp nghe.
5. Nói: "Anh chị nhìn kỹ. Ở đây có nút Cho phép và nút Hủy. Có thấy ô tích nào để bỏ chọn từng quyền không? Không có. Đây là chấp nhận cả nhóm hoặc hủy. Nên đọc trước rồi mới bấm."
6. Bấm Cho phép, quay lại Claude, chỉ cho lớp thấy connector đã bật.
7. Mở trình duyệt, vào trang quản lý tài khoản Google, mục Bảo mật, phần ứng dụng bên thứ ba. Chỉ tay vào chỗ gỡ quyền. Nói: "Đây là đường về. Sau buổi học anh chị vào đây gỡ."

#### Bước 2 (3 phút): đọc dữ liệu thật và đối chiếu với brief

1. Dán PROMPT 10 (nội dung đầy đủ ở phần thực hành bên dưới).
2. Chiếu bảng kết quả lên màn hình.
3. Cùng lớp kiểm tra 2 dòng bất kỳ: mở lại Google Sheet, tìm đúng dòng đó, đọc to. Hỏi lớp "nó cộng đúng chưa?"
4. Nói: "Tôi cố ý làm bước kiểm tra này trước mặt anh chị. Nguyên tắc là: nó làm nhanh, nhưng người vẫn phải rà. Nó đọc 40 dòng trong 20 giây, anh chị bỏ 2 phút soi lại là quá lời."
5. Chỉ vào phần cuối kết quả, chỗ nó ghi "chưa đủ dữ liệu": "Anh chị để ý, bảng này không có cột chi phí quảng cáo, nên nó KHÔNG tính được chi phí trên mỗi đơn. Và nó ghi thẳng ra là chưa đủ dữ liệu, chứ không đưa cho tôi một con số nghe hợp lý. Đây là kết quả của cái brief anh chị viết ở khối trước."

**Số liệu để giảng viên đối chiếu nhanh** (bộ số này đã khớp sẵn với file [thao-an-don-hang-demo.csv](../case-study/thao-an/assets/thao-an-don-hang-demo.csv), chỉ cần tải file đó lên Google Sheet là dùng được, không phải tự dựng):
tổng 40 đơn, tổng doanh thu 10.840.000đ. Theo kênh: Facebook 24 đơn, Shopee 16 đơn. Theo SKU: SKU-01 Serum rau má B5 20 đơn và 6.400.000đ; SKU-02 Kem nghệ mật ong 12 đơn và 3.000.000đ; SKU-03 Mặt nạ đất sét trà xanh 8 đơn và 1.440.000đ. Nếu Claude ra số khác thì nói thẳng với lớp là nó tính sai và bảo nó tính lại.

### HOẠT ĐỘNG HỌC VIÊN (12 phút)

#### Việc 1 (7 phút): nối Claude vào Google Drive

**Đề bài, đọc trước khi lớp bấm gì:** "Trước khi anh chị bấm, tôi nói lại lần thứ hai: chỉ nối tài khoản Google demo tôi phát, hoặc tài khoản Google cá nhân của anh chị. **Không nối tài khoản công ty.** Ai đang định mở Drive công ty ra thì đóng lại giúp tôi ngay."

**Giảng viên và trợ giảng đi hỗ trợ:** trợ giảng đi kiểm tra TỪNG MÁY trước khi người đó bấm nút cấp quyền, xem đang đăng nhập tài khoản nào. Đây là bước bắt buộc, không bỏ. Giảng viên đứng đầu lớp xử lý câu hỏi chung.

**Tiêu chí xong Việc 1:** thấy connector Google Drive đã bật trong Settings, và Claude trả lời được câu thử `Bạn đang đọc được Drive của tài khoản nào của tôi?`

#### Việc 2 (5 phút): đọc bảng đơn hàng và đối chiếu với brief

**PROMPT 10:**

```
Trên Google Drive của tôi có thư mục LOP-AI-MARKETING. Trong đó có file
Google Sheet tên thao-an-don-hang-demo, gồm 5 cột đúng tên như sau:
Ngày, Kênh, Mã SKU, Số lượng, Thành tiền.
Cột Kênh chỉ có 2 giá trị: Facebook, Shopee.
Cột Mã SKU chỉ có 3 giá trị: SKU-01, SKU-02, SKU-03.

Hãy làm 3 việc:

1. Đọc toàn bộ file đó. Chỉ đọc, không sửa, không xóa gì cả.
2. Tổng hợp cho tôi thành 1 bảng gồm: tổng số đơn và tổng doanh thu; tách theo
   kênh; tách theo SKU. Chỉ ra SKU nào bán chạy nhất theo số đơn.
3. Đối chiếu với file CLAUDE.md trong thư mục làm việc của tôi và trả lời:
   SKU bán chạy nhất theo số liệu thật này có trùng với SKU tôi đang ghi là
   sản phẩm dẫn dắt trong brief không?

Quan trọng: nếu có chỉ số nào tôi hỏi mà bảng này không đủ dữ liệu để tính
thì ghi thẳng "chưa đủ dữ liệu, cần bổ sung [tên dữ liệu còn thiếu]".
Tuyệt đối không ước lượng, không dùng số trung bình ngành.
Cuối cùng liệt kê giúp tôi: để tính được chi phí trên mỗi đơn thì tôi còn
thiếu những cột dữ liệu nào.
```

**Câu chốt cuối K4:** "Anh chị để ý một chuyện: cái brief anh chị viết ở khối hai ghi serum rau má là sản phẩm dẫn dắt, và số liệu đơn hàng thật vừa xác nhận đúng như vậy. Đó là lúc AI có ích thật: nó nối được cái mình tin với cái số liệu nói. Còn chỗ nó ghi 'chưa đủ dữ liệu' thì đó chính là danh sách việc anh chị phải đi lấy số tuần này."

**Tiêu chí xong Việc 2:** có bảng tổng hợp đủ 3 phần, có ít nhất 1 dòng ghi "chưa đủ dữ liệu", và có câu trả lời cho phần đối chiếu với brief.

### DỰ PHÒNG

- **IT công ty chặn ứng dụng bên thứ ba ở cấp quản trị Google Workspace:** đây là chặn ở cấp quản trị, đổi mạng hoặc phát sóng điện thoại KHÔNG giải quyết được, đừng mất thời gian thử. Chuyển ngay sang tài khoản demo của lớp hoặc tài khoản Google cá nhân.
- **Học viên ngại cấp quyền Google:** đừng ép. Nói: "anh chị không cần bấm, xem chung màn hình người bên cạnh cũng được." Vẫn phát hướng dẫn gỡ quyền cho cả lớp dù có bấm hay không.
- **Không nối được MCP cho cả lớp:** giảng viên chạy toàn bộ trên máy mình, chiếu lên, lớp chuyển sang chế độ xem và ghi. Chuyển phần nối MCP sang bài tập về nhà, kèm hướng dẫn in giấy. Không kéo dài K4 lấn sang K5.
- **Claude tính sai số so với Sheet gốc:** đừng che giấu. Nói thẳng: "đây, nó cộng sai dòng này. Chính vì vậy tôi mới dặn phải rà lại. Nó nhanh chứ không phải nó luôn đúng." Rồi bảo nó tính lại.
- **Có người đòi nối Drive công ty để làm luôn cho việc thật:** từ chối dứt khoát, không thương lượng. Nêu lý do: dữ liệu khách hàng của người khác. Đề nghị họ bàn với bộ phận IT sau buổi nếu công ty muốn triển khai chính thức.
- **Claude đòi ghi file mới lên Drive:** hôm nay chỉ đọc, không ghi. Nói với lớp: "buổi 5 mới làm phần ghi và tự động hóa. Hôm nay ta dừng ở đọc, cho an toàn."

---

## K5. TỔNG KẾT, BÀI TẬP VÀ MỞ ĐƯỜNG SANG BUỔI 2 (10 phút, 10:20 - 10:30)

### LỜI GIẢNG

"Hai tiếng rưỡi vừa rồi anh chị dựng được bốn tầng, tôi chốt lại. **Tầng 1:** bản brief thương hiệu, file `CLAUDE.md`, Claude đọc trước mọi việc, anh chị không phải dán lại bối cảnh lần nào nữa. **Tầng 2:** quy trình từng việc, skill `viet-bai-ban-hang`, và anh chị đã đi trọn một vòng viết, chạy thật, soi lại, sửa. **Tầng 3:** sổ bàn giao, Memory, phiên sau mở ra là nó đã biết anh chị là ai. **Tầng 4:** thẻ ra vào, MCP, nó tự đọc được số liệu thật trên Drive."

*(Chiếu lại bảng sản phẩm và đọc to, bảo lớp tự đối chiếu máy mình.)*

**Danh sách sản phẩm anh chị phải có trên máy lúc này:**

| # | Sản phẩm | Ở đâu |
|---|---|---|
| 1 | Thư mục làm việc mở được bằng tab Code | Màn hình nền, tên `thao-an-marketing` |
| 2 | File `CLAUDE.md` đủ 9 mục | Ngay trong thư mục làm việc |
| 3 | Memory đã bật và đã kiểm tra ở phiên mới | Settings của Claude Desktop |
| 4 | Skill `viet-bai-ban-hang` chạy được | `.claude/skills/viet-bai-ban-hang/SKILL.md` |
| 5 | 3 bài viết bán hàng do skill sinh ra | Lưu vào thư mục làm việc |
| 6 | 10 hook và 10 CTA | Lưu vào thư mục làm việc |
| 7 | 1 kết nối MCP đọc được dữ liệu | Settings, mục Connectors |

"Ai thiếu mục nào thì giơ tay ngay bây giờ, tôi ghi lại để hỗ trợ trước buổi sau."

"**Giờ tôi nhắc lại ba nguyên tắc chống bịa, vì đây là thứ anh chị mang theo suốt sáu buổi. Một:** chỉ dùng dữ liệu anh chị cấp, không tự chế số liệu, thành phần, công dụng, giá, tên khách. **Hai:** gắn nhãn nguồn, `[DATA THẬT]` cho thông tin từ file đưa vào, `[SUY LUẬN]` cho phần nó tự suy ra, thiếu thì ghi 'chưa đủ dữ liệu'. Anh chị nhớ lúc tôi hỏi nó ngân sách quảng cáo và số review không? Nó nói chưa đủ dữ liệu. Đó là dấu hiệu hệ thống của anh chị đang chạy đúng. **Ba:** người duyệt cuối, mọi thứ gửi khách đều là nháp, Claude không tự bấm đăng."

"Giờ tôi nói cái giới hạn của những thứ hôm nay, để anh chị không kỳ vọng sai. Anh chị để ý: mọi thứ vẫn phải có người bấm chạy từng bước. Anh chị bấm cho nó viết bài. Rồi bấm cho nó ra hook. Rồi bấm cho nó đọc Drive. Ba lần bấm cho một chuỗi việc. Và cái skill anh chị vừa viết mới chỉ dùng được cho chính anh chị, chưa bàn giao cho người khác được. Hai chuyện đó có buổi riêng. Buổi 5 dạy tự động hóa nhiều bước và luồng đăng bài. Buổi 6 dạy đóng gói skill thành bộ bàn giao được kèm playbook và chỉ số đo. Hôm nay ta dừng ở mức dựng lần đầu, đơn giản, chạy được."

"**Bài tập về nhà, ba việc. Việc một:** chạy thật skill `viet-bai-ban-hang` ít nhất 3 lần trong tuần, và ghi lại chỗ nào anh chị phải sửa tay sau khi nó chạy xong. Cái ghi chép đó chính là danh sách sửa cho lần sau, buổi sau tôi hỏi. **Việc hai:** ai đang dùng dữ liệu Thảo An thì viết hồ sơ sản phẩm của chính thương hiệu mình theo đúng cấu trúc file `san-pham-thao-an.md`, bỏ vào thư mục làm việc và bảo Claude viết lại `CLAUDE.md` cho thương hiệu mình. **Việc ba, làm ngay tối nay:** ai đã cấp quyền Google bằng tài khoản cá nhân mà không định dùng tiếp thì vào gỡ quyền theo hướng dẫn tôi phát. Đừng để đó."

"**Buổi sau chúng ta xây Customer Insight Agent.** Nó đọc review và tin nhắn khách thật, rút ra khách đang nói gì bằng chính lời của họ. Anh chị nhớ mục 'năm nỗi đau khách' trong file `CLAUDE.md` hôm nay không? Nó đang gắn nhãn `[SUY LUẬN]`, tức là chúng ta đang đoán. Buổi sau ta thay chỗ đoán đó bằng lời khách nói thật. Đầu vào của buổi sau chính là file `CLAUDE.md` và cái skill anh chị vừa làm. Ai chưa có thì buổi sau ngồi làm lại từ đầu. Cảm ơn anh chị, hẹn gặp buổi sau."

---

## CHECKLIST CHUẨN BỊ TRƯỚC BUỔI

### Làm trước buổi ít nhất 5 ngày

- [ ] Chốt với đơn vị tổ chức: ai mua tài khoản Claude trả phí cho học viên. Gói miễn phí sẽ hết lượt giữa buổi, không đủ cho 150 phút thực hành. Đây là rủi ro hỏng buổi lớn nhất, phải chốt sớm nhất.
- [ ] Gửi học viên file [huong-dan-cai-dat.md](huong-dan-cai-dat.md) kèm hạn chót cài đặt, yêu cầu: cài Claude Desktop từ claude.ai/download, đăng nhập được, bấm thấy tab Code, cài Git for Windows từ git-scm.com.
- [ ] Gửi kèm yêu cầu chuẩn bị dữ liệu: ai có hồ sơ sản phẩm thật thì mang, dạng thô cũng được. Ai không có thì dùng bộ Thảo An, vẫn nộp đủ sản phẩm.
- [ ] Nói rõ trước với lớp: **KHÔNG mang dữ liệu khách hàng thật tới lớp, không dùng tài khoản Google công ty.**
- [ ] Hỏi bộ phận IT của đơn vị: Google Workspace công ty có chặn ứng dụng bên thứ ba ở cấp quản trị không. Nếu chặn thì chốt luôn phương án tài khoản demo và báo trước cho học viên.

### Làm trước buổi 1 ngày

- [ ] Máy giảng viên có sẵn 2 thư mục demo: `demo-trong` rỗng, và `demo-day-du` có `san-pham-thao-an.md`, `CLAUDE.md`, skill `viet-bai-ban-hang`. Đã chạy thử cả PROMPT 1 và PROMPT 2. K1 phụ thuộc hoàn toàn vào demo này, hỏng là hỏng cả khối.
- [ ] Chạy thử PROMPT 4 ít nhất 2 lần trên máy giảng viên, xác nhận Claude trả "chưa đủ dữ liệu" cho cả 3 câu. Nếu nó bịa thì bổ sung dòng ràng buộc cứng vào `CLAUDE.md` mẫu trước buổi.
- [ ] Đã tải file [thao-an-don-hang-demo.csv](../case-study/thao-an/assets/thao-an-don-hang-demo.csv) lên Drive lớp, mở bằng Google Sheet, đặt tên đúng `thao-an-don-hang-demo` và để trong thư mục `LOP-AI-MARKETING`. File này đã có sẵn đúng 5 cột khớp PROMPT 10 và bộ số khớp phần đối chiếu ở K4, chỉ cần tải lên, không phải gõ tay.
- [ ] Máy giảng viên đã nối sẵn connector Google Drive và đã chạy thử PROMPT 10.
- [ ] Chụp sẵn ảnh màn hình kết quả của PROMPT 1, PROMPT 2, PROMPT 4 và PROMPT 10 để dùng khi mạng chậm.
- [ ] Mở Claude Desktop kiểm tra lại đúng đường bấm tới: nút mở thư mục ở tab Code, Settings, Memory, Connectors. Ghi ra giấy nhắc, vì giao diện có thể đổi theo phiên bản.
- [ ] Chuẩn bị bảng viết hoặc flipchart để vẽ: bảng 4 tầng, sơ đồ 4 bước skill, hai cột KHÔNG MCP và CÓ MCP.

### Mang tới lớp

- [ ] Phiếu copy 10 prompt in giấy, đủ mỗi người 1 bản cộng 5 bản dự phòng.
- [ ] Bản mềm toàn bộ prompt và file `san-pham-thao-an.md` trên Drive lớp, link rút gọn viết sẵn lên bảng.
- [ ] USB chứa `san-pham-thao-an.md`, dự phòng khi mạng hỏng.
- [ ] File [huong-dan-cai-dat.md](huong-dan-cai-dat.md) in giấy, phát cho ai chưa cài xong.
- [ ] Hướng dẫn gỡ quyền Google in giấy, phát cho cả lớp ở K4 dù họ có nối hay không.
- [ ] Giấy trắng phát cho học viên viết tay ở K0.
- [ ] 2 bộ tài khoản Google demo, 2 tài khoản Claude trả phí dự phòng.
- [ ] Điện thoại đã bật sẵn tính năng phát sóng, đủ dung lượng, làm mạng dự phòng.
- [ ] 1 trợ giảng, đã được dặn: K4 phải đi kiểm tra từng máy trước khi học viên bấm cấp quyền Google.

---

## XỬ LÝ TÌNH HUỐNG LỚP HỌC

### Tình huống về kỹ thuật

| Tình huống | Xử lý ngay |
|---|---|
| Có người chưa cài được Claude Desktop | Ghép cặp ngay với người bên cạnh, hai người thay phiên cầm chuột. Trợ giảng cài trong giờ nghỉ. Đừng ngồi cài giữa giờ giảng. |
| Không bấm thấy tab Code trong app | Kiểm tra app có phải bản mới tải từ claude.ai/download không. App cũ thì ghép cặp, cập nhật vào giờ nghỉ. |
| Tài khoản Claude báo hết lượt dùng | Ghép chung máy với người bên cạnh, mỗi người giữ thư mục riêng. Ghi tên để nhắc làm bù ở bài tập về nhà. |
| Claude tạo file mà học viên không thấy file đâu | Mở thư mục trên màn hình nền, bấm F5 làm mới. Vẫn không thấy thì gõ `Liệt kê tất cả file trong thư mục này kèm đường dẫn đầy đủ.` |
| Claude không nhận ra skill vừa viết | Kiểm tra đường dẫn đúng `.claude/skills/<ten>/SKILL.md`. Gọi đích danh tên skill trong prompt. Kiểm tra frontmatter có đủ hai dòng ba dấu gạch không. |
| Claude bịa số liệu, đưa ra con số không có trong file | Nói thẳng với lớp là nó bịa, mở file gốc dò ngược trước mặt lớp. Rồi thêm dòng ràng buộc cứng vào `CLAUDE.md`, chạy lại. Lấy đó làm bài học: sửa brief chứ không sửa kết quả. |
| Mạng chậm toàn lớp | Bật phát sóng điện thoại. Vẫn chậm thì giảng viên chạy trên máy mình chiếu lên, lớp chuyển sang xem và ghi, phần thực hành chuyển sang bài tập. |
| Máy chiếu hỏng giữa buổi | Chia lớp thành 2 hoặc 3 nhóm đứng quanh màn hình laptop. Cắt phần demo dài, giữ phần thực hành. |
| Google chặn cấp quyền ở cấp quản trị công ty | Không thử đổi mạng, không mất thời gian. Chuyển ngay sang tài khoản demo của lớp hoặc tài khoản cá nhân. |

### Tình huống về lớp

| Tình huống | Xử lý ngay |
|---|---|
| Lớp mất tập trung giữa K1 (30 phút lý thuyết) | Dừng lại, hỏi một câu về nghề chứ không phải về AI, ví dụ "ở đây ai đang phải viết bài cho quá ba kênh cùng lúc?". Kéo lại rồi giảng tiếp. |
| Lớp im lặng không trả lời câu hỏi tương tác | Chờ tối đa 15 giây rồi tự trả lời và giải thích. Lần sau đổi cách hỏi: chỉ đích danh một người và hỏi về công việc của chính họ. |
| Có người đi quá nhanh, xong sớm cả khối | Giao thêm: viết mục "Khi nào KHÔNG dùng skill này" vào cuối file, hoặc viết skill thứ hai cho một việc khác ghi trên bảng ở K0. |
| Có người không theo kịp, ngồi im | Ghép trực tiếp với người bên cạnh, bảo họ đọc từng bước cho người kia gõ. Trợ giảng đứng cạnh 2 phút. Đừng để ai ngồi xem suốt buổi. |
| Có người muốn nối Drive công ty thật | Từ chối dứt khoát, không thương lượng. Nêu lý do: dữ liệu khách hàng của người khác. Đề nghị bàn với IT sau buổi nếu công ty muốn triển khai chính thức. |
| Có người hỏi "AI có thay thế người làm content không?" | Trả lời thẳng và ngắn: "Trong buổi hôm nay, người vẫn viết brief, người vẫn viết quy trình, người vẫn duyệt và bấm đăng. Cái nó thay là việc gõ lại và việc dò từ cấm. Ai viết brief và quy trình giỏi thì càng có giá." Không né, không hứa quá. |
| Có người hỏi câu vượt phạm vi buổi, ví dụ về tự động đăng bài hoặc bàn giao skill cho team | Ghi câu hỏi lên góc bảng, hẹn trả lời ở Buổi 5 và Buổi 6. Đừng sa đà giữa giờ thực hành. |
| Có người bảo "bài AI viết vẫn chưa hay bằng tôi viết" | Đồng ý luôn, đừng cãi: "Đúng, và hôm nay mục tiêu không phải hay hơn anh chị. Mục tiêu là bản nháp thứ nhất mất 30 giây thay vì 30 phút, và nó không bao giờ quên danh sách từ cấm." |

### ƯU TIÊN KHI THIẾU GIỜ

Thứ tự giữ lại, từ quan trọng nhất: **K3 (viết skill) > K1 (lý thuyết) > K2 (CLAUDE.md) > K4 (MCP) > K5 > K0.**

- **Thiếu 5 phút:** rút chặng 4 của K3 (soi và sửa skill) xuống 3 phút, chuyển phần sửa sang bài tập về nhà.
- **Thiếu 10 phút:** bỏ phần thực hành nối MCP ở K4, chỉ giữ lời giảng và demo của giảng viên, phát hướng dẫn về nhà. Vẫn giữ nguyên đoạn cảnh báo an toàn dữ liệu.
- **Thiếu 15 phút trở lên:** gộp chặng 3 của K3 (hook và CTA) vào bài tập về nhà, và cắt K4 xuống còn 10 phút chỉ demo. Vẫn giữ nguyên K1 và chặng 1, chặng 2 của K3.
- **Không bao giờ cắt:** phần thử phép chống bịa ở K2 bước 3; đoạn cảnh báo an toàn dữ liệu ở K4; và quy định cứng về tài khoản demo.

---

## GHI CHÚ CUỐI

- **Ranh giới với Buổi 5.** Buổi 1 chỉ nối 1 MCP và chỉ ĐỌC dữ liệu, không ghi, không đăng. Tự động hóa nhiều bước và luồng đăng bài là nội dung của Buổi 5. Nếu học viên hỏi về việc cho Claude tự đăng bài lên Facebook, ghi câu hỏi lên bảng và hẹn Buổi 5. Đừng demo trước, vì demo trước mà không có phần người duyệt đi kèm là dạy sai thứ tự.
- **Ranh giới với Buổi 6.** Buổi 1 chỉ viết 1 skill đơn giản cho chính học viên dùng. Đóng gói skill thành bộ bàn giao được cho người khác, kèm playbook và chỉ số đo, là nội dung của Buổi 6. Nếu có người hỏi cách chia skill cho cả phòng, trả lời ngắn "được, và Buổi 6 làm việc đó" rồi quay lại bài.
- **Feed sang Buổi 2.** File `CLAUDE.md` và skill `viet-bai-ban-hang` là nền để Buổi 2 dựng Customer Insight Agent. Ai chưa hoàn thành 2 thứ này thì phải làm bù trước Buổi 2, nếu không sẽ không chạy tiếp được. Giảng viên ghi lại danh sách người chưa xong ngay cuối K5.
- **Mục "5 nỗi đau khách" trong `CLAUDE.md` hôm nay bắt buộc gắn nhãn `[SUY LUẬN]`.** Đây là chủ ý thiết kế, không phải thiếu sót. Buổi 2 sẽ thay phần suy luận đó bằng lời khách nói thật rút từ review và tin nhắn. Giảng viên phải nói rõ điều này ở K5, nếu không học viên sẽ tưởng bộ nỗi đau đó là dữ liệu thật.
- **Toàn bộ 10 prompt trong bài soạn này phải khớp nguyên văn với phiếu copy prompt phát cho học viên.** Không tự sửa lời prompt trước lớp. Cần sửa thì sửa đồng thời ở cả bài soạn, phiếu copy và bản mềm trên Drive lớp.
- **Số liệu trong Google Sheet `thao-an-don-hang-demo` là số mô phỏng phục vụ đào tạo**, và Thảo An là thương hiệu giả định. Nói rõ điều này với lớp ít nhất một lần, để không ai mang số đó đi dùng thật.
- **Buổi 1 KHÔNG dạy:** viết quảng cáo trả tiền và tối ưu ads; phân tích review khách (Buổi 2); chấm điểm lead sỉ và soạn proposal (Buổi 3); dựng chiến dịch nhiều ngày (Buổi 4); tự động hóa và đăng bài (Buổi 5); đóng gói bàn giao (Buổi 6).
