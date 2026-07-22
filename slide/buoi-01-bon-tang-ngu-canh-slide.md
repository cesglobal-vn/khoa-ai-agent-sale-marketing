# Nội dung slide Buổi 01: Bốn tầng ngữ cảnh cho Claude

**Khóa:** AI Agent cho Sale & Marketing
**Hình thức:** online live qua Zoom hoặc Meet
**Thời lượng buổi:** 150 phút
**Tổng số slide:** 40 slide, trong đó 22 slide nội dung và bảng, 13 slide prompt, 3 slide đề bài thực hành, 1 slide bìa, 1 slide giải lao
**Giáo án nguồn:** `giao-an/buoi-01-bon-tang-ngu-canh.md`
**Ma trận mục tiêu:** `00-tong-quan/ma-tran-muc-tieu.md` mục tiêu 1.1 tới 1.5

## Ghi chú thiết kế chung

- Nền trắng, chữ đậm, cỡ chữ tối thiểu 28pt vì lớp học qua màn hình chia sẻ
- Slide prompt để chữ cỡ lớn trong khối code, học viên nhìn màn hình chia sẻ gõ theo được
- Mỗi slide một thông điệp, tối đa 6 dòng
- Phần "Lời giảng viên nói khi chiếu slide này" KHÔNG in lên slide
- Màu, logo, font do bước đóng gói áp vào, không ghi ở đây

---

### Slide 1: Buổi 1. Đóng gói ngữ cảnh cho Claude

**Loại:** tiêu đề

**Nội dung hiển thị:**
- AI Agent cho Sale & Marketing
- Buổi 1 trên 6
- CLAUDE.md, Skill, Memory, MCP
- 150 phút, học trực tiếp qua màn hình chia sẻ

**Lời giảng viên nói khi chiếu slide này:** "Chào anh chị. Trước khi vào bài, tôi hỏi một câu và anh chị trả lời thật lòng giúp tôi trong ô chat: ai ở đây từng gõ lại đoạn giới thiệu thương hiệu của mình vào một ô chat AI, quá năm lần rồi? Anh chị gõ số 1 vào chat nếu đúng."

**Hình minh họa gợi ý:** Tên buổi cỡ rất lớn ở giữa. Bốn ô nhỏ xếp ngang dưới chân slide ghi bốn từ: BRIEF, QUY TRÌNH, TRÍ NHỚ, THẺ RA VÀO.

**Thời điểm:** K0, phút 0

---

### Slide 2: Hết buổi hôm nay anh chị làm được gì

**Loại:** nội dung

**Nội dung hiển thị:**
- Chỉ đúng nội dung nào đặt vào tầng nào trong bốn tầng
- Viết `CLAUDE.md` đủ 9 mục, giọng văn tả bằng hành vi
- Dựng skill `viet-bai-ban-hang` chạy ra bài thật
- Bật Memory và nối 1 MCP đọc dữ liệu thật
- Bắt được lúc Claude bịa số và sửa brief để chặn

**Lời giảng viên nói khi chiếu slide này:** "Năm dòng này là năm thứ tôi sẽ chấm ở cuối buổi. Không phải chấm bằng điểm, mà chấm bằng file trên máy anh chị. Cuối buổi tôi gọi vài người chia sẻ màn hình, mở file ra, đủ mục thì đạt. Anh chị chú ý dòng cuối: bắt được lúc Claude bịa. Đây là dòng phân biệt người dùng AI được việc với người dùng AI để rồi mang số sai đi báo cáo."

**Hình minh họa gợi ý:** 5 ô có ô vuông trống để tích, xếp dọc.

**Thời điểm:** K0, phút 1

---

### Slide 3: Nhịp buổi hôm nay

**Loại:** bảng

**Nội dung hiển thị:**

| Khối | Đồng hồ | Việc |
|---|---|---|
| K0 | 08:00 - 08:15 | Mở máy, tạo thư mục làm việc |
| K1 | 08:15 - 08:40 | Chỉ nghe và ghi vở |
| K2 | 08:40 - 09:05 | Viết CLAUDE.md, bật Memory |
| Nghỉ | 09:05 - 09:15 | Giải lao |
| K3 | 09:15 - 09:55 | Viết skill đầu tiên |
| K4 | 09:55 - 10:20 | Nối MCP |
| K5 | 10:20 - 10:30 | Tổng kết, giao bài |

**Lời giảng viên nói khi chiếu slide này:** "Về cách chạy buổi: mười lăm phút đầu anh chị mở máy làm quen, rồi hai mươi lăm phút tiếp theo chỉ nghe và ghi vở, không ai phải gõ gì. Từ khối thứ ba trở đi là gõ liên tục tới hết buổi, kể cả lúc tôi demo. Tôi gõ trên máy tôi thì anh chị gõ cùng lúc trên máy mình, tôi đi chậm và chờ cả lớp. Một lưu ý về công cụ: cả buổi hôm nay chỉ dùng Claude Desktop, và chỉ dùng tab Code ở trên cùng, không phải tab Chat."

**Hình minh họa gợi ý:** Thanh ngang chia 7 đoạn theo tỉ lệ thời lượng, đoạn K3 tô đậm nhất.

**Thời điểm:** K0, phút 2

---

### Slide 4: Ba thứ kiểm ngay bây giờ

**Loại:** nội dung

**Nội dung hiển thị:**
- Đã cài Claude Desktop và đăng nhập được
- Đang dùng tài khoản trả phí, Pro trở lên
- Đã cài Git for Windows
- Ai thiếu thì gõ vào chat ngay, đừng ngồi im

**Lời giảng viên nói khi chiếu slide này:** "Sáu phút này ai cũng phải làm được. Ai vướng thì gõ vào ô chat ngay, đừng ngồi im, vì cả buổi sau dựa vào bước này. Nói thật với anh chị về Git: Git không bắt buộc tuyệt đối, thiếu Git thì Claude Code vẫn chạy được bằng PowerShell có sẵn trong Windows. Nhưng cả lớp cài để mọi máy giống nhau, tôi hướng dẫn một đường là đúng cho tất cả. Ai dùng tài khoản miễn phí thì tôi nói thẳng: gói miễn phí sẽ hết lượt giữa buổi, không đủ cho 150 phút thực hành."

**Hình minh họa gợi ý:** 3 ô vuông trống để tích, mỗi ô một dòng.

**Thời điểm:** K0, phút 5

---

### Slide 5: Tạo thư mục làm việc, làm theo 6 bước

**Loại:** sơ đồ

**Nội dung hiển thị:**
1. Chuột phải màn hình nền, New rồi Folder
2. Đặt tên `thao-an-marketing`, không dấu, không cách
3. Mở Claude Desktop, bấm tab **Code**
4. Bấm nút mở thư mục, trỏ tới thư mục vừa tạo
5. Gõ: `Bạn đang mở thư mục nào?`
6. Kéo file `san-pham-thao-an.md` vào thư mục

**Lời giảng viên nói khi chiếu slide này:** "Anh chị làm theo tôi từng bước, tôi đọc số mấy anh chị làm số đó. Ai xong bước nào thì gõ số bước đó vào ô chat cho tôi biết. Bước 5 là bước kiểm: Claude phải trả lời đúng tên thư mục đó. Nếu nó trả lời sai hoặc nói không mở thư mục nào, tức là bước 4 chưa xong, anh chị làm lại bước 4."

**Hình minh họa gợi ý:** 6 ô nối bằng mũi tên, ô số 5 tô đậm và ghi thêm chữ "chỗ kiểm".

**Thời điểm:** K0, phút 6

---

### Slide 6: PROMPT 0. Tạo file đầu tiên

**Loại:** prompt

**Nội dung hiển thị:**

```
Tạo giúp tôi file viec-lap-lai.md ngay trong thư mục làm việc này.

Nội dung file gồm đúng 3 dòng, mỗi dòng là một đầu việc nội dung
hoặc bán hàng mà tuần nào tôi cũng phải làm lại:

1. [gõ việc thứ nhất của anh chị vào đây]
2. [gõ việc thứ hai vào đây]
3. [gõ việc thứ ba vào đây]

Chỉ tạo file, chưa phân tích gì cả. Tạo xong đọc lại nội dung
file cho tôi xem.
```

