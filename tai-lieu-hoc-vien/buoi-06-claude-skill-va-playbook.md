# Tài liệu học viên · Buổi 6: Claude Skill và Playbook

**Khóa:** AI Agent cho Sale & Marketing · CES Global
**Buổi:** 6 trên 6 · 150 phút · **Ngày học:** ______

Đây là bản mang về để tra và làm lại. Bản làm trong lớp là [../workbook/buoi-06-claude-skill-va-playbook.md](../workbook/buoi-06-claude-skill-va-playbook.md). Mẫu Skill hoàn chỉnh để đối chiếu nằm ở [../demo/buoi-06/skill-dong-goi-va-playbook.md](../demo/buoi-06/skill-dong-goi-va-playbook.md), bí chỗ nào thì mở ra xem cách viết. Bảng đối chiếu tài sản của cả sáu buổi nằm ở [checklist-toan-khoa.md](checklist-toan-khoa.md).

---

## 1. Buổi này anh chị đã làm gì

Buổi cuối không tạo dữ liệu mới. Nó gom cái đã có thành thứ người khác cầm lên dùng được.

- Gom tài sản 5 buổi vào một cấu trúc thư mục 8 nhánh đánh số, đổi tên file theo quy tắc.
- Rút quy trình đang làm bằng tay thành các bước đánh số, mỗi bước ghi rõ đầu vào, đầu ra, ai duyệt.
- Viết tiêu chuẩn đầu ra bằng số cho từng loại đầu ra, và viết ranh giới không được vượt.
- Nâng skill viết ở buổi 1 thành một Skill đủ 7 mục, có ba nguyên tắc chống bịa nguyên văn trong phần thân.
- Thử Skill trên hai yêu cầu chưa từng chạy trong khóa, trong một phiên trò chuyện mới, không gọi tên skill.
- Viết AI Agent Playbook 7 mục và kế hoạch triển khai 14 ngày, rồi trình bày 5 phút và chấm chéo.

**`CLAUDE.md` là hồ sơ của một thương hiệu. `SKILL.md` là quy trình mang đi được.** Đổi thương hiệu là viết lại `CLAUDE.md` từ đầu. Còn Skill thì gói lại rồi mang sang thương hiệu nào cũng chạy. Một agency có 8 khách hàng thì có 8 thư mục làm việc và 8 file `CLAUDE.md`, nhưng chỉ cần một bộ skill dùng chung.

**Từ hôm nay ba nguyên tắc chống bịa nằm trong Skill, không nằm trong trí nhớ.** Trí nhớ không bàn giao được. Người mới vào công ty cầm Skill của anh chị lên chạy thì họ cũng có đủ ba nguyên tắc đó, dù chưa từng học khóa này.

---

## 2. Bộ prompt copy dùng ngay

### NHÓM A · Gom tài sản và rút quy trình

**A1. Đề xuất cấu trúc thư mục cho cả bộ tài sản**

```
Tôi vừa hoàn thành 5 buổi xây hệ thống AI Sale & Marketing cho [TÊN THƯƠNG HIỆU].
Các đầu ra tôi đang có:

Buổi 1: thư mục làm việc, file CLAUDE.md (câu định vị, 3 thông điệp, 5 nỗi đau,
giọng văn, danh sách từ cấm), hồ sơ sản phẩm, Memory đã bật, skill
viet-bai-ban-hang, 3 bài bán hàng, 10 hook, 10 CTA, 1 kết nối MCP.
Buổi 2: bảng insight có trích dẫn, persona, 5 content angle, 5 bài social,
3 brief hình ảnh, 3 visual.
Buổi 3: lead scoring 10 lead, 10 email, 10 tin nhắn, kịch bản gọi 5 phút,
10 kịch bản xử lý từ chối, proposal nháp.
Buổi 4: campaign brief, lịch 14 ngày, 10 bài social, 3 email nurturing,
landing page section, 3 video script, carousel, 5 brief hình ảnh.
Buổi 5: automation map, bảng quản lý, luồng post bài, mẫu thông báo,
checklist kiểm soát rủi ro.

Hãy đề xuất cấu trúc thư mục để một người mới vào công ty mở ra là tìm được
trong 10 giây. Yêu cầu:
- Giữ nguyên file CLAUDE.md và thư mục .claude/skills/ ở ngay gốc thư mục làm
  việc. Đây là hai chỗ Claude tự đọc, không được gói vào thư mục đánh số.
- Các thư mục còn lại đánh số đầu để giữ thứ tự.
- Tên file chữ thường, nối bằng gạch nối, nói rõ nội dung.
- Có một thư mục "đọc trước" chứa tài liệu người mới phải đọc đầu tiên.
- Có chỗ chứa bản nháp cũ, không xóa nhưng không lẫn vào bản đang dùng.
Trả về dạng cây thư mục, kèm 1 dòng giải thích mỗi thư mục.
```

