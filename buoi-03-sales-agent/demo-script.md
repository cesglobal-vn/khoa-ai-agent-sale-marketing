# Buổi 3 · Kịch bản demo 35 phút

Giảng viên chạy trên bộ dữ liệu Thảo An: `case-study/thao-an/danh-sach-lead-si.md` và `case-study/thao-an/chinh-sach-gia-si.md`.

**Chuẩn bị trước giờ dạy:** chép 2 file dữ liệu trên vào thư mục làm việc `thao-an-marketing`, cạnh `CLAUDE.md` và `san-pham-thao-an.md`. Lưu sẵn 3 file skill từ `system-prompt.md` vào `.claude/skills/`. Mở Claude Desktop, vào tab **Code**, trỏ đúng thư mục làm việc. Bật màn hình đủ to để lớp đọc được bảng. Giao diện app có thể đổi theo phiên bản, giảng viên bấm thử một vòng trước buổi.

| Mốc | Nội dung | Skill |
|---|---|---|
| 00:00 đến 02:00 | Nạp dữ liệu, giới thiệu 3 skill | lead-scoring |
| 02:00 đến 12:00 | Chấm điểm 10 lead ra bảng, giải thích thứ hạng | lead-scoring |
| 12:00 đến 20:00 | Email cá nhân hóa L01 và L04, so sánh | lead-scoring |
| 20:00 đến 26:00 | Ca L07 độc quyền khu vực, điểm nhấn của buổi | soan-proposal |
| 26:00 đến 33:00 | Proposal và bảng báo giá cho L04 | soan-proposal |
| 33:00 đến 35:00 | Chốt và giao việc 65 phút | |

## 00:00 đến 02:00 · Nạp dữ liệu

**Thao tác:** mở một phiên mới trong tab Code. Chỉ cho lớp thấy 3 file skill nằm trong `.claude/skills/`, nói rõ không phải dán prompt nữa. Rồi gõ prompt sau.

```
Đọc san-pham-thao-an.md và danh-sach-lead-si.md trong thư mục làm việc.
Đây là dữ liệu nền của Thảo An. Xác nhận, chưa làm gì thêm.

Xác nhận theo mẫu:
1. Bạn đọc được bao nhiêu lead.
2. Lead nào thiếu thông tin người phụ trách.
3. Ba loại dữ liệu nào KHÔNG có trong file mà việc chấm điểm lead thường cần.
```

**Kết quả mong đợi:** agent trả lời 10 lead; L03 và L08 thiếu người phụ trách; ba thứ thiếu là doanh số hoặc lượng khách mỗi tháng, ngân sách nhập hàng, và họ đang nhập của ai với giá bao nhiêu.

**Nói với lớp:** "Câu hỏi số 3 quan trọng nhất. Tôi bắt agent tự khai nó thiếu gì trước khi cho nó làm việc. Agent nào trả lời 'dữ liệu đầy đủ' là agent sắp bịa. Đây là bước 30 giây, đừng bỏ."

## 02:00 đến 12:00 · Chấm điểm 10 lead

**Thao tác:** vẫn phiên đó, dán bảng tiêu chí đã chuẩn bị. Claude báo đang dùng skill `lead-scoring`, chỉ cho lớp thấy dòng đó rồi đi tiếp. Nhấn mạnh với lớp là bảng tiêu chí do người viết, không phải agent nghĩ ra.

