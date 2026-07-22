# Chân dung học viên: AI Agent cho Sale & Marketing

| Mục | Nội dung |
|---|---|
| Khách hàng | Khóa mở của CES Global, bán vé lẻ |
| Đối tượng | Chủ doanh nghiệp SME, trưởng phòng sale và marketing, nhân sự content, ads, CRM, agency và freelancer |
| Số học viên | 20 (dự kiến) |
| Số buổi và thời lượng | 6 buổi x 150 phút, tổng 15 giờ |
| Hình thức | Online live qua Zoom hoặc Meet |
| Ngày khai giảng | 22/07/2026 |
| Giọng | `khoa-mo` |

---

## Cách đọc file này

Khóa này bán vé lẻ và chưa chạy khảo sát đầu vào, nên toàn bộ chân dung dưới đây là **giả định thiết kế**, không phải số liệu. File dùng đúng hai nhãn mà khóa dạy học viên dùng:

| Nhãn | Nghĩa | Ai xử lý |
|---|---|---|
| `[SUY LUẬN]` | Giả định thiết kế, rút từ đối tượng đã công bố và từ ba khóa cùng dạng đã dạy. Dùng tạm để soạn bài | Người soạn bài |
| `[CHỜ DATA THẬT]` | Ô trống, chỉ điền được sau khi thu phiếu khảo sát | Người phụ trách lớp |

Mọi con số phần trăm trong file này đang là `[SUY LUẬN]`. Không được trích chúng ra tài liệu bán khóa, không đưa vào báo cáo, không nói với học viên như thể đã đo.

**Phiếu khảo sát:** `danh-gia/khao-sat-truoc-khoa.md`. Gửi trước buổi 1 ít nhất 5 ngày, nhắc lại sau 3 ngày.

---

## Nguồn dữ liệu

| Nguồn | Chi tiết |
|---|---|
| Phỏng vấn người đặt hàng | Không có. Khóa mở không có một người đặt hàng duy nhất. Vai trò đó do CES Global tự giữ, và mục tiêu khóa là mục tiêu do CES Global đặt ra |
| Khảo sát học viên | `[CHỜ DATA THẬT]` Gửi ngày ..., thu về ... trên ... phiếu, đạt ... phần trăm |
| Độ tin cậy | Hiện tại: không có phiếu nào. Toàn bộ chân dung là giả định thiết kế |

**Ngưỡng tin được:** thu về từ 70 phần trăm phiếu trở lên mới đủ để chốt mức khởi điểm. Dưới ngưỡng đó thì giữ nguyên thiết kế hiện tại và ghi rõ trong báo cáo là chưa đo được.

---

## 1. Bốn nhóm học viên điển hình

Bốn nhóm dưới đây là `[SUY LUẬN]`. Tỉ lệ từng nhóm chỉ điền được sau khảo sát.

### Nhóm 1: Chủ doanh nghiệp SME

| Mục | Nội dung |
|---|---|
| Đang làm gì | Vừa chốt đơn vừa duyệt bài vừa lo dòng tiền. Đội marketing 1 tới 3 người, hoặc thuê ngoài theo tháng. Tự viết bài khi bí người |
| Trình độ AI | Đã gõ ChatGPT hoặc Gemini ở tab chat, chủ yếu để soạn nhanh bài đăng và tin nhắn trả lời khách. Chưa ai dùng Claude Code |
| Nỗi đau chính | Nội dung ra đều nhưng không ai chịu trách nhiệm về chất lượng. Người mới vào phải giải thích lại thương hiệu từ đầu. Không có chỗ để chuẩn hóa cách làm |
| Kỳ vọng ở khóa | Một hệ thống bàn giao được cho nhân viên, để họ nghỉ một tuần mà đội vẫn ra bài đúng giọng |
| Rủi ro bỏ giữa chừng | Bận việc gấp, vắng một buổi rồi hụt nguyên liệu buổi sau. Đây là nhóm hay vắng nhất vì lịch của họ không do họ quyết |
| Cách giữ | Nhắn riêng trước mỗi buổi kèm danh sách file cần mang. Vắng thì gửi bản ghi và bộ Thảo An để chạy lại trong 30 phút |

### Nhóm 2: Trưởng phòng sale hoặc marketing

