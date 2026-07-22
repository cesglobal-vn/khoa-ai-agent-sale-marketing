# Ma trận mục tiêu: AI Agent cho Sale & Marketing

| Mục | Nội dung |
|---|---|
| Khách hàng | Khóa mở của CES Global, bán vé lẻ |
| Số buổi | 6 |
| Thời lượng mỗi buổi | 150 phút |
| Nhịp | moc-gio |
| Hình thức | Online live qua Zoom hoặc Meet, cả 6 buổi trực tiếp, không có buổi video tự học |
| Khoảng cách giữa các buổi | Theo lịch lớp. Cách nhau quá 2 tuần thì phải kéo dài khối mở đầu của buổi sau |
| Ngày khai giảng | 22/07/2026 |
| Nguồn | `00-tong-quan/chan-dung-hoc-vien.md`, `00-tong-quan/chuan-dau-ra.md`, 6 file trong `giao-an/` |
| Trạng thái | Chờ duyệt |

File này là xương sống của khóa. `bg-giao-an`, `bg-slide`, `bg-thuc-hanh`, `bg-danh-gia` đọc file này thay vì đoán lại. Sửa file này là sửa cả khóa.

**Lưu ý về nguồn:** khóa đã có sẵn 6 giáo án trước khi có ma trận. Mục tiêu dưới đây rút ngược từ giáo án và từ `chuan-dau-ra.md`, rồi viết lại cho đo được. Chỗ nào mục tiêu trong giáo án không đo được thì ghi rõ ở mục 8, không im lặng sửa.

---

## 1. Bảng ma trận

