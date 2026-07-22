# Buổi 6 · Workbook học viên

**Bạn có 65 phút.** Chia làm 3 chặng: 18 phút gom tài sản, 29 phút viết và thử Skill, 18 phút viết Playbook và kế hoạch 14 ngày.

**Nộp cuối buổi 6 thứ:** 1 Claude Skill · 1 AI Agent Playbook · 1 bộ tài sản sắp xếp theo project · 1 automation hoặc prototype · 1 demo 5 phút · 1 kế hoạch 14 ngày.

Chưa có dữ liệu thật thì dùng bộ Thảo An trong [../demo/thao-an/](../demo/thao-an/), vẫn nộp đủ 6 sản phẩm. Mẫu Skill hoàn chỉnh để đối chiếu nằm ở [../demo/buoi-06/skill-dong-goi-va-playbook.md](../demo/buoi-06/skill-dong-goi-va-playbook.md), bí chỗ nào thì mở ra xem cách viết.

---

## CHẶNG 1 · Gom tài sản 5 buổi (18 phút)

### 1.1 Đối chiếu đủ hay thiếu

Đánh dấu vào cột trạng thái. Thiếu thì ghi vào cột cuối cách xử lý: chạy lại prompt, hay dùng bản Thảo An thay thế.

| Buổi | Đầu ra | Số lượng | Có | Thiếu | Xử lý |
|---|---|---|---|---|---|
| 1 | Thư mục làm việc, mở được bằng tab Code | 1 | ☐ | ☐ | |
| 1 | `CLAUDE.md` (câu định vị · 3 thông điệp · 5 nỗi đau · giọng văn · từ cấm) · hồ sơ sản phẩm | 1 · 1 | ☐ | ☐ | |
| 1 | Memory đã bật · skill `viet-bai-ban-hang` chạy được · kết nối MCP | 1 · 1 · 1 | ☐ | ☐ | |
| 1 | Hook · CTA · bài viết bán hàng | 10 · 10 · 3 | ☐ | ☐ | |
| 2 | Bảng insight có trích dẫn · persona | 1 · 1 | ☐ | ☐ | |
| 2 | Content angle · bài social | 5 · 5 | ☐ | ☐ | |
| 2 | Brief hình ảnh · visual đã sản xuất | 3 · 3 | ☐ | ☐ | |
| 3 | Lead scoring | 10 lead | ☐ | ☐ | |
| 3 | Email · tin nhắn | 10 · 10 | ☐ | ☐ | |
| 3 | Kịch bản gọi 5 phút · kịch bản xử lý từ chối · proposal nháp | 1 · 10 · 1 | ☐ | ☐ | |
| 4 | Campaign brief · lịch 14 ngày | 1 · 1 | ☐ | ☐ | |
| 4 | Bài social · email nurturing | 10 · 3 | ☐ | ☐ | |
| 4 | Landing page section · video script · carousel | 1 bộ · 3 · 1 | ☐ | ☐ | |
| 4 | Brief hình ảnh | 5 | ☐ | ☐ | |
| 5 | Automation map · bảng quản lý | 1 · 1 | ☐ | ☐ | |
| 5 | Luồng post bài chạy được · mẫu thông báo | 1 · 1 bộ | ☐ | ☐ | |
| 5 | Checklist kiểm soát rủi ro | 1 | ☐ | ☐ | |

### 1.2 Tạo cấu trúc thư mục

Tạo trên máy, thư mục gốc đặt theo tên thương hiệu của bạn: `ten-thuong-hieu-ai-system/`. Bên trong đúng 8 nhánh đánh số để giữ thứ tự:

`00-doc-truoc/` (playbook.md và ke-hoach-14-ngay.md) · `01-nen-tang/` buổi 1 · `02-khach-hang/` buổi 2 · `03-ban-hang/` buổi 3 · `04-chien-dich/` buổi 4 · `05-tu-dong-hoa/` buổi 5 · `06-skill/` (bản skill để đọc và `tham-chieu/`) · `99-luu-tru/` bản nháp cũ.

