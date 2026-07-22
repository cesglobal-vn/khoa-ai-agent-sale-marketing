# Nội dung slide Buổi 02: Customer Insight Agent

**Khóa:** AI Agent cho Sale & Marketing
**Hình thức:** online live qua Zoom hoặc Meet
**Thời lượng buổi:** 150 phút
**Tổng số slide:** 38 slide, trong đó 21 slide nội dung và bảng, 12 slide prompt, 3 slide đề bài và mốc thời gian, 1 slide bìa, 1 slide giải lao
**Giáo án nguồn:** `giao-an/buoi-02-customer-insight-agent.md`
**Kịch bản demo nguồn:** `so-tay-giang-vien/buoi-02-customer-insight-agent.md`
**Ma trận mục tiêu:** `00-tong-quan/ma-tran-muc-tieu.md` mục tiêu 2.1 tới 2.5

## Ghi chú thiết kế chung

- Nền trắng, chữ đậm, cỡ chữ tối thiểu 28pt vì lớp học qua màn hình chia sẻ
- Slide prompt để chữ cỡ lớn trong khối code, học viên nhìn màn hình chia sẻ gõ theo được
- Mỗi slide một thông điệp, tối đa 6 dòng
- Phần "Lời giảng viên nói khi chiếu slide này" KHÔNG in lên slide
- Màu, logo, font do bước đóng gói áp vào, không ghi ở đây

---

### Slide 1: Buổi 2. Customer Insight Agent

**Loại:** tiêu đề

**Nội dung hiển thị:**
- AI Agent cho Sale & Marketing
- Buổi 2 trên 6
- Biến dữ liệu khách hàng thành insight và nội dung
- 150 phút

**Lời giảng viên nói khi chiếu slide này:** "Chào anh chị. Buổi này dạy một việc rất cụ thể: đọc bình luận, review, tin nhắn khách để thấy điều họ thật sự quan tâm, rồi biến thành góc nội dung bám nỗi đau thật. Có một luật xuyên suốt buổi hôm nay: mọi insight phải trích được nguyên văn khách nói. Không trích được thì gắn nhãn suy luận."

**Hình minh họa gợi ý:** Mũi tên lớn từ khối chữ lộn xộn bên trái sang bảng có cột ID bên phải.

**Thời điểm:** Khối 1 Framework, phút 0

---

### Slide 2: Hết buổi hôm nay anh chị làm được gì

**Loại:** nội dung

**Nội dung hiển thị:**
- Dựng skill `customer-insight` chạy trên tối thiểu 30 mẩu
- Ra bảng insight mà mọi dòng đều có mã nguồn và trích dẫn nguyên văn
- Xếp hạng pain theo tần suất dạng x trên tổng
- Ra 5 content angle, 5 bài social, 3 brief hình, 3 visual
- Bắt được lúc agent bịa trích dẫn, bịa tần suất, bịa persona

**Lời giảng viên nói khi chiếu slide này:** "Dòng thứ hai là dòng tôi chấm chặt nhất. Cuối buổi tôi sẽ bốc ngẫu nhiên hai dòng trong bảng của anh chị, mở file gốc dò ngược. Sai một dòng là chưa đạt. Nghe khắt khe, nhưng đây chính là thứ phân biệt bảng insight dùng được với bảng insight đẹp mà không dám mang đi họp."

**Hình minh họa gợi ý:** 5 ô vuông trống để tích, ô thứ hai đóng khung đậm.

**Thời điểm:** Khối 1, phút 1

---

### Slide 3: Anh chị mở lại thư mục làm việc của buổi 1

**Loại:** nội dung

**Nội dung hiển thị:**
- Mở Claude Desktop, tab **Code**, thư mục `thao-an-marketing`
- Trong đó phải có sẵn: `san-pham-thao-an.md`, `CLAUDE.md`, skill `viet-bai-ban-hang`
- Hôm nay không tạo thư mục mới, chỉ thêm một skill nữa
- Chép file data khách vào đúng thư mục đó, không để ở Downloads

**Lời giảng viên nói khi chiếu slide này:** "Buổi 2 không tạo thư mục mới. Ta thêm một skill nữa vào chính thư mục đó, tên customer-insight. Claude tự đọc CLAUDE.md mỗi phiên, nên agent mới đọc được cả hồ sơ sản phẩm lẫn dữ liệu khách mà không phải dán lại gì. Ai vắng buổi 1 hoặc chưa có thư mục làm việc thì gõ vào chat cho tôi biết, anh chị tạo một thư mục mới trên màn hình nền, chép file hồ sơ Thảo An vào, rồi nhờ Claude viết nhanh CLAUDE.md theo mẫu buổi 1. Mất 5 phút, tôi sẽ kèm riêng."

**Hình minh họa gợi ý:** Cây thư mục 3 nhánh: `san-pham-thao-an.md`, `CLAUDE.md`, `.claude/skills/`.

**Thời điểm:** Khối 1, phút 2

---

### Slide 4: Lời hứa cuối buổi 1 phải trả trong hôm nay

**Loại:** nội dung

**Nội dung hiển thị:**
- Buổi 1: mục "5 nỗi đau khách" trong `CLAUDE.md` gắn nhãn `[SUY LUẬN]`
- Đó là chủ ý thiết kế, không phải thiếu sót
- Cuối buổi nay: thay 5 dòng đoán bằng 5 nỗi đau có mã trích dẫn
- Đổi nhãn thành `[DATA THẬT]`
- Dòng nào không gắn được ID thì giữ nguyên `[SUY LUẬN]`

**Lời giảng viên nói khi chiếu slide này:** "Tôi nói ngay đầu buổi để anh chị biết đích đến. Buổi 1 chúng ta đoán năm nỗi đau của khách. Hôm nay anh chị có data thật, và ở 20 phút cuối buổi anh chị sẽ mở lại chính file đó, đặt hai cột cạnh nhau: bên trái là năm dòng mình đoán, bên phải là năm dòng từ data. Lúc đó anh chị thấy tận mắt mình đoán trúng mấy dòng và trật mấy dòng. Với tôi đó là mười phút đáng tiền nhất của cả buổi."

**Hình minh họa gợi ý:** Hai cột đối chiếu, cột trái nhãn `[SUY LUẬN]` mờ, cột phải nhãn `[DATA THẬT]` đậm.

**Thời điểm:** Khối 1, phút 3

---

### Slide 5: Nhịp buổi hôm nay

**Loại:** bảng

**Nội dung hiển thị:**

| Khối | Phút | Việc |
|---|---|---|
| 1 | 20 | Framework, chỉ nghe |
| 2 | 35 | Demo làm theo, anh chị gõ cùng tôi |
| 3a | 30 | Anh chị làm sản phẩm, chặng 1 |
| Nghỉ | 10 | Giải lao |
| 3b | 25 | Anh chị làm sản phẩm, chặng 2 |
| 4 | 10 | Review, 3 người chia sẻ màn hình |
| 5 | 20 | Hoàn thiện và nộp |

