# OUTLINE BUỔI 3: Agent tạo ảnh, từ caption ra hình đăng được

> **Một câu về buổi này:** hết buổi, anh chị nối được Claude vào công cụ vẽ ảnh của ChatGPT, tự tạo ảnh cho bài đăng, và lập một trợ lý chuyên ra ảnh gắn sẵn logo thương hiệu.
>
> **Nối tiếp buổi 2:** buổi 2 anh chị đã hiểu agent, MCP, và lập được agent. Buổi 3 dùng đúng ba thứ đó vào một việc thật và sướng tay nhất: làm ra hình ảnh để đăng.
>
> **Nguyên tắc:** đau trước, giải pháp sau. Mỗi phần có Lý thuyết ngắn rồi Thao tác có prompt. Đi từ tạo một ảnh lẻ, lên tới một trợ lý tự ra ảnh hàng loạt.

---

## Cách buổi này đi dần

- Phần A: hiểu và nối công cụ vẽ ảnh vào Claude (MCP tạo ảnh)
- Phần B: viết mô tả để ra ảnh đúng ý, đúng sản phẩm
- Phần C: lập một trợ lý chuyên tạo ảnh (đỉnh buổi)
- Phần D: gắn logo thương hiệu, người duyệt, và chi phí

---

## Nhịp 150 phút

| Khối | Nội dung | Phút |
|---|---|---|
| K0 | Mở đầu: một nỗi đau chung | 10 |
| K1 | Nối công cụ vẽ ảnh vào Claude, tạo ảnh đầu tiên | 30 |
| K2 | Viết mô tả để ra ảnh đúng ý | 25 |
| Giải lao | | 10 |
| K3 | Lập một trợ lý chuyên tạo ảnh (đỉnh buổi) | 40 |
| K4 | Gắn logo, người duyệt, chi phí | 25 |
| K5 | Chốt và giao bài | 10 |

---

## K0. Mở đầu: một nỗi đau chung (10 phút)

**Câu hỏi khơi:** "Anh chị viết được bài bán hàng hay rồi, nhưng tới lúc cần một tấm ảnh để đăng thì sao? Chờ thiết kế, hay tự lấy ảnh mạng?"

- Nỗi đau thật: bài hay mà thiếu ảnh, hoặc thuê thiết kế lâu và đắt, hoặc lấy ảnh mạng thì đụng hàng và không đúng sản phẩm.
- Đặt đích: hôm nay Claude tự vẽ ảnh cho anh chị, gắn sẵn logo, ra hình đăng được ngay.
- Chưa định nghĩa gì, chỉ khơi nhu cầu.

---

## K1. Nối công cụ vẽ ảnh vào Claude

### Lý thuyết

Buổi 2 anh chị đã biết MCP là cái thẻ cho Claude với tới công cụ bên ngoài. Hôm nay ta cắm một công cụ cụ thể: **công cụ vẽ ảnh của ChatGPT**. Cắm xong, anh chị bảo Claude "vẽ giúp tôi tấm ảnh này", nó vẽ thật, trả về một file ảnh trên máy.

Một điều nói thẳng ngay: bước **cài và nối công cụ vẽ ảnh là phần khó nhất buổi** cho người không rành máy, vì nó cần đăng nhập tài khoản ChatGPT một lần. Nên phần này giảng viên chuẩn bị kỹ, và có đường dự phòng cho ai chưa nối được (xem giảng viên demo, làm bù sau).

### Thao tác
- Kiểm tra công cụ vẽ ảnh đã nối chưa (giảng viên hướng dẫn nối, hoặc đã nối sẵn cho lớp).
- Tạo ảnh đầu tiên bằng một prompt đơn giản, thấy file ảnh hiện ra.
- Prompt mẫu: tạo một ảnh nền đơn giản cho bài đăng.

---

## K2. Viết mô tả để ra ảnh đúng ý

### Lý thuyết

Ảnh đẹp hay xấu, đúng hay lệch, phần lớn do **cách anh chị tả**. Một mô tả tốt cần nói rõ năm thứ: chủ thể (cái gì trong ảnh), bối cảnh (đặt ở đâu), phong cách (sang, tối giản, tươi), tỉ lệ khung (vuông cho Facebook, dọc cho story), và tông màu.

