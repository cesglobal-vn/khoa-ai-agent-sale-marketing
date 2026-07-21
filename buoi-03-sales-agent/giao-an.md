# Buổi 3 · Sales Agent

**Phụ đề:** Email, tin nhắn, kịch bản gọi và proposal thật.

Sale hết loay hoay "gọi ai trước, mở lời thế nào". Buổi này học viên xây một dây chuyền 3 agent: chấm điểm lead, soạn đề xuất, và chuẩn bị sẵn cách xử lý từ chối.

---

## Mục tiêu buổi

Hết 2,5 giờ, học viên phải:

1. Tự định nghĩa được bộ tiêu chí chấm điểm lead của chính mình, có thang và trọng số, không copy của ai.
2. Dùng agent áp công thức đó lên 10 lead thô, ra bảng xếp hạng kèm cột độ tin cậy.
3. Viết được email và tin nhắn bám vào ghi chú trao đổi thật của từng lead, không phải mẫu điền tên.
4. Dựng được proposal và bảng báo giá đúng chính sách, và biết agent phải dừng ở đâu khi khách hỏi điều chưa có chính sách.
5. Hiểu vì sao chia việc cho 3 agent lại tốt hơn nhồi vào 1 agent.

---

## Học viên cần chuẩn bị gì

Mang tới lớp 3 thứ, dạng file text hoặc bảng đều được:

| Cần có | Nội dung tối thiểu | Lấy ở đâu |
|---|---|---|
| Danh sách lead | 10 dòng: tên cơ sở, loại hình, khu vực, kênh liên hệ, người phụ trách, ghi chú trao đổi | Xuất CRM: lọc trạng thái "chưa chốt", chọn 6 cột trên, xuất CSV. Không có CRM thì mở inbox Facebook và Zalo, gom tay 10 hội thoại gần nhất |
| Chính sách giá | Bảng chiết khấu theo số lượng, điều khoản thanh toán và vận chuyển, và danh sách điều chưa có chính sách | Hỏi chủ doanh nghiệp hoặc kế toán. Chưa có thì viết ra 4 mức, mất 10 phút |
| Lịch sử trao đổi | Ghi chú thật của từng lead, nguyên văn càng tốt | Copy đoạn chat, đừng tóm tắt lại |

Ba file trên chép vào **thư mục làm việc** đã lập ở buổi 1, cùng chỗ với `CLAUDE.md`. Claude tự đọc, không phải đính kèm gì.

Cộng thêm đầu ra 2 buổi trước, cũng đã nằm sẵn trong thư mục đó: **hồ sơ sản phẩm** (`san-pham-thao-an.md`), **câu định vị, 3 thông điệp, giọng văn và danh sách từ cấm** trong `CLAUDE.md`, và **bảng insight khách hàng có trích dẫn** của buổi 2 (`insight-khach-hang.md`). Không có thì lấy nguyên bộ Thảo An trong `case-study/thao-an/`.

> Nhắc học viên: cột ghi chú để trống là chấp nhận được. Trống thì agent hạ độ tin cậy. Điền bừa cho đẹp bảng là tự phá bài của mình.

---

## Timeline 2,5 giờ

| Khối | Thời lượng | Nội dung | Đầu ra |
|---|---|---|---|
| 1. Framework | 20 phút | Vì sao 3 agent; lead scoring; ranh giới agent không được vượt | Học viên hiểu công thức trước khi mở Claude |
| 2. Demo | 35 phút | Giảng viên chạy trên 10 lead Thảo An: chấm điểm, 2 email khác tính chất, ca L07 độc quyền khu vực, proposal | Lớp thấy đủ 3 skill chạy nối nhau |
| 3. Học viên làm | 65 phút | Theo `workbook-hoc-vien.md`, bước 1 đến bước 8 | 7 sản phẩm |
| 4. Review | 10 phút | Chấm chéo theo 6 tiêu chí bên dưới | Mỗi người nhận 2 nhận xét |
| 5. Hoàn thiện và nộp | 20 phút | Sửa theo nhận xét, chạy checklist tự kiểm, nộp | Bộ file hoàn chỉnh |

---

## Khối 1 · Framework (20 phút)

### 1.1 Vì sao chia 3 agent thay vì 1 (7 phút)

Nói thẳng với lớp: nhồi cả quy trình sale vào một prompt dài thì agent làm việc gì cũng nửa vời. Lý do cụ thể:

- **Ba việc cần ba thái độ khác nhau.** Chấm điểm cần lạnh và nhất quán: cùng dữ liệu phải ra cùng điểm. Viết proposal cần bám chính sách từng dòng. Xử lý từ chối cần mềm và linh hoạt. Một prompt ôm cả ba thì thái độ trộn lẫn, agent bắt đầu "chấm điểm có cảm xúc".
- **Sai ở đâu sửa ở đó.** Điểm lead lệch thì sửa Outbound Agent, không đụng phần proposal. Prompt gộp thì sửa một chỗ hỏng chỗ khác.
- **Đầu ra cái này là đầu vào cái kia.** Bảng điểm ra trước, proposal viết cho lead nhóm A, closer viết theo phản hồi thật. Chia rõ thì học viên nhìn thấy dòng chảy.
- **Chia được việc cho người.** Sale mới chạy Outbound, sale cứng chạy Proposal. Không chia agent thì không chia được người.
- **Mỗi agent đóng thành một file skill, dùng lại được.** Giống buổi 1: mỗi agent lưu một `SKILL.md` riêng trong thư mục làm việc. Lần sau chỉ cần gõ việc cần làm, Claude tự gọi đúng skill, không phải dán lại prompt dài. Ba file này cũng là ba mảnh của bộ bàn giao gom lại ở buổi 6.

Vẽ lên bảng:

```
Danh sách lead thô
      ↓
[skill lead-scoring]        →  bảng điểm + xếp nhóm + script mở đầu
      ↓  (lead nhóm A)
[skill soan-proposal]       →  đề xuất hợp tác + bảng báo giá + email cover
      ↓  (khách phản hồi)
[skill theo-duoi-chot-don]  →  timeline follow-up + xử lý từ chối + tin nhắn chốt
```

Ba file nằm ở `.claude/skills/lead-scoring/SKILL.md`, `.claude/skills/soan-proposal/SKILL.md`, `.claude/skills/theo-duoi-chot-don/SKILL.md`. Nội dung đầy đủ trong `system-prompt.md`.

### 1.2 Lead scoring hoạt động thế nào (8 phút)

Nguyên tắc gốc: **người định nghĩa tiêu chí và trọng số, agent chỉ áp công thức.** Nếu để agent tự nghĩ tiêu chí thì mỗi lần chạy ra một kiểu, và không ai giải thích được vì sao lead này trên lead kia khi sếp hỏi.

Bộ tiêu chí mẫu cho Thảo An, thang 1 đến 5, tổng trọng số 100%:

| Tiêu chí | Trọng số | 5 điểm | 3 điểm | 1 điểm |
|---|---|---|---|---|
| **A. Quy mô đơn dự kiến** | 25% | Đại lý, từ 300 sp | Spa hoặc cửa hàng lẻ, 30 đến 99 sp | Dưới đơn tối thiểu hoặc không đoán được |
| **B. Độ khớp định vị** | 25% | Khách nói thẳng cần dòng lành tính, thiên nhiên | Khớp một phần, ví dụ cửa hàng đa thương hiệu | Tệp khách lệch hẳn |
| **C. Mức độ quan tâm** | 30% | Hỏi giá từ 2 lần, hoặc xin hồ sơ để duyệt nội bộ | Từng mua nhưng chưa quay lại | Chưa phản hồi lần nào |
| **D. Khả năng chốt trong 30 ngày** | 20% | Người quyết là chủ, không có quy trình duyệt | Có người phụ trách nhưng phải trình duyệt | Chưa rõ ai phụ trách |

Công thức: `Điểm = (A×0,25 + B×0,25 + C×0,30 + D×0,20) × 20` để ra thang 100.

Giải thích 3 lựa chọn trọng số cho lớp, đây là phần dạy nghề:

- **C nặng nhất (30%)** vì đó là dữ liệu quan sát được, không phải phán đoán. Khách chủ động hỏi giá 2 lần là hành vi thật.
- **A và B bằng nhau (25%)** vì đơn to mà lệch định vị thì bán một lần rồi thôi, còn khớp định vị mà đơn quá nhỏ thì không nuôi nổi.
- **D nhẹ nhất (20%)** vì khó chốt không có nghĩa là không đáng theo, chỉ có nghĩa là xếp sau.

Chấm thử 3 lead ngay tại lớp cho quen tay:

| Lead | A | B | C | D | Điểm | Độ tin cậy |
|---|---|---|---|---|---|---|
| L01 Spa An Nhiên | 3 | 5 | 5 | 5 | **90** | Cao |
| L04 Chuỗi Beauty House | 4 | 4 | 5 | 2 | **78** | Cao |
| L03 Spa Hương Sen | 3 | 4 | 2 | 1 | **51** | **Thấp** |

Chỉ vào L03: ba trong bốn tiêu chí chấm bằng suy luận từ loại hình cơ sở, không có ghi chú trao đổi nào ngoài "hỏi bảng giá". L03 và L08 chưa rõ người phụ trách, nên **độ tin cậy phải hạ xuống Thấp**. Việc cần làm với hai lead này không phải gửi proposal, mà là đi tìm đúng người trước.