| Buổi | Nhóm việc | Mục tiêu buổi | Bậc Bloom | Sản phẩm cầm về | Cách đo đạt hay chưa | Hình thức | Phụ thuộc |
|---|---|---|---|---|---|---|---|
| 01 | Đóng gói ngữ cảnh thương hiệu cho Claude | 1.1 Phân biệt được bốn tầng ngữ cảnh (CLAUDE.md, Skill, Memory, MCP) và chỉ đúng nội dung nào đặt vào tầng nào | Hiểu | Thư mục làm việc mở được bằng tab Code; `CLAUDE.md`; Memory đã bật; skill `viet-bai-ban-hang`; 3 bài bán hàng; 10 hook; 10 CTA; 1 kết nối MCP | Giảng viên hỏi "quy trình 8 bước viết bài Facebook đặt vào tầng mấy", học viên trả lời tầng 2 và nêu được lý do. Kiểm chéo bằng file: mở `CLAUDE.md` của học viên, không thấy quy trình chi tiết từng bước nằm trong đó | truc-tiep | |
| 01 | | 1.2 Viết được `CLAUDE.md` đủ 9 mục, câu định vị đủ 4 phần, mục giọng văn mô tả bằng hành vi (xưng hô, độ dài câu tối đa, số emoji tối đa) chứ không bằng tính từ | Vận dụng | | Giảng viên mở file trên màn hình học viên: đếm đủ 9 tiêu đề mục; câu định vị nêu được bán cho ai, giải quyết chuyện gì, khác ở đâu, bằng chứng nào; mục giọng văn không chứa các từ "chuyên nghiệp", "thân thiện", "uy tín", "trẻ trung" | truc-tiep | |
| 01 | | 1.3 Dựng được skill `viet-bai-ban-hang` đặt đúng `.claude/skills/viet-bai-ban-hang/SKILL.md`, có frontmatter `name` và `description`, chạy ra 3 bài bán hàng không dính từ cấm | Vận dụng | | Học viên chạy skill trước mặt giảng viên, ra một bài mới. Bài không chứa từ trong danh sách cấm. Phép thử đổi tên: thay tên thương hiệu bằng tên khác, bài không còn đúng nữa là đạt | truc-tiep | |
| 01 | | 1.4 Cấu hình được Memory và một kết nối MCP để Claude nhớ đúng cách làm việc và đọc được bảng đơn hàng demo trên Google Sheet | Vận dụng | | Hai phép thử tại chỗ: mở một cuộc trò chuyện mới, Claude nêu đúng tên thương hiệu và đủ 4 thông tin cần hỏi trước khi viết bài; và Claude trả lời đúng một con số có trong bảng đơn hàng demo | truc-tiep | |
| 01 | | 1.5 Chẩn đoán được khi Claude bịa số và sửa được `CLAUDE.md` để chặn lần sau | Phân tích | | Chạy prompt hỏi 3 con số hồ sơ ghi rõ là chưa có. Đạt khi cả 3 câu trả về "chưa đủ dữ liệu". Nếu Claude bịa, học viên chỉ ra được đúng chỗ bịa và thêm được dòng ràng buộc vào `CLAUDE.md`, chạy lại ra đúng | truc-tiep | |
| 02 | Rút insight khách hàng thành góc nội dung | 2.1 Dựng được skill `customer-insight` chạy trên tối thiểu 30 mẩu review và tin nhắn, ra bảng insight mà **mọi dòng** đều có mã nguồn và trích dẫn nguyên văn | Vận dụng | `customer-insight` agent; `insight-khach-hang.md`; `CLAUDE.md` đã thay 5 nỗi đau `[SUY LUẬN]` bằng 5 nỗi đau `[DATA THẬT]` có mã trích dẫn; 5 content angle; 5 bài social; 3 brief hình ảnh; 3 visual | Giảng viên đếm: số dòng có mã nguồn phải bằng tổng số dòng. Rồi chọn ngẫu nhiên 2 dòng, mở file gốc dò ngược, thấy đúng nguyên văn. Sai một dòng là chưa đạt | truc-tiep | 01 |
| 02 | | 2.2 Xếp hạng được pain theo tần suất xuất hiện trong data, tách được đâu là dữ liệu thô đâu là insight dùng được | Phân tích | | Bảng có cột tần suất ghi dạng "x trên y mẩu". Giảng viên chọn một dòng, đếm lại tay trong file gốc, con số phải khớp. Bảng không có cột tần suất là chưa đạt | truc-tiep | 01 |
| 02 | | 2.3 Chuyển được insight thành 5 content angle, mỗi angle truy được về tối thiểu 1 trích dẫn | Vận dụng | | Giảng viên chỉ vào một angle bất kỳ, học viên nêu được mã trích dẫn đứng sau nó trong 15 giây | truc-tiep | 01 |
| 02 | | 2.4 Viết được 5 bài social bám angle, 3 brief hình ảnh và 3 visual đúng tỷ lệ kênh | Vận dụng | | Mỗi bài social nêu được nó bám angle số mấy. Brief hình ảnh đủ để người thiết kế làm mà không hỏi lại: có bố cục, chữ trên hình, tông màu, tỷ lệ. Visual mở ra đúng tỷ lệ kênh đã khai | truc-tiep | 01 |
| 02 | | 2.5 Thẩm định được một bảng insight có bịa hay không: bịa trích dẫn, bịa tần suất, bịa persona | Đánh giá | | Giảng viên phát một bảng insight có cài sẵn 1 trích dẫn không tồn tại trong file gốc và 1 con số tần suất sai. Học viên chỉ ra được cả hai trong 3 phút | truc-tiep | 01 |
| 03 | Chấm lead và tiếp cận khách | 3.1 Thiết kế được bộ tiêu chí chấm điểm lead của chính mình, có thang điểm và trọng số, tổng trọng số bằng 100 | Sáng tạo | Sales Research Agent; Lead Scoring Sheet 10 lead; 10 email; 10 tin nhắn; kịch bản gọi 5 phút; 10 kịch bản xử lý từ chối; proposal nháp 3 tới 5 trang | Bảng tiêu chí có tối thiểu 4 tiêu chí, mỗi tiêu chí có thang và trọng số, tổng bằng 100. Giảng viên hỏi "vì sao tiêu chí này nặng hơn tiêu chí kia", học viên trả lời bằng lý do kinh doanh của mình, không phải "thấy hợp lý" | truc-tiep | 01 |
| 03 | | 3.2 Dùng được agent áp bộ tiêu chí đó lên 10 lead thô, ra bảng xếp hạng có cột lý do và cột độ tin cậy | Vận dụng | | Mở bảng: đủ 10 dòng, mỗi dòng có điểm, lý do và độ tin cậy. Lead nào thiếu ghi chú trao đổi phải bị hạ độ tin cậy. Bảng nào cũng "độ tin cậy cao" là dấu hiệu agent đang bịa, chưa đạt | truc-tiep | 01 |
| 03 | | 3.3 Viết được 10 email và 10 tin nhắn cá nhân hóa bằng ghi chú trao đổi thật của từng lead | Vận dụng | | Giảng viên chọn 2 email bất kỳ, tìm được câu lấy từ ghi chú của đúng lead đó. Phép thử đổi tên: thay tên lead khác vào mà email vẫn dùng được thì đó là mẫu điền tên, chưa đạt | truc-tiep | 01, 02 |
| 03 | | 3.4 Dựng được proposal 3 tới 5 trang kèm bảng giá đúng chính sách, và chỉ được chỗ agent phải dừng khi khách hỏi điều chưa có chính sách | Vận dụng | | Chạy ca độc quyền khu vực (lead L07 của bộ Thảo An, hoặc ca tương đương của học viên). Đạt khi proposal để trống mục đó và ghi rõ "cần xin ý kiến", không tự hứa một con số | truc-tiep | 01 |
| 03 | | 3.5 Chuẩn bị được kịch bản gọi 5 phút và 10 kịch bản xử lý từ chối, không câu trả lời nào hứa quá chính sách | Vận dụng | | Kịch bản gọi có đủ mở đầu, câu hỏi thăm dò, chuyển tiếp, kết. Giảng viên đọc 3 trong 10 câu trả lời từ chối, đối chiếu bảng chính sách giá, không câu nào vượt | truc-tiep | 01 |
| 04 | Dựng chiến dịch nội dung 14 ngày | 4.1 Dựng được skill Content Engine nhận một insight và trả ra lịch 14 ngày đúng ràng buộc đã khai, gọi lại được skill `viet-bai-ban-hang` ở bước viết caption | Vận dụng | Content Engine Agent; campaign brief; `lich-14-ngay.md`; 10 bài social; 3 email nurturing; 1 khối landing page; 3 video script; 1 carousel 6 tới 8 slide; 5 brief hình ảnh | Chạy lại skill trên một insight khác, vẫn ra đúng cấu trúc lịch. Kiểm giọng: bài do Content Engine sinh ra vẫn đúng xưng hô và vẫn sạch từ cấm đã khai ở buổi 1 | truc-tiep | 01, 02 |
| 04 | | 4.2 Thiết kế được nhịp 14 ngày có đủ 4 loại ngày (giáo dục, bằng chứng, xử lý phản đối, ưu đãi), mỗi bài nối được về một bước trong hành trình mua | Sáng tạo | | Mở lịch: mỗi ngày có nhãn loại, có đủ cả 4 loại, không có 3 ngày liền cùng một loại. Giảng viên chỉ vào một ngày bất kỳ, học viên nói được bài đó đẩy khách đi bước nào | truc-tiep | 02 |
| 04 | | 4.3 Sản xuất được 10 bài social không trùng ý, mỗi bài có đúng 1 nỗi đau, 1 điểm khác biệt và 1 lời kêu gọi hành động | Vận dụng | | Giảng viên lập bảng 10 dòng, ghi nỗi đau của từng bài. Hai bài trùng nỗi đau và trùng cách nói là chưa đạt, phải viết lại | truc-tiep | 02 |
| 04 | | 4.4 Khai báo được ràng buộc pháp lý và ràng buộc thương hiệu trước khi agent viết chữ đầu tiên, để agent tự chặn | Vận dụng | | Giảng viên yêu cầu học viên nhờ agent viết một câu chứa từ cấm của ngành mình. Đạt khi agent từ chối hoặc thay từ và nói rõ lý do, không phải khi học viên ngồi sửa tay sau | truc-tiep | 01 |
| 04 | | 4.5 Cắt được một bài xuống đúng giới hạn ký tự của kênh mà vẫn giữ đủ nỗi đau, điểm khác biệt và lời kêu gọi | Phân tích | | Đếm ký tự bài đã cắt, đúng dưới giới hạn kênh. Rồi chỉ ra được ba phần đó vẫn còn trong bài. Mất một phần là chưa đạt | truc-tiep | 01 |
| 05 | Nối thành luồng tự chạy và đăng bài | 5.1 Vẽ được automation map của chính mình: liệt kê việc lặp lại, chọn 3 việc đáng tự động, và loại ra việc không nên tự động kèm lý do | Phân tích | `automation-map.md`; bảng quản lý trên Google Sheet, Airtable hoặc Notion; 1 automation chạy được hoặc prototype; mẫu thông báo; checklist kiểm soát rủi ro | Map phải có cả cột "không tự động" kèm lý do. Map chỉ ghi việc được chọn, không ghi việc bị loại, là chưa đạt. Giảng viên hỏi "vì sao việc này không tự động", học viên trả lời bằng một trong ba điều kiện đã học | truc-tiep | 01 |
| 05 | | 5.2 Dựng được bảng quản lý có cột trạng thái và cột người duyệt, agent ghi được vào bảng đó | Vận dụng | | Học viên chạy một lượt, bảng có thêm một dòng mới do agent ghi, dòng đó có trạng thái và có tên người duyệt để trống chờ điền | truc-tiep | 01 |
| 05 | | 5.3 Chạy được tối thiểu 1 luồng tự động từ đầu tới cuối, hoặc dựng được prototype có đủ 5 phần: kích hoạt, xử lý, đầu ra, người duyệt, chỗ ghi log | Vận dụng | | Chạy thử một lượt trước mặt giảng viên, ra kết quả ở đầu bên kia. Prototype cũng tính đạt, nhưng phải chỉ ra được đủ 5 phần trên sơ đồ | truc-tiep | 01 |
| 05 | | 5.4 Chạy trọn luồng post bài: lấy caption từ lịch 14 ngày, soát giới hạn của kênh, chuẩn bị ảnh, dừng lại cho người duyệt, rồi mới hẹn giờ đăng lên kênh demo | Vận dụng | | Nhìn màn hình học viên: bài đã lên lịch trên kênh demo, hoặc bản nháp đã sẵn sàng chờ bấm. Kiểm bắt buộc: có một điểm dừng chờ người duyệt trong luồng. Luồng đăng thẳng không qua người là chưa đạt, dù chạy được | truc-tiep | 04 |
| 05 | | 5.5 Thẩm định được ranh giới ba quyền (đọc, ghi, gửi ra ngoài) và chỉ đúng chỗ bắt buộc có người duyệt trong luồng của chính mình | Đánh giá | | Giảng viên diễn cảnh bỏ bước duyệt. Học viên nêu được hậu quả cụ thể trên luồng của chính mình, không nói chung chung. Checklist rủi ro ghi rõ việc nào tuyệt đối không chạy tự động | truc-tiep | 01 |
| 06 | Đóng gói và bàn giao | 6.1 Nâng được skill của buổi 1 thành một Skill phủ cả bộ việc Sale và Marketing, có vai trò, tiêu chuẩn đầu ra đo được, ranh giới không được vượt, và cách xử lý khi thiếu dữ liệu | Sáng tạo | Claude Skill hoàn chỉnh; AI Agent Playbook; bộ tài sản 5 buổi đã sắp xếp; automation hoặc prototype kèm hướng dẫn chạy; bài demo 5 phút; kế hoạch triển khai 14 ngày | Mở file Skill: có đủ 4 phần trên. Phần tiêu chuẩn đầu ra phải đo được, ví dụ "mỗi bài có đúng 1 nỗi đau và 1 lời kêu gọi", không được viết "viết cho hấp dẫn" | truc-tiep | 01, 02, 03, 04, 05 |
| 06 | | 6.2 Thẩm định được Skill chạy đúng ngoài bối cảnh gốc: nhận một yêu cầu chưa từng làm, vẫn ra kết quả đạt tiêu chuẩn đã khai | Đánh giá | | Giảng viên đưa một đề chưa từng chạy trong khóa. Kết quả đối chiếu đúng bảng tiêu chuẩn đầu ra do chính học viên viết. Cách đo mạnh hơn: đưa Skill cho một học viên khác chạy, kết quả tương đương | truc-tiep | 01 |
| 06 | | 6.3 Viết được AI Agent Playbook có quy trình, tiêu chuẩn đầu ra, ranh giới, và chỉ số đo | Sáng tạo | | Playbook trả lời được 4 câu: làm theo thứ tự nào, đầu ra thế nào là đạt, agent không được làm gì, nhìn vào số nào để biết có tác dụng. Thiếu một câu là chưa đạt | truc-tiep | 01, 02, 03, 04, 05 |
| 06 | | 6.4 Sắp xếp được toàn bộ tài sản 5 buổi vào một cấu trúc thư mục tìm được trong 10 giây | Vận dụng | | Giảng viên đọc tên 3 tài sản bất kỳ trong danh sách chuẩn đầu ra. Học viên mở được cả 3 file, mỗi file dưới 10 giây | truc-tiep | 01, 02, 03, 04, 05 |
| 06 | | 6.5 Trình bày được hệ thống trong 5 phút bằng kết quả chứ không bằng tên công cụ, và nộp kế hoạch triển khai 14 ngày ghi rõ ngày, việc, người làm, kết quả cần thấy | Vận dụng | | Demo chéo có bấm giờ, quá 5 phút là chưa đạt. Bạn cùng nhóm chấm theo rubric: kể được kết quả trước, tên công cụ sau. Kế hoạch 14 ngày có đủ 4 cột, không dòng nào bỏ trống cột người làm | truc-tiep | 01, 02, 03, 04, 05 |