**Lời giảng viên nói khi chiếu slide này:** "Anh chị không cầm bút. Anh chị gõ vào ô nhập của tab Code đúng câu trên màn hình này, rồi tự điền ba việc của mình vào. Ví dụ: viết bài bán hàng cho Facebook, trả lời tin nhắn hỏi giá, soạn email chào sỉ cho spa, viết kịch bản video ngắn. Bản mềm prompt nằm trên Drive lớp, link tôi đã ghim trong chat. Dán xong rồi tôi nói tiếp: anh chị vừa tạo file đầu tiên bằng cách bảo Claude tạo. Không mở Notepad, không nhớ chỗ Save as. Đây là cách cả buổi hôm nay anh chị tạo file."

**Hình minh họa gợi ý:** Khối code chiếm trọn slide, cỡ chữ lớn nhất có thể.

**Thời điểm:** K0, phút 11

---

### Slide 7: Đề bài K0. Ba việc anh chị làm đi làm lại

**Loại:** thực hành

**Nội dung hiển thị:**
- Việc: gõ 3 đầu việc nội dung hoặc bán hàng làm lại hàng tuần
- Thời gian: 4 phút
- Nộp: file `viec-lap-lai.md` trong thư mục làm việc
- Đây là đề bài chính thức của K3 lát nữa

**Lời giảng viên nói khi chiếu slide này:** "Ba đầu việc mà tuần nào anh chị cũng phải làm lại, liên quan tới nội dung hoặc bán hàng. Mỗi việc một dòng, không cần dài. Anh chị có 4 phút, tôi đếm ngược. Trong lúc anh chị gõ, tôi đọc ô chat và gom lại ba việc nhiều người cùng nêu nhất, tôi sẽ ghim lên đầu chat. Lát nữa ở K3 anh chị viết skill cho một trong ba việc này."

**Hình minh họa gợi ý:** Số 4 cỡ rất lớn kèm biểu tượng đồng hồ đếm ngược.

**Thời điểm:** K0, phút 11 tới 15

---

### Slide 8: 25 phút tới anh chị bỏ tay khỏi bàn phím

**Loại:** chuyển khối

**Nội dung hiển thị:**
- K1: 08:15 tới 08:40
- Chỉ nghe và ghi vở, không ai gõ máy
- Bốn thứ phải có trong vở khi hết khối
- Cuối khối có demo, đừng bỏ đoạn đó

**Lời giảng viên nói khi chiếu slide này:** "Tôi biết ngồi nghe hai mươi lăm phút hơi lâu, nhất là khi học qua màn hình. Nhưng bỏ qua phần này thì lúc mở máy anh chị sẽ làm mà không hiểu mình đang làm gì. Bốn thứ phải có trong vở: bảng bốn tầng, sơ đồ bốn bước skill chạy, đường dẫn file SKILL.md, và ba nguyên tắc chống bịa. Cuối khối tôi có một demo so sánh, đó là mười phút đắt nhất của cả buổi."

**Hình minh họa gợi ý:** Biểu tượng quyển vở và cây bút, gạch chéo lên biểu tượng bàn phím.

**Thời điểm:** K1, phút 15

---

### Slide 9: Bốn tầng ngữ cảnh và năng lực

**Loại:** bảng

**Nội dung hiển thị:**

| Tầng | Trong Claude là gì | Ví như trong nghề marketing |
|---|---|---|
| 1 | File `CLAUDE.md` | Bản brief thương hiệu ai vào team cũng đọc |
| 2 | Skill, `.claude/skills/<tên>/SKILL.md` | Quy trình chuẩn cho từng đầu việc |
| 3 | Memory | Sổ bàn giao khi bạn content nghỉ phép |
| 4 | MCP | Thẻ ra vào có phân quyền |

**Lời giảng viên nói khi chiếu slide này:** "Ngữ cảnh là những thứ AI cần biết trước khi bắt tay vào việc. Giống một bạn content mới nhận việc: trước khi giao bài, anh chị phải cho bạn ấy biết thương hiệu bán gì, bán cho ai, giọng viết thế nào, từ nào cấm dùng. Nếu không nói, bạn ấy viết sai không phải vì kém, mà vì không biết. Tầng 1 ai vào team cũng đọc, nên chỉ ghi thứ luôn đúng cho mọi việc. Tầng 2 chỉ lấy ra khi đúng việc, nên được phép dài và chi tiết. Tầng 3 tiện nhưng phải kiểm định kỳ, nó nhớ sai một điều thì áp cái sai đó vào mọi bài sau. Tầng 4 là lúc Claude thôi ngồi trong phòng kín."

**Hình minh họa gợi ý:** 4 tầng xếp chồng như bánh kem, tầng 1 dưới cùng rộng nhất.

**Thời điểm:** K1, phút 15 tới 21

---

### Slide 10: Bốn câu chép vào vở

**Loại:** nội dung

**Nội dung hiển thị:**
1. CLAUDE.md đọc trước mọi việc, nên chỉ ghi thứ luôn đúng
2. Skill chỉ lấy khi đúng việc, nên ghi càng chi tiết càng tốt
3. Memory Claude tự ghi tự dùng lại, nên phải kiểm định kỳ
4. MCP với tới dữ liệu thật, nên phải biết đường gỡ quyền

**Lời giảng viên nói khi chiếu slide này:** "Bốn câu này anh chị chép nguyên vào vở. Tôi hỏi nhanh một câu, anh chị gõ đáp án vào chat: cái quy trình 8 bước để viết một bài bán hàng cho Facebook, nên đặt vào tầng mấy? Đáp án là tầng 2, skill. Ai trả lời tầng 1 thì tôi hỏi lại: nếu đặt vào bản brief thì lúc anh chị nhờ nó soạn email chào sỉ, nó cũng phải đọc 8 bước viết bài Facebook. Có cần không?"

**Hình minh họa gợi ý:** 4 dòng đánh số lớn, mỗi số trong một vòng tròn.

**Thời điểm:** K1, phút 21

---

### Slide 11: Claude tìm và dùng skill thế nào

**Loại:** sơ đồ

**Nội dung hiển thị:**
1. Anh chị nêu yêu cầu
2. Claude lướt qua nhãn dán của từng skill
3. Rút đúng tập ra, nạp toàn bộ SKILL.md
4. Làm theo từng bước, thiếu tin thì hỏi ngược lại

**Lời giảng viên nói khi chiếu slide này:** "Bước 2 là bước quan trọng nhất. Claude nhìn qua tất cả skill đang có, nhưng nó KHÔNG đọc hết. Nó chỉ đọc đúng một dòng mô tả của mỗi skill, giống anh chị lướt mắt qua nhãn dán trên gáy từng tập tài liệu trong tủ. Hai điểm nhớ kỹ. Thứ nhất: chất lượng kết quả phụ thuộc chất lượng quy trình anh chị viết, không phụ thuộc anh chị gõ câu lệnh hay hay dở. Thứ hai: Claude chọn skill dựa vào cái nhãn, tức dòng description. Nhãn viết mơ hồ thì nó rút nhầm tập tài liệu."

**Hình minh họa gợi ý:** 4 ô nối mũi tên. Ô số 2 vẽ thêm hình tủ hồ sơ có gáy dán nhãn.

**Thời điểm:** K1, phút 21 tới 24

---

### Slide 12: Skill nằm ở đâu và mở đầu bằng gì

**Loại:** nội dung

**Nội dung hiển thị:**

```
.claude/skills/viet-bai-ban-hang/SKILL.md
```

```
---
name: viet-bai-ban-hang
description: Viết bài bán hàng cho Facebook và Shopee của
  Thảo An. Dùng khi cần bài giới thiệu một SKU, bài xử lý lo
  ngại kích ứng, hoặc bài đẩy đơn dịp khuyến mãi. Không dùng
  cho email chào sỉ B2B.
---
```

