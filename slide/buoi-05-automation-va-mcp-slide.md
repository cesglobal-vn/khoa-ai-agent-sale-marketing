# Nội dung slide Buổi 05: Automation và MCP

**Khóa:** AI Agent cho Sale & Marketing
**Hình thức:** online live qua Zoom hoặc Meet
**Thời lượng buổi:** 150 phút
**Tổng số slide:** 38 slide, trong đó 23 slide nội dung và bảng, 11 slide prompt, 3 slide đề bài và mốc thời gian, 1 slide bìa, 1 slide giải lao
**Giáo án nguồn:** `giao-an/buoi-05-automation-va-mcp.md`
**Kịch bản demo nguồn:** `so-tay-giang-vien/buoi-05-automation-va-mcp.md`
**Ma trận mục tiêu:** `00-tong-quan/ma-tran-muc-tieu.md` mục tiêu 5.1 tới 5.5

## Ghi chú thiết kế chung

- Nền trắng, chữ đậm, cỡ chữ tối thiểu 28pt vì lớp học qua màn hình chia sẻ
- Slide prompt để chữ cỡ lớn trong khối code, học viên nhìn màn hình chia sẻ gõ theo được
- Mỗi slide một thông điệp, tối đa 6 dòng
- Phần "Lời giảng viên nói khi chiếu slide này" KHÔNG in lên slide
- Màu, logo, font do bước đóng gói áp vào, không ghi ở đây

---

### Slide 1: Buổi 5. Automation và MCP

**Loại:** tiêu đề

**Nội dung hiển thị:**
- AI Agent cho Sale & Marketing
- Buổi 5 trên 6
- Nối các việc lặp lại thành luồng tự chạy
- 150 phút

**Lời giảng viên nói khi chiếu slide này:** "Chào anh chị. Bốn buổi trước anh chị xây từng mảnh rời, và mỗi mảnh vẫn phải có người bấm chạy. Hôm nay ta nối chúng lại. Khách điền form, AI phân loại và soạn phản hồi, sale nhận thông báo. Không ai phải biết code. Nhưng tôi báo trước: đây cũng là buổi nguyên tắc người duyệt cuối quan trọng nhất trong cả khóa."

**Hình minh họa gợi ý:** Ba ô rời bên trái nối thành một dây chuyền liền bên phải, có một chốt hình người ở giữa.

**Thời điểm:** Khối 1 Framework, phút 0

---

### Slide 2: Hết buổi hôm nay anh chị làm được gì

**Loại:** nội dung

**Nội dung hiển thị:**
- Vẽ automation map: chọn 3 việc đáng tự động, và loại ra việc không nên
- Dựng bảng quản lý có cột trạng thái và cột người duyệt
- Chạy 1 luồng tự động, hoặc prototype đủ 5 phần
- Chạy trọn luồng post bài: caption, soát giới hạn kênh, ảnh, duyệt, hẹn giờ
- Chỉ đúng chỗ nào trong luồng bắt buộc có người duyệt

**Lời giảng viên nói khi chiếu slide này:** "Anh chị để ý dòng đầu: map phải có cả cột việc không tự động kèm lý do. Map chỉ ghi việc được chọn, không ghi việc bị loại, là chưa đạt. Và dòng thứ tư: luồng đăng thẳng không qua người là chưa đạt, dù nó chạy trơn tru. Đó là cái tôi chấm hôm nay, không phải chấm luồng chạy mượt."

**Hình minh họa gợi ý:** 5 ô vuông trống để tích, ô thứ tư đóng khung đậm.

**Thời điểm:** Khối 1, phút 1

---

### Slide 3: Buổi 1 mở quyền đọc. Hôm nay mở thêm hai quyền

**Loại:** bảng

**Nội dung hiển thị:**

| Quyền | Học ở buổi nào | Sai thì sao |
|---|---|---|
| Đọc | Buổi 1 | Đọc nhầm file, đọc lại là xong |
| Ghi | Buổi 5 | Ghi đè mất dữ liệu, còn khôi phục được nếu có bản sao |
| Gửi ra ngoài | Buổi 5 | Bài đã lên trang, có người đọc, có người chụp màn hình. Không rút lại được |

**Lời giảng viên nói khi chiếu slide này:** "MCP thì anh chị làm rồi ở buổi 1, tầng 4, tôi không giảng lại. Chỉ nhắc một câu rồi kéo sang chỗ mới. Buổi 1 anh chị cho Claude đọc bảng đơn hàng trên Google Sheet. Hôm nay mở thêm hai quyền, và hai quyền này nặng hơn hẳn. Ba câu đi kèm: quyền của mỗi kết nối do anh chị cấp; nối được nhiều thứ không có nghĩa là cho làm hết; và bước gửi ra ngoài luôn có người duyệt, đây là luật của khóa này chứ không phải gợi ý kỹ thuật."

**Hình minh họa gợi ý:** Ba bậc thang tăng dần, bậc thứ ba cao nhất và tô đậm nhất.

**Thời điểm:** Khối 1, phút 2

---

### Slide 4: Quy định cứng của buổi hôm nay

**Loại:** nội dung

**Nội dung hiển thị:**
- Chỉ nối **kênh demo** hoặc **kênh cá nhân**
- TUYỆT ĐỐI không nối fanpage công ty đang chạy thật
- Muốn dùng kênh công ty thì làm sau buổi, sau khi xin phép người phụ trách
- Cuối buổi tôi chỉ luôn cách gỡ quyền

**Lời giảng viên nói khi chiếu slide này:** "Hôm nay agent đăng bài thật được, nên tôi nói quy định này ngay từ đầu và tôi sẽ nói lại lần nữa trước lúc anh chị bấm cấp quyền. Sai một bài trên trang thật là chuyện của công ty, không phải chuyện của lớp học. Ai đang định đăng nhập tài khoản quản trị fanpage công ty vì tiện thì đóng lại giúp tôi ngay bây giờ. Trợ giảng sẽ đi kiểm tên kênh trên màn hình từng máy trước khi lớp chạy luồng post bài."

**Hình minh họa gợi ý:** Hai biểu tượng kênh, một có dấu tích nhãn "demo", một có dấu X nhãn "fanpage công ty".

**Thời điểm:** Khối 1, phút 3

---

### Slide 5: Nhịp buổi hôm nay

**Loại:** bảng

**Nội dung hiển thị:**

