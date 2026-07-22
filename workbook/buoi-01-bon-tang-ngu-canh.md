# Buổi 1 · Workbook học viên

**Workbook này dùng trong 3 khối thực hành: K2, K3, K4. Tổng khoảng 85 phút.** Làm theo thứ tự, đừng nhảy cóc. Mỗi khối có prompt mẫu copy dán được và bảng để bạn điền tay.

**Cuối buổi bạn phải có:** 1 file `CLAUDE.md` cho thương hiệu mình, 1 skill chạy được, 1 kết nối MCP, 10 hook, 10 CTA, 3 bài viết bán hàng.

## Checklist trước khi bắt đầu

Chưa tick đủ thì báo giảng viên ngay trong 15 phút đầu buổi.

- [ ] Claude Desktop đã cài, đăng nhập bằng tài khoản trả phí
- [ ] Thấy tab **Code** ở trên cùng và bấm vào được
- [ ] Đã chọn đúng thư mục làm việc `C:\Users\<tên bạn>\thao-an-marketing`
- [ ] Claude tạo được file thật trong thư mục đó

Chưa cài xong? Mở [../tai-lieu-hoc-vien/huong-dan-cai-dat.md](../tai-lieu-hoc-vien/huong-dan-cai-dat.md).

---

# K2 · Viết CLAUDE.md và bật Memory (25 phút)

Mục tiêu: Claude biết bạn là ai mà bạn không phải dán lại bối cảnh mỗi lần chat.

## Bước 1 · Điền bảng hồ sơ của bạn (8 phút)

Điền tay trước, đừng nhờ Claude điền hộ. Bạn biết thương hiệu mình, Claude thì không. Chưa có thương hiệu thật thì đọc mục cuối trang rồi quay lại.

**Câu định vị.** Theo cấu trúc: `[Thương hiệu] là [loại sản phẩm] dành cho [ai cụ thể] đang gặp [vấn đề gì]. Khác với [nhóm đối thủ], [thương hiệu] [điểm khác biệt] vì [bằng chứng].`

```


```

**3 thông điệp bán hàng:**

| # | Thông điệp (tối đa 2 câu) | Nhắm tình huống mua nào |
|---|---|---|
| 1 | | |
| 2 | | |
| 3 | | |

**5 nỗi đau và 5 mong muốn của khách:**

| # | Nỗi đau | Mong muốn |
|---|---|---|
| 1 | | |
| 2 | | |
| 3 | | |
| 4 | | |
| 5 | | |

**Giọng văn.** Mô tả bằng hành vi cụ thể, không dùng tính từ chung như "chuyên nghiệp", "thân thiện". Tính từ chung thì Claude hiểu kiểu gì cũng được, và nó sẽ hiểu sai.

| Mục | Nội dung của bạn |
|---|---|
| Xưng mình là gì, gọi khách là gì | |
| Độ dài câu, cách xuống dòng | |
| Số emoji tối đa mỗi bài | |
| **Nên dùng:** 3 kiểu câu | |
| **Nên tránh:** 3 kiểu câu | |

**Từ cấm của ngành bạn.** Phần quan trọng nhất, ngành nào cũng có ranh giới pháp lý riêng. Chưa rõ thì hỏi pháp chế, hoặc mở 3 bài cũ tìm chỗ đội đã tự né.

| # | Từ hoặc cách nói bị cấm | Nói thay bằng gì |
|---|---|---|
| 1 | | |
| 2 | | |
| 3 | | |
| 4 | | |
| 5 | | |

## Bước 2 · Nhờ Claude dựng file CLAUDE.md (8 phút)

Mở tab **Code**, đúng thư mục làm việc. Dán prompt dưới, thay phần trong ngoặc vuông bằng nội dung Bước 1.

```
Tạo file CLAUDE.md trong thư mục làm việc này.

Đây là hồ sơ thương hiệu để bạn tự đọc mỗi lần tôi mở phiên mới.
Viết tiếng Việt, câu ngắn, dùng bảng markdown khi hợp.

Nội dung gồm 8 mục theo đúng thứ tự:
1. Thương hiệu bán gì cho ai: [điền]
2. Danh sách sản phẩm và giá: [điền]
3. Câu định vị: [dán câu định vị]
4. Ba thông điệp bán hàng: [dán 3 thông điệp]
5. Chân dung khách: [dán 5 nỗi đau, 5 mong muốn]
6. Giọng văn nên dùng và nên tránh, mỗi bên kèm 2 ví dụ câu: [điền]
7. Danh sách từ cấm và cách nói thay thế: [dán bảng từ cấm]
8. Ba nguyên tắc chống bịa, chép nguyên văn:
   - Chỉ dùng dữ liệu tôi cấp. Không tự chế số liệu, thành phần, công dụng,
     giá, tên khách.
   - Gắn nhãn [DATA THẬT] và [SUY LUẬN]. Thiếu thì ghi "chưa đủ dữ liệu".
   - Tôi là người duyệt cuối. Mọi thứ gửi khách là nháp, bạn không tự bấm gửi.

Ghi xong thì tóm tắt file cho tôi trong 5 dòng.
```

