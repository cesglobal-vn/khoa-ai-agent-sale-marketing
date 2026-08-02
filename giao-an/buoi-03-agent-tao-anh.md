# BÀI SOẠN GIÁO VIÊN - BUỔI 3

## Agent tạo ảnh: từ caption ra hình đăng được

> Bản script giảng được ngay. Đọc theo, không cần soạn thêm.
> Lớp: 10 đến 20 người làm sale và marketing. Chủ doanh nghiệp nhỏ, trưởng phòng marketing, nhân sự content, nhân sự ads. Phần lớn KHÔNG biết code, chưa quen dòng lệnh. Đây là ràng buộc thiết kế quan trọng nhất của buổi. Mỗi thao tác phải ghi rõ bấm gì, gõ gì, thấy gì thì biết đúng.
> Học online live qua Zoom hoặc Google Meet. Giảng viên chia sẻ màn hình, học viên làm trên máy mình và chia sẻ màn hình lại khi cần hỗ trợ.
> Công cụ học viên dùng: **Claude Desktop, tab Code**. Cả buổi làm ở tab Code.
> Case study xuyên suốt: **Thảo An**, thương hiệu mỹ phẩm thảo mộc giả định, 3 SKU, bán B2C qua Facebook và Shopee, bán sỉ B2B cho spa.
> Thời lượng: 150 phút, đã gồm 10 phút giải lao.
> Nguyên tắc thiết kế xuyên suốt: **đau trước, giải pháp sau.** Mỗi khối mở bằng một nỗi đau anh chị tự cảm, rồi công cụ mới hiện ra như lời giải. Mỗi phần có Lý thuyết ngắn rồi Thao tác có prompt.
> Nối tiếp buổi 2: buổi 2 anh chị đã hiểu MCP là gì và đã tự lập được agent trong `.claude/agents/`. Buổi 3 dùng lại đúng hai thứ đó vào việc thật và sướng tay nhất: làm ra hình để đăng. KHÔNG giảng lại hai khái niệm đó từ đầu, chỉ nhắc một câu.

---

## LƯU Ý LỚN NHẤT CHO GIẢNG VIÊN, ĐỌC TRƯỚC KHI DẠY

Buổi này có một chỗ khó thật, khó hơn mọi thứ ở buổi 1 và buổi 2: **nối công cụ vẽ ảnh vào Claude cần cài đặt và đăng nhập một lần bằng dòng lệnh.** Với lớp không biết code, phần lớn sẽ KHÔNG tự nối được tại chỗ trong 30 phút.

Cách xử lý đã chốt cho buổi này:

1. **Giảng viên nối sẵn trên máy mình trước buổi.** Trong buổi, giảng viên demo lại các bước để lớp hiểu, lớp chủ yếu XEM.
2. **Gửi file hướng dẫn cài trước buổi 2 ngày.** Ai cài xong trước thì trong buổi làm theo cùng giảng viên. Ai chưa, xem demo rồi làm bù ở nhà theo file hướng dẫn.
3. **Nói thẳng câu này với lớp ở đầu K1:** "Ai chưa nối được ngay bây giờ thì không sao. Anh chị xem tôi làm cho hiểu, rồi làm bù ở nhà theo file hướng dẫn. Từ K2 trở đi, ai chưa có công cụ vẫn theo được bằng cách xem tôi tạo ảnh trên màn hình."

Đừng để cả lớp kẹt 30 phút ở khâu cài. Mục tiêu K1 là HIỂU đường nối và thấy một ảnh ra thật, không phải cả lớp cùng cài xong.

---

## BẢNG MỐC ĐỒNG HỒ CẢ BUỔI

Giả định giờ bắt đầu 08h00. Bắt đầu giờ khác thì cộng dồn tương ứng.

| Khối | Đồng hồ | Phút | Nội dung | Ai làm |
|---|---|---|---|---|
| K0 | 08:00 - 08:10 | 10 | Mở đầu: bài hay mà thiếu ảnh | Giảng 6 + học viên 4 |
| K1 | 08:10 - 08:40 | 30 | Nối công cụ vẽ ảnh vào Claude, tạo ảnh đầu tiên | Demo 20 + thực hành hoặc xem 10 |
| K2 | 08:40 - 09:05 | 25 | Viết mô tả để ra ảnh đúng ý | Giảng và demo 10 + thực hành 15 |
| Giải lao | 09:05 - 09:15 | 10 | Nghỉ | |
| K3 | 09:15 - 09:55 | 40 | Lập trợ lý chuyên tạo ảnh (đỉnh buổi) | Giảng và demo 13 + thực hành 27 |
| K4 | 09:55 - 10:20 | 25 | Gắn logo, người duyệt, chi phí | Giảng và demo 13 + thực hành 12 |
| K5 | 10:20 - 10:30 | 10 | Chốt và giao bài | Giảng 10 |

**Cộng lại để tự kiểm:** 10 + 30 + 25 + 10 + 40 + 25 + 10 = **150 phút**, khớp thời lượng khai báo.

**Tay học viên đặt trên bàn phím:** K0 4 phút, K1 tùy máy (ai nối được thì 10, chưa thì xem), K2 15 phút, K3 27 phút, K4 12 phút. Đỉnh thực hành là K3 (lập agent tạo ảnh), giống K3 buổi 2 (lập skill). Đừng ép K1 thành thực hành cả lớp, vì khâu cài dễ kẹt.

**Mốc phải bám cứng:** 08:40 xong K1 dù ai cài được hay không. 09:55 xong K3. **Không cắt K3.** K3 là sản phẩm chính học viên mang về.

**Lưu ý về giao diện và lệnh:** app Claude Desktop, đường vào cấu hình MCP, và các lệnh cài đặt có thể đổi theo phiên bản. Mọi chỗ bài này mô tả đường bấm hay lệnh gõ, trước buổi phải mở máy kiểm tra lại và ghi ra giấy nhắc. Các điểm cần kiểm được đánh dấu rõ trong từng khối.

---

## K0. MỞ ĐẦU: BÀI HAY MÀ THIẾU ẢNH (10 phút, 08:00 - 08:10)

### LỜI GIẢNG (6 phút)

"Chào anh chị. Hai buổi vừa rồi anh chị đã dạy được Claude viết bài đúng giọng thương hiệu, và đóng gói được việc lặp lại thành nút bấm. Giờ tôi hỏi một câu, anh chị giơ tay thật lòng giúp tôi: ai từng viết xong một bài bán hàng ưng ý, tới lúc cần một tấm ảnh để đăng thì tắc?"

*(Dừng 10 giây. Phần lớn giơ tay. Để nguyên đó, chưa vội giải thích.)*

"Đúng rồi. Bài hay mà thiếu ảnh thì không đăng được. Mà kiếm ảnh thì ba đường, đường nào cũng khổ. Một, chờ bạn thiết kế, hôm nay bận thì mai mới có. Hai, thuê ngoài, vừa lâu vừa tốn. Ba, lấy ảnh trên mạng, thì đụng hàng, và không đúng sản phẩm của mình. Ảnh serum của hãng khác dán vào bài Thảo An, khách tinh mắt là biết ngay."

"Hôm nay ta gỡ đúng nỗi đau đó. Cuối buổi, Claude tự vẽ ảnh cho anh chị. Anh chị đưa nội dung bài, nó ra hình, gắn được logo, đăng được ngay. Và hay nhất là ta lập một trợ lý chuyên làm ảnh, giống buổi 2 anh chị đã lập trợ lý viết bài, chỉ khác là trợ lý này ra hình."

"Cách chạy buổi online vẫn như cũ: tôi chia sẻ màn hình, anh chị vừa nghe vừa làm. Riêng phần đầu, phần nối công cụ, hơi khó, tôi sẽ nói rõ ai làm được thì làm cùng, ai chưa thì xem tôi làm rồi làm bù ở nhà. Đừng lo, không ai bị bỏ lại."

### THAO TÁC HỌC VIÊN (4 phút)

Nói trước: "Bốn phút này chỉ mở lại chỗ làm việc, chưa làm gì nặng."

**Bước 1. Mở lại thư mục làm việc.**

1. Mở Claude Desktop.
2. Bấm tab **Code** ở hàng trên cùng.
3. Mở thư mục làm việc của anh chị (thư mục `thao-an-marketing` hoặc thư mục thương hiệu thật, đã dựng ở buổi 2).

**Bước 2. Gõ một câu kiểm tra nhanh.**

**PROMPT B3-0:**

```
Bạn đang mở thư mục nào, và trong thư mục này đã có file CLAUDE.md chưa?
Trả lời ngắn gọn.
```