| Mục | Nội dung |
|---|---|
| Đang làm gì | Quản 3 tới 10 người, duyệt bài, duyệt email chào khách, làm báo cáo tuần cho sếp. Đang có sẵn lead và có sẵn CRM hoặc file Excel thay CRM |
| Trình độ AI | Đã dùng AI vài lần mỗi tuần. Có người đã thử viết prompt dài, chưa biết cách lưu lại để dùng lần sau |
| Nỗi đau chính | Mỗi người trong đội hỏi AI một kiểu, lưu một nơi, đầu ra không so được với nhau. Lead có sẵn mà vẫn phân loại bằng cảm tính |
| Kỳ vọng ở khóa | Một chuẩn đầu ra cho cả đội, và một cách chấm lead không phụ thuộc trí nhớ của người cũ |
| Rủi ro bỏ giữa chừng | Không mang được dữ liệu thật tới lớp vì công ty chưa duyệt. Học ba buổi trên case giả rồi thấy xa việc của mình |
| Cách giữ | Nói rõ ngay buổi 1 là dữ liệu che thông tin nhạy cảm vẫn dùng được. Cho phép thay tên khách, giữ nguyên nội dung trao đổi |

### Nhóm 3: Nhân sự thực thi (content, ads, CRM, sale)

| Mục | Nội dung |
|---|---|
| Đang làm gì | Ra bài hằng ngày, chạy quảng cáo, trực inbox, gọi khách. Việc lặp lại nhiều, deadline dày |
| Trình độ AI | Nhóm dùng AI nhiều nhất trong lớp, gần như mỗi ngày, nhưng chỉ ở tab chat và chỉ cho từng bài lẻ |
| Nỗi đau chính | Viết bài nào cũng phải nhắc lại thương hiệu từ đầu. Bài ra đúng ngữ pháp mà sai giọng, sếp trả lại. Không có chỗ lưu cách làm đã ăn |
| Kỳ vọng ở khóa | Làm nhanh hơn ngay tuần sau, và có bộ prompt của riêng mình để không phải nghĩ lại mỗi sáng |
| Rủi ro bỏ giữa chừng | Tự trả tiền vé và tự trả tiền tài khoản. Thấy buổi 1 nặng phần cài đặt thì nản. Cũng là nhóm dễ nghĩ mình biết rồi rồi lơ là |
| Cách giữ | Buổi 1 phải cho ra kết quả nhìn thấy trong 20 phút đầu. Có bài mở rộng cho người xong sớm ở mọi buổi |

### Nhóm 4: Agency, freelancer, consultant

| Mục | Nội dung |
|---|---|
| Đang làm gì | Chạy cùng lúc nhiều khách, mỗi khách một giọng, một danh sách từ cấm. Bán dịch vụ theo gói |
| Trình độ AI | Quen công cụ, chịu thử cái mới, một số đã nghe tới MCP và automation |
| Nỗi đau chính | Đổi khách là dựng lại từ đầu. Không đóng gói được cách làm thành thứ bán được hoặc giao cho cộng tác viên |
| Kỳ vọng ở khóa | Một bộ khung nhân bản được cho khách mới trong một buổi, và một thứ đem đi demo cho khách |
| Rủi ro bỏ giữa chừng | Đi trước nội dung, thấy buổi 1 và buổi 2 chậm. Hoặc bận job của khách, bỏ buổi giữa |
| Cách giữ | Giao vai chấm chéo ở khối review. Bài mở rộng: nhân bản CLAUDE.md sang khách thứ hai ngay trong buổi |

**Tỉ lệ bốn nhóm:** `[CHỜ DATA THẬT]` điền từ câu 2 của phiếu khảo sát.

---

## 2. Trình độ nền giả định

Toàn bộ mục này là `[SUY LUẬN]`. Sau khảo sát phải thay bằng phân bố thật.