**Hai thứ nằm NGOÀI 8 nhánh đó, để ngay ở gốc thư mục:** file `CLAUDE.md`, và thư mục `.claude/skills/` chứa skill chạy thật. Đây là hai chỗ Claude tự đọc, gói vào thư mục đánh số là nó không thấy nữa. Đừng tạo tay thư mục `.claude`, Windows ẩn nó đi và dễ gõ sai. Bảo Claude tạo.

Đổi tên file theo quy tắc: chữ thường, nối bằng gạch nối, nói rõ nội dung. Bỏ hết chữ "final", "moi", "v2".

☐ Đã tạo đủ 8 thư mục đánh số ☐ `CLAUDE.md` và `.claude/skills/` nằm ở gốc ☐ Đã chuyển hết file vào đúng chỗ ☐ Đã đổi tên file theo quy tắc ☐ Mở ra tìm được phần giọng văn và từ cấm trong 10 giây

---

## CHẶNG 2 · Viết và thử Skill (29 phút)

Làm đúng thứ tự 5 bước. Copy prompt, dán vào ô nhập của tab **Code**, đang mở đúng thư mục làm việc của bạn. Sửa phần trong ngoặc vuông.

### Bước 1 · Rút quy trình đang làm bằng tay (5 phút)

```
Trong thư mục làm việc này, 5 buổi qua tôi đã dựng cho thương hiệu
[TÊN THƯƠNG HIỆU]: nền dữ liệu trong CLAUDE.md và hồ sơ sản phẩm,
skill viet-bai-ban-hang, rồi 5 agent là Customer Insight, Content Engine,
Outbound, Proposal, Closer, cộng một luồng tự động hóa.

Hãy đọc các file system prompt và các đầu ra tôi đã lưu trong thư mục này,
rồi rút ra quy trình tôi đang làm bằng tay, viết dưới dạng các bước đánh số.

Mỗi bước ghi rõ: tên bước, đầu vào cần gì, việc làm (dùng động từ,
không dùng tính từ), đầu ra cụ thể đếm được, và bước nào bắt buộc
người duyệt trước khi đi tiếp.

Chỗ nào không đủ dữ liệu để rút ra thì ghi "chưa đủ dữ liệu",
đừng suy đoán quy trình giúp tôi.
```

Chép lại các bước ra đây, đây là xương sống của Skill:

| # | Tên bước | Đầu vào | Đầu ra | Ai duyệt |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |
| 5 | | | | |
| 6 | | | | |

### Bước 2 · Viết tiêu chuẩn đầu ra bằng số (5 phút)

Đây là chỗ hầu hết mọi người bỏ qua, và cũng là chỗ khiến Skill của người khác dùng không ra kết quả. Không dùng tính từ. Mỗi dòng phải kiểm được bằng mắt.

| Loại đầu ra | Đạt khi (viết bằng số hoặc câu kiểm được) |
|---|---|
| Bài social | |
| Tin nhắn tư vấn | |
| Email chào hàng | |
| Proposal | |
| Brief hình ảnh | |

Ví dụ đúng cho bài social Thảo An: "dưới 250 chữ, mở bằng một tình huống da cụ thể, tối đa 2 emoji, có đúng 1 CTA ở cuối, không chứa từ trong danh sách cấm, mọi số liệu có nhãn nguồn."
Ví dụ sai: "bài viết hấp dẫn, đúng giọng thương hiệu."

### Bước 3 · Viết ranh giới không được vượt (4 phút)

| Loại ranh giới | Nội dung cụ thể |
|---|---|
| Từ cấm dùng | |
| Điều không được cam kết | |
| Số liệu không được tự chế | |
| Việc agent không được tự quyết | |
| Việc bắt buộc người làm | |

### Bước 4 · Sinh Skill (7 phút)

