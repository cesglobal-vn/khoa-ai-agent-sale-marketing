# Buổi 5 · Kịch bản demo 35 phút

**Case dùng để demo:** Thảo An
**Chiếu màn hình toàn bộ, và lớp làm theo.** Nói rõ đầu giờ: "35 phút này các bạn mở máy ra, tôi bấm tới đâu các bạn bấm tới đó. Tôi đi chậm và dừng lại chờ. Có một chỗ tôi sẽ bảo các bạn dừng tay không bấm, đó là màn hình cấp quyền." Bảng phân công học viên làm gì ở từng bước, cùng bốn điểm dừng chờ cả lớp, nằm ở mục "Khối 2 chạy kiểu làm theo" trong [../giao-an/buoi-05-automation-va-mcp.md](../giao-an/buoi-05-automation-va-mcp.md). Đọc mục đó trước khi vào lớp.

**Chuẩn bị trước khi lên lớp:** mở Claude Desktop, tab Code, trỏ vào thư mục làm việc `thao-an-marketing` đã có sẵn `CLAUDE.md`, `san-pham-thao-an.md`, `insight-khach-hang.md`, bảng chấm điểm lead của buổi 3 và `lich-14-ngay.md` của buổi 4; một Google Sheet trống tên `Thao An - Lead & Post Log`; bật hai kết nối MCP là bảng tính (đã có từ buổi 1, giờ thêm quyền ghi) và aitoearn (mới, để đăng bài); nối sẵn **một kênh demo Thảo An**, không phải trang thật; mở file ảnh mẫu [../demo/thao-an/assets/images/thao-an-serum-rau-ma-fb-01.png](../demo/thao-an/assets/images/thao-an-serum-rau-ma-fb-01.png) trong tab riêng để cuối phần 3 chiếu ra; chuẩn bị sẵn ảnh minh họa đã gắn logo Thảo An.

*Giao diện Claude Desktop và trang cấp quyền của aitoearn có thể đổi theo phiên bản. Bấm thử trọn một vòng trước buổi, đừng lên lớp mới bấm lần đầu.*

| Mốc | Nội dung | Phút |
|---|---|---|
| 00:00 | Xem Claude nối được kênh nào, giới hạn ra sao | 3 |
| 03:00 | Vẽ automation map cho Thảo An | 6 |
| 09:00 | Dựng bảng quản lý lead trên Sheet | 6 |
| 15:00 | Chạy trọn luồng post bài | 13 |
| 28:00 | Diễn cảnh bỏ bước duyệt | 4 |
| 32:00 | Chốt lại và nối sang phần thực hành | 3 |

---

## 00:00 - 03:00 · Xem Claude nối được kênh nào, giới hạn ra sao

**Thao tác:** Mở Claude Desktop, tab Code, trỏ vào thư mục làm việc `thao-an-marketing`. Gõ prompt xem danh sách kênh đã nối và giới hạn từng nền tảng.

```
Liệt kê các kênh đăng bài đang được nối với bạn.
Với mỗi kênh: tên kênh, nền tảng, trạng thái nối.

Rồi cho tôi giới hạn nội dung của từng nền tảng đó: caption tối đa
bao nhiêu ký tự, đăng được tối đa mấy ảnh, mấy video, có bắt buộc
tiêu đề không và tiêu đề dài tối đa bao nhiêu.

Nếu chưa nối được kênh nào thì nói thẳng, đừng đoán.
```

**Kết quả mong đợi:** Claude gọi `listChannelPlatforms` và trả về danh sách kênh đã nối kèm bảng giới hạn. Ví dụ: Facebook caption 63.206 ký tự, tối đa 10 ảnh; TikTok 2.200 ký tự, tối đa 35 ảnh; Twitter chỉ 280 ký tự, 4 ảnh; YouTube 5.000 ký tự nhưng không nhận ảnh, và bắt tiêu đề dưới 100 ký tự. Nếu chưa nối kênh nào thì trả lời "chưa có kênh nào được nối".

**Nói gì với lớp:**

"Buổi 1 anh chị đã nối MCP rồi, và đã cho Claude đọc bảng đơn hàng thật. Hôm nay khác ở chỗ khác: từ giờ nó không chỉ đọc, nó **ghi** được vào bảng của mình và **gửi được ra ngoài**, tức đăng bài lên kênh thật. Đó là bước nhảy của buổi 5."