Claude xin phép ghi file thì bấm **Yes**.

- [ ] File `CLAUDE.md` đã có trong thư mục làm việc
- [ ] Đã mở file đọc lại và sửa tay chỗ nghe không giống mình

Bí chỗ nào thì mở [../demo/buoi-01/claude-md-va-skill-mau.md](../demo/buoi-01/claude-md-va-skill-mau.md), phần 1 là `CLAUDE.md` mẫu hoàn chỉnh của Thảo An.

## Bước 3 · Kiểm tra Claude đọc được chưa (3 phút)

Mở phiên mới trong cùng thư mục, gõ:

```
Không cần đọc lại file nào, trả lời thẳng: thương hiệu của tôi tên gì,
bán cho ai, và có bao nhiêu từ nằm trong danh sách cấm?
```

- [ ] Claude trả lời đúng mà bạn không phải dán lại gì

Sai hoặc hỏi ngược lại? Kiểm 2 điều: file đúng tên `CLAUDE.md` chưa, và có nằm ngay trong thư mục làm việc chưa (không phải thư mục con).

## Bước 4 · Thử bẫy dữ liệu thiếu (3 phút)

Bài kiểm tra quan trọng nhất của K2. Hỏi một con số biết chắc file không có:

```
Cho tôi bảng chỉ số kinh doanh hiện tại của thương hiệu tôi:
ngân sách quảng cáo mỗi tháng, giá trị đơn trung bình,
số lượng khách đang có, tỷ lệ khách mua lại.
Gắn nhãn nguồn cho từng dòng.
```

**Đúng:** Claude ghi "chưa đủ dữ liệu" ở các dòng thiếu.
**Sai:** Claude điền một con số nghe hợp lý. Nó đang bịa. Thêm đoạn này vào cuối `CLAUDE.md` rồi chạy lại:

```
QUAN TRỌNG: Trước khi trả lời bất kỳ câu hỏi nào có số liệu,
kiểm tra con số đó có trong file này không. Không có thì bắt buộc ghi
"chưa đủ dữ liệu". Không ước lượng. Không lấy số trung bình ngành.
```

- [ ] Đã thử bẫy, Claude phản ứng đúng

## Bước 5 · Bật Memory (3 phút)

Memory là chỗ Claude nhớ những điều bạn chốt trong lúc làm, không phải hồ sơ cố định.

**Cách 1, thử trước:** gõ dấu thăng `#` ở đầu dòng rồi viết điều muốn nhớ. Claude hỏi lưu vào đâu, chọn lưu cho thư mục làm việc này. **Cách 2, nếu máy bạn không hiện tùy chọn đó:** bỏ dấu `#`, nhờ Claude ghi thẳng vào cuối `CLAUDE.md` mục "Ghi nhớ trong lúc làm".

```
# Tôi luôn duyệt bài trước khi đăng. Không bao giờ tự đăng thay tôi.
```

Ba điều bạn muốn Claude nhớ lâu dài:

| # | Điều cần nhớ |
|---|---|
| 1 | |
| 2 | |
| 3 | |

- [ ] Đã lưu ít nhất 1 điều

---

# K3 · Viết Skill đầu tiên (35 phút)

Skill là quy trình làm một việc lặp đi lặp lại, viết một lần dùng mãi. `CLAUDE.md` nói **bạn là ai**, skill nói **việc này làm theo mấy bước**. Skill hôm nay: `viet-bai-ban-hang`.

## Bước 1 · Điền khung SKILL.md (12 phút)

Điền tay vào khung 6 phần dưới. Điền càng cụ thể, skill chạy càng đúng. Mẫu đã điền đầy đủ ở [../demo/buoi-01/claude-md-va-skill-mau.md](../demo/buoi-01/claude-md-va-skill-mau.md) phần 2.

