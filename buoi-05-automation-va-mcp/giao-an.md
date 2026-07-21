# Buổi 5 · Automation & MCP Mindset

**Phụ đề:** Tự động hóa lead, content, báo cáo và chăm sóc khách hàng
**Thời lượng:** 2,5 giờ
**Agent xây được:** Automation Orchestrator, đóng thành file skill `.claude/skills/automation-orchestrator/SKILL.md` trong thư mục làm việc
**File đi kèm:** [demo-script.md](demo-script.md) · [workbook-hoc-vien.md](workbook-hoc-vien.md) · [luong-post-bai.md](luong-post-bai.md) · [system-prompt.md](system-prompt.md)

> Ý chính của buổi: nối các việc lặp lại thành luồng tự chạy. Khách điền form, AI phân loại và soạn phản hồi, sale nhận thông báo. Học viên không cần biết code.

Buổi 1 đã nối MCP nhưng chỉ cho Claude **đọc**: đọc bảng đơn hàng trên Google Sheet, đọc file trong thư mục làm việc. Buổi 5 mở thêm hai quyền nặng hơn hẳn: **ghi** vào bảng quản lý, và **gửi ra ngoài**, tức đăng bài thật lên kênh thật. Nên đây cũng là buổi nguyên tắc "người duyệt cuối" quan trọng nhất.

---

## Mục tiêu buổi

Hết 2,5 giờ, học viên phải:

- Vẽ được automation map của chính mình: liệt kê việc lặp lại, chọn ra 3 việc đáng tự động, bỏ ra việc không nên tự động.
- Có một bảng quản lý chạy được trên Google Sheet, Airtable hoặc Notion, có cột trạng thái và cột người duyệt.
- Chạy được ít nhất 1 luồng tự động, hoặc dựng được prototype của luồng đó nếu chưa nối được công cụ thật.
- Chạy trọn luồng post bài: từ caption trong chiến dịch 14 ngày, soát giới hạn của kênh, chuẩn bị ảnh, dừng lại cho người duyệt, rồi mới hẹn giờ đăng lên kênh thật.
- Chỉ đúng ranh giới giữa quyền đọc đã có từ buổi 1 và hai quyền mới của buổi 5: quyền ghi và quyền gửi ra ngoài. Và chỉ đúng chỗ nào trong luồng bắt buộc có người duyệt.

---

## Học viên chuẩn bị gì trước buổi

| Việc | Bắt buộc | Ghi chú |
|---|---|---|
| Thư mục làm việc của buổi 1 | Có | Trong đó có `CLAUDE.md`, `san-pham-thao-an.md`, `insight-khach-hang.md` (buổi 2), bảng chấm điểm lead (buổi 3), `lich-14-ngay.md` (buổi 4) |
| Tài khoản Google (Sheet) | Có | Hoặc Notion, hoặc Airtable bản miễn phí |
| Claude bản trả phí | Có | Cần để bật kết nối MCP |
| **Một kênh demo hoặc kênh cá nhân để nối** | Có | Lập trước ở nhà. **Tuyệt đối không nối fanpage công ty đang chạy thật.** Muốn dùng kênh công ty thì làm sau buổi, sau khi xin phép người phụ trách |
| Tài khoản aitoearn đã nối sẵn kênh demo | Nên có | Nối trước buổi ở nhà. Trong buổi không đủ thời gian đăng ký và duyệt quyền |
| Ảnh minh họa đã chuẩn bị, và logo file PNG nền trong | Nên có | Ảnh chụp thật hoặc ảnh làm sẵn từ buổi 4 đều được |
| Quyền đăng bài trên kênh | Tùy | Không có thì làm prototype, vẫn tính đạt |
| Danh sách việc lặp lại trong tuần | Nên có | Ghi thô ra giấy cũng được |

Nhắc trước buổi 1 ngày: "Mang theo danh sách những việc tuần nào bạn cũng phải làm lại. Càng chán càng tốt. Việc chán là việc đáng tự động. Và nhớ: hôm nay agent đăng bài thật được, nên chỉ nối kênh demo hoặc kênh cá nhân. Đừng ai nối fanpage công ty đang chạy."

---