---

## 2. Đếm bậc Bloom toàn khóa

| Bậc | Số mục tiêu | Nằm ở buổi nào |
|---|---|---|
| Nhớ | 0 | |
| Hiểu | 1 | 01 |
| Vận dụng | 18 | 01 (3), 02 (3), 03 (4), 04 (3), 05 (3), 06 (2) |
| Phân tích | 4 | 01 (1), 02 (1), 04 (1), 05 (1) |
| Đánh giá | 3 | 02 (1), 05 (1), 06 (1) |
| Sáng tạo | 4 | 03 (1), 04 (1), 06 (2) |
| **Tổng** | **30** | |

**Phép tính:** số mục từ bậc Vận dụng trở lên là 18 cộng 4 cộng 3 cộng 4 bằng 29. Lấy 29 chia 30 bằng 0,9667, tức **96,7 phần trăm**. Ngưỡng 70 phần trăm: **đạt**.

Mục tiêu bậc Hiểu duy nhất là 1.1, phân biệt bốn tầng ngữ cảnh, nằm ở buổi 1. Giữ nó vì cả 29 mục tiêu còn lại đều dựa vào việc học viên đặt đúng nội dung vào đúng tầng. Đặt nhầm tầng thì skill của buổi 3 và buổi 4 vẫn chạy nhưng ra sai giọng, và không ai biết vì sao. Từ buổi 2 trở đi không còn mục tiêu bậc Nhớ hay Hiểu nào.