| Mục | Giả định thiết kế | Hệ quả đã đưa vào bài | Câu khảo sát thay số |
|---|---|---|---|
| Mức quen máy tính | Ngồi máy 4 tới 8 giờ mỗi ngày cho việc văn phòng. Tạo được thư mục, tải file, biết File Explorer. Nhiều người chưa quen khái niệm đường dẫn tuyệt đối | `huong-dan-cai-dat.md` chỉ từng bước tạo thư mục và đọc đường dẫn, không giả định người học biết sẵn | Câu 4, câu 10 |
| Đã dùng AI chưa | Phần lớn đã dùng, ở tab chat, mức thử vài lần tới gần như mỗi ngày. Gần như không ai từng dùng Claude Code | Buổi 1 bỏ hẳn phần "AI là gì", vào thẳng bốn tầng ngữ cảnh | Câu 5, câu 6 |
| Có biết dòng lệnh không | Giả định 80 phần trăm chưa từng mở cửa sổ dòng lệnh và không muốn mở | Ràng buộc thiết kế cứng của cả khóa: không có bước nào bắt gõ lệnh. Dùng tab Code trong Claude Desktop, không cài Node.js, không cài Claude Code qua npm | Câu 9 |
| Máy và quyền cài phần mềm | Giả định 30 tới 40 phần trăm dùng máy công ty, trong đó một phần bị chặn cài phần mềm | Hướng dẫn cài đặt có sẵn phương án chống cháy bằng bản web, kèm cảnh báo phần Skill sẽ hạn chế | Câu 10 |
| Có dữ liệu thật không | Giả định một nửa lớp không mang được dữ liệu thật ở buổi 1 và buổi 2 | Case Thảo An chạy xuyên 6 buổi, ai không có dữ liệu vẫn nộp đủ sản phẩm | Câu 11, câu 12 |
| Tài khoản trả phí | Giả định 20 tới 30 phần trăm vào lớp bằng gói miễn phí | Xem `00-tong-quan/tai-khoan-va-chi-phi.md`, mục "Không có tài khoản trả phí thì học thế nào" | Câu 8 |

### Ba nhóm trình độ dùng để chia lớp

Cách xếp nhóm giữ nguyên chuẩn của plugin, chỉ đổi tín hiệu cho hợp khóa này.

| Nhóm | Điều kiện xếp nhóm | Số người | Cách đối xử trong lớp |
|---|---|---|---|
| A. Chưa chạm | Câu 6 chọn "chưa bao giờ" hoặc "thử vài lần", và câu 7 chọn "chưa cài" | `[CHỜ DATA THẬT]` | Gọi riêng trước buổi 1, cài xong tại chỗ trong 20 phút. Trong buổi cho ghép cặp ở phòng breakout. Đạt tối thiểu là ra được CLAUDE.md, chưa cần xong skill |
| B. Đã thử, chưa thành nếp | Câu 6 chọn "thử vài lần" hoặc "vài lần mỗi tháng" | `[CHỜ DATA THẬT]` | Nhóm chính của khóa. Giữ nguyên thiết kế hiện tại |
| C. Đang dùng đều | Câu 6 chọn "gần như mỗi ngày", hoặc câu 5 chọn từ 3 công cụ trở lên | `[CHỜ DATA THẬT]` | Mỗi buổi có một bài mở rộng, xem mục 5 của `ma-tran-muc-tieu.md`. Giao vai chấm chéo ở khối review |

**Mức khởi điểm đang chọn:** giả định nhóm B đông nhất. Buổi 1 vào thẳng bốn tầng ngữ cảnh, không giới thiệu công cụ AI là gì, nhưng vẫn giữ 15 phút đầu để kiểm tra cài đặt.

**Lý do:** `[SUY LUẬN]`, chưa có số liệu. Sau khảo sát phải viết lại mục này bằng số thật, theo bảng chọn mức khởi điểm trong `bg-brief`.

---

## 3. Bảng điều kiện cần trước khi vào lớp

Gửi bảng này kèm phiếu khảo sát. Ai thiếu dòng nào có chữ "Bắt buộc" thì phải xử lý xong trước buổi 1, không xử lý trong buổi.

