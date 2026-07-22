# Nội dung slide Buổi 06: Claude Skill và AI Agent Playbook

**Khóa:** AI Agent cho Sale & Marketing
**Hình thức:** online live qua Zoom hoặc Meet
**Thời lượng buổi:** 150 phút
**Tổng số slide:** 35 slide, trong đó 22 slide nội dung và bảng, 8 slide prompt, 3 slide đề bài và mốc thời gian, 1 slide bìa, 1 slide giải lao
**Giáo án nguồn:** `giao-an/buoi-06-claude-skill-va-playbook.md`
**Kịch bản demo nguồn:** `so-tay-giang-vien/buoi-06-claude-skill-va-playbook.md`
**Ma trận mục tiêu:** `00-tong-quan/ma-tran-muc-tieu.md` mục tiêu 6.1 tới 6.5

## Ghi chú thiết kế chung

- Nền trắng, chữ đậm, cỡ chữ tối thiểu 28pt vì lớp học qua màn hình chia sẻ
- Slide prompt để chữ cỡ lớn trong khối code, học viên nhìn màn hình chia sẻ gõ theo được
- Mỗi slide một thông điệp, tối đa 6 dòng
- Phần "Lời giảng viên nói khi chiếu slide này" KHÔNG in lên slide
- Màu, logo, font do bước đóng gói áp vào, không ghi ở đây

---

### Slide 1: Buổi 6. Claude Skill và AI Agent Playbook

**Loại:** tiêu đề

**Nội dung hiển thị:**
- AI Agent cho Sale & Marketing
- Buổi 6 trên 6, buổi cuối
- Đóng gói thành hệ thống dùng được hoặc bán được
- 150 phút

**Lời giảng viên nói khi chiếu slide này:** "Chào anh chị. Buổi cuối. Năm buổi qua anh chị đã làm ra hơn 40 đầu ra, nhưng chúng đang nằm rải rác trong nhiều thư mục, nhiều cửa sổ chat, và phần lớn cách làm vẫn nằm trong đầu anh chị. Hôm nay gom cả bộ thành một Skill và một Playbook mà người khác cầm lên dùng được, không cần hỏi lại anh chị. Đó là lúc nó thành tài sản, không còn là kỹ năng cá nhân."

**Hình minh họa gợi ý:** Nhiều mảnh giấy rải rác bên trái, một hộp có nhãn gọn gàng bên phải, mũi tên nối.

**Thời điểm:** Khối 1 Framework, phút 0

---

### Slide 2: Hết buổi hôm nay anh chị làm được gì

**Loại:** nội dung

**Nội dung hiển thị:**
- Nâng skill buổi 1 thành Skill phủ cả bộ việc Sale và Marketing
- Chứng minh Skill chạy đúng trên một yêu cầu chưa từng làm
- Có AI Agent Playbook đồng nghiệp đọc là vận hành được
- Sắp xếp tài sản 5 buổi vào cấu trúc tìm được trong 10 giây
- Trình bày hệ thống trong 5 phút bằng kết quả, không bằng tên công cụ
- Có kế hoạch triển khai 14 ngày ghi rõ ngày, việc, người làm, kết quả

**Lời giảng viên nói khi chiếu slide này:** "Dòng thứ hai là dòng tôi coi trọng nhất và cũng là dòng tôi sẽ không cắt dù thiếu giờ. Skill chạy đúng trên ví dụ đã demo thì chưa nói lên gì. Phải chạy đúng trên cái nó chưa từng thấy. Chiều nay tôi sẽ đưa anh chị một đề chưa buổi nào dạy, và anh chị đối chiếu kết quả với bảng tiêu chuẩn do chính anh chị viết."

**Hình minh họa gợi ý:** 6 ô vuông trống để tích, ô thứ hai đóng khung đậm.

**Thời điểm:** Khối 1, phút 1

---

### Slide 3: Anh chị phải mở sẵn tài sản của cả năm buổi

**Loại:** bảng

**Nội dung hiển thị:**

| Buổi | Phải có |
|---|---|
| 1 | `CLAUDE.md`, hồ sơ sản phẩm, skill `viet-bai-ban-hang`, 3 bài, 10 hook, 10 CTA |
| 2 | `insight-khach-hang.md`, persona, 5 angle, 5 bài social, 3 brief, 3 visual |
| 3 | Lead scoring 10 lead, 10 email, 10 tin nhắn, kịch bản gọi, 10 kịch bản từ chối, proposal |
| 4 | Campaign brief, `lich-14-ngay.md`, 10 bài, 3 email, landing, 3 video script, carousel |
| 5 | `automation-map.md`, bảng quản lý, luồng post bài, mẫu thông báo, checklist rủi ro |

**Lời giảng viên nói khi chiếu slide này:** "Buổi này không tạo ra dữ liệu mới, nó gom cái đã có. Thiếu đầu vào là ngồi làm lại, mất thời gian của cả lớp. Ai thiếu buổi nào thì gõ số buổi đó vào chat cho tôi biết ngay bây giờ, tôi sắp xếp cho anh chị chạy trên bộ Thảo An ở phần đó, đừng để tới giữa buổi mới phát hiện."

**Hình minh họa gợi ý:** 5 chồng file xếp cạnh nhau, mỗi chồng ghi số buổi.

**Thời điểm:** Khối 1, phút 2

---

### Slide 4: Hôm nay không dạy khái niệm mới

**Loại:** nội dung

**Nội dung hiển thị:**
- Không thêm agent mới
- Gom 5 agent cộng luồng tự động hóa thành một hệ thống bàn giao được
- Cách viết file SKILL.md buổi 1 đã dạy, không giảng lại
- Hôm nay nâng cấp cái đã có

**Lời giảng viên nói khi chiếu slide này:** "Anh chị mở luôn file skill viet-bai-ban-hang của mình ra, để nguyên trên màn hình suốt buổi. Đường dẫn, frontmatter hai dòng, vì sao dòng description quan trọng nhất: buổi 1 đã dạy kỹ, tôi không giảng lại. Hôm nay ta không viết lại từ đầu, ta nâng cấp cái này."

**Hình minh họa gợi ý:** Một file nhỏ nhãn "buổi 1" với mũi tên đi lên thành một file lớn hơn nhãn "buổi 6".

**Thời điểm:** Khối 1, phút 3

---

