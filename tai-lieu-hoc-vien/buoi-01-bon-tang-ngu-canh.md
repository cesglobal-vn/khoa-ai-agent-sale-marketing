# Tài liệu học viên · Buổi 1: Bốn tầng ngữ cảnh

**Khóa:** AI Agent cho Sale & Marketing · CES Global
**Buổi:** 1 trên 6 · 150 phút · **Ngày học:** 22/07/2026

Đây là bản mang về để tra và làm lại. Bản làm trong lớp là [../workbook/buoi-01-bon-tang-ngu-canh.md](../workbook/buoi-01-bon-tang-ngu-canh.md).

---

## 1. Buổi này anh chị đã làm gì

Hôm nay anh chị dựng bốn tầng ngữ cảnh cho Claude, trong đúng một thư mục làm việc.

- **Tầng 1, `CLAUDE.md`:** bản brief thương hiệu, Claude đọc trước mọi việc, anh chị không phải dán lại bối cảnh lần nào nữa.
- **Tầng 2, Skill:** quy trình viết bài bán hàng, đặt tại `.claude/skills/viet-bai-ban-hang/SKILL.md`, đã chạy thật rồi tự soi và sửa một vòng.
- **Tầng 3, Memory:** sổ bàn giao giữa các phiên, phiên mới mở ra là Claude đã biết anh chị là ai.
- **Tầng 4, MCP:** một kết nối đọc được dữ liệu thật trên Google Drive hoặc Google Sheet.

Sản phẩm mang về: 1 thư mục làm việc, 1 `CLAUDE.md` đủ 9 mục, 1 Skill chạy được, 3 bài bán hàng, 10 hook, 10 CTA, 1 kết nối MCP.

Ba nguyên tắc chống bịa đi theo suốt 6 buổi: chỉ dùng dữ liệu anh chị cấp; gắn nhãn `[DATA THẬT]` và `[SUY LUẬN]`, thiếu thì ghi "chưa đủ dữ liệu"; người duyệt cuối, Claude không tự bấm đăng.

---

## 2. Bộ prompt copy dùng ngay

Chỗ nào ghi `[CẦN ĐIỀN]` thì thay bằng thông tin của anh chị. Ai dùng thương hiệu thật của mình thì thay hồ sơ Thảo An bằng hồ sơ của mình, giữ nguyên cấu trúc prompt.

### NHÓM A · Dựng nền: CLAUDE.md và Memory

**A1. Nhờ Claude viết `CLAUDE.md`**

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

Dùng khi: mở thư mục làm việc mới cho một thương hiệu. Làm một lần cho mỗi thương hiệu.

**A2. Kiểm nhanh Claude đã đọc được `CLAUDE.md` chưa**

```
Thảo An cấm dùng những từ nào, và gọi khách hàng bằng gì?
```

Dùng khi: vừa tạo xong `CLAUDE.md`, hoặc nghi Claude đang làm việc ở nhầm thư mục.

**A3. Bật Memory và dặn ba điều**

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

Dùng khi: đã bật Memory trong Settings. Dặn một lần, dùng cho mọi phiên sau.

**A4. Kiểm Memory ở một phiên trò chuyện MỚI**

```
Tôi làm marketing cho thương hiệu nào, và bạn cần hỏi tôi những gì trước khi viết bài bán hàng?
```

Dùng khi: ngay sau A3. Claude ngơ ngác không biết anh chị là ai tức là Memory chưa bật thật.

### NHÓM B · Thử phép chống bịa

**B1. Hỏi ba con số mà hồ sơ ghi rõ là chưa có**

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

Dùng khi: vừa viết xong `CLAUDE.md`, và mỗi lần nhận bàn giao một thư mục làm việc của người khác. Đạt là cả 3 câu đều trả "chưa đủ dữ liệu".

**B2. Nó vẫn bịa số thì thêm dòng ràng buộc cứng vào `CLAUDE.md`**

```
Mở file CLAUDE.md trong thư mục này, thêm vào mục 9 đúng một dòng sau,
giữ nguyên từng chữ:

Khi tôi hỏi một con số không có trong file của thư mục này, câu trả lời duy
nhất được phép là "chưa đủ dữ liệu, cần bổ sung từ [tên nguồn]". Không ước
lượng, không dùng số trung bình ngành.
```

Dùng khi: chạy B1 mà Claude đưa ra một con số nghe hợp lý. Thêm dòng này rồi chạy lại B1. Đây là cách sửa gốc: sửa brief chứ không sửa kết quả.

### NHÓM C · Viết và chạy Skill

**C1. Tạo file Skill**

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