Dùng khi: ngay khi mở thư mục trống. Cấu trúc lớp đã dùng, để đối chiếu:

```
<ten-thuong-hieu>-ai-system/
├── CLAUDE.md         hồ sơ thương hiệu, Claude tự đọc trước mọi việc
├── .claude/skills/   nơi skill chạy thật, mỗi skill một thư mục con
├── 00-doc-truoc/     playbook.md · ke-hoach-14-ngay.md
├── 01-nen-tang/      san-pham · hook-cta · bai-ban-hang-mau
├── 02-khach-hang/    insight-khach-hang · persona · content-angle
├── 03-ban-hang/      bang-diem-lead · email-va-tin-nhan · kich-ban-goi-va-tu-choi · proposal-mau
├── 04-chien-dich/    campaign-brief · lich-14-ngay · noi-dung-da-kenh/
├── 05-tu-dong-hoa/   automation-map · luong-post-bai · checklist-rui-ro
├── 06-skill/         ban-doc-SKILL.md · tham-chieu/ (mẫu, checklist, dữ liệu nền)
└── 99-luu-tru/       bản nháp cũ, không xóa nhưng không dùng
```

**Bốn quy tắc đặt tên:** đánh số đầu thư mục; tên file chữ thường nối bằng gạch nối; không dùng chữ "final", "moi", "v2"; bản cũ đẩy vào `99-luu-tru/`. Thư mục bắt đầu bằng dấu chấm bị Windows ẩn đi, đừng tạo tay, bảo Claude tạo.

**A2. Rút quy trình đang làm bằng tay thành các bước**

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

Dùng khi: trước khi viết Skill, mỗi lần quy trình của anh chị đổi. Kết quả thường ra 5 tới 7 bước. **Nhìn kỹ bước duyệt.** Bước duyệt phải nằm trong quy trình, không nằm trong lời hứa. Cái gì không viết vào quy trình thì lúc gấp là bỏ qua đầu tiên.

### NHÓM B · Viết Skill và thử Skill

**B1. Sinh Skill từ quy trình vừa rút**

Anh chị không viết lại từ đầu. Anh chị nâng cấp skill đã có ở buổi 1.

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

Dùng khi: mỗi lần đóng gói một bộ việc mới, hoặc nhận thêm một khách hàng. **Trước khi chạy prompt này, anh chị phải có sẵn hai bảng:** bảng tiêu chuẩn đầu ra viết bằng số cho từng loại, và bảng ranh giới. Hai bảng đó nằm ở Bước 2 và Bước 3 chặng 2 của workbook. Không có hai bảng đó thì Skill sinh ra vẫn chung chung.

Phép thử một câu: đưa Skill cho người mới vào công ty tuần đầu, họ chạy ra kết quả anh chị dám gửi khách không. Không thì Skill chưa xong.

**B2. Thử Skill trên yêu cầu mới, không bỏ bước này**

Cách chạy: mở một phiên trò chuyện **mới** trong tab Code, vẫn ở thư mục làm việc đó. Phiên cũ còn nhớ hết bối cảnh vừa nói, chạy trong đó là tự lừa mình. Gõ thẳng yêu cầu như người dùng thật sẽ gõ, **không nhắc tên skill**. Dòng `description` viết đúng thì Claude phải tự rút skill ra; không tự rút ra được thì lỗi nằm ở dòng đó, không phải ở phần thân.

Chạy đúng hai phép thử, khác luồng nhau. Gợi ý chọn đề: một dịp mới (hội chợ, khai trương); một câu hỏi khó mà dữ liệu không có sẵn; một kênh mới (TikTok, Zalo OA, tờ rơi in); một nhóm khách mới (doanh nghiệp, đại lý tỉnh).

Hai đề lớp đã chạy trên case Thảo An, để anh chị thấy dạng đề:

