# Nội dung slide Buổi 03: Sales Agent

**Khóa:** AI Agent cho Sale & Marketing
**Hình thức:** online live qua Zoom hoặc Meet
**Thời lượng buổi:** 150 phút
**Tổng số slide:** 37 slide, trong đó 22 slide nội dung và bảng, 10 slide prompt, 3 slide đề bài và mốc thời gian, 1 slide bìa, 1 slide giải lao
**Giáo án nguồn:** `giao-an/buoi-03-sales-agent.md`
**Kịch bản demo nguồn:** `so-tay-giang-vien/buoi-03-sales-agent.md`
**Ma trận mục tiêu:** `00-tong-quan/ma-tran-muc-tieu.md` mục tiêu 3.1 tới 3.5

## Ghi chú thiết kế chung

- Nền trắng, chữ đậm, cỡ chữ tối thiểu 28pt vì lớp học qua màn hình chia sẻ
- Slide prompt để chữ cỡ lớn trong khối code, học viên nhìn màn hình chia sẻ gõ theo được
- Mỗi slide một thông điệp, tối đa 6 dòng
- Phần "Lời giảng viên nói khi chiếu slide này" KHÔNG in lên slide
- Màu, logo, font do bước đóng gói áp vào, không ghi ở đây

---

### Slide 1: Buổi 3. Sales Agent

**Loại:** tiêu đề

**Nội dung hiển thị:**
- AI Agent cho Sale & Marketing
- Buổi 3 trên 6
- Email, tin nhắn, kịch bản gọi và proposal thật
- 150 phút

**Lời giảng viên nói khi chiếu slide này:** "Chào anh chị. Buổi này giải quyết đúng một câu hỏi mà sale nào cũng loay hoay mỗi sáng: gọi ai trước, và mở lời thế nào. Hết buổi anh chị có một dây chuyền ba agent: chấm điểm lead, soạn đề xuất, và chuẩn bị sẵn cách xử lý từ chối."

**Hình minh họa gợi ý:** Ba ô nối bằng mũi tên ngang, mỗi ô một biểu tượng: bảng điểm, tài liệu, bong bóng thoại.

**Thời điểm:** Khối 1 Framework, phút 0

---

### Slide 2: Hết buổi hôm nay anh chị làm được gì

**Loại:** nội dung

**Nội dung hiển thị:**
- Tự viết bộ tiêu chí chấm lead của mình, tổng trọng số bằng 100
- Áp bộ đó lên 10 lead thô, ra bảng có cột lý do và cột độ tin cậy
- Viết 10 email và 10 tin nhắn bám ghi chú trao đổi thật
- Dựng proposal 3 tới 5 trang đúng chính sách giá
- Chỉ đúng chỗ agent phải dừng khi khách hỏi điều chưa có chính sách

**Lời giảng viên nói khi chiếu slide này:** "Dòng cuối là dòng tôi coi trọng nhất. Cuối buổi tôi sẽ cho anh chị chạy một ca thật: khách đòi độc quyền khu vực, thứ chưa có trong chính sách. Đạt là khi proposal của anh chị để trống mục đó và ghi rõ cần xin ý kiến, chứ không tự hứa một con số. Agent nào tự chế ra một mức chiết khấu là agent đã hỏng."

**Hình minh họa gợi ý:** 5 ô vuông trống để tích, ô cuối đóng khung đậm.

**Thời điểm:** Khối 1, phút 1

---

### Slide 3: Ba file anh chị phải có trong thư mục làm việc

**Loại:** bảng

**Nội dung hiển thị:**

| Cần có | Nội dung tối thiểu |
|---|---|
| Danh sách lead | 10 dòng: tên cơ sở, loại hình, khu vực, kênh liên hệ, người phụ trách, ghi chú trao đổi |
| Chính sách giá | Bảng chiết khấu theo số lượng, điều khoản thanh toán và vận chuyển, danh sách điều chưa có chính sách |
| Lịch sử trao đổi | Ghi chú thật của từng lead, nguyên văn càng tốt |

**Lời giảng viên nói khi chiếu slide này:** "Ba file này chép vào chính thư mục làm việc buổi 1, cùng chỗ với CLAUDE.md. Claude tự đọc, anh chị không phải đính kèm gì. Ai chưa có CRM thì mở inbox Facebook và Zalo, gom tay 10 hội thoại gần nhất. Ai chưa có chính sách giá thì viết ra bốn mức, mất 10 phút. Và một câu nhắc quan trọng: cột ghi chú để trống là chấp nhận được, trống thì agent hạ độ tin cậy. Điền bừa cho đẹp bảng là tự phá bài của mình. Ai chưa có gì cả thì dùng nguyên bộ Thảo An trong `demo/thao-an/`, ra sản phẩm y hệt."

**Hình minh họa gợi ý:** Ba biểu tượng file rơi vào một thư mục chung, cạnh biểu tượng `CLAUDE.md` đã có sẵn.

**Thời điểm:** Khối 1, phút 2

---

### Slide 4: Hôm nay đứng trên hai buổi trước

**Loại:** nội dung

**Nội dung hiển thị:**
- Buổi 1: `CLAUDE.md`, giọng văn, danh sách từ cấm, cách dựng skill
- Buổi 2: `insight-khach-hang.md`, persona đặt tên theo nỗi lo
- Persona hôm nay dùng để cá nhân hóa email
- Email cho "người từng bị kích ứng" khác hẳn email cho "người đang so giá"

**Lời giảng viên nói khi chiếu slide này:** "Buổi 2 anh chị dựng ba persona đặt tên theo nỗi lo. Hôm nay ba persona đó có việc làm: nó quyết định email mở lời thế nào. Ai vắng buổi 2 thì vẫn học được, dùng bộ Thảo An, nhưng anh chị sẽ thiếu phần cá nhân hóa theo nỗi lo thật của khách mình."

**Hình minh họa gợi ý:** Hai mũi tên từ ô Buổi 1 và ô Buổi 2 chụm vào ô Buổi 3.

**Thời điểm:** Khối 1, phút 3

---

### Slide 5: Nhịp buổi hôm nay

**Loại:** bảng

**Nội dung hiển thị:**

| Khối | Phút | Việc |
|---|---|---|
| 1 | 20 | Framework, chỉ nghe |
| 2 | 35 | Demo làm theo, anh chị gõ cùng tôi |
| 3a | 30 | Anh chị làm, chặng 1 |
| Nghỉ | 10 | Giải lao |
| 3b | 25 | Anh chị làm, chặng 2 |
| 4 | 10 | Chấm chéo theo cặp |
| 5 | 20 | Hoàn thiện và nộp |

