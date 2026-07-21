# Buổi 3 · Workbook học viên

65 phút, 8 bước, 7 sản phẩm. Làm tuần tự, đừng nhảy cóc. Điền thẳng vào các bảng trống trong file này.

**Trước khi bắt đầu:** lưu 3 file skill từ `system-prompt.md` vào thư mục làm việc: `.claude/skills/lead-scoring/SKILL.md`, `.claude/skills/soan-proposal/SKILL.md`, `.claude/skills/theo-duoi-chot-don/SKILL.md`. Không tạo thư mục bằng tay, nhờ Claude tạo giùm trong tab Code. Sau đó mỗi bước dưới đây chạy trong **một phiên riêng**, gọi đúng một skill. Nhồi cả 3 vào một phiên là đến câu thứ 30 agent quên bảng tiêu chí của bạn.

---

## Checklist chuẩn bị data (5 phút)

Mọi file dưới đây chép vào **thư mục làm việc** đã lập ở buổi 1, cạnh `CLAUDE.md`. Claude tự đọc, không phải đính kèm.

- [ ] Danh sách 10 lead, đủ 6 cột: tên cơ sở, loại hình, khu vực, kênh liên hệ, người phụ trách, ghi chú trao đổi.
- [ ] Ghi chú trao đổi là **nguyên văn**, không phải tóm tắt. Copy thẳng đoạn chat.
- [ ] Lead nào thiếu thông tin thì **để trống**, không điền bừa.
- [ ] Chính sách giá: bảng chiết khấu theo số lượng, điều khoản thanh toán và vận chuyển.
- [ ] Danh sách **điều chưa có chính sách**. Chưa viết thì viết ngay, 5 dòng là đủ.
- [ ] Đầu ra buổi 1 và 2 đã nằm sẵn trong thư mục: hồ sơ sản phẩm `san-pham-thao-an.md`; câu định vị, 3 thông điệp, giọng văn và danh sách từ cấm trong `CLAUDE.md`; bảng insight khách hàng `insight-khach-hang.md` của buổi 2.
- [ ] Đủ 3 file skill trong `.claude/skills/`.

**Chưa có lead thật thì làm gì:** chép nguyên `case-study/thao-an/danh-sach-lead-si.md` (10 lead) và `case-study/thao-an/chinh-sach-gia-si.md` vào thư mục làm việc. Đủ để hoàn thành cả 7 sản phẩm. Đừng ngồi chờ xin data, làm trên Thảo An xong về thay dữ liệu là ra bộ của mình.

## Bước 1 · Bắt agent tự khai nó thiếu gì (4 phút · skill `lead-scoring`)

Mở phiên mới trong tab Code.

```
Đọc hồ sơ sản phẩm và danh sách lead trong thư mục làm việc.
Đây là dữ liệu nền. Xác nhận, chưa làm gì thêm.

Xác nhận theo mẫu:
1. Bạn đọc được bao nhiêu lead.
2. Lead nào thiếu thông tin người phụ trách.
3. Ba loại dữ liệu nào KHÔNG có trong file mà việc chấm điểm lead thường cần.
```

Ghi lại 3 thứ agent nói là thiếu: ..................................................

Agent trả lời "dữ liệu đầy đủ" là agent sắp bịa. Kiểm lại: Claude có báo đang dùng skill `lead-scoring` không. Không báo thì dòng `description` trong `SKILL.md` viết chưa đúng, sửa rồi chạy lại.

## Bước 2 · Tự viết bảng tiêu chí chấm điểm (9 phút)

**Điền bảng này trên giấy trước, chưa mở Claude.** Đây là phần agent không được làm thay.

Chọn 4 tiêu chí. Tổng trọng số phải bằng 100%. Mô tả mốc 5, 3, 1 đủ rõ để người khác chấm lại ra cùng kết quả.

| Tiêu chí | Trọng số | 5 điểm | 3 điểm | 1 điểm |
|---|---|---|---|---|
| A. | % | | | |
| B. | % | | | |
| C. | % | | | |
| D. | % | | | |

**Tự trả lời trước khi đi tiếp:** vì sao tiêu chí trọng số cao nhất lại cao nhất? ....................

Bí thì lấy bộ mẫu Thảo An rồi sửa: Quy mô đơn 25% · Độ khớp định vị 25% · Mức độ quan tâm 30% · Khả năng chốt trong 30 ngày 20%. Mức độ quan tâm nặng nhất vì đó là hành vi quan sát được, không phải phán đoán.

