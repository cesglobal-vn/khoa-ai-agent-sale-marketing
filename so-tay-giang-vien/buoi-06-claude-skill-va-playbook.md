# Buổi 6 · Kịch bản demo 35 phút

**Case demo:** Thảo An
**Chuẩn bị trước khi lên lớp:**
- Thư mục làm việc `thao-an-marketing` của buổi 1, mở sẵn bằng tab **Code** của Claude Desktop. Trong đó phải có đủ: `CLAUDE.md`, `san-pham-thao-an.md`, và skill `.claude/skills/viet-bai-ban-hang/SKILL.md`.
- Các file nền của buổi 2 tới buổi 5 đã nằm sẵn trong thư mục đó, vì Claude chỉ đọc được thứ nằm trong thư mục đang mở.
- Một thư mục trống trên máy tên `thao-an-ai-system`, chiếu được lên màn hình.
- Mở sẵn tab trình duyệt file [../demo/thao-an/assets/thao-an-agent-team-diagram.html](../demo/thao-an/assets/thao-an-agent-team-diagram.html), để tab riêng, chưa chiếu.
- Mở sẵn [../demo/buoi-06/skill-dong-goi-va-playbook.md](../demo/buoi-06/skill-dong-goi-va-playbook.md) để copy Skill mẫu khi cần.

> Nhắc lớp ngay từ đầu: "35 phút này các bạn mở máy ra gõ theo tôi, không ngồi xem. Tôi đi chậm và dừng lại chờ cả lớp. Có một đoạn ở phút 18 là phần quan trọng nhất cả buổi, tôi sẽ báo trước khi tới, và đoạn đó không ai được ngồi xem." Bảng phân công học viên gõ gì ở từng bước, cùng bốn điểm dừng chờ cả lớp, nằm ở mục "Khối 2 chạy kiểu làm theo" trong [../giao-an/buoi-06-claude-skill-va-playbook.md](../giao-an/buoi-06-claude-skill-va-playbook.md). Đọc mục đó trước khi vào lớp.

---

## Mốc 00:00 - 05:00 · Gom tài sản 5 buổi thành cấu trúc thư mục

### Thao tác

Mở thư mục trống trên màn hình. Hỏi lớp: "Bây giờ tôi có 40 file nằm rải rác trong Download, Zalo, Google Docs và 5 cửa sổ chat. Bắt đầu từ đâu?"

Không tự nghĩ cấu trúc. Nhờ Claude nghĩ, vì Claude biết chính xác 5 buổi đã ra những gì.

### Prompt

```
Tôi vừa hoàn thành 5 buổi xây hệ thống AI Sale & Marketing cho Thảo An.
Các đầu ra tôi đang có:

Buổi 1: thư mục làm việc, file CLAUDE.md (câu định vị, 3 thông điệp, 5 nỗi đau,
giọng văn, danh sách từ cấm), hồ sơ sản phẩm san-pham-thao-an.md, Memory đã bật,
skill viet-bai-ban-hang, 3 bài bán hàng, 10 hook, 10 CTA, 1 kết nối MCP.
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

### Kết quả mong đợi

Cây thư mục 8 nhánh, đánh số 00 tới 99. Giống bảng trong giáo án. Nếu Claude trả về khác đôi chút thì giữ nguyên, đừng ép, miễn là có đủ nhánh "đọc trước" và nhánh lưu trữ.

### Nói gì với lớp

"Việc này chán nhất buổi hôm nay. Nhưng bỏ qua nó thì mọi thứ phía sau vô nghĩa. Playbook hay tới đâu mà người ta không tìm được file thì cũng không ai dùng."

Chỉ vào nhánh `00-doc-truoc/`: "Đây là chỗ đắt nhất. Người mới vào mở thư mục này, đọc 2 file, là làm việc được. Không phải đi hỏi ai."

Tạo thật các thư mục trên màn hình, kéo vài file vào cho lớp thấy nó thành hình.

---

## Mốc 05:00 - 10:00 · Rút quy trình đang làm bằng tay thành các bước

### Thao tác

Nói với lớp: "Trước khi viết Skill, phải biết mình đang làm gì. Phần lớn mọi người không nói ra được quy trình của chính mình. Nhờ Claude phỏng vấn ngược."

### Prompt

```
Trong thư mục làm việc này, 5 buổi qua tôi đã dựng: nền dữ liệu thương hiệu
trong file CLAUDE.md và hồ sơ sản phẩm, skill viet-bai-ban-hang, rồi 5 agent
là Customer Insight, Content Engine, Outbound, Proposal, Closer, cộng một
luồng tự động hóa của buổi 5.