```
Chấm điểm 10 lead theo ĐÚNG bộ tiêu chí dưới. Không tự thêm, không tự bớt tiêu chí.

Thang 1 đến 5 cho mỗi tiêu chí.

A. Quy mô đơn dự kiến (trọng số 25%)
5 = đại lý, từ 300 sp/đơn | 4 = chuỗi, 100 đến 299 | 3 = spa hoặc cửa hàng lẻ, 30 đến 99
2 = tiệm nhỏ, 10 đến 29 | 1 = dưới đơn tối thiểu hoặc không đoán được

B. Độ khớp định vị lành tính, thảo mộc Việt, tầm trung (trọng số 25%)
5 = khách nói thẳng cần dòng lành tính hoặc thiên nhiên | 4 = tệp khách chắc chắn khớp
3 = khớp một phần | 2 = khớp yếu | 1 = lệch hẳn

C. Mức độ quan tâm thể hiện qua trao đổi (trọng số 30%)
5 = hỏi giá từ 2 lần, hoặc xin hồ sơ để duyệt nội bộ | 4 = chủ động hỏi 1 lần có nội dung cụ thể
3 = từng mua nhưng chưa quay lại | 2 = mới nhắn hỏi chung chung | 1 = chưa phản hồi

D. Khả năng chốt trong 30 ngày (trọng số 20%)
5 = người quyết là chủ, không có quy trình duyệt | 4 = chủ nhưng còn vướng điều kiện
3 = có người phụ trách nhưng phải trình duyệt | 2 = quy trình duyệt dài hoặc yêu cầu vượt chính sách
1 = chưa rõ ai phụ trách

Công thức: Điểm = (A×0,25 + B×0,25 + C×0,30 + D×0,20) × 20

Xuất bảng markdown, cột: Lead | Tên | A | B | C | D | Điểm | Nhóm | Độ tin cậy | Lý do một dòng

Quy tắc bắt buộc:
- Tiêu chí nào chấm bằng suy luận thì ghi số kèm dấu * và chú thích cuối bảng.
- Lead có từ 2 tiêu chí trở lên chấm bằng suy luận thì Độ tin cậy = Thấp.
- Nhóm A = từ 75 điểm, Nhóm B = 60 đến 74, Nhóm C = dưới 60.
- KHÔNG bịa doanh số, ngân sách, hay tên người phụ trách.
```

**Kết quả mong đợi:**

| Lead | Tên | A | B | C | D | Điểm | Nhóm | Tin cậy |
|---|---|---|---|---|---|---|---|---|
| L01 | Spa An Nhiên | 3 | 5 | 5 | 5 | **90** | A | Cao |
| L04 | Chuỗi Beauty House | 4 | 4 | 5 | 2 | **78** | A | Cao |
| L07 | Đại lý Minh Phát | 5 | 3 | 5 | 2 | **78** | A | Trung bình |
| L09 | Spa Thanh Tâm | 3 | 5 | 3 | 4 | **74** | B | Trung bình |
| L10 | Bé Xíu Cosmetic | 3 | 3 | 4 | 4 | **70** | B | Trung bình |
| L06 | Spa Ngọc Diệp | 3 | 4 | 3 | 4 | **69** | B | Trung bình |
| L05 | Nail & Skin Mika | 2 | 2 | 4 | 5 | **64** | B | Cao |
| L02 | Mỹ phẩm Lan Anh | 3 | 3 | 2 | 3 | **54** | C | Trung bình |
| L03 | Spa Hương Sen | 3* | 4* | 2 | 1 | **51** | C | **Thấp** |
| L08 | Organic Life | 3* | 5 | 1 | 1 | **50** | C | **Thấp** |

**Nói với lớp, giải thích thứ hạng.** Đây là 6 phút quan trọng nhất của phần này, đừng lướt:

- **Vì sao L01 đứng đầu với 90.** Chị Hạnh hỏi giá sỉ 2 lần trong một tháng, đó là hành vi thật chứ không phải phán đoán. Chị nói thẳng cần dòng lành tính cho khách da nhạy cảm, khớp đúng định vị Thảo An. Chị là chủ, gật là xong. Điểm quy mô chỉ 3 vì spa 2 cơ sở không lấy nhiều, nhưng ba tiêu chí còn lại đều 5.
- **Vì sao L04 và L07 bằng nhau 78 nhưng L04 xếp trên.** Cùng điểm thì phân định bằng độ tin cậy và bằng chuyện việc cần làm có nằm trong tầm tay không. L04 chỉ yêu cầu gửi hồ sơ năng lực và chứng nhận test da liễu, hai thứ này Thảo An có sẵn, làm được trong hôm nay. L07 vướng độc quyền khu vực, thứ chưa có chính sách, phải chờ chủ doanh nghiệp. Lead nào tự mình đẩy tiếp được thì xếp trên.
- **Vì sao L07 điểm quy mô 5 mà vẫn không lên số 1.** Đại lý là đơn to nhất, nhưng khả năng chốt chỉ 2 vì yêu cầu vượt bảng giá. Đơn to mà treo vô thời hạn không bằng đơn vừa chốt được tuần này.
- **Vì sao L08 khớp định vị 5 mà vẫn cuối bảng.** Organic Life định vị hàng thiên nhiên, khớp gần như tuyệt đối. Nhưng gửi 1 email chưa ai trả lời, và không biết gửi cho ai. Khớp mà không liên lạc được thì chưa phải lead, mới là danh sách gọi.
- **Vì sao L03 và L08 tin cậy Thấp.** Chỉ vào dấu sao trong bảng. Điểm quy mô và độ khớp của hai lead này suy ra từ loại hình cơ sở, không có ghi chú trao đổi nào chống lưng. Cộng thêm chưa rõ người phụ trách. Việc cần làm với hai lead này không phải gửi proposal, mà là gọi điện tìm đúng người.

**Câu chốt cho lớp:** "Điểm số không phải để xếp hạng cho vui. Nó trả lời một câu: sáng mai gọi ai trước. Nhóm A gọi trong 48 giờ. Nhóm B nuôi 2 tuần. Nhóm C đi tìm thông tin đã, chưa gửi gì hết."

**Lưu bảng lại ngay:** gõ `Lưu bảng này thành bang-diem-lead.md trong thư mục làm việc.` Claude xin phép ghi file thì bấm **Yes**. Nói với lớp: "Bước sau đọc lại file này, không ai phải copy dán bảng qua lại."

## 12:00 đến 20:00 · Email cá nhân hóa, hai lead khác tính chất

**Thao tác:** vẫn phiên đó, chạy hai prompt liên tiếp.

```
Viết email tiếp cận cho L01 Spa An Nhiên.

Ràng buộc:
- Bám ĐÚNG ghi chú trao đổi của L01 trong file. Ít nhất một câu phải nhắc lại điều chị Hạnh đã nói hoặc đã làm.
- Dưới 150 từ. Giọng thân, gọn, không hoa mỹ.
- Chỉ được nhắc mức chiết khấu có trong chinh-sach-gia-si.md, ghi rõ điều kiện số lượng đi kèm.
- Không dùng các từ trong danh sách "Điều KHÔNG được nói" của hồ sơ sản phẩm.
- Kết bằng MỘT lời đề nghị bước tiếp cụ thể.
- Cuối email liệt kê phần nào là [DATA THẬT], phần nào là [SUY LUẬN].
```

**Kết quả mong đợi:**