## Bước 3 · Chấm điểm 10 lead (9 phút · skill `lead-scoring`)

Dán nguyên bảng bước 2 vào prompt.

```
Chấm điểm 10 lead theo ĐÚNG bộ tiêu chí dưới. Không tự thêm, không tự bớt tiêu chí.

[dán nguyên bảng tiêu chí của bạn, có mô tả mốc 5/3/1]

Công thức: Điểm = (A×trọng số + B×trọng số + C×trọng số + D×trọng số) × 20

Xuất bảng markdown, cột:
Lead | Tên | A | B | C | D | Điểm | Nhóm | Độ tin cậy | Lý do một dòng | Việc cần làm tiếp

Quy tắc bắt buộc:
- Tiêu chí nào chấm bằng suy luận thì ghi số kèm dấu * và chú thích cuối bảng.
- Lead có từ 2 tiêu chí trở lên chấm bằng suy luận thì Độ tin cậy = Thấp.
- Nhóm A từ 75 điểm, Nhóm B 60 đến 74, Nhóm C dưới 60.
- KHÔNG bịa doanh số, ngân sách, hay tên người phụ trách.
```

### Sản phẩm 2 · Lead Scoring Sheet

| Lead | Tên cơ sở | A | B | C | D | Điểm | Nhóm | Tin cậy | Việc cần làm tiếp |
|---|---|---|---|---|---|---|---|---|---|
| 01 | | | | | | | | | |
| 02 | | | | | | | | | |
| 03 | | | | | | | | | |
| 04 | | | | | | | | | |
| 05 | | | | | | | | | |
| 06 | | | | | | | | | |
| 07 | | | | | | | | | |
| 08 | | | | | | | | | |
| 09 | | | | | | | | | |
| 10 | | | | | | | | | |

**Kiểm ngay:** đếm số ô có dấu *. Ra 0 là agent đang bịa, vì dữ liệu gốc thiếu doanh số, ngân sách và nhà cung cấp hiện tại của mọi lead. Chạy lại và nhắc nguyên tắc gắn nhãn nguồn.

**Lưu lại ngay:** gõ `Lưu bảng này thành bang-diem-lead.md trong thư mục làm việc.` Bấm **Yes** khi Claude xin phép ghi file. Bước 8 sẽ đọc lại file này.

## Bước 4 và 5 · Mười email và mười tin nhắn (20 phút · skill `lead-scoring`)

Chạy theo lô 3 đến 4 lead một lần, đừng đòi 10 email trong một lượt.

```
Viết email tiếp cận cho lead [số]: [tên].

Ràng buộc:
- Bám ĐÚNG ghi chú trao đổi của lead này. Ít nhất một câu phải nhắc lại điều họ đã nói hoặc đã làm.
- Dưới 150 từ. Giọng theo phần giọng văn trong CLAUDE.md.
- Chỉ được nhắc mức chiết khấu có trong file chính sách, ghi rõ điều kiện số lượng đi kèm.
- Không dùng từ trong danh sách "Điều KHÔNG được nói".
- Kết bằng MỘT lời đề nghị bước tiếp cụ thể, khác nhau tùy lead.
- Tài liệu nào chưa chắc có sẵn thì ghi [CẦN XÁC NHẬN], không hứa gửi.
- Cuối email liệt kê [DATA THẬT] và [SUY LUẬN].
```

Xong 10 email thì chạy tiếp prompt thứ hai:

```
Chuyển 10 email trên thành tin nhắn Zalo (hoặc LinkedIn nếu lead là doanh nghiệp lớn).

Ràng buộc:
- Tối đa 4 câu. Không xuống dòng nhiều lần.
- Không mở bằng "Chào anh/chị, em là..." rồi mới vào việc. Vào việc từ câu đầu.
- Không dán bảng giá vào tin nhắn. Chỉ nêu MỘT con số hoặc MỘT lợi ích, rồi hỏi.
- Kết bằng một câu hỏi trả lời được bằng một dòng.
- Giữ nguyên chi tiết riêng của từng lead như trong email.
```

### Sản phẩm 3 và 4 · Bảng theo dõi 10 email và 10 tin nhắn

| Lead | Tiêu đề email | Câu trích từ ghi chú trao đổi | Lời đề nghị bước tiếp | Tin nhắn (4 câu) |
|---|---|---|---|---|
| 01 | | | | |
| 02 | | | | |
| 03 | | | | |
| 04 | | | | |
| 05 | | | | |
| 06 | | | | |
| 07 | | | | |
| 08 | | | | |
| 09 | | | | |
| 10 | | | | |