| # | Điều kiện | Bắt buộc | Cần cho buổi | Kiểm bằng cách nào | Thiếu thì sao |
|---|---|---|---|---|---|
| 1 | Máy Windows 11 hoặc Windows 10, còn trống khoảng 2 GB | Bắt buộc | 1 tới 6 | Học viên tự kiểm | Mượn máy, hoặc ghép cặp trong phòng breakout |
| 2 | Quyền tự cài phần mềm trên máy đó | Bắt buộc | 1 | Tải thử một file cài rồi bấm chạy | Xin bộ phận công nghệ thông tin trước ít nhất 2 ngày. Không kịp thì mang máy cá nhân |
| 3 | Tài khoản Claude gói Pro trở lên, đã thanh toán xong | Bắt buộc | 1 tới 6 | Đăng nhập được vào Claude Desktop và thấy đủ 3 tab | Xem phương án ở `tai-khoan-va-chi-phi.md`. Gói miễn phí hết lượt giữa buổi |
| 4 | Claude Desktop đã cài, bấm thấy tab Code | Bắt buộc | 1 tới 6 | Mở app, nhìn hàng tab trên cùng | Cài lại bản mới ở claude.ai/download. Vẫn không được thì báo trước buổi |
| 5 | Thư mục làm việc đã tạo, Claude Code mở được | Bắt buộc | 1 tới 6 | Gõ một câu hỏi, Claude nhắc lại đúng đường dẫn | Làm lại theo phần C và D của `huong-dan-cai-dat.md` |
| 6 | Git for Windows | Nên có | 1 | Bấm phím Windows, gõ `git bash`, thấy app hiện ra | Không có vẫn học được, Claude Code chạy bằng PowerShell. Báo giảng viên trước buổi |
| 7 | Tài khoản Google | Bắt buộc | 1 và 5 | Đăng nhập được Google Drive | Lập mới, mất 5 phút |
| 8 | Mạng ổn định, tai nghe có micro | Bắt buộc | 1 tới 6 | Tự thử một cuộc gọi video | Lớp online, mất tiếng là mất buổi |
| 9 | Tài khoản tikhub đã nạp phí | Nên có | 2 và 4 | Gọi thử một lượt trước buổi | Bỏ đúng bước lấy dữ liệu thật, dùng bộ Thảo An, vẫn nộp đủ sản phẩm |
| 10 | Tài khoản aitoearn đã nối một kênh demo | Nên có | 4 và 5 | Kênh hiện trong danh sách đã nối | Làm prototype thay vì đăng thật, vẫn tính đạt |
| 11 | Hồ sơ sản phẩm hoặc dịch vụ thật | Nên có | 1 tới 6 | Có file ghi tên sản phẩm, giá, thành phần hoặc tính năng, điều không được nói | Dùng case Thảo An trọn khóa |
| 12 | Dữ liệu khách hàng nguyên văn, tối thiểu 20 mẩu | Nên có | 2 | Đếm số mẩu, mỗi mẩu đã đánh ID | Dùng bộ 15 review và 15 tin nhắn của Thảo An |
| 13 | Danh sách 10 lead và chính sách giá | Nên có | 3 | Đủ 6 cột theo bảng ở giáo án buổi 3 | Dùng bộ lead sỉ và chính sách giá của Thảo An |
| 14 | Một kênh mạng xã hội demo hoặc cá nhân | Nên có | 5 | Đăng thử được một bài | Làm prototype. **Tuyệt đối không nối kênh công ty đang chạy thật** |

---

## 4. Việc tốn thời gian nhất, xếp hạng

Bảng này là nguyên liệu để `bg-outline` chia buổi. Hiện đang xếp theo giả định, phải xếp lại bằng câu 4 và câu 13 của phiếu khảo sát.

| Hạng | Việc | Số người chọn | Buổi nhận việc này | Trạng thái |
|---|---|---|---|---|
| 1 | Viết nội dung bán hàng đều tay, đúng giọng thương hiệu | `[CHỜ DATA THẬT]` | 1 và 4 | `[SUY LUẬN]` |
| 2 | Đọc phản hồi khách để biết viết gì cho trúng | `[CHỜ DATA THẬT]` | 2 | `[SUY LUẬN]` |
| 3 | Phân loại lead và soạn email, tin nhắn tiếp cận | `[CHỜ DATA THẬT]` | 3 | `[SUY LUẬN]` |
| 4 | Lên lịch nội dung và đăng bài nhiều kênh | `[CHỜ DATA THẬT]` | 4 và 5 | `[SUY LUẬN]` |
| 5 | Gom số liệu và làm báo cáo tuần | `[CHỜ DATA THẬT]` | 5, phần bảng quản lý | `[SUY LUẬN]` |
| 6 | Bàn giao cách làm cho người mới hoặc cho khách | `[CHỜ DATA THẬT]` | 6 | `[SUY LUẬN]` |

Việc đã cân nhắc và loại khỏi khóa, kèm lý do: xem mục 7 của `ma-tran-muc-tieu.md`.

---

## 5. Đối chiếu kỳ vọng