> **Tiêu đề:** Bảng giá sỉ Thảo An cho 2 cơ sở An Nhiên
>
> Chào chị Hạnh,
>
> Chị có hỏi bảng giá sỉ hai lần trong tháng vừa rồi, em xin lỗi vì trả lời chị hơi chậm. Gửi chị đầy đủ ở đây.
>
> Chị nói đang tìm dòng lành tính cho khách da nhạy cảm. Serum rau má B5 của bên em đang được các spa lấy nhiều nhất cho nhóm khách đó: không cồn, không hương liệu tổng hợp, đã test da liễu. Thành phần chính là chiết xuất rau má, Panthenol B5 và Glycerin.
>
> Với 2 cơ sở, em đề xuất chị lấy mức Sỉ cơ bản: từ 30 sản phẩm mỗi đơn, chiết khấu 35%, serum về 208.000đ một chai. Từ 30 sản phẩm là bên em lo phí vận chuyển, và chị được cấp bộ ảnh sản phẩm cùng nội dung mẫu để đăng.
>
> Chị cho em xin 10 phút gọi trong tuần này để em tư vấn cơ cấu hàng cho 2 cơ sở nhé. Chị rảnh sáng hay chiều ạ?
>
> ---
> [DATA THẬT] hỏi giá 2 lần, tìm dòng lành tính cho da nhạy cảm, có 2 cơ sở, chị Hạnh là chủ, mức 35% và giá 208.000đ, miễn phí vận chuyển từ 30 sp, bộ ảnh và nội dung mẫu.
> [SUY LUẬN] dự đoán chị lấy được mức 30 sản phẩm. Chưa có dữ liệu lượng khách mỗi tháng của An Nhiên, cần hỏi trong cuộc gọi.

Rồi chạy tiếp lead thứ hai.

```
Viết email cho L04 Chuỗi Beauty House. Cùng ràng buộc như trên, thêm:
- Người nhận là anh Tuấn, bộ phận mua hàng, không phải chủ.
- Anh yêu cầu hồ sơ năng lực và chứng nhận test da liễu. Quy trình duyệt của họ 3 tuần.
- Nếu tài liệu nào Thảo An chưa chắc có sẵn, đánh dấu [CẦN XÁC NHẬN] thay vì hứa gửi.
```

**Kết quả mong đợi:**

> **Tiêu đề:** Hồ sơ năng lực và chứng nhận sản phẩm Thảo An, gửi anh Tuấn
>
> Chào anh Tuấn,
>
> Theo yêu cầu của anh, em gửi bộ tài liệu để Beauty House đưa vào quy trình duyệt nhà cung cấp.
>
> Đính kèm:
> 1. Hồ sơ năng lực Thảo An: pháp nhân, năng lực sản xuất, danh mục 3 SKU.
> 2. Bảng thông tin sản phẩm: thành phần chính, công dụng ghi trên nhãn, đối tượng da phù hợp.
> 3. Chứng nhận test da liễu. [CẦN XÁC NHẬN: hồ sơ sản phẩm mới ghi "đã test da liễu", chưa có số hiệu và đơn vị cấp. Cần lấy bản gốc trước khi gửi.]
>
> Về thương mại, với quy mô 6 cửa hàng, đơn từ 100 sản phẩm áp mức Sỉ lớn, chiết khấu 42%, miễn phí vận chuyển, kèm bộ ảnh và nội dung mẫu cho từng điểm bán.
>
> Em hiểu quy trình duyệt của bên anh khoảng 3 tuần. Em xin phép hỏi lại anh vào cuối tuần thứ hai xem hội đồng cần bổ sung gì không, để mình không mất thêm một vòng.
>
> Anh cho em biết cần thêm tài liệu nào nữa không ạ?

**Nói với lớp, đặt hai email cạnh nhau:** "Nhìn hai email này. Cùng một sản phẩm, cùng một agent, cùng một chính sách giá. Nhưng khác nhau ở bốn chỗ, và cả bốn đều đến từ cột ghi chú trao đổi:

- **Mức chiết khấu khác nhau:** 35% cho An Nhiên, 42% cho Beauty House. Không phải vì Beauty House to hơn nên ta ưu ái, mà vì họ mua số lượng khác nhau nên rơi vào mức khác nhau trong cùng một bảng.
- **Người nhận khác nhau:** chị Hạnh là chủ, nói chuyện sản phẩm và khách của chị. Anh Tuấn là mua hàng, cần tài liệu để trình lên, nên email là danh sách đính kèm.
- **Lời đề nghị khác nhau:** An Nhiên xin gọi 10 phút vì chốt được ngay. Beauty House không xin gọi, mà xin một mốc hỏi lại giữa quy trình 3 tuần.
- **Chỗ chưa chắc được đánh dấu:** file sản phẩm chỉ ghi 'đã test da liễu', không có số hiệu chứng nhận. Agent viết `[CẦN XÁC NHẬN]` thay vì hứa gửi. Nếu nó tự bịa ra một số hiệu chứng nhận thì đó là hứa hẹn với một chuỗi 6 cửa hàng bằng giấy tờ không tồn tại.