Chốt: **cột độ tin cậy quan trọng ngang cột điểm.** Điểm 51 tin cậy Cao là một việc, điểm 51 tin cậy Thấp là việc khác hẳn.

### 1.3 Ranh giới agent không được tự quyết (5 phút)

Đây là phần khiến khóa này khác các khóa mẹo prompt. Ba nguyên tắc chống bịa, áp cho cả 3 agent:

1. **Chỉ dùng dữ liệu người dùng cấp.** Không bịa quy mô, nhu cầu, giá, tên khách, doanh số.
2. **Gắn nhãn nguồn.** `[DATA THẬT]` khi trích được từ file. `[SUY LUẬN]` khi tự suy ra. Thiếu thì ghi "chưa đủ dữ liệu" và hạ độ tin cậy.
3. **Người duyệt cuối.** Email, tin nhắn, proposal, hợp đồng đều là nháp. Agent không tự bấm gửi.

Ba nhóm việc agent **tuyệt đối không được tự quyết**:

- **Giá và chiết khấu.** Chỉ dùng đúng bảng có sẵn. File `chinh-sach-gia-si.md` có 4 mức: 25% / 35% / 42% / 48%. Ngoài 4 mức đó là vùng cấm.
- **Cam kết.** Thời gian giao, công dụng sản phẩm, thời gian có kết quả, quyền đổi trả ngoài điều khoản.
- **Ưu đãi và điều kiện hợp tác.** Độc quyền khu vực, chiết khấu vượt 48%, ký gửi, thanh toán sau khi bán, chi phí hỗ trợ marketing tại điểm bán.

Nói với lớp: mục "Điều CHƯA có chính sách" trong file giá không phải phần thừa. Đó là hàng rào. Câu duy nhất agent được nói khi chạm hàng rào là: **"Việc này cần xin ý kiến chủ doanh nghiệp, tôi ghi nhận và phản hồi anh chị trong 2 ngày làm việc."**

Đưa luôn ca thật: L07 Minh Phát đang hỏi độc quyền khu vực Nghệ An và xin chiết khấu cao hơn bảng chuẩn. Agent nào tự chế ra mức 52% cho L07 là agent đã hỏng, và học viên phải nhìn ra ngay trong demo phần sau.

---

## Khối 4 · Tiêu chí review 10 phút

Chấm chéo theo cặp. Mỗi người đọc bài của bạn bên cạnh, cho 2 nhận xét: 1 điểm được, 1 điểm sửa. Bám 6 câu hỏi:

1. **Trọng số có lý do không?** Hỏi tác giả "vì sao tiêu chí này 30% mà không phải 20%". Trả lời không được là chưa tự nghĩ.
2. **Điểm có tái lập được không?** Đưa cùng bảng tiêu chí cho người khác chấm lại 2 lead. Lệch quá 10 điểm là tiêu chí mô tả chưa rõ.
3. **Lead thiếu dữ liệu có bị hạ độ tin cậy không?** Bảng nào 10 dòng đều tin cậy Cao là bảng đang bịa.
4. **Email có bám ghi chú thật không?** Che tên cơ sở đi, còn đoán được là email nào của lead nào không. Không đoán được thì đó là email điền tên.
5. **Có con số nào không có trong chính sách không?** Rà từng con số trong proposal, đối chiếu bảng giá.
6. **Chỗ vượt rào có được đánh dấu không?** Tìm câu "cần xin ý kiến chủ doanh nghiệp". Không có mà lead lại hỏi điều ngoài chính sách là trượt.

---

## Điểm học viên hay vấp

**Vấp 1: Để agent tự nghĩ tiêu chí chấm điểm.**
Dấu hiệu: học viên gõ "chấm điểm 10 lead này giúp tôi" rồi lấy nguyên kết quả. Agent sẽ ra một bộ tiêu chí nghe rất hay nhưng lần chạy sau lại khác.
Xử lý: bắt học viên điền xong bảng tiêu chí trên giấy rồi mới mở Claude. Prompt phải chứa nguyên bảng đó. Câu chốt để nói: "Agent là máy tính, không phải người quyết định."

**Vấp 2: Email điền tên, tưởng là cá nhân hóa.**
Dấu hiệu: 10 email giống hệt, chỉ khác chỗ "Chị Hạnh" và "Chị Lan".
Xử lý: chơi trò che tên. Che hết tên riêng, đưa email cho người bên cạnh đoán là lead nào. Không đoán được thì viết lại. Bắt buộc: mỗi email phải có ít nhất một câu trích thẳng từ ghi chú trao đổi của lead đó.