## Timeline 2,5 giờ

| Khối | Thời lượng | Giảng viên làm gì |
|---|---|---|
| **1. Framework** | 20 phút | Giảng 4 phần: việc nào nên và không nên tự động; nhắc lại MCP và mở thêm quyền ghi; ba lớp của một luồng; vì sao luôn có chốt duyệt. Không mở công cụ, chỉ nói và vẽ bảng. |
| **2. Demo thật** | 35 phút | Chạy [demo-script.md](demo-script.md) trên case Thảo An. Vẽ map, dựng bảng lead, chạy trọn luồng post bài, rồi diễn cảnh bỏ bước duyệt. |
| **3. Làm sản phẩm** | 65 phút | Học viên mở [workbook-hoc-vien.md](workbook-hoc-vien.md). 18 phút đầu vẽ map; 25 phút giữa dựng bảng và nối luồng; 22 phút cuối chạy thử và viết mẫu thông báo. |
| **4. Review nhanh** | 10 phút | Gọi 3 học viên chiếu màn hình. Soát theo bảng tiêu chí bên dưới. |
| **5. Hoàn thiện và nộp** | 20 phút | Hoàn thiện checklist rủi ro, lưu automation map thành file `automation-map.md` trong thư mục làm việc, gỡ quyền kênh nếu không dùng tiếp, nộp. Chấm đạt hoặc chưa đạt tại chỗ. |

---

## Nội dung 20 phút Framework

### Phần 1 · Việc nào nên tự động, việc nào không (5 phút)

Mở bằng câu hỏi: "Tuần rồi ai copy dữ liệu từ chỗ này sang chỗ kia quá 3 lần?" Gần như cả lớp giơ tay. Đó là danh sách ứng viên tự động hóa.

Việc **nên** tự động, đủ cả 3 điều kiện:

1. **Lặp lại đều.** Tuần nào cũng làm, tháng nào cũng làm.
2. **Quy tắc rõ.** Bạn viết ra được: gặp trường hợp A thì làm B. Nếu bạn không viết ra được thì máy cũng không làm được.
3. **Sai thì sửa được.** Lỡ sai thì gỡ, sửa, làm lại. Không mất tiền, không mất khách.

Việc **không nên** tự động, chỉ cần dính một điều:

- Quyết định có tiền trong đó: duyệt giá, duyệt chiết khấu, chốt hợp đồng.
- Nội dung gửi thẳng ra ngoài mà không ai đọc lại: bài đăng, email khách, tin nhắn.
- Việc quy trình còn đang loạn. Tự động một mớ lộn xộn thì được một mớ lộn xộn chạy nhanh hơn.
- Việc mỗi lần một khác, không rút được quy tắc.

Câu chốt: "Tự động hóa là nhân bản quy trình bạn đang có. Quy trình tốt thì nhân ra tốt. Quy trình dở thì nhân ra dở, và dở nhanh hơn."

### Phần 2 · Nhắc lại MCP và mở thêm quyền ghi (2 phút)

MCP thì lớp làm rồi, ở buổi 1, tầng 4. Không giảng lại. Chỉ nhắc một câu rồi kéo sang chỗ mới:

"Buổi 1 anh chị đã nối một kết nối và cho Claude **đọc**: đọc bảng đơn hàng trên Google Sheet. Hôm nay mở thêm hai quyền nữa, và hai quyền này nặng hơn hẳn: **ghi** vào bảng của mình, và **gửi ra ngoài**, tức đăng bài lên kênh thật."

Vẽ lên bảng đúng ba dòng này, đây là phần phải nhấn:

| Quyền | Học ở buổi nào | Sai thì sao |
|---|---|---|
| Đọc | Buổi 1 | Đọc nhầm file, đọc lại là xong |
| Ghi | Buổi 5 | Ghi đè mất dữ liệu, còn khôi phục được nếu có bản sao |
| Gửi ra ngoài | Buổi 5 | Bài đã lên fanpage, có người đọc, có người chụp màn hình. Không rút lại được |

Ba câu chốt đi kèm bảng đó, nói nhanh, không giải thích dài:

