# OUTLINE BUỔI 4: Nắm xu hướng thị trường, để agent tự chạy ra content

> **Một câu về buổi này:** hết buổi, anh chị có một trợ lý đọc được thị trường đang nói gì (qua tikhub và last30days), tự gợi ý góc content bám xu hướng, và biết cho trợ lý đó tự chạy theo lịch bằng routine, người duyệt trước khi đăng.
>
> **Nối tiếp các buổi trước:** buổi 2 anh chị lập được agent và nối MCP. Buổi 3 dùng agent làm ra ảnh. Buổi 4 cho agent một giác quan mới: nghe ngóng thị trường. Từ chỗ "đăng theo cảm tính" sang "đăng theo cái thị trường đang quan tâm".
>
> **Nguyên tắc:** đau trước, giải pháp sau. Mỗi phần có Lý thuyết ngắn rồi Thao tác có prompt. Đi từ cào một mẻ dữ liệu tay, lên tới một trợ lý tự chạy hàng ngày.

---

## Cách buổi này đi dần

- Phần A: nối và cấu hình tikhub, cào đúng dữ liệu theo ngành nghề của mình
- Phần B: cài last30days, nghe ngóng xu hướng đa nền tảng
- Phần C: ghép hai nguồn thành một bản tin xu hướng
- Phần D: lập trợ lý nắm xu hướng, cho nó tự chạy bằng routine (đỉnh buổi)

---

## Cắt gì, giữ gì (đọc trước, vì buổi này rất nặng)

Buổi này gánh **hai lần cài công cụ** (tikhub và last30days) cộng **một agent** cộng **một routine**. Với lớp không rành máy, nhồi hết vào 150 phút là vỡ. Đề xuất:

**GIỮ, tay học viên gõ thật:**
- Cấu hình tikhub và cào một mẻ xu hướng đúng ngành (đã đăng ký tài khoản ở nhà)
- Prompt ghép hai nguồn ra bản tin xu hướng
- Lập trợ lý nắm xu hướng trong `.claude/agents/`
- Bật một routine chạy thử

**CÂN NHẮC hạ xuống mức xem demo, làm ở nhà:**
- Cài last30days. Đây là **phần cài khó nhất cả khóa**: cần Python 3.12 trở lên, có bước thiết lập lần đầu (đọc cookie trình duyệt, cài yt-dlp). Đề xuất: giảng viên cài sẵn và demo, học viên có hướng dẫn mang về tự cài. Ai cài được tại lớp thì càng tốt.

**CẮT khỏi buổi này (để dành hoặc bỏ):**
- Cào sâu từng đối thủ, phân tích KOL, số liệu quảng cáo. tikhub có rất nhiều loại lệnh, buổi này chỉ đụng nhóm xu hướng và bình luận.

Nếu anh chị thấy tiếc phần nào, nói tôi giữ và cắt phần khác. Bản đề xuất, không phải chốt cứng.

---

## Nhịp 150 phút

| Khối | Nội dung | Phút |
|---|---|---|
| K0 | Mở đầu: đăng theo cảm tính là đang đoán mò | 10 |
| K1 | tikhub: cấu hình MCP, cào đúng xu hướng theo ngành | 30 |
| K2 | last30days: cài và nghe ngóng xu hướng đa nền tảng | 25 |
| Giải lao | | 10 |
| K3 | Ghép tikhub và last30days thành bản tin xu hướng | 25 |
| K4 | Lập trợ lý nắm xu hướng ra gợi ý content (đỉnh buổi) | 30 |
| K5 | Routine: cho trợ lý tự chạy theo lịch, người duyệt cuối | 15 |
| K6 | Chốt và giao bài | 5 |

**Cộng lại:** 10 + 30 + 25 + 10 + 25 + 30 + 15 + 5 = **150 phút**.

---

## K0. Mở đầu: đăng theo cảm tính là đang đoán mò (10 phút)

**Câu hỏi khơi:** "Tuần rồi anh chị đăng bài dựa vào đâu? Vào việc mình nghĩ khách thích, hay vào việc thị trường đang thật sự bàn?"