### Slide 5: Nhịp buổi hôm nay

**Loại:** bảng

**Nội dung hiển thị:**

| Khối | Phút | Việc |
|---|---|---|
| 1 | 20 | Framework, chỉ nghe |
| 2 | 35 | Demo làm theo, anh chị gõ cùng tôi |
| 3a | 30 | Gom tài sản và viết Skill |
| Nghỉ | 10 | Giải lao |
| 3b | 25 | Thử Skill và viết Playbook |
| 4 | 10 | Demo chéo, mỗi người 5 phút |
| 5 | 20 | Hoàn thiện, nộp, kết khóa |

**Lời giảng viên nói khi chiếu slide này:** "Khối 4 hôm nay khác các buổi trước: không phải tôi review, mà anh chị chấm nhau. Chia cặp hoặc nhóm ba, mỗi người trình bày agent của mình đúng 5 phút, người còn lại chấm theo rubric. Tôi đi nghe, không cắt ngang. Nếu không kịp thì mức đạt tối thiểu là Playbook rút xuống 2 trang và kế hoạch rút xuống 7 ngày, nhưng phần thử Skill trên yêu cầu mới thì tuyệt đối không cắt."

**Hình minh họa gợi ý:** Thanh ngang chia 7 đoạn theo tỉ lệ thời lượng.

**Thời điểm:** Khối 1, phút 4

---

### Slide 6: Anh chị nghỉ phép hai tuần

**Loại:** nội dung

**Nội dung hiển thị:**
- Đồng nghiệp mở thư mục làm việc của anh chị ra
- Họ làm được bài đăng đúng chuẩn không?
- Thư mục có đủ dữ liệu thương hiệu
- Còn cách làm vẫn nằm trong đầu anh chị

**Lời giảng viên nói khi chiếu slide này:** "Anh chị gõ vào chat: có hay không. Phần lớn sẽ trả lời không. Đó là toàn bộ bài toán của buổi hôm nay. Thư mục làm việc chứa dữ liệu, còn quy trình thì chưa ai viết ra. Trí nhớ không bàn giao được."

**Hình minh họa gợi ý:** Một thư mục mở với nhiều file, bên cạnh là một cái đầu người có dấu chấm hỏi.

**Thời điểm:** Khối 1, phút 4 tới 6

---

### Slide 7: CLAUDE.md khác SKILL.md ở đâu

**Loại:** bảng

**Nội dung hiển thị:**

| `CLAUDE.md` | `SKILL.md` |
|---|---|
| Hồ sơ MỘT thương hiệu | Quy trình mang đi được |
| Bán gì, bán cho ai | Các bước làm việc |
| Giọng văn, từ cấm | Tiêu chuẩn đầu ra |
| Buộc vào 1 thương hiệu | Ranh giới không được vượt |
| Đổi khách là viết lại từ đầu | Đưa đồng nghiệp, đưa khách, dùng lại được |

**Lời giảng viên nói khi chiếu slide này:** "Ví dụ thực tế cho dễ hình dung: một agency có 8 khách hàng. Họ sẽ có 8 thư mục làm việc, mỗi khách một CLAUDE.md riêng. Nhưng chỉ cần 1 bộ skill dùng chung cho cả 8, vì quy trình viết bài giống nhau, chỉ khác dữ liệu. Nhắc lại điều buổi 1 đã nói qua: đặt bộ skill đó ở thư mục người dùng thì mọi thư mục trên máy đều gọi được."

**Hình minh họa gợi ý:** Bên trái 8 thư mục riêng biệt, bên phải 1 hộp skill có 8 mũi tên tỏa ra.

**Thời điểm:** Khối 1, phút 6 tới 9

---

### Slide 8: Bốn thứ buổi 1 chưa có

**Loại:** nội dung

**Nội dung hiển thị:**
1. **Vai trò.** Agent đóng vai ai trong đội, tả bằng một ví von nghề nghiệp
2. **Tiêu chuẩn đầu ra cho TỪNG loại.** Bài social, tin nhắn, email sỉ, proposal, brief
3. **Ranh giới không được vượt.** Không chỉ từ cấm, còn là việc gì không được tự quyết
4. **Xử lý khi thiếu dữ liệu.** Gặp chỗ trống thì làm gì, theo thứ tự nào

**Lời giảng viên nói khi chiếu slide này:** "Skill buổi 1 làm được đúng một việc cho đúng một người. Bốn thứ này là phần buổi 1 chưa có, và cũng là phần khiến người khác cầm lên dùng được. Ví dụ mục 1 cho Thảo An: viết như dược sĩ tư vấn ở quầy thuốc, giải thích thành phần trước, mời mua sau. Mục 4 là mục để người dùng sau biết đường xử lý mà không phải gọi điện hỏi anh chị."

**Hình minh họa gợi ý:** 4 ô xếp 2 hàng 2 cột, mỗi ô một số lớn.

**Thời điểm:** Khối 1, phút 8 tới 9

---

### Slide 9: Quy trình của anh chị có đóng gói được không

**Loại:** nội dung

**Nội dung hiển thị:**
1. Việc này có lặp lại không?
2. Có mô tả được bằng các bước không?
3. Kết quả đúng trông như thế nào?
4. Chỗ nào tuyệt đối không được vượt?

Phép thử: đưa Skill cho người mới vào công ty tuần đầu. Họ chạy ra kết quả anh chị dám gửi khách không?

**Lời giảng viên nói khi chiếu slide này:** "Câu 3 và câu 4 là chỗ 90 phần trăm người viết Skill bỏ qua. Họ viết được các bước, quên viết tiêu chuẩn và ranh giới. Kết quả là Skill chạy ra thứ nhìn giống việc nhưng dùng không được. Còn câu 2 là câu lọc: nếu anh chị không nói được bước 1 làm gì, bước 2 làm gì, thì anh chị chưa hiểu quy trình của chính mình."

**Hình minh họa gợi ý:** 4 dấu hỏi xếp dọc. Câu 3 và câu 4 tô đậm.

**Thời điểm:** Khối 1, phút 9 tới 14

---

### Slide 10: Playbook cần bảy mục

**Loại:** bảng

**Nội dung hiển thị:**