Hãy đọc các file system prompt và các đầu ra tôi đã lưu trong thư mục này,
rồi rút ra quy trình tôi đang làm bằng tay, viết dưới dạng các bước đánh số.

Với mỗi bước ghi rõ:
- Tên bước
- Đầu vào: cần file hoặc thông tin gì mới chạy được
- Việc làm: mô tả bằng động từ, không dùng tính từ
- Đầu ra: kết quả cụ thể, đếm được
- Ai duyệt: bước nào bắt buộc người xem trước khi đi tiếp

Nếu chỗ nào bạn không đủ dữ liệu để rút ra, ghi thẳng "chưa đủ dữ liệu",
đừng suy đoán quy trình giúp tôi.
```

### Kết quả mong đợi

Danh sách 5 tới 7 bước. Ví dụ với Thảo An: (1) nạp nền dữ liệu thương hiệu vào `CLAUDE.md` và hồ sơ sản phẩm; (2) đọc review và tin nhắn, ra bảng insight có trích dẫn; (3) chọn góc nội dung, ra content angle; (4) sản xuất nội dung theo kênh, ra bài và brief hình ảnh; (5) chấm điểm lead và soạn email hoặc tin nhắn; (6) người duyệt, rồi mới đăng hoặc gửi.

### Nói gì với lớp

"Nhìn kỹ bước 6. Bước duyệt phải nằm trong quy trình, không phải nằm trong lời hứa. Cái gì không viết vào quy trình thì lúc gấp là bỏ qua đầu tiên."

Nếu Claude ghi "chưa đủ dữ liệu" ở đâu đó, dừng lại chỉ cho lớp: "Đây là agent làm đúng. Nó không bịa hộ tôi quy trình mà tôi chưa từng làm."

---

## Mốc 10:00 - 18:00 · Viết Skill từ quy trình đó

### Thao tác

Nói rõ khác biệt trước khi gõ: "Quy trình vừa rút là để tôi đọc. Skill là để Claude đọc. Bây giờ dịch từ cái thứ nhất sang cái thứ hai."

Mở luôn file `.claude/skills/viet-bai-ban-hang/SKILL.md` viết ở buổi 1, chiếu lên. Nói: "Cách viết file thì buổi 1 anh chị làm rồi, tôi không giảng lại. Chỗ khác nằm ở đây: cái này làm được đúng một việc cho đúng một người. Cái ta viết bây giờ phủ cả bộ việc, và có thêm bốn mục để người khác cầm lên là chạy được."

Chỉ tay lên bảng vào bốn mục đã ghi ở phần framework: Vai trò, Tiêu chuẩn đầu ra cho từng loại, Ranh giới không được vượt, Xử lý khi thiếu dữ liệu. Không giải thích lại, chỉ đọc tên.

### Prompt

```
Mở file .claude/skills/viet-bai-ban-hang/SKILL.md tôi đã viết ở buổi 1
để xem lại cách tôi viết skill.

Bây giờ tạo cho tôi một skill mới, rộng hơn, phủ cả quy trình vừa rút ở trên.
Đường dẫn: .claude/skills/thao-an-sale-marketing/SKILL.md

Frontmatter viết theo đúng kiểu file cũ. Riêng dòng description phải rộng hơn:
liệt kê rõ từng loại yêu cầu sẽ kích hoạt skill này (bài Facebook, mô tả Shopee,
tin nhắn tư vấn inbox, email chào hàng sỉ, kịch bản gọi khách spa, proposal
bán sỉ, lịch nội dung, brief hình ảnh), kể cả khi tôi chỉ gõ tên SKU kèm tên
kênh. Nêu luôn một tình huống KHÔNG dùng skill này.

Phần thân gồm đúng 7 mục sau. Bốn mục đầu là phần file cũ chưa có:

1. Vai trò: skill này đóng vai ai trong đội, tả bằng một ví von nghề nghiệp,
   kèm quy tắc xưng hô lấy từ CLAUDE.md.