**Tiêu chí coi là xong:** mỗi máy mở đúng thư mục, Claude xác nhận có `CLAUDE.md`. File này quan trọng cho cả buổi, vì lát nữa trợ lý tạo ảnh sẽ đọc nó để lấy màu và phong cách thương hiệu.

### DỰ PHÒNG

- **Máy chưa có `CLAUDE.md`:** phát bộ Thảo An mẫu (thư mục `thao-an-marketing` có sẵn `san-pham-thao-an.md` và `CLAUDE.md`), tải về mở bằng tab Code. Vẫn theo được cả buổi.
- **App cũ không thấy tab Code:** tải bản mới ở claude.ai/download. Trong lúc chờ, ghép xem chung màn hình một bạn qua Zoom, không cài giữa giờ.

---

## K1. NỐI CÔNG CỤ VẼ ẢNH VÀO CLAUDE, TẠO ẢNH ĐẦU TIÊN (30 phút, 08:10 - 08:40)

**Câu hỏi dẫn:** Claude viết chữ giỏi rồi, nhưng làm sao nó vẽ được ảnh, thứ nó không tự làm được?

**Mục tiêu khối:** lớp HIỂU đường nối công cụ vẽ ảnh vào Claude, thấy một ảnh ra thật trên màn hình. Ai cài được thì có công cụ trong tay; ai chưa, biết đường làm bù ở nhà.

### PHẦN 1: LÝ THUYẾT (3 phút)

"Buổi 2 anh chị đã biết MCP là cái thẻ cho Claude với tới công cụ bên ngoài. Nhắc đúng một câu thôi, không giảng lại. Hôm nay ta cắm một công cụ cụ thể vào cái thẻ đó: **công cụ vẽ ảnh của ChatGPT.** Cắm xong, anh chị bảo Claude 'vẽ giúp tôi tấm ảnh này', nó vẽ thật, trả về một file ảnh trên máy."

"Tôi nói thẳng ngay, để anh chị không sốt ruột: **nối công cụ này là phần khó nhất buổi.** Nó cần cài một ít và đăng nhập tài khoản ChatGPT một lần. Tôi đã nối sẵn trên máy tôi. Bây giờ tôi làm lại từng bước cho anh chị thấy đường đi. Ai đã cài trước theo file tôi gửi thì làm cùng. Ai chưa, cứ xem, ghi lại các bước, làm bù ở nhà. Từ khối sau, ai chưa có công cụ vẫn theo được bằng cách xem tôi tạo ảnh."

**Cảnh báo phải nói thật với lớp, đọc nguyên văn:** "Một điều tôi phải nói thẳng cho anh chị yên tâm dùng đúng cách. Công cụ này nối vào cổng web của ChatGPT, KHÔNG phải cổng chính thức của hãng. Nghĩa là dùng nhiều, dồn dập, có thể bị giới hạn tốc độ hoặc khóa tài khoản. Cho nên: dùng một tài khoản ChatGPT phụ để thử, đừng dùng tài khoản chính quan trọng của anh chị. Đây là công cụ để học và thử nghiệm, không phải để cắm chạy sản xuất hàng nghìn ảnh."

**Nói rõ công cụ này làm gì, không làm gì, để lớp không kỳ vọng sai. Chiếu bảng:**

| Công cụ ai-image-gpt | Có làm | Không làm |
|---|---|---|
| Vẽ ảnh từ mô tả | Có | |
| Kiểm tra đăng nhập và lượt còn lại | Có | |
| Ghép logo vào ảnh | | Không, phần này làm tay bằng Canva ở K4 |
| Viết chữ tiếng Việt chuẩn lên ảnh | | Không đáng tin, hay sai dấu, xem K2 |
| Tự đăng ảnh lên trang | | Không, người duyệt rồi tự đăng |

"Anh chị ghi nhớ đúng hai việc nó làm: vẽ ảnh, và kiểm đăng nhập. Ba việc còn lại trong bảng, hoặc mình làm tay, hoặc mình không giao cho nó. Biết trước giới hạn này để không thất vọng giữa buổi."

### PHẦN 2: THAO TÁC DEMO NỐI CÔNG CỤ (giảng viên demo, 15 phút)

**Giảng viên làm trên màn hình, đọc to từng bước. Học viên nào đã cài trước thì làm cùng, còn lại xem và ghi.**

*Lưu ý cho giảng viên: cả sáu bước dưới đây phải chạy trọn một lần trên máy trước buổi và ghi lại kết quả thật. Đường vào cấu hình MCP của Claude Desktop có thể đổi theo phiên bản, kiểm trước.*

**Bước cài, làm một lần cho máy chưa có Python:** máy cần **Python 3.12 trở lên** và **uv** (công cụ chạy Python). Nếu máy chưa có, cài trước theo file hướng dẫn. Giảng viên nói: "Cái này như cài sẵn bếp trước khi nấu. Máy tôi có rồi nên tôi đi tiếp."

**B3-1. Tải mã nguồn công cụ về máy.** Buổi 1 anh chị đã có Git. Mở cửa sổ dòng lệnh, hoặc nhờ chính Claude trong tab Code chạy giúp bằng cách gõ: "Chạy giúp tôi lệnh sau trong thư mục Tài liệu của tôi." rồi dán lệnh:

```
git clone https://github.com/andyluu98/ai-image-gpt-mcp.git
```

**Anh chị sẽ thấy:** một thư mục mới tên `ai-image-gpt-mcp` xuất hiện. Đó là bộ công cụ vừa tải về.

**B3-2. Cài các thứ công cụ cần.** Vào trong thư mục vừa tải, chạy:

```
uv sync
```

**Anh chị sẽ thấy:** một loạt dòng chữ chạy qua, báo cài xong. Lần đầu hơi lâu, đừng tắt giữa chừng.

**B3-3. Đăng ký công cụ vào Claude Desktop.** Đây là bước cắm thẻ MCP. Mở phần cấu hình MCP của Claude Desktop, thêm đoạn sau. Chỗ `<đường dẫn tuyệt đối>` thay bằng đường dẫn thật tới thư mục vừa tải ở B3-1:

```
{
  "mcpServers": {
    "ai-image-gpt": {
      "command": "uv",
      "args": ["run", "--directory", "<đường dẫn tuyệt đối tới thư mục ai-image-gpt-mcp>", "aigpt-mcp"]
    }
  }
}
```

**Anh chị sẽ thấy:** sau khi lưu và mở lại Claude Desktop, trong danh sách công cụ MCP có tên `ai-image-gpt`. Đó là dấu hiệu đã cắm thẻ xong.

*Lưu ý cho giảng viên: chỗ dán JSON này khác nhau theo phiên bản, có thể ở phần Settings phần Developer, hoặc ở một file cấu hình. Kiểm trên máy trước buổi, ghi rõ đường vào ra giấy nhắc, đừng mô tả theo trí nhớ trước lớp.*

**B3-4. Đăng nhập ChatGPT, bước một.** Chạy:

```
uv run aigpt login
```

**Anh chị sẽ thấy:** trình duyệt tự mở ra trang đăng nhập ChatGPT. Anh chị đăng nhập bằng tài khoản phụ. Đăng nhập xong, trình duyệt chuyển tới một trang của platform.openai.com.

**B3-5. Đăng nhập ChatGPT, bước hai. Đây là bước nhiều người quên nhất.** Ở trang platform.openai.com vừa mở, copy TOÀN BỘ đường dẫn trên thanh địa chỉ trình duyệt. Rồi chạy lệnh sau, dán đường dẫn đó vào giữa hai dấu ngoặc kép:

```
uv run aigpt login --callback "<dán toàn bộ đường dẫn vừa copy vào đây>"
```

**Anh chị sẽ thấy:** báo đăng nhập thành công. Giảng viên nhấn mạnh: "Đăng nhập công cụ này có ĐÚNG HAI bước. Chạy login xong chưa xong đâu, phải quay lại dán đường dẫn thì mới thật sự vào. Rất nhiều người dừng ở bước một rồi tưởng hỏng."

**B3-6. Kiểm tra đã vào chưa và còn lượt không.** Chạy:

```
uv run aigpt accounts
```

**Anh chị sẽ thấy:** một dòng cho biết tài khoản đã đăng nhập và còn bao nhiêu lượt tạo ảnh. Ghi nhớ chỗ này, vì cuối buổi ta quay lại xem chi phí.

### PHẦN 3: TẠO ẢNH ĐẦU TIÊN (demo, và ai nối xong thì làm theo, 12 phút)

"Nối xong rồi. Giờ là phần vui: bảo Claude vẽ. Tôi làm một ảnh đơn giản trước, cho anh chị thấy nó chạy thật."

**THAO TÁC DEMO:**