**Lời giảng viên nói khi chiếu slide này:** "Hai mươi phút đầu anh chị chỉ nghe và ghi. Từ khối 2 trở đi là gõ liên tục. Khối 2 không phải tôi biểu diễn cho anh chị xem, tôi gõ gì thì anh chị gõ y hệt trên máy mình. Tôi đi chậm hơn bình thường, và cứ sau mỗi prompt lớn tôi sẽ dừng lại hỏi ai chưa ra kết quả. Anh chị gõ vào chat ngay lúc đó, đừng ngại, vì tôi chạy tiếp là anh chị mất luôn khúc sau."

**Hình minh họa gợi ý:** Thanh ngang chia 7 đoạn theo tỉ lệ thời lượng, hai đoạn khối 3 tô đậm.

**Thời điểm:** Khối 1, phút 4

---

### Slide 6: Câu này là dữ liệu hay insight

**Loại:** nội dung

**Nội dung hiển thị:**
> "Da mình nhạy cảm lắm, dùng cái này không bị rát gì hết."

- Anh chị gõ đáp án vào chat

**Lời giảng viên nói khi chiếu slide này:** "Anh chị đọc câu này rồi gõ vào chat: dữ liệu hay insight? Tôi chờ 20 giây. Đáp án: đây là dữ liệu thô. Một người, một câu, một lần. Nó chưa nói được gì về việc anh chị phải viết bài thế nào tháng sau."

**Hình minh họa gợi ý:** Câu trích trong khung bong bóng chat cỡ lớn, giữa slide.

**Thời điểm:** Khối 1, phút 4 tới 6

---

### Slide 7: Ba thứ biến dữ liệu thô thành insight

**Loại:** nội dung

**Nội dung hiển thị:**
1. **Lặp lại**: nhiều người nói, ở nhiều chỗ khác nhau
2. **Có lý do đằng sau**: vì sao họ nói vậy
3. **Đổi được hành vi bán hàng**: biết rồi thì viết khác, bán khác

**Lời giảng viên nói khi chiếu slide này:** "Ở câu vừa rồi, lý do đằng sau là họ từng bị kích ứng nên sợ, chứ không phải họ thích cảm giác mát. Hai cách hiểu đó dẫn tới hai bài viết hoàn toàn khác nhau. Chốt ý cho gọn: dữ liệu thô là khách nói gì, insight là vì sao họ nói vậy và ta phải làm gì."

**Hình minh họa gợi ý:** 3 ô xếp dọc, mũi tên đi xuống, ô cuối tô đậm.

**Thời điểm:** Khối 1, phút 6 tới 8

---

### Slide 8: Công thức viết một insight

**Loại:** nội dung

**Nội dung hiển thị:**

```
[Nhóm khách nào] + [lo hoặc muốn điều gì] + [vì sao]
+ [bằng chứng ID] + [tần suất trên tổng]
```

> Nhóm khách da nhạy cảm sợ sản phẩm mới làm rát và nổi mẩn, vì họ đã từng bị với sản phẩm khác. Bằng chứng: R01, R11, M01, M02, M06, M10. Tần suất: 9 trên 30 mẩu.

**Lời giảng viên nói khi chiếu slide này:** "Anh chị so câu này với câu hay thấy trong các báo cáo: khách hàng quan tâm đến chất lượng sản phẩm. Câu đó đúng, nhưng vô dụng. Nó đúng với mọi ngành, mọi thương hiệu, mọi thời điểm. Đây là phép thử tôi muốn anh chị nhớ: insight tốt phải sai được. Nếu một câu không thể sai thì nó không phải insight."

**Hình minh họa gợi ý:** Công thức 5 khối màu nối bằng dấu cộng. Ví dụ bên dưới trong khung viền.

**Thời điểm:** Khối 1, phút 8 tới 11

---

### Slide 9: Dữ liệu thật lấy ở đâu

**Loại:** bảng

**Nội dung hiển thị:**

| Đường | Cách làm | Chi phí |
|---|---|---|
| Chép tay | Review sàn, inbox Facebook, bình luận bài viết | Không tốn phí, chậm |
| Claude tự lấy | Nối tikhub, gọi công cụ lấy bình luận TikTok hoặc Instagram | Mỗi lượt gọi tính tiền |

Ba điều nhớ: gọi một lần rồi lưu file. Data thật vẫn phải đánh ID. Chỉ lấy nội dung công khai.

**Lời giảng viên nói khi chiếu slide này:** "Điều một: mỗi lần gọi là tốn tiền, dịch vụ ghi thẳng là yêu cầu này sẽ tính phí. Nên gọi đúng một lần và lưu ngay thành file, lát nữa muốn phân tích lại thì đọc file, đừng gọi lại. Điều hai: bình luận lấy về từ TikTok cũng chỉ là mấy chục dòng chữ, agent vẫn bịa được trên chữ thật nếu ta không ép nó chỉ ra dòng nào. Điều ba: câu người ta viết công khai thì lấy được, còn gom tên tài khoản và đường dẫn trang cá nhân thành một danh sách thì không. Đó là dựng danh sách người, không phải đọc khách hàng. Ai chưa đăng ký tikhub thì vẫn học được và vẫn nộp đủ sản phẩm, dùng bộ Thảo An là chạy trọn buổi."

**Hình minh họa gợi ý:** Hai đường mũi tên vào cùng một ô đích ghi "file data có ID". Đường thứ hai gắn biểu tượng đồng tiền.

**Thời điểm:** Khối 1, phút 11 tới 13

---

### Slide 10: Xếp hạng theo tần suất, không theo cảm giác

**Loại:** nội dung

**Nội dung hiển thị:**
- Ta nhớ mẩu gây cảm xúc mạnh nhất, không nhớ mẩu lặp nhiều nhất
- Một review 1 sao ám cả tuần
- 9 câu hỏi "có cồn không shop" rải rác cả tháng thì không ai nhớ
- 9 câu kia mới là thứ đang chặn đơn hàng
- Ghi "9 trên 30" thì kiểm được. Ghi "đa số khách" thì không

**Lời giảng viên nói khi chiếu slide này:** "Ai làm marketing lâu cũng có linh cảm về khách. Linh cảm thường sai theo một kiểu rất cụ thể, đúng như dòng đầu tiên trên slide. Quy tắc của buổi hôm nay: xếp hạng pain theo số mẩu nhắc tới, ghi dạng x trên tổng. Cấm ba chữ đa số, rất nhiều, phần lớn. Ba chữ đó là chỗ agent và người đều hay bịa, và thường thì đa số hóa ra là 3 trên 30. Một lưu ý nghề: tần suất chỉ phản ánh người đã nói, người bỏ đi im lặng không nằm trong đó. Nên tần suất dùng để xếp thứ tự ưu tiên, không dùng để suy ra thị phần."