2. Nguồn dữ liệu: liệt kê tên từng file nền trong thư mục này, ghi rõ file nào
   là nguồn sự thật cho giá, cho giọng văn, cho lời khách nói.
3. Tiêu chuẩn đầu ra: viết riêng cho TỪNG loại đầu ra kể trên. Mỗi dòng phải
   là con số hoặc câu kiểm được bằng mắt. Không dùng tính từ kiểu "hay",
   "hấp dẫn", "chuyên nghiệp".
4. Ranh giới không được vượt: ngoài danh sách từ cấm trong CLAUDE.md, ghi thêm
   việc gì skill không được tự quyết và việc gì bắt buộc người làm.
5. Quy trình từng bước: mỗi bước một việc, viết bằng động từ, ghi rõ đầu vào
   và đầu ra. Bước cuối là tự soát trước khi trả về.
6. Xử lý khi thiếu dữ liệu: gặp chỗ trống thì làm gì, theo thứ tự nào.
7. File tham chiếu: liệt kê đúng tên và đúng đường dẫn các file nền.

Ba nguyên tắc chống bịa đang nằm trong CLAUDE.md của thư mục này: chép nguyên
văn sang phần thân skill, không diễn đạt lại, không rút gọn.
```

### Kết quả mong đợi

Một file Skill hoàn chỉnh. Bản mẫu nguyên văn nằm ở [../demo/buoi-06/skill-dong-goi-va-playbook.md](../demo/buoi-06/skill-dong-goi-va-playbook.md), mở ra chiếu lên cho lớp đối chiếu.

Chiếu phần đầu để lớp thấy hình dạng:

```
---
name: thao-an-sale-marketing
description: Dùng khi cần tạo bất kỳ đầu ra Sale hoặc Marketing cho thương hiệu
  mỹ phẩm thảo mộc Thảo An: bài Facebook, mô tả Shopee, tin nhắn tư vấn inbox,
  email chào hàng sỉ, kịch bản gọi khách spa, proposal bán sỉ, lịch nội dung,
  brief hình ảnh. Kích hoạt cả khi người dùng chỉ nói tên SKU và tên kênh.
  Không dùng cho trả lời khiếu nại, xử lý khủng hoảng hay phản hồi review xấu.