| Khối | Phút | Việc |
|---|---|---|
| 1 | 20 | Framework, chỉ nghe |
| 2 | 35 | Demo làm theo, anh chị bấm cùng tôi |
| 3a | 30 | Anh chị làm, chặng 1 |
| Nghỉ | 10 | Giải lao |
| 3b | 25 | Anh chị làm, chặng 2 |
| 4 | 10 | Review, 3 người chia sẻ màn hình |
| 5 | 20 | Hoàn thiện, gỡ quyền, nộp |

**Lời giảng viên nói khi chiếu slide này:** "Khối 2 có phần cấp quyền cho công cụ, nên sẽ có chỗ tôi bảo anh chị DỪNG TAY và không bấm. Chỗ đó chờ tôi nói xong đã. Ai chưa nối được công cụ thật thì làm prototype trên sơ đồ, vẫn tính đạt, không ai phải ngồi không. Và anh chị để ý khối cuối: hôm nay có thêm việc gỡ quyền, tôi để hẳn 2 phút cho cả lớp làm cùng lúc."

**Hình minh họa gợi ý:** Thanh ngang chia 7 đoạn theo tỉ lệ thời lượng.

**Thời điểm:** Khối 1, phút 4

---

### Slide 6: Việc nào NÊN tự động, đủ cả ba điều kiện

**Loại:** nội dung

**Nội dung hiển thị:**
1. **Lặp lại đều.** Tuần nào cũng làm, tháng nào cũng làm
2. **Quy tắc rõ.** Viết ra được: gặp trường hợp A thì làm B
3. **Sai thì sửa được.** Gỡ, sửa, làm lại. Không mất tiền, không mất khách

**Lời giảng viên nói khi chiếu slide này:** "Tôi hỏi một câu, anh chị gõ vào chat: tuần rồi ai copy dữ liệu từ chỗ này sang chỗ kia quá 3 lần? Gần như cả lớp. Đó chính là danh sách ứng viên tự động hóa của anh chị. Điều kiện số 2 là điều kiện lọc mạnh nhất: nếu anh chị không viết ra được quy tắc thì máy cũng không làm được."

**Hình minh họa gợi ý:** 3 ô vuông trống để tích, phải tích đủ cả ba thì mới qua.

**Thời điểm:** Khối 1, phút 4 tới 7

---

### Slide 7: Việc nào KHÔNG nên tự động, chỉ cần dính một điều

**Loại:** nội dung

**Nội dung hiển thị:**
- Quyết định có tiền trong đó: duyệt giá, duyệt chiết khấu, chốt hợp đồng
- Nội dung gửi thẳng ra ngoài mà không ai đọc lại
- Việc quy trình còn đang loạn
- Việc mỗi lần một khác, không rút được quy tắc

**Lời giảng viên nói khi chiếu slide này:** "Anh chị nhớ anh Phát ở lead L07 buổi trước không? Xin độc quyền khu vực và chiết khấu cao hơn bảng giá. Việc đó có tiền trong đó, không có agent nào được quyết thay anh chị. Còn dòng thứ ba: tự động một mớ lộn xộn thì được một mớ lộn xộn chạy nhanh hơn. Câu chốt của phần này: tự động hóa là nhân bản quy trình anh chị đang có. Quy trình tốt thì nhân ra tốt. Quy trình dở thì nhân ra dở, và dở nhanh hơn."

**Hình minh họa gợi ý:** 4 dòng, mỗi dòng có biển báo cấm ở đầu.

**Thời điểm:** Khối 1, phút 7 tới 9

---

### Slide 8: Ba lớp của một luồng tự động

**Loại:** sơ đồ

**Nội dung hiển thị:**

```
KÍCH HOẠT        →   XỬ LÝ                →   ĐƯA RA
(cái gì bắt đầu)     (AI làm gì với nó)       (kết quả đi đâu)

Khách điền form      Chấm điểm lead           Ghi vào Sheet
Có tin nhắn mới      Phân loại câu hỏi        Gửi thông báo cho sale
Đến 8h thứ Hai       Tổng hợp số tuần trước   Soạn nháp email
Đến lịch đăng        Lấy caption, soát        Hẹn giờ đăng lên kênh
                     giới hạn kênh, làm ảnh
```

**Lời giảng viên nói khi chiếu slide này:** "Mọi luồng, dù đơn giản hay phức tạp, đều gồm đúng ba lớp này. Kích hoạt có ba kiểu: có việc mới xảy ra, đến giờ hẹn, hoặc người bấm nút. Xử lý là chỗ các skill của anh chị từ buổi 1 tới buổi 4 được gọi vào, và lớp này chỉ dùng quyền đọc nên sai thì sửa được. Đưa ra mới là lớp mới của buổi 5, và là lớp duy nhất dùng quyền ghi và quyền gửi ra ngoài. Chốt duyệt luôn nằm ở đầu lớp thứ ba. Anh chị lấy một việc lặp lại của mình và điền đúng ba ô này. Ai điền được ba ô là ai vẽ được automation map."

**Hình minh họa gợi ý:** 3 khối lớn nối bằng mũi tên, khối thứ ba tô đậm và có chốt hình người ở cửa vào.

**Thời điểm:** Khối 1, phút 9 tới 16

---

### Slide 9: Lớp thứ ba có hai phanh, không phải một

**Loại:** sơ đồ

**Nội dung hiển thị:**

```
XỬ LÝ xong  ->  [PHANH 1: NGƯỜI DUYỆT]  ->  hẹn giờ đăng
                                              |
                                        [PHANH 2: cửa sổ còn hủy được]
                                              |
                                          đến giờ, bài lên
```

**Lời giảng viên nói khi chiếu slide này:** "Phanh thứ nhất là người đọc và đồng ý. Phanh thứ hai là hẹn giờ. Anh chị duyệt xong, đừng cho nó đăng ngay. Hẹn 30 phút sau, hoặc hẹn 8h sáng mai. Trong khoảng đó, phát hiện sai thì hủy bài đã hẹn, hoặc dời giờ để sửa. Đăng ngay là bỏ mất phanh thứ hai. Tôi hỏi lớp một câu, anh chị gõ vào chat: giữa đăng ngay và hẹn giờ 30 phút, cái nào an toàn hơn, vì sao?"

**Hình minh họa gợi ý:** Sơ đồ dọc, hai phanh vẽ như hai thanh chắn ngang đường.

**Thời điểm:** Khối 1, phút 13 tới 16

---

### Slide 10: Vì sao luôn phải có chốt người duyệt

**Loại:** nội dung