**Lời giảng viên nói khi chiếu slide này:** "Hai mươi phút đầu chỉ nghe. Từ khối 2 trở đi anh chị gõ liên tục. Ai chưa có 10 lead của mình thì mở bộ 10 lead sỉ Thảo An ra, chạy trên bộ đó, ra sản phẩm y hệt. Tôi báo trước mức đạt tối thiểu nếu anh chị không kịp: bảng chấm điểm 10 lead cộng 3 email, phần còn lại làm ở nhà."

**Hình minh họa gợi ý:** Thanh ngang chia 7 đoạn theo tỉ lệ thời lượng.

**Thời điểm:** Khối 1, phút 4

---

### Slide 6: Vì sao chia 3 agent thay vì nhồi vào 1

**Loại:** nội dung

**Nội dung hiển thị:**
- Ba việc cần ba thái độ khác nhau
- Chấm điểm cần lạnh và nhất quán; proposal cần bám chính sách; từ chối cần mềm
- Sai ở đâu sửa ở đó, không đụng phần khác
- Đầu ra cái này là đầu vào cái kia
- Chia được agent thì chia được người
- Mỗi agent một file skill, tuần sau gõ một câu là chạy lại

**Lời giảng viên nói khi chiếu slide này:** "Nhồi cả quy trình sale vào một prompt dài thì agent làm việc gì cũng nửa vời. Một prompt ôm cả ba thái độ thì thái độ trộn lẫn, agent bắt đầu chấm điểm có cảm xúc. Còn dòng cuối: mỗi agent lưu một file SKILL.md riêng, giống hệt buổi 1. Ba file này cũng là ba mảnh của bộ bàn giao mà buổi 6 sẽ gom lại."

**Hình minh họa gợi ý:** Bên trái một ô to nhồi 3 biểu tượng chồng lên nhau, gạch chéo. Bên phải 3 ô tách rời, có dấu tích.

**Thời điểm:** Khối 1, phút 4 tới 11

---

### Slide 7: Dây chuyền ba agent

**Loại:** sơ đồ

**Nội dung hiển thị:**

```
Danh sách lead thô
      ↓
[skill lead-scoring]        →  bảng điểm + xếp nhóm
      ↓  (lead nhóm A)
[skill soan-proposal]       →  đề xuất + bảng báo giá + email cover
      ↓  (khách phản hồi)
[skill theo-duoi-chot-don]  →  timeline follow-up + xử lý từ chối
```

**Lời giảng viên nói khi chiếu slide này:** "Ba file nằm ở chấm claude gạch chéo skills, mỗi skill một thư mục con, y hệt cách buổi 1 làm. Anh chị nhìn hai mũi tên có chú thích trong ngoặc: đó là điều kiện chuyển giai đoạn. Chỉ lead nhóm A mới đi tiếp sang proposal. Chưa có phản hồi của khách thì chưa chạy agent thứ ba."

**Hình minh họa gợi ý:** Sơ đồ dọc 3 khối, mũi tên có nhãn điều kiện, mỗi khối gắn biểu tượng file SKILL.md.

**Thời điểm:** Khối 1, phút 8 tới 11

---

### Slide 8: Người đặt tiêu chí, agent chỉ áp công thức

**Loại:** nội dung

**Nội dung hiển thị:**
- Để agent tự nghĩ tiêu chí thì mỗi lần chạy ra một kiểu
- Sếp hỏi "vì sao lead này trên lead kia" thì không giải thích được
- Anh chị điền xong bảng tiêu chí rồi mới mở Claude
- Prompt phải chứa nguyên bảng đó

**Lời giảng viên nói khi chiếu slide này:** "Đây là nguyên tắc gốc của khối này, và cũng là lỗi số một tôi thấy ở lớp. Nhiều người gõ chấm điểm 10 lead này giúp tôi rồi lấy nguyên kết quả. Agent sẽ ra một bộ tiêu chí nghe rất hay nhưng lần chạy sau lại khác. Câu tôi muốn anh chị nhớ: agent là máy tính, không phải người quyết định."

**Hình minh họa gợi ý:** Hai bàn tay, một tay cầm bảng tiêu chí, tay kia là bánh răng máy tính. Mũi tên đi từ tay người sang bánh răng.

**Thời điểm:** Khối 1, phút 11 tới 13

---

### Slide 9: Bộ tiêu chí mẫu, tổng trọng số 100

**Loại:** bảng

**Nội dung hiển thị:**

| Tiêu chí | Trọng số | 5 điểm | 1 điểm |
|---|---|---|---|
| A. Quy mô đơn dự kiến | 25% | Đại lý, từ 300 sp | Dưới đơn tối thiểu |
| B. Độ khớp định vị | 25% | Khách nói thẳng cần dòng lành tính | Tệp khách lệch hẳn |
| C. Mức độ quan tâm | 30% | Hỏi giá từ 2 lần | Chưa phản hồi lần nào |
| D. Khả năng chốt 30 ngày | 20% | Người quyết là chủ | Chưa rõ ai phụ trách |

`Điểm = (A×0,25 + B×0,25 + C×0,30 + D×0,20) × 20`

**Lời giảng viên nói khi chiếu slide này:** "Đây là bộ mẫu cho Thảo An, không phải bộ của anh chị. Lát nữa anh chị viết bộ của mình. Bảng đầy đủ có cả mốc 4, 3, 2 điểm, nằm trong workbook. Công thức nhân 20 ở cuối là để quy về thang 100 cho dễ nói chuyện với sếp."

**Hình minh họa gợi ý:** Bảng chiếm phần lớn slide. Cột trọng số vẽ thêm thanh ngang dài ngắn theo tỉ lệ 25, 25, 30, 20.

**Thời điểm:** Khối 1, phút 13 tới 16

---

### Slide 10: Vì sao trọng số đặt như thế

**Loại:** nội dung

**Nội dung hiển thị:**
- **C nặng nhất 30%**: đó là dữ liệu quan sát được, không phải phán đoán
- **A và B bằng nhau 25%**: đơn to mà lệch định vị thì bán một lần rồi thôi
- **D nhẹ nhất 20%**: khó chốt không có nghĩa là không đáng theo, chỉ là xếp sau

