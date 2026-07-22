# Rubric chấm sản phẩm cuối khóa: AI Agent cho Sale & Marketing

Chấm bộ sản phẩm buổi 6. Sáu tiêu chí, mỗi tiêu chí 3 mức, tổng 18 điểm.

**Công bố cho học viên ngay lúc giao bài ở đầu buổi 6, không phải lúc trả bài.** Rubric giấu đi thì nó chỉ là công cụ chấm. Đưa sớm thì nó thành hướng dẫn làm bài, và cả lớp biết mình phải nhắm tới đâu.

---

## Sản phẩm phải nộp

Năm thứ, nộp vào nhóm lớp trước 22 giờ ngày học buổi 6. Ai chưa xong thì được thêm 5 ngày, xem phần làm lại ở cuối file.

| # | Sản phẩm | Dạng nộp |
|---|---|---|
| 1 | **Claude Skill hoàn chỉnh**, đóng gói cả bộ việc Sale và Marketing | File `SKILL.md`, hoặc ảnh chụp toàn bộ nội dung file |
| 2 | **AI Agent Playbook** | File văn bản hoặc PDF |
| 3 | **Bộ tài sản 5 buổi đã sắp xếp** | Ảnh chụp cây thư mục, hoặc link thư mục chia sẻ |
| 4 | **Bản ghi màn hình demo 5 phút** | Video, hoặc trình bày trực tiếp trong khối demo chéo của buổi 6 |
| 5 | **Kế hoạch triển khai 14 ngày** | Bảng 4 cột: ngày, việc, người làm, kết quả cần thấy |

Nộp thiếu một trong năm thứ thì tiêu chí tương ứng chấm mức 1 điểm, không hoãn chấm.

---

## Bảng chấm

| Tiêu chí | 1 điểm: Chưa đạt | 2 điểm: Đạt | 3 điểm: Tốt |
|---|---|---|---|
| **1. Skill có đủ bốn phần** | Skill chỉ có các bước làm việc. Thiếu ít nhất hai trong bốn phần: vai trò, tiêu chuẩn đầu ra, ranh giới không được vượt, cách xử lý khi thiếu dữ liệu. | Có đủ bốn phần. Tiêu chuẩn đầu ra viết bằng số hoặc bằng thứ đếm được, ví dụ "bài dưới 250 chữ, có 1 hook, có 1 lời kêu gọi". Ranh giới ghi ra được ít nhất 3 điều cấm cụ thể. | Như mức 2, và có **tiêu chuẩn riêng cho từng loại đầu ra**: bài social, tin nhắn inbox, email chào sỉ, proposal, brief hình ảnh, mỗi loại một bảng chuẩn riêng. |
| **2. Skill chống bịa** | Chạy phép thử ở mục dưới: agent điền một con số hoặc một chi tiết không có trong dữ liệu. Hoặc Skill không có mục nào nói về việc thiếu dữ liệu thì làm gì. | Chạy phép thử: cả 3 câu hỏi đều trả về "chưa đủ dữ liệu" kèm tên nguồn cần bổ sung. Skill có ghi rõ quy tắc gắn nhãn `[DATA THẬT]` và `[SUY LUẬN]`. | Như mức 2, và mọi đầu ra của Skill đều tự liệt kê ở cuối: câu nào là `[DATA THẬT]`, câu nào là `[SUY LUẬN]`. Học viên chỉ ra được ít nhất một lần trước đây agent đã bịa, và chỉ được đúng dòng đã thêm vào Skill để chặn. |
| **3. Skill chạy ngoài bối cảnh gốc** | Đưa một yêu cầu chưa từng chạy trong khóa, Skill ra kết quả sai giọng, dính từ cấm, hoặc lệch hẳn tiêu chuẩn đầu ra do chính học viên viết. | Đưa một yêu cầu chưa từng chạy trong khóa, kết quả đối chiếu đúng bảng tiêu chuẩn đầu ra do chính học viên viết, không phải sửa tay. | Như mức 2, và **một học viên khác cầm Skill chạy trên máy mình**, ra kết quả tương đương, không phải hỏi lại người viết câu nào. Có ảnh chụp kết quả của người đó. |
| **4. Playbook bàn giao được** | Không có Playbook, hoặc Playbook chỉ liệt kê tên công cụ và các bước bấm. | Playbook trả lời được đủ 4 câu: làm theo thứ tự nào; đầu ra thế nào là đạt; agent không được làm gì; nhìn vào số nào để biết có tác dụng. Mỗi bước ghi rõ đầu vào và đầu ra. | Như mức 2, và có thêm mục xử lý khi agent ra sai, ghi theo ba mức: sửa prompt, bổ sung dữ liệu, dừng và báo người phụ trách. Có ghi rõ ai dùng được Playbook này và cần biết gì trước. |
| **5. Bộ tài sản tìm được** | Tài sản còn nằm rải rác trong nhiều cửa sổ chat, nhiều thư mục, hoặc thiếu tài sản của từ hai buổi trở lên. | Có một thư mục gốc đặt tên thương hiệu. Người chấm đọc tên 3 tài sản bất kỳ trong `00-tong-quan/chuan-dau-ra.md`, học viên mở được cả 3, mỗi file dưới 10 giây. | Như mức 2, và có một file mục lục ở thư mục gốc, liệt kê từng tài sản kèm đường dẫn và một dòng nói file đó dùng vào việc gì. |
| **6. Demo 5 phút và kế hoạch 14 ngày** | Demo quá 5 phút. Hoặc demo mở đầu bằng tên công cụ và cách bấm, không nêu kết quả. Hoặc kế hoạch 14 ngày thiếu cột, hoặc có dòng bỏ trống cột người làm. | Demo dưới 5 phút có bấm giờ, mở đầu bằng kết quả đã ra được, tên công cụ nói sau. Kế hoạch 14 ngày đủ 4 cột ngày, việc, người làm, kết quả cần thấy, không dòng nào bỏ trống. | Như mức 2, và cột "kết quả cần thấy" ghi bằng con số đo được, ví dụ "9 bài đã lên lịch", "20 lead đã chấm điểm". Demo có nêu ít nhất một con số so sánh trước và sau, ví dụ thời gian làm một bài từ 45 phút xuống 12 phút. |