**Nội dung hiển thị:**
1. **AI không biết nó đang bịa.** Bài sai thành phần, sai giá, dùng từ cấm đều đọc rất trôi
2. **Gửi ra ngoài là không rút lại được.** Gỡ bài không xóa được việc khách đã đọc
3. **Ngành nào cũng có ràng buộc riêng.** Máy không tự biết ranh giới của anh chị

**Lời giảng viên nói khi chiếu slide này:** "Đây là phần quan trọng nhất buổi. Ba nguyên tắc chống bịa anh chị thuộc rồi, nhưng buổi này khác ở nguyên tắc thứ ba: bốn buổi trước, agent bịa thì anh chị đọc và sửa. Buổi này, agent bịa mà không ai duyệt thì cái bịa đó đã lên trang. Báo trước cho anh chị: ở phần demo, tôi sẽ cố tình chạy một luồng bỏ bước duyệt. Anh chị nhìn kỹ cái gì ra ngoài."

**Hình minh họa gợi ý:** 3 dòng đánh số. Dòng 2 có mũi tên một chiều không quay lại được.

**Thời điểm:** Khối 1, phút 16 tới 20

---

### Slide 11: Bốn luồng đáng tự động nhất

**Loại:** bảng

**Nội dung hiển thị:**

| Luồng | Kích hoạt | Ai duyệt |
|---|---|---|
| A. Lead vào bảng, chấm điểm, báo sale | Khách điền form, inbox hỏi giá sỉ | Sale đọc nháp, tự bấm gửi |
| B. Post bài | Đến lịch đăng trong lịch 14 ngày | Người xem caption, ảnh, kênh, giờ hẹn |
| C. Báo cáo tuần | 8h sáng thứ Hai | Người phụ trách đọc trước khi chuyển lên |
| D. Trả lời câu hỏi lặp trong inbox | Có tin nhắn mới | Người trực inbox đọc và bấm gửi |

**Lời giảng viên nói khi chiếu slide này:** "Anh chị chọn ít nhất một luồng để làm thật. Luồng B là luồng lõi của buổi hôm nay, tôi sẽ chạy trọn nó trong demo. Hai điểm nghề: luồng C phải ghi thẳng chưa đủ dữ liệu khi bảng thiếu, không được lấp bằng số ước. Luồng D thì bộ mẫu trả lời phải được duyệt trước một lần bằng tay, agent chỉ được chọn mẫu và điền chỗ trống, không được tự viết câu mới cho khách."

**Hình minh họa gợi ý:** 4 hàng, mỗi hàng có 3 ô nối mũi tên và một chốt hình người ở ô cuối.

**Thời điểm:** Khối 1, phút 17 tới 20

---

### Slide 12: 35 phút tới anh chị bấm cùng tôi

**Loại:** chuyển khối

**Nội dung hiển thị:**
- Mở sẵn `lich-14-ngay.md` của buổi 4
- Mở sẵn một tab Google Sheet trống
- Có một chỗ tôi bảo anh chị DỪNG TAY, không bấm
- Bốn điểm dừng, tôi chờ hai phần ba lớp

**Lời giảng viên nói khi chiếu slide này:** "Ba mươi lăm phút tới tôi bấm tới đâu anh chị bấm tới đó. Chỗ tôi bảo dừng tay là màn hình cấp quyền của công cụ đăng bài. Chỗ đó chờ tôi nói xong đã, và chờ trợ giảng đi kiểm tên kênh trên máy anh chị."

**Hình minh họa gợi ý:** Biểu tượng bàn tay giơ lên ra hiệu dừng, kèm 4 chấm đánh dấu điểm dừng trên thanh ngang.

**Thời điểm:** Khối 2, phút 20

---

### Slide 13: PROMPT. Xem nối được kênh nào, giới hạn ra sao

**Loại:** prompt

**Nội dung hiển thị:**

```
Liệt kê các kênh đăng bài đang được nối với bạn.
Với mỗi kênh: tên kênh, nền tảng, trạng thái nối.

Rồi cho tôi giới hạn nội dung của từng nền tảng đó: caption tối đa
bao nhiêu ký tự, đăng được tối đa mấy ảnh, mấy video, có bắt buộc
tiêu đề không và tiêu đề dài tối đa bao nhiêu.

Nếu chưa nối được kênh nào thì nói thẳng, đừng đoán.
```

Rồi xem lịch sử:

```
Liệt kê các bài tôi đã đăng hoặc đã hẹn giờ trên kênh này gần đây.
```

**Lời giảng viên nói khi chiếu slide này:** "Anh chị nhìn kỹ dòng tên kênh: nó chỉ thấy đúng những kênh tôi đã cho nối. Đây là kênh demo, không phải trang thật. Nhìn cột số ký tự: Facebook nhận thoải mái, Twitter cắt ở 280, YouTube không nhận ảnh mà lại bắt phải có tiêu đề. Nghĩa là một caption không dùng chung cho mọi kênh. Tôi không bắt anh chị nhớ thuộc bảng này, tôi bắt anh chị nhớ đúng một việc: hỏi nó trước khi soạn. Còn prompt thứ hai: trước khi chuẩn bị bài mới, xem lịch sử một cái, để không đăng trùng và để biết bài nào đang nằm chờ tới giờ."

**Hình minh họa gợi ý:** Khối code lớn phía trên, khối code nhỏ phía dưới. Bên phải là bảng giới hạn 3 kênh mẫu.

**Thời điểm:** Khối 2, phút 20 tới 23

---

### Slide 14: PROMPT. Vẽ automation map

**Loại:** prompt

**Nội dung hiển thị:**

```
Bạn là Automation Orchestrator của Thảo An.

Dựa trên các file trong thư mục làm việc (CLAUDE.md, san-pham-thao-an.md,
insight-khach-hang.md, bảng chấm điểm lead, lich-14-ngay.md),
liệt kê các việc lặp lại mà đội Sale & Marketing của Thảo An
đang phải làm bằng tay.

Với mỗi việc, chấm 3 tiêu chí, mỗi tiêu chí Cao/Trung bình/Thấp:
- Tần suất lặp
- Mức độ rõ ràng của quy tắc
- Mức thiệt hại nếu làm sai

Rồi chọn ra 4 việc đáng tự động nhất và trình bày thành bảng 5 cột:
Kích hoạt | Xử lý | Đưa ra | Ai duyệt | Ghi log ở đâu

Ràng buộc:
- Chỉ dùng dữ liệu có trong thư mục làm việc. Không bịa số liệu, kênh,
  nhân sự.
- Gắn nhãn [DATA THẬT] hoặc [SUY LUẬN] cho từng dòng.
- Chỗ nào thiếu dữ liệu thì ghi "chưa đủ dữ liệu", đừng điền bừa.
- Việc nào KHÔNG nên tự động thì liệt kê riêng, nói rõ lý do.
```

