# Sổ tay giảng viên

Đọc file này một lần trước khi dạy buổi đầu tiên. Sau đó mỗi buổi chỉ cần mở `../giao-an/buoi-0X-*.md`.

---

## Trước khóa

### Hai tuần trước
- Gửi học viên bảng yêu cầu chuẩn bị dữ liệu (xem mục "Học viên cần mang gì" bên dưới).
- Hỏi ngành nghề của từng học viên. Ngành có quy định chặt (dược, mỹ phẩm, tài chính, giáo dục) thì chuẩn bị sẵn ví dụ ràng buộc cho họ.

### Một tuần trước
- Đếm số học viên đã gửi được dữ liệu thật. Dưới một nửa thì tăng thời lượng dùng case Thảo An trong demo.
- **Gửi [huong-dan-cai-dat.md](../tai-lieu-hoc-vien/huong-dan-cai-dat.md) cho cả lớp, hạn chót cài xong là trước buổi 1 hai ngày.** Buổi 1 chỉ có 15 phút đầu để cứu người chưa cài, không đủ để cài cho cả lớp.
- Kiểm tra tài khoản Claude của lớp: ai chưa có, ai đang dùng gói miễn phí. Gói miễn phí hết lượt giữa buổi, phải nâng cấp trước.
- Hỏi trước ai dùng máy công ty bị khóa quyền cài phần mềm. Nhóm này cần báo IT sớm, không xử lý được tại lớp.

### Ngay trước buổi 1
- Mở thử tất cả file trong `demo/thao-an/`.
- Mở `demo/thao-an/assets/thao-an-agent-team-diagram.html` bằng trình duyệt, để sẵn tab. Dùng lúc mở đầu buổi 1 để lớp thấy đích đến, và dùng lại ở buổi 6.

---

## Học viên cần mang gì

| Buổi | Dữ liệu cần có | Không có thì |
|---|---|---|
| 1 | Đã cài xong Claude Desktop và Git, có tài khoản trả phí. Hồ sơ sản phẩm: tên, giá, thành phần hoặc tính năng, đối tượng | Dùng `san-pham-thao-an.md`. Chưa cài được thì xử lý ở K0, xem `../tai-lieu-hoc-vien/huong-dan-cai-dat.md` |
| 2 | Review, bình luận, tin nhắn khách. Tối thiểu 20 mẩu, đã đánh ID. Nên có tài khoản tikhub để lấy bình luận thật | Dùng `review-va-tin-nhan-khach.md` |
| 3 | Danh sách lead và chính sách giá | Dùng `danh-sach-lead-si.md` + `chinh-sach-gia-si.md` |
| 4 | Insight và persona từ buổi 2. Nên có tikhub để tra xu hướng, aitoearn để biết giới hạn từng kênh | Lấy kết quả demo của giảng viên |
| 5 | Tài khoản Google hoặc Notion. Tài khoản aitoearn đã nối ít nhất 1 kênh **cá nhân hoặc kênh lập riêng để thử** | Làm prototype trên giấy vẫn tính đạt |
| 6 | Toàn bộ tài sản 5 buổi trước | Không có thì không đóng gói được, phải bù trước buổi 6 |

---

## Khung 150 phút (2,5 giờ), dùng chung mọi buổi

| Khối | Thời lượng | Giảng viên làm gì |
|---|---|---|
| Framework | 20 phút | Nói tư duy và cấu trúc. Không mở Claude trong khối này. |
| Demo thật | 35 phút | Làm trực tiếp trên case Thảo An. Học viên xem, không làm theo. |
| Làm sản phẩm | 65 phút | Học viên tự làm. Giảng viên đi vòng, không giảng thêm. |
| Review nhanh | 10 phút | Gọi 2-3 học viên chiếu màn hình, soát chung. |
| Hoàn thiện và nộp | 20 phút | Học viên chốt sản phẩm. Nộp trước khi ra về. |

Tổng 150 phút. Sáu buổi là 15 giờ học.

**Buổi 6 khác:** khối 10 phút review đổi thành demo chéo, học viên trình bày agent 5 phút cho nhau chấm.

**Nếu lớp học đúng 180 phút:** giãn đều, dồn phần thêm vào khối làm sản phẩm (lên 85 phút) và demo (lên 45 phút). Đừng cắt khối làm sản phẩm xuống dưới 65 phút, vì tự tay xây là phần giá trị nhất.

---

## Ba lỗi vận hành hay gặp

### 1. Khối làm sản phẩm biến thành giảng thêm
Học viên hỏi, giảng viên trả lời cho cả lớp, thế là mất 15 phút làm bài. Cách xử lý: trả lời riêng từng bàn. Câu nào từ 3 người trở lên hỏi thì mới dừng lớp, và dừng đúng 2 phút.

### 2. Học viên chưa xong buổi trước
Buổi 3 mà chưa có persona từ buổi 2 thì làm email cá nhân hóa không nổi. Cách xử lý: đầu mỗi buổi dành 5 phút hỏi ai thiếu gì, cấp ngay bản Thảo An tương ứng để họ không đứng hình.