---

## Phép thử tiêu chí 2: hỏi điều dữ liệu không trả lời được

Đây là tiêu chí phân biệt khóa này với các khóa dạy mẹo prompt, nên chấm phải làm đúng cách, không chấm bằng cách đọc file Skill.

**Cách chạy, mất 3 phút mỗi học viên:**

1. Người chấm ngồi cạnh, hoặc học viên chia sẻ màn hình.
2. Học viên mở một cuộc trò chuyện mới trong thư mục làm việc của mình, chạy Skill.
3. Người chấm đọc **ba câu hỏi** dưới đây. Học viên gõ nguyên văn vào, không sửa chữ nào.

Ba câu hỏi cho học viên chạy trên case Thảo An:

```
Ngân sách quảng cáo tháng trước của thương hiệu là bao nhiêu?
Giá trị đơn hàng trung bình của kênh Shopee là bao nhiêu?
Thời gian phản hồi trung bình cho tin nhắn inbox Facebook là bao lâu?
```

Học viên chạy trên thương hiệu thật của mình thì người chấm đổi ba câu, theo đúng nguyên tắc: **hỏi ba con số mà hồ sơ trong thư mục làm việc ghi rõ là chưa có.** Trước khi chấm, người chấm mở hồ sơ của học viên ra, chọn ba mục còn trống.

**Cách chấm:**

| Kết quả | Điểm tiêu chí 2 |
|---|---|
| Có bất kỳ câu nào trả về một con số, một khoảng, hoặc một mức "tham khảo của ngành" | 1 điểm, Chưa đạt |
| Cả ba câu trả về "chưa đủ dữ liệu", có nêu tên nguồn cần bổ sung, và Skill có quy tắc gắn nhãn | 2 điểm, Đạt |
| Như trên, cộng thêm phần tự liệt kê `[DATA THẬT]` và `[SUY LUẬN]` ở cuối mọi đầu ra, và học viên chỉ được đúng dòng đã thêm vào Skill để chặn | 3 điểm, Tốt |

**Không có ngoại lệ nào cho tiêu chí này.** Agent điền bừa một con số nghe hợp lý là chưa đạt, dù năm tiêu chí còn lại đều tốt. Lý do: con số đó học viên sẽ mang đi báo cáo sếp, hoặc đưa vào proposal gửi khách. Cho qua ở đây là để lại rủi ro thật cho việc thật của họ.

---

## Phép thử tiêu chí 3: đưa cho người khác chạy

Đây là tiêu chí bàn giao, và nó cũng phải chấm bằng cách chạy, không chấm bằng cách đọc.

**Mức 2 điểm, chấm trong khối demo chéo của buổi 6:**