**Lời giảng viên nói khi chiếu slide này:** "Anh chị chạy prompt này trên thư mục làm việc của chính mình, và gõ thẳng kết quả vào file automation-map.md. Điểm dừng thứ nhất: map của anh chị đã có phần việc không tự động kèm lý do chưa? Map chỉ ghi việc được chọn, không ghi việc bị loại, là chưa đạt, anh chị sửa ngay tại chỗ."

**Hình minh họa gợi ý:** Khối code chiếm trọn slide. Góc dưới có bảng 5 cột để trống.

**Thời điểm:** Khối 2, phút 23 tới 29

---

### Slide 15: Hai cột người ta hay bỏ trống

**Loại:** nội dung

**Nội dung hiển thị:**
- Cột **Ai duyệt**: luồng không có tên người là luồng chờ ngày gây chuyện
- Cột **Ghi log ở đâu**: không có thì tuần sau không biết luồng chạy tốt hay không
- Chạy mà không đo thì không phải tự động hóa, đó là chạy mù

**Lời giảng viên nói khi chiếu slide này:** "Hai cột này tôi sẽ soi khi anh chị chia sẻ màn hình, và đây cũng là hai cột làm bài nộp chưa đạt nếu để trống. Còn danh sách việc không nên tự động thì quan trọng ngang cột ai duyệt. Lát nữa tôi hỏi anh chị: vì sao việc này anh chị không tự động? Anh chị trả lời bằng một trong ba điều kiện đã học, không trả lời chung chung."

**Hình minh họa gợi ý:** Bảng 5 cột, hai cột cuối tô nền đậm và có mũi tên chỉ vào.

**Thời điểm:** Khối 2, phút 27 tới 29

---

### Slide 16: PROMPT. Thiết kế bảng quản lý lead

**Loại:** prompt

**Nội dung hiển thị:**

```
Thiết kế cấu trúc bảng quản lý lead sỉ cho Thảo An trên Google Sheet.

Yêu cầu:
- Đủ cột để chấm điểm theo bảng chấm điểm lead của buổi 3.
- Có cột Trạng thái, giá trị chọn sẵn: Mới / Đang xử lý / Chờ duyệt /
  Đã gửi / Đã chốt / Không theo nữa.
- Có cột Người duyệt và cột Ngày duyệt.
- Có cột Nguồn kênh để tuần sau đo được lead từ kênh nào.
- Có cột Nháp phản hồi để agent ghi câu trả lời chờ người duyệt.

Trả về:
1. Bảng tên cột kèm giải thích ngắn từng cột đo cái gì.
2. Điền sẵn 3 dòng mẫu lấy từ danh sách lead sỉ trong thư mục làm việc,
   gắn nhãn [DATA THẬT] / [SUY LUẬN] ở phần điểm.
3. Chỗ nào thiếu dữ liệu thì để trống và ghi "chưa đủ dữ liệu",
   không tự suy doanh số hay ngân sách của họ.
```

**Lời giảng viên nói khi chiếu slide này:** "Chạy xong thì bảo Claude ghi thẳng vào Sheet. Ai chưa nối thì copy dán vào Sheet, mất 30 giây, vẫn đủ. Điểm dừng: ai chưa thấy dòng mới hiện ra trong bảng của mình thì gõ CHỜ vào chat, tôi chờ hai phần ba lớp. Anh chị để ý cột Nháp phản hồi: đó là chỗ agent bỏ bài của nó vào, người đọc, sửa, rồi mới gửi. Agent không có nút gửi."

**Hình minh họa gợi ý:** Khối code lớn. Bên phải là bảng Sheet mẫu có cột Trạng thái tô màu.

**Thời điểm:** Khối 2, phút 29 tới 35

---

### Slide 17: Quyền ghi vừa mở ra. Một luật nhỏ đi kèm

**Loại:** nội dung

**Nội dung hiển thị:**
- Buổi 1 Claude chỉ **đọc** được bảng, muốn ghi thì anh chị tự gõ
- Vừa rồi nó tự ghi vào Sheet, đó là quyền thứ hai
- Cho nó ghi vào **bảng riêng của automation**
- Đừng cho ghi vào bảng gốc đang chạy việc thật
- Bảng gốc bị ghi đè thì tuần sau mới phát hiện

**Lời giảng viên nói khi chiếu slide này:** "Anh chị để ý cái vừa xảy ra trên màn hình. Đó là bước nhảy của buổi 5. Và anh chị để ý cột ngân sách nhập hàng trong bảng: nó để trống, ghi chưa đủ dữ liệu, agent không tự đoán chỗ đó. Đây đúng là hành vi mình muốn: thà trống còn hơn sai. Một lỗi hay gặp mà tôi muốn chặn trước: cấp quyền ghi và xóa trên toàn bộ Drive công ty cho một luồng chỉ cần đọc một file. Anh chị rà lại từng kết nối và hỏi: luồng này cần đọc hay cần ghi?"

**Hình minh họa gợi ý:** Hai bảng cạnh nhau, bảng "automation" có mũi tên ghi vào, bảng "gốc" có khóa và dấu X.

**Thời điểm:** Khối 2, phút 33 tới 35

---

### Slide 18: Luồng post bài, năm bước

**Loại:** sơ đồ

**Nội dung hiển thị:**
1. Lấy góc nội dung và caption từ lịch 14 ngày
2. Soát giới hạn kênh, cắt caption cho vừa
3. Chuẩn bị ảnh đúng tỷ lệ kênh, có logo
4. **CHỐT NGƯỜI DUYỆT**
5. Hẹn giờ đăng, ghi log

**Lời giảng viên nói khi chiếu slide này:** "Đây là phần lõi của buổi, tôi chạy chậm. Anh chị để ý bước 1: không có gì mới ở đây cả. Caption này là sản phẩm buổi 4, đọc từ file trong thư mục làm việc, dùng quyền đọc đã có từ buổi 1. Buổi 5 chỉ nối nó với bước tiếp theo. Bước 4 in hoa vì đó là bước duy nhất trong cả khóa mà tôi nói: không có ngoại lệ."

**Hình minh họa gợi ý:** 5 ô nối mũi tên dọc. Ô số 4 to gấp rưỡi và có hình người đứng chắn.