**Lời giảng viên nói khi chiếu slide này:** "Đây là phần dạy nghề, không phải dạy công cụ. Khách chủ động hỏi giá hai lần là hành vi thật, ai cũng nhìn thấy như nhau. Còn quy mô đơn dự kiến thì phần lớn là ta đoán từ loại hình cơ sở. Ba dòng này chính là câu trả lời khi có người hỏi anh chị vì sao tiêu chí này nặng hơn tiêu chí kia. Lát nữa lúc chấm chéo, bạn bên cạnh sẽ hỏi anh chị đúng câu đó."

**Hình minh họa gợi ý:** 3 dòng, mỗi dòng có tỉ trọng vẽ bằng hình tròn to nhỏ khác nhau.

**Thời điểm:** Khối 1, phút 16 tới 18

---

### Slide 11: Cột độ tin cậy quan trọng ngang cột điểm

**Loại:** bảng

**Nội dung hiển thị:**

| Lead | A | B | C | D | Điểm | Độ tin cậy |
|---|---|---|---|---|---|---|
| L01 Spa An Nhiên | 3 | 5 | 5 | 5 | 90 | Cao |
| L04 Chuỗi Beauty House | 4 | 4 | 5 | 2 | 78 | Cao |
| L03 Spa Hương Sen | 3 | 4 | 2 | 1 | 51 | **Thấp** |

**Lời giảng viên nói khi chiếu slide này:** "Anh chị nhìn L03. Ba trong bốn tiêu chí chấm bằng suy luận từ loại hình cơ sở, không có ghi chú trao đổi nào ngoài hỏi bảng giá. Cộng thêm chưa rõ người phụ trách. Nên độ tin cậy phải hạ xuống Thấp. Việc cần làm với lead này không phải gửi proposal, mà là đi tìm đúng người trước. Chốt: điểm 51 tin cậy Cao là một việc, điểm 51 tin cậy Thấp là việc khác hẳn. Và một dấu hiệu tôi luôn để ý khi chấm bài: bảng nào 10 dòng đều tin cậy Cao là bảng đang bịa."

**Hình minh họa gợi ý:** Bảng 3 dòng, ô "Thấp" tô nền đậm.

**Thời điểm:** Khối 1, phút 18 tới 20

---

### Slide 12: Ba nhóm việc agent tuyệt đối không tự quyết

**Loại:** nội dung

**Nội dung hiển thị:**
1. **Giá và chiết khấu.** Chỉ dùng đúng 4 mức trong bảng: 25%, 35%, 42%, 48%
2. **Cam kết.** Thời gian giao, công dụng, thời gian có kết quả, quyền đổi trả
3. **Ưu đãi và điều kiện hợp tác.** Độc quyền khu vực, chiết khấu vượt 48%, ký gửi, hỗ trợ marketing tại điểm bán

Câu duy nhất agent được nói khi chạm hàng rào: "Việc này cần xin ý kiến chủ doanh nghiệp, tôi ghi nhận và phản hồi anh chị trong 2 ngày làm việc."

**Lời giảng viên nói khi chiếu slide này:** "Mục Điều CHƯA có chính sách trong file giá không phải phần thừa. Đó là hàng rào. Nên trong ba file skill của anh chị, file nào cũng phải có một mục tên là ranh giới, liệt kê thẳng ra: cái gì agent được trả lời, cái gì agent phải dừng. Tôi đưa luôn ca thật mà lát nữa ta chạy: lead L07 Minh Phát đang hỏi độc quyền khu vực Nghệ An và xin chiết khấu cao hơn bảng chuẩn. Agent nào tự chế ra mức 52 phần trăm cho L07 là agent đã hỏng, và anh chị phải nhìn ra ngay trong demo."

**Hình minh họa gợi ý:** Hàng rào vẽ ngang giữa slide. Ba biển báo dừng cắm trên hàng rào.

**Thời điểm:** Khối 1, phút 15 tới 20

---

### Slide 13: 35 phút tới anh chị gõ cùng tôi

**Loại:** chuyển khối

**Nội dung hiển thị:**
- Mở thư mục làm việc, đặt tay lên bàn phím
- Lưu đủ 3 file skill trước rồi mới làm việc gì
- Mỗi skill chạy trong một phiên riêng
- Bốn điểm dừng, tôi chờ hai phần ba lớp

**Lời giảng viên nói khi chiếu slide này:** "Ba mươi lăm phút tới tôi gõ gì thì anh chị gõ y hệt trên máy mình. Một lỗi tôi muốn chặn ngay từ đầu: đừng dán prompt vào chat cho nhanh rồi bỏ qua việc lưu thành file skill. Làm vậy thì hết buổi là mất sạch. Và đừng nhồi ba việc vào một phiên: chấm điểm xong gõ tiếp giờ viết proposal luôn thì đến câu thứ ba mươi agent quên bảng tiêu chí và bắt đầu chấm lại theo cảm tính. Chậm hơn hai phút, sạch hơn nhiều, và tuần sau còn dùng lại được."

**Hình minh họa gợi ý:** 3 cửa sổ phiên tách rời, mỗi cửa sổ gắn một tên skill.

**Thời điểm:** Khối 2, phút 20

---

### Slide 14: PROMPT. Bắt agent tự khai nó thiếu gì

**Loại:** prompt

**Nội dung hiển thị:**

```
Đọc san-pham-thao-an.md và danh-sach-lead-si.md trong thư mục làm việc.
Đây là dữ liệu nền của Thảo An. Xác nhận, chưa làm gì thêm.

Xác nhận theo mẫu:
1. Bạn đọc được bao nhiêu lead.
2. Lead nào thiếu thông tin người phụ trách.
3. Ba loại dữ liệu nào KHÔNG có trong file mà việc chấm điểm lead
   thường cần.
```

**Lời giảng viên nói khi chiếu slide này:** "Kết quả đúng: 10 lead; L03 và L08 thiếu người phụ trách; ba thứ thiếu là doanh số hoặc lượng khách mỗi tháng, ngân sách nhập hàng, và họ đang nhập của ai với giá bao nhiêu. Câu hỏi số 3 quan trọng nhất. Tôi bắt agent tự khai nó thiếu gì trước khi cho nó làm việc. Agent nào trả lời dữ liệu đầy đủ là agent sắp bịa. Đây là bước 30 giây, đừng bỏ."

**Hình minh họa gợi ý:** Khối code lớn. Bên dưới ba ô trống có dấu hỏi, nhãn "ba chỗ agent phải tự khai".