**Lời giảng viên nói khi chiếu slide này:** "Một skill trong Claude là một THƯ MỤC, chứ không phải một file lẻ. Đọc từ phải sang cho dễ: file tên đúng là SKILL.md, viết hoa cả chữ SKILL. Nó nằm trong thư mục mang tên skill. Thư mục đó nằm trong skills. skills nằm trong chấm claude. Còn cái khung dưới gọi là frontmatter, nghe lạ nhưng đơn giản: mấy dòng khai báo tên và mô tả, kẹp giữa hai dòng ba dấu gạch. Dòng description chính là cái nhãn dán trên gáy hồ sơ. Đây là dòng anh chị phải viết kỹ nhất trong cả file. Anh chị nhìn ví dụ: nói rõ viết cho kênh nào, ba tình huống nào thì gọi ra, và một câu nói rõ khi nào KHÔNG dùng."

**Hình minh họa gợi ý:** Đường dẫn tách thành 4 khối màu nối bằng dấu gạch chéo, khối `SKILL.md` đậm nhất.

**Thời điểm:** K1, phút 24 tới 28

---

### Slide 13: Sáu phần dưới frontmatter

**Loại:** nội dung

**Nội dung hiển thị:**
1. Skill này làm gì
2. Đầu vào bắt buộc, chỗ hay bị bỏ sót nhất
3. Các bước làm, bước 1 luôn là kiểm đủ đầu vào
4. Ràng buộc: từ cấm, độ dài, xưng hô, số emoji
5. Định dạng đầu ra
6. Ví dụ mẫu, một bài đã viết xong

**Lời giảng viên nói khi chiếu slide này:** "Sáu phần này anh chị chép vào vở vì lát nữa K3 dùng ngay. Mục 2 là chỗ hay bị bỏ sót nhất, thiếu ở đây thì Claude tự đoán, mà nó đoán thì bài ra chung chung. Mục 6 là mẹo hay nhất: Claude bắt chước một bài mẫu đã viết xong nhanh hơn nhiều so với đọc lời tả. Giống anh chị đào tạo bạn content mới, đưa họ đọc ba bài đã đăng và đúng giọng thì họ hiểu ngay, còn tả bằng miệng thì họ vẫn mơ hồ."

**Hình minh họa gợi ý:** 6 ô xếp 2 hàng 3 cột, ô số 2 và ô số 6 tô đậm.

**Thời điểm:** K1, phút 28 tới 32

---

### Slide 14: Ba nguyên tắc chống bịa

**Loại:** nội dung

**Nội dung hiển thị:**
1. Chỉ dùng dữ liệu người dùng cấp
2. Gắn nhãn nguồn: `[DATA THẬT]`, `[SUY LUẬN]`, "chưa đủ dữ liệu"
3. Người duyệt cuối, Claude không tự bấm đăng

**Lời giảng viên nói khi chiếu slide này:** "Phần này ngắn nhưng là phần tách khóa này khỏi các khóa dạy mẹo prompt. Nguyên tắc một quan trọng gấp đôi trong ngành mỹ phẩm, vì bịa một công dụng là chạm vào chuyện pháp lý, không chỉ là chuyện viết sai. Nguyên tắc hai quan trọng nhất, vì AI không biết là nó đang bịa, nó chỉ đang chọn từ nghe hợp lý tiếp theo. Bắt nó gắn nhãn là bắt nó tự khai chỗ nào chắc, chỗ nào đoán. Anh chị chỉ phải soi kỹ phần suy luận. Báo trước: lát nữa tôi sẽ cố tình hỏi Claude một con số mà hồ sơ Thảo An ghi rõ là chưa có."

**Hình minh họa gợi ý:** 3 dòng, dòng số 2 to gấp rưỡi hai dòng kia.

**Thời điểm:** K1, phút 32 tới 34

---

### Slide 15: DEMO. Chạy trong một thư mục trống

**Loại:** prompt

**Nội dung hiển thị:**

```
Viết cho tôi 1 bài đăng Facebook bán serum rau má B5
của thương hiệu Thảo An.
```

- Thư mục `demo-trong`: không brief, không skill, không hồ sơ

**Lời giảng viên nói khi chiếu slide này:** "Anh chị nhìn màn hình tôi chia sẻ. Thư mục này hoàn toàn trống. Không có brief, không có skill, không có hồ sơ sản phẩm. Đúng như tình trạng máy anh chị lúc mới cài xong. Tôi gõ đúng một câu này thôi. Anh chị chưa gõ gì cả, chỉ nhìn."

**Hình minh họa gợi ý:** Khối code lớn, bên cạnh là biểu tượng thư mục rỗng.

**Thời điểm:** K1, phút 34 tới 37

---

### Slide 16: Bài này sai ở đâu

**Loại:** nội dung

**Nội dung hiển thị:**
- Bịa hoặc né giá, giá thật là 320.000đ cho 30ml
- Bịa thành phần, hoặc "chiết xuất thiên nhiên" chung chung
- Dính từ cấm: trị mụn, đặc trị, trắng da cấp tốc
- Hứa thời gian: 7 ngày hết thâm
- Xưng hô sai: chúng tôi, quý khách
- Thay tên thương hiệu nào vào cũng dùng được

**Lời giảng viên nói khi chiếu slide này:** "Nhìn lướt thì trông cũng được đấy chứ: đúng ngữ pháp, có emoji, có kêu gọi mua. Nhưng nếu anh chị là người duyệt bài của Thảo An, anh chị sẽ trả lại. Anh chị gõ vào chat giúp tôi những chỗ sai và những chỗ chung chung. Gạch cuối cùng là phép thử tôi muốn anh chị mang về dùng mãi: lấy một câu trong bài, thay tên Thảo An bằng tên đối thủ. Nếu câu đó vẫn đúng thì câu đó chưa dùng được."

**Hình minh họa gợi ý:** 6 dòng, mỗi dòng có dấu X ở đầu. Dòng cuối tô đậm và đóng khung.

**Thời điểm:** K1, phút 37 tới 39

---

### Slide 17: DEMO. Chạy trong thư mục có ngữ cảnh

**Loại:** prompt

**Nội dung hiển thị:**

```
Dùng skill viet-bai-ban-hang để viết 1 bài đăng Facebook bán
SKU-01 Serum rau má B5 của Thảo An.

Đầu vào:
- Người đọc: nữ 25 đến 40 tuổi, da nhạy cảm hoặc da sau mụn,
  ngân sách 200 đến 500 nghìn cho một sản phẩm dưỡng da.
- Kênh đăng: Facebook, bài thường, không phải quảng cáo trả tiền.
- Mục tiêu của bài: người đọc nhắn tin hỏi thêm.

Chỉ dùng thông tin có trong file san-pham-thao-an.md và
CLAUDE.md của thư mục này. Không thêm thành phần, công dụng,
giá hay con số nào ngoài hồ sơ. Chỗ nào thiếu dữ liệu thì ghi
"chưa đủ dữ liệu", đừng đoán.

Cuối bài, liệt kê riêng thành 2 nhóm: câu nào là [DATA THẬT],
câu nào là [SUY LUẬN].
```

**Lời giảng viên nói khi chiếu slide này:** "Vẫn là Claude đó. Vẫn là tôi gõ. Khác duy nhất: lần này thư mục có bản brief và có quy trình viết bài. Anh chị để ý ba chỗ khi kết quả ra: giá đúng 320.000đ cho 30ml, không còn từ cấm, và có phần gắn nhãn nguồn ở cuối."

**Hình minh họa gợi ý:** Khối code lớn, bên cạnh là biểu tượng thư mục có 3 file.

**Thời điểm:** K1, phút 39 tới 40

---

### Slide 18: Cùng một Claude, khác duy nhất ở ngữ cảnh

**Loại:** chuyển khối

**Nội dung hiển thị:**
- 25 phút vừa rồi: anh chị hiểu ngữ cảnh là gì
- 100 phút còn lại: tự tay dựng nó
- Từ đây trở đi anh chị gõ cùng lúc với tôi
- Bắt đầu với tầng 1: bản brief thương hiệu