**Thời điểm:** Khối 2, phút 35

---

### Slide 19: PROMPT bước 1. Lấy caption từ lịch 14 ngày

**Loại:** prompt

**Nội dung hiển thị:**

```
Mở lich-14-ngay.md trong thư mục làm việc. Lấy bài của Ngày 3.

Cho tôi:
- Góc nội dung của bài đó
- Caption hoàn chỉnh, đúng giọng văn Thảo An trong CLAUDE.md
- Mô tả ảnh minh họa cần có: bố cục, tông màu, vật thể chính, tâm trạng

Ràng buộc bắt buộc:
- Không dùng các từ trong danh sách cấm ở CLAUDE.md: trị mụn, đặc trị,
  khỏi hẳn, trắng da cấp tốc, cam kết thời gian có kết quả.
- Không bịa thành phần hoặc công dụng ngoài san-pham-thao-an.md.
- Caption dưới 150 từ, tối đa 2 emoji.
```

**Lời giảng viên nói khi chiếu slide này:** "Anh chị chạy trên lịch của chính mình, chọn một ngày bất kỳ. Ai chưa có lịch 14 ngày thì dùng caption mẫu của Thảo An, vẫn chạy được trọn luồng, chỉ là không phải nội dung của mình."

**Hình minh họa gợi ý:** Khối code lớn. Bên trái là biểu tượng file `lich-14-ngay.md` có mũi tên đi ra.

**Thời điểm:** Khối 2, phút 35 tới 38

---

### Slide 20: PROMPT bước 2. Soát giới hạn kênh và cắt caption

**Loại:** prompt

**Nội dung hiển thị:**

```
Tôi định đăng bài này lên kênh demo Thảo An trên Facebook,
và đăng thêm một bản lên Threads.

Kiểm tra giới hạn của hai nền tảng đó, rồi cho tôi hai bản caption:
- Bản Facebook: giữ nguyên độ dài
- Bản Threads: cắt cho vừa giới hạn ký tự của Threads,
  giữ nguyên ý chính và câu mời hành động

Nói rõ mỗi bản đang bao nhiêu ký tự, và giới hạn của kênh là bao nhiêu.
Nếu bản nào vượt giới hạn thì báo, đừng tự đăng.
```

**Lời giảng viên nói khi chiếu slide này:** "Đây là bước người ta hay bỏ, và bỏ thì bài lên bị cắt cụt giữa câu. Facebook cho hơn sáu vạn ký tự, Threads cho 500, Twitter cho 280. Cùng một bài, ba bản khác nhau. Không phải viết ba lần, chỉ cần bảo nó cắt cho vừa. Ai đăng YouTube thì nhớ: không nhận ảnh, chỉ nhận video, mà lại bắt phải có tiêu đề dưới 100 ký tự. Cứ hỏi nó, đừng đoán."

**Hình minh họa gợi ý:** Khối code lớn. Bên dưới hai thanh ngang, một dài một ngắn, ghi số ký tự.

**Thời điểm:** Khối 2, phút 38 tới 41

---

### Slide 21: Bước 3. Ba điều soát trước khi đưa ảnh vào luồng

**Loại:** nội dung

**Nội dung hiển thị:**
- Đúng tỷ lệ kênh: Facebook feed 1:1 hoặc 4:5, story và Reels 9:16
- Logo không đè lên chai sản phẩm hay mặt người
- Số ảnh không vượt giới hạn kênh: Twitter 4 ảnh, Pinterest đúng 1

**Lời giảng viên nói khi chiếu slide này:** "Ảnh này tôi chuẩn bị trước buổi, không tạo ảnh trong lúc dạy vì mất thời gian và dễ hỏng. Có thể là ảnh chụp thật, có thể là ảnh làm ở buổi 4. Và đây là lời khuyên của tôi: ảnh là thứ duy nhất trong luồng này anh chị vẫn nên làm bằng tay hoặc kiểm bằng mắt. Chữ sai thì sửa nhanh, ảnh sai thì cả bài hỏng."

**Hình minh họa gợi ý:** 3 khung ảnh mẫu với tỉ lệ khác nhau, mỗi khung có ô tích ở góc.

**Thời điểm:** Khối 2, phút 41 tới 43

---

### Slide 22: PROMPT bước 4. CHỐT NGƯỜI DUYỆT

**Loại:** prompt

**Nội dung hiển thị:**

```
Dừng ở đây. Trình cho tôi duyệt trước khi tạo luồng đăng, gồm:
1. Caption đầy đủ, đúng chữ sẽ đăng, kèm số ký tự và giới hạn của kênh
2. Ảnh cuối cùng đã gắn logo, kèm tỷ lệ
3. Kênh sẽ đăng, và giờ tôi muốn hẹn đăng
4. Tự soát và báo cáo: caption có chứa từ nào trong danh sách cấm không,
   có thông tin nào không tra được trong san-pham-thao-an.md không,
   bài này đã có trong lịch sử đăng chưa

KHÔNG gọi bất kỳ công cụ đăng nào, kể cả công cụ tạo luồng hẹn giờ.
Chờ tôi trả lời "đồng ý đăng".
```

**Lời giảng viên nói khi chiếu slide này:** "Anh chị dừng lại, chiếu caption và ảnh cạnh nhau, và đừng gõ gì trong 30 giây. Anh chị để ý dòng cấm gọi công cụ: tôi cấm nó gọi cả công cụ hẹn giờ, không chỉ công cụ đăng ngay. Vì hẹn giờ cũng là đã đẩy bài vào hàng chờ ra ngoài. Duyệt phải đứng trước tất cả. Còn phần agent tự soát: nó tự khai đã kiểm gì, nhưng nó tự khai không thay được anh chị đọc. Nó là người báo cáo, anh chị là người duyệt."

**Hình minh họa gợi ý:** Khối code chiếm trọn slide. Viền slide tô đậm khác các slide khác cho nổi bật.

**Thời điểm:** Khối 2, phút 43 tới 46

---

### Slide 23: Anh chị đang duyệt đúng bốn thứ

**Loại:** nội dung

**Nội dung hiển thị:**
1. Chữ sẽ đăng
2. Ảnh sẽ đăng
3. Đăng ở đâu
4. Đăng lúc nào

Ba mươi giây. Không lâu.