**Hình minh họa gợi ý:** Cột số 9 to gấp ba lần cột số 1 bên cạnh, nhưng cột số 1 tô màu chói.

**Thời điểm:** Khối 1, phút 13 tới 15

---

### Slide 11: Vì sao mỗi insight phải có trích dẫn

**Loại:** nội dung

**Nội dung hiển thị:**
- Mô hình rất giỏi viết câu nghe đúng mà không có thật
- Hai loại đó nhìn giống nhau khi đọc lướt
- Ép agent ghi ID thì: insight bịa lộ ra ngay
- Anh chị Ctrl+F kiểm được trong 5 giây
- Sếp hỏi "dựa vào đâu" thì có câu trả lời

**Lời giảng viên nói khi chiếu slide này:** "Đây là phần quan trọng nhất buổi. Cách duy nhất tách được câu thật với câu nghe đúng là ép agent chỉ ra mẩu nào. Tôi nhắc lại ba nguyên tắc chống bịa của buổi 1, áp cho mọi agent trong khóa: chỉ dùng dữ liệu người dùng cấp; gắn nhãn nguồn; người duyệt cuối. Và một điểm cần nói rõ: nhãn suy luận không xấu. Suy luận là việc có ích. Cái xấu là suy luận đội lốt dữ liệu."

**Hình minh họa gợi ý:** Hai dòng chữ giống hệt nhau, một dòng có mã ID gắn bên cạnh và dấu tích, dòng kia không có và có dấu hỏi.

**Thời điểm:** Khối 1, phút 15 tới 17

---

### Slide 12: Content angle khác thông điệp thế nào

**Loại:** bảng

**Nội dung hiển thị:**

| Thông điệp | Content angle |
|---|---|
| Da khỏe từ thảo mộc Việt | "Từng đổi serum rồi nổi mẩn? Đọc cái này trước khi đổi lần nữa" |
| Không cồn, đã test da liễu | "Bóc nhãn thành phần: đọc từng dòng, cái nào là gì" |
| Hỗ trợ giảm thâm sau mụn | "1 tuần chưa thấy gì có phải là hỏng không" |

Phép thử: thay tên thương hiệu bằng đối thủ mà angle vẫn dùng được thì loại.

**Lời giảng viên nói khi chiếu slide này:** "Thông điệp là điều thương hiệu muốn nói, một thương hiệu có một hoặc hai thông điệp, giữ nguyên cả năm. Content angle là góc vào để khách chịu đọc, nó bắt đầu từ nỗi lo của khách chứ không từ ưu điểm của sản phẩm. Một thông điệp đẻ ra được mười angle. Còn phép thử ở dưới: chất lượng tốt, giá hợp lý dùng được cho mọi shop, nên nó không phải angle. Angle mạnh luôn truy ngược được về một insight, insight đó truy ngược được về một ID."

**Hình minh họa gợi ý:** Bảng hai cột, cột phải rộng gấp đôi. Dưới bảng vẽ mũi tên truy ngược: angle sang insight sang ID.

**Thời điểm:** Khối 1, phút 17 tới 20

---

### Slide 13: Đích đến hôm nay, bảng insight mẫu

**Loại:** bảng

**Nội dung hiển thị:**

| # | Pain | Tần suất | Trích dẫn ID |
|---|---|---|---|
| 1 | Sợ rát, nổi mẩn, muốn bằng chứng an toàn | 9/30 | R01, R02, R04, R11, M01, M02, M04, M06, M10 |
| 2 | Băn khoăn giá và dung tích, muốn size dùng thử | 5/30 | R03, R13, M07, M08, M14 |
| 3 | Kết cấu chưa vừa ý, kem đặc, mặt nạ khô căng | 5/30 | R06, R07, R08, R10, M13 |
| 4 | Cần bằng chứng để tin: giấy test, hàng chuẩn | 5/30 | R04, R14, M04, M09, M14 |
| 5 | Sốt ruột vì chưa thấy kết quả | 4/30 | R02, R05, M05, M15 |

**Lời giảng viên nói khi chiếu slide này:** "Đây là đích đến, để anh chị biết cuối buổi mình cầm cái gì. Ba nhận xét đáng nói. Một: pain số 1 gấp đôi mọi pain khác, nhưng nó gần như không nằm ở phần review chê. Bộ này không có review nào dưới 2 sao, và 5 trong 9 mẩu là tin nhắn hỏi trước khi mua. Ai chỉ đọc review sẽ bỏ lỡ hơn nửa pain lớn nhất. Hai: cả 4 review 4 sao đều kèm một câu chê cụ thể. Review 4 sao là mỏ vàng, khách hài lòng nên nói thật, không giận nên nói rõ. Ba: có một pain nữa về giao chậm và muốn thanh toán khi nhận hàng, đó là pain vận hành, không viết bài về nó mà chuyển cho bộ phận vận hành."

**Hình minh họa gợi ý:** Bảng chiếm trọn slide, cột Trích dẫn ID tô nền nhạt cho nổi.

**Thời điểm:** Khối 1, phút 18 tới 20

---

### Slide 14: 35 phút tới anh chị gõ cùng tôi

**Loại:** chuyển khối

**Nội dung hiển thị:**
- Mở đúng thư mục làm việc của buổi 1
- Tôi gõ gì thì anh chị gõ y hệt trên máy mình
- Bốn điểm dừng, tôi chờ hai phần ba lớp mới đi tiếp
- Chưa ra kết quả thì gõ CHỜ vào chat ngay

**Lời giảng viên nói khi chiếu slide này:** "Ba mươi lăm phút tới không phải là tôi biểu diễn cho anh chị xem. Tôi đi chậm hơn bình thường, và cứ sau mỗi prompt lớn tôi sẽ dừng lại hỏi ai chưa ra kết quả. Anh chị gõ vào chat ngay lúc đó, đừng ngại. Quy tắc của tôi: thà chạy chậm mà cả lớp gõ, còn hơn chạy đúng giờ mà nửa lớp ngồi xem."

**Hình minh họa gợi ý:** Biểu tượng bàn phím lớn ở giữa, 4 chấm tròn đánh dấu 4 điểm dừng trên một thanh ngang.

**Thời điểm:** Khối 2, phút 20

---

### Slide 15: PROMPT. Lấy bình luận thật bằng tikhub

**Loại:** prompt

**Nội dung hiển thị:**

```
Dùng công cụ tikhub tên tiktok_app_v3_fetch_video_comments để lấy
bình luận của video này: [dán đường dẫn video TikTok]

Lấy tối đa 50 bình luận. Rồi làm đúng 3 việc:
1. Lưu kết quả thành file binh-luan-tiktok-goc.md ngay trong thư
   mục làm việc này.
2. Đánh ID cho từng bình luận theo dạng T01, T02, T03...
3. Bỏ tên tài khoản, ảnh đại diện và đường dẫn trang cá nhân của
   người bình luận. Chỉ giữ nguyên văn câu họ viết, giữ cả lỗi
   chính tả.

Gọi công cụ đúng MỘT lần. Gọi xong báo lại lấy được bao nhiêu
bình luận. Chưa phân tích gì cả.
```