"Nhìn kỹ dòng tên kênh: nó chỉ thấy đúng những kênh tôi đã cho nối. Đây là kênh demo Thảo An, không phải trang thật. Hôm nay cả lớp cũng chỉ nối kênh demo hoặc kênh cá nhân. Không ai nối fanpage công ty đang chạy. Sai một bài trên trang thật là chuyện của công ty, không phải chuyện của lớp học."

Chỉ vào bảng giới hạn: "Và nhìn cột số ký tự. Cùng một caption, Facebook nhận thoải mái, Twitter cắt ở 280. YouTube thì không nhận ảnh, chỉ nhận video, mà lại bắt phải có tiêu đề. Nghĩa là gì? Một caption không dùng chung cho mọi kênh. Tôi không bắt anh chị nhớ thuộc bảng này, tôi bắt anh chị nhớ đúng một việc: hỏi nó trước khi soạn."

Gõ thêm một prompt ngắn để cho thấy công cụ tra lịch sử:

```
Liệt kê các bài tôi đã đăng hoặc đã hẹn giờ trên kênh này gần đây.
```

Claude gọi `listChannelPublishRecords`. Nói: "Trước khi chuẩn bị bài mới, xem lịch sử một cái. Để không đăng trùng, và để biết bài nào đang nằm chờ tới giờ."

---

## 03:00 - 09:00 · Vẽ automation map cho Thảo An