| Mục | Trả lời câu hỏi |
|---|---|
| Mục đích | Hệ thống này giải bài toán gì |
| Ai dùng | Vị trí nào, cần biết gì trước |
| Quy trình từng bước | Mở cái gì, gõ gì, làm gì tiếp |
| Tiêu chuẩn đầu ra | Thế nào là đạt |
| Ranh giới không được vượt | Cấm gì |
| Chỉ số đo | Nhìn vào đâu biết hệ thống có hiệu quả |
| Xử lý khi agent ra sai | Sai thì làm gì |

**Lời giảng viên nói khi chiếu slide này:** "Skill là thứ Claude đọc. Playbook là thứ người đọc. Thiếu Playbook, đồng nghiệp có Skill mà vẫn không biết dùng lúc nào, dùng xong kiểm thế nào. Thiếu mục nào thì người dùng sẽ quay lại hỏi anh chị đúng mục đó. Và tôi nói thẳng một điều với anh chị nào làm agency: Playbook không phải tài liệu trang trí, nó là thứ anh chị bán được cho khách. Khách không mua prompt, khách mua quy trình có bảo hành."

**Hình minh họa gợi ý:** 7 dòng, mỗi dòng có ô tích ở đầu.

**Thời điểm:** Khối 1, phút 14 tới 17

---

### Slide 11: Chọn chỉ số nào để đo

**Loại:** bảng

**Nội dung hiển thị:**

| Đo được ngay từ tuần 1 | Đo sau 4 tuần trở đi |
|---|---|
| Thời gian làm 1 đầu ra, trước và sau | Số lead mỗi tuần, gắn được nguồn kênh |
| Số đầu ra mỗi tuần | Tỉ lệ lead thành đơn |
| Tỉ lệ nháp được duyệt ngay lần đầu | Chi phí trên mỗi lead |
| Số lần agent bị bắt lỗi bịa, mục tiêu là 0 | Doanh thu theo kênh |

**Lời giảng viên nói khi chiếu slide này:** "Đo sai chỉ số thì hệ thống chạy tốt mà không ai tin, hoặc chạy dở mà ai cũng khen. Cột trái là chỉ số quá trình, ví dụ một bài social từ 45 phút xuống 12 phút. Và đây là câu cảnh báo tôi muốn anh chị nhớ: đừng hứa với sếp là hệ thống này tăng doanh thu trong 2 tuần. Trong 2 tuần anh chị chứng minh được thời gian giảm và số lượng tăng. Doanh thu cần thêm chu kỳ. Hứa đúng cái đo được thì lần sau người ta còn tin anh chị."

**Hình minh họa gợi ý:** Hai cột, cột trái có biểu tượng đồng hồ, cột phải có biểu tượng đồ thị đi lên.

**Thời điểm:** Khối 1, phút 17 tới 20

---

### Slide 12: Buổi cuối rồi, anh chị mở hết ra

**Loại:** chuyển khối

**Nội dung hiển thị:**
- Thư mục làm việc, `CLAUDE.md`, tài sản cả năm buổi
- Tôi gõ gì thì anh chị gõ y hệt, trên bộ tài sản của chính mình
- Phút thứ 18 là phần quan trọng nhất cả buổi, tôi báo trước
- Đoạn đó không ai được ngồi xem

**Lời giảng viên nói khi chiếu slide này:** "Ba mươi lăm phút tới tôi đi đúng năm bước: gom tài sản, rút quy trình, viết Skill, thử Skill trên cái mới, và lên lịch 14 ngày. Bước thứ tư là bước quan trọng nhất, tôi sẽ báo trước khi tới. Ai bỏ bước đó thì đừng nộp bài."

**Hình minh họa gợi ý:** 5 ô nối mũi tên ngang, ô thứ tư to gấp rưỡi và tô đậm.

**Thời điểm:** Khối 2, phút 20

---

### Slide 13: Cấu trúc thư mục đề xuất

**Loại:** sơ đồ

**Nội dung hiển thị:**

```
thao-an-ai-system/
├── CLAUDE.md         hồ sơ thương hiệu, Claude tự đọc trước mọi việc
├── .claude/skills/   nơi skill chạy thật
├── 00-doc-truoc/     playbook.md · ke-hoach-14-ngay.md
├── 01-nen-tang/      hồ sơ sản phẩm · hook-cta · bài mẫu
├── 02-khach-hang/    insight · persona · content-angle
├── 03-ban-hang/      lead-scoring · email · kịch bản · proposal
├── 04-chien-dich/    campaign-brief · lich-14-ngay · nội dung đa kênh
├── 05-tu-dong-hoa/   automation-map · luồng post bài · checklist rủi ro
├── 06-skill/         bản đọc SKILL.md · tham chiếu
└── 99-luu-tru/       bản nháp cũ, không xóa nhưng không dùng
```

**Lời giảng viên nói khi chiếu slide này:** "Bốn quy tắc. Một: đánh số đầu thư mục để thứ tự không nhảy lung tung. Hai: tên file chữ thường, nối bằng gạch nối, nói rõ nội dung, insight-khach-hang tốt hơn insight-final-v3. Ba: không dùng chữ final, moi, v2; bản cũ đẩy vào thư mục lưu trữ. Bốn, và đây là chỗ hay nhầm: bản skill chạy thật nằm ở chấm claude gạch chéo skills ngay trong thư mục gốc, đúng như buổi 1. Thư mục 06-skill giữ một bản để người đọc. Thư mục bắt đầu bằng dấu chấm bị Windows ẩn đi, anh chị đừng tạo tay, bảo Claude tạo."

**Hình minh họa gợi ý:** Cây thư mục chiếm trọn slide. Nhánh `00-doc-truoc/` tô đậm.

**Thời điểm:** Khối 2, phút 20 tới 25

---

### Slide 14: PROMPT. Nhờ Claude đề xuất cấu trúc thư mục

**Loại:** prompt

**Nội dung hiển thị:**

```
Tôi vừa hoàn thành 5 buổi xây hệ thống AI Sale & Marketing.
Các đầu ra tôi đang có: [liệt kê đầu ra của cả 5 buổi]

Hãy đề xuất cấu trúc thư mục để một người mới vào công ty mở ra là tìm
được trong 10 giây. Yêu cầu:
- Giữ nguyên file CLAUDE.md và thư mục .claude/skills/ ở ngay gốc thư
  mục làm việc. Đây là hai chỗ Claude tự đọc, không được gói vào thư
  mục đánh số.
- Các thư mục còn lại đánh số đầu để giữ thứ tự.
- Tên file chữ thường, nối bằng gạch nối, nói rõ nội dung.
- Có một thư mục "đọc trước" chứa tài liệu người mới phải đọc đầu tiên.
- Có chỗ chứa bản nháp cũ, không xóa nhưng không lẫn vào bản đang dùng.
Trả về dạng cây thư mục, kèm 1 dòng giải thích mỗi thư mục.
```