**Lời giảng viên nói khi chiếu slide này:** "Trước khi phân tích, tôi lấy data đã. Bộ 30 mẩu của Thảo An lát nữa ta dùng là data giả định, tôi dựng ra để dạy. Còn đây là bình luận thật, của người thật, dưới một video thật đang chạy trên TikTok sáng nay. Ai đã có tài khoản tikhub thì gọi trên kênh của mình hoặc của đối thủ, bình luận dưới video đối thủ thường thẳng thắn hơn vì họ không biết anh chị đọc. Ai chưa có thì mở sẵn file review-va-tin-nhan-khach.md trong thư mục của mình. Xong tôi chạy thêm một prompt ngắn để anh chị thấy insight rút từ data thật vẫn trích dẫn được: đọc file binh-luan-tiktok-goc.md, rút đúng 3 điều khách nói nhiều nhất, mỗi điều ghi tần suất, danh sách đủ ID và một câu nguyên văn copy đúng ký tự."

**Hình minh họa gợi ý:** Khối code chiếm trọn slide. Góc phải trên có biểu tượng đồng tiền và dòng chữ nhỏ "mỗi lượt gọi tính phí".

**Thời điểm:** Khối 2, phút 20 tới 25

---

### Slide 16: Ba câu về data thật, không bỏ câu nào

**Loại:** nội dung

**Nội dung hiển thị:**
1. Gọi một lần, lưu ngay thành file. Lần sau đọc file, đừng gọi lại
2. Bỏ tên và ảnh người bình luận. Ta đọc điều khách nói, không dựng danh sách người
3. Data thật rồi vẫn phải đánh ID, vẫn phải Ctrl+F kiểm

**Lời giảng viên nói khi chiếu slide này:** "Điều hai không phải phép lịch sự, đây là ranh giới. Điều ba mới là điều nhiều người bỏ qua: bình luận thật cũng chỉ là chữ, và agent vẫn bịa được trên chữ thật. Data thật không tự nó thành bằng chứng. Nếu lúc nãy tikhub gọi lỗi hoặc mạng chậm, anh chị đừng ngồi sửa, chuyển thẳng sang bộ Thảo An. Phần còn lại của buổi chạy y hệt, chỉ đổi file data."

**Hình minh họa gợi ý:** 3 dòng đánh số, dòng 3 đóng khung đậm.

**Thời điểm:** Khối 2, phút 24 tới 25

---

### Slide 17: PROMPT. Bắt agent đếm trước khi phân tích

**Loại:** prompt

**Nội dung hiển thị:**

```
Đọc file review-va-tin-nhan-khach.md trong thư mục này. Đây là dữ
liệu khách hàng của Thảo An: 15 review Shopee (R01-R15) và 15 tin
nhắn inbox Facebook (M01-M15).

Trước khi phân tích, làm đúng 3 việc:
1. Đếm và báo lại: tổng bao nhiêu mẩu, bao nhiêu review, bao nhiêu
   tin nhắn.
2. Liệt kê các SKU xuất hiện trong data.
3. Nói cho tôi biết dữ liệu này KHÔNG trả lời được những câu hỏi nào.

Chưa rút insight vội. Chỉ làm 3 việc trên.
```

**Lời giảng viên nói khi chiếu slide này:** "Anh chị để ý, tôi không dán một chữ system prompt nào. Cái quy trình dài ba trang tôi đã lưu thành file skill từ trước, giống hệt cách buổi 1 làm với skill viết bài. Tôi chỉ nói việc, nó tự rút hồ sơ ra. Việc đầu tiên không phải hỏi insight, việc đầu tiên là bắt agent đếm. Nếu nó đếm sai số mẩu ngay từ đầu thì mọi con số tần suất phía sau đều sai. Và để ý câu số 3: tôi đang bắt nó tự khai chỗ nó không biết, trước khi nó kịp bịa. Điểm dừng thứ nhất: ai chưa ra kết quả thì gõ CHỜ vào chat, tôi chờ hai phần ba lớp."

**Hình minh họa gợi ý:** Khối code lớn. Bên dưới ghi kết quả mong đợi cỡ lớn: "30 mẩu = 15 review + 15 tin nhắn".

**Thời điểm:** Khối 2, phút 25 tới 28

---

### Slide 18: PROMPT chính. Bảng insight có trích dẫn

**Loại:** prompt

**Nội dung hiển thị:**

```
Bây giờ phân tích toàn bộ 30 mẩu.

Bước 1: gom các mẩu nói cùng một chuyện vào một nhóm chủ đề. Một
mẩu được nằm ở nhiều nhóm nếu nó nói nhiều chuyện.

Bước 2: với mỗi nhóm, viết ra một pain theo đúng cấu trúc:
[nhóm khách nào] + [lo hoặc muốn điều gì] + [vì sao]

Bước 3: xuất ra bảng markdown đúng các cột sau, xếp giảm dần theo
tần suất:

| # | Pain | Tần suất | Trích dẫn ID | Nguyên văn 1 câu tiêu biểu | Nhãn |

Quy tắc bắt buộc:
- Tần suất ghi đúng dạng "x/30". Cấm dùng: đa số, rất nhiều, phần
  lớn, hầu hết.
- Cột Trích dẫn ID liệt kê ĐỦ các ID đã đếm, không viết tắt kiểu
  "R01 và các mẩu khác".
- Số ID liệt kê phải khớp đúng với x. Không khớp thì sửa x.
- Cột Nguyên văn copy đúng ký tự từ file, không viết lại cho mượt.
- Nhãn ghi [DATA THẬT] hoặc [SUY LUẬN].
```

**Lời giảng viên nói khi chiếu slide này:** "Đây là prompt xương sống của cả buổi. Kết quả phải ra bảng 6 tới 8 dòng, dòng đầu là nỗi lo kích ứng và an toàn, khoảng 9 trên 30. Đây là điểm dừng dài nhất, tôi chờ tới 90 giây. Bảng insight là xương sống cả buổi, ai hụt ở đây là hụt tới cuối. Ai chưa ra bảng thì gõ CHỜ, tôi gọi trợ giảng vào phòng nhỏ."

**Hình minh họa gợi ý:** Khối code chiếm trọn slide.

**Thời điểm:** Khối 2, phút 28 tới 35

---

### Slide 19: Thao tác 5 giây kiểm agent có bịa không

**Loại:** sơ đồ

**Nội dung hiển thị:**
1. Đọc dòng 1, lấy một ID, ví dụ R01
2. Sang tab chứa file gốc
3. Ctrl+F, gõ đoạn agent trích
4. Khớp 100 phần trăm ký tự thì đạt
5. Làm lại với một ID ở dòng cuối bảng