```
Tuần sau Thảo An có gian hàng ở hội chợ mỹ phẩm.
Soạn cho tôi:
- 1 tờ rơi A5 phát tại gian hàng, cho khách lẻ.
- 1 kịch bản chào 60 giây khi khách dừng lại xem.
- 1 tin nhắn gửi lại cho khách đã để số điện thoại, gửi sau hội chợ 2 ngày.
```

```
Một spa ở Đà Nẵng nhắn hỏi: "Bên em nhập sỉ 50 chai serum thì giá bao nhiêu,
có hỗ trợ tư vấn cho nhân viên spa không?"
Soạn tin nhắn trả lời.
```

Dùng khi: sau mỗi lần sửa Skill, và trước mỗi lần đưa Skill cho người khác. Bảy ô phải đạt ở cả hai phép thử: Claude tự gọi skill; đúng giọng và xưng hô; không chứa từ cấm; có nhãn `[DATA THẬT]` và `[SUY LUẬN]`; gặp chỗ trống thì ghi "chưa đủ dữ liệu"; ghi rõ đây là nháp cần người duyệt; đạt đúng bảng tiêu chuẩn đầu ra do chính anh chị viết.

**Ô nào chưa đạt thì sửa Skill rồi chạy lại, không sửa kết quả.** Skill hiếm khi đúng ngay lần đầu. Nó đúng sau vòng thử thứ hai hoặc thứ ba.

### NHÓM C · Playbook và kế hoạch 14 ngày

**C1. Bảy mục bắt buộc của Playbook**

Skill là thứ Claude đọc. Playbook là thứ người đọc. Lưu vào `00-doc-truoc/playbook.md`. Thiếu mục nào thì người dùng sẽ quay lại hỏi anh chị đúng mục đó.

| Mục | Trả lời câu hỏi | Viết bao nhiêu là đủ |
|---|---|---|
| Mục đích | Hệ thống này giải bài toán gì, thay việc nào đang làm tay | 2 tới 3 dòng |
| Ai dùng | Vị trí nào, cần biết gì trước, không cần biết gì | 2 dòng |
| Quy trình từng bước | Mở cái gì, gõ gì, làm gì tiếp | Bảng, mỗi bước ghi đầu vào và đầu ra |
| Tiêu chuẩn đầu ra | Thế nào là đạt | Chép nguyên bảng đã viết trong Skill |
| Ranh giới không được vượt | Cấm gì, không được tự quyết gì | Chép nguyên bảng đã viết trong Skill |
| Chỉ số đo | Nhìn vào đâu biết hệ thống có tác dụng | 3 chỉ số quá trình, 2 chỉ số kinh doanh |
| Xử lý khi agent ra sai | Sai thì làm gì, ai làm | Ba mức: sửa prompt; bổ sung dữ liệu; dừng và báo người phụ trách |

Hai mục hay bị bỏ nhất là tiêu chuẩn đầu ra và ranh giới. Thiếu chúng thì người dùng chạy xong không biết nên gửi hay nên sửa. Câu hỏi để tự soát: **ai là người bấm nút duyệt, và họ nhìn vào đâu để quyết.** Câu trả lời chính là tiêu chuẩn cần viết.

**C2. Lập kế hoạch triển khai 14 ngày**

```
Lập kế hoạch triển khai 14 ngày để đưa hệ thống này vào chạy thật tại
[TÊN THƯƠNG HIỆU].

Bối cảnh: đội có [SỐ] người. [Ghi rõ ai phụ trách việc gì].
Mục tiêu đang chạy là [MỤC TIÊU VIẾT BẰNG CON SỐ].

Trả về bảng 4 cột: Ngày | Việc | Ai làm | Kết quả cần thấy.

Ràng buộc:
- Cột "Kết quả cần thấy" phải là thứ nhìn vào biết ngay đã xong hay chưa,
  không viết kiểu "hoàn thiện quy trình".
- Tuần 1 tập trung chạy thử trên số ít và sửa Skill. Tuần 2 mới mở rộng.
- Ngày 7 và ngày 14 phải có mốc kiểm, ghi rõ nhìn vào chỉ số nào.
- Ba chỉ số theo dõi bắt buộc: thời gian làm 1 đầu ra, số đầu ra mỗi tuần,
  tỉ lệ nháp được duyệt ngay lần đầu.
- Không xếp việc vào ngày nghỉ nếu tôi không nói có làm cuối tuần.
```

Dùng khi: ngay sau khi Skill chạy được, và mỗi lần bắt đầu một đợt triển khai mới. Lưu vào `00-doc-truoc/ke-hoach-14-ngay.md`.