- Nỗi đau: nội dung tự nghĩ ra trong phòng kín, không biết ngoài kia đang nóng chủ đề gì, hashtag nào đang lên, đối thủ đang ăn với dạng bài nào.
- Đặt đích: hôm nay cho trợ lý một cái tai. Nó nghe thị trường, chỉ cho anh chị nên nói về cái gì tuần này, rồi tự làm việc đó mỗi sáng.
- Chưa định nghĩa công cụ, chỉ khơi nhu cầu.

---

## K1. tikhub: cấu hình MCP, cào đúng xu hướng theo ngành (30 phút)

### Lý thuyết

Buổi 2 anh chị biết MCP là cái thẻ cho Claude với tới công cụ ngoài. tikhub là một thẻ như vậy, chuyên đọc dữ liệu công khai trên TikTok, Instagram, YouTube. Buổi Customer Insight ta dùng nó đọc bình luận để hiểu nỗi đau. Buổi này dùng nó theo hướng khác: **đọc cái đang nóng của cả ngành**, không chỉ của riêng mình.

Nói thẳng hai điều ghi vào vở:
- **Mỗi lượt gọi tính tiền.** Nghĩ kỹ trước khi bấm, đừng gọi loạn.
- **Cào đúng ngành mới có giá trị.** Cào chung chung ra rác. Phải khóa theo từ khóa ngành, hashtag ngành, đối thủ cụ thể.

### Thao tác

- Đăng nhập tài khoản tikhub (đã đăng ký ở nhà tại `user.tikhub.io`), lấy khóa, dán vào cấu hình MCP theo hướng dẫn. Giảng viên chiếu màn hình từng bước.
- Kiểm tra Claude đã thấy tikhub chưa: nhờ nó liệt kê công cụ tikhub đang có.
- Cào một mẻ xu hướng, ba nhóm lệnh chính:
  - **Cái đang hot chung:** danh sách tìm kiếm đang lên, hashtag đang trend (ví dụ nhóm lệnh trending search, hot search, hashtag trends).
  - **Cái hot đúng ngành mình:** tìm theo từ khóa ngành, lấy video và bài đang lên của chủ đề đó (ví dụ general search theo từ khóa, hashtag video list).
  - **Đối thủ đang làm gì:** lấy bài mới và bình luận dưới bài của một đối thủ cụ thể.
- Prompt mẫu (khóa theo ngành, không cào chung chung): "Dùng tikhub, tìm trên TikTok những video đang lên nhiều trong 2 tuần qua về [chủ đề ngành của tôi, ví dụ dưỡng da thảo mộc]. Lưu kết quả thành file `xu-huong-tikhub.md` trong thư mục làm việc. Chỉ giữ tiêu đề, lượt xem, hashtag, đừng lấy tên tài khoản người dùng."

**Điểm dừng bắt buộc:** sau mẻ cào đầu, hỏi cả lớp "ai đã ra file xu hướng". Ai chưa có tikhub thì mở bộ dữ liệu xu hướng mẫu (giảng viên chuẩn bị sẵn trong repo) để vẫn theo kịp.

---

## K2. last30days: cài và nghe ngóng xu hướng đa nền tảng (25 phút)

### Lý thuyết

tikhub mạnh ở TikTok, Instagram. Nhưng xu hướng còn nằm ở Reddit, YouTube, tin tức, diễn đàn. **last30days** là một công cụ chuyên trả lời một câu: "30 ngày qua người ta nói gì về [chủ đề]". Nó gom bài và lượt tương tác từ nhiều nền tảng rồi tóm lại thành cái đang nóng, ai đang khen, ai đang chê.

Nói thẳng với lớp: **đây là phần cài khó nhất khóa.** Nó cần Python 3.12 trở lên trên máy, và lần chạy đầu có bước thiết lập tự động (cài công cụ đọc YouTube, đọc cookie trình duyệt). Nên:
- Giảng viên cài sẵn trên máy mình, demo cho lớp thấy nó chạy ra gì.
- Ai máy có sẵn Python thì cài theo tại lớp. Ai chưa, có hướng dẫn mang về.
- Không cài được vẫn học trọn buổi: xem demo, và dùng file xu hướng mẫu ở K3.