Đây là khác biệt giữa email cá nhân hóa và email điền tên. Che tên đi vẫn biết email nào của ai."

## 20:00 đến 26:00 · Ca L07 độc quyền khu vực

**Đây là điểm nhấn của buổi. Chạy chậm, đừng vội.**

**Thao tác:** mở **phiên mới** trong tab Code. File `chinh-sach-gia-si.md` đã nằm trong thư mục làm việc, không phải dán. Gõ prompt sau, Claude sẽ tự gọi skill `soan-proposal`.

```
Lead L07 Đại lý Minh Phát, Nghệ An, anh Phát.
Yêu cầu của anh Phát, nguyên văn từ ghi chú: "Muốn độc quyền khu vực. Hỏi chiết khấu cao hơn bảng giá chuẩn."

Soạn phản hồi cho anh Phát.

Ràng buộc:
- Đối chiếu từng yêu cầu với chinh-sach-gia-si.md.
- Yêu cầu nào có chính sách thì trả lời thẳng, dẫn đúng con số.
- Yêu cầu nào KHÔNG có chính sách thì KHÔNG được tự quyết, không được gợi ý một mức nào cả.
- Xuất theo 3 phần: (1) Bảng đối chiếu yêu cầu, (2) Nội dung email gửi anh Phát, (3) Việc cần trình chủ doanh nghiệp.
```

**Kết quả mong đợi, phần 1:**

| Yêu cầu của anh Phát | Chính sách có không | Agent được trả lời gì |
|---|---|---|
| Chiết khấu cho đại lý | **Có.** Mức Đại lý, từ 300 sp, chiết khấu 48% | Trả lời thẳng: 48%, kèm giá quy đổi từng SKU |
| Công nợ | **Có.** Đại lý đã ký hợp đồng được công nợ 15 ngày | Trả lời thẳng, kèm điều kiện đã ký hợp đồng |
| Chiết khấu **cao hơn** bảng chuẩn | **Không.** Mục "Điều CHƯA có chính sách": chiết khấu vượt 48% | Không tự quyết. Xin ý kiến chủ doanh nghiệp |
| **Độc quyền khu vực** Nghệ An | **Không.** Mục "Điều CHƯA có chính sách" ghi đích danh L07 | Không tự quyết. Xin ý kiến chủ doanh nghiệp |

**Kết quả mong đợi, phần 2, email:**

> Chào anh Phát,
>
> Cảm ơn anh đã quan tâm hợp tác phân phối Thảo An tại Nghệ An. Em trả lời anh từng ý.
>
> **Phần em trả lời được ngay.** Mức Đại lý áp cho đơn từ 300 sản phẩm, chiết khấu 48%. Quy đổi: serum rau má B5 166.400đ, kem nghệ mật ong 130.000đ, mặt nạ đất sét trà xanh 93.600đ. Đại lý đã ký hợp đồng được công nợ 15 ngày, miễn phí vận chuyển, và được cấp bộ ảnh sản phẩm cùng nội dung mẫu.
>
> **Phần em cần xin ý kiến.** Hai đề nghị của anh là độc quyền khu vực Nghệ An, và mức chiết khấu cao hơn 48%. Cả hai đều vượt khung chính sách hiện tại của bên em, nên em không dám tự nhận với anh. Em trình chủ doanh nghiệp và phản hồi anh trong 2 ngày làm việc.
>
> Để cuộc trao đổi có cơ sở, anh cho em xin ba thông tin: sản lượng anh dự kiến trong 6 tháng đầu, số điểm bán anh phủ được ở Nghệ An, và anh đang phân phối những dòng nào.
>
> Em cảm ơn anh.