**Thời điểm:** Khối 2, phút 20 tới 22

---

### Slide 15: PROMPT. Chấm điểm 10 lead, phần 1

**Loại:** prompt

**Nội dung hiển thị:**

```
Chấm điểm 10 lead theo ĐÚNG bộ tiêu chí dưới. Không tự thêm, không
tự bớt tiêu chí.

Thang 1 đến 5 cho mỗi tiêu chí.

A. Quy mô đơn dự kiến (trọng số 25%)
5 = đại lý, từ 300 sp/đơn | 4 = chuỗi, 100 đến 299 | 3 = spa hoặc
cửa hàng lẻ, 30 đến 99 | 2 = tiệm nhỏ, 10 đến 29 | 1 = dưới đơn tối
thiểu hoặc không đoán được

B. Độ khớp định vị lành tính, thảo mộc Việt, tầm trung (trọng số 25%)
5 = khách nói thẳng cần dòng lành tính hoặc thiên nhiên | 4 = tệp
khách chắc chắn khớp | 3 = khớp một phần | 2 = khớp yếu | 1 = lệch hẳn

C. Mức độ quan tâm thể hiện qua trao đổi (trọng số 30%)
5 = hỏi giá từ 2 lần, hoặc xin hồ sơ để duyệt nội bộ | 4 = chủ động
hỏi 1 lần có nội dung cụ thể | 3 = từng mua nhưng chưa quay lại
2 = mới nhắn hỏi chung chung | 1 = chưa phản hồi

D. Khả năng chốt trong 30 ngày (trọng số 20%)
5 = người quyết là chủ, không có quy trình duyệt | 4 = chủ nhưng còn
vướng điều kiện | 3 = có người phụ trách nhưng phải trình duyệt
2 = quy trình duyệt dài hoặc yêu cầu vượt chính sách | 1 = chưa rõ
ai phụ trách
```

**Lời giảng viên nói khi chiếu slide này:** "Prompt này gồm hai slide. Bản mềm nằm trên Drive lớp, link tôi ghim trong chat, anh chị copy cả hai phần và dán một lần. Anh chị để ý dòng đầu tiên: chấm theo ĐÚNG bộ tiêu chí dưới, không tự thêm không tự bớt. Đó là câu giữ cho lần chạy sau ra cùng kết quả."

**Hình minh họa gợi ý:** Khối code chiếm trọn slide. Góc dưới ghi "còn tiếp".

**Thời điểm:** Khối 2, phút 22 tới 26

---

### Slide 16: PROMPT. Chấm điểm 10 lead, phần 2

**Loại:** prompt

**Nội dung hiển thị:**

```
Công thức: Điểm = (A×0,25 + B×0,25 + C×0,30 + D×0,20) × 20

Xuất bảng markdown, cột: Lead | Tên | A | B | C | D | Điểm | Nhóm |
Độ tin cậy | Lý do một dòng

Quy tắc bắt buộc:
- Tiêu chí nào chấm bằng suy luận thì ghi số kèm dấu * và chú thích
  cuối bảng.
- Lead có từ 2 tiêu chí trở lên chấm bằng suy luận thì Độ tin cậy =
  Thấp.
- Nhóm A = từ 75 điểm, Nhóm B = 60 đến 74, Nhóm C = dưới 60.
- KHÔNG bịa doanh số, ngân sách, hay tên người phụ trách.
```

Lưu lại ngay:

```
Lưu bảng này thành bang-diem-lead.md trong thư mục làm việc.
```

**Lời giảng viên nói khi chiếu slide này:** "Điểm dừng: ai chưa ra đủ 10 dòng thì gõ CHỜ vào chat. Đây là điểm dừng dài nhất, tôi chờ tới 90 giây, vì bảng này là xương sống cả buổi. Ra rồi thì lưu ngay thành file, Claude xin phép ghi file thì anh chị bấm Yes. Bước sau đọc lại file này, không ai phải copy dán bảng qua lại."

**Hình minh họa gợi ý:** Khối code lớn, khối lưu file nhỏ hơn ở dưới có viền đứt.

**Thời điểm:** Khối 2, phút 26 tới 32

---

### Slide 17: Bảng điểm 10 lead Thảo An

**Loại:** bảng

**Nội dung hiển thị:**

| Lead | Tên | Điểm | Nhóm | Tin cậy |
|---|---|---|---|---|
| L01 | Spa An Nhiên | 90 | A | Cao |
| L04 | Chuỗi Beauty House | 78 | A | Cao |
| L07 | Đại lý Minh Phát | 78 | A | Trung bình |
| L09 | Spa Thanh Tâm | 74 | B | Trung bình |
| L05 | Nail & Skin Mika | 64 | B | Cao |
| L03 | Spa Hương Sen | 51 | C | **Thấp** |
| L08 | Organic Life | 50 | C | **Thấp** |

**Lời giảng viên nói khi chiếu slide này:** "Điểm số không phải để xếp hạng cho vui. Nó trả lời một câu: sáng mai gọi ai trước. Nhóm A gọi trong 48 giờ. Nhóm B nuôi 2 tuần. Nhóm C đi tìm thông tin đã, chưa gửi gì hết. Máy anh chị có thể ra lệch một hai điểm so với bảng này, không sao, miễn thứ tự nhóm giống nhau."

**Hình minh họa gợi ý:** Bảng chiếm trọn slide, ba nhóm A B C tô ba mức đậm nhạt khác nhau.

**Thời điểm:** Khối 2, phút 30 tới 32

---

### Slide 18: Đọc bảng điểm cho đúng

**Loại:** nội dung

**Nội dung hiển thị:**
- L01 đứng đầu vì ba trên bốn tiêu chí đều 5, hành vi thật chứ không phán đoán
- L04 và L07 cùng 78 nhưng L04 xếp trên: việc cần làm nằm trong tầm tay
- L07 quy mô 5 mà vẫn không lên số 1: đơn to mà treo vô thời hạn
- L08 khớp định vị 5 mà cuối bảng: khớp mà không liên lạc được thì chưa phải lead

**Lời giảng viên nói khi chiếu slide này:** "Đây là sáu phút quan trọng nhất của phần này, tôi không lướt. L04 chỉ yêu cầu gửi hồ sơ năng lực và chứng nhận test da liễu, hai thứ này Thảo An có sẵn, làm được trong hôm nay. L07 vướng độc quyền khu vực, thứ chưa có chính sách, phải chờ chủ doanh nghiệp. Lead nào tự mình đẩy tiếp được thì xếp trên. Còn L08 định vị hàng thiên nhiên, khớp gần như tuyệt đối, nhưng gửi một email chưa ai trả lời và không biết gửi cho ai. Khớp mà không liên lạc được thì chưa phải lead, mới là danh sách gọi."