**Lời giảng viên nói khi chiếu slide này:** "Anh chị dừng lại, phóng to cột Trích dẫn ID trên máy mình. Đây là chỗ kiểm chứng được. Cả bảng này, chỉ có cột này đáng tin. Mọi cột khác là chữ, mà chữ thì mô hình nào cũng viết hay được. Tôi làm thao tác kiểm trước mặt anh chị, rồi anh chị làm lại trên máy mình. Năm giây. Đó là toàn bộ chi phí để biết agent có bịa hay không. Ai không làm việc năm giây này thì đang mang số liệu bịa đi họp. Một mẹo: chọn ID ở dòng cuối bảng, đó là chỗ agent hay ẩu nhất. Và cẩn thận một lỗi tinh vi hơn: ID có thật nhưng câu trích bị agent viết mượt lại cho hay. Agent làm mượt câu chê của khách là đang làm hỏng bằng chứng."

**Hình minh họa gợi ý:** 5 bước nối mũi tên. Bước 4 vẽ kính lúp trên chữ được bôi vàng.

**Thời điểm:** Khối 2, phút 33 tới 35

---

### Slide 20: PROMPT. Ba câu data không trả lời được

**Loại:** prompt

**Nội dung hiển thị:**

```
Dựa trên data này, cho tôi biết:
1. Khách của Thảo An chủ yếu ở tỉnh thành nào?
2. Tỷ lệ khách mua lần đầu so với khách mua lại là bao nhiêu?
3. Nhóm khách nào nhắn tin nhiều nhất rồi không mua, và vì sao họ
   không mua?
```

Nếu agent lỡ bịa, chạy tiếp:

```
Câu trả lời vừa rồi có chỗ không trích dẫn được từ data.
Rà lại từng câu bạn vừa viết. Câu nào không gắn được ID thì xóa
hoặc đổi thành "chưa đủ dữ liệu".
Liệt kê cho tôi những câu bạn vừa xóa và lý do.
```

**Lời giảng viên nói khi chiếu slide này:** "Ba câu vừa rồi là ba câu sếp hay hỏi nhất. Và data này không trả lời được câu nào. Anh chị gõ vào chat: máy anh chị nói chưa đủ dữ liệu mấy trên ba câu? Máy nào ra khác thì chia sẻ màn hình cho cả lớp xem, đó là tình huống dạy được, không phải chuyện xấu hổ. Agent bịa không phải lỗi của anh chị. Không phát hiện ra mới là lỗi của anh chị. Chốt phần này: ba chỗ thiếu vừa rồi cũng là danh sách việc phải làm. Muốn biết khách ở tỉnh nào thì tháng sau thêm một câu hỏi vào form đặt hàng. Insight tốt luôn đẻ ra một việc phải làm cho tháng sau."

**Hình minh họa gợi ý:** Khối code trên, khối code sửa lỗi dưới có viền đứt và nhãn "chỉ dùng khi agent bịa".

**Thời điểm:** Khối 2, phút 35 tới 39

---

### Slide 21: PROMPT. Dựng persona từ bảng insight

**Loại:** prompt

**Nội dung hiển thị:**

```
Từ bảng insight trên, dựng tối đa 3 persona.

Mỗi persona ghi:
- Tên gọi ngắn (đặt theo nỗi lo, không đặt theo nhân khẩu học)
- Nỗi lo chính, kèm ID
- Câu họ thật sự đang hỏi trong đầu (trích nguyên văn 1 mẩu)
- Cái họ cần thấy để yên tâm bấm mua
- SKU phù hợp nhất và lý do

Ràng buộc:
- Không bịa tuổi, nghề, thu nhập, nơi ở. Data không có thì ghi
  "chưa đủ dữ liệu".
- Mỗi persona phải gắn được tối thiểu 3 ID.
```

**Lời giảng viên nói khi chiếu slide này:** "Kết quả phải ra ba persona kiểu này: người từng bị kích ứng; người mụn ẩn và thâm chưa biết chọn gì; người đang cân giá. Anh chị để ý persona không có tuổi, không có nghề, không có chị Lan 32 tuổi ở Hà Nội thích yoga. Vì data không nói điều đó. Persona bịa nhân khẩu học nghe rất sinh động và dẫn ta đi sai suốt cả quý. Persona đặt tên theo nỗi lo thì viết bài xong biết ngay bài đó cho ai."

**Hình minh họa gợi ý:** 3 thẻ persona xếp ngang, mỗi thẻ có tên đặt theo nỗi lo và dãy ID ở chân thẻ.

**Thời điểm:** Khối 2, phút 39 tới 42

---

### Slide 22: PROMPT. Năm content angle

**Loại:** prompt

**Nội dung hiển thị:**

```
Từ bảng insight và 3 persona trên, đề xuất 5 content angle.

Mỗi angle ghi đúng 4 dòng:
- Tên angle (1 câu, viết như tiêu đề khách sẽ đọc)
- Bám pain số mấy, tần suất bao nhiêu
- Trích dẫn ID làm bằng chứng
- Persona nhắm tới

Ràng buộc:
- 5 angle phải bám tối thiểu 4 pain KHÁC NHAU.
- Phép thử trước khi xuất: nếu thay tên Thảo An bằng tên một
  thương hiệu khác mà angle vẫn dùng được thì angle đó bị loại,
  viết lại angle khác.
- Đối chiếu mục "Điều KHÔNG được nói" trong hồ sơ sản phẩm. Không
  angle nào được hứa mốc thời gian hay dùng từ trị mụn, đặc trị.
```

**Lời giảng viên nói khi chiếu slide này:** "Điểm dừng thứ tư: ai đã có đủ 5 angle trên máy mình thì gõ XONG vào chat. Chưa đủ thì dùng tạm 3 angle, làm nốt ở khối sau. Anh chị nhìn angle số 3 trong kết quả của tôi: nó sinh ra từ một review 3 sao, chỉ có một người nói. Nhưng cộng thêm hai tin nhắn nữa là ba mẩu, và nó chạm đúng lúc khách sắp bỏ cuộc. Insight tần suất thấp mà đúng thời điểm quyết định vẫn đáng viết. Tần suất dùng để xếp thứ tự, không phải để loại bỏ. Một lỗi hay gặp: năm angle thật ra là một angle viết năm kiểu, cả năm đều xoay quanh lành tính và an toàn. Ràng buộc bốn pain khác nhau trong prompt là để chặn đúng lỗi đó."

**Hình minh họa gợi ý:** Khối code lớn. Bên dưới là 5 ô nối tới 4 ô pain khác nhau bằng mũi tên.

**Thời điểm:** Khối 2, phút 42 tới 45

---

### Slide 23: PROMPT. Năm bài social

**Loại:** prompt

**Nội dung hiển thị:**

