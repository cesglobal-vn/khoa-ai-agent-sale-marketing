# Tài liệu học viên · Buổi 2: Customer Insight Agent

**Khóa:** AI Agent cho Sale & Marketing · CES Global
**Buổi:** 2 trên 6 · 150 phút · **Ngày học:** ______

Đây là bản mang về để tra và làm lại. Bản làm trong lớp là [../workbook/buoi-02-customer-insight-agent.md](../workbook/buoi-02-customer-insight-agent.md).

---

## 1. Buổi này anh chị đã làm gì

Hôm nay anh chị đọc dữ liệu khách hàng nguyên văn và rút ra điều họ thật sự quan tâm.

- Cài **Customer Insight Agent** thành skill `.claude/skills/customer-insight/SKILL.md` trong đúng thư mục làm việc của buổi 1.
- Bắt agent đếm dữ liệu và tự khai ba chỗ dữ liệu KHÔNG trả lời được, trước khi cho nó phân tích.
- Ra bảng insight có trích dẫn ID, tần suất ghi dạng x trên tổng, không có chữ "đa số".
- Dựng persona, rồi chuyển sang 5 content angle, 5 bài social, 3 brief hình ảnh và 3 visual đăng được.
- Trả lời hứa của buổi 1: thay 5 nỗi đau `[SUY LUẬN]` trong `CLAUDE.md` bằng 5 nỗi đau có mã trích dẫn thật.

Nguyên tắc lớn của buổi: insight nào không chỉ ra được mẩu nào thì insight đó chưa chắc. `[SUY LUẬN]` không xấu; suy luận đội lốt dữ liệu mới xấu.

---

## 2. Bộ prompt copy dùng ngay

Chạy theo đúng thứ tự nhóm. Nhóm C hỏng thì mọi nhóm sau đều hỏng.

### NHÓM A · Lấy dữ liệu bằng tikhub (bỏ qua nếu chưa có tài khoản)

**A1. Lấy bình luận dưới một video TikTok**

```
Dùng công cụ tikhub tên tiktok_app_v3_fetch_video_comments để lấy bình luận
của video này: [dán đường dẫn video TikTok]

Lấy tối đa 50 bình luận. Rồi làm đúng 3 việc:
1. Lưu kết quả thành file binh-luan-tiktok-goc.md ngay trong thư mục làm việc này.
2. Đánh ID cho từng bình luận theo dạng T01, T02, T03...
3. Bỏ tên tài khoản, ảnh đại diện và đường dẫn trang cá nhân của người bình luận.
   Chỉ giữ nguyên văn câu họ viết, giữ cả lỗi chính tả.

Gọi công cụ đúng MỘT lần. Gọi xong báo lại lấy được bao nhiêu bình luận.
Chưa phân tích gì cả.
```

Dùng khi: cần vài chục mẩu dữ liệu thật trong mười giây. Bài Instagram thì đổi tên công cụ thành `instagram_v3_get_post_comments` và đổi ID thành `I01, I02...`.

**Mỗi lượt gọi tính tiền anh chị trả.** Dịch vụ ghi thẳng "This request will incur a charge".

**A2. Khóa lại, không cho gọi lại tốn phí**

```
Từ giờ dùng dữ liệu trong file binh-luan-tiktok-goc.md đã lưu.
Không gọi lại công cụ tikhub trừ khi tôi yêu cầu rõ ràng.
```

Dùng khi: ngay sau A1. Đây là chỗ tiết kiệm nhiều tiền nhất.

### NHÓM B · Nạp agent và bắt nó tự khai chỗ thiếu

**B1. Cài skill Customer Insight**

```
Tạo file .claude/skills/customer-insight/SKILL.md trong thư mục làm việc này,
tạo luôn thư mục cha nếu chưa có. Nội dung như sau: [dán nội dung vừa copy]
```

Nội dung copy từ [../demo/buoi-02/skill-customer-insight.md](../demo/buoi-02/skill-customer-insight.md), lấy toàn bộ phần trong code block gồm cả ba dấu gạch và hai dòng `name`, `description`. Làm một lần, dùng mãi.

**B2. Bắt agent đếm và khai chỗ dữ liệu không trả lời được**

