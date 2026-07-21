# Buổi 1 · Hướng dẫn cài đặt trước buổi học

**Làm hướng dẫn này ở nhà, trước buổi học ít nhất 3 ngày. Mất khoảng 20 phút.**

Đừng để tới hôm học mới cài. Lớp chỉ có 15 phút đầu để kiểm tra máy, không đủ để cài lại từ đầu cho cả phòng. Ai chưa cài xong sẽ ngồi nhìn người khác thực hành.

Làm hết 5 phần A đến E là tới lớp mở máy lên chạy được ngay.

---

## Cần chuẩn bị gì

| Mục | Yêu cầu | Ghi chú |
|---|---|---|
| Tài khoản Claude | Gói trả phí, Claude Pro trở lên | Đăng ký tại claude.ai. Gói miễn phí hết lượt giữa chừng, không đủ cho 150 phút thực hành |
| Máy tính | Windows 11 (Windows 10 vẫn chạy được) | Máy cá nhân dễ hơn máy công ty |
| Quyền cài phần mềm | Tự cài được app trên máy | **Nhiều máy công ty khóa quyền này. Kiểm tra sớm, cần thì xin IT trước ít nhất 2 ngày** |
| Mạng | Wifi hoặc mạng dây ổn định | Claude chạy trên mạng, mất mạng là dừng |
| Ổ đĩa trống | Khoảng 2 GB | Claude Desktop và Git cộng lại chưa tới 1 GB |

**Cách kiểm tra nhanh quyền cài phần mềm:** tải thử một file cài bất kỳ rồi bấm chạy. Nếu hiện bảng đỏ kiểu "Your administrator has blocked this program", hoặc bắt nhập mật khẩu quản trị mà bạn không có, thì máy đang bị khóa. Nhắn IT ngay, đừng chờ tới hôm học.

**Hai điều nhiều người hiểu nhầm, nói rõ luôn:**

- **KHÔNG cần cài Node.js.**
- **KHÔNG cần cài Claude Code riêng bằng lệnh npm.** Claude Code nằm sẵn trong Claude Desktop, ở tab tên là **Code**.

---

## Cài ba thứ, mỗi thứ để làm gì

Biết mình đang cài cái gì thì đỡ hoang mang lúc gặp lỗi.

| Cài gì | Để làm gì | Bắt buộc không |
|---|---|---|
| Claude Desktop | App chính. Tab **Code** bên trong nó là thứ cả khóa dùng để đọc và tạo file trên máy bạn | Bắt buộc |
| Git for Windows | Bộ công cụ nền, giúp mọi máy trong lớp chạy giống nhau | Nên có. Thiếu vẫn học được, xem giải thích ở phần B |
| Thư mục làm việc | "Bàn làm việc" của bạn suốt 6 buổi. Mọi file bạn làm ra nằm ở đây | Bắt buộc |

---

## Phần A · Cài Claude Desktop (khoảng 7 phút)

1. Mở trình duyệt (Chrome, Edge, trình duyệt nào cũng được).
2. Gõ vào ô địa chỉ: `https://claude.ai/download` rồi Enter.
3. Trang hiện nút tải cho Windows. Bấm nút đó.
4. File cài tải về thư mục **Downloads**, tên bắt đầu bằng `Claude`. Bấm đúp chuột vào file.
5. Windows có thể hiện bảng xanh "Windows protected your PC". Bấm dòng chữ nhỏ **More info**, rồi bấm nút **Run anyway**. Đây là cảnh báo mặc định của Windows với mọi phần mềm mới tải, không phải lỗi.
6. Chờ cài xong. App tự mở.
7. Bấm nút đăng nhập, đăng nhập bằng tài khoản Claude **trả phí** của bạn.

**Dấu hiệu đúng:** cửa sổ Claude mở ra, phía trên cùng có 3 tab: **Chat**, **Cowork**, **Code**. Thấy đủ 3 tab là xong phần A.