1. **Quyền của mỗi kết nối do bạn cấp.** Bạn nối cái gì thì Claude làm được cái đó.
2. **Nối được nhiều thứ không có nghĩa là cho làm hết.** Đọc là một quyền. Ghi là quyền khác. Gửi ra ngoài là quyền nặng nhất, cấp riêng.
3. **Bước gửi ra ngoài luôn có người duyệt.** Đây là luật của khóa này, không phải gợi ý kỹ thuật.

Nói thêm đúng một câu về kênh, rồi chuyển: "Hôm nay chỉ nối kênh demo hoặc kênh cá nhân. Không ai nối fanpage công ty đang chạy thật. Cuối buổi tôi chỉ luôn cách gỡ quyền."

Câu chốt: "MCP tự động không có nghĩa là tự do. Tự động là máy làm các bước. Tự do là máy tự quyết. Chúng ta chỉ cho cái thứ nhất."

### Phần 3 · Ba lớp của một luồng tự động (9 phút)

Mọi luồng, dù đơn giản hay phức tạp, đều gồm đúng ba lớp. Vẽ lên bảng:

```
KÍCH HOẠT          →   XỬ LÝ                  →   ĐƯA RA
(cái gì bắt đầu)       (AI làm gì với nó)         (kết quả đi đâu)

Khách điền form        Chấm điểm lead             Ghi vào Sheet
Có tin nhắn mới        Phân loại câu hỏi          Gửi thông báo cho sale
Đến 8h sáng thứ Hai    Tổng hợp số tuần trước     Soạn nháp email
Đến lịch đăng          Lấy caption, soát giới     Hẹn giờ đăng lên kênh
                       hạn kênh, chuẩn bị ảnh
```

Giải thích từng lớp:

**Kích hoạt** là cái làm luồng chạy. Có ba kiểu: có việc mới xảy ra (khách điền form), đến giờ hẹn (8h sáng thứ Hai), hoặc người bấm nút.

**Xử lý** là phần AI làm. Đọc, phân loại, chấm điểm, viết nháp, chuẩn bị ảnh. Đây là chỗ các skill của bạn từ buổi 1 đến buổi 4 được gọi vào: skill viết bài, bảng chấm điểm lead, chiến dịch 14 ngày. Lớp này chỉ dùng quyền đọc, nên sai thì sửa được, không phải xin ai.

**Đưa ra** là kết quả đi đâu. Ghi vào bảng, gửi thông báo, đăng bài, gửi email. Đây mới là lớp mới của buổi 5, và là lớp duy nhất dùng quyền ghi và quyền gửi ra ngoài.

Nhấn: **chốt duyệt luôn nằm ở đầu lớp thứ ba.** Xử lý xong, dừng lại, người xem, người đồng ý, rồi mới đưa ra. Không có ngoại lệ cho bước gửi ra ngoài.

**Lớp thứ ba có hai phanh, không phải một.** Vẽ tiếp lên bảng:

```
XỬ LÝ xong  ->  [PHANH 1: NGƯỜI DUYỆT]  ->  hẹn giờ đăng
                                              |
                                        [PHANH 2: cửa sổ còn hủy được]
                                              |
                                          đến giờ, bài lên
```

Giải thích: "Phanh thứ nhất là người đọc và đồng ý. Phanh thứ hai là hẹn giờ. Anh chị duyệt xong, đừng cho nó đăng ngay. Hẹn 30 phút sau, hoặc hẹn 8h sáng mai. Trong khoảng đó, phát hiện sai thì hủy bài đã hẹn, hoặc dời giờ để sửa. Đăng ngay là bỏ mất phanh thứ hai."

Hỏi lớp một câu, dừng chờ: "Vậy giữa đăng ngay và hẹn giờ 30 phút, cái nào an toàn hơn? Vì sao?" Đáp án cần nghe: hẹn giờ, vì còn cửa sổ để hủy.

Nói thêm về giới hạn từng kênh, một câu thôi: "Mỗi nền tảng một giới hạn khác nhau. Twitter cho 280 ký tự, Facebook cho hơn sáu vạn. YouTube bắt phải có tiêu đề dưới 100 ký tự. Đừng nhớ thuộc, lát nữa có công cụ hỏi ra được. Chỉ cần nhớ: một caption không dùng chung cho mọi kênh."