```
Đọc file data khách hàng trong thư mục này. Trước khi phân tích, làm đúng 3 việc:
1. Đếm và báo lại: tổng bao nhiêu mẩu, chia theo từng loại nguồn.
2. Liệt kê các sản phẩm hoặc dịch vụ xuất hiện trong data.
3. Nói cho tôi biết dữ liệu này KHÔNG trả lời được những câu hỏi nào.

Chưa rút insight vội. Chỉ làm 3 việc trên.
```

Dùng khi: mỗi lần nạp một bộ dữ liệu mới. Agent đếm lệch số mẩu thì dừng lại kiểm file, đừng đi tiếp: đếm sai ở đây là mọi tần suất phía sau sai.

### NHÓM C · Bảng insight

**C1. Ra bảng insight có trích dẫn**

```
Bây giờ phân tích toàn bộ data.

Bước 1: gom các mẩu nói cùng một chuyện vào một nhóm chủ đề. Một mẩu được nằm ở nhiều nhóm nếu nó nói nhiều chuyện.

Bước 2: với mỗi nhóm, viết một pain theo cấu trúc:
[nhóm khách nào] + [lo hoặc muốn điều gì] + [vì sao]

Bước 3: xuất bảng markdown đúng các cột sau, xếp giảm dần theo tần suất:

| # | Pain | Tần suất | Trích dẫn ID | Nguyên văn 1 câu tiêu biểu | Nhãn |

Quy tắc bắt buộc:
- Tần suất ghi dạng "x/[tổng số mẩu]". Cấm dùng: đa số, rất nhiều, phần lớn, hầu hết.
- Cột Trích dẫn ID liệt kê ĐỦ ID đã đếm, không viết tắt kiểu "và các mẩu khác".
- Số ID liệt kê phải khớp đúng với x. Không khớp thì sửa x, không sửa danh sách ID.
- Cột Nguyên văn copy đúng ký tự từ file, không viết lại cho mượt.
- Nhãn ghi [DATA THẬT] hoặc [SUY LUẬN].
```

Dùng khi: đã có tối thiểu 20 mẩu đã đánh ID.

**C2. Sửa khi trích dẫn không khớp nguyên văn**

```
Trích dẫn ở dòng số ... không khớp nguyên văn file gốc.
Rà lại toàn bộ cột Nguyên văn, copy đúng ký tự từ data, không diễn đạt lại.
Dòng nào không tìm được câu gốc thì xóa dòng đó.
```

Dùng khi: Ctrl+F một trích dẫn trong file gốc mà không khớp 100% ký tự.

**C3. Sửa khi agent phóng đại tần suất**

```
Bỏ mọi từ định lượng mơ hồ: đa số, rất nhiều, phần lớn, hầu hết.
Mỗi pain ghi đúng dạng "x/30" và liệt kê đủ ID đã đếm.
Nếu số ID liệt kê không khớp với x thì sửa lại x, không sửa danh sách ID.
```

Dùng khi: bảng xuất hiện chữ "đa số khách", "rất nhiều khách phàn nàn".

**C4. Dựng persona**

```
Từ bảng insight trên, dựng tối đa 3 persona.

Mỗi persona ghi:
- Tên gọi ngắn, đặt theo nỗi lo, không đặt theo tuổi hay nghề nghiệp
- Nỗi lo chính, kèm ID
- Câu họ thật sự đang hỏi trong đầu (trích nguyên văn 1 mẩu)
- Cái họ cần thấy để yên tâm mua
- Sản phẩm hoặc gói phù hợp nhất và lý do

Ràng buộc:
- Không bịa tuổi, nghề, thu nhập, nơi ở. Data không có thì ghi "chưa đủ dữ liệu".
- Mỗi persona phải gắn được tối thiểu 3 ID.
```

Dùng khi: đã có bảng insight tối thiểu 5 dòng.

### NHÓM D · Từ insight ra nội dung

**D1. Năm content angle**

```
Từ bảng insight và 3 persona trên, đề xuất 5 content angle.

Mỗi angle ghi đúng 4 dòng:
- Tên angle (1 câu, viết như tiêu đề khách sẽ đọc)
- Bám pain số mấy, tần suất bao nhiêu
- Trích dẫn ID làm bằng chứng
- Persona nhắm tới

Ràng buộc:
- 5 angle phải bám tối thiểu 4 pain KHÁC NHAU.
- Phép thử trước khi xuất: nếu thay tên thương hiệu tôi bằng tên đối thủ mà angle vẫn dùng được thì loại, viết lại angle khác.
- Đối chiếu mục "Điều KHÔNG được nói" trong hồ sơ sản phẩm của tôi. Không angle nào được hứa mốc thời gian có kết quả.
```