Dùng khi: chuẩn hóa một đầu việc lặp lại hằng tuần. Mỗi đầu việc một skill riêng.

**C2. Thử skill bằng một yêu cầu CỐ Ý thiếu thông tin**

```
Dùng skill viet-bai-ban-hang viết cho tôi một bài.
```

Dùng khi: vừa tạo xong skill. Đạt là Claude hỏi ngược lại đủ 4 đầu vào chứ không tự đoán.

**C3. Chạy skill ra 3 bài bán hàng**

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

Dùng khi: cần một loạt bài cho nhiều SKU và nhiều mục tiêu khác nhau.

**C4. Ra 10 hook và 10 CTA**

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

Dùng khi: cần kho hook và CTA dùng dần cho cả tháng.

**C5. Nhờ chính Claude soi lại và sửa skill**

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

Dùng khi: đã chạy skill được vài lần và thấy phải sửa tay kết quả nhiều lần.

### NHÓM D · MCP đọc dữ liệu thật

**D1. Kiểm kết nối đang trỏ vào tài khoản nào**

```
Bạn đang đọc được Drive của tài khoản nào của tôi?
```

Dùng khi: ngay sau khi bật connector. Sai tài khoản thì gỡ ra nối lại, đừng chạy tiếp.

**D2. Đọc bảng đơn hàng và đối chiếu với brief**

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

Dùng khi: cần đối chiếu điều mình tin với số liệu bán hàng thật. Đối chiếu tay 2 dòng bất kỳ trước khi tin con số Claude cộng ra.

### NHÓM E · Cứu lỗi

**E1. Không thấy file Claude vừa tạo**

```
Liệt kê tất cả file trong thư mục này kèm đường dẫn đầy đủ.
```

**E2. Claude không nhận ra skill vừa viết**

```
Liệt kê các skill đang có trong thư mục này kèm đường dẫn.
```

**E3. Bài viết vẫn dính từ cấm**

```
Trong file SKILL.md, mục Ràng buộc, thêm nguyên danh sách từ cấm và thêm bước
bắt buộc dò lại toàn bài với danh sách đó trước khi trả kết quả.
```

Dùng khi: kết quả sai lặp lại. Sửa quy trình, không sửa kết quả.

---

## 3. Sản phẩm buổi 1 anh chị phải có trên máy

| # | Sản phẩm | Nằm ở đâu |
|---|---|---|
| 1 | Thư mục làm việc `thao-an-marketing` | Màn hình nền, hoặc `C:\Users\<tên đăng nhập>\thao-an-marketing` |
| 2 | Hồ sơ sản phẩm `san-pham-thao-an.md` | Trong thư mục làm việc, chép từ [../demo/thao-an/san-pham-thao-an.md](../demo/thao-an/san-pham-thao-an.md) |
| 3 | `CLAUDE.md` đủ 9 mục | Ngay trong thư mục làm việc |
| 4 | Skill `viet-bai-ban-hang` | `.claude/skills/viet-bai-ban-hang/SKILL.md` trong thư mục làm việc |
| 5 | 3 bài bán hàng, lưu thành `bai-ban-hang-mau.md` | Trong thư mục làm việc |
| 6 | 10 hook và 10 CTA, lưu thành `hook-cta.md` | Trong thư mục làm việc |
| 7 | Memory đã bật và đã kiểm ở phiên mới | Settings của Claude Desktop |
| 8 | 1 kết nối MCP đọc được dữ liệu | Settings, mục Connectors |

Bản mẫu `CLAUDE.md` và `SKILL.md` để đối chiếu: [../demo/buoi-01/claude-md-va-skill-mau.md](../demo/buoi-01/claude-md-va-skill-mau.md).

---

## 4. Checklist tự kiểm

- [ ] Mở Claude Desktop, tab **Code**, đang trỏ đúng thư mục `thao-an-marketing`
- [ ] `CLAUDE.md` có đủ 9 mục; câu định vị đủ 4 phần
- [ ] Mục giọng văn KHÔNG chứa các từ "chuyên nghiệp", "thân thiện", "uy tín", "trẻ trung"
- [ ] Mục từ cấm chép đủ, không bớt dòng nào so với hồ sơ sản phẩm
- [ ] Mục 5 nỗi đau đang gắn nhãn `[SUY LUẬN]`. Đây là chủ ý, buổi 2 sẽ thay bằng lời khách thật
- [ ] Chạy prompt B1: cả 3 câu đều trả "chưa đủ dữ liệu"
- [ ] File skill nằm đúng `.claude/skills/viet-bai-ban-hang/SKILL.md`, frontmatter đủ 2 dòng
- [ ] Dòng `description` có nêu cả tình huống KHÔNG dùng skill
- [ ] Mục 6 của skill có 1 bài mẫu đã viết xong
- [ ] Có 3 bài bán hàng, không bài nào chứa từ cấm, mỗi bài có phần gắn nhãn nguồn ở cuối
- [ ] Có 10 hook và 10 CTA, đã qua phép thử đổi tên thương hiệu
- [ ] Memory bật thật: mở phiên mới, Claude vẫn nêu đúng tên thương hiệu
- [ ] Connector đang trỏ vào tài khoản Google demo hoặc cá nhân, KHÔNG phải tài khoản công ty