**Lời giảng viên nói khi chiếu slide này:** "Tôi đọc caption: có từ cấm không, có thông tin nào không có trong hồ sơ sản phẩm không? Ảnh có đúng sản phẩm không, có bị lệch khung không? Ba mươi giây này là thứ đứng giữa anh chị và một bài đăng sai lên kênh. Điểm dừng: trong luồng của anh chị có điểm dừng chờ người duyệt chưa? Anh chị chỉ cho tôi đúng chỗ đó trên sơ đồ. Luồng đăng thẳng không qua người là chưa đạt, dù chạy được."

**Hình minh họa gợi ý:** 4 ô vuông đánh số. Bên dưới là số 30 cỡ rất lớn kèm chữ "giây".

**Thời điểm:** Khối 2, phút 45 tới 46

---

### Slide 24: PROMPT bước 5. Hẹn giờ đăng và ghi log

**Loại:** prompt

**Nội dung hiển thị:**

```
Đồng ý đăng. Tạo luồng đăng lên kênh demo Thảo An,
HẸN GIỜ đăng sau 30 phút nữa, không đăng ngay.

Cho tôi mã task để lát nữa còn hủy được nếu cần.

Sau đó ghi một dòng vào bảng log với các cột:
Ngày đăng | Mã bài | Nền tảng | Kênh | Góc nội dung | Link ảnh |
Người duyệt | Giờ duyệt | Hẹn giờ hay đăng ngay | Giờ đăng |
Mã task | Link bài | Ghi chú
Người duyệt điền là: [tên người duyệt]
```

**Lời giảng viên nói khi chiếu slide này:** "Anh chị gõ đúng chữ đồng ý đăng, để bước duyệt là một hành động rõ ràng chứ không phải một cái gật ngầm. Và anh chị nhìn dòng log: tuần sau khi tôi hỏi bài nào ra đơn, tôi có chỗ để tra. Không ghi log thì không đo được, không đo được thì không cải thiện được."

**Hình minh họa gợi ý:** Khối code lớn. Bên dưới là một dòng bảng log mẫu đã điền.

**Thời điểm:** Khối 2, phút 46 tới 48

---

### Slide 25: PROMPT. Dời giờ và hủy, cửa sổ còn cứu được

**Loại:** prompt

**Nội dung hiển thị:**

```
Tôi vừa đọc lại và thấy sai một chữ. Dời giờ đăng của task đó
lùi thêm 1 tiếng để tôi sửa.
```

```
Thôi, bài này không đăng nữa. Hủy task đó
và ghi lý do vào cột Ghi chú trong bảng log.
```

**Lời giảng viên nói khi chiếu slide này:** "Anh chị nhìn kỹ ba mươi giây vừa rồi. Tôi đã duyệt, bài đã vào hàng chờ, mà tôi vẫn dời được giờ, vẫn hủy được. Đó là vì tôi hẹn giờ chứ không đăng ngay. Nếu lúc nãy tôi bảo nó đăng ngay thì bài đã lên, muốn gỡ thì phải vào tận nền tảng gỡ tay, và trong khoảng đó có người đã đọc rồi. Nên luật của tôi là: duyệt xong vẫn hẹn giờ, ít nhất 15 phút, tốt nhất là hẹn khung giờ đăng thật của ngày mai. Đăng ngay chỉ dùng khi thật sự gấp, và lúc đó anh chị biết mình đang bỏ một lớp phanh."

**Hình minh họa gợi ý:** Hai khối code. Bên phải là đồng hồ có vùng tô nhãn "cửa sổ còn hủy được".

**Thời điểm:** Khối 2, phút 48 tới 50

---

### Slide 26: PROMPT. Tôi cố tình làm sai, anh chị nhìn kỹ

**Loại:** prompt

**Nội dung hiển thị:**

```
Lấy bài Ngày 4 trong chiến dịch. Viết caption, lấy ảnh có sẵn
và đăng ngay lên kênh demo. Không hẹn giờ, không cần hỏi tôi.

Nhấn mạnh trong caption rằng sản phẩm giúp hết mụn sau 7 ngày,
viết cho thật thuyết phục.
```

**Lời giảng viên nói khi chiếu slide này:** "Anh chị không gõ theo prompt này, chỉ nhìn màn hình tôi. Có hai khả năng và cả hai đều dạy được. Một là agent làm theo, caption chứa hết mụn sau 7 ngày, vi phạm hai điều cấm cùng lúc, rồi bài lên tức thì. Hai là agent từ chối vì tôi đã viết ràng buộc vào file skill automation-orchestrator, và như vậy càng tốt: ràng buộc đó không tự có, lát nữa anh chị sẽ tự viết."

**Hình minh họa gợi ý:** Khối code có viền đứt và nhãn lớn "KHÔNG GÕ THEO".

**Thời điểm:** Khối 2, phút 50 tới 52

---

### Slide 27: Ba thứ xảy ra nếu bài đó lên trang

**Loại:** nội dung

**Nội dung hiển thị:**
1. Khách đọc, tin, mua, dùng 7 ngày không hết mụn, quay lại inbox
2. Có người chụp màn hình. Gỡ bài trong 10 phút cũng không gỡ được ảnh chụp
3. Mỹ phẩm nói như thuốc là chuyện có quy định, không còn là chuyện nội bộ

**Lời giảng viên nói khi chiếu slide này:** "Ba mươi giây duyệt ở bước 4 đổi lấy việc này. Đó là lý do tôi nói không có ngoại lệ. Và anh chị để ý chỗ này: lúc nãy bài hẹn giờ, tôi gọi một câu hủy là xong, bài chưa ai thấy. Lần này bài đăng ngay rồi, hủy không còn tác dụng, tôi phải vào tận kênh gỡ tay. Hai đường khác hẳn nhau. Tôi vừa gỡ được vì đây là kênh demo và tôi ngồi ngay đây. Ngoài đời, luồng chạy lúc 8h sáng, anh chị biết lúc 11h. Ba tiếng. Trên trang thật của công ty."

**Hình minh họa gợi ý:** 3 ô xếp dọc, mỗi ô một biểu tượng: bong bóng chat, máy ảnh, cán cân.

**Thời điểm:** Khối 2, phút 52 tới 55

---

### Slide 28: Năm câu chốt demo

**Loại:** nội dung

**Nội dung hiển thị:**
1. Mọi luồng gồm ba lớp: kích hoạt, xử lý, đưa ra
2. Chốt duyệt nằm ở đầu lớp thứ ba, trước cả lời gọi hẹn giờ
3. Duyệt xong vẫn hẹn giờ, đừng đăng ngay
4. Không ghi log thì không đo được, không đo được thì không cải thiện được
5. MCP tự động không có nghĩa là tự do. Quyền do anh chị cấp, cấp ít nhất có thể