````
---
name: viet-bai-ban-hang
description:
  (2 tới 4 câu. Nêu skill làm gì, và ÍT NHẤT 3 TÌNH HUỐNG người dùng
   sẽ gõ gì thì skill này phải chạy. Claude chọn skill dựa vào đúng dòng
   này. Viết sơ sài là skill không bao giờ được gọi.)
---

# 1. Skill này làm gì


# 2. Đầu vào cần có
(Thứ bắt buộc phải có mới làm được: sản phẩm nào, nhắm nhóm khách nào,
 đăng kênh nào, mấy bài và dài bao nhiêu chữ)


# 3. Các bước làm
Bước 1: Kiểm tra đủ đầu vào ở mục 2 chưa. Thiếu thì HỎI LẠI, không tự đoán.
Bước 2:
Bước 3:
Bước 4:
Bước 5: Soát lại, không để lọt từ trong danh sách cấm ở CLAUDE.md.


# 4. Đầu ra
(Định dạng trả về: mấy bài, mỗi bài mấy chữ, có gợi ý ảnh không,
 có ghi rõ dùng hook số mấy CTA số mấy không)


# 5. Ví dụ mẫu
(Một bài viết hoàn chỉnh, đúng chuẩn bạn muốn. Đây là phần Claude bắt chước
 nhiều nhất. Viết dở thì kết quả dở theo.)


# 6. Khi nào KHÔNG dùng skill này

````

## Bước 2 · Nhờ Claude tạo file skill (5 phút)

```
Tạo file .claude/skills/viet-bai-ban-hang/SKILL.md trong thư mục làm việc này.
Tạo luôn các thư mục cha nếu chưa có.
Nội dung file đúng như sau, giữ nguyên frontmatter YAML ở đầu:

[dán khung 6 phần bạn đã điền]

Ghi xong báo tôi đường dẫn đầy đủ của file.
```

Bấm **Yes** khi Claude xin phép ghi file.

- [ ] File nằm đúng tại `.claude/skills/viet-bai-ban-hang/SKILL.md`
- [ ] Mở file thấy 3 dấu gạch ở dòng đầu, có `name` và `description`

**Đặt file ở đâu:** hôm nay dùng cách 1, đặt trong thư mục làm việc, tức `C:\Users\<tên>\thao-an-marketing\.claude\skills\viet-bai-ban-hang\SKILL.md`. Muốn skill xài được ở mọi thư mục thì đặt ở `C:\Users\<tên>\.claude\skills\viet-bai-ban-hang\SKILL.md`.

## Bước 3 · Kiểm tra skill có được gọi không (3 phút)

Mở phiên mới. **Đừng nhắc tên skill.** Gõ một câu tự nhiên như khi làm thật:

```
Viết cho tôi 3 bài đăng Facebook bán serum rau má, nhắm khách nữ da nhạy cảm.
```

- [ ] Claude báo đang dùng skill `viet-bai-ban-hang`, hoặc làm đúng theo các bước bạn viết

Skill không chạy? Lỗi gần như luôn ở dòng `description`. Viết `Viết bài bán hàng` thì Claude không biết khi nào gọi. Viết `Viết bài đăng bán hàng cho Facebook và Shopee. Dùng khi người dùng nói "viết bài bán serum", "soạn caption Facebook cho mặt nạ", "viết 3 bài cho khách chưa mua"` thì nó gọi đúng.

## Bước 4 · Chạy skill ra sản phẩm (15 phút)

```
Dùng skill viet-bai-ban-hang, làm 3 việc:

1. 10 hook mở bài. Mỗi hook phải chứa chi tiết chỉ thương hiệu tôi
   mới nói được.
2. 10 CTA, ghi rõ mỗi CTA dùng cho kênh nào.
3. 3 bài viết bán hàng, mỗi bài 150 tới 250 chữ, mỗi bài nhắm một
   tình huống: bài 1 khách mới biết lần đầu, bài 2 khách đã xem
   chưa mua, bài 3 khách đang so sánh với sản phẩm khác.

Bám đúng giọng văn và danh sách từ cấm trong CLAUDE.md.
Cuối mỗi bài ghi rõ đã dùng hook số mấy, CTA số mấy.
```

**10 hook và 10 CTA.** Cột "thay tên" là bài kiểm tra: thay tên thương hiệu bạn bằng tên đối thủ, câu vẫn hợp lý thì hook đó chưa đạt, phải viết lại.

| # | Hook | Thay tên đối thủ vào còn đúng không | CTA | Kênh nào |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |
| 5 | | | | |
| 6 | | | | |
| 7 | | | | |
| 8 | | | | |
| 9 | | | | |
| 10 | | | | |

**3 bài viết bán hàng:**