Dùng khi: cần góc nội dung cho tháng tới, bám nỗi đau thật thay vì bám ưu điểm sản phẩm.

**D2. Năm bài social**

```
Viết 5 bài đăng cho kênh chính của tôi, mỗi bài cho một angle ở trên.

Yêu cầu mỗi bài:
- Dài 120 đến 200 chữ
- Câu mở đầu lấy từ chính nỗi lo của khách, không mở bằng lời khen sản phẩm
- Có tối thiểu 1 câu trích nguyên văn khách, ghi rõ trích từ ID nào
- Kết bằng 1 lời mời hành động nhẹ, không giục
- Đúng phần giọng văn và danh sách từ cấm trong file CLAUDE.md của thư mục này

Cấm: hứa mốc thời gian có kết quả, so sánh đích danh thương hiệu khác, và mọi từ trong mục "Điều KHÔNG được nói".

Cuối mỗi bài, xuống dòng ghi: Nguồn insight: pain số ..., ID ...
```

Dùng khi: có 5 angle rồi. Khi đăng thật thì xóa dòng "Nguồn insight" đi.

**D3. Rà từ cấm, bắt buộc chạy trước khi đăng**

```
Rà 5 bài vừa viết, đối chiếu mục "Điều KHÔNG được nói" trong hồ sơ sản phẩm.
Liệt kê từng câu vi phạm kèm số bài, đề xuất câu thay thế.
Không tự sửa. Chỉ liệt kê để tôi duyệt.
```

Dùng khi: trước mỗi lần đăng, mọi buổi, không riêng buổi 2.

### NHÓM E · Hình ảnh

**E1. Ba brief hình ảnh**

```
Viết 3 brief hình ảnh cho 3 bài trong số 5 bài trên. Chọn 3 bài bám 3 pain khác nhau.

Mỗi brief đủ 5 mục:
1. Thông điệp một câu mà người xem phải hiểu trong 2 giây
2. Bố cục (đặt gì ở đâu, chữ chính chiếm bao nhiêu phần)
3. Chữ trên ảnh (tối đa 8 chữ, viết ra chính xác)
4. Màu và tông (bám phần giọng văn trong CLAUDE.md)
5. Điều cấm trong ảnh

Mỗi brief ghi thêm: bám pain số mấy, ID nào.
```

**E2. Ra visual bằng Artifact, chọn khi cần chữ tiếng Việt sắc nét**

```
Từ brief số 1, tạo một Artifact HTML kích thước 1080x1080, hiển thị đúng brief.
Yêu cầu:
- Chữ tiếng Việt có dấu, cỡ chữ chính đủ lớn để đọc trên điện thoại
- Nền phẳng theo tông màu trong brief, không dùng ảnh từ internet
- Toàn bộ nằm gọn trong khung vuông, không tràn
```

**E3. Ra prompt ảnh AI, chọn khi cần ảnh sản phẩm hoặc nền có chất liệu**

```
Từ brief số 1, viết cho tôi 1 prompt tạo ảnh bằng công cụ ảnh AI.
Yêu cầu prompt:
- Mô tả bối cảnh, ánh sáng, góc chụp, tông màu
- KHÔNG có chữ trong ảnh (chữ sẽ chèn sau để đảm bảo tiếng Việt đúng dấu)
Viết prompt bằng tiếng Anh, kèm bản dịch tiếng Việt để tôi kiểm.
```

### NHÓM F · Mang insight ngược về CLAUDE.md

**F1. Lưu bảng insight thành file**

```
Lưu bảng insight, danh sách pain vận hành, 3 persona và 5 content angle vừa làm
thành file insight-khach-hang.md ngay trong thư mục làm việc này.

Giữ nguyên cột Trích dẫn ID và cột Nguyên văn. Không rút gọn, không bỏ ID.
Đầu file ghi 3 dòng: ngày phân tích, tên file data nguồn, tổng số mẩu.
Cuối file giữ nguyên mục "Chỗ còn thiếu dữ liệu".
```