**Vấp 3: Agent bịa giá và điều kiện.**
Dấu hiệu: proposal xuất hiện "chiết khấu 45%", "hỗ trợ 50% chi phí biển hiệu", "giao trong 24h". Không con số nào có trong chính sách.
Xử lý: chạy bước rà số bắt buộc. Bôi vàng mọi con số trong proposal, đối chiếu từng cái với file chính sách. Số nào không tìm thấy nguồn thì xóa hoặc thay bằng `[CẦN XÁC NHẬN]`. Đây là bước 10 phút, đừng bỏ.

**Vấp 4: Điền đầy bảng cho đẹp.**
Dấu hiệu: L03 và L08 không có người phụ trách nhưng bảng vẫn ghi "chủ cơ sở", cột độ tin cậy 10/10 dòng đều Cao.
Xử lý: nhắc lại nguyên tắc 2. Yêu cầu học viên đếm số ô `[SUY LUẬN]` trong bảng của mình. Đếm ra 0 là chắc chắn đang bịa, vì dữ liệu gốc thiếu doanh số, ngân sách và nhà cung cấp hiện tại của cả 10 lead.

**Vấp 5: Nhồi 3 việc vào 1 phiên, hoặc dán prompt thay vì lưu skill.**
Dấu hiệu: học viên chấm điểm xong, gõ tiếp "giờ viết proposal luôn" trong cùng phiên. Đến câu thứ 30 thì agent quên bảng tiêu chí, bắt đầu chấm lại theo cảm tính. Dấu hiệu thứ hai: học viên dán nguyên prompt vào chat cho nhanh, không chịu lưu thành file skill, nên hết buổi là mất sạch.
Xử lý: bắt lưu đủ 3 file `SKILL.md` trước khi làm việc gì. Rồi mỗi bước mở một phiên mới trong tab Code, gọi đúng một skill. Đầu ra bước trước lưu thành file trong thư mục làm việc, bước sau đọc lại file đó. Chậm hơn 2 phút, sạch hơn nhiều, và tuần sau còn dùng lại được.

**Vấp 5b: Skill không được gọi vì dòng `description` viết chung chung.**
Dấu hiệu: học viên gõ "chấm điểm giúp tôi" nhưng Claude không nhắc tên skill nào, trả lời như chưa từng đọc file.
Xử lý: mở lại `SKILL.md`, viết lại dòng `description` cho sát những chữ học viên thật sự gõ, nêu ít nhất 3 câu ví dụ. Đây là dòng duy nhất Claude dùng để chọn skill.

**Vấp 6: Kịch bản xử lý từ chối viết như bài luận.**
Dấu hiệu: mỗi câu trả lời dài 6 dòng, đọc lên nghe như đang đọc văn bản.
Xử lý: giới hạn cứng 3 câu cho mỗi phản hồi, câu cuối bắt buộc là một câu hỏi hoặc một đề xuất bước tiếp. Bắt học viên đọc to lên. Nghe không giống người nói thì viết lại.

---

## Sản phẩm nộp và cách chấm

Nộp 7 mục, đúng số lượng:

| # | Sản phẩm | Số lượng | Điểm |
|---|---|---|---|
| 1 | Ba file skill trong `.claude/skills/`, đã chỉnh theo ngành và chính sách của mình | 3 file | 10 |
| 2 | Lead Scoring Sheet, có cột độ tin cậy | 10 lead | 20 |
| 3 | Email cá nhân hóa | 10 email | 20 |
| 4 | Tin nhắn Zalo hoặc LinkedIn | 10 tin | 10 |
| 5 | Kịch bản gọi 5 phút | 1 | 10 |
| 6 | Kịch bản xử lý từ chối | 10 kịch bản | 15 |
| 7 | Proposal nháp 3 đến 5 trang, kèm bảng báo giá | 1 | 15 |

**Thang chấm:**

- **Đạt (từ 70 điểm):** đủ số lượng, bảng điểm có trọng số do học viên tự đặt, không có con số nào ngoài chính sách.
- **Khá (từ 85):** thêm được điều kiện là email đọc lên nhận ra ngay là của lead nào, và mọi chỗ vượt rào đều được đánh dấu xin ý kiến.
- **Trượt tự động, không cần chấm tiếp:** proposal chứa mức chiết khấu không có trong chính sách; hoặc bảng điểm 10 dòng đều tin cậy Cao trong khi dữ liệu gốc thiếu doanh số và ngân sách.

Nộp vào thư mục cá nhân, đặt tên `buoi03-<tên>-<sản phẩm>.md`. Đầu ra buổi này là đầu vào buổi 4, giữ nguyên định dạng bảng để dùng lại.