---

## 5. Việc làm ở nhà trước buổi 2

| # | Việc | Nộp gì | Hạn |
|---|---|---|---|
| 1 | Chạy thật skill `viet-bai-ban-hang` ít nhất 3 lần trong tuần cho việc thật. Ghi lại chỗ nào phải sửa tay sau khi nó chạy xong | Danh sách chỗ phải sửa tay, mang vào buổi 2 | Trước buổi 2 |
| 2 | Ai đang dùng dữ liệu Thảo An: viết hồ sơ sản phẩm của chính thương hiệu mình theo đúng cấu trúc `san-pham-thao-an.md`, bỏ vào thư mục làm việc, rồi chạy lại prompt A1 | File hồ sơ sản phẩm và `CLAUDE.md` của thương hiệu mình | Trước buổi 2 |
| 3 | Ai đã cấp quyền Google bằng tài khoản cá nhân mà không dùng tiếp: vào gỡ quyền ngay tối nay, ở cả hai chỗ (trang quản lý tài khoản Google, và Settings > Connectors của Claude Desktop) | Ảnh chụp màn hình đã gỡ | Ngay tối nay |
| 4 | **Gom dữ liệu khách hàng cho buổi 2:** tối thiểu 20 mẩu, tốt nhất 30 tới 60. Một mẩu là một review, một câu hỏi inbox, hoặc một bình luận. Xóa tên thật, số điện thoại, địa chỉ. Đánh ID R01, M01, C01. Giữ nguyên văn kể cả sai chính tả | File dữ liệu đã đánh ID, để sẵn trong thư mục làm việc | Trước buổi 2 |
| 5 | Ai muốn lấy bình luận thật từ TikTok hoặc Instagram ở buổi 2: đăng ký tài khoản **tikhub** và nạp một khoản nhỏ. Mỗi lượt gọi tính tiền, tự trả. Không đăng ký vẫn học đủ và nộp đủ sản phẩm | Tài khoản đã dùng được | Trước buổi 2 |

Buổi 2 lấy `CLAUDE.md` và skill của hôm nay làm đầu vào. Ai chưa có 2 thứ này thì buổi 2 phải ngồi làm lại từ đầu.

---

## 6. Năm lỗi hay gặp khi làm lại ở nhà

| Lỗi | Dấu hiệu anh chị thấy | Cách xử lý |
|---|---|---|
| Sai thư mục làm việc | Claude làm rất đúng nhưng anh chị không tìm thấy file vừa tạo | Đây là lỗi phổ biến nhất. Nhìn góc màn hình xem tab Code đang mở thư mục nào. Sai thì bấm nút chọn thư mục, trỏ lại. Hoặc chạy prompt E1 để Claude đọc đường dẫn đầy đủ |
| Claude không gọi skill ra | Gõ "viết bài bán hàng giúp tôi" mà bài ra chung chung, không nhắc tên skill nào | Chạy E2 kiểm đường dẫn. Đúng đường dẫn rồi thì lỗi nằm ở dòng `description`: viết lại cho sát những chữ anh chị thật sự gõ, nêu 3 tình huống cụ thể |
| Claude bịa số | Đưa ra ngân sách, số review, giá trị đơn trung bình nghe rất hợp lý | Mở hồ sơ dò ngược, không thấy dòng nào thì chạy prompt B2 thêm ràng buộc cứng vào `CLAUDE.md`, rồi chạy lại B1. Sửa brief, không sửa kết quả |
| Bài viết vẫn dính từ cấm | Xuất hiện "trị mụn", "đặc trị", "7 ngày hết thâm" | Chạy E3. Đừng sửa tay từng bài, sửa mục Ràng buộc trong skill rồi chạy lại cả loạt |
| `CLAUDE.md` phình quá dài | File hơn 100 dòng, có cả quy trình 8 bước viết bài | Gõ: `Rút gọn còn khoảng 60 dòng, bỏ hết phần quy trình chi tiết của từng việc.` Quy trình để dành cho skill, brief chỉ ghi thứ luôn đúng cho mọi việc |

---

CES Global · Creative, Effective, Sustainable