---
```

### Nói gì với lớp

Đọc lướt dòng `description`, không giảng lại: "Buổi 1 anh chị đã biết đây là dòng Claude đọc để quyết định có mở skill ra hay không. Chỗ khác duy nhất: skill này rộng hơn nên dòng này phải kể đủ các loại đầu ra, và phải nói rõ khi nào KHÔNG dùng." Xong, đi tiếp ngay. Đây là chỗ hay bị sa đà, giảng viên tự canh đồng hồ.

Dừng lâu nhất ở phần **Tiêu chuẩn đầu ra**, vì đây mới là phần mới. Chỉ vào một dòng có số: "Thấy chưa, 'dưới 250 chữ' kiểm được, 'bài hay' thì không. Và để ý là mỗi loại đầu ra một chuẩn riêng: bài Facebook một chuẩn, tin nhắn inbox một chuẩn, email chào sỉ một chuẩn. Buổi 1 anh chị mới viết chuẩn cho một loại. Người khác cầm skill này lên vẫn ra đúng chuẩn vì chuẩn viết bằng số."

Dừng tiếp ở mục **Ranh giới không được vượt**, chỉ vào dòng nói về chiết khấu: "Đây là thứ buổi 1 chưa có. Không phải chỉ cấm chữ. Còn là cấm tự quyết. Người mới vào cầm skill này thì cũng không tự hứa chiết khấu ngoài bảng được."

Kéo xuống ba nguyên tắc chống bịa, nói ngắn: "Ba cái này anh chị đã ghi trong `CLAUDE.md` từ buổi 1, nhưng `CLAUDE.md` chỉ đúng trong thư mục này. Giờ nó nằm trong skill, mà skill thì mang đi được. Ai cầm skill cũng có nó, kể cả người chưa từng học khóa này. Đây là điểm quan trọng nhất của buổi cuối."

---

## Mốc 18:00 - 25:00 · Thử Skill trên một yêu cầu mới

### Thao tác

Báo trước cho lớp: "Đoạn này là phép thử quan trọng nhất. Skill chạy đúng trên ví dụ đã demo thì chưa nói lên gì. Phải chạy đúng trên cái nó chưa từng thấy."

Mở một phiên trò chuyện MỚI trong tab Code, vẫn ở thư mục làm việc đó. Giải thích: "Phiên cũ còn nhớ hết bối cảnh chúng ta vừa nói. Chạy trong đó là tự lừa mình." Không gọi tên skill trong prompt, gõ thẳng yêu cầu như người dùng thật sẽ gõ. Nói rõ với lớp lý do: "Tôi cố ý không nhắc tên skill. Nếu dòng `description` viết đúng thì Claude phải tự rút nó ra. Không tự rút ra được thì lỗi ở dòng đó, không phải lỗi ở phần thân."

### Prompt thử nghiệm 1

```
Tuần sau Thảo An có gian hàng ở hội chợ mỹ phẩm.
Soạn cho tôi:
- 1 tờ rơi A5 phát tại gian hàng, cho khách lẻ.
- 1 kịch bản chào 60 giây khi khách dừng lại xem.
- 1 tin nhắn gửi lại cho khách đã để số điện thoại, gửi sau hội chợ 2 ngày.
```

### Kết quả mong đợi

Ba đầu ra đúng chuẩn dù chưa buổi nào dạy làm tờ rơi hay kịch bản hội chợ. Cụ thể phải thấy:

- Đúng giọng Thảo An: xưng "Thảo An", gọi khách là "bạn", câu ngắn.
- Không có từ cấm: không "trị mụn", không "đặc trị", không cam kết thời gian.
- Có nhãn `[DATA THẬT]` ở phần giá và thành phần, `[SUY LUẬN]` ở phần phỏng đoán hành vi khách tại hội chợ.
- Có ít nhất một chỗ ghi "chưa đủ dữ liệu", vì hồ sơ Thảo An không có thông tin về ngân sách, số lượng mẫu thử, hay ai đứng gian hàng.
- Tin nhắn gửi sau hội chợ ghi rõ đây là nháp, cần người duyệt trước khi gửi.

### Prompt thử nghiệm 2

Chạy thêm một cái nữa, khác luồng, để chứng minh không phải ăn may:

```
Một spa ở Đà Nẵng nhắn hỏi: "Bên em nhập sỉ 50 chai serum thì giá bao nhiêu,
có hỗ trợ tư vấn cho nhân viên spa không?"
Soạn tin nhắn trả lời.
```

### Kết quả mong đợi

Tin nhắn dùng đúng bảng chiết khấu trong chính sách giá sỉ, có nhãn nguồn, và quan trọng nhất: gặp phần "hỗ trợ tư vấn cho nhân viên spa" mà chính sách không có thì phải ghi "chưa đủ dữ liệu, cần xác nhận với người phụ trách" chứ không tự hứa.

### Nói gì với lớp

Trước khi bấm gửi, hỏi lớp: "Đoán xem nó có bịa cái chương trình đào tạo cho spa không?" Rồi bấm. Nếu Skill xử lý đúng: "Đây là lúc bạn biết Skill xong. Nó gặp chỗ trống mà không lấp bằng chữ nghe hay."

Nếu Skill bịa (có thể xảy ra, và nếu xảy ra thì càng tốt cho lớp): dừng lại, chỉ ra chính xác câu bịa, rồi sửa Skill ngay trước mặt lớp bằng cách thêm một dòng vào mục Xử lý khi thiếu dữ liệu, chạy lại. Nói: "Đây mới là cách người ta làm thật. Skill không đúng ngay lần đầu. Nó đúng sau vòng thử thứ hai hoặc thứ ba."

---

## Mốc 25:00 - 30:00 · Dùng sơ đồ hệ thống để trình bày cho sếp hoặc khách

### Thao tác

Chuyển sang tab trình duyệt đã mở sẵn: [../demo/thao-an/assets/thao-an-agent-team-diagram.html](../demo/thao-an/assets/thao-an-agent-team-diagram.html).

*Lưu ý cho giảng viên:* sơ đồ này đã cập nhật đúng theo khóa hiện tại. Ô số 1 là `CLAUDE.md`, nền thương hiệu dùng chung, không phải một agent riêng. Năm ô còn lại là 5 agent học viên đã xây từ buổi 2 tới buổi 5.

Nói: "Từ nãy tới giờ là làm. Bây giờ là bán. Sếp không đọc Skill của bạn. Khách cũng không. Họ nhìn một trang này trong 2 phút rồi quyết."

Trình bày mẫu ngay trên sơ đồ, đúng như học viên sẽ phải làm ở khối demo chéo:

**Bước 1, khối 3 nguyên tắc ở đầu sơ đồ (30 giây).** "Trước khi nói hệ thống làm được gì, tôi nói nó không làm gì: không bịa số, mọi thứ có nhãn nguồn, không tự gửi cho khách." Mở đầu bằng ranh giới là cách nhanh nhất để người nghe hạ hàng phòng thủ.

**Bước 2, luồng chính từ trái sang phải (90 giây).** `CLAUDE.md` và hồ sơ sản phẩm là nền dữ liệu, Customer Insight ra persona và bảng nỗi lo, rồi tách hai nhánh: B2C qua Content Engine ra caption Facebook, Shopee, Zalo; B2B qua Outbound, Proposal, Closer ra đơn sỉ. Năm agent, một nền dữ liệu. Mỗi khối 3 tới 5 giây, không đọc chi tiết.

**Bước 3, mũi tên vòng lặp quay về Insight (30 giây).** "Review và tin nhắn mới đổ về nuôi lại bước 2. Hệ thống càng chạy càng hiểu khách hơn."

**Bước 4, ô cuối "Đơn / Hợp đồng (sau khi bạn duyệt)" (30 giây).** "Chú ý dòng trong ngoặc. Người vẫn bấm nút cuối."

**Bước 5, phần chi tiết từng agent phía dưới (60 giây).** "Phần này không trình bày, để người hỏi sâu tự đọc. Đưa link, đừng đọc lên."

### Nói gì với lớp

"Một trang này thay được 15 slide. Học viên nào làm agency thì đây chính là thứ bạn gửi khách trước cuộc gặp. Khách xem xong thì cuộc gặp bắt đầu từ câu 'triển khai bao lâu' chứ không phải câu 'AI là gì'."

Bảo lớp: file này mở bằng trình duyệt, không cần cài gì. Ai muốn làm bản của mình thì nhờ Claude tạo lại một trang tương tự với tên agent và luồng của mình.

---

## Mốc 30:00 - 35:00 · Lập kế hoạch triển khai 14 ngày

### Thao tác

Nói: "Còn một việc nữa. Ra khỏi lớp mà không có lịch cụ thể thì 3 hôm sau mọi thứ nằm im."

### Prompt

```
Lập kế hoạch triển khai 14 ngày để đưa hệ thống này vào chạy thật tại Thảo An.