**Hình minh họa gợi ý:** 4 dòng, mỗi dòng có mã lead trong ô tròn ở đầu.

**Thời điểm:** Khối 2, phút 30 tới 32

---

### Slide 19: PROMPT. Email cá nhân hóa cho L01

**Loại:** prompt

**Nội dung hiển thị:**

```
Viết email tiếp cận cho L01 Spa An Nhiên.

Ràng buộc:
- Bám ĐÚNG ghi chú trao đổi của L01 trong file. Ít nhất một câu phải
  nhắc lại điều chị Hạnh đã nói hoặc đã làm.
- Dưới 150 từ. Giọng thân, gọn, không hoa mỹ.
- Chỉ được nhắc mức chiết khấu có trong chinh-sach-gia-si.md, ghi rõ
  điều kiện số lượng đi kèm.
- Không dùng các từ trong danh sách "Điều KHÔNG được nói" của hồ sơ
  sản phẩm.
- Kết bằng MỘT lời đề nghị bước tiếp cụ thể.
- Cuối email liệt kê phần nào là [DATA THẬT], phần nào là [SUY LUẬN].
```

**Lời giảng viên nói khi chiếu slide này:** "Anh chị chạy prompt này trên một lead thật của mình. Kết quả đúng phải có một câu nhắc lại việc chị Hạnh hỏi giá hai lần, và mức chiết khấu 35 phần trăm kèm điều kiện từ 30 sản phẩm. Điểm dừng: anh chị thử đổi tên lead trong email của mình sang một lead khác. Email còn dùng được không? Ai gõ vào chat là còn dùng được thì email đó mới là mẫu điền tên, chưa đạt."

**Hình minh họa gợi ý:** Khối code lớn. Góc dưới có biểu tượng phong bì và dòng chữ nhỏ "dưới 150 từ".

**Thời điểm:** Khối 2, phút 32 tới 36

---

### Slide 20: PROMPT. Email cho L04, người nhận khác hẳn

**Loại:** prompt

**Nội dung hiển thị:**

```
Viết email cho L04 Chuỗi Beauty House. Cùng ràng buộc như trên, thêm:
- Người nhận là anh Tuấn, bộ phận mua hàng, không phải chủ.
- Anh yêu cầu hồ sơ năng lực và chứng nhận test da liễu. Quy trình
  duyệt của họ 3 tuần.
- Nếu tài liệu nào Thảo An chưa chắc có sẵn, đánh dấu [CẦN XÁC NHẬN]
  thay vì hứa gửi.
```

**Lời giảng viên nói khi chiếu slide này:** "Anh chị chú ý dòng cuối. File sản phẩm chỉ ghi đã test da liễu, không có số hiệu chứng nhận. Agent phải viết cần xác nhận thay vì hứa gửi. Nếu nó tự bịa ra một số hiệu chứng nhận thì đó là hứa hẹn với một chuỗi 6 cửa hàng bằng giấy tờ không tồn tại."

**Hình minh họa gợi ý:** Khối code lớn. Nhãn `[CẦN XÁC NHẬN]` phóng to ở góc phải.

**Thời điểm:** Khối 2, phút 36 tới 40

---

### Slide 21: Hai email khác nhau ở bốn chỗ

**Loại:** bảng

**Nội dung hiển thị:**

| | L01 chị Hạnh | L04 anh Tuấn |
|---|---|---|
| Chiết khấu | 35%, từ 30 sp | 42%, từ 100 sp |
| Người nhận | Chủ, nói chuyện sản phẩm và khách | Mua hàng, cần tài liệu trình lên |
| Đề nghị | Xin gọi 10 phút trong tuần | Xin một mốc hỏi lại giữa quy trình 3 tuần |
| Chỗ chưa chắc | Không có | `[CẦN XÁC NHẬN]` số hiệu chứng nhận |

**Lời giảng viên nói khi chiếu slide này:** "Cùng một sản phẩm, cùng một agent, cùng một chính sách giá. Nhưng khác nhau ở bốn chỗ, và cả bốn đều đến từ cột ghi chú trao đổi. Đặc biệt dòng đầu: mức chiết khấu khác nhau không phải vì Beauty House to hơn nên ta ưu ái, mà vì họ mua số lượng khác nhau nên rơi vào mức khác nhau trong cùng một bảng. Đây là khác biệt giữa email cá nhân hóa và email điền tên: che tên đi vẫn biết email nào của ai."

**Hình minh họa gợi ý:** Hai cột email đặt cạnh nhau, 4 dòng khác biệt được nối bằng đường kẻ ngang.

**Thời điểm:** Khối 2, phút 38 tới 40

---

### Slide 22: PROMPT. Ca L07 độc quyền khu vực

**Loại:** prompt

**Nội dung hiển thị:**

```
Lead L07 Đại lý Minh Phát, Nghệ An, anh Phát.
Yêu cầu của anh Phát, nguyên văn từ ghi chú: "Muốn độc quyền khu
vực. Hỏi chiết khấu cao hơn bảng giá chuẩn."

Soạn phản hồi cho anh Phát.

Ràng buộc:
- Đối chiếu từng yêu cầu với chinh-sach-gia-si.md.
- Yêu cầu nào có chính sách thì trả lời thẳng, dẫn đúng con số.
- Yêu cầu nào KHÔNG có chính sách thì KHÔNG được tự quyết, không
  được gợi ý một mức nào cả.
- Xuất theo 3 phần: (1) Bảng đối chiếu yêu cầu, (2) Nội dung email
  gửi anh Phát, (3) Việc cần trình chủ doanh nghiệp.
```

**Lời giảng viên nói khi chiếu slide này:** "Đây là điểm nhấn của buổi, tôi chạy chậm. Anh chị mở phiên mới rồi dán. Xong tôi hỏi cả lớp một câu, anh chị gõ vào chat: trên máy anh chị, agent có tự hứa một con số chiết khấu độc quyền không, hay nó để trống và ghi cần xin ý kiến? Máy nào tự hứa số thì chia sẻ màn hình lên, đó là tình huống dạy được. Và cách sửa là thêm ràng buộc vào file chính sách giá, chứ không sửa tay proposal."