**Lời giảng viên nói khi chiếu slide này:** "Anh chị dán danh sách đầu ra của chính mình vào chỗ trong ngoặc. Việc này chán nhất buổi hôm nay, nhưng bỏ qua nó thì mọi thứ phía sau vô nghĩa. Playbook hay tới đâu mà người ta không tìm được file thì cũng không ai dùng. Điểm dừng: tôi đọc tên 3 tài sản bất kỳ, anh chị mở được cả 3 file trong 10 giây không? Mở không được thì cấu trúc chưa đạt, sửa ngay."

**Hình minh họa gợi ý:** Khối code chiếm trọn slide. Góc phải có đồng hồ ghi "10 giây".

**Thời điểm:** Khối 2, phút 20 tới 25

---

### Slide 15: PROMPT. Rút quy trình đang làm bằng tay

**Loại:** prompt

**Nội dung hiển thị:**

```
Trong thư mục làm việc này, 5 buổi qua tôi đã dựng: nền dữ liệu thương
hiệu trong file CLAUDE.md và hồ sơ sản phẩm, skill viet-bai-ban-hang,
rồi 5 agent là Customer Insight, Content Engine, Outbound, Proposal,
Closer, cộng một luồng tự động hóa của buổi 5.

Hãy đọc các file system prompt và các đầu ra tôi đã lưu trong thư mục
này, rồi rút ra quy trình tôi đang làm bằng tay, viết dưới dạng các
bước đánh số.

Với mỗi bước ghi rõ:
- Tên bước
- Đầu vào: cần file hoặc thông tin gì mới chạy được
- Việc làm: mô tả bằng động từ, không dùng tính từ
- Đầu ra: kết quả cụ thể, đếm được
- Ai duyệt: bước nào bắt buộc người xem trước khi đi tiếp

Nếu chỗ nào bạn không đủ dữ liệu để rút ra, ghi thẳng "chưa đủ dữ liệu",
đừng suy đoán quy trình giúp tôi.
```

**Lời giảng viên nói khi chiếu slide này:** "Trước khi viết Skill, phải biết mình đang làm gì. Phần lớn mọi người không nói ra được quy trình của chính mình, nên ta nhờ Claude phỏng vấn ngược. Kết quả ra 5 tới 7 bước. Anh chị nhìn kỹ bước cuối: bước duyệt phải nằm trong quy trình, không phải nằm trong lời hứa. Cái gì không viết vào quy trình thì lúc gấp là bỏ qua đầu tiên. Và nếu Claude ghi chưa đủ dữ liệu ở đâu đó thì đó là agent làm đúng, nó không bịa hộ anh chị quy trình mà anh chị chưa từng làm."

**Hình minh họa gợi ý:** Khối code lớn. Bên phải là 6 ô đánh số nối dọc, ô cuối có hình người.

**Thời điểm:** Khối 2, phút 25 tới 30

---

### Slide 16: PROMPT. Viết Skill mới, phần 1

**Loại:** prompt

**Nội dung hiển thị:**

```
Mở file .claude/skills/viet-bai-ban-hang/SKILL.md tôi đã viết ở buổi 1
để xem lại cách tôi viết skill.

Bây giờ tạo cho tôi một skill mới, rộng hơn, phủ cả quy trình vừa rút
ở trên. Đường dẫn: .claude/skills/thao-an-sale-marketing/SKILL.md

Frontmatter viết theo đúng kiểu file cũ. Riêng dòng description phải
rộng hơn: liệt kê rõ từng loại yêu cầu sẽ kích hoạt skill này (bài
Facebook, mô tả Shopee, tin nhắn tư vấn inbox, email chào hàng sỉ, kịch
bản gọi khách spa, proposal bán sỉ, lịch nội dung, brief hình ảnh), kể
cả khi tôi chỉ gõ tên SKU kèm tên kênh. Nêu luôn một tình huống KHÔNG
dùng skill này.
```

**Lời giảng viên nói khi chiếu slide này:** "Prompt này gồm hai slide, anh chị copy cả hai phần rồi dán một lần. Anh chị đổi tên skill và danh sách loại đầu ra cho khớp ngành mình. Về dòng description tôi chỉ nói đúng một câu, vì buổi 1 đã dạy rồi: skill này rộng hơn nên dòng đó phải kể đủ các loại đầu ra, và phải nói rõ khi nào KHÔNG dùng."

**Hình minh họa gợi ý:** Khối code chiếm trọn slide. Góc dưới ghi "còn tiếp".

**Thời điểm:** Khối 2, phút 30 tới 33

---

### Slide 17: PROMPT. Viết Skill mới, phần 2 với bảy mục

**Loại:** prompt

**Nội dung hiển thị:**

```
Phần thân gồm đúng 7 mục sau. Bốn mục đầu là phần file cũ chưa có:

1. Vai trò: skill này đóng vai ai trong đội, tả bằng một ví von nghề
   nghiệp, kèm quy tắc xưng hô lấy từ CLAUDE.md.
2. Nguồn dữ liệu: liệt kê tên từng file nền trong thư mục này, ghi rõ
   file nào là nguồn sự thật cho giá, cho giọng văn, cho lời khách nói.
3. Tiêu chuẩn đầu ra: viết riêng cho TỪNG loại đầu ra kể trên. Mỗi dòng
   phải là con số hoặc câu kiểm được bằng mắt. Không dùng tính từ kiểu
   "hay", "hấp dẫn", "chuyên nghiệp".
4. Ranh giới không được vượt: ngoài danh sách từ cấm trong CLAUDE.md,
   ghi thêm việc gì skill không được tự quyết và việc gì bắt buộc người
   làm.
5. Quy trình từng bước: mỗi bước một việc, viết bằng động từ, ghi rõ
   đầu vào và đầu ra. Bước cuối là tự soát trước khi trả về.
6. Xử lý khi thiếu dữ liệu: gặp chỗ trống thì làm gì, theo thứ tự nào.
7. File tham chiếu: liệt kê đúng tên và đúng đường dẫn các file nền.

Ba nguyên tắc chống bịa đang nằm trong CLAUDE.md của thư mục này: chép
nguyên văn sang phần thân skill, không diễn đạt lại, không rút gọn.
```