Bài tập nhanh tại chỗ, 2 phút: cho lớp lấy một việc lặp lại của mình và điền đúng ba ô này lên giấy. Ai điền được ba ô là ai vẽ được automation map.

### Phần 4 · Vì sao luôn phải có chốt người duyệt (4 phút)

Đây là phần quan trọng nhất buổi. Nói thẳng ba lý do:

1. **AI không biết nó đang bịa.** Nó chọn từ nghe hợp lý tiếp theo. Một bài viết sai thành phần, sai giá, hoặc dùng từ cấm như "trị mụn" đều đọc rất trôi.
2. **Gửi ra ngoài là không rút lại được.** Bài đăng có người chụp màn hình. Email đã vào hộp thư người ta. Gỡ bài không xóa được việc khách đã đọc.
3. **Ngành nào cũng có ràng buộc riêng.** Thảo An có danh sách từ cấm. Tài chính có quy định quảng cáo. Y tế còn chặt hơn. Máy không tự biết ranh giới của bạn.

Nhắc lại ba nguyên tắc chống bịa, và nói rõ vì sao buổi này khác:

1. **Chỉ dùng dữ liệu người dùng cấp.** Không tự chế số liệu, giá, tên khách, thành phần.
2. **Gắn nhãn nguồn.** `[DATA THẬT]` cho phần trích từ file, `[SUY LUẬN]` cho phần agent tự suy. Thiếu thì ghi "chưa đủ dữ liệu".
3. **Người duyệt cuối.** Bốn buổi trước, agent bịa thì bạn đọc và sửa. Buổi này, agent bịa mà không ai duyệt thì cái bịa đó đã lên fanpage.

Báo trước cho lớp: "Ở phần demo, tôi sẽ cố tình chạy một luồng bỏ bước duyệt. Các bạn nhìn kỹ cái gì ra ngoài."

---

## Bốn luồng đáng tự động nhất cho Thảo An

Dùng bốn luồng này làm ví dụ chuẩn cho cả buổi. Học viên chọn ít nhất một luồng để làm thật.

### Luồng A · Lead vào bảng, chấm điểm, báo sale

- **Kích hoạt:** khách điền form quan tâm sỉ, hoặc có inbox mới trên fanpage hỏi giá sỉ.
- **Xử lý:** agent đọc nội dung, rút ra loại cơ sở, khu vực, nhu cầu; chấm điểm theo bảng chấm điểm lead của buổi 3; soạn sẵn câu trả lời đầu tiên.
- **Đưa ra:** ghi một dòng mới vào bảng lead; gửi thông báo cho sale kèm điểm và câu trả lời nháp.
- **Chốt duyệt:** sale đọc câu trả lời nháp, sửa nếu cần, rồi tự bấm gửi cho khách. Agent không gửi.
- **Ghi log:** ngày nhận, kênh vào, điểm, ai nhận, ngày phản hồi đầu tiên.

### Luồng B · Luồng post bài

Đây là luồng lõi của buổi. Đặc tả đầy đủ nằm trong [luong-post-bai.md](luong-post-bai.md).

- **Kích hoạt:** đến lịch đăng trong chiến dịch 14 ngày của buổi 4.
- **Xử lý:** lấy góc nội dung và caption; hỏi `listChannelPlatforms` xem kênh định đăng cho bao nhiêu ký tự, bao nhiêu ảnh, có bắt tiêu đề không; cắt caption cho vừa; chuẩn bị ảnh đúng tỷ lệ kênh, có logo.
- **Chốt duyệt:** người xem caption, ảnh, tên kênh và giờ hẹn cùng lúc, sửa hoặc bấm đồng ý. Bắt buộc, không được bỏ. Agent chưa được gọi công cụ đăng nào trước lúc này, kể cả công cụ tạo luồng hẹn giờ.
- **Đưa ra:** gọi `createChannelPublishFlow` **hẹn giờ**, không đăng ngay. Trong cửa sổ chờ, phát hiện sai thì `cancelChannelPublishTask` để hủy, hoặc `updateChannelPublishAt` để dời giờ mà sửa. Cần gấp thì `publishChannelTaskNow`.
- **Ghi log:** bài nào, ngày nào, kênh nào, hẹn giờ hay đăng ngay, mã task, ai duyệt. Lấy link bài bằng `listChannelPublishRecords`.