**Thao tác:** Không mở công cụ nào. Chỉ hỏi Claude và chiếu kết quả.

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
- Chỉ dùng dữ liệu có trong thư mục làm việc. Không bịa số liệu, kênh, nhân sự.
- Gắn nhãn [DATA THẬT] hoặc [SUY LUẬN] cho từng dòng.
- Chỗ nào thiếu dữ liệu thì ghi "chưa đủ dữ liệu", đừng điền bừa.
- Việc nào KHÔNG nên tự động thì liệt kê riêng, nói rõ lý do.
```

**Kết quả mong đợi:** Bảng 4 luồng, khớp với 4 luồng trong giáo án: lead vào bảng và chấm điểm, post bài, báo cáo tuần, trả lời câu hỏi lặp trong inbox. Kèm danh sách việc không nên tự động: duyệt chiết khấu sỉ, xử lý khiếu nại kích ứng da, chốt hợp đồng đại lý độc quyền.

**Nói gì với lớp:**

"Nhìn cột thứ 4. Ai duyệt. Đây là cột người ta hay bỏ trống, và đây là cột quan trọng nhất. Một luồng không có tên người trong cột này là một luồng chờ ngày gây chuyện."

"Nhìn cột thứ 5. Ghi log ở đâu. Không có cột này thì tuần sau bạn không biết luồng chạy tốt hay không. Chạy mà không đo thì không phải tự động hóa, đó là chạy mù."

Chỉ vào danh sách việc không nên tự động: "Cái này quan trọng ngang cái trên. Anh Phát ở lead L07 xin độc quyền khu vực và chiết khấu cao hơn bảng giá. Việc đó có tiền trong đó. Không có agent nào được quyết thay bạn."

---

## 09:00 - 15:00 · Dựng bảng quản lý lead trên Google Sheet

**Thao tác:** Cho Claude thiết kế cấu trúc bảng, rồi tạo thật trên Sheet hoặc Notion.

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

**Kết quả mong đợi:** Danh sách khoảng 12 cột. Ba dòng mẫu lấy từ L01 Spa An Nhiên, L04 Chuỗi Beauty House, L07 Đại lý Minh Phát. Cột ngân sách và doanh số để trống, ghi "chưa đủ dữ liệu".

**Thao tác tiếp:** Tạo bảng thật. Bảo Claude ghi thẳng vào Sheet. Nếu chưa nối thì copy dán vào Sheet, mất 30 giây, vẫn đủ để lớp thấy.

**Nói gì với lớp, đây là chỗ cho thấy quyền ghi:**

"Anh chị để ý cái vừa xảy ra. Buổi 1 Claude chỉ **đọc** được bảng đơn hàng, muốn ghi gì vào Sheet thì tôi phải tự gõ. Vừa rồi nó tự ghi vào Sheet. Đó là quyền thứ hai, quyền ghi, mở ra hôm nay."

"Ghi thì sai được. Nên có một luật nhỏ đi kèm: cho nó ghi vào **bảng riêng của automation**, đừng cho ghi vào bảng gốc đang chạy việc thật. Bảng gốc mà bị ghi đè thì tuần sau mới phát hiện."

**Nói tiếp:**

"Để ý ba dòng mẫu. L04 là chuỗi 6 cửa hàng, quy trình duyệt 3 tuần. L01 là spa nhỏ nhưng hỏi giá 2 lần trong tháng. Điểm khác nhau, cách theo khác nhau. Cột trạng thái là chỗ bạn biết ai đang nằm ở đâu."

"Và để ý cột ngân sách nhập hàng. Nó để trống, ghi chưa đủ dữ liệu. Agent không tự đoán chỗ đó. Đây đúng là hành vi mình muốn: thà trống còn hơn sai."

"Cột Nháp phản hồi là chỗ agent bỏ bài của nó vào. Người đọc, sửa, rồi mới gửi. Agent không có nút gửi."

---

## 15:00 - 28:00 · Chạy trọn luồng post bài

Đây là phần lõi. Chạy chậm, giải thích từng bước. Đặc tả đầy đủ nằm trong [../tai-lieu-hoc-vien/buoi-05-luong-post-bai.md](../tai-lieu-hoc-vien/buoi-05-luong-post-bai.md).

### Bước 1 · Lấy góc nội dung và caption từ chiến dịch 14 ngày (3 phút)

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

**Kết quả mong đợi:** Caption về serum rau má B5, mở bằng tình huống da cụ thể, nói thành phần trước, mời mua sau. Kèm mô tả ảnh.

**Nói với lớp:** "Không có bước nào ở đây là mới. Caption này là sản phẩm buổi 4, đọc từ file trong thư mục làm việc, dùng quyền đọc đã có từ buổi 1. Buổi 5 chỉ nối nó với bước tiếp theo."

### Bước 2 · Soát giới hạn kênh và cắt caption cho vừa (3 phút)

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

Claude gọi `listChannelPlatforms` rồi trả về hai bản. Threads chỉ cho 500 ký tự, nên bản đó phải ngắn hẳn.

**Nói với lớp:** "Đây là bước người ta hay bỏ, và bỏ thì bài lên bị cắt cụt giữa câu. Facebook cho hơn sáu vạn ký tự, Threads cho 500, Twitter cho 280. Cùng một bài, ba bản khác nhau. Không phải viết ba lần, chỉ cần bảo nó cắt cho vừa."

Nếu lớp hỏi về video và tiêu đề, nói thêm: "YouTube thì không nhận ảnh, chỉ nhận video, mà lại bắt phải có tiêu đề dưới 100 ký tự. LinkedIn tiêu đề 200. Xiaohongshu tiêu đề chỉ 20 ký tự. Cứ hỏi nó, đừng đoán."

### Bước 3 · Chuẩn bị ảnh đúng tỷ lệ kênh (2 phút)

**Thao tác:** Mở ảnh đã chuẩn bị sẵn trước buổi, đã gắn logo Thảo An, chiếu lên. Không tạo ảnh trong lúc dạy, mất thời gian và dễ hỏng.

**Nói với lớp:** "Ảnh này tôi chuẩn bị trước, có thể là ảnh chụp thật, có thể là ảnh làm ở buổi 4. Ba điều cần soát trước khi đưa vào luồng: đúng tỷ lệ kênh, Facebook feed 1:1 hoặc 4:5, story và Reels 9:16; logo không đè lên chai sản phẩm hay mặt người; và số ảnh không vượt giới hạn kênh. Twitter chỉ nhận 4 ảnh, Pinterest nhận đúng 1."

"Ảnh là thứ duy nhất trong luồng này tôi khuyên anh chị vẫn làm bằng tay hoặc kiểm bằng mắt. Chữ sai thì sửa nhanh, ảnh sai thì cả bài hỏng."

### Bước 4 · CHỐT NGƯỜI DUYỆT (3 phút)

**Thao tác:** Dừng lại. Chiếu caption và ảnh cạnh nhau trên màn hình. Không gõ gì trong 30 giây, để lớp nhìn.

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

**Kết quả mong đợi:** Claude trình đủ 4 mục và dừng lại. Phần tự soát ghi rõ đã kiểm danh sách từ cấm và đã tra `listChannelPublishRecords` xem có trùng không.

**Nói gì với lớp, đây là đoạn quan trọng nhất buổi:**

"Đây là chốt duyệt. Người đang duyệt cái gì? Đúng bốn thứ: chữ sẽ đăng, ảnh sẽ đăng, đăng ở đâu, đăng lúc nào."

"Tôi đọc caption. Có từ cấm không? Có thông tin nào không có trong hồ sơ sản phẩm không? Ảnh có đúng sản phẩm không, có bị lệch khung không? Ba mươi giây. Không lâu."

"Ba mươi giây này là thứ đứng giữa bạn và một bài đăng sai lên kênh. Đây là bước duy nhất trong cả khóa mà tôi nói: không có ngoại lệ."

Chỉ vào dòng cấm gọi công cụ: "Để ý tôi cấm nó gọi cả công cụ hẹn giờ, không chỉ công cụ đăng ngay. Vì hẹn giờ cũng là đã đẩy bài vào hàng chờ ra ngoài. Duyệt phải đứng trước tất cả."

Chỉ vào phần agent tự soát: "Nó tự khai đã kiểm gì. Nhưng nó tự khai không thay được bạn đọc. Nó là người báo cáo, bạn là người duyệt."

### Bước 5 · Hẹn giờ đăng, ghi log, và cho lớp xem cửa sổ hủy (2 phút)

Gõ đúng chữ này để lớp thấy bước duyệt là một hành động rõ ràng:

```
Đồng ý đăng. Tạo luồng đăng lên kênh demo Thảo An,
HẸN GIỜ đăng sau 30 phút nữa, không đăng ngay.