```
Viết 5 bài đăng Facebook, mỗi bài cho một angle ở trên.

Yêu cầu mỗi bài:
- Dài 120 đến 200 chữ
- Câu mở đầu lấy từ chính nỗi lo của khách, không mở bằng lời khen
  sản phẩm
- Có tối thiểu 1 câu trích nguyên văn khách, ghi rõ trích từ ID nào
  (khi đăng thật sẽ bỏ ID, giữ để tôi kiểm)
- Kết bằng 1 lời mời hành động nhẹ, không giục
- Đúng phần giọng văn và danh sách từ cấm trong file CLAUDE.md của
  thư mục này

Cấm tuyệt đối: trị mụn, đặc trị, khỏi hẳn, trắng da cấp tốc, hứa
mốc thời gian có kết quả, so sánh đích danh thương hiệu khác.

Cuối mỗi bài, xuống dòng ghi: Nguồn insight: pain số ..., ID ...
```

**Lời giảng viên nói khi chiếu slide này:** "Dòng Nguồn insight ở cuối mỗi bài chính là thứ phân biệt bài viết bằng data với bài viết bằng cảm hứng. Khi sếp hỏi vì sao tháng này viết chủ đề kích ứng thì anh chị chỉ vào dòng đó. Khi đăng thật thì xóa dòng này đi."

**Hình minh họa gợi ý:** Khối code lớn. Chân slide có mẫu dòng "Nguồn insight: pain 1, ID R11 M06" đóng khung.

**Thời điểm:** Khối 2, phút 45 tới 48

---

### Slide 24: PROMPT. Rà lại 5 bài, không tự sửa

**Loại:** prompt

**Nội dung hiển thị:**

```
Rà lại 5 bài vừa viết, đối chiếu mục "Điều KHÔNG được nói".
Liệt kê từng câu vi phạm kèm số bài và đề xuất câu thay.
Không tự sửa. Chỉ liệt kê để tôi duyệt.
```

**Lời giảng viên nói khi chiếu slide này:** "Anh chị để ý chữ cuối: không tự sửa, chỉ liệt kê để tôi duyệt. Đó là nguyên tắc số 3, người duyệt cuối. Agent không được tự tay đổi nội dung rồi im lặng. Nếu anh chị để nó tự sửa thì tháng sau anh chị không biết bài của mình đã bị đổi những gì."

**Hình minh họa gợi ý:** Khối code nhỏ ở giữa. Bên dưới là biểu tượng con dấu duyệt trong tay người.

**Thời điểm:** Khối 2, phút 48 tới 49

---

### Slide 25: PROMPT. Ba brief hình ảnh

**Loại:** prompt

**Nội dung hiển thị:**

```
Viết 3 brief hình ảnh cho 3 bài trong số 5 bài trên (chọn bài 1, 2, 4).

Mỗi brief đủ 5 mục:
1. Thông điệp một câu mà người xem phải hiểu trong 2 giây
2. Bố cục (đặt gì ở đâu, chữ chính chiếm bao nhiêu phần)
3. Chữ trên ảnh (tối đa 8 chữ, viết ra chính xác)
4. Màu và tông (bám phần giọng văn trong CLAUDE.md)
5. Điều cấm trong ảnh (không hình ảnh y tế, không ảnh trước sau,
   không biểu đồ bịa số liệu)

Mỗi brief ghi thêm: bám pain số mấy, ID nào.
```

**Lời giảng viên nói khi chiếu slide này:** "Mục 5, điều cấm trong ảnh, là mục người ta hay bỏ. Ảnh trước và sau là chỗ ngành mỹ phẩm dính rắc rối nhiều nhất. Viết ra thành ràng buộc thì lần sau không ai trong team quên. Ở khối này anh chị ra được một brief là đủ, ba brief để dành cho phần làm sản phẩm."

**Hình minh họa gợi ý:** Khối code lớn. Góc phải là khung vuông 1080 chia ô theo bố cục mẫu.

**Thời điểm:** Khối 2, phút 49 tới 52

---

### Slide 26: PROMPT. Tạo visual bằng Artifact

**Loại:** prompt

**Nội dung hiển thị:**

```
Từ brief số 2, tạo một Artifact HTML kích thước 1080x1080, hiển thị
đúng như brief.
Yêu cầu:
- Chữ tiếng Việt có dấu, dùng font hệ thống, cỡ chữ chính đủ lớn để
  đọc trên điện thoại
- Nền phẳng theo tông màu trong brief, không dùng ảnh từ internet
- Toàn bộ nằm gọn trong khung vuông, không tràn
Xuất ra để tôi xem trước, tôi sẽ chụp lại làm ảnh đăng.
```

**Lời giảng viên nói khi chiếu slide này:** "Có hai đường làm visual. Đường này dùng khi cần chữ tiếng Việt sắc nét và bố cục chuẩn. Đường còn lại là công cụ ảnh AI, dùng khi cần ảnh sản phẩm hoặc nền có chất liệu, và khi đó anh chị nhớ một mẹo: không để chữ trong ảnh AI, vì công cụ ảnh vẫn hay viết sai dấu tiếng Việt. Ảnh AI lo phần nền và chất liệu, chữ chèn sau bằng Canva hoặc Artifact. Nếu visual ra chưa đẹp thì giữ nguyên, đừng ngồi sửa: nó đúng brief và đúng insight là được. Sửa đẹp mất 10 phút. Sửa một chiến dịch đi sai insight mất một tháng."

**Hình minh họa gợi ý:** Khối code lớn. Bên phải là khung vuông ghi "1080 x 1080".

**Thời điểm:** Khối 2, phút 52 tới 55

---

### Slide 27: Đường đi từ 30 mẩu tới 5 bài

**Loại:** sơ đồ

**Nội dung hiển thị:**
- 30 mẩu nguyên văn
- 7 pain xếp theo tần suất, mỗi pain có ID
- Bỏ pain vận hành
- 3 persona đặt tên theo nỗi lo
- 5 content angle, mỗi angle truy ngược về ID
- 5 bài social, 3 brief hình, 3 visual

**Lời giảng viên nói khi chiếu slide này:** "Ba câu chốt khối này. Một: mọi thứ ở đáy sơ đồ đều truy ngược lên đỉnh được, truy không được thì là bịa. Hai: ba chỗ agent nói chưa đủ dữ liệu chính là danh sách việc phải làm cho tháng sau. Ba: bảng insight này còn sống tới buổi 3 và buổi 4. Buổi 3 dùng persona để cá nhân hóa email sale, buổi 4 dùng cả bảng để dựng chiến dịch 14 ngày. Đừng để nó lạc trong cửa sổ chat."

**Hình minh họa gợi ý:** Sơ đồ hình phễu dọc, 6 tầng, mũi tên đi xuống, đáy phễu là ba biểu tượng: bài viết, brief, ảnh.

**Thời điểm:** Khối 2, phút 52 tới 55

---

### Slide 28: Đề bài chặng 1. Dựng bảng insight của anh chị

**Loại:** thực hành