Kết quả thật của luồng này: [../case-study/thao-an/assets/images/thao-an-serum-rau-ma-fb-01.png](../case-study/thao-an/assets/images/thao-an-serum-rau-ma-fb-01.png). Mở ra chiếu cho lớp xem.

Nhấn với lớp một câu: "Hẹn giờ không phải để bài lên đúng khung giờ vàng. Hẹn giờ là để anh chị còn kịp hủy."

### Luồng C · Báo cáo tuần tự tổng hợp

- **Kích hoạt:** 8h sáng thứ Hai hàng tuần.
- **Xử lý:** agent đọc bảng lead và bảng log bài đăng của 7 ngày trước; đếm lead mới theo kênh, số bài đã đăng, số đơn gắn được nguồn; so với tuần trước; ghi rõ chỗ nào thiếu dữ liệu.
- **Đưa ra:** soạn bản nháp báo cáo, gửi vào nhóm chat nội bộ hoặc ghi vào một trang Notion.
- **Chốt duyệt:** báo cáo nội bộ, người phụ trách đọc trước khi chuyển lên sếp. Nhẹ tay hơn luồng B vì không ra ngoài công ty.
- **Ghi log:** tuần nào, ai xem, quyết định gì sau đó.

Nhấn với lớp: báo cáo phải ghi thẳng "chưa đủ dữ liệu" khi bảng thiếu, không được lấp bằng số ước.

### Luồng D · Trả lời câu hỏi lặp trong inbox theo mẫu duyệt sẵn

- **Kích hoạt:** có tin nhắn mới trong inbox fanpage.
- **Xử lý:** agent phân loại tin vào 6 nhóm quen thuộc: hỏi giá lẻ, hỏi giá sỉ, hỏi thành phần, hỏi hợp loại da nào, hỏi ship, hỏi khác. Chọn mẫu trả lời tương ứng đã duyệt sẵn, điền thông tin thiếu.
- **Đưa ra:** đưa nháp vào ô chờ duyệt, gắn nhãn nhóm câu hỏi.
- **Chốt duyệt:** người trực inbox đọc và bấm gửi. Nhóm "hỏi khác" không có mẫu, chuyển thẳng cho người.
- **Ghi log:** nhóm câu hỏi, thời gian phản hồi, có sửa nháp hay không.

Nhấn: bộ mẫu trả lời phải được duyệt trước, một lần, bằng tay. Agent chỉ được chọn mẫu và điền chỗ trống, không được tự viết câu mới cho khách.

---

## Điểm học viên hay vấp và cách xử lý

**1. Tự động hóa quá sớm, khi quy trình còn loạn.**
Biểu hiện: học viên muốn nối form vào CRM, mà chưa có ai chốt lead vào thì ai xử lý, xử lý trong bao lâu.
Xử lý: bắt viết ra quy trình bằng tay trước, đúng 5 dòng: ai nhận, làm gì, trong bao lâu, chuyển cho ai, ghi vào đâu. Không viết được 5 dòng đó thì chưa tự động được. Cho làm luồng khác đơn giản hơn.

**2. Để agent tự đăng, không ai duyệt.**
Biểu hiện: học viên khoe "em nối thẳng, nó tự đăng luôn, khỏi mất công".
Xử lý: mở đoạn demo bỏ bước duyệt cho xem lại. Bắt thêm một bước dừng vào luồng. Nói rõ: luồng nào không có chốt duyệt thì bài nộp chưa đạt, dù chạy trơn tru.

**2b. Duyệt rồi nhưng cho đăng ngay, bỏ mất phanh thứ hai.**
Biểu hiện: học viên duyệt xong bấm `publishChannelTaskNow` cho nhanh, bài lên tức thì.
Xử lý: bắt đổi sang hẹn giờ ít nhất 15 phút. Hỏi lại: "Duyệt xong 2 phút mới thấy sai chính tả tên khách thì làm gì?" Chỉ vào `cancelChannelPublishTask` và `updateChannelPublishAt`. Đăng ngay chỉ dùng khi có lý do gấp và người duyệt biết mình đang bỏ phanh.