**Lời giảng viên nói khi chiếu slide này:** "Điểm dừng dài nhất: ai chưa thấy file Skill hiện ra thì gõ CHỜ vào chat, tôi chờ tới 90 giây. Không có Skill thì cả chặng sau và cả phần nộp đều hụt. Anh chị chú ý câu cuối cùng của prompt: chép nguyên văn, không diễn đạt lại. Đây là điểm quan trọng nhất của buổi cuối, lát nữa tôi nói kỹ hơn."

**Hình minh họa gợi ý:** Khối code chiếm trọn slide. Bốn mục đầu tô nền nhạt.

**Thời điểm:** Khối 2, phút 33 tới 38

---

### Slide 18: Ba chỗ đọc kỹ khi Skill sinh ra

**Loại:** nội dung

**Nội dung hiển thị:**
- **Tiêu chuẩn đầu ra**: "dưới 250 chữ" kiểm được, "bài hay" thì không
- **Ranh giới**: không chỉ cấm chữ, còn cấm tự quyết chiết khấu
- **Ba nguyên tắc chống bịa**: phải nằm nguyên văn trong thân Skill

**Lời giảng viên nói khi chiếu slide này:** "Mỗi loại đầu ra một chuẩn riêng: bài Facebook một chuẩn, tin nhắn inbox một chuẩn, email chào sỉ một chuẩn. Buổi 1 anh chị mới viết chuẩn cho một loại. Người khác cầm skill này lên vẫn ra đúng chuẩn vì chuẩn viết bằng số. Còn ba nguyên tắc chống bịa: anh chị đã ghi trong CLAUDE.md từ buổi 1, nhưng CLAUDE.md chỉ đúng trong thư mục đó. Giờ nó nằm trong skill, mà skill thì mang đi được. Ai cầm skill cũng có nó, kể cả người chưa từng học khóa này. Điểm dừng: anh chị đọc to tiêu chuẩn của mình lên, có câu nào không đếm được không? Câu kiểu viết cho hấp dẫn là chưa đạt, sửa tại chỗ trước khi đi tiếp."

**Hình minh họa gợi ý:** 3 dòng, mỗi dòng có kính lúp ở đầu. Dòng cuối đóng khung đậm.

**Thời điểm:** Khối 2, phút 36 tới 38

---

### Slide 19: Phép thử quan trọng nhất. Mở một phiên MỚI

**Loại:** nội dung

**Nội dung hiển thị:**
- Skill chạy đúng trên ví dụ đã demo thì chưa nói lên gì
- Phải chạy đúng trên cái nó chưa từng thấy
- Mở phiên trò chuyện MỚI, vẫn ở thư mục làm việc đó
- Phiên cũ còn nhớ hết bối cảnh, chạy trong đó là tự lừa mình
- KHÔNG gọi tên skill trong prompt

**Lời giảng viên nói khi chiếu slide này:** "Đây là đoạn tôi báo trước từ đầu buổi, và đoạn này không ai được ngồi xem. Tôi cố ý không nhắc tên skill: nếu dòng description viết đúng thì Claude phải tự rút nó ra. Không tự rút ra được thì lỗi ở dòng đó, không phải lỗi ở phần thân."

**Hình minh họa gợi ý:** Hai cửa sổ chat, cửa sổ cũ mờ và gạch chéo, cửa sổ mới đậm.

**Thời điểm:** Khối 2, phút 38 tới 40

---

### Slide 20: PROMPT thử nghiệm 1. Gian hàng hội chợ

**Loại:** prompt

**Nội dung hiển thị:**

```
Tuần sau Thảo An có gian hàng ở hội chợ mỹ phẩm.
Soạn cho tôi:
- 1 tờ rơi A5 phát tại gian hàng, cho khách lẻ.
- 1 kịch bản chào 60 giây khi khách dừng lại xem.
- 1 tin nhắn gửi lại cho khách đã để số điện thoại, gửi sau hội chợ
  2 ngày.
```

**Lời giảng viên nói khi chiếu slide này:** "Chưa buổi nào dạy làm tờ rơi hay kịch bản hội chợ. Đó chính là điểm. Anh chị thay bằng một tình huống ngoài bối cảnh của ngành mình, ví dụ một buổi gặp khách hàng, một sự kiện, một kênh chưa từng chạy. Rồi chạy trên máy mình."

**Hình minh họa gợi ý:** Khối code lớn. Bên phải là ba khung đầu ra: tờ rơi, kịch bản, tin nhắn.

**Thời điểm:** Khối 2, phút 40 tới 44

---

### Slide 21: PROMPT thử nghiệm 2. Chứng minh không phải ăn may

**Loại:** prompt

**Nội dung hiển thị:**

```
Một spa ở Đà Nẵng nhắn hỏi: "Bên em nhập sỉ 50 chai serum thì giá bao
nhiêu, có hỗ trợ tư vấn cho nhân viên spa không?"
Soạn tin nhắn trả lời.
```

**Lời giảng viên nói khi chiếu slide này:** "Trước khi bấm gửi, tôi hỏi anh chị một câu, gõ vào chat: đoán xem nó có bịa cái chương trình đào tạo cho nhân viên spa không? Rồi ta cùng bấm. Kết quả đúng là: tin nhắn dùng đúng bảng chiết khấu trong chính sách giá sỉ, có nhãn nguồn, và gặp phần hỗ trợ tư vấn cho nhân viên spa mà chính sách không có thì phải ghi chưa đủ dữ liệu, cần xác nhận với người phụ trách, chứ không tự hứa."

**Hình minh họa gợi ý:** Khối code nhỏ. Bên dưới hai nhánh kết quả: một nhánh có dấu tích ghi "chưa đủ dữ liệu", một nhánh có dấu X ghi "tự hứa".

**Thời điểm:** Khối 2, phút 44 tới 47

---

### Slide 22: Kết quả đúng trông thế nào

**Loại:** nội dung