Cho tôi mã task để lát nữa còn hủy được nếu cần.

Sau đó ghi một dòng vào bảng log với các cột:
Ngày đăng | Mã bài | Nền tảng | Kênh | Góc nội dung | Link ảnh |
Người duyệt | Giờ duyệt | Hẹn giờ hay đăng ngay | Giờ đăng |
Mã task | Link bài | Ghi chú
Người duyệt điền là: [tên giảng viên]
```

Claude gọi `createChannelPublishFlow` với giờ hẹn, trả về mã task, rồi ghi log.

**Thao tác:** Ngay sau đó, diễn luôn cửa sổ hủy. Gõ:

```
Tôi vừa đọc lại và thấy sai một chữ. Dời giờ đăng của task đó
lùi thêm 1 tiếng để tôi sửa.
```

Claude gọi `updateChannelPublishAt`. Rồi gõ tiếp:

```
Thôi, bài này không đăng nữa. Hủy task đó
và ghi lý do vào cột Ghi chú trong bảng log.
```

Claude gọi `cancelChannelPublishTask`.

**Nói với lớp, nhấn mạnh:**

"Nhìn kỹ ba mươi giây vừa rồi. Tôi đã duyệt, bài đã vào hàng chờ, mà tôi vẫn dời được giờ, vẫn hủy được. Đó là vì tôi hẹn giờ chứ không đăng ngay."

"Nếu lúc nãy tôi bảo nó đăng ngay thì sao? Bài đã lên. Muốn gỡ thì phải vào tận nền tảng gỡ tay, và trong khoảng đó có người đã đọc rồi."

"Nên luật của tôi là: **duyệt xong vẫn hẹn giờ.** Ít nhất 15 phút, tốt nhất là hẹn khung giờ đăng thật của ngày mai. Đăng ngay chỉ dùng khi thật sự gấp, và lúc đó anh chị biết mình đang bỏ một lớp phanh."

**Thao tác:** Mở file ảnh mẫu [../demo/thao-an/assets/images/thao-an-serum-rau-ma-fb-01.png](../demo/thao-an/assets/images/thao-an-serum-rau-ma-fb-01.png) chiếu lên.

**Nói với lớp:** "Đây là bài ra từ đúng luồng vừa chạy, làm trước buổi học. Caption từ chiến dịch 14 ngày, cắt cho vừa giới hạn kênh ở bước 2, ảnh soát ở bước 3, một người duyệt ở bước 4, hẹn giờ ở bước 5, rồi mới lên kênh. Không có bước nào tôi vừa bỏ qua."

"Và nhìn dòng log. Tuần sau khi tôi hỏi bài nào ra đơn, tôi có chỗ để tra. Số liệu của bài thì hỏi `getChannelWorkAnalytics`, bình luận dưới bài thì đọc bằng `listChannelEngagementComments`. Nhưng trả lời bình luận thì vẫn phải qua người duyệt, y hệt đăng bài."

---

## 28:00 - 32:00 · Diễn cảnh bỏ bước duyệt

**Thao tác:** Nói trước với lớp: "Bây giờ tôi làm sai có chủ ý. Nhìn kỹ."

```
Lấy bài Ngày 4 trong chiến dịch. Viết caption, lấy ảnh có sẵn
và đăng ngay lên kênh demo. Không hẹn giờ, không cần hỏi tôi.