**3. Không ghi log, nên tuần sau không đo được gì.**
Biểu hiện: luồng chạy đẹp, bài lên đều, nhưng hỏi "tuần rồi đăng mấy bài, kênh nào ra đơn" thì không trả lời được.
Xử lý: bắt thêm bảng log ngay trong buổi. Tối thiểu 6 cột: ngày, nội dung, kênh, ai duyệt, kết quả, ghi chú. Chưa có bảng log thì chưa tính là luồng hoàn chỉnh.

**4. Nối quá nhiều bước ngay lần đầu.**
Biểu hiện: sơ đồ có 9 bước, 4 nhánh rẽ, chạy thử thì hỏng ở bước 3 và không biết hỏng chỗ nào.
Xử lý: cắt xuống còn 3 bước, chạy cho thông, rồi mới thêm. Nguyên tắc: luồng đầu tiên phải chạy được từ đầu tới cuối trong 1 lần, dù thô.

**5. Cấp quyền quá rộng cho kết nối.**
Biểu hiện: học viên cấp quyền ghi và xóa trên toàn bộ Drive công ty cho một luồng chỉ cần đọc một file.
Xử lý: rà lại từng kết nối, hỏi "luồng này cần đọc hay cần ghi?" Cấp đúng cái cần. Tạo file hoặc thư mục riêng cho automation, không trỏ vào thư mục chung.

**5b. Nối nhầm fanpage công ty đang chạy thật.**
Biểu hiện: đến bước nối kênh, học viên đăng nhập luôn tài khoản quản trị fanpage công ty vì "tiện, em có sẵn quyền".
Xử lý: dừng ngay, gỡ ra, nối lại bằng kênh demo hoặc kênh cá nhân. Đây là quy định cứng của buổi, không phải khuyến nghị. Trợ giảng đi một vòng kiểm tra tên kênh trên màn hình từng máy trước khi lớp chạy luồng post bài. Muốn dùng kênh công ty thì làm sau buổi, sau khi đã xin phép người phụ trách trang.

**5c. Học xong để nguyên quyền, không gỡ.**
Biểu hiện: hết buổi, kết nối vẫn còn, kênh vẫn nối, không ai nhớ tới nữa.
Xử lý: dành 2 phút trong 20 phút cuối để cả lớp làm cùng lúc. Hai chỗ phải gỡ: trong Claude Desktop vào Settings rồi Connectors, ngắt kết nối aitoearn; trên chính nền tảng (Facebook, TikTok, LinkedIn...) vào phần ứng dụng đã cấp quyền, gỡ ứng dụng ra. Ai còn dùng tiếp thì giữ, nhưng phải biết đường gỡ. *Giao diện có thể đổi theo phiên bản, giảng viên bấm thử một lượt trước buổi.*

**6. Không có phương án khi công cụ hỏng.**
Biểu hiện: hỏi "hôm nào Make lỗi thì sao" thì học viên ngớ người.
Xử lý: bắt viết một dòng vào checklist rủi ro: ai kiểm tra, kiểm mấy ngày một lần, hỏng thì làm tay theo bước nào. Luồng nào cũng phải làm tay được, nếu không thì luồng đó là điểm chết.

**7. Chưa nối được công cụ thật nên ngồi im.**
Biểu hiện: học viên không có quyền fanpage, không mở được tài khoản Make, ngồi chờ hết 65 phút.
Xử lý: chỉ vào phần "chưa nối được công cụ thật thì làm gì" trong workbook. Làm prototype trên giấy hoặc chạy tay từng bước, vẫn tính là đạt.

---

## Tiêu chí review 10 phút

Gọi 3 học viên chiếu màn hình. Mỗi người 2 phút. Soát đúng 5 điểm, không lan man:

| # | Soát cái gì | Đạt khi |
|---|---|---|
| 1 | Mở automation map, chỉ vào một luồng bất kỳ | Điền đủ 5 ô: kích hoạt, xử lý, đưa ra, ai duyệt, ghi log ở đâu |
| 2 | Hỏi "chốt duyệt nằm ở bước số mấy, và sau đó bài lên kiểu gì" | Trả lời được ngay: chốt duyệt nằm trước mọi lời gọi công cụ đăng, và sau chốt là hẹn giờ, không phải đăng ngay |
| 3 | Mở bảng quản lý | Có cột trạng thái và cột người duyệt, không phải bảng chỉ để chứa dữ liệu |
| 4 | Đọc to mẫu thông báo hoặc email | Đủ thông tin để người nhận hành động ngay: việc gì, của ai, cần làm gì, hạn nào |
| 5 | Hỏi "tuần sau bạn đo cái gì từ luồng này" | Chỉ được vào cột cụ thể trong bảng log, không trả lời chung chung |

Trước khi review, hỏi nhanh cả lớp một câu: "Ai đang nối kênh không phải kênh demo hay kênh cá nhân, giơ tay." Có người giơ thì xử lý ngay tại chỗ, gỡ ra, nối lại.

Nếu có học viên để agent tự đăng không duyệt, dừng lại và cho cả lớp xem. Đây là lỗi đắt nhất của buổi 5.

---

## Sản phẩm nộp cuối buổi

Nộp trong 20 phút cuối. Đúng danh sách này, không thiếu, không thừa:

| # | Sản phẩm | Số lượng |
|---|---|---|
| 1 | Automation map (bảng 5 cột, tối thiểu 3 luồng) | 1 |
| 2 | Bảng quản lý trên Sheet, Airtable hoặc Notion | 1 |
| 3 | Automation chạy được, hoặc prototype có ảnh chụp từng bước | 1 |
| 4 | Mẫu thông báo hoặc email | 1 |
| 5 | Checklist kiểm soát rủi ro | 1 |

### Cách chấm

**Đạt** khi đủ cả 5 điều:

- Đủ 5 sản phẩm ở bảng trên.
- Automation map điền đủ 5 ô cho mỗi luồng, trong đó ô "ai duyệt" không được để trống.
- Luồng nào có bước gửi ra ngoài đều có chốt duyệt trước bước đó, và chốt đó nằm trước cả lời gọi tạo luồng hẹn giờ.
- Bảng quản lý có cột trạng thái, cột người duyệt, và các cột đủ để tuần sau đo được.
- Checklist rủi ro nêu được ít nhất 3 rủi ro cụ thể kèm cách xử lý, không phải câu chung chung. Trong đó bắt buộc có hai dòng: kênh đang nối là kênh gì, và gỡ quyền thế nào khi không dùng tiếp.

**Chưa đạt** khi rơi vào một trong các trường hợp:

- Có luồng gửi ra ngoài mà không có chốt duyệt. Lỗi nặng nhất, chưa đạt ngay.
- Nối kênh của công ty đang chạy thật thay vì kênh demo hoặc kênh cá nhân. Chưa đạt ngay, và phải gỡ tại chỗ.
- Automation map để trống ô "ai duyệt" hoặc ô "ghi log ở đâu".
- Bảng quản lý chỉ chứa dữ liệu, không có cột trạng thái, không đo được gì.
- Mẫu thông báo chung chung kiểu "có lead mới", người nhận đọc xong vẫn phải đi tra.
- Checklist rủi ro chỉ chép lại lý thuyết, không gắn với luồng học viên vừa dựng.

Chưa đạt thì sửa và nộp lại trước buổi 6. Buổi 6 đóng gói cả hệ thống thành Claude Skill và playbook, thiếu automation map là thiếu một chương của playbook.

---

## Nối sang buổi 6

Nói câu này trước khi giải tán lớp:

"Năm buổi vừa rồi các bạn xây từng mảnh: thư mục làm việc, insight, sale, content, automation. Buổi sau chúng ta đóng gói cả bộ thành một thứ bàn giao được cho người khác dùng: Claude Skill và AI Agent Playbook, kèm kế hoạch triển khai 14 ngày. Automation map hôm nay là một chương trong playbook đó. Ai chưa lưu thành file `automation-map.md` trong thư mục làm việc thì buổi sau phải vẽ lại."

---

CES Global · Creative, Effective, Sustainable