**Nội dung hiển thị:**
- Đúng giọng: xưng "Thảo An", gọi khách là "bạn", câu ngắn
- Không có từ cấm, không cam kết thời gian
- Có nhãn `[DATA THẬT]` ở giá và thành phần, `[SUY LUẬN]` ở phần phỏng đoán
- Có ít nhất một chỗ ghi "chưa đủ dữ liệu"
- Tin nhắn ghi rõ đây là nháp, cần người duyệt trước khi gửi

**Lời giảng viên nói khi chiếu slide này:** "Điểm dừng: kết quả trên máy anh chị có đối chiếu đúng bảng tiêu chuẩn đầu ra do chính anh chị viết không? Ai không đạt thì đó là dấu hiệu tiêu chuẩn viết chưa đo được, anh chị quay lại sửa Skill chứ không sửa kết quả. Nếu Skill của tôi bịa, và chuyện đó có thể xảy ra, thì càng tốt cho lớp: tôi sẽ chỉ ra chính xác câu bịa, thêm một dòng vào mục Xử lý khi thiếu dữ liệu, rồi chạy lại. Đây mới là cách người ta làm thật. Skill không đúng ngay lần đầu, nó đúng sau vòng thử thứ hai hoặc thứ ba."

**Hình minh họa gợi ý:** 5 ô tích, ô thứ tư đóng khung đậm.

**Thời điểm:** Khối 2, phút 44 tới 47

---

### Slide 23: Sơ đồ hệ thống, thứ anh chị gửi cho sếp

**Loại:** sơ đồ

**Nội dung hiển thị:**
- Mở đầu bằng khối 3 nguyên tắc: không bịa số, có nhãn nguồn, không tự gửi
- Luồng chính: `CLAUDE.md` và hồ sơ sản phẩm là nền dữ liệu
- Customer Insight ra persona và bảng nỗi lo
- Nhánh B2C qua Content Engine, nhánh B2B qua Outbound, Proposal, Closer
- Vòng lặp: review và tin nhắn mới nuôi lại bước Insight
- Ô cuối: "Đơn hoặc Hợp đồng, sau khi bạn duyệt"

**Lời giảng viên nói khi chiếu slide này:** "Từ nãy tới giờ là làm. Bây giờ là bán. Sếp không đọc Skill của anh chị. Khách cũng không. Họ nhìn một trang này trong 2 phút rồi quyết. Tôi trình bày mẫu đúng như anh chị sẽ phải làm ở khối demo chéo: 30 giây cho khối nguyên tắc, 90 giây cho luồng chính, 30 giây cho vòng lặp, 30 giây cho ô cuối, và phần chi tiết từng agent thì đưa link chứ không đọc lên. Mở đầu bằng ranh giới là cách nhanh nhất để người nghe hạ hàng phòng thủ. Một trang này thay được 15 slide. Ai làm agency thì đây chính là thứ gửi khách trước cuộc gặp, để cuộc gặp bắt đầu từ câu triển khai bao lâu chứ không phải câu AI là gì."

**Hình minh họa gợi ý:** Sơ đồ ngang: 1 ô nền dữ liệu, 1 ô Insight, tách hai nhánh B2C và B2B, chụm về ô cuối có chốt hình người. Mũi tên vòng lặp quay ngược về Insight.

**Thời điểm:** Khối 2, phút 47 tới 52

---

### Slide 24: PROMPT. Kế hoạch triển khai 14 ngày

**Loại:** prompt

**Nội dung hiển thị:**

```
Lập kế hoạch triển khai 14 ngày để đưa hệ thống này vào chạy thật.

Bối cảnh: [mô tả đội của anh chị, mấy người, ai làm gì, mục tiêu đang chạy]

Trả về bảng 4 cột: Ngày | Việc | Ai làm | Kết quả cần thấy.

Ràng buộc:
- Cột "Kết quả cần thấy" phải là thứ nhìn vào biết ngay đã xong hay
  chưa, không viết kiểu "hoàn thiện quy trình".
- Tuần 1 tập trung chạy thử trên số ít và sửa Skill. Tuần 2 mới mở rộng.
- Ngày 7 và ngày 14 phải có mốc kiểm, ghi rõ nhìn vào chỉ số nào.
- Ba chỉ số theo dõi bắt buộc: thời gian làm 1 đầu ra, số đầu ra mỗi
  tuần, tỉ lệ nháp được duyệt ngay lần đầu.
- Không xếp việc vào ngày nghỉ nếu tôi không nói có làm cuối tuần.
```

**Lời giảng viên nói khi chiếu slide này:** "Ra khỏi lớp mà không có lịch cụ thể thì 3 hôm sau mọi thứ nằm im. Hai chỗ tôi soi trong kết quả. Một, ngày 1 và ngày 2 phải làm được ngay chiều nay hoặc sáng mai; kế hoạch nào mà ngày 1 đã cần họp với 3 phòng ban thì kế hoạch đó chết từ ngày 1. Hai, cột ai làm phải ghi tên người, không ghi team. Việc không có tên là việc không xảy ra."

**Hình minh họa gợi ý:** Khối code lớn. Bên phải là bảng 4 cột với 14 dòng để trống, dòng 7 và 14 tô đậm.

**Thời điểm:** Khối 2, phút 52 tới 55

---

### Slide 25: Đề bài chặng 1. Gom tài sản và viết Skill

**Loại:** thực hành

**Nội dung hiển thị:**
- Mở `workbook/buoi-06-claude-skill-va-playbook.md`
- 14 phút: gom tài sản 5 buổi vào đúng cấu trúc thư mục, đổi tên file
- 16 phút: rút quy trình, viết tiêu chuẩn đầu ra, sinh file Skill
- Tiêu chuẩn đầu ra phải viết bằng số hoặc câu kiểm được bằng mắt
- Ba nguyên tắc chống bịa chép nguyên văn vào thân Skill

**Lời giảng viên nói khi chiếu slide này:** "Slide này đứng nguyên suốt 30 phút, anh chị vừa làm vừa liếc lại. Phần gom tài sản là việc chán nhất buổi, tôi biết, nhưng bỏ qua thì Playbook vô dụng. Tôi sẽ gọi từng người chia sẻ màn hình và làm đúng một phép thử: tôi đọc tên 3 tài sản bất kỳ, anh chị mở được cả 3 file trong 10 giây không."

**Hình minh họa gợi ý:** Số 30 cỡ rất lớn kèm đồng hồ. Hai vạch chia 14 và 16 phút.