**Lời giảng viên nói khi chiếu slide này:** "Cùng một Claude. Cùng một người gõ. Khác nhau duy nhất ở chỗ có ngữ cảnh hay không. Giờ anh chị mở máy ra, đặt tay lên bàn phím. Từ giờ tới hết buổi, tôi gõ gì thì anh chị gõ y hệt trên máy mình, không ngồi nhìn. Tôi đi chậm hơn bình thường và tôi sẽ dừng lại chờ. Ai chưa kịp thì gõ chữ CHỜ vào chat ngay, đừng để tôi chạy tiếp rồi anh chị mất luôn khúc sau."

**Hình minh họa gợi ý:** Hai cột kết quả đặt cạnh nhau, cột trái mờ, cột phải đậm. Mũi tên lớn chỉ sang phải.

**Thời điểm:** K2, phút 40

---

### Slide 19: PROMPT 3. Viết CLAUDE.md, phần 1

**Loại:** prompt

**Nội dung hiển thị:**

```
Trong thư mục này có file san-pham-thao-an.md. Đọc kỹ file đó
trước khi làm.

Sau đó tạo giúp tôi file CLAUDE.md đặt ngay trong thư mục này.
Đây là bản brief thương hiệu mà bạn sẽ đọc trước MỌI việc tôi
giao trong thư mục này.

Viết đủ 9 mục sau, mỗi mục một tiêu đề riêng:

1. Thương hiệu này là ai: viết 1 câu định vị duy nhất, có đủ
   4 phần: bán cho ai, giải quyết chuyện gì, khác đối thủ ở
   đâu, bằng chứng nào.
2. Bán gì: liệt kê 3 SKU, mỗi SKU ghi giá, thành phần chính,
   công dụng ghi trên nhãn, hợp với loại da nào. Lấy đúng số
   trong hồ sơ, không làm tròn.
3. Bán cho ai: chân dung khách B2C và chân dung khách B2B.
4. Ba thông điệp bán hàng, mỗi thông điệp 1 dòng.
5. Năm nỗi đau của khách. Vì hôm nay tôi chưa đưa bạn review
   khách thật, phần này bạn phải đánh dấu [SUY LUẬN] và ghi rõ
   cần kiểm chứng lại.
```

**Lời giảng viên nói khi chiếu slide này:** "Prompt này dài, anh chị đừng gõ tay. Bản mềm nằm trên Drive lớp, link tôi đã ghim trong chat. Anh chị copy nguyên cả đoạn, cả phần trên slide sau nữa, dán một lần vào ô nhập của tab Code. Ai có thương hiệu thật của mình thì thay hồ sơ Thảo An bằng hồ sơ của mình, nhưng giữ nguyên cấu trúc prompt. Chưa bấm Enter vội, chờ tôi đọc nốt phần sau."

**Hình minh họa gợi ý:** Khối code chiếm trọn slide. Góc dưới ghi "còn tiếp, xem slide sau".

**Thời điểm:** K2, phút 40 tới 43

---

### Slide 20: PROMPT 3. Viết CLAUDE.md, phần 2

**Loại:** prompt

**Nội dung hiển thị:**

```
6. Giọng văn, mô tả bằng HÀNH VI chứ không phải bằng tính từ.
   Cấm dùng các từ "chuyên nghiệp", "thân thiện", "uy tín",
   "trẻ trung". Thay vào đó hãy viết rõ: xưng hô thế nào, mở
   bài bằng gì, câu dài tối đa bao nhiêu chữ, tối đa mấy dấu
   chấm than, tối đa mấy emoji.
7. Từ cấm và điều không được nói: chép nguyên danh sách trong
   mục "Điều KHÔNG được nói" của hồ sơ, không bớt dòng nào.
8. Ba nguyên tắc chống bịa, ghi nguyên văn như sau:
   - Chỉ dùng dữ liệu trong các file của thư mục này. Không tự
     chế số liệu, thành phần, công dụng, giá, tên khách.
   - Gắn nhãn nguồn: [DATA THẬT] cho thông tin trích được từ
     file, [SUY LUẬN] cho phần tự suy ra. Thiếu thì ghi
     "chưa đủ dữ liệu".
   - Mọi thứ gửi khách đều là bản nháp. Bạn không tự bấm đăng,
     không tự bấm gửi.
9. Chỗ còn thiếu dữ liệu: chép nguyên mục "Chỗ còn thiếu dữ
   liệu" của hồ sơ. Khi tôi hỏi những mục này, câu trả lời duy
   nhất được phép là "chưa đủ dữ liệu".

Viết gọn trong khoảng 60 dòng. Tiếng Việt có dấu, câu ngắn.
Đừng đưa quy trình chi tiết của từng việc vào đây, phần đó tôi
để riêng ở skill.
```

**Lời giảng viên nói khi chiếu slide này:** "Giờ anh chị dán cùng tôi, bấm Enter cùng tôi. Tôi dừng ở đây chờ. Ai đã thấy file CLAUDE.md hiện ra trong thư mục thì gõ chữ XONG vào chat. Tôi chờ tới khi có hai phần ba lớp gõ xong rồi mới đi tiếp."

**Hình minh họa gợi ý:** Khối code chiếm trọn slide.

**Thời điểm:** K2, phút 43 tới 45

---

### Slide 21: Giọng văn viết bằng hành vi, không bằng tính từ

**Loại:** nội dung

**Nội dung hiển thị:**
- Không viết: chuyên nghiệp, thân thiện, uy tín, trẻ trung
- Gọi mình là "Thảo An", gọi khách là "bạn"
- Mở bài bằng một tình huống da cụ thể, không mở bằng lời chào
- Câu dưới 20 chữ
- Tối đa 1 dấu chấm than, tối đa 2 emoji mỗi bài

**Lời giảng viên nói khi chiếu slide này:** "Anh chị mở file của chính mình ra, tôi đọc tới đâu anh chị dò tới đó trên máy mình. Anh chị để ý: ở đây không có chữ chuyên nghiệp, không có chữ thân thiện, không có chữ uy tín. Ba từ đó ai cũng viết được và AI không dùng được. Cái viết ở đây là hành vi: câu dài bao nhiêu chữ, gọi khách bằng gì, tối đa mấy emoji. Đọc một câu là biết đúng hay sai ngay. Còn danh sách từ cấm thì tôi không tự nghĩ ra, nó nằm nguyên trong mục Điều KHÔNG được nói của hồ sơ sản phẩm."

**Hình minh họa gợi ý:** Hai cột. Cột trái tiêu đề "Tính từ, bỏ" gạch chéo. Cột phải tiêu đề "Hành vi, giữ".

**Thời điểm:** K2, phút 45 tới 47

---

### Slide 22: PROMPT 4. Thử phép chống bịa

**Loại:** prompt

**Nội dung hiển thị:**

```
Dựa trên các file trong thư mục này, trả lời 3 câu sau.

Quy tắc trả lời: câu nào hồ sơ không có dữ liệu thì trả lời
đúng một câu "chưa đủ dữ liệu". Không ước lượng. Không đưa con
số tham khảo của ngành. Không nói "thường thì các thương hiệu
tương tự...".

1. Tháng này Thảo An chi bao nhiêu tiền cho quảng cáo?
2. Giá trị đơn trung bình của Thảo An là bao nhiêu?
3. Serum rau má B5 hiện có bao nhiêu đánh giá của khách?

Trả lời xong 3 câu, liệt kê thêm: trong hồ sơ còn mục dữ liệu
nào đang trống mà tôi nên bổ sung trước khi chạy quảng cáo?
```

**Lời giảng viên nói khi chiếu slide này:** "Giờ tới đoạn tôi hứa với anh chị ở khối trước. Tôi sẽ hỏi nó ba con số mà hồ sơ Thảo An ghi rõ là chưa có. Anh chị dán cùng tôi và nhìn kỹ máy của chính mình, vì rất có thể máy anh chị ra khác máy tôi. Chỗ khác nhau đó mới là chỗ đáng học. Xong rồi anh chị gõ vào chat: máy anh chị trả lời chưa đủ dữ liệu mấy trên ba câu? Kết quả đúng là ba trên ba. Một AI nói chưa đủ dữ liệu có ích hơn nhiều một AI đưa cho anh chị con số nghe rất hợp lý mà sai, vì con số sai đó anh chị sẽ mang đi báo cáo sếp."