Hai chỗ phải sửa tay sau khi Claude trả bảng về: cột "Ai làm" ghi tên người thật, không ghi "team"; ngày 1 và ngày 2 phải là việc làm được ngay chiều nay hoặc sáng mai. Kế hoạch nào mà ngày 1 đã cần họp với ba phòng ban thì kế hoạch đó chết từ ngày 1.

---

## 3. Sản phẩm buổi 6 anh chị phải có

| # | Sản phẩm | Nằm ở đâu |
|---|---|---|
| 1 | Claude Skill hoàn chỉnh, đủ 7 mục, có 3 nguyên tắc chống bịa nguyên văn | `.claude/skills/<tên-skill>/SKILL.md` ngay trong thư mục làm việc. Một bản để đọc đặt ở `06-skill/` |
| 2 | AI Agent Playbook đủ 7 mục | `00-doc-truoc/playbook.md` |
| 3 | Bộ tài sản 5 buổi sắp xếp theo cấu trúc 8 nhánh | Thư mục `<ten-thuong-hieu>-ai-system/` |
| 4 | Automation hoặc prototype kế thừa buổi 5, có bước người duyệt | `05-tu-dong-hoa/` |
| 5 | Demo agent 5 phút, đã trình bày và được chấm chéo | Ghi chú demo trong workbook, kèm phiếu chấm của bạn cùng nhóm |
| 6 | Kế hoạch triển khai 14 ngày, đủ 4 cột, có tên người thật | `00-doc-truoc/ke-hoach-14-ngay.md` |

**Chấm theo rubric 6 tiêu chí, tổng 18 điểm, xem [../danh-gia/rubric-san-pham-cuoi-khoa.md](../danh-gia/rubric-san-pham-cuoi-khoa.md).** Từ 12 điểm là Đạt, từ 15 điểm là Đạt loại tốt. Hai điều kiện chặn: không tiêu chí nào ở mức 1 điểm, và tiêu chí chống bịa phải từ 2 điểm. Chưa đạt thì được làm lại một lần trong vòng 5 ngày, chỉ phải sửa những tiêu chí bị 1 điểm.

---

## 4. Checklist tự kiểm

**Skill**

- [ ] File nằm đúng chỗ: `.claude/skills/<tên-skill>/SKILL.md` ngay trong thư mục làm việc
- [ ] Frontmatter đủ hai trường `name` và `description`; dòng `description` kể đủ các loại đầu ra và nêu một tình huống KHÔNG dùng
- [ ] Phần thân đủ 7 mục: vai trò, nguồn dữ liệu, tiêu chuẩn đầu ra, ranh giới, quy trình từng bước, xử lý khi thiếu dữ liệu, file tham chiếu
- [ ] Tiêu chuẩn đầu ra viết bằng số, có chuẩn riêng cho từng loại đầu ra, không còn tính từ kiểu "hay", "hấp dẫn"
- [ ] Ba nguyên tắc chống bịa nằm nguyên văn trong phần thân, không chỉ nằm trong `CLAUDE.md`
- [ ] Đã chạy 2 phép thử ngoài bối cảnh gốc mà không nhắc tên skill, cả 2 đều đạt

**Playbook**

- [ ] Đủ 7 mục, không mục nào bỏ trống, nhất là tiêu chuẩn đầu ra và ranh giới
- [ ] Có 3 chỉ số quá trình, mỗi chỉ số ghi rõ đo bằng cách nào
- [ ] Bảng xử lý khi agent ra sai có ghi tên người, không ghi chức danh chung chung

**Bộ tài sản**

- [ ] Đủ 8 thư mục đánh số, không còn file tên kiểu "final", "moi", "v2"
- [ ] `CLAUDE.md` và thư mục `.claude/skills/` nằm ngay ở gốc, không bị gói vào thư mục đánh số
- [ ] Đã có `00-doc-truoc/playbook.md` và `00-doc-truoc/ke-hoach-14-ngay.md`
- [ ] Người khác đọc tên 3 tài sản bất kỳ trong [checklist-toan-khoa.md](checklist-toan-khoa.md), tôi mở được cả 3 trong 10 giây
- [ ] Luồng buổi 5 vẫn chạy được, vẫn có bước người duyệt trước khi đăng hoặc gửi

**Chống bịa và đo được**