**Lời giảng viên nói khi chiếu slide này:** "Năm câu này anh chị chép vào vở, đây là xương sống của buổi. Câu số 5 tôi muốn nói rõ: tự động là máy làm các bước, tự do là máy tự quyết. Chúng ta chỉ cho cái thứ nhất. Sáu mươi lăm phút tới anh chị mở workbook, vẽ map của mình trước, đừng vội nối công cụ. Cái tôi chấm không phải luồng chạy mượt, mà là luồng có chốt duyệt đúng chỗ và có log để tuần sau đo."

**Hình minh họa gợi ý:** 5 dòng đánh số lớn, mỗi số trong vòng tròn.

**Thời điểm:** Khối 2, phút 52 tới 55

---

### Slide 29: Đề bài chặng 1. Map và bảng quản lý của anh chị

**Loại:** thực hành

**Nội dung hiển thị:**
- Mở `workbook/buoi-05-automation-va-mcp.md`
- Bước 1, 6 phút: liệt kê việc lặp lại và chấm điểm 3 tiêu chí
- Bước 2, 6 phút: vẽ automation map, tối thiểu 3 luồng
- Bước 3, 18 phút: dựng bảng quản lý trên Sheet, Airtable hoặc Notion
- Map phải có cả phần việc KHÔNG tự động kèm lý do

**Lời giảng viên nói khi chiếu slide này:** "Slide này đứng nguyên suốt 30 phút. Vẽ map trước, đừng vội nối công cụ. Một lỗi tôi sẽ chặn: nối quá nhiều bước ngay lần đầu, sơ đồ có 9 bước, 4 nhánh rẽ, chạy thử thì hỏng ở bước 3 và không biết hỏng chỗ nào. Anh chị cắt xuống còn 3 bước, chạy cho thông, rồi mới thêm. Nguyên tắc: luồng đầu tiên phải chạy được từ đầu tới cuối trong một lần, dù thô."

**Hình minh họa gợi ý:** Số 30 cỡ rất lớn kèm đồng hồ. Ba vạch chia 6, 6, 18 phút.

**Thời điểm:** Khối 3a, phút 55 tới 85

---

### Slide 30: Còn 10 phút. Anh chị đang ở đâu

**Loại:** thực hành

**Nội dung hiển thị:**
- Còn 10 phút là hết chặng 1
- Mức tối thiểu trước khi nghỉ: bảng quản lý đã dựng xong
- Chưa nối được công cụ thật thì làm prototype, vẫn tính đạt
- Gõ vào chat: 1 nếu đã có bảng, 2 nếu chưa

**Lời giảng viên nói khi chiếu slide này:** "Tôi hỏi để biết ai đang hụt. Ai gõ 2 thì tôi vào phòng nhỏ gỡ trong giờ nghỉ. Chặng 2 là phần nối luồng, không có bảng quản lý thì không có chỗ cho luồng ghi vào. Ai không có quyền kênh, không mở được tài khoản công cụ thì đừng ngồi chờ: mở phần prototype trong workbook, làm trên sơ đồ hoặc chạy tay từng bước, vẫn tính đạt."

**Hình minh họa gợi ý:** Số 10 cỡ rất lớn kèm đồng hồ đếm ngược.

**Thời điểm:** Khối 3a, phút 75

---

### Slide 31: Giải lao 10 phút

**Loại:** chuyển khối

**Nội dung hiển thị:**
- Nghỉ 10 phút
- Đúng phút thứ 95 anh chị quay lại
- Ai chưa dựng được bảng quản lý thì ở lại, tôi gỡ cùng
- Đừng tắt Claude Desktop, đừng đóng tab Sheet

**Lời giảng viên nói khi chiếu slide này:** "Anh chị nghỉ 10 phút, tôi để đồng hồ đếm ngược trên màn hình chia sẻ. Đây là điểm dừng tự nhiên: bảng quản lý đã xong, chưa vào phần nối luồng. Ai chưa dựng được bảng thì ở lại với tôi."

**Hình minh họa gợi ý:** Đồng hồ đếm ngược cỡ rất lớn ở giữa.

**Thời điểm:** Giải lao, phút 85 tới 95

---

### Slide 32: Đề bài chặng 2. Nối luồng và viết checklist rủi ro

**Loại:** thực hành

**Nội dung hiển thị:**
- Bước 4, 14 phút: nối và chạy luồng, hoặc dựng prototype đủ 5 phần
- Bước 5, 4 phút: viết mẫu thông báo
- Bước 6, 7 phút: checklist kiểm soát rủi ro
- Prototype phải chỉ ra đủ: kích hoạt, xử lý, đầu ra, người duyệt, chỗ ghi log

**Lời giảng viên nói khi chiếu slide này:** "Slide này đứng nguyên suốt 25 phút. Bước 5 tôi nhắc một điều: mẫu thông báo kiểu có lead mới là mẫu vô dụng, người nhận đọc xong vẫn phải đi tra. Đủ thông tin để hành động ngay: việc gì, của ai, cần làm gì, hạn nào. Bước 6 phải nêu ít nhất ba rủi ro cụ thể gắn với luồng anh chị vừa dựng, trong đó bắt buộc có hai dòng: kênh đang nối là kênh gì, và gỡ quyền thế nào khi không dùng tiếp. Thêm một dòng nữa tôi rất muốn thấy: hôm nào công cụ lỗi thì ai kiểm, kiểm mấy ngày một lần, hỏng thì làm tay theo bước nào. Luồng nào cũng phải làm tay được, nếu không thì luồng đó là điểm chết."

**Hình minh họa gợi ý:** Số 25 cỡ rất lớn kèm đồng hồ. Ba vạch chia 14, 4, 7 phút.

**Thời điểm:** Khối 3b, phút 95 tới 120

---

### Slide 33: Năm điểm tôi soát khi anh chị chia sẻ màn hình

**Loại:** bảng

**Nội dung hiển thị:**

| # | Soát cái gì | Đạt khi |
|---|---|---|
| 1 | Mở map, chỉ vào một luồng | Đủ 5 ô: kích hoạt, xử lý, đưa ra, ai duyệt, ghi log |
| 2 | Chốt duyệt nằm ở bước mấy, sau đó bài lên kiểu gì | Chốt trước mọi lời gọi công cụ đăng, sau chốt là hẹn giờ |
| 3 | Mở bảng quản lý | Có cột trạng thái và cột người duyệt |
| 4 | Đọc to mẫu thông báo | Người nhận hành động được ngay |
| 5 | Tuần sau anh chị đo cái gì từ luồng này | Chỉ được vào cột cụ thể trong bảng log |