Một cảnh báo quan trọng, ghi vào vở: **ảnh do AI vẽ hay viết sai chữ tiếng Việt, nhất là chữ có dấu.** Nên dùng ảnh cho phần hình nền và bố cục, còn chữ quan trọng như tên sản phẩm, giá, thì thêm sau bằng Canva. Đừng để AI viết chữ tiếng Việt lên ảnh rồi đăng thẳng.

### Thao tác
- Tạo một ảnh cho sản phẩm thật của anh chị, tả đủ năm thứ trên.
- So một ảnh tả sơ sài với một ảnh tả kỹ, thấy khác biệt.
- Thử đúng tỉ lệ cho từng kênh.

---

## GIẢI LAO (10 phút)

---

## K3. Lập một trợ lý chuyên tạo ảnh (40 phút, đỉnh buổi)

### Lý thuyết

Tả từng ảnh một thì lâu. Buổi 2 anh chị đã lập được agent, giờ ta lập một **trợ lý chuyên tạo ảnh**. Anh chị chỉ đưa nội dung bài đăng, trợ lý tự nghĩ ra mô tả ảnh hợp bài, gọi công cụ vẽ, rồi trả ảnh về. Giống như có một bạn thiết kế đã hiểu gu thương hiệu, chỉ cần đưa brief là ra hình.

Trợ lý này nằm trong `.claude/agents/` của thư mục làm việc, đúng như agent anh chị lập ở buổi 2. Nó đọc `CLAUDE.md` để biết màu và phong cách thương hiệu, nên ảnh ra hợp brand hơn.

### Thao tác
- Lập agent tạo ảnh, đặt trong `.claude/agents/`, có quyền gọi công cụ vẽ ảnh.
- Trong hướng dẫn agent: đọc CLAUDE.md lấy màu và phong cách, tự viết mô tả ảnh từ nội dung bài, chọn đúng tỉ lệ kênh, và không viết chữ tiếng Việt lên ảnh.
- Chạy thử: đưa một caption, để trợ lý ra ảnh.

---

## K4. Gắn logo, người duyệt, chi phí (25 phút)

### Lý thuyết

Ba việc để ảnh dùng được thật:
- **Logo thương hiệu:** ảnh phải có nhận diện. Cách chắc nhất là chừa chỗ trống rồi ghép logo thật vào, thay vì để AI tự vẽ logo (nó vẽ sai).
- **Người duyệt cuối:** ảnh cũng như bài viết, là bản nháp. Anh chị xem rồi mới đăng. Agent không tự đăng.
- **Chi phí:** mỗi lần vẽ ảnh đều tốn quota hoặc tiền. Nên nghĩ kỹ mô tả trước khi bấm, đừng vẽ đi vẽ lại chục lần.

### Thao tác
- Ghép logo vào ảnh vừa tạo.
- Xem lại, chọn ảnh đạt, loại ảnh lỗi.
- Ghi nhớ cách kiểm chi phí còn lại.

---

## K5. Chốt và giao bài (10 phút)

- Ba thứ mang về: công cụ vẽ ảnh đã nối, một trợ lý tạo ảnh trong `.claude/agents/`, vài ảnh có logo đăng được.
- Ba nguyên tắc chống bịa nhắc lại, thêm một điều riêng của buổi: không để AI viết chữ tiếng Việt lên ảnh rồi đăng thẳng.
- Mồi buổi sau.

---

## HAI ĐIỀU CẦN ANH CHỊ CHỐT TRƯỚC KHI TÔI VIẾT GIÁO ÁN ĐẦY ĐỦ

1. **Buổi 3 tối nay đổi thành buổi tạo ảnh này, vậy Customer Insight đi đâu?** Customer Insight đã soạn xong. Nó dời sang buổi 4, hay bỏ, hay ghép một phần vào buổi khác? Cần biết để không gãy mạch các buổi sau.

2. **Học viên nối công cụ vẽ ảnh bằng cách nào?** MCP `ai-image-gpt` cần cài bằng dòng lệnh (git clone, uv, đăng nhập ChatGPT), khá khó cho lớp không biết code. Ba lựa chọn:
   - (a) Giảng viên nối sẵn trên máy mình, học viên xem demo, tự làm ở nhà theo hướng dẫn.
   - (b) Gửi hướng dẫn cài trước buổi, ai cài được thì thực hành, chưa được thì xem.
   - (c) Dùng một công cụ vẽ ảnh dễ nối hơn nếu có, để cả lớp làm được tại chỗ.