1. Trong Claude Desktop, tab Code, mở thư mục làm việc.
2. Dán **PROMPT B3-7**, bấm Enter.

**PROMPT B3-7:**

```
Dùng công cụ vẽ ảnh ai-image-gpt tạo giúp tôi một ảnh nền đơn giản cho bài
đăng: một chai serum mỹ phẩm đặt trên bàn gỗ sáng, cạnh vài lá rau má xanh,
ánh sáng tự nhiên dịu, phong cách sạch sẽ tối giản. Tỉ lệ vuông.

Lưu ảnh vào thư mục 05-tai-lieu. Tạo đúng một ảnh thôi.
```

3. **Chờ. Nói cho lớp biết trước:** "Vẽ một ảnh mất khoảng một tới bốn phút, có khi lâu hơn. Trong lúc chờ, màn hình như đứng im, anh chị ĐỪNG bấm lại, đừng tưởng treo. Bấm lại là nó vẽ thêm cái nữa, tốn thêm lượt."
4. Khi ảnh ra, mở file trong `05-tai-lieu` cho lớp xem. Nói: "Đây, một tấm ảnh thật, do Claude vẽ, nằm trong thư mục của tôi. Chưa cần đẹp hoàn hảo, mục tiêu bây giờ là thấy nó CHẠY."

**Học viên nào đã nối xong:** dán y hệt PROMPT B3-7, đổi thư mục lưu nếu cần. Ai chưa nối, xem giảng viên, ghi lại prompt để làm ở nhà.

**Tiêu chí coi là xong K1:** lớp hiểu sáu bước nối; thấy ít nhất một ảnh ra thật trên màn hình giảng viên; ai nối được thì có một ảnh trong thư mục của mình.

### DỰ PHÒNG (K1 là khối nhiều bẫy nhất, đọc kỹ)

- **Chạy login xong mà `accounts` vẫn báo chưa đăng nhập:** gần như chắc là quên bước hai (B3-5). Bảo làm lại từ B3-4, lần này nhớ copy đường dẫn ở platform.openai.com rồi dán vào lệnh `--callback`.
- **Đã làm đủ hai bước mà vẫn báo chưa đăng nhập:** file lưu đăng nhập đôi khi bị lưu sai. Cách chữa đơn giản: đăng nhập lại một lần nữa từ B3-4. Thường lần hai là được.
- **Tạo ảnh báo lỗi 503 hoặc "server busy":** cổng web của ChatGPT đang bận, hay gặp khi tạo nhiều ảnh liên tiếp. Chờ một chút rồi thử lại, và giãn cách giữa các lần tạo, đừng bấm dồn.
- **Ảnh vẽ mãi không ra, quá bốn năm phút:** không tắt, không bấm lại ngay. Chờ thêm chút. Nếu vẫn không ra thì thử lại một lần. Mạng chậm hoặc cổng bận là nguyên nhân thường gặp.
- **Cả lớp không ai nối được tại chỗ:** hoàn toàn bình thường, đã lường trước. Giảng viên tạo ảnh trên máy mình cho cả lớp xem suốt K2 và K3. Học viên làm bù ở nhà theo file hướng dẫn. Không dừng buổi để đi cài từng máy.
- **Có người hỏi vì sao phức tạp vậy:** trả lời thật: "Vì đây là công cụ nối qua cổng web, không phải nút bấm sẵn. Bù lại nó vẽ ảnh miễn phí qua tài khoản ChatGPT của anh chị. Cài một lần, dùng mãi. Lần sau mở máy là có luôn, không phải cài lại."

---

## K2. VIẾT MÔ TẢ ĐỂ RA ẢNH ĐÚNG Ý (25 phút, 08:40 - 09:05)

**Câu hỏi dẫn:** Cùng một công cụ, vì sao ảnh người này ra đẹp đúng ý, người kia ra lệch lung tung?

**Mục tiêu khối:** mỗi học viên biết tả một ảnh đủ năm yếu tố, và tạo được một ảnh cho sản phẩm thật của mình (hoặc Thảo An), chọn đúng tỉ lệ kênh.

### PHẦN 1: LÝ THUYẾT, NĂM YẾU TỐ (5 phút)

"Ảnh đẹp hay lệch, đúng hay trật, phần lớn do CÁCH anh chị tả. Nói 'vẽ cái chai' thì nó vẽ đại một cái chai không giống sản phẩm mình. Một mô tả tốt cần đủ năm thứ. Anh chị ghi vào vở, đây là công thức tả ảnh:"

*(Chiếu bảng, đọc từng dòng.)*

| Yếu tố | Trả lời câu hỏi | Ví dụ cho Thảo An |
|---|---|---|
| 1. Chủ thể | Cái gì trong ảnh | chai serum thủy tinh trong, nhãn tối giản |
| 2. Bối cảnh | Đặt ở đâu | trên bàn đá sáng màu, cạnh lá rau má tươi |
| 3. Phong cách | Nhìn kiểu gì | sạch sẽ, cao cấp, tối giản, kiểu ảnh mỹ phẩm |
| 4. Tỉ lệ khung | Khung hình nào | vuông cho Facebook, dọc cho story |
| 5. Tông màu | Gam màu chủ đạo | xanh lá nhạt và trắng kem, dịu, tự nhiên |

"Đủ năm thứ này, ảnh ra sát ý hơn hẳn. Thiếu thì nó tự đoán, mà đoán thì trật."

"Trong năm yếu tố, tỉ lệ khung là chỗ nhiều người bỏ quên nhất, mà bỏ quên là ảnh sai kênh ngay. Anh chị ghi bảng này vào vở, chọn tỉ lệ theo chỗ định đăng:"

*(Chiếu bảng, đọc từng dòng.)*

| Kênh định đăng | Tỉ lệ | Cách nói trong prompt |
|---|---|---|
| Bài trên trang Facebook | Vuông 1:1 | "tỉ lệ vuông, cho bài Facebook" |
| Story và reels | Dọc 9:16 | "tỉ lệ dọc 9:16, cho story và reels" |
| Ảnh bìa, ảnh ngang | Ngang 16:9 | "tỉ lệ ngang 16:9, cho ảnh bìa" |

"Đăng nhầm ảnh dọc vào ô vuông thì bị cắt mất đầu mất chân sản phẩm. Cho nên nói rõ kênh ngay từ đầu."

"Ngoài chữ tiếng Việt, ảnh AI còn hay mắc ba lỗi khác, anh chị để ý khi duyệt: một, vẽ tay người thừa ngón hoặc thiếu ngón; hai, vẽ sản phẩm thêm chi tiết lạ, ví dụ chai hai nắp; ba, ghép cảnh vô lý, ví dụ bóng đổ sai hướng. Ba lỗi này không sửa bằng tả kỹ hơn được hết, nên nguyên tắc là tạo vài ảnh rồi CHỌN cái đạt, không cố ép một ảnh duy nhất phải hoàn hảo."

**Cảnh báo riêng của buổi, ghi vào vở, đọc nguyên văn:** "Đây là điều quan trọng nhất buổi hôm nay, quan trọng hơn cả cách tả. **Ảnh do AI vẽ hay viết SAI chữ tiếng Việt, nhất là chữ có dấu.** Nó viết 'Thảo An' thành 'Thao Ann', viết 'dưỡng ẩm' thành một chuỗi chữ lạ. Cho nên nguyên tắc là: **dùng ảnh cho phần HÌNH, còn chữ quan trọng như tên sản phẩm, giá, thì thêm sau bằng Canva.** Đừng để AI viết chữ tiếng Việt lên ảnh rồi đăng thẳng. Nếu bắt buộc phải có chữ trên ảnh, có một cách giảm sai, tôi chỉ ở phần thao tác."

### PHẦN 2: THAO TÁC DEMO, TẢ SƠ SÀI SO VỚI TẢ KỸ (giảng viên, 5 phút)

"Tôi cho anh chị thấy khác biệt. Cùng một sản phẩm, tôi tả hai kiểu."

**Cách tả sơ sài, PROMPT B3-8:**

```
Dùng ai-image-gpt vẽ giúp tôi ảnh một chai serum. Tỉ lệ vuông.
```

Nói: "Xem nó ra cái gì. Một chai serum chung chung, không giống Thảo An, nền tùy hứng." *(Chờ ảnh, cho lớp xem.)*

**Cách tả kỹ đủ năm yếu tố, PROMPT B3-9:**