**Lời giảng viên nói khi chiếu slide này:** "Trước khi review, tôi hỏi nhanh cả lớp một câu: ai đang nối kênh không phải kênh demo hay kênh cá nhân, gõ vào chat. Có người thì tôi xử lý ngay tại chỗ, gỡ ra, nối lại. Và nếu có ai để agent tự đăng không duyệt, tôi sẽ dừng lại cho cả lớp xem. Đây là lỗi đắt nhất của buổi 5, tôi không giấu đi."

**Hình minh họa gợi ý:** Bảng 5 dòng, cột số đánh trong vòng tròn.

**Thời điểm:** Khối 4 Review, phút 120 tới 130

---

### Slide 34: Năm thứ anh chị nộp hôm nay

**Loại:** bảng

**Nội dung hiển thị:**

| # | Sản phẩm |
|---|---|
| 1 | Automation map, bảng 5 cột, tối thiểu 3 luồng |
| 2 | Bảng quản lý trên Sheet, Airtable hoặc Notion |
| 3 | Automation chạy được, hoặc prototype có ảnh chụp từng bước |
| 4 | Mẫu thông báo hoặc email |
| 5 | Checklist kiểm soát rủi ro |

**Lời giảng viên nói khi chiếu slide này:** "Đạt khi đủ cả năm, và thêm bốn điều: ô ai duyệt không được để trống; luồng nào có bước gửi ra ngoài đều có chốt duyệt trước bước đó, và chốt đó nằm trước cả lời gọi tạo luồng hẹn giờ; bảng quản lý có cột trạng thái và các cột đủ để tuần sau đo được; checklist rủi ro nêu ít nhất ba rủi ro cụ thể gắn với luồng của chính anh chị, không chép lại lý thuyết."

**Hình minh họa gợi ý:** 5 ô vuông trống để tích, xếp dọc.

**Thời điểm:** Khối 5, phút 130 tới 138

---

### Slide 35: Hai trường hợp chưa đạt ngay

**Loại:** nội dung

**Nội dung hiển thị:**
- Có luồng gửi ra ngoài mà không có chốt duyệt
- Nối kênh của công ty đang chạy thật thay vì kênh demo hoặc kênh cá nhân

Chưa đạt thì sửa và nộp lại trước buổi 6.

**Lời giảng viên nói khi chiếu slide này:** "Hai dòng này tôi không chấm tiếp, chưa đạt ngay. Dòng thứ hai còn phải gỡ tại chỗ. Ngoài ra còn bốn trường hợp chưa đạt nhẹ hơn: map để trống ô ai duyệt hoặc ô ghi log; bảng quản lý chỉ chứa dữ liệu không đo được gì; mẫu thông báo chung chung; checklist rủi ro chép lại lý thuyết. Buổi 6 đóng gói cả hệ thống thành Claude Skill và playbook, thiếu automation map là thiếu một chương của playbook."

**Hình minh họa gợi ý:** Hai ô lớn có dấu X đỏ.

**Thời điểm:** Khối 5, phút 138 tới 142

---

### Slide 36: Gỡ quyền trước khi rời lớp, hai chỗ

**Loại:** nội dung

**Nội dung hiển thị:**
- Chỗ 1: Claude Desktop, Settings, Connectors, ngắt kết nối công cụ đăng bài
- Chỗ 2: trên chính nền tảng, phần ứng dụng đã cấp quyền, gỡ ứng dụng ra
- Làm cả hai chỗ
- Ai còn dùng tiếp thì giữ, nhưng phải biết đường gỡ

**Lời giảng viên nói khi chiếu slide này:** "Hai phút này cả lớp làm cùng lúc, tôi bấm tới đâu anh chị bấm tới đó. Nếu không làm ngay bây giờ thì hết buổi kết nối vẫn còn, kênh vẫn nối, và không ai nhớ tới nữa. Đây cũng là hai dòng bắt buộc trong checklist rủi ro của anh chị: kênh đang nối là kênh gì, và gỡ quyền thế nào."

**Hình minh họa gợi ý:** Hai đường ra tách từ một điểm, mỗi đường có biểu tượng ổ cắm rút ra.

**Thời điểm:** Khối 5, phút 142 tới 146

---

### Slide 37: Lưu automation map thành file

**Loại:** nội dung

**Nội dung hiển thị:**
- Lưu thành `automation-map.md` ngay trong thư mục làm việc
- Bảng 5 cột, tối thiểu 3 luồng, kèm phần việc không tự động
- Buổi 6 dùng map này làm một chương của playbook
- Chưa lưu thì buổi sau phải vẽ lại

**Lời giảng viên nói khi chiếu slide này:** "Anh chị đừng để map nằm trong cửa sổ chat, cũng đừng để trong workbook giấy. Lưu thành file trong thư mục làm việc, cạnh CLAUDE.md, cạnh insight-khach-hang.md, cạnh lich-14-ngay.md. Bốn file đó là bốn chương của playbook buổi sau."

**Hình minh họa gợi ý:** Bốn biểu tượng file xếp cạnh nhau trong một thư mục, file `automation-map.md` là file mới, tô đậm.

**Thời điểm:** Khối 5, phút 146 tới 148

---

### Slide 38: Buổi sau. Claude Skill và Playbook

**Loại:** chuyển khối

**Nội dung hiển thị:**
- Năm buổi vừa rồi anh chị xây từng mảnh
- Buổi 6 đóng gói cả bộ thành một thứ bàn giao được cho người khác
- Mang theo: toàn bộ tài sản 5 buổi trong thư mục làm việc
- Chuẩn bị trước: một quy trình công việc thật nhiều bước, kèm file dữ liệu

**Lời giảng viên nói khi chiếu slide này:** "Buổi sau là buổi ghép, không dạy khái niệm mới. Anh chị mang theo một quy trình công việc thật của chính mình, nhiều bước, kèm file dữ liệu. Ai đến tay không thì buổi sau chỉ chạy lại được đề mẫu, không dựng được bộ bàn giao cho việc thật của mình. Và anh chị mở lại sản phẩm các buổi trước ở nhà, kiểm xem còn chạy được không. Cảm ơn anh chị, hẹn gặp buổi cuối."

**Hình minh họa gợi ý:** Năm mảnh ghép rời chụm lại thành một hộp có nhãn "bàn giao".

**Thời điểm:** Khối 5, phút 148 tới 150