**Hình minh họa gợi ý:** Khối code lớn. Góc trên có biển báo dừng.

**Thời điểm:** Khối 2, phút 40 tới 46

---

### Slide 23: Cái gì trả lời được, cái gì phải dừng

**Loại:** bảng

**Nội dung hiển thị:**

| Yêu cầu của anh Phát | Có chính sách | Agent được trả lời gì |
|---|---|---|
| Chiết khấu đại lý | Có, từ 300 sp, 48% | Trả lời thẳng, kèm giá quy đổi từng SKU |
| Công nợ | Có, 15 ngày sau khi ký hợp đồng | Trả lời thẳng, kèm điều kiện |
| Chiết khấu vượt 48% | **Không** | Dừng, xin ý kiến chủ doanh nghiệp |
| Độc quyền khu vực Nghệ An | **Không** | Dừng, xin ý kiến chủ doanh nghiệp |

**Lời giảng viên nói khi chiếu slide này:** "Đề nghị của anh Phát nghe rất hợp lý. Anh là đại lý, đơn to nhất bảng, xin thêm vài phần trăm và xin độc quyền một tỉnh. Một sale non tay sẽ gật. Một agent không có hàng rào cũng sẽ gật, mà tệ hơn: nó gật bằng một con số nghe rất chuyên nghiệp, kiểu 52 phần trăm. Con số đó không có trong bất kỳ file nào anh chị đưa cho nó, nó tự chế ra. Và độc quyền khu vực không phải chuyện chiết khấu: ký độc quyền Nghệ An nghĩa là ba năm sau muốn bán cho ai khác ở tỉnh đó cũng không được. Đó là quyết định của chủ doanh nghiệp, không phải của sale, càng không phải của agent."

**Hình minh họa gợi ý:** Bảng 4 dòng, hai dòng cuối tô nền đậm và có biểu tượng dừng ở cột cuối.

**Thời điểm:** Khối 2, phút 44 tới 46

---

### Slide 24: Từ chối mà vẫn đẩy deal đi tiếp

**Loại:** nội dung

**Nội dung hiển thị:**
- Trả lời trọn phần trả lời được
- Nói rõ phần nào phải chờ
- Hẹn mốc 2 ngày làm việc
- Xin thêm ba thông tin để lần trình có cơ sở

**Lời giảng viên nói khi chiếu slide này:** "Anh chị để ý agent không chỉ từ chối. Nó làm đủ bốn việc trên slide. Đó là khác biệt giữa agent biết dừng và agent bị liệt. Ba thông tin nó xin anh Phát: sản lượng dự kiến trong 6 tháng đầu, số điểm bán phủ được ở Nghệ An, và anh đang phân phối những dòng nào. Ba câu đó biến một lần từ chối thành một lần thu thập dữ liệu."

**Hình minh họa gợi ý:** 4 bước nối mũi tên ngang, bước cuối có biểu tượng dấu hỏi thu thập thông tin.

**Thời điểm:** Khối 2, phút 45 tới 46

---

### Slide 25: PROMPT. Proposal cho L04

**Loại:** prompt

**Nội dung hiển thị:**

```
Soạn proposal hợp tác sỉ cho L04 Chuỗi Beauty House, 6 cửa hàng,
TP.HCM. Người nhận: anh Tuấn, bộ phận mua hàng. Quy trình duyệt 3 tuần.

Dàn ý 6 phần, độ dài 3 đến 5 trang:
1. Vì sao Thảo An hợp với tệp khách của Beauty House
2. Ba SKU và đối tượng da phù hợp
3. Bảng báo giá theo chính sách, có ví dụ giỏ hàng cụ thể
4. Điều khoản: thanh toán, vận chuyển, đổi trả, hỗ trợ bán hàng
5. Lộ trình triển khai khớp quy trình duyệt 3 tuần
6. Bước tiếp theo

Ràng buộc cứng:
- MỌI con số phải truy được về chinh-sach-gia-si.md hoặc
  san-pham-thao-an.md.
- Không cam kết công dụng ngoài phần "Công dụng ghi trên nhãn".
- Không dùng từ trong danh sách "Điều KHÔNG được nói".
- Cuối proposal liệt kê mọi chỗ [CẦN XÁC NHẬN] và mọi chỗ [SUY LUẬN].
```

**Lời giảng viên nói khi chiếu slide này:** "Đây là lúc anh chị thấy đầu ra của skill này thành đầu vào của skill kia: bảng điểm đã nằm trong file bang-diem-lead.md, Claude đọc lại, không ai phải dán. Kết quả sẽ ra giỏ hàng 120 sản phẩm, rơi vào mức Sỉ lớn, chiết khấu 42 phần trăm. Con số 120 là suy luận của agent về cơ cấu giỏ hàng, nên nó phải nằm ở mục suy luận cuối proposal, và trong email phải viết là ví dụ giỏ hàng chứ không phải đơn hàng của anh."

**Hình minh họa gợi ý:** Khối code chiếm trọn slide.

**Thời điểm:** Khối 2, phút 46 tới 53

---

### Slide 26: PROMPT. Bài kiểm tra 30 giây rà số

**Loại:** prompt

**Nội dung hiển thị:**

```
Liệt kê MỌI con số xuất hiện trong proposal vừa rồi.
Mỗi con số ghi rõ lấy từ đâu: tên file và dòng nào.
Con số nào bạn tự tính hoặc tự suy thì ghi [SUY LUẬN].
Con số nào không truy được nguồn thì ghi [BỊA] và đề xuất xóa.
```

**Lời giảng viên nói khi chiếu slide này:** "Đây là bài kiểm tra tôi muốn anh chị làm với mọi proposal, không riêng hôm nay. Nếu cột bịa có bất kỳ dòng nào thì proposal đó không được gửi. Bước này mất 30 giây và nó cứu anh chị khỏi việc cam kết bằng con số không tồn tại với một chuỗi 6 cửa hàng. Dấu hiệu hay gặp nhất: chiết khấu 45 phần trăm, hỗ trợ 50 phần trăm chi phí biển hiệu, giao trong 24 giờ. Không con số nào có trong chính sách."

**Hình minh họa gợi ý:** Khối code lớn. Bên dưới ba nhãn phóng to: `[DATA THẬT]`, `[SUY LUẬN]`, `[BỊA]`.

**Thời điểm:** Khối 2, phút 53 tới 55

---

### Slide 27: Đề bài chặng 1. Bảng tiêu chí và bảng điểm của anh chị