**Thời điểm:** Khối 3a, phút 55 tới 85

---

### Slide 26: Còn 10 phút. Anh chị đang ở đâu

**Loại:** thực hành

**Nội dung hiển thị:**
- Còn 10 phút là hết chặng 1
- Mức tối thiểu trước khi nghỉ: file Skill đã sinh ra
- Chưa có Skill thì bỏ phần đổi tên file, sinh Skill trước
- Gõ vào chat: 1 nếu đã có file Skill, 2 nếu chưa

**Lời giảng viên nói khi chiếu slide này:** "Tôi hỏi để biết ai đang hụt. Ai gõ 2 thì bỏ ngay phần sắp xếp file, tập trung sinh Skill, sắp xếp làm sau. Cả chặng 2 và cả phần nộp đều dựa vào file Skill này. Ai chưa xong thì ở lại trong giờ nghỉ, tôi gỡ cùng."

**Hình minh họa gợi ý:** Số 10 cỡ rất lớn kèm đồng hồ đếm ngược.

**Thời điểm:** Khối 3a, phút 75

---

### Slide 27: Giải lao 10 phút

**Loại:** chuyển khối

**Nội dung hiển thị:**
- Nghỉ 10 phút
- Đúng phút thứ 95 anh chị quay lại
- Ai chưa sinh được file Skill thì ở lại, tôi gỡ cùng
- Đừng tắt Claude Desktop

**Lời giảng viên nói khi chiếu slide này:** "Anh chị nghỉ 10 phút, tôi để đồng hồ đếm ngược trên màn hình chia sẻ. Điểm dừng đúng chỗ: file Skill đã sinh ra, chưa vào phần thử Skill. Ai chưa có thì ở lại với tôi, vì cả phần sau dựa vào nó."

**Hình minh họa gợi ý:** Đồng hồ đếm ngược cỡ rất lớn ở giữa.

**Thời điểm:** Giải lao, phút 85 tới 95

---

### Slide 28: Đề bài chặng 2. Thử Skill và viết Playbook

**Loại:** thực hành

**Nội dung hiển thị:**
- 8 phút: thử Skill trên yêu cầu mới, mở phiên MỚI, không gọi tên skill
- Chạy đủ 2 phép thử ngoài bối cảnh gốc
- 17 phút: viết Playbook đủ 7 mục và kế hoạch 14 ngày
- Lệch chuẩn thì sửa Skill, không sửa kết quả

**Lời giảng viên nói khi chiếu slide này:** "Slide này đứng nguyên suốt 25 phút. Bước thử Skill là bước tôi không cho ai bỏ. Nếu kết quả lệch chuẩn thì nguyên nhân thường là Skill mô tả theo tình huống cụ thể thay vì mô tả theo bước. Anh chị sửa bằng cách viết lại các bước ở dạng chung, đẩy phần cụ thể xuống file tham chiếu. Ai không kịp thì Playbook rút xuống 2 trang, đủ 4 câu trả lời bắt buộc là đạt: làm theo thứ tự nào, đầu ra thế nào là đạt, agent không được làm gì, nhìn vào số nào để biết có tác dụng."

**Hình minh họa gợi ý:** Số 25 cỡ rất lớn kèm đồng hồ. Hai vạch chia 8 và 17 phút.

**Thời điểm:** Khối 3b, phút 95 tới 120

---

### Slide 29: Demo chéo. Năm phút, mỗi phút một việc

**Loại:** bảng

**Nội dung hiển thị:**

| Phút | Nói gì | Sai lầm hay gặp |
|---|---|---|
| 1 | **Bài toán.** Trước mất bao lâu, ai làm, đau ở đâu. Nói bằng con số | Kể lể dài dòng về công ty |
| 2 | **Cách làm.** Hệ thống gồm gì, mấy bước. Mở sơ đồ, 3 giây mỗi khối | Đọc từng dòng system prompt |
| 3 | **Chạy thử.** Gõ một yêu cầu thật, chờ kết quả ra trước mắt người xem | Chiếu kết quả chuẩn bị sẵn |
| 4 | **Kết quả.** Đọc to 1 đầu ra tốt nhất, chỉ ra nhãn nguồn | Khoe tính năng công cụ |
| 5 | **Kế hoạch tiếp.** 14 ngày tới làm gì, ai làm, nhìn chỉ số nào | Kết bằng "em xong rồi ạ" |

**Lời giảng viên nói khi chiếu slide này:** "Anh chị chia cặp hoặc nhóm ba, bấm giờ nghiêm, quá 5 phút là chưa đạt. Người nghe không quan tâm anh chị dùng công cụ gì. Họ quan tâm việc này trước mất 45 phút, giờ mất 12 phút, và kết quả có dám gửi khách không. Nếu ai sa đà khoe công cụ thì bạn cùng nhóm bấm chuông ở phút thứ 2 và bắt chuyển sang chạy thật ngay."

**Hình minh họa gợi ý:** Đồng hồ 5 vạch, mỗi vạch một nhãn ngắn.

**Thời điểm:** Khối 4 Demo chéo, phút 120 tới 130

---

### Slide 30: Rubric chấm, tổng 12 điểm

**Loại:** bảng

**Nội dung hiển thị:**

| # | Tiêu chí | 2 điểm khi |
|---|---|---|
| 1 | Bài toán rõ | Có con số trước và sau |
| 2 | Skill chạy được thật | Chạy ngay, ra đúng chuẩn |
| 3 | Chất lượng đầu ra | Cụ thể, chỉ thương hiệu này viết được |
| 4 | Ba nguyên tắc chống bịa | Nằm trong Skill, đầu ra có nhãn nguồn |
| 5 | Playbook bàn giao được | Đủ 7 mục, người lạ đọc là làm được |
| 6 | Kế hoạch 14 ngày | Đủ ngày, việc, người làm, kết quả cần thấy |

Từ 10 điểm là đạt. Từ 7 tới 9 thì sửa rồi nộp lại. Dưới 7 thì làm lại phần yếu nhất.

**Lời giảng viên nói khi chiếu slide này:** "Người cùng nhóm chấm, ghi vào workbook của người trình bày. Tiêu chí số 4 là tiêu chí tôi để ý nhất: nhắc miệng nhưng không có trong Skill chỉ được 1 điểm. Trí nhớ không bàn giao được. Tiêu chí số 3 dùng lại phép thử đổi tên của buổi 1: thay tên thương hiệu vào mà đầu ra vẫn đúng thì đó là 0 điểm."