---

## Phần B · Cài Git for Windows (khoảng 5 phút)

Nói thật trước cho khỏi hoang mang: **Git không bắt buộc tuyệt đối.** Không có Git thì Claude Code trên Windows vẫn chạy được bằng PowerShell. Nhưng cả lớp cài Git để mọi máy giống nhau, giảng viên hướng dẫn một đường đúng cho tất cả, không phải rẽ nhánh giữa buổi.

1. Mở trình duyệt, gõ `https://git-scm.com` rồi Enter.
2. Trang chủ có nút tải cho Windows. Bấm vào.
3. Chọn bản **64-bit Git for Windows Setup** (bản Standalone Installer). File tải về tên kiểu `Git-2.xx.x-64-bit.exe`.
4. Bấm đúp chuột vào file để chạy.
5. **Trong lúc cài, cứ bấm Next cho tới hết, để nguyên mọi lựa chọn mặc định.** Có khoảng 10 màn hình hỏi lựa chọn. Bạn không cần hiểu từng cái. Mặc định là đúng cho lớp này.
6. Tới màn hình cuối bấm **Install**, chờ khoảng 1 phút, rồi bấm **Finish**. Bỏ tick ô "View Release Notes" nếu có.

**Dấu hiệu đúng:** bấm phím Windows, gõ `git bash`, thấy app **Git Bash** hiện ra trong danh sách. Không cần mở nó, chỉ cần thấy là được.

---

## Phần C · Tạo thư mục làm việc cho khóa học (khoảng 3 phút)

Thư mục này là "bàn làm việc" của bạn suốt 6 buổi. Mọi file bạn làm ra sẽ nằm ở đây.

1. Bấm phím **Windows + E** để mở File Explorer (cửa sổ quản lý file, biểu tượng thư mục vàng).
2. Khung bên trái, bấm **This PC**, rồi bấm ổ **Windows (C:)**.
3. Mở thư mục **Users**, rồi mở thư mục mang tên đăng nhập của bạn.
4. Bấm chuột phải vào khoảng trống bên phải, chọn **New**, rồi chọn **Folder**.
5. Gõ tên: `thao-an-workspace` rồi Enter. Gõ đúng chữ thường, không dấu, không khoảng trắng.

**Đường dẫn đầy đủ của bạn giờ là:** `C:\Users\<tên đăng nhập>\thao-an-workspace`

**Không biết tên đăng nhập Windows của mình?** Mở File Explorer, bấm vào ô địa chỉ ở trên cùng, xóa hết rồi gõ `%USERPROFILE%` và Enter. Cửa sổ nhảy thẳng vào thư mục của bạn, ô địa chỉ hiện tên. Tạo thư mục mới ngay tại đó.

**Ghi đường dẫn này ra giấy hoặc note điện thoại.** Buổi học dùng lại nhiều lần.

---

## Phần D · Mở Claude Code trong thư mục đó (khoảng 5 phút)

1. Mở **Claude Desktop**.
2. Bấm tab **Code** ở trên cùng.
3. Lần đầu vào, app hỏi bạn chọn thư mục làm việc. Bấm nút chọn thư mục (nút ghi **Open folder** hoặc **Add folder**), trỏ tới `C:\Users\<tên bạn>\thao-an-workspace`, bấm **Select Folder**.
4. Ô nhập lệnh hiện ra ở dưới cùng. Gõ câu này rồi Enter:

```
Cho tôi biết bạn đang làm việc trong thư mục nào.
```

**Dấu hiệu đúng:** Claude trả lời và nhắc lại đúng đường dẫn thư mục bạn vừa chọn.

5. Thử tiếp một câu tạo file. Gõ:

```
Tạo giúp tôi file ghi-chu.md trong thư mục này, nội dung một dòng:
Máy đã sẵn sàng cho buổi 1.
```