**Hình minh họa gợi ý:** Khối code lớn. Bên dưới ghi con số "3 / 3" cỡ rất lớn kèm chữ "chưa đủ dữ liệu".

**Thời điểm:** K2, phút 47 tới 49

---

### Slide 23: Đề bài K2. CLAUDE.md của thương hiệu anh chị

**Loại:** thực hành

**Nội dung hiển thị:**
- Việc 1, 9 phút: chạy PROMPT 3, mở file đọc lại, sửa chỗ chưa đúng
- Việc 2, 6 phút: bật Memory rồi chạy PROMPT 5
- Nộp: file `CLAUDE.md` đủ 9 mục trong thư mục làm việc
- Đạt khi: mục giọng văn không chứa "chuyên nghiệp", "thân thiện", "uy tín"

**Lời giảng viên nói khi chiếu slide này:** "Mỗi người làm trên máy của mình. Tôi sẽ gọi lần lượt vài người chia sẻ màn hình, tôi chỉ soi đúng ba thứ: file có tên đúng CLAUDE.md và nằm ngay trong thư mục làm việc; mục giọng văn là hành vi hay là danh sách tính từ; mục từ cấm có đủ dòng lấy từ hồ sơ không. Ai bị Claude trả về file dài hơn 100 dòng thì gõ thêm đúng một câu: rút gọn còn khoảng 60 dòng, bỏ hết phần quy trình chi tiết của từng việc."

**Hình minh họa gợi ý:** Số 15 cỡ rất lớn kèm đồng hồ, bên dưới chia hai vạch 9 và 6.

**Thời điểm:** K2, phút 50 tới 65

---

### Slide 24: PROMPT 5. Bật Memory và kiểm tra

**Loại:** prompt

**Nội dung hiển thị:**

```
Từ giờ trở đi hãy ghi nhớ 3 điều sau về cách tôi làm việc, và
tự áp dụng lại ở những lần trò chuyện sau mà tôi không phải
dặn lại:

1. Tôi làm marketing cho Thảo An, thương hiệu mỹ phẩm dưỡng da
   từ thảo mộc, 3 SKU, bán B2C qua Facebook và Shopee, bán sỉ
   B2B cho spa. Tên SKU luôn ghi đúng là SKU-01 Serum rau má
   B5, SKU-02 Kem nghệ mật ong, SKU-03 Mặt nạ đất sét trà xanh.
2. Mỗi khi tôi nhờ viết bài bán hàng, luôn hỏi tôi đủ 4 thông
   tin trước khi viết: viết cho SKU nào, đăng kênh nào, người
   đọc là ai, mục tiêu của bài là gì (nhắn tin, bấm link, hay
   lưu bài).
3. Mọi bài viết trả về đều phải có phần cuối liệt kê câu nào
   [DATA THẬT], câu nào [SUY LUẬN]. Và mọi bài đều là bản nháp,
   tôi là người bấm đăng.

Ghi nhớ xong, đọc lại cho tôi nghe bạn đã nhớ những gì, để tôi
kiểm tra có nhớ sai chỗ nào không.
```

Câu kiểm tra, mở một cuộc trò chuyện MỚI rồi gõ:

```
Tôi làm marketing cho thương hiệu nào, và bạn cần hỏi tôi những
gì trước khi viết bài bán hàng?
```

**Lời giảng viên nói khi chiếu slide này:** "Trước khi dán prompt này, anh chị vào Cài đặt bật Memory lên trước. Bấm vào biểu tượng tài khoản, chọn Settings, tìm mục Memory hoặc Trí nhớ, gạt công tắc sang bật. Chỗ đó cũng có nút để xem lại và xóa những gì Claude đã nhớ, anh chị nhớ đường vào, vì sổ bàn giao ghi sai thì mọi bài sau sai theo. Câu kiểm tra ở dưới quan trọng: nếu ở cuộc trò chuyện mới nó vẫn trả lời đúng thì sổ bàn giao đã hoạt động. Nếu nó ngơ ngác không biết anh chị là ai thì Memory chưa bật thật, anh chị gõ vào chat cho tôi."

**Hình minh họa gợi ý:** Khối code lớn phía trên, khối code nhỏ phía dưới có viền đứt và nhãn "kiểm tra ở phiên mới".

**Thời điểm:** K2, phút 59 tới 65

---

### Slide 25: Giải lao 10 phút

**Loại:** chuyển khối

**Nội dung hiển thị:**
- Nghỉ 10 phút
- 09:15 anh chị quay lại phòng học
- Ai chưa có file `CLAUDE.md` thì ở lại, tôi làm cùng
- Đừng tắt Claude Desktop, để nguyên đó

**Lời giảng viên nói khi chiếu slide này:** "Anh chị nghỉ 10 phút, đúng 09:15 quay lại. Tôi để slide này trên màn hình chia sẻ suốt giờ nghỉ, kèm đồng hồ đếm ngược, anh chị nhìn là biết còn mấy phút. Ai chưa có file CLAUDE.md thì đừng tắt phòng, ở lại với tôi, vì bước sau dựa hoàn toàn vào file này. Ai đang cài Git dở thì trợ giảng sẽ vào phòng nhỏ hỗ trợ."

**Hình minh họa gợi ý:** Đồng hồ đếm ngược cỡ rất lớn ở giữa. Dòng chữ "09:15 quay lại" ngay dưới.

**Thời điểm:** Giải lao, phút 65 tới 75

---

### Slide 26: K3. Viết skill đầu tiên, 33 phút chia 4 chặng

**Loại:** chuyển khối

**Nội dung hiển thị:**
- Chặng 1, 13 phút: nhờ Claude viết skill
- Chặng 2, 10 phút: chạy skill ra 3 bài bán hàng
- Chặng 3, 5 phút: chạy ra 10 hook và 10 CTA
- Chặng 4, 5 phút: bảo Claude soi lại skill và sửa
- Tôi bấm giờ báo chuyển chặng

**Lời giảng viên nói khi chiếu slide này:** "Đây là phần quan trọng nhất buổi hôm nay, và cũng là phần anh chị mang về dùng được ngay từ chiều nay. Nhắc lại đường dẫn: skill là một THƯ MỤC nằm ở chấm claude gạch chéo skills, bên trong có file tên đúng là SKILL.md. Anh chị không phải tự tạo mấy thư mục lồng nhau đó, cứ bảo Claude tạo, nó tạo hết. Ai có thương hiệu thật thì làm cho thương hiệu mình. Ai muốn làm skill cho một trong ba việc đã gõ vào file viec-lap-lai.md ở đầu buổi thì đổi phần việc cần chuẩn hóa trong prompt, giữ nguyên phần còn lại."

**Hình minh họa gợi ý:** Thanh ngang chia 4 đoạn theo tỉ lệ 13, 10, 5, 5. Mỗi đoạn ghi tên chặng.

**Thời điểm:** K3, phút 75 tới 77

---

### Slide 27: PROMPT 6. Dựng skill, phần 1

**Loại:** prompt

**Nội dung hiển thị:**

```
Tạo cho tôi một skill mới trong thư mục làm việc này.

Đường dẫn file: .claude/skills/viet-bai-ban-hang/SKILL.md
Nếu thư mục .claude hoặc .claude/skills chưa có thì tạo luôn.

File bắt đầu bằng phần frontmatter kẹp giữa hai dòng ba dấu
gạch, bên trong có đúng 2 dòng: name và description.
- name: viet-bai-ban-hang
- description: viết thật kỹ dòng này, vì đây là dòng bạn dùng
  để quyết định có gọi skill này ra hay không. Trong một dòng
  phải nói được: skill viết bài bán hàng cho kênh nào của Thảo
  An, ba tình huống cụ thể khiến nó được gọi ra, và một tình
  huống rõ ràng KHÔNG dùng nó.

Phần dưới frontmatter viết bằng markdown, đủ 6 mục sau:

1. Skill này làm gì: 3 dòng.
2. Đầu vào bắt buộc: 4 thứ tôi phải cấp trước khi bạn viết,
   gồm viết cho SKU nào, đăng kênh nào, người đọc là ai, mục
   tiêu bài là gì.
```