- [ ] Chạy ba câu hỏi về số liệu mà hồ sơ ghi rõ là chưa có: cả ba đều trả về "chưa đủ dữ liệu" kèm tên nguồn cần bổ sung
- [ ] Mọi đầu ra tự liệt kê ở cuối: câu nào `[DATA THẬT]`, câu nào `[SUY LUẬN]`
- [ ] Tôi chỉ được đúng dòng trong Skill đã thêm vào để chặn một lần agent bịa trước đây
- [ ] Kế hoạch 14 ngày đủ 14 dòng, cột "Ai làm" ghi tên người thật
- [ ] Ngày 7 và ngày 14 có mốc kiểm chỉ số; ngày 1 làm được trong 24 giờ tới

---

## 5. Kế hoạch 14 ngày sau khóa và cách tự duy trì

Buổi 6 hết là hệ thống mới chỉ chạy được trong lớp. Mười bốn ngày tới quyết định nó sống hay nằm im.

### 5.1 Nhịp 14 ngày

| Mốc | Việc | Nhìn vào đâu biết đã xong |
|---|---|---|
| Trong 24 giờ | Chạy Skill trên một việc thật, nhỏ, làm xong trong 20 phút | Có 1 đầu ra đã dùng cho khách thật hoặc kênh thật |
| Ngày 1 tới 6 | Chạy thử trên số ít. Mỗi lần đầu ra lệch chuẩn thì sửa Skill, không sửa tay kết quả | Danh sách các lần đã sửa Skill, mỗi dòng ghi sửa gì |
| **Ngày 7** | Mốc kiểm tuần 1. Ghi ba chỉ số bằng con số cụ thể | Ba con số đã điền, không ô nào bỏ trống |
| Ngày 8 tới 13 | Tăng số lượng. Đưa Skill và Playbook cho một người khác chạy thử | Ảnh chụp kết quả người đó chạy ra, và danh sách câu họ phải hỏi lại |
| **Ngày 14** | Mốc kiểm tuần 2. So ba chỉ số với ngày 7, quyết giữ hay đổi | Bảng so hai mốc, kèm một dòng quyết định |

**Ba chỉ số bắt buộc theo dõi**, chọn thêm chỉ số kinh doanh sau tuần 4:

| Chỉ số | Đo bằng cách nào | Nói lên điều gì |
|---|---|---|
| Thời gian làm 1 đầu ra | Bấm giờ 3 lần rồi lấy trung bình, so với thời gian trước khóa | Hệ thống có bỏ được phần lặp lại không |
| Số đầu ra mỗi tuần | Đếm trong bảng log của buổi 5 | Công suất có tăng thật không |
| Tỉ lệ nháp được duyệt ngay lần đầu | Số nháp không phải sửa chia cho tổng số nháp | Tiêu chuẩn đầu ra trong Skill đã đủ rõ chưa |

Chỉ số kinh doanh (số lead mỗi tuần, tỉ lệ lead thành đơn, chi phí trên mỗi lead, doanh thu theo kênh) chỉ đọc được từ tuần thứ 4 trở đi. **Đừng hứa với sếp là hệ thống tăng doanh thu trong hai tuần.** Trong hai tuần anh chị chứng minh được thời gian giảm và số lượng tăng, đó là hai thứ đo được. Hứa đúng cái đo được thì lần sau người ta còn tin.

### 5.2 Nhịp bảo trì sau 14 ngày

| Khi nào | Việc | Mất bao lâu |
|---|---|---|
| Mỗi tuần | Ghi ba chỉ số vào Playbook. Đọc bảng log buổi 5, xem cột "Hẹn giờ hay đăng ngay" | 10 phút |
| Mỗi tuần | Chạy một phép thử ngoài bối cảnh gốc. Lệch chuẩn thì sửa Skill ngay hôm đó | 10 phút |
| Mỗi tháng | Cập nhật `CLAUDE.md`: sản phẩm mới, giá mới, từ cấm mới. Bản cũ đẩy vào `99-luu-tru/` | 20 phút |
| Mỗi tháng | Chạy lại Customer Insight Agent trên đợt review và tin nhắn mới. Pain đổi thứ hạng thì content angle phải đổi theo | 30 phút |
| Mỗi quý | Rà quyền đã cấp cho các công cụ. Cái nào không dùng tiếp thì gỡ, ở cả hai chỗ | 15 phút |
| Khi có người mới | Đưa `00-doc-truoc/` cho họ, không giải thích miệng. Ghi lại mọi câu họ phải hỏi lại | Ghi trong lúc họ chạy |