**Nội dung hiển thị:**
- Mở `workbook/buoi-02-customer-insight-agent.md`
- Chuẩn bị data 8 phút: đánh ID, xóa thông tin cá nhân, chép vào thư mục làm việc
- Bước 1, 7 phút: nạp agent và bắt nó đếm
- Bước 2, 15 phút: ra bảng insight có cột trích dẫn
- Nộp cuối chặng: bảng insight tối thiểu 5 dòng, mọi dòng có ID

**Lời giảng viên nói khi chiếu slide này:** "Ai có data của công ty thì dùng data của mình. Ai chưa có gì thì dùng bộ Thảo An, làm ra sản phẩm y hệt. Tôi để slide này đứng nguyên trên màn hình chia sẻ suốt 30 phút, anh chị vừa làm vừa liếc lại. Bàn nào ra bảng insight mà cột trích dẫn còn trống thì gõ vào chat ngay, đừng đi tiếp bước sau. Đó là bàn đang đi sai."

**Hình minh họa gợi ý:** Số 30 cỡ rất lớn kèm đồng hồ. Ba vạch nhỏ chia 8, 7, 15 phút.

**Thời điểm:** Khối 3a, phút 55 tới 85

---

### Slide 29: Còn 10 phút. Anh chị đang ở đâu

**Loại:** thực hành

**Nội dung hiển thị:**
- Còn 10 phút là hết chặng 1
- Chưa có bảng insight thì kéo về bộ Thảo An ngay
- Có bảng rồi nhưng thiếu cột trích dẫn thì chạy lại prompt chính
- Gõ vào chat: 1 nếu đã có bảng, 2 nếu chưa

**Lời giảng viên nói khi chiếu slide này:** "Tôi hỏi nhanh để biết ai đang hụt. Anh chị gõ 1 hoặc 2 vào chat. Ai gõ 2 thì tôi kéo về bộ Thảo An ngay, bỏ bước làm sạch data, chạy thẳng prompt chính. Thà có một bảng insight trên bộ demo còn hơn hết giờ mà chưa có bảng nào, vì hai khối sau đều đứng trên bảng này."

**Hình minh họa gợi ý:** Số 10 cỡ rất lớn kèm đồng hồ đếm ngược.

**Thời điểm:** Khối 3a, phút 75

---

### Slide 30: Giải lao 10 phút

**Loại:** chuyển khối

**Nội dung hiển thị:**
- Nghỉ 10 phút
- Đúng phút thứ 95 anh chị quay lại
- Ai chưa ra bảng insight thì ở lại, tôi gỡ cùng
- Đừng tắt Claude Desktop

**Lời giảng viên nói khi chiếu slide này:** "Anh chị nghỉ 10 phút. Tôi để đồng hồ đếm ngược trên màn hình chia sẻ, nhìn là biết còn mấy phút. Ai chưa ra bảng insight thì đừng rời phòng, ở lại với tôi, vì chặng 2 dựng hoàn toàn trên bảng đó. Mười phút này tôi gỡ cho máy nào còn vướng, để anh chị vào chặng 2 không bị hụt."

**Hình minh họa gợi ý:** Đồng hồ đếm ngược cỡ rất lớn ở giữa.

**Thời điểm:** Giải lao, phút 85 tới 95

---

### Slide 31: Đề bài chặng 2. Từ bảng insight ra sản phẩm

**Loại:** thực hành

**Nội dung hiển thị:**
- Bước 3, 6 phút: dựng persona
- Bước 4, 8 phút: năm content angle
- Bước 5, 7 phút: năm bài social
- Bước 6, 4 phút: ba brief hình ảnh và ba visual
- Bước 7 để dành cho 20 phút cuối buổi

**Lời giảng viên nói khi chiếu slide này:** "Slide này cũng đứng nguyên suốt 25 phút, anh chị vừa làm vừa liếc lại. Bốn prompt anh chị cần đều nằm trong workbook, copy dán được ngay. Hai lỗi tôi sẽ đi soi trong lúc anh chị làm: một là năm angle thật ra là một angle viết năm kiểu; hai là trong năm angle có một angle về giao hàng nhanh. Angle giao hàng là pain vận hành, không viết bài về nó."

**Hình minh họa gợi ý:** Số 25 cỡ rất lớn kèm đồng hồ. Bốn vạch chia 6, 8, 7, 4 phút.

**Thời điểm:** Khối 3b, phút 95 tới 120

---

### Slide 32: Ba câu tôi sẽ hỏi khi anh chị chia sẻ màn hình

**Loại:** nội dung

**Nội dung hiển thị:**
1. Tôi chỉ vào một dòng insight bất kỳ: mẩu nào?
2. Đọc to angle số 3: angle này bám pain nào, tần suất bao nhiêu?
3. Đọc lướt một bài social: có từ cấm không, có hứa kết quả không?

**Lời giảng viên nói khi chiếu slide này:** "Tôi gọi 3 anh chị, mỗi người 2 phút. Câu 1: anh chị phải mở được file data và chỉ ra đúng câu, ấp úng là insight chưa chắc. Câu 2: trả lời được thì đường truy ngược thông. Câu 3: có thì ta sửa tại chỗ. Tôi không giảng lý thuyết ở khối này, chỉ làm ba thao tác đó. Xong tôi ghi lên chat ba lỗi phổ biến nhất vừa thấy để cả lớp sửa trong 20 phút cuối."

**Hình minh họa gợi ý:** 3 dấu hỏi lớn xếp dọc, mỗi dấu hỏi kèm một dòng.

**Thời điểm:** Khối 4 Review, phút 120 tới 130

---

### Slide 33: PROMPT 7.1. Lưu bảng insight thành file

**Loại:** prompt

**Nội dung hiển thị:**

```
Lưu bảng insight, danh sách pain vận hành, 3 persona và 5 content
angle vừa làm thành file insight-khach-hang.md ngay trong thư mục
làm việc này.

Giữ nguyên cột Trích dẫn ID và cột Nguyên văn. Không rút gọn, không
bỏ ID.
Đầu file ghi 3 dòng: ngày phân tích, tên file data nguồn, tổng số mẩu.
Cuối file giữ nguyên mục "Chỗ còn thiếu dữ liệu".
```

**Lời giảng viên nói khi chiếu slide này:** "Bảng insight còn nằm trong cửa sổ chat là chưa tính hoàn thành. File nằm trong thư mục thì buổi sau mở tab Code lên là Claude đọc được ngay, không phải dán lại. Để rời trong cửa sổ chat thì hai buổi sau anh chị phải làm lại từ đầu."

**Hình minh họa gợi ý:** Khối code lớn. Bên phải là biểu tượng file `insight-khach-hang.md` nằm cạnh `CLAUDE.md`.

**Thời điểm:** Khối 5, phút 130 tới 133

---

### Slide 34: PROMPT 7.2. Thay 5 nỗi đau đoán bằng 5 nỗi đau thật

**Loại:** prompt

**Nội dung hiển thị:**