**Lời giảng viên nói khi chiếu slide này:** "Năm phút này anh chị gõ cùng tôi, không ngồi xem. Prompt gồm hai slide, anh chị copy cả hai phần từ bản mềm trên Drive, dán một lần. Tôi đọc nốt phần sau rồi ta cùng bấm Enter."

**Hình minh họa gợi ý:** Khối code chiếm trọn slide. Góc dưới ghi "còn tiếp".

**Thời điểm:** K3, phút 77 tới 79

---

### Slide 28: PROMPT 6. Dựng skill, phần 2

**Loại:** prompt

**Nội dung hiển thị:**

```
3. Các bước làm: đánh số 8 bước, mỗi bước một việc. Bước 1 bắt
   buộc là kiểm tra đủ 4 đầu vào, thiếu thì hỏi lại tôi, tuyệt
   đối không tự đoán. Trong 8 bước phải có: chọn 1 nỗi đau cụ
   thể để mở bài; nêu thành phần trước rồi mới nêu công dụng;
   đối chiếu toàn bài với danh sách từ cấm trong CLAUDE.md;
   bước cuối gắn nhãn [DATA THẬT] hoặc [SUY LUẬN] cho từng ý.
4. Ràng buộc: chép danh sách từ cấm và quy tắc giọng văn từ
   CLAUDE.md của thư mục này. Thêm: bài dài 120 đến 180 chữ,
   câu dưới 20 chữ, tối đa 1 dấu chấm than, tối đa 2 emoji.
5. Định dạng đầu ra: bài gồm 4 phần theo thứ tự là hook mở bài,
   phần thân, câu kêu gọi hành động, rồi phần gắn nhãn nguồn
   đặt cuối cùng.
6. Ví dụ mẫu: viết luôn 1 bài hoàn chỉnh cho SKU-01 Serum rau
   má B5, đăng Facebook, người đọc là nữ 25 đến 40 tuổi da nhạy
   cảm, mục tiêu là nhắn tin. Dùng đúng giá và đúng thành phần
   trong file san-pham-thao-an.md.

Viết bằng tiếng Việt có dấu, câu ngắn, người không rành máy
tính đọc là làm theo được. Không dùng thuật ngữ lập trình.
```

**Lời giảng viên nói khi chiếu slide này:** "Dán cùng tôi, bấm Enter cùng tôi. Tôi dừng ở đây: ai đã thấy Claude báo tạo xong file SKILL.md thì gõ XONG vào chat. Tôi chờ hai phần ba lớp. Máy nào chưa ra thì trợ giảng vào phòng nhỏ ngay, vì cả 33 phút sau dựa vào file này. Ra rồi thì anh chị gõ tiếp: cho tôi xem nội dung file SKILL.md vừa tạo. Rồi thử một yêu cầu cố ý thiếu: dùng skill viet-bai-ban-hang viết cho tôi một bài. Nó phải hỏi ngược lại anh chị bốn thông tin đầu vào."

**Hình minh họa gợi ý:** Khối code chiếm trọn slide.

**Thời điểm:** K3, phút 79 tới 82

---

### Slide 29: Đề bài chặng 1. Skill của chính anh chị

**Loại:** thực hành

**Nội dung hiển thị:**
- Việc: chạy PROMPT 6, đọc lại file, viết kỹ dòng `description`
- Thời gian: 13 phút
- Nộp: `.claude/skills/viet-bai-ban-hang/SKILL.md`
- Đạt khi: frontmatter đủ 2 dòng, description nêu cả tình huống KHÔNG dùng, mục 6 có 1 bài mẫu viết xong

**Lời giảng viên nói khi chiếu slide này:** "Tôi sẽ gọi lần lượt vài người chia sẻ màn hình, và tôi chỉ soi đúng một chỗ: dòng description. Tôi hỏi anh chị một câu: nếu tuần sau anh chị viết thêm một skill soạn email chào sỉ cho spa, thì đọc dòng này Claude có phân biệt được hai cái không? Nếu không phân biệt được thì anh chị gõ ngay: viết lại dòng description cho tách bạch hẳn với skill soạn email chào sỉ B2B. Hết 13 phút mà chưa xong thì cứ dùng bản Claude vừa trả, không sửa gì, chuyển sang chặng 2. Thà chạy thử được một bản chưa hoàn hảo còn hơn ngồi mãi ở chặng 1."

**Hình minh họa gợi ý:** Số 13 cỡ rất lớn kèm đồng hồ đếm ngược.

**Thời điểm:** K3, phút 82 tới 95

---

### Slide 30: PROMPT 7. Chạy skill ra 3 bài bán hàng

**Loại:** prompt

**Nội dung hiển thị:**

```
Dùng skill viet-bai-ban-hang để viết 3 bài đăng, làm đúng từng
bước trong skill, không bỏ bước nào.

Bài 1:
- SKU: SKU-01 Serum rau má B5
- Kênh: Facebook, bài thường
- Người đọc: nữ 25 đến 40 tuổi, da sau mụn còn thâm, đã từng
  dùng sản phẩm mạnh và bị kích ứng
- Mục tiêu: người đọc nhắn tin hỏi thêm

Bài 2:
- SKU: SKU-02 Kem nghệ mật ong
- Kênh: Facebook, bài thường
- Người đọc: nữ 25 đến 40 tuổi, da khô, mùa hanh bị bong tróc
- Mục tiêu: người đọc lưu bài lại

Bài 3:
- SKU: SKU-03 Mặt nạ đất sét trà xanh
- Kênh: Shopee, phần mô tả sản phẩm
- Người đọc: nữ 25 đến 40 tuổi, da dầu, lỗ chân lông to vùng
  chữ T
- Mục tiêu: người đọc bấm mua

Chỉ dùng giá, thành phần và công dụng có trong file
san-pham-thao-an.md. Không thêm bất kỳ con số nào ngoài hồ sơ.
Thiếu thì ghi "chưa đủ dữ liệu". Mỗi bài kết thúc bằng phần
gắn nhãn [DATA THẬT] và [SUY LUẬN].
```

**Lời giảng viên nói khi chiếu slide này:** "Chặng 2, 10 phút. Ba bài cho ba SKU, ba mục tiêu khác nhau, để thấy skill nó bám theo đầu vào chứ không viết một kiểu. Giữa chặng này tôi sẽ bảo anh chị dừng tay 30 giây làm phép thử đổi tên: lấy câu mở bài của bài 1, thay chữ Thảo An bằng tên một hãng mỹ phẩm bất kỳ. Câu đó còn đúng không? Nếu vẫn đúng thì bài đó chưa dùng được, anh chị bảo Claude viết lại kèm chi tiết chỉ Thảo An mới có. Ai vẫn bị dính từ cấm thì đừng sửa tay bài viết. Sửa quy trình chứ không sửa kết quả: thêm danh sách từ cấm vào mục Ràng buộc của skill rồi chạy lại."

**Hình minh họa gợi ý:** Khối code chiếm trọn slide. Góc phải trên ghi số 10 kèm đồng hồ.

**Thời điểm:** K3, phút 95 tới 105

---

### Slide 31: PROMPT 8. 10 hook và 10 CTA

**Loại:** prompt

**Nội dung hiển thị:**

```
Vẫn dùng skill viet-bai-ban-hang và file CLAUDE.md của thư mục
này.

Viết cho tôi:
- 10 hook mở bài cho Thảo An. Mỗi hook 1 dòng, dưới 20 chữ, mở
  bằng một tình huống da cụ thể, không mở bằng lời chào. Ghi rõ
  mỗi hook dùng cho SKU nào.
- 10 câu kêu gọi hành động. Chia rõ: 4 câu cho mục tiêu nhắn
  tin, 3 câu cho mục tiêu bấm mua trên Shopee, 3 câu cho mục
  tiêu lưu bài.

Ràng buộc: không dùng từ trong danh sách cấm ở CLAUDE.md. Không
hứa thời gian. Sau khi viết xong, tự kiểm tra lại giúp tôi:
hook nào thay tên Thảo An bằng tên thương hiệu khác mà vẫn đúng
thì đánh dấu YẾU và viết lại câu đó.
```