Bạn không viết lại từ đầu. Bạn nâng cấp skill đã có ở buổi 1. Cách viết file, frontmatter, dòng `description`: buổi 1 làm rồi, đừng học lại. Bốn mục **Vai trò**, **Tiêu chuẩn đầu ra cho từng loại**, **Ranh giới không được vượt**, **Xử lý khi thiếu dữ liệu** mới là phần mới, và cũng là phần bạn vừa điền ở Bước 2 và Bước 3.

```
Mở file .claude/skills/viet-bai-ban-hang/SKILL.md tôi đã viết ở buổi 1
để xem lại cách tôi viết skill.

Bây giờ tạo cho tôi một skill mới, rộng hơn, phủ cả quy trình và tiêu chuẩn
ở trên. Đường dẫn: .claude/skills/[TEN-SKILL-MOI]/SKILL.md

Frontmatter viết theo đúng kiểu file cũ. Riêng dòng description phải rộng hơn:
liệt kê rõ từng loại yêu cầu sẽ kích hoạt skill này, viết y như những chữ
tôi thật sự sẽ gõ. Nêu luôn một tình huống KHÔNG dùng skill này.

Phần thân gồm đúng 7 mục sau. Bốn mục đầu là phần file cũ chưa có:

1. Vai trò: skill này đóng vai ai, tả bằng một ví von nghề nghiệp, kèm quy tắc
   xưng hô lấy từ CLAUDE.md.
2. Nguồn dữ liệu: liệt kê tên từng file nền trong thư mục này, ghi rõ file nào
   là nguồn sự thật cho giá, cho giọng văn, cho lời khách nói.
3. Tiêu chuẩn đầu ra: viết riêng cho TỪNG loại đầu ra. Dùng đúng bảng tôi đã
   điền ở trên. Mỗi dòng là con số hoặc câu kiểm được bằng mắt, không tính từ.
4. Ranh giới không được vượt: dùng đúng bảng ranh giới tôi đã điền ở trên.
5. Quy trình từng bước: mỗi bước một việc, viết bằng động từ, ghi rõ đầu vào
   và đầu ra. Bước cuối là tự soát trước khi trả về.
6. Xử lý khi thiếu dữ liệu: gặp chỗ trống thì làm gì, theo thứ tự nào.
7. File tham chiếu: liệt kê đúng tên và đúng đường dẫn các file nền.

Ba nguyên tắc chống bịa đang nằm trong CLAUDE.md của thư mục này: chép nguyên
văn sang phần thân skill, không diễn đạt lại, không rút gọn.
```

### Bước 5 · Thử Skill trên yêu cầu mới (8 phút)

**Đây là bước quan trọng nhất buổi hôm nay. Bỏ bước này thì đừng nộp bài.**

Mở phiên trò chuyện MỚI trong tab Code, vẫn ở thư mục làm việc đó. Gõ 2 yêu cầu chưa từng làm trong 5 buổi, khác luồng nhau. **Không gọi tên skill trong prompt.** Nếu dòng `description` viết đúng thì Claude phải tự rút skill ra; không rút ra được thì lỗi nằm ở dòng đó. Gợi ý yêu cầu: nội dung cho một dịp mới (hội chợ, khai trương); câu hỏi khó của khách mà dữ liệu không có sẵn; kênh mới (TikTok, Zalo OA, tờ rơi in); nhóm khách mới (doanh nghiệp, đại lý tỉnh).

Phép thử 1, yêu cầu tôi đưa: ______________________________________________

Phép thử 2, yêu cầu tôi đưa: ______________________________________________