Bối cảnh: đội có 2 người. Một người phụ trách content và inbox Facebook,
một người phụ trách bán sỉ cho spa. Mục tiêu đang chạy là 30 đơn trong 30 ngày,
mọi đơn gắn được nguồn kênh.

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

### Kết quả mong đợi

Bảng 14 dòng. Tuần 1 nhẹ, tập trung chạy thử và sửa. Tuần 2 tăng số lượng. Ngày 7 và ngày 14 có dòng kiểm chỉ số riêng.

### Nói gì với lớp

Chỉ vào ngày 1 và ngày 2: "Hai ngày đầu phải làm được ngay chiều nay hoặc sáng mai. Kế hoạch nào mà ngày 1 đã cần họp với 3 phòng ban thì kế hoạch đó chết từ ngày 1."

Chỉ vào cột "Ai làm": "Ghi tên người. Không ghi 'team'. Việc không có tên là việc không xảy ra."

Chốt cả demo, nối sang khối học viên làm:

"35 phút vừa rồi tôi đi đúng 5 bước: gom tài sản, rút quy trình, viết Skill, thử Skill trên cái mới, và lên lịch 14 ngày. 55 phút tới các bạn làm y hệt trên thương hiệu của mình, chia hai chặng, giữa hai chặng nghỉ 10 phút. Chặng 1 làm tới lúc file Skill sinh ra rồi nghỉ. Bước quan trọng nhất là bước thử Skill trên yêu cầu mới, nằm ở chặng 2. Ai bỏ bước đó thì đừng nộp bài."

---

CES Global · Creative, Effective, Sustainable