```
Dùng ai-image-gpt vẽ giúp tôi một ảnh sản phẩm cho Thảo An.

- Chủ thể: một chai serum thủy tinh trong suốt, dáng cao thanh, nhãn giấy tối
  giản, không chữ.
- Bối cảnh: đặt trên mặt đá sáng màu, cạnh vài lá rau má xanh tươi và giọt nước.
- Phong cách: ảnh sản phẩm mỹ phẩm cao cấp, sạch sẽ, tối giản, ánh sáng tự nhiên.
- Tỉ lệ khung: vuông, cho bài đăng Facebook.
- Tông màu: xanh lá nhạt và trắng kem, dịu mắt, cảm giác thiên nhiên lành tính.

KHÔNG viết chữ tiếng Việt nào lên ảnh. Chừa một khoảng trống ở góc dưới bên
phải để lát nữa tôi ghép logo. Lưu vào 05-tai-lieu.
```

Đặt hai ảnh cạnh nhau. Nói câu chốt: "Cùng một công cụ, cùng một sản phẩm. Khác nhau ở chỗ tả. Ảnh dưới sát ý hơn nhiều, đúng tông thương hiệu, lại chừa sẵn góc cho logo. Anh chị để ý hai câu cuối: tôi cấm nó viết chữ tiếng Việt, và tôi bảo chừa góc trống. Hai câu đó lát nữa cứu anh chị."

*Nếu cần chữ trên ảnh thật:* "Ai bắt buộc phải có chữ trên ảnh, ví dụ chữ tiếng Việt ngắn, thì dùng bản dòng lệnh với tùy chọn `--thinking` mức cao, nó cố render chữ có dấu đúng hơn nhưng chậm hơn. Ví dụ: `uv run aigpt gen \"...\" --out ten-file.png --thinking extended`. Dù vậy tôi vẫn khuyên thêm chữ bằng Canva cho chắc."

### PHẦN 3: HOẠT ĐỘNG HỌC VIÊN (15 phút)

**Đề bài đọc cho lớp:** "Tới lượt anh chị. Ai nối được công cụ thì tạo một ảnh cho sản phẩm THẬT của mình, tả đủ năm yếu tố như tôi vừa làm. Ai chưa nối được thì soạn sẵn phần mô tả năm yếu tố cho sản phẩm mình vào một file, để về nhà tạo. Soạn mô tả cũng là kỹ năng chính, không phí đâu."

**Cách làm:** học viên lấy PROMPT B3-9 làm khung, thay năm yếu tố cho sản phẩm của mình. Nhắc giữ nguyên hai câu cuối: cấm chữ tiếng Việt, và chừa góc trống cho logo.

**Cách giảng viên đi hỗ trợ (qua Zoom):** mời vài người đọc phần mô tả của họ. Soi đúng ba thứ: (a) có đủ năm yếu tố không, hay thiếu tông màu, thiếu tỉ lệ; (b) tỉ lệ có đúng kênh họ định đăng không, vuông cho Facebook, dọc cho story và reels; (c) có câu cấm chữ tiếng Việt và chừa góc logo không.

**Tiêu chí coi là xong:** ai nối được thì có một ảnh sản phẩm của mình trong thư mục, đúng tỉ lệ kênh; ai chưa nối thì có một mô tả năm yếu tố viết xong, sẵn để về nhà tạo.

### DỰ PHÒNG

- **Ảnh ra sai sản phẩm, ví dụ vẽ hộp thay vì chai:** tả rõ hơn phần chủ thể, thêm chi tiết dáng, chất liệu. Đừng vẽ lại chục lần, mỗi lần tốn một lượt. Sửa mô tả rồi mới vẽ lại.
- **Ảnh vẫn cố viết chữ lên:** thêm vào cuối prompt câu `Tuyệt đối không có bất kỳ chữ hay chữ số nào trong ảnh.` Nếu vẫn còn, chấp nhận, vì chữ sẽ được ghép bằng Canva sau, chỗ chữ nó tự thêm sẽ bị logo và chữ Canva đè lên.
- **Học viên muốn tỉ lệ dọc cho story:** đổi câu tỉ lệ thành "tỉ lệ dọc 9:16, cho story và reels". Các tỉ lệ hay dùng: vuông 1:1 cho bài Facebook, dọc 9:16 cho story và reels, ngang 16:9 cho ảnh bìa.
- **Mạng chậm, ảnh ra lâu:** giảng viên tạo sẵn vài ảnh mẫu trước buổi, chiếu lên để lớp thấy kết quả và tập trung vào kỹ năng tả, không ngồi chờ máy quay.

---

## GIẢI LAO (10 phút, 09:05 - 09:15)

**Việc giảng viên làm trong lúc lớp nghỉ:**

- Rà nhanh: máy nào nối được công cụ, máy nào chưa, ghi lại. Người chưa nối vào K3 sẽ theo bằng cách xem, cần bố trí ghép nhóm.
- Kiểm máy giảng viên: công cụ vẽ ảnh còn chạy không, còn lượt không, chạy thử một prompt tạo ảnh cho chắc.
- Chiếu sẵn lên màn hình: khung frontmatter 3 dòng của file agent (name, description, tools), để nguyên đó suốt K3.

---

## K3. LẬP MỘT TRỢ LÝ CHUYÊN TẠO ẢNH (40 phút, 09:15 - 09:55, đỉnh của buổi)

**Câu hỏi dẫn:** Tả tay từng ảnh một thì lâu. Có cách nào chỉ đưa nội dung bài, ảnh tự ra không?

**Mục tiêu khối:** mỗi học viên lập được một agent chuyên tạo ảnh, đặt đúng chỗ trong thư mục làm việc, chạy thử ra ảnh từ một caption.

**Cộng thời lượng khối:** giảng và demo 13 + thực hành 27 = **40 phút**. Đây là phần quan trọng nhất buổi và là thứ anh chị mang về dùng được. Được nhiều giờ nhất vì người lập agent lần đầu sẽ cần sửa.

### PHẦN 1: NỖI ĐAU VÀ NỐI VỀ BUỔI 2 (5 phút)

"Nãy giờ mỗi ảnh anh chị phải ngồi tả đủ năm yếu tố. Làm một hai ảnh thì được, nhưng tuần nào cũng chục bài, mỗi bài một ảnh, tả tay mệt và không đều tay. Bài này đặt tông xanh, bài kia quên mất, ra ảnh lệch nhau."

*(Dừng cho vài người gật.)*

"Buổi 2 anh chị đã lập được một trợ lý, nhớ không? Trợ lý viết bài, trợ lý nghiên cứu đối thủ, đặt trong `.claude/agents/`. Hôm nay ta làm y hệt cách đó, chỉ khác nghề: một **trợ lý chuyên tạo ảnh.** Tôi không giảng lại cách lập agent từ đầu, vì buổi 2 anh chị làm rồi. Ta dùng lại đúng kỹ năng đó."

"Trợ lý này khác gì việc anh chị vừa làm ở K2? Ở K2 anh chị tả tay từng ảnh. Trợ lý này thì anh chị chỉ đưa NỘI DUNG BÀI ĐĂNG, nó tự nghĩ ra mô tả ảnh hợp bài, tự chọn tỉ lệ theo kênh, tự chừa góc cho logo, rồi gọi công cụ vẽ. Giống như có một bạn thiết kế đã thuộc gu thương hiệu, anh chị chỉ đưa brief là ra hình. Và vì nó đọc `CLAUDE.md`, nó biết màu và phong cách của anh chị, nên ảnh ra hợp brand hơn."

*(Chiếu bảng so sánh, đọc to.)*

| | K2: tả tay | K3: trợ lý tạo ảnh |
|---|---|---|
| Anh chị đưa gì | Mô tả đủ năm yếu tố | Chỉ nội dung bài đăng |
| Ai nghĩ ra năm yếu tố | Anh chị | Trợ lý tự suy từ bài và CLAUDE.md |
| Ai chọn tỉ lệ | Anh chị | Trợ lý theo kênh anh chị nói |
| Ai nhớ chừa góc logo | Anh chị phải nhớ dặn | Trợ lý luôn tự làm |
| Hợp cho | Một hai ảnh lẻ | Làm ảnh đều tay cả tuần |

"Anh chị thấy cột phải gọn hơn nhiều. Đó là lý do đáng bỏ mười phút lập trợ lý: lập một lần, sau đó mỗi bài chỉ cần đưa caption."

### PHẦN 2: LẬP AGENT TẠO ẢNH (demo làm theo, 8 phút, và thực hành)

**Tám phút demo này học viên nào nối được công cụ thì gõ cùng. Ai chưa nối vẫn lập file agent được, chỉ chưa chạy ra ảnh, để dành về nhà chạy.**

**Nhắc lại chỗ đặt agent, đọc cho lớp:** "Giống buổi 2. Agent đặt ở `.claude/agents/<tên>.md` NGAY TRONG thư mục làm việc của anh chị, không phải chỗ chung nào trên máy. Để nó gắn với đúng dự án này và sau này chia cho đồng đội được. Anh chị không phải tự tạo thư mục lồng nhau, cứ bảo Claude tạo."