**Bài kiểm tra che tên:** che hết tên riêng trong 3 email bất kỳ, đưa người bên cạnh đoán là lead nào. Không đoán được thì viết lại. Cột "câu trích" mà trống hoặc chung chung là email điền tên, không phải cá nhân hóa.

## Bước 6 · Kịch bản gọi 5 phút (7 phút · skill `theo-duoi-chot-don`)

Mở phiên mới. Skill này tự đọc `bang-diem-lead.md` để biết lead nào nhóm A.

```
Viết kịch bản gọi điện 5 phút cho lead nhóm A.

Cấu trúc theo mốc thời gian, mỗi mốc ghi rõ lời thoại nguyên văn:
0:00 đến 0:30  Mở đầu, xin phép, nêu lý do gọi
0:30 đến 1:30  Ba câu hỏi tìm hiểu, kèm mục đích của từng câu
1:30 đến 3:00  Gắn sản phẩm vào điều họ vừa nói, không đọc thuộc lòng tính năng
3:00 đến 4:00  Nêu mức giá và điều kiện đi kèm, chỉ dùng số trong chính sách
4:00 đến 5:00  Chốt bước tiếp theo, xin cam kết nhỏ

Kèm ô "Nếu khách nói X thì rẽ sang" cho 3 tình huống hay gặp nhất.
Viết như lời nói, đọc lên phải giống người. Không viết như văn bản.
```

### Sản phẩm 5 · Kịch bản gọi

| Mốc | Lời thoại | Mục đích |
|---|---|---|
| 0:00 đến 0:30 | | |
| 0:30 đến 1:30 | | |
| 1:30 đến 3:00 | | |
| 3:00 đến 4:00 | | |
| 4:00 đến 5:00 | | |

Ba nhánh rẽ: 1. .............. 2. .............. 3. .............. **Kiểm:** đọc to lên, nghe không giống người nói thì viết lại ngắn hơn.

## Bước 7 · Mười kịch bản xử lý từ chối (9 phút · skill `theo-duoi-chot-don`)

```
Viết 10 kịch bản xử lý từ chối cho ngành [ngành của bạn], bán sỉ cho [loại khách].

Mỗi kịch bản gồm 4 phần:
1. Lời từ chối, viết đúng cách khách hay nói, không viết kiểu sách vở.
2. Điều họ thực sự lo bên dưới câu đó.
3. Câu trả lời, TỐI ĐA 3 câu, câu cuối là một câu hỏi hoặc một đề xuất bước tiếp.
4. Bằng chứng cần có sẵn trong tay khi trả lời.

Ràng buộc: không hứa điều ngoài chính sách. Chạm điều chưa có chính sách thì ghi
"cần xin ý kiến chủ doanh nghiệp".
```

### Mười lời từ chối hay gặp, để đối chiếu (bám case Thảo An)

1. "Sản phẩm này khách của em da nhạy cảm, lỡ kích ứng thì em chịu trách nhiệm sao?" (L09 Thanh Tâm đang lo đúng điều này)
2. "Bên em đang nhập của một bên khác rồi, đang ổn."
3. "Giá cao quá, bên kia cho chiết khấu tốt hơn."
4. "Lấy về bán không được thì tồn kho, em không dám ôm hàng."
5. "Thương hiệu Việt khách chưa tin, khách toàn hỏi hàng Hàn hàng Nhật."
6. "Cho em ký gửi đi, bán được rồi em thanh toán."
7. "Em muốn độc quyền khu vực này thì mới làm." (L07 Minh Phát)
8. "Để em xem doanh số dòng cũ đã rồi tính." (L02 Lan Anh)
9. "Em không có ảnh với nội dung để đăng bán, tự làm không nổi." (L10 Bé Xíu)
10. "Cái này em phải trình lại, quy trình duyệt bên em lâu lắm." (L04 Beauty House)

### Sản phẩm 6 · Bảng 10 kịch bản

| # | Lời từ chối | Lo thật bên dưới | Câu trả lời (tối đa 3 câu) | Bằng chứng cần có |
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

**Kiểm số 6 và số 7:** ký gửi và độc quyền khu vực đều nằm trong mục "Điều chưa có chính sách". Hai ô này bắt buộc phải có câu xin ý kiến chủ doanh nghiệp. Agent tự hứa được là prompt của bạn thiếu hàng rào.