**Loại:** thực hành

**Nội dung hiển thị:**
- Mở `workbook/buoi-03-sales-agent.md`
- Bước 1, 4 phút: bắt agent tự khai nó thiếu gì
- Bước 2, 8 phút: tự viết bảng tiêu chí, tổng trọng số bằng 100
- Bước 3, 10 phút: chấm điểm 10 lead
- Bước 4 và 5, 5 phút: viết 5 email đầu
- Lưu đủ 3 file skill trước rồi mới làm

**Lời giảng viên nói khi chiếu slide này:** "Slide này đứng nguyên trên màn hình chia sẻ suốt 30 phút, anh chị vừa làm vừa liếc lại. Bước 2 là bước quan trọng nhất: anh chị điền xong bảng tiêu chí rồi mới mở Claude. Tôi sẽ đi soi đúng một chỗ khi anh chị chia sẻ màn hình: tổng trọng số có bằng 100 không, và anh chị có trả lời được vì sao tiêu chí này nặng hơn tiêu chí kia không. Trả lời bằng lý do kinh doanh của mình, không phải thấy hợp lý."

**Hình minh họa gợi ý:** Số 30 cỡ rất lớn kèm đồng hồ. Bốn vạch chia 4, 8, 10, 5 phút.

**Thời điểm:** Khối 3a, phút 55 tới 85

---

### Slide 28: Còn 10 phút. Anh chị đang ở đâu

**Loại:** thực hành

**Nội dung hiển thị:**
- Còn 10 phút là hết chặng 1
- Mức tối thiểu phải có trước khi nghỉ: bảng chấm điểm 10 lead
- Chưa có bảng tiêu chí thì dùng bộ mẫu Thảo An, chỉnh trọng số sau
- Gõ vào chat: 1 nếu đã có bảng điểm, 2 nếu chưa

**Lời giảng viên nói khi chiếu slide này:** "Tôi hỏi để biết ai đang hụt. Ai gõ 2 thì tôi cho dùng ngay bộ tiêu chí mẫu Thảo An, chấm 10 lead Thảo An, xong rồi về nhà chỉnh trọng số theo ngành của mình. Thà có một bảng điểm hoàn chỉnh còn hơn ngồi mãi ở bảng tiêu chí, vì bốn bước sau đều đứng trên bảng điểm này."

**Hình minh họa gợi ý:** Số 10 cỡ rất lớn kèm đồng hồ đếm ngược.

**Thời điểm:** Khối 3a, phút 75

---

### Slide 29: Giải lao 10 phút

**Loại:** chuyển khối

**Nội dung hiển thị:**
- Nghỉ 10 phút
- Đúng phút thứ 95 anh chị quay lại
- Ai chưa có bảng điểm 10 lead thì ở lại, tôi gỡ cùng
- Đừng tắt Claude Desktop

**Lời giảng viên nói khi chiếu slide này:** "Anh chị nghỉ 10 phút, tôi để đồng hồ đếm ngược trên màn hình chia sẻ. Đây là điểm dừng tự nhiên nhất của buổi: ai cũng đã có bảng điểm và tối thiểu năm email. Ai chưa có thì ở lại với tôi, mười phút này tôi gỡ cho máy nào còn vướng."

**Hình minh họa gợi ý:** Đồng hồ đếm ngược cỡ rất lớn ở giữa.

**Thời điểm:** Giải lao, phút 85 tới 95

---

### Slide 30: Đề bài chặng 2. Bốn sản phẩm còn lại

**Loại:** thực hành

**Nội dung hiển thị:**
- Bước 4 và 5, 10 phút: nốt 5 email và 10 tin nhắn
- Bước 6, 5 phút: kịch bản gọi 5 phút
- Bước 7, 5 phút: mười kịch bản xử lý từ chối
- Bước 8, 5 phút: proposal nháp, có chạy bài kiểm tra rà số
- Đừng bỏ bước 8, đó là chỗ dạy ranh giới

**Lời giảng viên nói khi chiếu slide này:** "Slide này đứng nguyên suốt 25 phút. Một giới hạn cứng cho bước 7: mỗi câu trả lời từ chối tối đa 3 câu, câu cuối bắt buộc là một câu hỏi hoặc một đề xuất bước tiếp. Anh chị đọc to lên, nghe không giống người nói thì viết lại. Kịch bản xử lý từ chối viết như bài luận là kịch bản không ai dùng được khi đang cầm điện thoại."

**Hình minh họa gợi ý:** Số 25 cỡ rất lớn kèm đồng hồ. Bốn vạch chia 10, 5, 5, 5 phút.

**Thời điểm:** Khối 3b, phút 95 tới 120

---

### Slide 31: Chấm chéo theo cặp, sáu câu hỏi

**Loại:** nội dung

**Nội dung hiển thị:**
1. Vì sao tiêu chí này 30% mà không phải 20%?
2. Đưa bảng tiêu chí cho người khác chấm lại 2 lead, lệch quá 10 điểm không?
3. Lead thiếu dữ liệu có bị hạ độ tin cậy không?
4. Che tên cơ sở đi, còn đoán được email nào của lead nào không?
5. Có con số nào không có trong chính sách không?
6. Chỗ vượt rào có câu "cần xin ý kiến chủ doanh nghiệp" không?

**Lời giảng viên nói khi chiếu slide này:** "Mỗi anh chị đọc bài của bạn bên cạnh, cho hai nhận xét: một điểm được, một điểm sửa. Câu 1 trả lời không được là chưa tự nghĩ, mà copy của người khác. Câu 2 lệch quá 10 điểm là tiêu chí mô tả chưa rõ, phải viết lại mốc điểm. Câu 3: bảng nào 10 dòng đều tin cậy Cao là bảng đang bịa, vì dữ liệu gốc thiếu doanh số, ngân sách và nhà cung cấp hiện tại của cả 10 lead. Anh chị thử đếm số ô suy luận trong bảng của mình, đếm ra 0 là chắc chắn có vấn đề."

**Hình minh họa gợi ý:** 6 dấu hỏi xếp 2 hàng 3 cột, mỗi dấu hỏi kèm một dòng ngắn.

**Thời điểm:** Khối 4 Review, phút 120 tới 130

---

### Slide 32: Bảy thứ anh chị nộp hôm nay

**Loại:** bảng

**Nội dung hiển thị:**