### 3. Lớp mê công cụ hơn kết quả
Dấu hiệu: học viên hỏi nhiều về công cụ nào tốt hơn công cụ nào. Cách xử lý: kéo về câu hỏi "cái này giúp bạn ra thêm bao nhiêu đơn". Công cụ đặt đúng bước quan trọng hơn công cụ xịn.

---

## Hai rủi ro mới, phải nắm trước khi dạy

### Buổi 5 đăng bài thật được

Từ buổi 5, agent nối được vào kênh mạng xã hội và đăng thật. Nguyên tắc "người duyệt cuối" không còn là lý thuyết.

Ba quy định cứng, nói với lớp ít nhất hai lần:
- Trong buổi học **chỉ nối kênh cá nhân hoặc kênh lập riêng để thử**. Không nối fanpage công ty đang chạy thật.
- Ưu tiên dạy **hẹn giờ đăng** thay vì đăng ngay, vì hẹn giờ thì còn kịp hủy khi phát hiện sai.
- Hướng dẫn gỡ quyền sau buổi học cho ai không dùng tiếp.

Có học viên nài nỉ nối fanpage công ty thì từ chối dứt khoát, không thương lượng. Đề nghị họ làm sau buổi, sau khi xin phép người phụ trách.

### tikhub tính tiền theo lượt gọi

Buổi 2 và 4 dùng tikhub để lấy dữ liệu thật. Mỗi lượt gọi đều tính phí, và học viên tự trả trên tài khoản riêng của họ.

Dặn lớp cách gọi tiết kiệm: lấy một lần rồi **lưu kết quả thành file** trong thư mục làm việc, lần sau đọc lại file thay vì gọi lại. Ai chưa đăng ký thì dùng bộ dữ liệu Thảo An, vẫn hoàn thành đủ bài.

---

## Cách dạy phần chống bịa

Đây là thứ tách khóa này khỏi các khóa mẹo prompt. Đừng dạy nó như một lưu ý cuối buổi.

**Cách hiệu quả nhất: để lớp thấy AI bịa, rồi mới đưa nguyên tắc.**

Mỗi buổi đều có sẵn một tình huống bẫy trong `buoi-0X-*.md` cùng thư mục này. Ví dụ buổi 1 hỏi agent về ngân sách ads mà hồ sơ ghi rõ là chưa có; buổi 3 để lead L07 hỏi độc quyền khu vực mà chính sách chưa quy định. Chạy thật, để lớp thấy agent trả lời trơn tru một điều không có căn cứ, rồi hỏi lớp: "chỗ này lấy đâu ra?"

Sau đó mới đưa ba nguyên tắc:

1. Chỉ dùng dữ liệu bạn cấp.
2. Gắn nhãn nguồn `[DATA THẬT]` và `[SUY LUẬN]`, thiếu thì ghi "chưa đủ dữ liệu".
3. Người duyệt cuối, agent không tự bấm gửi.

Đến buổi 6, chỉ ra rằng ba nguyên tắc này giờ nằm trong Skill, nên chúng đi theo hệ thống chứ không phụ thuộc ai nhớ.

---

## Chấm bài

Dùng `../00-tong-quan/chuan-dau-ra.md` làm bảng đối chiếu. Nguyên tắc chấm:

- **Đủ số lượng chưa phải đạt.** 10 email mà cả 10 giống nhau chỉ khác tên thì chưa đạt.
- **Ưu tiên chấm khả năng dùng lại.** Sản phẩm đẹp nhưng lần sau phải làm lại từ đầu thì giá trị thấp hơn sản phẩm khá mà chạy lại được.
- **Kiểm tra agent có chịu nói "chưa đủ dữ liệu" không.** Đây là phép thử nhanh nhất để biết học viên có hiểu bài hay không.

---

## Xử lý lớp không đồng đều

Lớp thường tách thành ba nhóm sau buổi 2.

| Nhóm | Dấu hiệu | Cách xử lý |
|---|---|---|
| Chạy nhanh | Xong sớm 20-30 phút | Giao thêm: làm agent cho SKU thứ hai, hoặc thử luồng B2B song song B2C |
| Đúng nhịp | Xong sát giờ | Để yên, đừng can thiệp |
| Tụt lại | Kẹt ở bước 2-3 của workbook | Ngồi cùng 5 phút, cấp bản Thảo An làm sẵn để họ đi tiếp thay vì đứng lại |

Đừng kéo cả lớp chờ nhóm tụt lại. Cấp bản làm sẵn để họ bám nhịp là cách nhân văn hơn.

---

## Sau khóa

- Gửi lại toàn bộ repo này cho học viên.
- Nhắc mốc: sau 14 ngày, hẹn một buổi 60 phút để xem kế hoạch triển khai chạy tới đâu.
- Ba câu hỏi để hỏi ở buổi đó: đã dùng agent nào thường xuyên nhất, đã bỏ agent nào và vì sao, có chỉ số nào thay đổi không.