## Bước 8 · Proposal nháp 3 đến 5 trang (7 phút · skill `soan-proposal`)

Mở phiên mới. Chọn **lead điểm cao nhất** trong `bang-diem-lead.md`, nêu rõ đang làm lead nào. Đừng bảo skill đọc cả 10 lead, proposal sẽ ra chung chung.

```
Soạn proposal hợp tác sỉ cho lead [số]: [tên]. Người nhận: [tên, chức vụ].

Dàn ý 6 phần, 3 đến 5 trang:
1. Vì sao chúng tôi hợp với tệp khách của bên anh/chị
2. Danh mục sản phẩm và đối tượng phù hợp
3. Bảng báo giá theo chính sách, có ví dụ giỏ hàng cụ thể
4. Điều khoản: thanh toán, vận chuyển, đổi trả, hỗ trợ bán hàng
5. Lộ trình triển khai
6. Bước tiếp theo

Ràng buộc cứng:
- MỌI con số phải truy được về file chính sách hoặc hồ sơ sản phẩm.
- Không cam kết công dụng ngoài phần ghi trên nhãn.
- Không dùng từ trong danh sách "Điều KHÔNG được nói".
- Cuối proposal liệt kê mọi chỗ [CẦN XÁC NHẬN] và [SUY LUẬN].
```

### Sản phẩm 7 · Dàn ý proposal

| Phần | Nội dung chính | Nguồn số liệu |
|---|---|---|
| 1. Vì sao hợp | | |
| 2. Danh mục | | |
| 3. Bảng báo giá | | |
| 4. Điều khoản | | |
| 5. Lộ trình | | |
| 6. Bước tiếp | | |

**Bài kiểm tra 30 giây, bắt buộc chạy:**

```
Liệt kê MỌI con số xuất hiện trong proposal vừa rồi.
Mỗi con số ghi rõ lấy từ đâu: tên file, dòng nào.
Con số nào bạn tự tính hoặc tự suy thì ghi [SUY LUẬN].
Con số nào không truy được nguồn thì ghi [BỊA] và đề xuất xóa.
```

Cột [BỊA] có bất kỳ dòng nào thì proposal không được gửi. Sửa rồi chạy lại.

## Checklist tự kiểm trước khi nộp

**Bảng điểm**
- [ ] Trọng số do tôi đặt, tôi giải thích được vì sao.
- [ ] Có ít nhất một ô đánh dấu suy luận, và không phải 10/10 dòng đều tin cậy Cao.
- [ ] Không có tên người phụ trách nào do agent tự đặt.

**Email và tin nhắn**
- [ ] Đủ 10 email, đủ 10 tin nhắn.
- [ ] Mỗi email có ít nhất một câu trích từ ghi chú trao đổi thật, che tên đi vẫn đoán được của ai.
- [ ] Lời đề nghị bước tiếp khác nhau giữa các lead, không copy chung một câu.
- [ ] Mọi mức chiết khấu nhắc trong email đều có trong chính sách, kèm điều kiện số lượng.

**Kịch bản gọi và xử lý từ chối**
- [ ] Kịch bản gọi đủ 5 mốc, đọc to lên nghe giống người nói.
- [ ] Đủ 10 kịch bản từ chối, mỗi câu trả lời tối đa 3 câu.
- [ ] Ô ký gửi và ô độc quyền khu vực đều có câu xin ý kiến chủ doanh nghiệp.

**Proposal và ba file skill**
- [ ] Proposal đủ 6 phần, 3 đến 5 trang, mọi con số truy được về file nguồn.
- [ ] Đã chạy bài kiểm tra 30 giây, cột [BỊA] trống.
- [ ] Đã lưu `bang-diem-lead.md` và `proposal-<mã lead>.md` vào thư mục làm việc.
- [ ] Đủ 3 file `SKILL.md` trong `.claude/skills/`, đã sửa theo ngành và chính sách của tôi, cả 3 đều có mục ranh giới.
- [ ] Mỗi file skill có frontmatter với `name` và `description`, dòng `description` nêu ít nhất 3 câu tôi thật sự sẽ gõ.
- [ ] Thử gọi từng skill bằng một câu tự nhiên, không nhắc tên skill, cả 3 đều chạy đúng.

Nộp vào thư mục cá nhân, đặt tên `buoi03-<tên>-<sản phẩm>.md`. Giữ nguyên định dạng bảng, buổi 4 dùng lại. Ba file skill để nguyên trong thư mục làm việc, buổi 6 gom lại thành bộ bàn giao.