**Lời giảng viên nói khi chiếu slide này:** "Chặng 3, 5 phút. Anh chị để ý câu cuối của prompt: tôi bảo chính nó tự chấm hook nào YẾU rồi viết lại. Đây là phép thử đổi tên tôi vừa dạy, nhưng cho nó tự chạy. Nếu kết quả trả về mà không có hook nào bị đánh dấu YẾU thì đáng ngờ, anh chị bảo nó soi lại nghiêm hơn."

**Hình minh họa gợi ý:** Khối code lớn. Góc phải trên ghi số 5 kèm đồng hồ.

**Thời điểm:** K3, phút 105 tới 110

---

### Slide 32: PROMPT 9. Bảo Claude soi lại chính skill của nó

**Loại:** prompt

**Nội dung hiển thị:**

```
Bạn vừa chạy skill viet-bai-ban-hang để viết 3 bài và bộ hook,
CTA cho Thảo An. Giờ đóng vai người kiểm tra quy trình và soi
lại chính file .claude/skills/viet-bai-ban-hang/SKILL.md đó.

Trả lời tôi đúng 4 mục, ngắn gọn:

1. Bước nào trong skill viết còn chung chung khiến bạn phải tự
   đoán? Nêu rõ bạn đã đoán gì.
2. Đầu vào nào lẽ ra phải liệt kê là bắt buộc nhưng skill đang
   bỏ sót?
3. Dòng description đã đủ rõ để phân biệt skill này với một
   skill soạn email chào sỉ B2B chưa? Nếu chưa thì viết lại
   giúp tôi.
4. Sửa lại file SKILL.md theo đúng những gì bạn vừa chỉ ra, giữ
   nguyên cấu trúc 6 mục. Ghi thêm một dòng cuối file:
   "Sửa lần 1, ngày [điền ngày hôm nay], lý do: ..." kèm lý do
   ngắn.
```

**Lời giảng viên nói khi chiếu slide này:** "Chặng 4, 5 phút. Đây là việc ít người nghĩ tới: bảo chính Claude soi lại cái quy trình mà nó vừa dùng. Nó biết chỗ nào nó phải tự đoán, vì chính nó đoán. Anh chị vừa đi trọn một vòng: viết quy trình, chạy thật, soi lại, sửa. Trong nghề marketing anh chị gọi vòng đó là gì? Đúng, là tối ưu. Skill cũng vậy. Chạy ba lần trong tuần là anh chị biết ngay chỗ nào phải sửa."

**Hình minh họa gợi ý:** Vòng tròn khép kín 4 mũi tên: viết, chạy, soi, sửa.

**Thời điểm:** K3, phút 110 tới 115

---

### Slide 33: MCP là thẻ ra vào có phân quyền

**Loại:** sơ đồ

**Nội dung hiển thị:**
- Không MCP: copy từ Sheet, dán vào Claude, dán ngược ra
- Có MCP: Claude tự đọc thẳng file trên Drive
- Một thẻ, nhưng chỉ quẹt được đúng tầng được phép
- Hôm nay chỉ ĐỌC, không ghi, không đăng

**Lời giảng viên nói khi chiếu slide này:** "Từ đầu buổi tới giờ, Claude vẫn là một người ngồi trong phòng kín. Nó rất giỏi, nó có brief, nó có quy trình, nó có trí nhớ. Nhưng muốn nó đọc cái gì thì anh chị vẫn phải bê tài liệu vào tận nơi. MCP viết tắt của Model Context Protocol, tạm hiểu là chuẩn cắm nối cho AI. Anh chị hình dung như cái thẻ ra vào của tòa nhà: một cái thẻ, nhưng quẹt được đúng những tầng công ty cho phép. Hôm nay ta dừng ở đọc, cho an toàn. Buổi 5 mới làm phần ghi và tự động hóa."

**Hình minh họa gợi ý:** Hai cột đối chiếu KHÔNG MCP và CÓ MCP. Cột trái vẽ mũi tên vòng vèo qua tay người, cột phải vẽ mũi tên thẳng.

**Thời điểm:** K4, phút 115 tới 120

---

### Slide 34: Skill khác MCP thế nào

**Loại:** bảng

**Nội dung hiển thị:**

| | Skill | MCP |
|---|---|---|
| Cho Claude cái gì | Cách LÀM một việc cho đúng chuẩn | TAY CHÂN để với tới dữ liệu thật |
| Thiếu nó thì sao | Với tới dữ liệu nhưng viết sai giọng | Vẫn phải copy dán bằng tay |

**Lời giảng viên nói khi chiếu slide này:** "Anh chị đừng nhầm skill với MCP, hai cái khác hẳn nhau. Tôi hỏi lớp một câu, anh chị gõ vào chat: nếu tôi chỉ có MCP mà không có skill, tôi bảo nó viết bài bán hàng, nó viết thế nào? Đáp án là viết chung chung, sai giọng, dính từ cấm, y như demo đầu buổi. Phải có cả hai."

**Hình minh họa gợi ý:** Hai biểu tượng cạnh nhau: quyển sổ quy trình và tấm thẻ từ. Dấu cộng ở giữa.

**Thời điểm:** K4, phút 120 tới 122

---

### Slide 35: Quy định cứng của lớp hôm nay

**Loại:** nội dung

**Nội dung hiển thị:**
- Chỉ nối tài khoản Google demo của lớp, hoặc tài khoản cá nhân
- TUYỆT ĐỐI không nối tài khoản công ty có dữ liệu khách hàng
- Màn hình cấp quyền của Google: đồng ý cả nhóm hoặc hủy, không tích từng quyền
- Đọc kỹ danh sách quyền trước khi bấm
- Claude ĐỌC và SOẠN NHÁP, người vẫn là người duyệt và bấm đăng

**Lời giảng viên nói khi chiếu slide này:** "Đây là quy định cứng của lớp hôm nay, tôi nói lần thứ nhất. Trong Drive công ty anh chị có danh sách khách, số điện thoại, lịch sử đơn hàng. Đó là dữ liệu cá nhân của người khác, không phải của anh chị, và hôm nay là buổi học chứ không phải triển khai chính thức. Về màn hình cấp quyền: nhiều người tưởng vào đó tích chọn được cái nào cho cái nào không. Không phải vậy. Thấy quyền nào không chấp nhận được thì bấm hủy, không cắm nối nữa. Ai ngại cấp quyền thì không cần bấm, xem chung màn hình tôi chia sẻ cũng được."

**Hình minh họa gợi ý:** Biểu tượng khóa lớn ở giữa. Ba dòng đầu có dấu chấm than trong tam giác.

**Thời điểm:** K4, phút 122

---

### Slide 36: Đường vào và đường ra

**Loại:** nội dung

**Nội dung hiển thị:**
- Vào: Settings, mục Connectors, chọn Google Drive, bấm kết nối
- Dừng ở màn hình cấp quyền, bỏ tay khỏi chuột, đọc hết rồi mới bấm
- Ra 1: trang quản lý tài khoản Google, Bảo mật, ứng dụng bên thứ ba, xóa quyền
- Ra 2: Settings của Claude, Connectors, bấm ngắt kết nối
- Làm cả hai chỗ

**Lời giảng viên nói khi chiếu slide này:** "Anh chị mở Settings của Claude Desktop ra, để nguyên đó. Sáu phút này tôi bấm tới đâu anh chị bấm tới đó. Có một chỗ tôi sẽ bảo anh chị DỪNG TAY và không bấm, đó là màn hình cấp quyền của Google. Chỗ đó chờ tôi nói xong đã, và chờ trợ giảng đi kiểm từng máy xem anh chị đang đăng nhập tài khoản nào. Cách gỡ quyền anh chị ghi vào vở luôn, tôi cũng đã gửi file hướng dẫn vào chat. Ai đã cấp quyền bằng tài khoản cá nhân mà không định dùng tiếp thì tối nay vào gỡ, đừng để đó."