6. Claude sẽ **hỏi xin phép** trước khi ghi file. Bấm đồng ý (**Yes** hoặc **Allow**). Đây là hành vi bình thường, Claude không tự ý sửa file trên máy bạn.
7. Mở File Explorer vào lại thư mục. Thấy file `ghi-chu.md` là máy chạy đúng.

---

## Lần sau mở lại thế nào

Không phải cài lại gì. Mỗi lần muốn làm bài:

1. Mở **Claude Desktop**.
2. Bấm tab **Code**.
3. Kiểm tra góc màn hình đang hiện đúng thư mục `thao-an-workspace`. Sai thư mục thì bấm nút chọn thư mục, trỏ lại cho đúng.
4. Gõ vào ô nhập và làm việc.

**Sai thư mục là lỗi phổ biến nhất trong lớp.** Claude làm việc rất đúng, nhưng đúng ở nhầm chỗ, và bạn không tìm thấy file mình vừa tạo.

---

## Nên mang thêm gì tới lớp (không bắt buộc)

Bạn có sản phẩm hoặc dịch vụ thật thì mang dữ liệu đi, buổi học sẽ ra sản phẩm dùng được ngay cho công ty bạn. Gom vào một file Word hoặc một file text:

- Tên thương hiệu, ngành, sản phẩm chính (tối đa 5 mục) và giá từng mục
- Thành phần hoặc tính năng chính, công dụng hoặc lợi ích đang công bố
- Khách hàng chính: tuổi, giới, nghề, mức chi
- Kênh đang bán
- Điều không được nói trong ngành bạn: từ cấm, cam kết cấm
- 2 tới 3 bài viết cũ của thương hiệu

Chưa có gì cũng không sao. Lớp có sẵn bộ dữ liệu Thảo An, làm đủ mọi bài tập.

---

## Tài khoản cần cho các buổi sau

Buổi 1 chỉ cần Claude và Git. Nhưng có hai tài khoản nên đăng ký sớm, vì tới buổi mới làm thì không kịp.

| Tài khoản | Dùng ở buổi | Bắt buộc | Chi phí |
|---|---|---|---|
| Google (Drive, Sheet) | 1 và 5 | Có | Miễn phí |
| **tikhub** | 2 và 4 | Nên có | **Tính tiền theo từng lượt gọi, bạn tự trả** |
| **aitoearn** | 4 và 5 | Nên có | Đăng ký miễn phí, cần nối kênh mạng xã hội |

**Về tikhub:** dùng để lấy bình luận thật và xu hướng thật từ TikTok, Instagram, YouTube. Mỗi lượt gọi đều tính tiền, phản hồi của dịch vụ ghi thẳng là sẽ tính phí. Bạn tự đăng ký và tự nạp một khoản nhỏ. Trong lớp sẽ có hướng dẫn gọi tiết kiệm: lấy một lần rồi lưu thành file, lần sau đọc lại file thay vì gọi lại.

Không đăng ký tikhub vẫn học đủ, chỉ bỏ đúng bước lấy dữ liệu thật, dùng bộ dữ liệu Thảo An thay thế.

**Về aitoearn:** dùng để đăng bài lên nhiều kênh cùng lúc và hẹn giờ đăng, hỗ trợ Facebook, TikTok, Instagram, LinkedIn, YouTube, Threads và nhiều kênh khác. Đăng ký trước, nhưng **đừng nối kênh công ty đang chạy thật**. Buổi học chỉ nối kênh cá nhân hoặc kênh lập riêng để thử.

---

## Phần E · Bài kiểm tra tự làm

Tick đủ 4 ô là bạn sẵn sàng vào lớp.