**Danh sách câu người mới phải hỏi lại chính là danh sách chỗ Playbook còn thiếu.** Bổ sung đúng những chỗ đó, đừng viết lại cả tài liệu.

### 5.3 Ba mốc lớp còn giữ liên lạc

| Mốc | Việc của anh chị |
|---|---|
| Trong 5 ngày sau buổi 6 | Ai chưa đạt rubric thì sửa đúng những tiêu chí bị 1 điểm rồi nộp lại. Chỉ được một lần |
| Trong 3 ngày sau buổi 6 | Nhận phiếu phản hồi sản phẩm cuối khóa, mỗi phiếu nêu đúng một việc nên sửa trước tiên. Làm đúng một việc đó |
| Sau 30 ngày | Nhận phiếu áp dụng 11 câu, mất 3 phút. Phiếu này quyết định buổi hỏi đáp online 60 phút đi vào chỗ nào. Chưa dùng được gì cũng xin anh chị điền, đó mới là chỗ cần sửa |

Phiếu sau 30 ngày sẽ hỏi lại đúng những việc anh chị đã ghi trong kế hoạch 14 ngày. Mở file `00-doc-truoc/ke-hoach-14-ngay.md` ra trước khi điền, đừng trả lời bằng trí nhớ.

---

## 6. Sáu lỗi hay gặp khi làm lại ở nhà

| Lỗi | Dấu hiệu anh chị thấy | Cách xử lý |
|---|---|---|
| Skill viết chung chung nên người khác dùng không ra kết quả | Phần thân ghi "viết bài hay, đúng giọng thương hiệu". Đưa cho người khác chạy thì ra bài của bất kỳ hãng nào cùng ngành | Thay mọi tính từ bằng số hoặc câu kiểm được. "Bài hay" đổi thành "dưới 250 chữ, mở bằng một tình huống cụ thể, tối đa 2 emoji, kết bằng 1 CTA". Phép thử: đưa Skill cho một người chạy thử, ra khác nhau nhiều là còn mơ hồ |
| Playbook thiếu tiêu chuẩn đầu ra | Có đủ các bước nhưng không mục nào nói kết quả đạt trông thế nào. Người dùng chạy xong không biết nên gửi hay nên sửa | Viết bảng 5 dòng "đạt khi" cho từng loại đầu ra chính. Tự hỏi: ai bấm nút duyệt, họ nhìn vào đâu để quyết. Câu trả lời chính là tiêu chuẩn cần viết |
| Skill chỉ chạy đúng trên đúng ví dụ đã demo | Chạy lại đề cũ thì đẹp. Đổi sang SKU khác hoặc nhóm khách khác thì kết quả lệch chuẩn | Chạy 2 phép thử ngoài bối cảnh gốc trước khi đưa cho ai. Lệch thường do Skill mô tả theo tình huống cụ thể thay vì mô tả theo bước. Viết lại các bước ở dạng chung, đẩy phần cụ thể xuống file tham chiếu |
| Ba nguyên tắc chống bịa nằm ngoài Skill | Anh chị nói "cái đó tôi nhớ rồi, lúc chạy tự nhắc". Trong Skill không có dòng nào về nhãn nguồn | Đây là lỗi nặng nhất. Trí nhớ không bàn giao được. Dán nguyên khối ba nguyên tắc vào phần thân Skill, thêm một dòng vào tiêu chuẩn đầu ra: mọi số liệu phải có nhãn `[DATA THẬT]` hoặc `[SUY LUẬN]` |
| Kế hoạch 14 ngày không có tên người | Cột "ai làm" ghi "team" hoặc để trống; cột kết quả ghi "tăng tương tác" | Điền tên cụ thể, không có ai khác thì ghi tên mình. Việc không có tên là việc không xảy ra. Đổi cột kết quả sang con số đếm được: "9 bài đã lên lịch", "20 lead đã chấm điểm" |
| Tài sản đổ dồn một thư mục | 40 file nằm chung một chỗ, tên kiểu `bai viet moi nhat (2).docx`. Hai tháng sau chính anh chị cũng không tìm ra | Tạo đúng 8 thư mục và đổi tên file, mất khoảng 10 phút. Đây là việc chán nhất nhưng bỏ qua thì Playbook vô dụng: người ta không tìm được file thì cũng không ai dùng |

---

CES Global · Creative, Effective, Sustainable