### Thao tác

- Cài last30days. Đường chuẩn cho lớp dùng Claude Desktop tab Code: thêm bộ cài qua marketplace (`mvanhorn/last30days-skill`). Giảng viên demo bước này.
- Kiểm tra máy có Python 3.12 chưa. Chưa có thì cài bằng một lệnh (Windows: `winget install Python.Python.3.12`).
- Chạy lệnh sức khỏe (doctor) để xem nguồn nào đã nối, nguồn nào chưa.
- Chạy lệnh đầu tiên: hỏi xu hướng đúng ngành mình. Prompt mẫu: "last30days [chủ đề ngành của tôi]". Đọc kết quả: cái gì đang nóng, người ta khen chê điều gì.
- Chỉ cho lớp thấy chế độ nắm xu hướng: hỏi "đang hot gì trong [ngành]" để nó tự gợi ý chủ đề (chế độ discovery/trending).

---

## GIẢI LAO (10 phút)

Bắt buộc, không gộp vào khối khác. Giảng viên dùng 10 phút này gỡ máy nào chưa cào được tikhub hoặc chưa cài được last30days.

---

## K3. Ghép tikhub và last30days thành một bản tin xu hướng (25 phút)

### Lý thuyết

Hai nguồn nhìn hai góc: tikhub thấy cái đang lên trên video ngắn, last30days thấy cái đang bàn trên diễn đàn và tin tức. Ghép lại mới ra bức tranh đủ. Một chủ đề nóng ở cả hai nơi là chủ đề đáng làm content ngay tuần này.

Nhắc nguyên tắc chống bịa: **agent chỉ được nói dựa trên dữ liệu hai nguồn trả về.** Cái nào suy ra thì gắn `[SUY LUẬN]`. Không tự chế con số xu hướng.

### Thao tác

- Prompt ghép, để Claude đọc cả hai file và tổng hợp: "Đọc `xu-huong-tikhub.md` và kết quả last30days về [ngành]. Lập một bản tin xu hướng tuần này cho tôi: 5 chủ đề đang nóng, mỗi chủ đề ghi nóng ở đâu (TikTok hay diễn đàn), vì sao nóng, và một góc content tôi có thể làm. Chủ đề nào chỉ thấy ở một nguồn thì ghi rõ."
- Ra bản tin xu hướng, lưu thành `ban-tin-xu-huong.md`.
- Từ bản tin, chọn 2 chủ đề, nhờ skill viết bài (đã có từ buổi 2) ra 2 bài bám xu hướng.

---

## K4. Lập trợ lý nắm xu hướng ra gợi ý content (30 phút, đỉnh buổi)

### Lý thuyết

Làm tay từng bước như trên thì lâu. Buổi 2 anh chị lập được agent, giờ gói cả quy trình trên thành **một trợ lý nắm xu hướng**. Anh chị chỉ nói "xem tuần này có gì", nó tự gọi tikhub, tự chạy last30days, tự tổng hợp bản tin, tự gợi ý góc content. Giống một bạn chuyên viên market research ngồi sẵn trong máy.

Trợ lý này nằm trong `.claude/agents/` của thư mục làm việc, đúng như agent buổi 2, 3. Nó đọc `CLAUDE.md` để biết ngành, sản phẩm, giọng thương hiệu, nên gợi ý content hợp với mình chứ không chung chung.

### Thao tác

- Lập agent nắm xu hướng, đặt trong `.claude/agents/`, cho quyền gọi tikhub và chạy last30days.
- Trong hướng dẫn agent, viết rõ: đọc CLAUDE.md lấy ngành và giọng; cào tikhub đúng từ khóa ngành; chạy last30days đúng chủ đề; tổng hợp bản tin 5 chủ đề; mỗi chủ đề kèm một góc content; gắn nhãn nguồn, không bịa số.
- Chạy thử: gõ đúng một câu "xem tuần này ngành mình có gì", để trợ lý chạy trọn và trả bản tin.