- [ ] **Ô 1.** Mở Claude Desktop, thấy tab **Code** ở trên cùng và bấm vào được.
- [ ] **Ô 2.** Trong tab Code, đã chọn được thư mục `C:\Users\<tên bạn>\thao-an-workspace`.
- [ ] **Ô 3.** Gõ một câu hỏi bất kỳ, Claude trả lời được (nghĩa là tài khoản trả phí còn dùng tốt).
- [ ] **Ô 4.** Claude tạo được file `ghi-chu.md` thật trong thư mục đó, mở file ra thấy đúng nội dung.

Thiếu ô nào thì xem bảng lỗi bên dưới.

---

## Lỗi hay gặp và cách xử lý

| Lỗi | Dấu hiệu bạn thấy | Cách xử lý |
|---|---|---|
| Máy công ty chặn cài phần mềm | Bảng đỏ "administrator has blocked", hoặc bắt nhập mật khẩu quản trị | Gửi IT xin quyền cài, kèm 2 link: claude.ai/download và git-scm.com. Chờ không kịp thì mang máy cá nhân đi học. Cách chống cháy: dùng bản web tại claude.ai, học được phần lớn nội dung nhưng **không thao tác được file trên máy**, nên phần Skill sẽ làm hạn chế |
| Không thấy tab Code | Trên cùng chỉ có Chat, hoặc chỉ có Chat và Cowork | 1) Đóng app rồi mở lại. 2) Kiểm tra đã đăng nhập chưa, chưa đăng nhập thì app ẩn bớt tính năng. 3) Kiểm tra bạn đang mở **Claude Desktop** chứ không phải trang claude.ai trong trình duyệt. 4) Gỡ app, tải lại bản mới nhất từ claude.ai/download |
| Tài khoản free hết lượt | Claude báo hết lượt, bắt chờ vài giờ | Nâng lên gói trả phí. Đây là điều kiện bắt buộc của lớp, 150 phút thực hành gói free không tải nổi. Nâng cấp trong Settings của app hoặc tại claude.ai |
| Không tìm thấy thư mục vừa tạo | Vào lại C:\Users mà không thấy `thao-an-workspace` | Mở File Explorer, bấm ô địa chỉ trên cùng, gõ `%USERPROFILE%` rồi Enter. Đúng thư mục của bạn sẽ mở ra. Nhìn xem có thư mục chưa, chưa có thì tạo lại ngay tại đó. Lỗi phổ biến: lúc nãy tạo nhầm trong Downloads hoặc Desktop |
| Cài Git xong vẫn báo thiếu | Claude Code báo không tìm thấy git, hoặc lệnh git không chạy | Khởi động lại máy. Windows chỉ nhận Git sau khi khởi động lại. Vẫn không được thì cài lại Git, lần này để nguyên mọi mặc định và không đổi thư mục cài. **Vẫn hỏng cũng không sao:** cứ tới lớp, Claude Code chạy được bằng PowerShell, chỉ cần báo giảng viên trước |
| Claude không chịu tạo file | Gõ lệnh tạo file nhưng không thấy file đâu | Xem lại có bảng xin phép hiện lên mà bạn bấm từ chối không. Gõ lại lệnh, lần này bấm **Yes**. Cũng kiểm tra bạn đang ở tab **Code**, không phải tab Chat. Tab Chat không thao tác được file trên máy |
| Không rõ mình đang ở đúng thư mục không | Không chắc Claude đang làm việc ở đâu | Gõ: `Liệt kê các file đang có trong thư mục làm việc hiện tại.` Claude sẽ đọc và trả về danh sách kèm đường dẫn |

---

## Trước buổi học

Kẹt ở bước nào thì **chụp màn hình chỗ đang kẹt, gửi vào nhóm lớp trước buổi học**. Ghi rõ bạn đang ở phần nào (A, B, C, D hay E). Giảng viên trả lời trong nhóm, hoặc gọi hỗ trợ riêng nếu cần.

Đừng để tới hôm học mới nói. Lúc đó cả lớp phải chờ bạn, và bạn mất phần thực hành.

---

CES Global · Creative, Effective, Sustainable