**Vì sao tỉ lệ cao tới 96,7 phần trăm:** khóa này ra 40 hơn tài sản trong 6 buổi, mỗi buổi học viên nộp file thật. Mục tiêu bậc Nhớ và Hiểu không có chỗ đứng vì không nộp được thành file. Đây là hệ quả của thiết kế, không phải do viết mục tiêu cho kêu.

---

## 3. Phụ thuộc giữa các buổi

| Buổi | Cần biết trước gì | Lấy từ buổi nào | Nếu học viên vắng buổi đó thì sao |
|---|---|---|---|
| 01 | Máy đã cài xong theo `tai-lieu-hoc-vien/huong-dan-cai-dat.md` | | Vắng buổi 1 là hụt nền của cả 5 buổi sau. Bắt buộc xem bản ghi và chạy lại toàn bộ trước buổi 2, mất khoảng 60 phút |
| 02 | Thư mục làm việc, `CLAUDE.md`, biết dựng skill | 01 | Xem bản ghi buổi 2 và chạy skill `customer-insight` trên bộ Thảo An. Mất khoảng 45 phút. Buổi 3 và buổi 4 đều cần `insight-khach-hang.md` |
| 03 | `CLAUDE.md`, biết dựng skill, bảng insight có trích dẫn | 01, 02 | Buổi 3 là nhánh riêng, không buổi nào sau phụ thuộc bắt buộc vào nó, trừ phần gom tài sản ở buổi 6. Vắng thì chạy lại sau khóa vẫn kịp |
| 04 | `CLAUDE.md`, skill `viet-bai-ban-hang`, `insight-khach-hang.md` | 01, 02 | Buổi 5 cần `lich-14-ngay.md` để chạy luồng post bài. Vắng buổi 4 thì buổi 5 dùng caption mẫu của Thảo An, vẫn chạy được luồng nhưng không phải nội dung của mình |
| 05 | Kết nối MCP của buổi 1, lịch 14 ngày của buổi 4 | 01, 04 | Vắng thì buổi 6 thiếu một trong 6 sản phẩm gom vào Playbook. Chạy lại được sau khóa nếu có kênh demo |
| 06 | Toàn bộ tài sản 5 buổi trước | 01, 02, 03, 04, 05 | Không bù được. Đây là buổi ghép, vắng là mất phần đóng gói và mất phần bàn giao. Chuyển sang lớp sau |