| Bài | Nhắm tình huống | Hook số | CTA số | Đã sửa tay chưa |
|---|---|---|---|---|
| 1 | Khách mới biết lần đầu | | | |
| 2 | Đã xem chưa mua | | | |
| 3 | Đang so sánh | | | |

Lưu lại, đừng để nguyên trong cửa sổ chat. Gõ: `Lưu 10 hook, 10 CTA và 3 bài viết ở trên vào file ket-qua-buoi-1.md trong thư mục làm việc.`

- [ ] Đã có file `ket-qua-buoi-1.md`

---

# K4 · Nối MCP (25 phút)

MCP là cầu nối để Claude với ra công cụ bên ngoài: đọc file trên Drive, tra bảng tính, đăng bài lên kênh. Không có MCP thì Claude chỉ biết những gì bạn dán vào.

> **CẢNH BÁO AN TOÀN DỮ LIỆU. ĐỌC TRƯỚC KHI BẤM BẤT KỲ NÚT NÀO.**
>
> 1. **Nối cái gì thì Claude đọc được cái đó.** Nối Drive công ty nghĩa là mọi file trong đó nằm trong tầm đọc. Trong lớp chỉ nối tài khoản cá nhân hoặc tài khoản thử. **Tuyệt đối không nối tài khoản chứa dữ liệu khách hàng thật, hợp đồng, hay số liệu tài chính.**
> 2. **Đọc kỹ bảng xin quyền trước khi bấm Allow.** Bảng đó ghi rõ Claude được đọc gì, ghi gì. Thấy có quyền xóa hoặc quyền gửi mà bạn không cần thì đừng nối.
> 3. **Không cấp quyền "gửi" hay "đăng" khi chưa cần.** Buổi này chỉ tập nối và đọc. Đăng thật để tới buổi 5, khi đã có bước người duyệt.
> 4. **Công ty bạn có quy định bảo mật thì hỏi trước, đừng tự quyết.**

## Bước 1 · Mở Connectors (4 phút)

Trong Claude Desktop bấm **Settings**, rồi tìm mục **Connectors** ở danh sách bên trái. Danh sách connector có sẵn hiện ra.

- [ ] Đã mở được màn hình Connectors

## Bước 2 · Chọn và bật một connector (8 phút)

Chọn một cái nhẹ, không đụng dữ liệu nhạy cảm:

| Connector | Dùng làm gì trong marketing | Rủi ro |
|---|---|---|
| Google Drive (tài khoản cá nhân) | Đọc hồ sơ sản phẩm, kế hoạch, báo cáo | Thấp nếu dùng tài khoản riêng |
| Google Sheets | Đọc bảng lead, bảng theo dõi đơn | Thấp |
| Công cụ tìm kiếm web | Tra thông tin thị trường, đối thủ | Rất thấp |

Bấm **Connect**, đăng nhập bằng tài khoản **thử hoặc cá nhân**, rồi **đọc kỹ bảng xin quyền**: nó xin đọc gì, ghi gì. Đồng ý thì bấm cho phép. Không đồng ý thì đóng lại, chọn cái khác.

| Mục | Ghi lại |
|---|---|
| Connector đã nối | |
| Tài khoản dùng (cá nhân hay công ty) | |
| Quyền nó xin (đọc, ghi, xóa) | |
| Dữ liệu nào của bạn giờ Claude nhìn thấy | |

- [ ] Đã nối được 1 connector
- [ ] Đã điền đủ 4 dòng. **Không điền được dòng cuối nghĩa là bạn chưa hiểu mình vừa cấp quyền gì. Ngắt kết nối và đọc lại.**

## Bước 3 · Kiểm tra và thử một việc chỉ đọc (13 phút)

Quay lại tab **Code**, mở phiên mới. Chạy lần lượt 3 lệnh, dừng lại xem kết quả từng lệnh:

```
1. Liệt kê các công cụ bên ngoài bạn đang nối được. Chỉ kể tên, chưa cần dùng.

2. Tìm trong Drive của tôi file nào có chữ "sản phẩm" trong tên. Chỉ liệt kê
   tên file và ngày sửa. Đừng mở, đừng sửa gì.

3. Đọc file [tên file] trên Drive, so với hồ sơ trong CLAUDE.md của tôi,
   chỉ ra 3 chỗ hai bên không khớp. Gắn nhãn [DATA THẬT] và [SUY LUẬN].
   Chỗ nào thiếu thì ghi "chưa đủ dữ liệu".
```