**Hình minh họa gợi ý:** Sơ đồ hai chiều: mũi tên đi vào có biển báo dừng ở giữa, mũi tên đi ra tách làm hai nhánh.

**Thời điểm:** K4, phút 122 tới 133

---

### Slide 37: PROMPT 10. Đọc bảng đơn hàng thật

**Loại:** prompt

**Nội dung hiển thị:**

```
Trên Google Drive của tôi có thư mục LOP-AI-MARKETING. Trong đó
có file Google Sheet tên thao-an-don-hang-demo, gồm 5 cột đúng
tên như sau: Ngày, Kênh, Mã SKU, Số lượng, Thành tiền.
Cột Kênh chỉ có 2 giá trị: Facebook, Shopee.
Cột Mã SKU chỉ có 3 giá trị: SKU-01, SKU-02, SKU-03.

Hãy làm 3 việc:

1. Đọc toàn bộ file đó. Chỉ đọc, không sửa, không xóa gì cả.
2. Tổng hợp cho tôi thành 1 bảng gồm: tổng số đơn và tổng doanh
   thu; tách theo kênh; tách theo SKU. Chỉ ra SKU nào bán chạy
   nhất theo số đơn.
3. Đối chiếu với file CLAUDE.md trong thư mục làm việc của tôi
   và trả lời: SKU bán chạy nhất theo số liệu thật này có trùng
   với SKU tôi đang ghi là sản phẩm dẫn dắt trong brief không?

Quan trọng: nếu có chỉ số nào tôi hỏi mà bảng này không đủ dữ
liệu để tính thì ghi thẳng "chưa đủ dữ liệu, cần bổ sung [tên
dữ liệu còn thiếu]". Tuyệt đối không ước lượng, không dùng số
trung bình ngành. Cuối cùng liệt kê giúp tôi: để tính được chi
phí trên mỗi đơn thì tôi còn thiếu những cột dữ liệu nào.
```

Số để đối chiếu: 40 đơn, 10.840.000đ. Facebook 24, Shopee 16.

**Lời giảng viên nói khi chiếu slide này:** "Anh chị chạy 5 phút. Chạy xong ta cùng kiểm 2 dòng bất kỳ: mở lại Google Sheet, tìm đúng dòng đó, đọc to. Tôi cố ý làm bước kiểm tra này trước mặt anh chị. Nguyên tắc là: nó làm nhanh, nhưng người vẫn phải rà. Nó đọc 40 dòng trong 20 giây, anh chị bỏ 2 phút soi lại là quá lời. Anh chị để ý phần cuối kết quả: bảng này không có cột chi phí quảng cáo, nên nó KHÔNG tính được chi phí trên mỗi đơn, và nó ghi thẳng ra là chưa đủ dữ liệu. Đó là kết quả của cái brief anh chị viết ở khối trước. Chỗ nó ghi chưa đủ dữ liệu chính là danh sách việc anh chị phải đi lấy số tuần này."

**Hình minh họa gợi ý:** Khối code chiếm phần lớn slide. Dải số đối chiếu đặt trong khung viền đứt ở dưới cùng.

**Thời điểm:** K4, phút 135 tới 140

---

### Slide 38: Bảy thứ phải có trên máy anh chị lúc này

**Loại:** bảng

**Nội dung hiển thị:**

| # | Sản phẩm | Ở đâu |
|---|---|---|
| 1 | Thư mục làm việc mở được bằng tab Code | Màn hình nền, `thao-an-marketing` |
| 2 | File `CLAUDE.md` đủ 9 mục | Trong thư mục làm việc |
| 3 | Memory đã bật, đã kiểm ở phiên mới | Settings |
| 4 | Skill `viet-bai-ban-hang` chạy được | `.claude/skills/viet-bai-ban-hang/SKILL.md` |
| 5 | 3 bài bán hàng do skill sinh ra | Thư mục làm việc |
| 6 | 10 hook và 10 CTA | Thư mục làm việc |
| 7 | 1 kết nối MCP đọc được dữ liệu | Settings, mục Connectors |

**Lời giảng viên nói khi chiếu slide này:** "Anh chị tự đối chiếu máy mình theo bảng này. Ai thiếu mục nào thì gõ số mục đó vào chat ngay bây giờ, tôi ghi lại để hỗ trợ trước buổi sau. Tôi nhắc lại ba nguyên tắc chống bịa, vì đây là thứ anh chị mang theo suốt sáu buổi. Một: chỉ dùng dữ liệu anh chị cấp. Hai: gắn nhãn nguồn. Ba: người duyệt cuối. Anh chị nhớ lúc tôi hỏi nó ngân sách quảng cáo và số review không? Nó nói chưa đủ dữ liệu. Đó là dấu hiệu hệ thống của anh chị đang chạy đúng."

**Hình minh họa gợi ý:** 7 ô vuông trống để tích, xếp dọc, mỗi ô một dòng.

**Thời điểm:** K5, phút 140 tới 145

---

### Slide 39: Bài tập về nhà, ba việc

**Loại:** nội dung

**Nội dung hiển thị:**
1. Chạy skill `viet-bai-ban-hang` ít nhất 3 lần trong tuần, ghi lại chỗ phải sửa tay
2. Viết hồ sơ sản phẩm của thương hiệu mình theo cấu trúc `san-pham-thao-an.md`, rồi bảo Claude viết lại `CLAUDE.md`
3. Làm ngay tối nay: ai cấp quyền Google bằng tài khoản cá nhân mà không dùng tiếp thì vào gỡ quyền

**Lời giảng viên nói khi chiếu slide này:** "Việc một quan trọng nhất: cái ghi chép chỗ phải sửa tay chính là danh sách sửa cho lần sau, buổi sau tôi hỏi. Việc ba làm ngay tối nay, đừng để đó. Nói thêm về giới hạn của những thứ hôm nay, để anh chị không kỳ vọng sai: mọi thứ vẫn phải có người bấm chạy từng bước. Anh chị bấm cho nó viết bài, rồi bấm cho nó ra hook, rồi bấm cho nó đọc Drive. Ba lần bấm cho một chuỗi việc. Chuyện nối các bước lại thành luồng tự chạy là buổi 5. Chuyện đóng gói skill bàn giao cho người khác là buổi 6."

**Hình minh họa gợi ý:** 3 ô đánh số, ô số 3 có nhãn nhỏ "làm ngay tối nay".

**Thời điểm:** K5, phút 145 tới 148

---

### Slide 40: Buổi sau chúng ta xây Customer Insight Agent

**Loại:** chuyển khối

**Nội dung hiển thị:**
- Hôm nay mục "5 nỗi đau khách" đang gắn nhãn `[SUY LUẬN]`
- Buổi sau thay chỗ đoán đó bằng lời khách nói thật
- Mang theo: `CLAUDE.md` và skill `viet-bai-ban-hang`
- Ai chưa có 2 thứ đó thì buổi sau ngồi làm lại từ đầu

**Lời giảng viên nói khi chiếu slide này:** "Anh chị nhớ mục năm nỗi đau khách trong file CLAUDE.md hôm nay không? Nó đang gắn nhãn suy luận, tức là chúng ta đang đoán. Đây là chủ ý thiết kế, không phải thiếu sót. Buổi sau ta thay chỗ đoán đó bằng lời khách nói thật, rút từ review và tin nhắn. Đầu vào của buổi sau chính là file CLAUDE.md và cái skill anh chị vừa làm. Ai chưa hoàn thành hai thứ này thì làm bù trước buổi 2, có bản ghi buổi để xem lại. Cảm ơn anh chị, hẹn gặp buổi sau."

**Hình minh họa gợi ý:** Mũi tên lớn từ ô ghi `[SUY LUẬN]` sang ô ghi `[DATA THẬT]`.

**Thời điểm:** K5, phút 148 tới 150