Kiểm: không buổi nào phụ thuộc buổi đứng sau nó. Đạt.

Buổi 3 và buổi 4 không phụ thuộc lẫn nhau, đảo thứ tự được nếu cần. Đang để buổi 3 trước vì nó chỉ cần insight, còn buổi 4 cần thêm thời gian để học viên ngấm phần angle của buổi 2.

**Ràng buộc phải nói với học viên ngay khi bán vé:** sản phẩm buổi trước là đầu vào buổi sau. Nghỉ một buổi là buổi sau hụt nguyên liệu. Khóa này không học rời từng buổi được.

---

## 4. Phân bổ lý thuyết và thực hành

Chỉ tính thời gian **tay học viên đặt lên bàn phím**. Khối demo giảng viên chỉ được tính vào thực hành khi học viên gõ theo cùng lúc. Học viên ngồi xem thì đó là lý thuyết.

Ngưỡng bắt buộc: **60 phần trăm thời lượng học thật**.

### 4.1 Buổi 1, theo bảng mốc đồng hồ đang có trong giáo án

| Khối | Tổng phút | Lý thuyết | Tay trên máy |
|---|---|---|---|
| K0 mở đầu, kiểm tra cài đặt, ra đề bài | 15 | 9 | 6 |
| K1 lý thuyết bốn tầng và demo so sánh (giáo án ghi rõ "không ai gõ máy ở khối này") | 30 | 30 | 0 |
| K2 viết `CLAUDE.md` và bật Memory | 25 | 10 | 15 |
| Giải lao | 10 | không tính | không tính |
| K3 viết skill đầu tiên | 35 | 7 | 28 |
| K4 nối MCP | 25 | 13 | 12 |
| K5 tổng kết và giao bài | 10 | 10 | 0 |
| **Cộng học thật** | **140** | **79** | **61** |

**Tỉ lệ tay trên máy:** 61 chia 140 bằng 43,6 phần trăm. Ngưỡng 60 phần trăm: **chưa đạt**.

### 4.2 Buổi 2 tới buổi 6, theo timeline đang có trong giáo án

Năm buổi này dùng chung một timeline: Framework 20, Demo 35, Học viên làm 65, Review 10, Hoàn thiện và nộp 20.

| Khối | Tổng phút | Lý thuyết | Tay trên máy |
|---|---|---|---|
| 1. Framework | 20 | 20 | 0 |
| 2. Demo giảng viên, học viên ngồi xem | 35 | 35 | 0 |
| 3. Học viên làm sản phẩm | 65 | 0 | 65 |
| 4. Review, 3 người chiếu màn hình | 10 | 10 | 0 |
| 5. Hoàn thiện và nộp | 20 | 0 | 20 |
| **Cộng học thật** | **150** | **65** | **85** |