| Kiểm | Thử 1 đạt | Thử 2 đạt | Ghi chú |
|---|---|---|---|
| Claude tự gọi skill ra dù tôi không nhắc tên | ☐ | ☐ | |
| Đúng giọng thương hiệu, xưng hô đúng | ☐ | ☐ | |
| Không chứa từ cấm | ☐ | ☐ | |
| Có nhãn `[DATA THẬT]` và `[SUY LUẬN]` | ☐ | ☐ | |
| Gặp chỗ trống thì ghi "chưa đủ dữ liệu", không bịa | ☐ | ☐ | |
| Ghi rõ đây là nháp, cần người duyệt | ☐ | ☐ | |
| Đạt tiêu chuẩn đầu ra tôi viết ở Bước 2 | ☐ | ☐ | |

Có ô nào chưa đạt thì sửa Skill rồi chạy lại. Ghi lại đã sửa gì:

Sửa lần 1: ______________________ Sửa lần 2: ______________________

---

## CHẶNG 3 · Playbook và kế hoạch 14 ngày (18 phút)

### 3.1 Khung AI Agent Playbook

Đây là tài liệu cho NGƯỜI đọc, khác Skill là tài liệu cho Claude đọc. Lưu vào `00-doc-truoc/playbook.md`.

**Mục đích.** Giải bài toán gì, cho ai, thay việc nào đang làm tay: ______________________

**Ai dùng.** Vị trí nào, cần biết gì trước, không cần biết gì: ______________________

**Quy trình từng bước.**

| # | Bước | Mở cái gì | Làm gì | Kết quả có được |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |
| 5 | | | | |
| 6 | | | | |

**Tiêu chuẩn đầu ra.** Chép bảng ở Bước 2 chặng 2 sang. Người duyệt nhìn vào đây để quyết gửi hay sửa.

**Ranh giới không được vượt.** Chép bảng ở Bước 3 chặng 2 sang.

**Chỉ số đo.** Chọn 3 chỉ số quá trình cho tuần 1 và 2 chỉ số kinh doanh cho sau tuần 4.

| Chỉ số | Đo bằng cách nào | Hiện tại | Mục tiêu sau 14 ngày |
|---|---|---|---|
| Thời gian làm 1 đầu ra | | | |
| Số đầu ra mỗi tuần | | | |
| Tỉ lệ nháp duyệt ngay lần đầu | | | |
| | | | |
| | | | |

**Xử lý khi agent ra sai.** Ba mức, ghi rõ ai làm gì:

| Mức | Dấu hiệu | Làm gì | Ai xử lý |
|---|---|---|---|
| 1 · Nhẹ | Lệch giọng, sai độ dài | | |
| 2 · Vừa | Thiếu nhãn nguồn, thiếu dữ liệu nền | | |
| 3 · Nặng | Bịa số liệu, vượt điều cấm nói | | |

### 3.2 Kế hoạch triển khai 14 ngày

Cột "Ai làm" phải ghi tên người thật. Cột "Kết quả cần thấy" phải nhìn vào là biết xong hay chưa.

| Ngày | Việc | Ai làm | Kết quả cần thấy |
|---|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |
| 4 | | | |
| 5 | | | |
| 6 | | | |
| **7** | **Mốc kiểm tuần 1** | | Đủ 3 chỉ số quá trình, có số cụ thể |
| 8 | | | |
| 9 | | | |
| 10 | | | |
| 11 | | | |
| 12 | | | |
| 13 | | | |
| **14** | **Mốc kiểm tuần 2 và quyết mở rộng** | | So 3 chỉ số với ngày 7, quyết giữ hay đổi |

Nguyên tắc xếp lịch: tuần 1 chạy thử trên số ít và sửa Skill; tuần 2 mới tăng số lượng. Ngày 1 và ngày 2 phải là việc làm được ngay chiều nay hoặc sáng mai.

### 3.3 Chuẩn bị demo 5 phút

Viết ra trước, đừng ứng khẩu. Bấm giờ tập 1 lần.