Khóa mở không có người đặt hàng riêng, nên chỗ lệch không nằm giữa sếp và nhân viên, mà nằm giữa **điều CES Global hứa khi bán vé** và **điều học viên tưởng mình sẽ nhận**.

| CES Global hứa | Học viên có thể đang tưởng | Xử lý |
|---|---|---|
| Dựng được agent chạy trên dữ liệu của chính mình | Được phát sẵn một bộ agent dùng ngay, không phải tự dựng | Nói rõ ngay email mời và 5 phút đầu buổi 1: đây là khóa tự tay dựng, không phải khóa nhận bộ mẫu |
| Không cần biết code | Sẽ không phải cài gì cả | `huong-dan-cai-dat.md` gửi trước, nói rõ 20 phút cài đặt ở nhà |
| Học trên dữ liệu của chính mình | Không mang gì tới cũng vẫn ra sản phẩm của công ty mình | Nói rõ: không mang dữ liệu thì sản phẩm ra là của Thảo An, vẫn đủ để nộp nhưng không dùng được ngay cho công ty |
| Đăng bài đa kênh ở buổi 5 | Được đăng lên fanpage công ty ngay trong buổi | Nói rõ từ buổi 4: chỉ nối kênh demo hoặc kênh cá nhân |

**Kết luận:** `[CHỜ DATA THẬT]` đối chiếu câu 14 của phiếu với bảng trên. Từ 50 phần trăm học viên nêu việc nằm ngoài 6 buổi là lệch, phải xử lý trước khai giảng.

---

## 6. Ràng buộc hạ tầng và bảo mật

| Mục | Tình hình | Việc phải làm trước buổi 1 |
|---|---|---|
| Đường truyền | Lớp online live. Rủi ro nằm ở phía học viên, không kiểm soát được | Gửi trước một cuộc gọi thử 10 phút cho ai muốn kiểm tra. Ghi hình mọi buổi để người rớt mạng xem lại |
| Máy học viên | `[CHỜ DATA THẬT]` từ câu 10 | Ai chọn "máy công ty bị chặn cài" thì gọi riêng, gửi hai đường dẫn claude.ai/download và git-scm.com để xin quyền |
| Chia sẻ màn hình | Cần cho khối review và khối demo chéo buổi 6 | Nhắc học viên đóng hết cửa sổ có dữ liệu công ty trước khi chia sẻ màn hình |
| Ai trả tiền tài khoản | Khóa mở: **học viên tự trả toàn bộ** | Gửi `tai-khoan-va-chi-phi.md` cùng email xác nhận vé, không đợi tới buổi 1 |
| Dữ liệu không được đưa lên công cụ ngoài | Mỗi học viên một công ty, mỗi nơi một quy định. Khóa không thể biết trước | Bắt buộc: buổi 1 dành thời gian cho ba nguyên tắc chống bịa và quy tắc dữ liệu. Học viên tự chịu trách nhiệm về dữ liệu mình đưa lên |
| Dữ liệu cá nhân trong bộ review | Buổi 2 làm trên review và tin nhắn khách | Bắt buộc bỏ tên thật, số điện thoại, địa chỉ, ảnh đại diện trước khi nạp cho agent. Giữ nguyên văn câu nói |

---

## 7. Mục tiêu khóa

Năm mục tiêu cho cả khóa. `bg-outline` đọc mục này để dựng ma trận, đừng ghi nơi khác.

| # | Mục tiêu | Động từ | Bậc Bloom |
|---|---|---|---|
| 1 | Viết được bộ ngữ cảnh thương hiệu trong `CLAUDE.md` đủ 9 mục, trong đó giọng văn mô tả bằng hành vi (xưng hô, độ dài câu, số emoji tối đa) chứ không bằng tính từ, để Claude trả lời đúng thương hiệu mà không phải dán lại brief | viết | Vận dụng |
| 2 | Dựng được tối thiểu 5 agent dạng skill (viết bài bán hàng, customer insight, chấm điểm lead, proposal, content engine), mỗi skill chạy lại được trên dữ liệu mới mà vẫn ra đúng định dạng đã khai | dựng | Sáng tạo |
| 3 | Rút được insight khách hàng có trích dẫn nguyên văn kèm mã nguồn, rồi chuyển thành lịch nội dung 14 ngày mà mỗi bài nối được về một bước trong hành trình mua | rút, chuyển | Vận dụng |
| 4 | Chẩn đoán được khi agent bịa (bịa số, bịa trích dẫn, bịa chính sách giá) và sửa được ràng buộc trong `CLAUDE.md` hoặc trong skill để chặn lần sau | chẩn đoán, sửa | Phân tích |
| 5 | Đóng gói được toàn bộ thành một Skill và một Playbook mà một đồng nghiệp chưa học khóa cầm lên vẫn ra được kết quả tương đương | đóng gói | Sáng tạo |