1. Dán **PROMPT B3-10**, bấm Enter. Nói to "dán cùng tôi". Nhắc lớp giữ nguyên tên tiếng Việt không dấu.

**PROMPT B3-10:**

```
Tạo cho tôi một agent mới trong thư mục làm việc này.

Đường dẫn file: .claude/agents/tao-anh-san-pham.md
Đặt đúng trong thư mục làm việc hiện tại. Nếu thư mục .claude hoặc
.claude/agents chưa có thì tạo luôn.

File bắt đầu bằng phần frontmatter kẹp giữa hai dòng ba dấu gạch, gồm 3 dòng:
- name: tao-anh-san-pham
- description: viết rõ đây là trợ lý chuyên tạo ảnh cho bài đăng. Nêu ba lúc
  gọi nó ra: cần ảnh cho một bài Facebook, cần ảnh cho story hoặc reels, cần
  một bộ vài ảnh cho một chiến dịch. Nói rõ KHÔNG dùng để viết nội dung bài.
- tools: Read, generate_image

Phần dưới frontmatter viết hướng dẫn cho trợ lý này bằng tiếng Việt, câu ngắn,
gồm các ý sau:
1. Nhiệm vụ: nhận nội dung một bài đăng từ tôi, tự tạo ra ảnh minh họa hợp bài.
2. Việc đầu tiên luôn làm: đọc file CLAUDE.md trong thư mục để lấy màu thương
   hiệu, phong cách, và tinh thần sản phẩm. Ảnh phải hợp với những thứ đó.
3. Tự viết mô tả ảnh đủ năm yếu tố: chủ thể, bối cảnh, phong cách, tỉ lệ khung,
   tông màu. Không hỏi tôi năm yếu tố, tự suy ra từ nội dung bài và CLAUDE.md,
   nhưng nếu thiếu thông tin sản phẩm quan trọng thì hỏi lại, không bịa.
4. Chọn tỉ lệ theo kênh: bài Facebook thì vuông 1:1; story và reels thì dọc
   9:16; ảnh bìa thì ngang 16:9. Nếu tôi không nói kênh thì hỏi.
5. Luôn chừa một góc trống, mặc định góc dưới bên phải, để tôi ghép logo sau.
6. TUYỆT ĐỐI không viết chữ tiếng Việt quan trọng lên ảnh, nhất là tên sản
   phẩm và giá. Chữ đó tôi thêm sau bằng Canva.
7. Tạo xong lưu ảnh vào thư mục 05-tai-lieu và cho tôi biết đã tạo mấy ảnh,
   tỉ lệ gì, và đã chừa góc nào cho logo.

Viết để người không rành máy tính đọc là hiểu. Xong thì đọc lại nguyên nội
dung file cho tôi xem.
```

2. **Điểm dừng bắt buộc:** hỏi "ai đã thấy Claude báo tạo xong file `tao-anh-san-pham.md` thì giơ tay hoặc gõ chat". Chờ hai phần ba lớp. Mở file ra, chỉ vào dòng `tools: Read, generate_image`, nói: "Chú ý dòng này. `generate_image` là quyền gọi công cụ vẽ ảnh, `Read` là quyền đọc `CLAUDE.md`. Thiếu `generate_image` thì trợ lý này không vẽ được, chỉ nói suông. Đây là chỗ khác với trợ lý viết bài buổi 2."

*Lưu ý cho giảng viên: tên tool cấp cho agent để gọi công cụ vẽ ảnh có thể hiển thị khác theo cách MCP đăng ký, ví dụ có tiền tố. Chạy thử PROMPT B3-11 trên máy trước buổi, nếu agent không gọi được thì kiểm lại tên tool trong dòng tools và sửa cho khớp tên thật trên máy.*

### PHẦN 3: CHẠY THỬ TRỢ LÝ VỚI MỘT CAPTION (thực hành, phần chính, 27 phút chia ra)

Chia 27 phút thực hành: hoàn thiện agent 8 phút, chạy thử 12 phút, sửa 7 phút.

#### Việc 1 (8 phút): hoàn thiện agent của mình

**Đề bài:** "Mở file `tao-anh-san-pham.md` ra đọc lại. Sửa cho hợp thương hiệu mình: nếu sản phẩm anh chị không phải chai serum thì đảm bảo phần nhiệm vụ không ghi cứng 'chai serum'. Kiểm dòng `tools` có `generate_image` và `Read`. Ai chưa nối công cụ vẫn hoàn thiện file, để về nhà chạy."

**Tiêu chí xong Việc 1:** có file `.claude/agents/tao-anh-san-pham.md` trong thư mục làm việc, frontmatter đủ ba dòng name, description, tools; phần hướng dẫn có đủ: đọc CLAUDE.md, chọn tỉ lệ theo kênh, chừa góc logo, cấm chữ tiếng Việt.

#### Việc 2 (12 phút): chạy thử, đưa caption cho trợ lý ra ảnh

**Đề bài:** "Giờ thử sức mạnh thật của trợ lý: anh chị KHÔNG tả ảnh nữa, chỉ đưa nội dung bài. Ai nối được công cụ thì chạy. Ai chưa, xem tôi chạy trên màn hình."

**Bước 1, đưa một caption ngắn, PROMPT B3-11:**

```
Nhờ trợ lý tao-anh-san-pham tạo ảnh cho bài đăng Facebook sau của tôi:

"Da đang sau mụn, dễ đỏ rát, mỗi lần thử sản phẩm mới là hồi hộp. Serum rau
má B5 của Thảo An làm dịu da, cấp ẩm, dành cho da nhạy cảm. Nhắn tin để được
tư vấn nhé."

Kênh đăng: Facebook. Làm đúng hướng dẫn trong file agent, không bỏ bước nào.
```

"Anh chị để ý: tôi không tả chủ thể, bối cảnh, tông màu gì cả. Tôi chỉ đưa bài. Trợ lý tự đọc `CLAUDE.md`, tự nghĩ ra ảnh hợp bài này, tự chọn tỉ lệ vuông vì tôi nói Facebook, tự chừa góc logo. Đó là cái sướng của việc lập trợ lý: brief một câu, ra hình."

**Bước 2, đưa bài của chính mình.** Ai có bài thật thì thay caption Thảo An bằng một bài của mình. Nhắc nói rõ kênh đăng.

**Tiêu chí xong Việc 2:** trợ lý đọc CLAUDE.md trước; ra được ảnh hợp nội dung bài; đúng tỉ lệ kênh; có chừa góc trống; không có chữ tiếng Việt quan trọng trên ảnh.

#### Việc 3 (7 phút): sửa cho đúng gu

**Đề bài:** "Agent không phải lập một lần là chuẩn ngay. Ảnh đầu thường lệch chút. Ta sửa bằng cách sửa HƯỚNG DẪN trong file agent, không sửa từng ảnh."

"Ví dụ ảnh ra tối màu quá so với thương hiệu tươi sáng của anh chị, thì đừng ngồi vẽ lại chục lần. Bảo Claude: `Trong file tao-anh-san-pham.md, phần hướng dẫn, thêm một câu: ảnh luôn sáng, tông tươi, nhiều ánh sáng tự nhiên.` Rồi chạy lại. Sửa công thức, không sửa kết quả, giống buổi 2 anh chị sửa skill."

"Ai không gặp lỗi thì làm việc này cho chắc: bảo chính Claude soi lại agent." Gõ (không đánh số): `Đọc lại file tao-anh-san-pham.md và chỉ ra: chỗ nào còn mơ hồ khiến ảnh dễ ra lệch gu thương hiệu, chỗ nào quên chưa dặn. Sửa lại file, giữ nguyên cấu trúc.`

**Câu chốt cuối K3:** "Anh chị vừa lập được một bạn thiết kế riêng, thuộc gu thương hiệu, làm ảnh cả ngày không mệt. Nó nằm trong thư mục làm việc của anh chị, gắn với đúng dự án này, và sau này chia cho đồng đội được. Đây là thứ giá trị nhất anh chị mang về hôm nay."

### DỰ PHÒNG