**Tỉ lệ tay trên máy:** 85 chia 150 bằng 56,7 phần trăm. Ngưỡng 60 phần trăm: **chưa đạt**.

Năm buổi này cũng **không có khối giải lao**, trong khi buổi 1 có 10 phút. Lớp online live ngồi liền 150 phút không nghỉ là quá sức chú ý.

### 4.3 Toàn khóa theo hiện trạng

| Buổi | Học thật | Tay trên máy |
|---|---|---|
| 01 | 140 | 61 |
| 02 tới 06, mỗi buổi 150 và 85 | 750 | 425 |
| **Cộng** | **890** | **486** |

486 chia 890 bằng **54,6 phần trăm**. Ngưỡng 60 phần trăm: **chưa đạt**. Thiếu khoảng 48 phút tay trên máy trên toàn khóa.

### 4.4 Nhịp đề xuất để đạt ngưỡng

Ba thay đổi, không thêm phút nào vào tổng thời lượng, không cắt nội dung nào.

**Thay đổi 1: khối demo đổi sang kiểu làm theo.** Giảng viên gõ chậm, học viên gõ cùng lúc trên máy mình. Trong 35 phút demo của buổi 2 tới buổi 6, tính 25 phút là tay trên máy, 10 phút còn lại là giảng viên nói và chỉ chỗ. Buổi 1 áp dụng cho ba khối demo của K2, K3, K4 (7 cộng 5 cộng 6 bằng 18 phút).

**Thay đổi 2: buổi 1 rút K1 từ 30 xuống 25 phút, dồn 5 phút sang K3.** Cắt phần lý thuyết, giữ nguyên demo so sánh có và không có ngữ cảnh.

**Thay đổi 3: buổi 1 đổi phần viết tay 4 phút của K0 sang gõ thẳng vào một file trong thư mục làm việc.** Vừa được thêm tay trên máy, vừa cho học viên thao tác tạo file lần đầu ngay phút thứ 11.

**Thay đổi 4: buổi 2 tới buổi 6 chèn 10 phút giải lao vào giữa khối 3.** Khối 3 chia thành 30 phút, nghỉ 10 phút, rồi 25 phút.

Bảng sau khi sửa:

| Buổi | Học thật | Lý thuyết | Tay trên máy | Tỉ lệ |
|---|---|---|---|---|
| 01 | 140 | 52 | 88 | 62,9 phần trăm |
| 02 tới 06, mỗi buổi | 140 | 40 | 100 | 71,4 phần trăm |
| **Cộng toàn khóa** | **840** | **252** | **588** | **70,0 phần trăm** |

Ngưỡng 60 phần trăm: **đạt**.

**Điều kiện để giữ được tỉ lệ này:** khối demo phải là demo làm theo. Nếu giảng viên bấm nhanh cho kịp giờ và học viên chỉ ngồi nhìn, toàn bộ 25 phút của mỗi buổi chuyển ngược sang cột lý thuyết và tỉ lệ tụt về mức chưa đạt. `bg-giao-an` phải ghi rõ vào từng khối demo là học viên gõ theo, và ghi rõ điểm dừng chờ cả lớp bắt kịp.

---

## 5. Nhóm nhanh và nhóm chậm

Nhóm nhanh: học viên đã dùng AI gần như mỗi ngày, phần lớn thuộc nhóm agency và nhân sự thực thi. Nhóm chậm: học viên chưa từng dùng, hoặc dùng máy công ty bị chặn cài phần mềm.

| Buổi | Bài mở rộng cho người xong sớm | Cách bắt kịp cho người tụt lại |
|---|---|---|
| 01 | Viết thêm một skill thứ hai cho một việc khác trong ba việc ghi trên bảng, rồi kèm một người nhóm chậm trong phòng breakout | Đạt tối thiểu là có `CLAUDE.md` đủ 9 mục. Skill và MCP chuyển sang bài về nhà, có bản ghi buổi để xem lại |
| 02 | Gọi tikhub lấy bình luận thật từ một video của đối thủ, so bảng insight từ data thật với bảng từ bộ Thảo An | Dùng thẳng bộ 15 review và 15 tin nhắn Thảo An đã đánh ID sẵn, bỏ bước làm sạch data. Mốc 30 phút mà chưa có bảng insight thì kéo về bộ Thảo An ngay |
| 03 | Chấm thêm 10 lead ở một phân khúc khác, so hai bộ trọng số và nêu bộ nào hợp hơn | Dùng bộ 10 lead sỉ Thảo An và chính sách giá có sẵn. Đạt tối thiểu là bảng chấm điểm 10 lead cộng 3 email, không cần đủ 10 email tại lớp |
| 04 | Nhân bản lịch 14 ngày sang kênh thứ hai với giới hạn ký tự khác hẳn, ví dụ từ Facebook sang Threads | Làm lịch 7 ngày thay vì 14, đủ 4 loại ngày là đạt. 10 bài social hạ xuống 5 bài tại lớp, 5 bài còn lại về nhà |
| 05 | Dựng luồng có 2 nhánh xử lý, ví dụ lead nóng đi nhánh gọi ngay, lead nguội đi nhánh nuôi bằng email | Làm prototype trên giấy hoặc trên sơ đồ, không nối công cụ thật. Vẫn tính đạt theo mục tiêu 5.3 |
| 06 | Nhân bản bộ Skill và Playbook sang một thương hiệu thứ hai, đây là bài dành riêng cho nhóm agency | Playbook rút xuống 2 trang, đủ 4 câu trả lời bắt buộc là đạt. Kế hoạch 14 ngày rút xuống 7 ngày |