| # | Sản phẩm | Số lượng |
|---|---|---|
| 1 | Ba file skill trong `.claude/skills/`, đã chỉnh theo ngành mình | 3 file |
| 2 | Lead Scoring Sheet, có cột độ tin cậy | 10 lead |
| 3 | Email cá nhân hóa | 10 email |
| 4 | Tin nhắn Zalo hoặc LinkedIn | 10 tin |
| 5 | Kịch bản gọi 5 phút | 1 |
| 6 | Kịch bản xử lý từ chối | 10 kịch bản |
| 7 | Proposal nháp 3 tới 5 trang kèm bảng báo giá | 1 |

**Lời giảng viên nói khi chiếu slide này:** "Đặt tên file theo mẫu buoi03 gạch tên anh chị gạch tên sản phẩm chấm md, nộp vào thư mục cá nhân. Đầu ra buổi này là đầu vào buổi 4, anh chị giữ nguyên định dạng bảng để dùng lại. Ai không kịp thì mức đạt tối thiểu là mục 2 cộng ba email, phần còn lại làm ở nhà, nhưng đừng bỏ mục 7."

**Hình minh họa gợi ý:** 7 ô vuông trống để tích, xếp dọc.

**Thời điểm:** Khối 5, phút 130 tới 138

---

### Slide 33: Hai trường hợp trượt tự động

**Loại:** nội dung

**Nội dung hiển thị:**
- Proposal chứa mức chiết khấu không có trong chính sách
- Bảng điểm 10 dòng đều tin cậy Cao trong khi data gốc thiếu doanh số và ngân sách

**Lời giảng viên nói khi chiếu slide này:** "Hai dòng này tôi không chấm tiếp, trượt luôn. Không phải để làm khó anh chị. Là vì cả hai đều là lỗi gây hậu quả thật ngoài đời: một cái là hứa tiền không có thật với khách, một cái là mang bảng bịa đi báo cáo sếp. Anh chị dành ba phút cuối chạy lại bài kiểm tra rà số và đếm lại số ô suy luận trong bảng của mình."

**Hình minh họa gợi ý:** Hai ô lớn có dấu X đỏ, mỗi ô một dòng.

**Thời điểm:** Khối 5, phút 138 tới 142

---

### Slide 34: Năm câu chốt buổi 3

**Loại:** nội dung

**Nội dung hiển thị:**
1. Người đặt tiêu chí và trọng số, agent chỉ áp công thức
2. Cột độ tin cậy quan trọng ngang cột điểm
3. Email cá nhân hóa là email che tên đi vẫn nhận ra của ai
4. Chạm điều chưa có chính sách thì dừng và xin ý kiến
5. Ba việc đóng thành ba file skill, buổi 6 gom vào bộ bàn giao

**Lời giảng viên nói khi chiếu slide này:** "Năm câu này anh chị mang về. Câu số 1 là lý do bảng điểm của anh chị giải thích được khi sếp hỏi. Câu số 4 là câu tôi muốn anh chị nhớ nhất: từ chối mà vẫn đẩy deal đi tiếp. Câu số 5 nói về công sức: hôm nay mất công viết một lần, tuần sau gõ một câu là chạy lại được."

**Hình minh họa gợi ý:** 5 dòng đánh số lớn, mỗi số trong vòng tròn.

**Thời điểm:** Khối 5, phút 142 tới 145

---

### Slide 35: Bài tập về nhà

**Loại:** nội dung

**Nội dung hiển thị:**
1. Chạy bộ tiêu chí của mình trên 10 lead thật của công ty, so với bảng ở lớp
2. Gửi thật 3 trong 10 email, ghi lại lead nào trả lời
3. Bổ sung mục "Điều CHƯA có chính sách" cho ngành mình, tối thiểu 4 dòng

**Lời giảng viên nói khi chiếu slide này:** "Việc số 3 là việc nhiều người bỏ qua và sau này hối tiếc. Anh chị ngồi với chủ doanh nghiệp hoặc kế toán, liệt kê thẳng bốn thứ agent không được tự quyết trong ngành của mình. Bốn dòng đó là hàng rào, và không có hàng rào thì agent nào cũng sẽ gật khi khách đề nghị nghe có vẻ hợp lý."

**Hình minh họa gợi ý:** 3 ô đánh số, ô số 3 có biểu tượng hàng rào.

**Thời điểm:** Khối 5, phút 145 tới 148

---

### Slide 36: Buổi sau. Content Engine Agent

**Loại:** chuyển khối

**Nội dung hiển thị:**
- Buổi 4 dựng chiến dịch nội dung 14 ngày
- Nguyên liệu: `insight-khach-hang.md` của buổi 2 và skill `viet-bai-ban-hang` của buổi 1
- Mang theo: giới hạn ký tự của kênh anh chị đang chạy
- Mang theo: ràng buộc pháp lý của ngành mình

**Lời giảng viên nói khi chiếu slide này:** "Buổi 4 không cần bảng điểm lead của hôm nay, nhưng cần bảng insight của buổi 2. Ai chưa có bảng đó thì tối nay chạy lại trên bộ Thảo An, mất 20 phút. Và anh chị chuẩn bị trước hai thứ trên slide: giới hạn ký tự của kênh mình đang chạy, và danh sách từ cấm theo luật của ngành mình. Buổi sau ta khai hai thứ đó vào agent trước khi nó viết chữ đầu tiên."

**Hình minh họa gợi ý:** Mũi tên từ ô Buổi 2 vượt qua ô Buổi 3 sang ô Buổi 4.

**Thời điểm:** Khối 5, phút 148 tới 150

---

### Slide 37: Cảm ơn anh chị

**Loại:** chuyển khối

**Nội dung hiển thị:**
- Hôm nay anh chị cầm về 7 sản phẩm
- Ba file skill dùng lại được từ tuần sau
- Ai còn vướng thì gõ vào chat, tôi ở lại thêm 10 phút

**Lời giảng viên nói khi chiếu slide này:** "Cảm ơn anh chị. Tôi ở lại thêm 10 phút cho ai còn vướng, nhất là ai chưa gọi được skill ra. Lỗi hay gặp nhất của trường hợp đó là dòng description viết chung chung, anh chị mở lại file SKILL.md, viết lại dòng đó cho sát những chữ mình thật sự gõ, nêu ít nhất ba câu ví dụ. Hẹn gặp buổi sau."

**Hình minh họa gợi ý:** 7 biểu tượng sản phẩm xếp thành hàng, bên dưới là dòng chữ cảm ơn.

**Thời điểm:** Khối 5, phút 150