- **Agent không gọi được công cụ vẽ, chỉ mô tả ảnh bằng chữ:** kiểm dòng `tools` có `generate_image` đúng tên trên máy chưa. Gõ `Liệt kê các tool mà agent tao-anh-san-pham đang được phép dùng.` Sửa dòng tools cho khớp tên thật, rồi chạy lại.
- **Agent không đọc CLAUDE.md, ảnh lệch brand:** bảo gõ `Sửa file agent: bước đầu tiên BẮT BUỘC là đọc CLAUDE.md, chưa đọc thì chưa được vẽ.` Chạy lại.
- **Agent hỏi lại năm yếu tố thay vì tự suy:** đó là nó quá thận trọng. Bảo gõ `Sửa file agent: tự suy năm yếu tố từ nội dung bài và CLAUDE.md, chỉ hỏi khi thiếu thông tin sản phẩm thật sự.`
- **Ảnh ra đẹp nhưng sai tỉ lệ kênh:** kiểm phần chọn tỉ lệ trong file agent, và nhắc học viên phải nói rõ kênh trong prompt gọi.
- **Hết giờ Việc 1 chưa xong file:** dùng luôn bản Claude vừa trả, chuyển sang chạy thử. Thà chạy được bản chưa hoàn hảo còn hơn ngồi mãi khâu viết.
- **Người xong sớm cả khối:** cho tạo một BỘ ba ảnh cho cùng một chiến dịch bằng cách thêm `--n` khi dùng dòng lệnh, hoặc bảo agent tạo ba biến thể; hoặc thêm vào file agent mục "tông màu cấm dùng" để ảnh không bao giờ lệch.
- **Người chưa nối công cụ:** vẫn lập và hoàn thiện file agent đầy đủ, ghép xem chung màn hình một bạn đã nối để thấy ảnh ra. Chạy thật ở nhà.

---

## K4. GẮN LOGO, NGƯỜI DUYỆT, CHI PHÍ (25 phút, 09:55 - 10:20)

**Câu hỏi dẫn:** Ảnh đẹp rồi, nhưng đăng thẳng lên có ổn không? Còn thiếu gì?

**Mục tiêu khối:** học viên biết ghép logo vào ảnh bằng Canva, hiểu ảnh là bản nháp cần người duyệt, và biết kiểm chi phí còn lại.

### PHẦN 1: GẮN LOGO BẰNG CANVA (giảng và demo 7 phút, thực hành 8 phút)

**Lý thuyết, nói thẳng, đọc nguyên văn:** "Ảnh phải có logo thì mới là ảnh thương hiệu. Nhưng tôi nói thật để anh chị không kỳ vọng sai: **công cụ vẽ ảnh này KHÔNG tự ghép logo được.** Nó chỉ có đúng hai việc: vẽ ảnh, và kiểm tra đăng nhập. Không có nút ghép logo. Và đừng bảo AI tự vẽ logo của anh chị, nó vẽ sai bét, chữ méo, hình lệch."

"Cách làm đúng, chắc chắn, tôi dùng thật: khi tạo ảnh, mình đã bảo trợ lý CHỪA một góc trống, nhớ không, đó là lý do ở K2 và K3 câu nào cũng có 'chừa góc dưới bên phải'. Giờ mình lấy logo THẬT của thương hiệu, ghép vào đúng góc đó bằng Canva. Kéo thả, hai phút xong. Logo thật thì lúc nào cũng đúng."

**THAO TÁC DEMO:**

1. Mở ảnh vừa tạo ở K3 (file trong `05-tai-lieu`).
2. Mở Canva trên trình duyệt, tạo một thiết kế, tải ảnh vừa tạo lên làm nền.
3. Tải file logo thật của thương hiệu lên Canva.
4. Kéo logo vào đúng góc trống đã chừa, chỉnh kích thước cho vừa mắt.
5. Nếu bài cần chữ, ví dụ tên sản phẩm hoặc giá, thêm chữ bằng Canva ngay lúc này. "Đây chính là chỗ ta thêm chữ tiếng Việt, bằng Canva, chữ chuẩn, không sai dấu. Nhớ lý do từ K2 chứ: AI viết chữ tiếng Việt hay sai, nên chữ để Canva làm."
6. Tải ảnh hoàn chỉnh về máy.

*Lưu ý cho giảng viên: đường bấm trong Canva có thể đổi theo phiên bản web. Kiểm trước buổi, hoặc dùng công cụ ghép ảnh khác quen tay. Điểm cốt lõi truyền đạt là: chừa góc khi tạo, ghép logo thật sau, đừng để AI vẽ logo.*

**THỰC HÀNH (8 phút):** "Ai có ảnh và có file logo thì ghép thử ngay. Ai chưa có ảnh thật thì ghép logo lên một ảnh mẫu tôi phát, cho quen tay. Ai chưa có logo số hóa thì đây là việc ghi vào bài về nhà: chuẩn bị một file logo nền trong suốt."

**Tiêu chí coi là xong:** mỗi học viên ghép được logo vào một góc ảnh, ra một ảnh có nhận diện thương hiệu; hiểu chữ tiếng Việt thêm bằng Canva.

### PHẦN 2: NGƯỜI DUYỆT CUỐI (giảng 3 phút)

"Nguyên tắc chống bịa thứ ba từ buổi 1, buổi 2, hôm nay áp cho ảnh. **Ảnh AI tạo là bản NHÁP, không phải bản đăng.** Anh chị xem kỹ rồi mới đăng. Trợ lý tạo ảnh không tự đăng lên trang, giống trợ lý viết bài không tự đăng bài."

"Xem gì khi duyệt ảnh? Ba thứ. Một, ảnh có đúng sản phẩm mình không, AI hay vẽ thêm chi tiết lạ, ví dụ chai có hai nắp, tay người sáu ngón. Hai, có chữ lạ nào lọt vào không, nếu có thì che bằng logo hoặc chữ Canva. Ba, ảnh có hợp giọng thương hiệu không, thương hiệu lành tính mà ảnh ra lòe loẹt thì loại."

"Anh chị tạo mấy ảnh thì chọn ảnh đạt, loại ảnh lỗi ngay, đừng tiếc. Ảnh lỗi giữ lại chỉ tổ đăng nhầm."

*(Chiếu bảng bốn câu hỏi duyệt ảnh, bảo lớp chép vào vở, dùng mỗi lần trước khi đăng.)*

| Duyệt ảnh, hỏi bốn câu | Không đạt thì |
|---|---|
| Đúng sản phẩm của mình không? | Loại, tạo lại với mô tả rõ hơn |
| Có chữ lạ hay chữ sai dấu lọt vào không? | Che bằng logo hoặc chữ Canva, hoặc loại |
| Có chi tiết vô lý không (tay thừa ngón, chai hai nắp)? | Loại ngay |
| Có hợp giọng và màu thương hiệu không? | Không hợp thì loại |

"Bốn câu này mất mười giây, nhưng nó chặn được cái ảnh lỗi lọt lên trang. Ảnh đăng rồi mới thấy sai thì mất uy tín, gỡ xuống cũng muộn."

### PHẦN 3: CHI PHÍ (giảng và demo 4 phút)

"Việc cuối, chuyện tiền. **Mỗi lần vẽ một ảnh đều tốn một lượt** trong tài khoản của anh chị. Vẽ đi vẽ lại chục lần cho một bài là hết lượt nhanh, và dồn dập quá còn dễ bị cổng web chặn tạm. Nên: **nghĩ kỹ mô tả trước khi bấm.** Tả cho đủ năm yếu tố ngay từ đầu, để ra đúng trong một hai lần, thay vì vẽ mò chục lần."

**THAO TÁC DEMO, xem còn bao nhiêu lượt:**

```
uv run aigpt accounts
```

"Đây là lệnh ở K1, giờ dùng để xem còn bao nhiêu lượt. Anh chị thỉnh thoảng chạy nó để biết mình còn dùng được bao nhiêu, giống xem số dư tài khoản."

*Cách khác trong Claude:* có thể hỏi thẳng trong tab Code `Kiểm tra trạng thái đăng nhập và lượt còn lại của công cụ ai-image-gpt.` để nó gọi tool kiểm tra.

**Câu chốt cuối K4:** "Ba việc để ảnh dùng được thật: gắn logo bằng cách chừa góc rồi ghép thật; luôn có người duyệt vì ảnh là nháp; và tiết kiệm lượt bằng cách tả kỹ trước khi bấm. Ba việc nhỏ mà tách ảnh nghiệp dư khỏi ảnh dùng được."

### DỰ PHÒNG

- **Học viên chưa có logo số hóa:** ghi vào bài về nhà, chuẩn bị file logo nền trong suốt (định dạng png). Trong buổi cứ ghép thử logo mẫu cho quen tay.
- **Có người hỏi sao không để AI ghép logo cho nhanh:** trả lời thẳng, không hứa suông: "Công cụ này chỉ vẽ ảnh và kiểm đăng nhập, không có việc ghép logo. Ghép thủ công bằng Canva mới chắc, và logo thật mới đúng."
- **Lệnh `accounts` báo hết lượt giữa buổi:** bình thường với tài khoản phụ dùng nhiều. Chuyển sang chiếu ảnh mẫu đã tạo sẵn, tập trung vào phần ghép logo và duyệt, hai phần này không cần tạo ảnh mới.
- **Có người muốn tạo thật nhiều ảnh một lúc:** nhắc lại cổng web dễ báo bận khi tạo dồn dập, và tốn lượt. Khuyên tạo giãn cách, tả kỹ để ăn ngay.