---

## 6. Buổi tự học qua video

Khóa này **không có buổi tự học qua video**. Cả 6 buổi là online live trực tiếp, không bàn giao gì cho `san-xuat-khoa-hoc`.

Có hai thứ dạng video nhưng không phải buổi học, không tính vào ma trận:

- Video hướng dẫn cài đặt gửi trước buổi 1, nội dung bám `tai-lieu-hoc-vien/huong-dan-cai-dat.md`.
- Bản ghi từng buổi, dành cho người vắng hoặc rớt mạng.

---

## 7. Việc đã loại khỏi khóa

| Việc | Lý do loại | Bù bằng gì |
|---|---|---|
| Chạy và tối ưu quảng cáo trả tiền, đọc số liệu trong trình quản lý quảng cáo | Cần quyền tài khoản quảng cáo và ngân sách thật. Lớp online không dựng được, và một lần chạy sai là mất tiền thật của học viên | Buổi 4 ra bài viết, kịch bản video và brief hình ảnh dùng được cho quảng cáo |
| Dựng chatbot trả lời khách tự động trên fanpage | Cần quyền quản trị fanpage công ty và cần duyệt của nền tảng, mất nhiều ngày. Trái luôn với ràng buộc "không nối kênh công ty đang chạy thật" của buổi 5 | Buổi 5 ra mẫu thông báo và luồng có điểm dừng chờ người duyệt |
| Dựng dashboard và phân tích số liệu bán hàng chuyên sâu | Mỗi học viên một hệ thống, một cách lưu số. Dạy chung thì không ai áp dụng được | Buổi 5 ra bảng quản lý trên Google Sheet có cột trạng thái và cột người duyệt |
| Sản xuất video: quay, dựng, lồng tiếng | Thuộc khóa khác. Nhét vào thì mất một buổi và không ai làm xong | Buổi 4 ra 3 kịch bản video 30 tới 60 giây, đủ để giao cho người dựng |
| Viết code, gọi API bằng tay, tự dựng máy chủ | Ràng buộc cứng của khóa: phần lớn học viên không biết code và không muốn mở dòng lệnh | Buổi 5 dùng MCP và công cụ có giao diện, không gõ lệnh nào |
| Thiết kế hình ảnh chuyên sâu | Không phải nghề của phần lớn học viên trong lớp | Buổi 2 và buổi 4 ra brief hình ảnh đủ để người thiết kế làm mà không hỏi lại |

---

## 8. Đối chiếu với giáo án đã có

Ba chỗ mục tiêu trong giáo án không qua được phép thử "đứng cuối buổi có nhìn được ai đạt ai chưa". Ma trận này đã viết lại, ghi ra đây để giảng viên biết mình đang cầm bản nào.

| Vị trí | Mục tiêu trong giáo án | Vấn đề | Ma trận viết lại thành |
|---|---|---|---|
| Buổi 2, gạch đầu dòng 1 | "Học viên phân biệt được dữ liệu thô với insight, và biết insight nào dùng được để viết nội dung" | "Biết insight nào dùng được" không nhìn được ai đạt | Mục tiêu 2.2, đo bằng cột tần suất trong bảng và bằng phép đếm lại tay của giảng viên |
| Buổi 3, mục tiêu 5 | "Hiểu vì sao chia việc cho 3 agent lại tốt hơn nhồi vào 1 agent" | Bậc Hiểu, không có sản phẩm nào chứng minh | Bỏ khỏi danh sách mục tiêu, chuyển thành một câu hỏi chốt trong khối framework. Nội dung giảng giữ nguyên, không cắt |
| Buổi 5, gạch đầu dòng 5 | "Chỉ đúng ranh giới giữa quyền đọc và hai quyền mới, và chỉ đúng chỗ nào bắt buộc có người duyệt" | Đo được nhưng chưa nói rõ nhìn vào đâu | Mục tiêu 5.5, đo bằng cảnh diễn bỏ bước duyệt cộng checklist rủi ro có ghi việc cấm chạy tự động |

---

## 9. Bảng tổng hợp toàn khóa