Dùng khi: xong bảng insight. Để rời trong cửa sổ chat là buổi 3 và buổi 4 mất.

**F2. Thay 5 nỗi đau đoán bằng 5 nỗi đau thật**

```
Mở file CLAUDE.md trong thư mục này, tìm mục 5 nỗi đau khách (hoặc mục chân dung
khách). Cả 5 dòng đang gắn nhãn [SUY LUẬN] vì buổi trước tôi chưa có data.

Giờ đọc file insight-khach-hang.md vừa lưu, rồi viết lại mục đó theo đúng quy tắc sau:

1. Mỗi nỗi đau lấy từ bảng insight, ưu tiên theo tần suất giảm dần.
2. Mỗi dòng ghi đủ 4 phần: nỗi đau viết bằng lời khách; tần suất dạng x/tổng;
   danh sách đủ mã trích dẫn; nhãn [DATA THẬT].
3. Kèm một câu nguyên văn khách nói, copy đúng ký tự, đặt trong ngoặc kép.
4. Nỗi đau nào KHÔNG gắn được mã trích dẫn thì GIỮ NGUYÊN nhãn [SUY LUẬN].
   Không đổi nhãn cho đủ 5 dòng.
5. Nỗi đau vận hành (giao hàng, thanh toán, đổi trả) không đưa vào mục này.
   Ghi riêng thành một dòng ở cuối, đánh dấu là việc của bộ phận vận hành.

Trước khi ghi đè, cho tôi xem bảng so sánh 2 cột: bên trái là 5 dòng cũ tôi đoán,
bên phải là dòng mới từ data. Dòng nào tôi đoán trật thì ghi rõ trật ở chỗ nào.
Tôi duyệt xong bạn mới ghi vào file.
```

Dùng khi: mỗi quý, khi có thêm một đợt dữ liệu khách mới. Đọc kỹ bảng so sánh trước khi bấm duyệt, đây là chỗ đáng tiền nhất của buổi.

---

## 3. Sản phẩm buổi 2 anh chị phải có trên máy

| # | Sản phẩm | Nằm ở đâu |
|---|---|---|
| 1 | Skill Customer Insight | `.claude/skills/customer-insight/SKILL.md` trong thư mục làm việc |
| 2 | File dữ liệu khách đã đánh ID | Trong thư mục làm việc. Chưa có data thật thì dùng [../demo/thao-an/review-va-tin-nhan-khach.md](../demo/thao-an/review-va-tin-nhan-khach.md) |
| 3 | `insight-khach-hang.md`: bảng insight, pain vận hành, 3 persona, 5 angle | Ngay trong thư mục làm việc, cạnh `CLAUDE.md` |
| 4 | 5 bài social, mỗi bài có 1 câu trích nguyên văn khách | Trong thư mục làm việc |
| 5 | 3 brief hình ảnh và 3 visual mở xem được | Trong thư mục làm việc |
| 6 | `CLAUDE.md` đã cập nhật mục 5 nỗi đau, có mã trích dẫn và tần suất | Ngay trong thư mục làm việc |
| 7 | `binh-luan-tiktok-goc.md`, chỉ ai dùng tikhub | Trong thư mục làm việc |

---

## 4. Checklist tự kiểm

- [ ] Bảng insight có tối thiểu 5 dòng, mỗi dòng tối thiểu 2 ID, không dòng nào trống cột trích dẫn
- [ ] Tần suất ghi dạng x trên tổng, không còn chữ "đa số", "rất nhiều", "phần lớn"
- [ ] Tự Ctrl+F kiểm 3 trích dẫn ngẫu nhiên, cả 3 khớp nguyên văn từng ký tự
- [ ] Có ít nhất 1 chỗ agent ghi "chưa đủ dữ liệu". Bảng điền kín không chỗ nào thiếu là dấu hiệu agent đang bịa
- [ ] Đã tách riêng pain vận hành (giao hàng, thanh toán, đổi trả) ra khỏi pain ra nội dung
- [ ] Tối đa 3 persona, mỗi persona gắn tối thiểu 3 ID, không persona nào có tuổi hay nghề bịa ra
- [ ] Đủ 5 angle, bám tối thiểu 4 pain khác nhau, không angle nào thay được tên thương hiệu mà vẫn đúng
- [ ] Đủ 5 bài social, mỗi bài có tối thiểu 1 câu trích nguyên văn khách, đã chạy prompt D3 rà từ cấm
- [ ] Đủ 3 brief đủ 5 mục và 3 visual mở xem được, chữ tiếng Việt không tràn khung
- [ ] Đã lưu `insight-khach-hang.md` vào thư mục làm việc
- [ ] Trong `CLAUDE.md`: không còn dòng nào gắn `[DATA THẬT]` mà cột mã trích dẫn để trống