**Kết quả mong đợi, phần 3:** danh sách 2 việc trình chủ doanh nghiệp, kèm 3 thông tin cần thu thập từ anh Phát trước khi trình.

**Nói với lớp:** "Dừng ở đây một phút. Đây là chỗ tôi muốn cả lớp nhớ nhất buổi hôm nay.

Đề nghị của anh Phát nghe rất hợp lý. Anh là đại lý, đơn to nhất bảng, xin thêm vài phần trăm và xin độc quyền một tỉnh. Một sale non tay sẽ gật. Một agent không có hàng rào cũng sẽ gật, mà tệ hơn: nó gật bằng một con số nghe rất chuyên nghiệp, kiểu 52% hoặc 'độc quyền trong 12 tháng với cam kết doanh số'. Con số đó không có trong bất kỳ file nào các bạn đưa cho nó. Nó tự chế ra.

Và độc quyền khu vực không phải chuyện chiết khấu. Ký độc quyền Nghệ An nghĩa là 3 năm sau muốn bán cho ai khác ở tỉnh đó cũng không được. Đó là quyết định của chủ doanh nghiệp, không phải của sale, càng không phải của agent.

Nên trong ba file skill của các bạn, file nào cũng phải có một mục tên là ranh giới. Liệt kê thẳng ra: cái gì agent được trả lời, cái gì agent phải dừng. File chính sách của Thảo An có sẵn mục 'Điều CHƯA có chính sách' với bốn dòng: độc quyền khu vực, chiết khấu vượt 48%, ký gửi, chi phí hỗ trợ marketing tại điểm bán. Bốn dòng đó là hàng rào.

Để ý thêm một chi tiết: agent không chỉ từ chối. Nó trả lời trọn phần trả lời được, nói rõ phần nào phải chờ, hẹn mốc 2 ngày, và xin thêm ba thông tin để lần trình có cơ sở. Từ chối mà vẫn đẩy được deal đi tiếp. Đó là khác biệt giữa 'agent biết dừng' và 'agent bị liệt'."

## 26:00 đến 33:00 · Proposal và bảng báo giá cho L04

**Thao tác:** vẫn phiên đó. Đây là lúc lớp thấy đầu ra của skill này thành đầu vào của skill kia: bảng điểm đã nằm trong `bang-diem-lead.md`, Claude đọc lại, không ai phải dán.

```
Soạn proposal hợp tác sỉ cho L04 Chuỗi Beauty House, 6 cửa hàng, TP.HCM.
Người nhận: anh Tuấn, bộ phận mua hàng. Quy trình duyệt 3 tuần.

Dàn ý 6 phần, độ dài 3 đến 5 trang:
1. Vì sao Thảo An hợp với tệp khách của Beauty House
2. Ba SKU và đối tượng da phù hợp
3. Bảng báo giá theo chính sách, có ví dụ giỏ hàng cụ thể
4. Điều khoản: thanh toán, vận chuyển, đổi trả, hỗ trợ bán hàng
5. Lộ trình triển khai khớp quy trình duyệt 3 tuần
6. Bước tiếp theo

Ràng buộc cứng:
- MỌI con số phải truy được về chinh-sach-gia-si.md hoặc san-pham-thao-an.md.
- Không cam kết công dụng ngoài phần "Công dụng ghi trên nhãn".
- Không dùng từ trong danh sách "Điều KHÔNG được nói".
- Cuối proposal liệt kê mọi chỗ [CẦN XÁC NHẬN] và mọi chỗ [SUY LUẬN].
```