---

## K5. CHỐT VÀ GIAO BÀI (10 phút, 10:20 - 10:30)

### LỜI GIẢNG

"Hai tiếng rưỡi vừa rồi anh chị đi từ bài hay mà thiếu ảnh, tới chỗ có một trợ lý riêng làm ảnh. Tôi chốt ba thứ anh chị mang về."

*(Chiếu bảng, đọc to, bảo lớp tự đối chiếu máy mình.)*

| # | Sản phẩm | Ở đâu |
|---|---|---|
| 1 | Công cụ vẽ ảnh đã nối vào Claude | Trên máy, tài khoản ChatGPT phụ. Ai chưa nối thì làm bù ở nhà theo file hướng dẫn |
| 2 | Một trợ lý tạo ảnh do mình lập | `.claude/agents/tao-anh-san-pham.md` trong thư mục làm việc |
| 3 | Vài ảnh có logo, đăng được | Thư mục `05-tai-lieu`, đã ghép logo bằng Canva |

"Ai thiếu mục nào giơ tay hoặc gõ chat, tôi ghi lại để hỗ trợ. Đặc biệt ai chưa nối được công cụ, tôi ghi tên, gửi kèm file hướng dẫn và hẹn hỗ trợ riêng."

"Ba nguyên tắc chống bịa vẫn nguyên, theo anh chị suốt khóa. **Một:** chỉ dùng dữ liệu anh chị cấp, không tự chế. **Hai:** gắn nhãn nguồn, thiếu thì ghi chưa đủ dữ liệu. **Ba:** người duyệt cuối, mọi thứ là nháp, Claude không tự đăng."

"Và một điều riêng của buổi ảnh, ghi vào vở, quan trọng nhất hôm nay: **không để AI viết chữ tiếng Việt lên ảnh rồi đăng thẳng.** Chữ tiếng Việt để Canva làm. AI làm phần hình, người làm phần chữ."

"**Bài tập về nhà, ba việc. Việc một:** ai chưa nối công cụ thì nối theo file hướng dẫn, nối được thì nhắn tôi. **Việc hai:** dùng trợ lý tạo ảnh làm ảnh cho ít nhất ba bài thật trong tuần, mỗi ảnh ghép logo bằng Canva, ghi lại chỗ nào trợ lý ra lệch để buổi sau sửa. **Việc ba:** ai chưa có file logo nền trong suốt thì chuẩn bị, vì tuần nào cũng cần."

"**Mồi cho buổi sau.** Giờ anh chị viết được bài, làm được ảnh. Nhưng đăng thủ công từng bài, từng ảnh, vẫn mất công. Buổi sau ta nối các mảnh lại: từ ý tưởng, ra bài, ra ảnh, tới lịch đăng, thành một dòng chảy. Cảm ơn anh chị, hẹn gặp buổi sau."

---

## CHECKLIST CHUẨN BỊ TRƯỚC BUỔI

### Làm trước buổi ít nhất 3 ngày

- [ ] **Gửi file hướng dẫn cài công cụ vẽ ảnh cho lớp.** File ghi rõ sáu bước B3-1 tới B3-6, kèm cách cài Python và uv. Nhắc học viên cố cài trước, và dùng tài khoản ChatGPT PHỤ, không dùng tài khoản chính.
- [ ] Xác nhận ai qua buổi 2, có thư mục làm việc và `CLAUDE.md`. Ai chưa thì chuẩn bị bộ Thảo An mẫu để phát.
- [ ] Nhắc lớp: chuẩn bị sẵn một file logo nền trong suốt (png) để ghép ở K4.

### Làm trước buổi 1 ngày

- [ ] **Máy giảng viên đã nối xong công cụ vẽ ảnh, chạy được.** Chạy trọn PROMPT B3-7 ra một ảnh thật, xác nhận. Đây là chỗ K1 phụ thuộc hoàn toàn.
- [ ] Chạy thử toàn bộ B3-0 tới B3-11 trên máy giảng viên, xác nhận chạy đúng. Riêng PROMPT B3-10 (lập agent) chạy trọn một lần, xác nhận file nằm đúng `.claude/agents/tao-anh-san-pham.md`, và PROMPT B3-11 (chạy agent) ra được ảnh thật.
- [ ] **Kiểm tên tool cấp cho agent:** chạy B3-11, nếu agent không gọi được công cụ vẽ, kiểm tên tool thật trên máy (có thể có tiền tố), sửa dòng `tools` trong B3-10 cho khớp trước khi in phiếu prompt.
- [ ] **Kiểm đường vào cấu hình MCP** của Claude Desktop trên phiên bản hiện tại, ghi rõ ra giấy nhắc. Đây là chỗ demo B3-3.
- [ ] Chạy `uv run aigpt accounts`, xác nhận còn đủ lượt cho cả buổi demo. Nếu gần hết, chuẩn bị tài khoản phụ thứ hai.
- [ ] Tạo sẵn 4 tới 6 ảnh mẫu (đủ tỉ lệ vuông, dọc, ngang; có ảnh chừa góc logo) để chiếu khi mạng chậm, để lớp không ngồi chờ máy quay.
- [ ] Chuẩn bị sẵn một ảnh mẫu và một file logo mẫu để phát cho người chưa có, dùng luyện ghép Canva ở K4.
- [ ] Kiểm Canva chạy được trên máy giảng viên, đăng nhập sẵn, có sẵn logo Thảo An mẫu để demo ghép.
- [ ] Chuẩn bị bảng hoặc slide vẽ sẵn: bảng năm yếu tố tả ảnh (K2), khung frontmatter 3 dòng của agent (K3), ba việc ở K4.

### Mang tới lớp hoặc gửi qua Zoom

- [ ] Phiếu copy các prompt B3-0 tới B3-11, gửi bản mềm qua chat Zoom và để trên Drive lớp.
- [ ] File hướng dẫn cài công cụ (sáu bước) gửi lại lần nữa trong buổi, cho ai chưa cài.
- [ ] Chụp sẵn ảnh màn hình kết quả B3-7, B3-9, B3-11 để dùng khi mạng chậm.
- [ ] Một trợ giảng trực khung chat Zoom, riêng buổi này lo phần ai kẹt khi nối công cụ ở K1.

---

## XỬ LÝ TÌNH HUỐNG LỚP HỌC

### Tình huống về kỹ thuật

| Tình huống | Xử lý ngay |
|---|---|
| Cả lớp không ai nối được công cụ ở K1 | Bình thường, đã lường trước. Giảng viên tạo ảnh trên máy mình suốt K2, K3. Lớp làm bù ở nhà theo file hướng dẫn. Không dừng buổi cài từng máy. |
| Chạy login xong mà báo chưa đăng nhập | Gần chắc quên bước hai. Làm lại từ B3-4, nhớ dán đường dẫn callback ở B3-5. |
| Đã làm đủ hai bước vẫn báo chưa đăng nhập | File lưu đăng nhập lưu sai. Đăng nhập lại một lần từ B3-4, thường lần hai được. |
| Tạo ảnh báo 503 hoặc server busy | Cổng web đang bận. Chờ chút rồi thử lại, giãn cách giữa các lần, đừng bấm dồn. |
| Ảnh vẽ mãi không ra | Đừng bấm lại. Vẽ một ảnh mất 1 tới 4 phút. Chờ thêm, quá lâu thì thử lại một lần. |
| Agent chỉ mô tả ảnh bằng chữ, không vẽ | Kiểm dòng `tools` có `generate_image` đúng tên chưa. Gõ `Liệt kê tool agent tao-anh-san-pham được dùng.` Sửa cho khớp, chạy lại. |
| Ảnh cố viết chữ tiếng Việt, sai dấu | Bình thường với AI. Chấp nhận, vì chữ sẽ do Canva thêm sau, đè lên. Nếu bắt buộc chữ trên ảnh, dùng dòng lệnh với `--thinking` mức cao. |
| Ảnh ra sai sản phẩm hoặc chi tiết lạ | Tả rõ hơn phần chủ thể, chạy lại. Đừng vẽ mò chục lần, mỗi lần tốn một lượt. |
| Hết lượt tạo ảnh giữa buổi | Chiếu ảnh mẫu đã tạo sẵn. Chuyển sang phần ghép logo và duyệt, hai phần này không cần tạo ảnh mới. |
| Đường vào cấu hình MCP khác bài mô tả | Dùng đường đã kiểm trên máy giảng viên (ghi ở giấy nhắc). Đừng mô tả theo trí nhớ. |