---

## K5. Routine: cho trợ lý tự chạy theo lịch, người duyệt cuối (15 phút)

### Lý thuyết

Trợ lý đã ngon, nhưng vẫn phải mở máy gõ tay mỗi lần. **Routine** là hẹn giờ cho trợ lý tự chạy: ví dụ 7 giờ sáng mỗi thứ Hai, nó tự làm bản tin xu hướng tuần và để sẵn cho anh chị đọc khi mở máy. Giống hẹn báo thức, nhưng báo thức này làm việc.

Hai điều nói thẳng, ghi vào vở:
- **Người duyệt cuối, luôn luôn.** Routine chỉ tới bước ra bản tin và bản nháp content. **Nó không tự đăng.** Anh chị đọc, sửa, rồi mới đăng tay. Đây là nguyên tắc chống bịa số 3 của cả khóa.
- **Công cụ chạy nền có giới hạn.** tikhub và last30days cần thiết lập trên máy anh chị. Routine chạy tự động có thể không với tới hết các thiết lập đó. Nên bản đầu để routine làm phần chắc chắn chạy được (ví dụ last30days), phần cào tikhub thì kiểm tay. Giảng viên nói rõ chỗ này để lớp không kỳ vọng nó chạy hoàn hảo ngay.

### Thao tác

- Bật một routine: hẹn trợ lý chạy bản tin xu hướng mỗi tuần một lần.
- Chạy thử một lần ngay để thấy nó ra kết quả.
- Nhắc lại: xem xong mới đăng, không để nó tự đăng.

---

## K6. Chốt và giao bài (5 phút)

- Ba thứ mang về: tikhub đã cào được xu hướng đúng ngành, một trợ lý nắm xu hướng trong `.claude/agents/`, một routine chạy thử được.
- Ba nguyên tắc chống bịa nhắc lại, nhấn số 3: người duyệt cuối, agent không tự đăng.
- Bài về nhà: cài last30days ở nhà nếu chưa kịp; để routine chạy một tuần rồi xem nó ra bản tin thế nào; chọn một chủ đề nóng ra một bài đăng thật.
- Mồi buổi sau.

---

## HAI ĐIỀU CẦN ANH CHỊ CHỐT TRƯỚC KHI TÔI VIẾT GIÁO ÁN ĐẦY ĐỦ

1. **Buổi 4 giờ là buổi xu hướng và automation này, vậy hai thứ cũ đi đâu?**
   - **Customer Insight** (đọc review khách tìm nỗi đau, file `buoi-02-customer-insight-agent.md`) và **bản gộp Sales + Content** (`buoi-04-sale-va-content-outline.md`) đang cùng nhắm slot buổi 4. Giờ buổi 4 thành xu hướng + automation thì hai cái kia dồn vào buổi 5, 6 thế nào? Cần biết để không gãy mạch. Đề xuất của tôi: buổi 4 xu hướng + automation này; buổi 5 Customer Insight + Content (nội dung bám cả nỗi đau lẫn xu hướng); buổi 6 Sales + đóng gói. Anh chị thấy sao?

2. **last30days cài tại lớp hay chỉ demo?**
   - (a) Giảng viên demo, học viên xem, mang hướng dẫn về nhà tự cài. An toàn, không vỡ buổi. (Đề xuất)
   - (b) Cả lớp cài tại chỗ. Chỉ nên chọn nếu lớp đa số máy đã có Python và anh chị chấp nhận rủi ro mất thời gian.

Trả lời hai câu này thì tôi viết giáo án đầy đủ `buoi-04-xu-huong-va-automation.md`: dẫn tới đâu prompt từng bước tới đó, kèm hướng dẫn cấu hình tikhub và cài last30days đầy đủ, danh sách lệnh tikhub cào đúng ngành, mẫu agent, và mẫu routine.