| Buổi | Tên buổi | Số mục tiêu | Bậc Bloom cao nhất | Sản phẩm chính cầm về |
|---|---|---|---|---|
| 01 | Cài Claude Code và bốn tầng ngữ cảnh | 5 | Phân tích | Thư mục làm việc có `CLAUDE.md`, Memory đã bật, skill `viet-bai-ban-hang` chạy được, 1 kết nối MCP |
| 02 | Customer Insight Agent | 5 | Đánh giá | `customer-insight` agent và `insight-khach-hang.md` có trích dẫn nguyên văn, 5 content angle |
| 03 | Sales Agent | 5 | Sáng tạo | Sales Research Agent, Lead Scoring Sheet 10 lead, proposal nháp 3 tới 5 trang |
| 04 | Content Engine Agent | 5 | Sáng tạo | Content Engine Agent và `lich-14-ngay.md` đủ 4 loại ngày |
| 05 | Automation và MCP | 5 | Đánh giá | `automation-map.md`, bảng quản lý, luồng post bài chạy được có điểm dừng duyệt |
| 06 | Claude Skill và Playbook | 5 | Sáng tạo | Claude Skill bàn giao được, AI Agent Playbook, kế hoạch triển khai 14 ngày |
| | **Cộng** | **30** | | **Trên 40 tài sản, xem `00-tong-quan/chuan-dau-ra.md`** |

---

## 10. Đối chiếu bốn mức Kirkpatrick

| Mức | Đo gì | Khóa này đo được không | Đo bằng công cụ nào | Trạng thái |
|---|---|---|---|---|
| 1. Phản ứng | Học viên thấy buổi học thế nào | Có | Khảo sát cuối mỗi buổi 5 tới 7 câu, và khảo sát cuối khóa | **Chưa có file.** Cần `danh-gia/khao-sat-cuoi-buoi.md` và `danh-gia/khao-sat-cuoi-khoa.md`, do `bg-danh-gia` dựng |
| 2. Học tập | Học viên có thật sự làm được thêm không | Có, và đây là mức khóa đo mạnh nhất | Chấm đạt hoặc chưa đạt tại chỗ mỗi buổi theo cột "Cách đo" của mục 1, đối chiếu `chuan-dau-ra.md`. Bằng chứng là file học viên nộp, không phải điểm thi. Cộng thêm quiz trước và sau khóa để so điểm | **Một phần.** Chuẩn đầu ra đã có. Quiz và rubric chấm chưa có, cần `bg-danh-gia` |
| 3. Hành vi | Về chỗ làm có áp dụng không | Có, nhưng có điều kiện | Khảo sát sau 30 ngày, bám đúng kế hoạch triển khai 14 ngày mà học viên nộp ở buổi 6: đã chạy mấy việc trong kế hoạch, cái nào chưa chạy và vì sao | **Chưa có file.** Rủi ro: khóa mở, học viên không thuộc một công ty nào nên tỉ lệ trả lời dự kiến dưới 40 phần trăm. Khi báo cáo phải ghi số phiếu thật, không quy ra phần trăm cả lớp |
| 4. Kết quả | Doanh nghiệp được lợi gì | **Không đo được** | Cần số liệu vận hành: số giờ tiết kiệm, số đơn, số lead chuyển đổi. Mỗi học viên một công ty, không ai cam kết cung cấp | Không làm. **Không được hứa mức 4 trong tài liệu bán khóa.** Ai muốn đo mức 4 thì phải mở lớp riêng tại doanh nghiệp và ký cam kết cung cấp số liệu |

Theo luật trong `nguyen-tac-su-pham.md`, khóa đào tạo doanh nghiệp bắt buộc có mức 1 và mức 2. Mức 2 của khóa này đã có xương sống là 40 hơn tài sản chấm được bằng file thật. Việc còn thiếu là bộ công cụ đo mức 1 và bộ quiz mức 2.

---

## 11. Việc còn treo

| # | Việc | Ai làm | Chặn cái gì |
|---|---|---|---|
| 1 | Chốt phương án tăng tỉ lệ tay trên máy ở mục 4.4, rồi sửa timeline trong 6 file giáo án | Người phụ trách khóa duyệt, sau đó `bg-giao-an` sửa | Khóa đang trượt ngưỡng 60 phần trăm ở mọi buổi |
| 2 | Chèn 10 phút giải lao vào buổi 2 tới buổi 6 | `bg-giao-an` | 150 phút online liền không nghỉ |
| 3 | Dựng bộ đo mức 1 và mức 2 Kirkpatrick | `bg-danh-gia` | Không nghiệm thu được, không có số đưa vào báo cáo sau khóa |
| 4 | Điền số thật vào `chan-dung-hoc-vien.md` sau khi thu phiếu khảo sát | Người phụ trách lớp | Mức khởi điểm đang là giả định. Đổi mức khởi điểm thì phải xem lại mục tiêu buổi 1 |
| 5 | Chốt khoảng cách giữa các buổi và ghi vào `khoa.json` | Người phụ trách khóa | Cách nhau quá 2 tuần thì khối mở đầu của mỗi buổi phải dài hơn |