### Tình huống về lớp

| Tình huống | Xử lý ngay |
|---|---|
| Có người nản vì phần nối công cụ khó | Trấn an: "Đây là phần khó nhất cả khóa. Nối một lần, dùng mãi. Chưa nối được hôm nay không sao, tôi hỗ trợ riêng." Cho xem demo để thấy đáng công. |
| Có người hỏi vì sao không dùng công cụ dễ hơn | Trả lời thẳng: công cụ này vẽ ảnh miễn phí qua tài khoản ChatGPT sẵn có, đổi lại cài hơi cực một lần. Đây là lựa chọn học và thử nghiệm. |
| Có người lo dùng bị khóa tài khoản | Đúng, đó là lý do dùng tài khoản PHỤ, và tạo giãn cách, không dồn dập. Nhắc lại đây là công cụ nối qua cổng web, không phải cổng chính thức. |
| Có người hỏi ảnh AI có được đăng bán hàng không | Trả lời: ảnh là bản nháp, người duyệt trước khi đăng. Kiểm đúng sản phẩm, không chữ lạ, hợp giọng. Ảnh minh họa thì được, ảnh giả mạo chứng nhận thì không. |
| Có người bảo AI vẽ chưa đẹp bằng thuê thiết kế | Đồng ý: "Đúng, mục tiêu không phải thay thiết kế cho ảnh quan trọng. Mục tiêu là ra ảnh nháp trong vài phút cho bài hàng ngày, thay vì chờ cả ngày." |
| Người xong sớm cả buổi | Cho tạo một bộ ba ảnh cho một chiến dịch, hoặc thêm mục tông màu cấm vào file agent, hoặc luyện ghép logo nhiều tỉ lệ. |
| Người chưa nối công cụ ngồi không ở K3 | Ghép xem chung màn hình một bạn đã nối. Vẫn cho lập và hoàn thiện file agent để về nhà chạy. Đừng để ai ngồi xem suông. |

---

## ƯU TIÊN KHI THIẾU GIỜ

Thứ tự giữ lại, từ quan trọng nhất: **K3 (lập trợ lý tạo ảnh) > K2 (viết mô tả năm yếu tố) > K4 (logo, duyệt, chi phí) > K1 (nối công cụ) > K5 > K0.**

Lý do K1 xếp thấp khi thiếu giờ: phần nối công cụ có thể chuyển hẳn thành xem demo và làm ở nhà, không nhất thiết cả lớp làm tại chỗ. Phần hiểu và làm ra ảnh (K2, K3) mới là giá trị mang về.

- **Thiếu 5 phút:** rút giờ sửa ở K3 (Việc 3) xuống còn nhờ Claude tự soi agent, chuyển sửa tay sang bài về nhà.
- **Thiếu 10 phút:** rút K1 xuống còn giảng viên demo nhanh sáu bước (không chờ ai làm cùng), dồn giờ cho K2 và K3. Ghép logo ở K4 chuyển thành demo, thực hành để về nhà.
- **Thiếu 15 phút trở lên:** K1 chỉ chiếu demo và nói "làm bù ở nhà theo file"; giữ nguyên K2 và K3; K4 rút còn nói ba nguyên tắc logo, duyệt, chi phí kèm một demo ghép logo, bỏ thực hành ghép tại lớp.
- **Không bao giờ cắt:** phần lập và chạy thử agent tạo ảnh ở K3; bài học chữ tiếng Việt ở K2; câu chừa góc để ghép logo; và cảnh báo tài khoản phụ ở K1.

---

## GHI CHÚ CUỐI

- **Đau trước, giải pháp sau là xương sống buổi này.** Mỗi khối mở bằng nỗi đau: bài thiếu ảnh (K0), tả tay từng ảnh mệt (K3), ảnh chưa có logo chưa dùng được (K4). Giữ đúng thứ tự đó, đừng đảo thành định nghĩa khô trước.
- **Phần nối công cụ ở K1 là chỗ khó nhất và dễ vỡ nhịp nhất.** Với lớp không biết code, đừng kỳ vọng cả lớp cùng nối xong tại chỗ. Thiết kế đã chốt: giảng viên nối sẵn, demo lại, lớp xem, làm bù ở nhà. Giảng viên khác dạy buổi này phải hiểu điều này, đừng cố ép cả lớp cài trong 30 phút.
- **Đăng nhập công cụ có ĐÚNG HAI bước.** B3-4 chạy login, B3-5 dán lại đường dẫn callback. Đây là bẫy số một, nhắc kỹ trong bài và trong file hướng dẫn.
- **Công cụ nối qua cổng web ChatGPT, không phải cổng chính thức.** Phải nói thật với lớp: dùng tài khoản phụ, tạo giãn cách, đây là công cụ học và thử nghiệm. Ghi rõ ở K1 và nhắc lại ở K4.
- **Công cụ chỉ có hai việc: vẽ ảnh và kiểm đăng nhập.** KHÔNG có ghép logo tự động. Bài đã viết trung thực điều này ở K4: chừa góc khi tạo, ghép logo thật bằng Canva sau. Đừng hứa MCP ghép logo, vì không có.
- **Chữ tiếng Việt trên ảnh là điểm riêng phải nhấn.** AI vẽ chữ tiếng Việt hay sai dấu. Nguyên tắc: AI làm hình, Canva làm chữ. Nếu bắt buộc chữ trên ảnh thì dùng dòng lệnh với `--thinking` mức cao để giảm sai, nhưng vẫn khuyên Canva. Đây là nguyên tắc chống bịa riêng của buổi ảnh.
- **Nối về buổi 2, không giảng lại.** Học viên đã biết MCP và đã lập agent ở buổi 2. Buổi 3 chỉ nhắc một câu rồi dùng lại. Đừng giảng lại hai khái niệm đó từ đầu, phí giờ.
- **Các điểm chưa chắc, phải kiểm trên máy trước buổi, đã liệt kê ở CHECKLIST:** đường vào cấu hình MCP; tên tool cấp cho agent để gọi công cụ vẽ (có thể có tiền tố); thời gian tạo một ảnh; đường bấm trong Canva; các tùy chọn dòng lệnh (`--aspect`, `--thinking`, `--n`). Đừng mô tả theo trí nhớ trước lớp.
- **Prompt B3-0 tới B3-11 phải khớp nguyên văn với phiếu copy phát cho học viên.** Cần sửa thì sửa đồng thời ở giáo án, phiếu copy và bản mềm trên Drive.
- **Feed sang buổi sau.** Buổi 3 cho ra bài và ảnh. Buổi sau nối chuỗi từ ý tưởng tới lịch đăng. Giảng viên ghi lại danh sách ai chưa nối được công cụ ngay cuối K5 để hỗ trợ riêng.
- **Buổi 3 KHÔNG dạy:** dùng cổng ảnh chính thức trả tiền của hãng (ngoài phạm vi); tự động đăng ảnh lên trang (buổi sau); dựng video từ ảnh; ghép logo tự động (công cụ không có); chỉnh sửa ảnh nâng cao trong Canva ngoài ghép logo và thêm chữ.

---

## PHỤ LỤC: DANH SÁCH PROMPT VÀ LỆNH DÙNG TRONG BUỔI

| Mã | Dùng ở | Nội dung tóm tắt |
|---|---|---|
| B3-0 | K0 | Kiểm tra thư mục và có CLAUDE.md chưa |
| B3-1 | K1 | `git clone` tải mã nguồn công cụ |
| B3-2 | K1 | `uv sync` cài các thứ cần |
| B3-3 | K1 | Dán JSON đăng ký MCP vào Claude Desktop |
| B3-4 | K1 | `uv run aigpt login` đăng nhập bước một |
| B3-5 | K1 | `uv run aigpt login --callback "..."` bước hai |
| B3-6 | K1 | `uv run aigpt accounts` kiểm đăng nhập và lượt |
| B3-7 | K1 | Tạo ảnh đầu tiên, ảnh nền đơn giản |
| B3-8 | K2 | Tả sơ sài, để so sánh |
| B3-9 | K2 | Tả kỹ đủ năm yếu tố cho Thảo An |
| B3-10 | K3 | Lập agent `tao-anh-san-pham` |
| B3-11 | K3 | Chạy agent với một caption |

Ba lệnh dòng lệnh hay dùng lại: `uv run aigpt accounts` (xem lượt), `uv run aigpt gen "..." --out ten.png --aspect 1:1 --thinking extended` (tạo ảnh có kiểm soát tỉ lệ và render chữ), thêm `--n 2` để tạo nhiều ảnh một lần.