---

## 5. Việc làm ở nhà trước buổi 3

| # | Việc | Nộp gì | Hạn |
|---|---|---|---|
| 1 | Chạy lại agent trên một đợt dữ liệu khác của mình, ví dụ inbox 30 ngày gần nhất. So bảng insight lần 2 với lần 1 | Hai bảng insight, ghi chú pain nào đổi thứ hạng | Trước buổi 3 |
| 2 | Lấp ba chỗ dữ liệu agent nói là KHÔNG trả lời được: nghĩ ra câu hỏi thêm vào form hoặc kịch bản inbox để tháng sau có số | Danh sách 3 câu hỏi mới | Trước buổi 3 |
| 3 | Đăng thử 1 trong 5 bài social lên kênh thật của mình, xem bình luận về nói gì | Ảnh chụp bài và bình luận | Trước buổi 3 |
| 4 | **Chuẩn bị cho buổi 3:** danh sách 10 lead đủ 6 cột (tên cơ sở, loại hình, khu vực, kênh liên hệ, người phụ trách, ghi chú trao đổi nguyên văn). Lead nào thiếu thông tin thì **để trống**, không điền bừa | File 10 lead trong thư mục làm việc | Trước buổi 3 |
| 5 | **Chuẩn bị cho buổi 3:** bảng chính sách giá sỉ (chiết khấu theo số lượng, thanh toán, vận chuyển) và danh sách **điều chưa có chính sách**, tối thiểu 5 dòng | File chính sách giá trong thư mục làm việc | Trước buổi 3 |

Chưa có lead thật thì chép [../demo/thao-an/danh-sach-lead-si.md](../demo/thao-an/danh-sach-lead-si.md) và [../demo/thao-an/chinh-sach-gia-si.md](../demo/thao-an/chinh-sach-gia-si.md) vào thư mục làm việc, vẫn hoàn thành đủ 7 sản phẩm buổi 3.

---

## 6. Năm lỗi hay gặp khi làm lại ở nhà

| Lỗi | Dấu hiệu anh chị thấy | Cách xử lý |
|---|---|---|
| Dữ liệu quá ít | Bảng insight chỉ ra 2 tới 3 dòng, tần suất toàn 1 trên 12 | Gộp thêm nguồn: bình luận bài viết, tin nhắn cũ, review sàn khác. Vẫn thiếu thì chạy hai lượt: lượt một trên bộ Thảo An để nắm tay, lượt hai trên data của mình |
| Dữ liệu toàn khen, không có chê | Shop mới hoặc shop có lọc review | **Câu hỏi trước mua chính là pain.** Người hỏi "có cồn không" đang lo dị ứng. Chuyển trọng tâm sang tin nhắn và bình luận. Đọc review 4 sao thay vì 5 sao, chỗ chê nằm ở đó |
| Agent bịa trích dẫn theo kiểu tinh vi | ID có thật, nhưng câu trích bị viết mượt lại cho hay | Copy đoạn agent trích, Ctrl+F trong file gốc. Không khớp 100% ký tự là hỏng. Chạy prompt C2. Agent làm mượt câu chê của khách là đang làm hỏng bằng chứng |
| Nhầm pain vận hành với pain nội dung | Trong 5 angle có một angle về giao hàng nhanh | Chia bảng insight làm hai nhóm ngay từ đầu. Giao chậm thì chuyển cho bộ phận vận hành, không viết bài. Viết bài xin lỗi về giao hàng là tự làm yếu thương hiệu |
| Năm angle thật ra là một angle viết năm kiểu | Cả 5 đều xoay quanh "lành tính, an toàn" | Ép mỗi angle map tới một pain khác nhau. Pain số 1 mạnh nhất thì cho phép 2 angle, còn lại mỗi pain một angle. Chạy lại D1 |

---

CES Global · Creative, Effective, Sustainable