1. Người chấm đưa một đề chưa từng chạy trong khóa. Ví dụ đề cho case Thảo An: *"Viết 3 tin nhắn Zalo gửi các spa đã mua một lần và ba tháng nay chưa quay lại."* Đề này chưa có trong bất kỳ buổi nào.
2. Học viên chạy Skill của mình trên đề đó.
3. Người chấm mở bảng tiêu chuẩn đầu ra do **chính học viên** viết trong Skill, đối chiếu từng dòng.
4. Đạt khi kết quả khớp bảng tiêu chuẩn đó mà không phải sửa tay.

**Mức 3 điểm, chấm chéo trong cặp:**

1. Học viên A gửi file Skill cho học viên B ngồi cặp.
2. B chép vào thư mục làm việc của B, chạy trên đề của B.
3. B **không được hỏi A câu nào** trong lúc chạy.
4. Kết quả của B đối chiếu đúng bảng tiêu chuẩn đầu ra trong Skill của A thì A được 3 điểm. B chụp màn hình kết quả làm bằng chứng.

Nếu B phải hỏi A dù chỉ một câu để chạy được, đó là dấu hiệu Skill còn thiếu một phần mà A đang giữ trong đầu. Ghi lại đúng câu hỏi đó vào phiếu phản hồi, đó là thứ A cần bổ sung.

---

## Ngưỡng đạt

| Kết quả | Điều kiện |
|---|---|
| **Đạt loại tốt** | Tổng từ 15 trên 18 trở lên, **và** không tiêu chí nào ở mức 1 điểm, **và** tiêu chí 2 đạt tối thiểu 2 điểm |
| **Đạt** | Tổng từ 12 trên 18 trở lên, **và** không tiêu chí nào ở mức 1 điểm, **và** tiêu chí 2 đạt tối thiểu 2 điểm |
| **Chưa đạt** | Tổng dưới 12, **hoặc** có bất kỳ tiêu chí nào ở mức 1 điểm, **hoặc** tiêu chí 2 chỉ được 1 điểm |

**Hai điều kiện chặn, không được bỏ:**

**Điều kiện chặn 1: không tiêu chí nào ở mức 1 điểm.** Một học viên có thể đóng gói rất gọn, viết Playbook rất kỹ, demo rất hay, nhưng bộ tài sản vẫn nằm rải rác không tìm ra. Tổng của người đó có thể lên 13 điểm. Người đó chưa bàn giao được cho ai cả, và chính họ hai tháng nữa cũng không tìm lại được file của mình. Cho qua là cho qua một hệ thống không dùng tiếp được.

**Điều kiện chặn 2: tiêu chí 2 phải từ 2 điểm.** Đây là điều kiện chặn nặng hơn điều kiện 1, và nó chỉ áp cho một tiêu chí duy nhất. Lý do đã nói ở trên: agent bịa số là thứ gây thiệt hại thật, không phải thứ trừ điểm cho đẹp bảng.

---

## Phiếu phản hồi trả về cho học viên

Mỗi bài trả về một phiếu như dưới, gửi trong vòng 3 ngày sau buổi 6. Trả về mỗi con số thì học viên vẫn không biết phải sửa gì.

```
SẢN PHẨM CUỐI KHÓA: [tên thương hiệu học viên làm]
Mã học viên: [bốn số cuối điện thoại]

Tiêu chí 1, Skill đủ bốn phần:         [1 / 2 / 3]
Tiêu chí 2, Skill chống bịa:           [1 / 2 / 3]
Tiêu chí 3, chạy ngoài bối cảnh gốc:   [1 / 2 / 3]
Tiêu chí 4, Playbook bàn giao được:    [1 / 2 / 3]
Tiêu chí 5, bộ tài sản tìm được:       [1 / 2 / 3]
Tiêu chí 6, demo và kế hoạch 14 ngày:  [1 / 2 / 3]

Tổng: [x]/18     Kết quả: [Đạt loại tốt / Đạt / Chưa đạt]

Giữ nguyên: [một câu, nêu đúng một thứ làm tốt, gọi tên cụ thể]
Sửa trước tiên: [một câu, nêu đúng một việc làm được ngay để lên mức trên]
```

**Chỉ nêu một thứ cần sửa.** Học viên sửa được một thứ là tiến bộ thật. Đọc năm thứ thì bỏ luôn.

Ví dụ đã điền:

```
SẢN PHẨM CUỐI KHÓA: Spa Hạ Vy, dịch vụ chăm sóc da
Mã học viên: 4821

Tiêu chí 1, Skill đủ bốn phần:         3
Tiêu chí 2, Skill chống bịa:           2
Tiêu chí 3, chạy ngoài bối cảnh gốc:   2
Tiêu chí 4, Playbook bàn giao được:    2
Tiêu chí 5, bộ tài sản tìm được:       3
Tiêu chí 6, demo và kế hoạch 14 ngày:  2

Tổng: 14/18     Kết quả: Đạt

Giữ nguyên: phần tiêu chuẩn đầu ra chị viết riêng cho tin nhắn inbox và
cho email chào sỉ, mỗi loại một bảng. Đó là chỗ hiếm người trong lớp làm
được, và cũng là chỗ giúp bạn nhân sự mới của chị dùng được ngay.

Sửa trước tiên: cột "kết quả cần thấy" trong kế hoạch 14 ngày của chị
đang ghi "tăng tương tác" ở 6 dòng. Đổi thành con số đếm được, ví dụ
"9 bài đã lên lịch trên fanpage" hoặc "15 tin nhắn đã gửi cho khách cũ".
Ngày 14 nhìn vào là biết ngay xong hay chưa xong.
```

---

## Chấm lại và làm lại

**Chưa đạt thì được làm lại một lần trong vòng 5 ngày.** Chấm lại đúng rubric này, không hạ chuẩn. Nói rõ điều này lúc giao bài ở đầu buổi 6, không nói lúc trả bài.

Học viên làm lại chỉ phải sửa những tiêu chí bị 1 điểm. Các tiêu chí đã từ 2 điểm giữ nguyên, không chấm lại.

**Nếu lần hai vẫn chưa đạt:** ghi vào `danh-gia/diem-danh.md` là chưa đạt, kèm một dòng nói tiêu chí nào vướng. Không kéo dài thêm lần ba. Học viên đó được mời vào buổi hỏi đáp sau một tháng, và được ưu tiên hỏi trước.

---

## Chấm chéo để kiểm rubric

Trước khi dùng chính thức, đưa cùng một bài cho hai người chấm độc lập. Lệch quá 1 điểm ở một tiêu chí nghĩa là ô mô tả còn mơ hồ, phải viết lại bằng hành vi cụ thể hơn.

Với lớp 20 người, khối demo chéo của buổi 6 chỉ có 10 phút, nên giảng viên không chấm hết được tại lớp. Cách chạy thực tế:

| Việc | Ai làm | Khi nào |
|---|---|---|
| Tiêu chí 3 mức 3, chạy chéo trong cặp | Học viên chấm cho nhau, theo mẫu ở trên | Trong khối demo chéo, buổi 6 |
| Tiêu chí 6, bấm giờ demo 5 phút | Bạn cùng cặp bấm giờ và ghi vào phiếu | Trong khối demo chéo, buổi 6 |
| Tiêu chí 2, phép thử ba câu hỏi | Giảng viên, đi từng người | Trong khối hoàn thiện và nộp, buổi 6 |
| Tiêu chí 1, 4, 5 | Giảng viên, đọc file đã nộp | Trong 3 ngày sau buổi 6 |

Học viên chấm chéo phải cầm rubric trong tay, không chấm bằng cảm nhận. Phát bản rút gọn gồm đúng bảng 6 tiêu chí, in một mặt A4, hoặc dán link vào khung chat.

---

## Kiểm rubric trước khi phát

- [x] Đủ 6 tiêu chí, mỗi tiêu chí 3 mức
- [x] Có tiêu chí chống bịa, chấm bằng cách chạy phép thử, không chấm bằng cách đọc file
- [x] Có tiêu chí bàn giao, chấm bằng cách đưa người khác chạy
- [x] Mọi ô mô tả bằng hành vi nhìn thấy được hoặc đếm được trên bài nộp
- [x] Mức 3 viết theo kiểu "như mức 2, và thêm...", người chấm không phải đọc lại từ đầu
- [x] Có ngưỡng đạt và hai điều kiện chặn
- [x] Có mẫu phiếu phản hồi, và phiếu chỉ nêu một thứ cần sửa
- [x] Có quy định làm lại, ghi rõ số ngày và số lần
- [x] Không có dấu gạch ngang dài
- [ ] Đã chấm chéo thử trên một bài thật, hai người chấm lệch không quá 1 điểm ở mỗi tiêu chí

Dòng cuối chưa tick được vì chưa có bài thật. Chạy chấm chéo ngay ở lớp đầu tiên, rồi sửa lại ô nào hai người chấm lệch nhau.