**Hình minh họa gợi ý:** Bảng 6 dòng, cột điểm hiện ba mức 0, 1, 2 dạng ba ô nhỏ.

**Thời điểm:** Khối 4, phút 120 tới 130

---

### Slide 31: Sáu thứ anh chị nộp hôm nay

**Loại:** bảng

**Nội dung hiển thị:**

| # | Sản phẩm | Đạt khi |
|---|---|---|
| 1 | Claude Skill | Đúng đường dẫn, đủ 7 mục, có 3 nguyên tắc chống bịa nguyên văn |
| 2 | AI Agent Playbook | Đủ 7 mục |
| 3 | Bộ tài sản sắp xếp | Đúng cấu trúc, tìm được trong 10 giây |
| 4 | Automation hoặc prototype | Kế thừa buổi 5, có bước người duyệt |
| 5 | Demo agent 5 phút | Đã chấm theo rubric, từ 10 điểm |
| 6 | Kế hoạch 14 ngày | Đủ 4 cột, có tên người thật |

**Lời giảng viên nói khi chiếu slide này:** "Đúng sáu mục, không thiếu, không thừa. Mục 1 tôi nhắc lại đường dẫn: chấm claude gạch chéo skills gạch chéo tên skill gạch chéo SKILL chấm md, đúng như buổi 1. Mục 6 phải có tên người thật, không có ai khác thì ghi tên mình."

**Hình minh họa gợi ý:** 6 ô vuông trống để tích, xếp 2 hàng 3 cột.

**Thời điểm:** Khối 5, phút 130 tới 140

---

### Slide 32: Năm trường hợp chưa đạt

**Loại:** nội dung

**Nội dung hiển thị:**
- Skill không có 3 nguyên tắc chống bịa trong phần thân
- Skill chạy trên yêu cầu mới thì lệch chuẩn, và chưa sửa
- Playbook thiếu mục tiêu chuẩn đầu ra hoặc mục ranh giới
- Kế hoạch 14 ngày không có tên người hoặc không có chỉ số
- Đầu ra trong demo có số liệu không tìm được trong file nguồn

**Lời giảng viên nói khi chiếu slide này:** "Dòng đầu tiên là lỗi nặng nhất của buổi cuối. Có anh chị sẽ nói cái đó em nhớ rồi, lúc chạy em tự nhắc. Tôi nói thẳng: trí nhớ không bàn giao được. Anh chị dán nguyên khối ba nguyên tắc vào phần thân Skill, và thêm một dòng vào tiêu chuẩn đầu ra là mọi số liệu phải có nhãn nguồn."

**Hình minh họa gợi ý:** 5 dòng, mỗi dòng có dấu X ở đầu, dòng thứ nhất to hơn.

**Thời điểm:** Khối 5, phút 140 tới 144

---

### Slide 33: Ba tầng anh chị mang về

**Loại:** nội dung

**Nội dung hiển thị:**
- **Tầng 1**: bộ tài sản dùng ngay được cho 14 ngày tới
- **Tầng 2**: Skill và Playbook, cả đội dùng lại được, người mới đọc là làm được
- **Tầng 3**: nếu làm agency hoặc freelancer, đây là một gói dịch vụ bán được

**Lời giảng viên nói khi chiếu slide này:** "Tôi chiếu lại bảng 6 buổi và đọc to danh sách những gì anh chị đã làm ra: từ một hồ sơ sản phẩm ban đầu, tới hơn 40 đầu ra, tới một Skill đóng gói được. Và tôi nói một câu: không ai trong phòng này viết một dòng code nào. Tầng 3 tôi nói riêng cho anh chị làm agency: khách mua quy trình có tiêu chuẩn, không mua mẹo prompt."

**Hình minh họa gợi ý:** Ba tầng xếp chồng, tầng dưới rộng nhất.

**Thời điểm:** Khối 5, phút 144 tới 147

---

### Slide 34: Ba con số báo lại sau 14 ngày

**Loại:** nội dung

**Nội dung hiển thị:**
1. Thời gian làm 1 đầu ra
2. Số đầu ra mỗi tuần
3. Tỉ lệ nháp được duyệt ngay lần đầu

Hẹn mốc kiểm lại sau 14 ngày.

**Lời giảng viên nói khi chiếu slide này:** "Trước khi kết, mỗi anh chị đọc to ngày 1 và ngày 2 trong kế hoạch của mình vào chat hoặc bật mic đọc lên. Đọc ra miệng thì tỉ lệ làm cao hơn hẳn. Rồi ta hẹn một mốc kiểm lại sau 14 ngày, mỗi người báo đúng ba con số này. Không báo doanh thu, vì doanh thu cần thêm chu kỳ."

**Hình minh họa gợi ý:** 3 ô số lớn để trống, bên dưới là lịch có ngày 14 khoanh tròn.

**Thời điểm:** Khối 5, phút 147 tới 149

---

### Slide 35: Câu cuối cùng của khóa

**Loại:** chuyển khối

**Nội dung hiển thị:**
- Hệ thống này không thay anh chị ra quyết định
- Nó bỏ giúp phần lặp lại, để anh chị dồn thời gian vào phần chỉ người làm được
- Chọn hướng, duyệt nội dung, nói chuyện với khách
- Ba nguyên tắc chống bịa giữ nguyên, và giờ nó nằm trong Skill của anh chị

**Lời giảng viên nói khi chiếu slide này:** "Ba nguyên tắc chống bịa giữ nguyên từ buổi 1: chỉ dùng dữ liệu anh chị cấp, gắn nhãn nguồn, anh chị duyệt cuối. Hôm nay ba nguyên tắc đó đã nằm trong Skill của anh chị, nên nó không phụ thuộc trí nhớ ai nữa. Đó là khác biệt giữa một người dùng AI giỏi và một đội có hệ thống. Cảm ơn anh chị đã đi cùng tôi sáu buổi."

**Hình minh họa gợi ý:** Một người và một bánh răng đứng cạnh nhau, mũi tên từ bánh răng chỉ vào phần việc lặp lại, mũi tên từ người chỉ vào phần quyết định.

**Thời điểm:** Khối 5, phút 149 tới 150