```
Mở file CLAUDE.md trong thư mục này, tìm mục 5 nỗi đau khách (hoặc
mục chân dung khách). Cả 5 dòng đang gắn nhãn [SUY LUẬN] vì buổi
trước tôi chưa có data.

Giờ đọc file insight-khach-hang.md vừa lưu, rồi viết lại mục đó theo
đúng quy tắc sau:

1. Mỗi nỗi đau lấy từ bảng insight, ưu tiên theo tần suất giảm dần.
2. Mỗi dòng ghi đủ 4 phần: nỗi đau viết bằng lời khách; tần suất
   dạng x/tổng; danh sách đủ mã trích dẫn; nhãn [DATA THẬT].
3. Kèm một câu nguyên văn khách nói, copy đúng ký tự, đặt trong
   ngoặc kép.
4. Nỗi đau nào KHÔNG gắn được mã trích dẫn thì GIỮ NGUYÊN nhãn
   [SUY LUẬN]. Không đổi nhãn cho đủ 5 dòng.
5. Nỗi đau vận hành (giao hàng, thanh toán, đổi trả) không đưa vào
   mục này. Ghi riêng thành một dòng ở cuối, đánh dấu là việc của
   bộ phận vận hành.

Trước khi ghi đè, cho tôi xem bảng so sánh 2 cột: bên trái là 5
dòng cũ tôi đoán, bên phải là dòng mới từ data. Dòng nào tôi đoán
trật thì ghi rõ trật ở chỗ nào. Tôi duyệt xong bạn mới ghi vào file.
```

**Lời giảng viên nói khi chiếu slide này:** "Anh chị để ý quy tắc số 4: dòng nào không gắn được mã trích dẫn thì giữ nguyên nhãn suy luận, đừng đổi nhãn cho đủ năm dòng. Đổi nhãn bừa là tự lừa mình. Và để ý đoạn cuối: nó phải cho anh chị xem bảng so sánh trước khi ghi đè. Anh chị đọc bảng đó rồi mới bấm duyệt."

**Hình minh họa gợi ý:** Khối code chiếm trọn slide.

**Thời điểm:** Khối 5, phút 133 tới 140

---

### Slide 35: Anh chị đoán trúng mấy dòng

**Loại:** bảng

**Nội dung hiển thị:**

| | Số dòng |
|---|---|
| Nỗi đau tôi đoán ở buổi 1 mà data xác nhận đúng | |
| Nỗi đau tôi đoán mà data không hề nhắc tới | |
| Nỗi đau data chỉ ra mà tôi chưa từng nghĩ tới | |

**Lời giảng viên nói khi chiếu slide này:** "Anh chị đọc bảng so sánh Claude vừa trả, rồi tự điền ba con số này vào workbook. Đây là chỗ đáng tiền nhất của cả buổi. Ai muốn thì gõ ba con số của mình vào chat, tôi rất muốn biết cả lớp đoán trúng bao nhiêu. Dòng thứ ba thường là dòng làm người ta bất ngờ nhất."

**Hình minh họa gợi ý:** Bảng 3 dòng, ô số bên phải để trống, viền đậm như ô điền tay.

**Thời điểm:** Khối 5, phút 140 tới 143

---

### Slide 36: Sáu thứ anh chị nộp hôm nay

**Loại:** bảng

**Nội dung hiển thị:**

| # | Sản phẩm | Ở đâu |
|---|---|---|
| 1 | Customer Insight Agent | `.claude/skills/customer-insight/SKILL.md` |
| 2 | Bảng insight tối thiểu 5 dòng, đủ cột ID | `insight-khach-hang.md` |
| 3 | 5 content angle, mỗi angle ghi bám pain nào | Trong `insight-khach-hang.md` |
| 4 | 5 bài social đúng giọng, không từ cấm | Thư mục làm việc |
| 5 | 3 brief hình ảnh và 3 visual | Thư mục làm việc |
| 6 | `CLAUDE.md` đã đổi 5 nỗi đau sang `[DATA THẬT]` | Thư mục làm việc |

**Lời giảng viên nói khi chiếu slide này:** "Đạt tối thiểu 5 trên 6 dòng thì tính là hoàn thành buổi 2. Riêng dòng số 6 là bắt buộc, thiếu dòng này thì chưa xong buổi. Cách tôi chấm dòng số 2: bốc ngẫu nhiên hai trích dẫn, mở file gốc dò ngược, cả hai phải khớp nguyên văn. Còn một dấu hiệu tôi luôn để ý: bảng nào điền kín, không chỗ nào ghi chưa đủ dữ liệu, không nhãn suy luận nào, thì đó là dấu hiệu agent đang bịa."

**Hình minh họa gợi ý:** 6 ô vuông trống để tích, ô số 6 đóng khung đậm kèm chữ "bắt buộc".

**Thời điểm:** Khối 5, phút 143 tới 147

---

### Slide 37: Bài tập về nhà

**Loại:** nội dung

**Nội dung hiển thị:**
1. Gom thêm data cho đủ 50 mẩu, chạy lại bảng insight, so hai bảng
2. Trả lời 3 câu: pain số 1 tần suất bao nhiêu; ba chỗ data không trả lời được là gì; ai hỏi "dựa vào đâu" thì mở file nào
3. Thêm một câu hỏi vào form đặt hàng để tháng sau lấp chỗ thiếu

**Lời giảng viên nói khi chiếu slide này:** "Việc số 1 là việc đáng làm nhất: 30 mẩu đủ để học kỹ thuật, 50 mẩu trở lên thì tần suất mới bắt đầu đáng tin. Việc số 3 nhỏ nhưng đúng tinh thần buổi hôm nay: insight tốt luôn đẻ ra một việc phải làm cho tháng sau. Ba chỗ agent nói chưa đủ dữ liệu chính là ba việc đó."

**Hình minh họa gợi ý:** 3 ô đánh số. Ô số 1 có mũi tên từ "30 mẩu" sang "50 mẩu".

**Thời điểm:** Khối 5, phút 147 tới 149

---

### Slide 38: Buổi sau. Sales Agent

**Loại:** chuyển khối

**Nội dung hiển thị:**
- Buổi 3 dùng persona hôm nay để cá nhân hóa email sale
- Email cho "người từng bị kích ứng" khác hẳn email cho "người đang so giá"
- Buổi 4 dùng cả bảng insight để dựng chiến dịch 14 ngày
- Mang theo: `insight-khach-hang.md` và `CLAUDE.md` đã cập nhật

**Lời giảng viên nói khi chiếu slide này:** "Bảng insight hôm nay còn sống tới hai buổi nữa. Không có bảng này thì buổi 4 phải bịa lịch nội dung, và ta quay về đúng chỗ xuất phát. Anh chị giữ file cẩn thận, để trong thư mục làm việc cạnh CLAUDE.md. Cảm ơn anh chị, hẹn gặp buổi sau."

**Hình minh họa gợi ý:** Mũi tên từ ô `insight-khach-hang.md` tách hai nhánh sang ô Buổi 3 và ô Buổi 4.

**Thời điểm:** Khối 5, phút 149 tới 150