**Phép đếm:** 5 mục từ Vận dụng trở lên trên tổng 5 mục, bằng 100 phần trăm. Ngưỡng 70 phần trăm: đạt.

---

## 8. Cảnh báo

Bốn dấu hiệu nguy hiểm theo `bg-brief`. Chưa đo được vì chưa có phiếu. Ngưỡng và cách xử lý ghi sẵn để người phụ trách lớp chạy ngay khi thu phiếu.

| Dấu hiệu | Ngưỡng chạm | Đo bằng câu nào | Đề xuất xử lý | Trạng thái |
|---|---|---|---|---|
| Học viên đã biết hết | Câu 6 chọn "gần như mỗi ngày" từ 40 phần trăm trở lên | Câu 5, câu 6 | Nâng buổi 1: rút phần bốn tầng xuống 20 phút, dồn thời gian cho phần MCP và phần chống bịa. Không tách lớp vì khóa mở đã bán vé | `[CHỜ DATA THẬT]` |
| Chưa đủ nền để theo | Câu 9 chọn "chưa nghe bao giờ" cộng câu 7 chọn "chưa cài" từ 30 phần trăm trở lên | Câu 7, câu 9, câu 10 | Mở một buổi kèm 45 phút trước khai giảng, chỉ để cài đặt và tạo thư mục làm việc. Không mở thì nhóm này rớt ngay buổi 1, vì buổi 1 đã tính là máy đã sẵn sàng | `[CHỜ DATA THẬT]` |
| Lệch kỳ vọng | Từ 50 phần trăm câu 14 nêu việc nằm ngoài 6 buổi | Câu 14 | Dựng bảng hai cột theo mục 5, gửi lại học viên trước khai giảng, nói rõ khóa có gì và không có gì. Không tự đổi nội dung khóa | `[CHỜ DATA THẬT]` |
| Học viên bị ép đi học | Câu 14 bỏ trống từ 30 phần trăm trở lên | Câu 14 | Ít gặp ở khóa mở vì học viên tự mua vé. Gặp thì thường là công ty mua vé cho nhân viên: nhắn riêng hỏi lý do, và buổi 1 phải cho ra kết quả nhìn thấy trong 20 phút đầu | `[CHỜ DATA THẬT]` |

**Dấu hiệu thứ năm, riêng của khóa mở:** trên 30 phần trăm chọn câu 8 là "đang dùng miễn phí, chưa định nâng". Đây là rủi ro lớn nhất của khóa này vì mọi buổi đều cần tài khoản trả phí. Gặp thì nhắn riêng từng người trước buổi 1, kèm bảng chi phí và phương án ghép cặp.

---

## 9. Việc phải làm khi thu xong phiếu

Chạy đúng thứ tự này, mất khoảng 90 phút:

1. Đếm phiếu. Dưới 70 phần trăm thì nhắc lại một lần nữa, chờ thêm 2 ngày.
2. Điền mọi ô `[CHỜ DATA THẬT]` trong file này bằng số thật, đổi nhãn `[SUY LUẬN]` thành `[DATA THẬT]` ở những mục đã có số.
3. Chạy bảng cảnh báo ở mục 8. Có dấu hiệu chạm ngưỡng thì báo người phụ trách khóa trong 24 giờ, kèm số liệu.
4. Xếp lại bảng việc tốn thời gian ở mục 4 theo câu 4 và câu 13. Thứ hạng đổi thì báo, vì nó ảnh hưởng thứ tự buổi.
5. Gọi riêng nhóm A và nhóm chưa có tài khoản trả phí.
6. Gom câu 13 của cả lớp, chọn ba việc được nhắc nhiều nhất, kiểm xem bộ demo Thảo An có phủ đủ ba việc đó không. Không phủ thì bổ sung một file demo.
7. Cập nhật `ma-tran-muc-tieu.md` nếu mức khởi điểm đổi.