| Phút | Nội dung | Tôi sẽ nói |
|---|---|---|
| 1 | **Bài toán.** Trước mất bao lâu, ai làm, đau ở đâu. Phải có con số | |
| 2 | **Cách làm.** Hệ thống gồm gì, mấy bước. Mở sơ đồ, chỉ nhanh | |
| 3 | **Chạy thử.** Yêu cầu tôi sẽ gõ trực tiếp trước mặt người xem | |
| 4 | **Kết quả.** Đầu ra tôi sẽ đọc to, chỉ ra nhãn nguồn | |
| 5 | **Kế hoạch tiếp.** 14 ngày, ai làm, chỉ số nào | |

Ba điều cấm trong demo:
- Cấm đọc từng dòng system prompt hay Skill.
- Cấm chiếu kết quả chuẩn bị sẵn thay cho chạy thật.
- Cấm kết bằng "em xong rồi ạ". Kết bằng con số và ngày 1 của kế hoạch.

### 3.4 Chấm chéo

Người cùng nhóm chấm bạn. Thang 2 điểm mỗi tiêu chí, tổng 12. Từ 10 trở lên là đạt.

| # | Tiêu chí | Điểm | Người chấm ghi chú |
|---|---|---|---|
| 1 | Bài toán rõ, có con số trước và sau | /2 | |
| 2 | Skill chạy được thật, ngay tại chỗ | /2 | |
| 3 | Đầu ra cụ thể, thay tên thương hiệu là sai ngay | /2 | |
| 4 | Ba nguyên tắc chống bịa nằm trong Skill | /2 | |
| 5 | Playbook đủ 7 mục, người lạ đọc là làm được | /2 | |
| 6 | Kế hoạch 14 ngày có tên người và chỉ số | /2 | |
| | **Tổng** | **/12** | |

---

## Checklist tự kiểm trước khi nộp

**Skill**
☐ File nằm đúng chỗ: `.claude/skills/<tên-skill>/SKILL.md` ngay trong thư mục làm việc
☐ Frontmatter đủ 2 trường `name` và `description`, dòng `description` kể đủ các loại đầu ra và nêu một tình huống KHÔNG dùng
☐ Phần thân đủ 7 mục: Vai trò, Nguồn dữ liệu, Tiêu chuẩn đầu ra, Ranh giới, Quy trình từng bước, Xử lý khi thiếu dữ liệu, File tham chiếu
☐ Ba nguyên tắc chống bịa nằm nguyên văn trong phần thân, không chỉ nằm trong `CLAUDE.md`
☐ Tiêu chuẩn đầu ra viết bằng số, có chuẩn riêng cho từng loại đầu ra, không còn tính từ kiểu "hay", "hấp dẫn"
☐ Đã chạy 2 phép thử ngoài bối cảnh gốc mà không nhắc tên skill, cả 2 đều đạt

**Playbook**
☐ Đủ 7 mục, không mục nào bỏ trống, nhất là tiêu chuẩn đầu ra và ranh giới
☐ Có 3 chỉ số quá trình, mỗi chỉ số ghi rõ cách đo
☐ Bảng xử lý khi agent ra sai có ghi tên người

**Bộ tài sản và automation**
☐ Đủ 8 thư mục đánh số, không còn file tên kiểu "final", "moi", "v2"
☐ `CLAUDE.md` và thư mục `.claude/skills/` nằm ngay ở gốc, không bị gói vào thư mục đánh số
☐ Đã có `00-doc-truoc/playbook.md` và `00-doc-truoc/ke-hoach-14-ngay.md`
☐ Luồng buổi 5 vẫn chạy được, có bước người duyệt trước khi đăng hoặc gửi

**Kế hoạch 14 ngày và demo**
☐ Đủ 14 dòng, cột "Ai làm" ghi tên người thật, không ghi "team"
☐ Ngày 7 và ngày 14 có mốc kiểm chỉ số; ngày 1 làm được trong 24 giờ tới
☐ Đã tập demo 1 lần có bấm giờ, đã được chấm chéo từ 10 điểm trở lên

---

CES Global · Creative, Effective, Sustainable