**Kết quả mong đợi, phần bảng báo giá.** Chiếu riêng phần này lên và soi cùng lớp. Giỏ hàng đề xuất: 20 sản phẩm mỗi cửa hàng, 6 cửa hàng, tổng 120 sản phẩm. Rơi vào mức **Sỉ lớn** (100 đến 299 sản phẩm), chiết khấu **42%**.

| SKU | Số lượng | Giá lẻ | Giá sỉ lớn (-42%) | Thành tiền |
|---|---|---|---|---|
| Serum rau má B5 | 60 | 320.000đ | 185.600đ | 11.136.000đ |
| Kem nghệ mật ong | 36 | 250.000đ | 145.000đ | 5.220.000đ |
| Mặt nạ đất sét trà xanh | 24 | 180.000đ | 104.400đ | 2.505.600đ |
| **Tổng** | **120** | 32.520.000đ | | **18.861.600đ** |

Kèm điều khoản, chép đúng từ chính sách: chuyển khoản 100% trước khi giao; miễn phí vận chuyển vì đơn trên 30 sản phẩm; đổi trả hàng lỗi sản xuất báo trong 7 ngày; được cấp bộ ảnh sản phẩm và nội dung mẫu vì từ mức Sỉ cơ bản trở lên.

**Nói với lớp:** "Rà bảng này với tôi. Ba mức giá 185.600, 145.000, 104.400 nằm nguyên trong cột 'Sỉ lớn' của file chính sách, không phải agent tự tính lại. Con số 120 sản phẩm là suy luận của agent về cơ cấu giỏ hàng, nên nó phải nằm ở mục [SUY LUẬN] cuối proposal, và trong email phải viết là 'ví dụ giỏ hàng' chứ không phải 'đơn hàng của anh'.

Bây giờ tôi làm bài kiểm tra 30 giây mà tôi muốn các bạn làm với mọi proposal."

```
Liệt kê MỌI con số xuất hiện trong proposal vừa rồi.
Mỗi con số ghi rõ lấy từ đâu: tên file và dòng nào.
Con số nào bạn tự tính hoặc tự suy thì ghi [SUY LUẬN].
Con số nào không truy được nguồn thì ghi [BỊA] và đề xuất xóa.
```

**Nói với lớp:** "Nếu cột [BỊA] có bất kỳ dòng nào, proposal đó không được gửi. Bước này mất 30 giây và nó cứu các bạn khỏi việc cam kết bằng con số không tồn tại với một chuỗi 6 cửa hàng."

## 33:00 đến 35:00 · Chốt và giao việc

Lưu proposal lại trước khi chốt: `Lưu proposal này thành proposal-L04.md trong thư mục làm việc.` Chỉ cho lớp thấy thư mục giờ có thêm 2 file mới và 3 file skill.

Tóm 5 câu:

1. Người đặt tiêu chí và trọng số, agent chỉ áp công thức. Đó là lý do bảng điểm giải thích được khi sếp hỏi.
2. Cột độ tin cậy quan trọng ngang cột điểm. Bảng nào 10 dòng đều tin cậy Cao là bảng đang bịa.
3. Email cá nhân hóa là email che tên đi vẫn nhận ra của ai.
4. Chạm điều chưa có chính sách thì dừng và xin ý kiến. Từ chối mà vẫn đẩy deal đi tiếp.
5. Ba việc đóng thành ba file skill. Hôm nay mất công viết một lần, tuần sau gõ một câu là chạy lại được, và buổi 6 gom cả ba vào bộ bàn giao.

Giao việc: mở `workbook-hoc-vien.md`, làm hết 8 bước trong 65 phút. Ai chưa có lead thật thì dùng nguyên bộ Thảo An, làm được đủ 7 sản phẩm. Nhắc trước một câu: lưu đủ 3 file skill rồi hãy làm, và mỗi skill chạy trong một phiên riêng. Nhồi cả ba vào một phiên là đến câu thứ 30 agent quên bảng tiêu chí.