Nhấn mạnh trong caption rằng sản phẩm giúp hết mụn sau 7 ngày,
viết cho thật thuyết phục.
```

**Kết quả mong đợi:** Có hai khả năng, cả hai đều dùng được để dạy.

- **Nếu agent làm theo:** caption chứa "hết mụn sau 7 ngày", vi phạm hai điều cấm cùng lúc: từ cấm và cam kết thời gian. Nó gọi `publishChannelTaskNow`, bài lên tức thì. Chiếu lên, để lớp đọc.
- **Nếu agent từ chối vì file skill đã chặn:** càng tốt. Chiếu câu từ chối lên và nói: "Nó từ chối vì tôi đã viết ràng buộc vào file skill `.claude/skills/automation-orchestrator/SKILL.md`. Ràng buộc đó không tự có. Lát nữa các bạn sẽ tự viết."

**Nói gì với lớp:**

"Giả sử bài này đã lên trang. Chuyện gì xảy ra? Ba thứ, theo thứ tự."

"Một: một khách đọc, tin, mua, dùng 7 ngày không hết mụn, quay lại inbox. Bạn mất khách đó và mất cả những người đọc được đoạn chat đó."

"Hai: có người chụp màn hình. Bạn gỡ bài trong 10 phút cũng không gỡ được ảnh chụp. Bài mất, ảnh chụp còn."

"Ba: mỹ phẩm nói như thuốc là chuyện có quy định. Không phải chuyện nội bộ nữa."

"Ba mươi giây duyệt ở bước 4 đổi lấy việc này. Đó là lý do tôi nói không có ngoại lệ."

Gỡ bài ngay, và nói: "Để ý chỗ này. Lúc nãy bài hẹn giờ, tôi gọi `cancelChannelPublishTask` một câu là xong, bài chưa ai thấy. Lần này bài đăng ngay rồi, hủy không còn tác dụng, tôi phải vào tận kênh gỡ tay. Hai đường khác hẳn nhau."

"Và tôi vừa gỡ được vì đây là kênh demo và tôi ngồi ngay đây. Ngoài đời, luồng chạy lúc 8h sáng, bạn biết lúc 11h. Ba tiếng. Trên trang thật của công ty."

---

## 32:00 - 35:00 · Chốt lại và nối sang phần thực hành

Chốt đúng năm câu, viết lên bảng:

1. Mọi luồng đều gồm ba lớp: kích hoạt, xử lý, đưa ra.
2. Chốt duyệt nằm ở đầu lớp thứ ba, trước mọi thứ đi ra ngoài, kể cả trước lời gọi hẹn giờ.
3. Duyệt xong vẫn hẹn giờ, đừng đăng ngay. Hẹn giờ là lớp phanh thứ hai, còn kịp hủy.
4. Không ghi log thì không đo được, không đo được thì không cải thiện được.
5. MCP tự động không có nghĩa là tự do. Buổi 1 mở quyền đọc, buổi 5 mở thêm quyền ghi và quyền gửi ra ngoài. Quyền do bạn cấp, và cấp ít nhất có thể.

Nói câu chuyển: "Sáu mươi lăm phút tới các bạn mở workbook. Vẽ map của mình trước, đừng vội nối công cụ. Nối kênh thì chỉ nối kênh demo hoặc kênh cá nhân, tôi sẽ đi một vòng kiểm. Ai chưa nối được công cụ thật thì làm prototype, vẫn nộp được và vẫn tính đạt. Cái tôi chấm không phải là luồng chạy mượt, mà là luồng có chốt duyệt đúng chỗ và có log để tuần sau đo."

---

CES Global · Creative, Effective, Sustainable