Lệnh 3 là điểm mấu chốt của cả buổi: MCP lấy dữ liệu ngoài, `CLAUDE.md` giữ luật, hai tầng làm việc cùng nhau.

- [ ] Claude kể đúng tên connector vừa nối
- [ ] Claude lấy được dữ liệu thật từ bên ngoài
- [ ] Claude vẫn giữ luật gắn nhãn nguồn khi làm với dữ liệu ngoài

Một việc bạn sẽ nối MCP để làm sau buổi học:

```


```

---

## Chưa có sản phẩm thật thì làm gì

Không sao. Dùng bộ Thảo An, bạn vẫn làm đủ mọi sản phẩm và học đủ mọi kỹ năng.

1. Mở [demo/thao-an/san-pham-thao-an.md](../demo/thao-an/san-pham-thao-an.md): hồ sơ 3 SKU, giá, thành phần, công dụng, danh sách điều không được nói. Copy file đó vào thư mục `thao-an-marketing`, rồi gõ: `Đọc file san-pham-thao-an.md tôi vừa bỏ vào thư mục này.`
2. K2: lấy dữ liệu từ file đó thay vì tự nghĩ. Riêng câu định vị và 3 thông điệp vẫn phải tự viết, đó là phần luyện.
3. Bí thì mở [../demo/buoi-01/claude-md-va-skill-mau.md](../demo/buoi-01/claude-md-va-skill-mau.md): phần 1 là `CLAUDE.md` hoàn chỉnh của Thảo An, phần 2 là `SKILL.md` hoàn chỉnh. K3 và K4 chạy nguyên prompt trong workbook, không phải sửa gì.

**Điều cần biết:** bộ này **cố tình thiếu 4 mục dữ liệu** (ngân sách ads tháng, giá trị đơn trung bình, số lượng review, người trực inbox). Đó là để bạn thấy Claude phản ứng ra sao khi gặp lỗ hổng. Bước 4 của K2 dựa vào đúng 4 mục này.

**Sau buổi học:** có dữ liệu thật rồi thì chỉ sửa `CLAUDE.md`, prompt và skill giữ nguyên. Đó là điểm lợi của việc dựng ngữ cảnh thay vì chat lẻ.

---

## Checklist tự kiểm trước khi nộp

Thiếu một ô là chưa đạt.

**Bốn tầng:**
- [ ] `CLAUDE.md` nằm đúng trong thư mục làm việc, đủ 8 mục, giọng văn mô tả bằng hành vi kèm ví dụ câu chứ không phải danh sách tính từ
- [ ] Mở phiên mới hỏi bất kỳ, Claude trả lời đúng mà không cần dán lại bối cảnh
- [ ] Đã lưu ít nhất 1 điều vào Memory
- [ ] Skill đúng tại `.claude/skills/viet-bai-ban-hang/SKILL.md`, có `name` và `description`, description nêu ít nhất 3 tình huống kích hoạt
- [ ] Bước 1 trong skill là kiểm tra đủ đầu vào, thiếu thì hỏi lại
- [ ] Gõ câu tự nhiên không nhắc tên skill, Claude vẫn gọi đúng skill
- [ ] Đã nối 1 connector, lấy được dữ liệu thật, và ghi rõ nó nhìn thấy dữ liệu nào của bạn

**Chống bịa, quan trọng nhất:**
- [ ] **Đã hỏi một con số hồ sơ không có, Claude ghi "chưa đủ dữ liệu" thay vì điền số nghe hợp lý.** Chưa qua ô này thì mọi thứ còn lại không đáng tin
- [ ] Kết quả có gắn nhãn `[DATA THẬT]` và `[SUY LUẬN]`
- [ ] Dò ngược 3 dòng `[DATA THẬT]` về hồ sơ gốc, cả 3 có thật
- [ ] Không có số liệu, thành phần, tên khách nào không tìm thấy trong nguồn

**Nội dung:**
- [ ] Đủ số: 1 câu định vị, 3 thông điệp, 5 nỗi đau, 5 mong muốn, 10 hook, 10 CTA, 3 bài viết
- [ ] Ít nhất 6 trên 10 hook qua được bài kiểm tra thay tên đối thủ
- [ ] 3 bài đã sửa tay, không để nguyên bản máy viết
- [ ] Soát lại toàn bộ, không lọt từ nào trong danh sách cấm

**Nộp gì:** file `CLAUDE.md`, file `SKILL.md`, file `ket-qua-buoi-1.md`, và 1 ảnh chụp màn hình phần Connectors thấy rõ connector đã nối.

---

CES Global · Creative, Effective, Sustainable
