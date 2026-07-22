# Tài liệu học viên · Buổi 3: Sales Agent

**Khóa:** AI Agent cho Sale & Marketing · CES Global
**Buổi:** 3 trên 6 · 150 phút · **Ngày học:** ______

Đây là bản mang về để tra và làm lại. Bản làm trong lớp là [../workbook/buoi-03-sales-agent.md](../workbook/buoi-03-sales-agent.md).

---

## 1. Buổi này anh chị đã làm gì

Hôm nay anh chị dựng một dây chuyền ba agent cho việc bán hàng, mỗi agent một file skill riêng.

- **`lead-scoring`:** chấm điểm 10 lead theo đúng bộ tiêu chí do chính anh chị đặt, ra bảng có cột độ tin cậy, rồi viết email và tin nhắn bám ghi chú trao đổi thật.
- **`soan-proposal`:** soạn đề xuất hợp tác và bảng báo giá, mọi con số truy được về file chính sách.
- **`theo-duoi-chot-don`:** kịch bản gọi 5 phút và 10 kịch bản xử lý từ chối.

Hai điều quan trọng nhất của buổi: **người định nghĩa tiêu chí, agent chỉ áp công thức**; và **cột độ tin cậy quan trọng ngang cột điểm**. Điểm 51 tin cậy Cao là một việc, điểm 51 tin cậy Thấp là việc khác hẳn.

Ba nhóm việc agent tuyệt đối không được tự quyết: giá và chiết khấu ngoài bảng; cam kết về thời gian giao, công dụng, đổi trả; ưu đãi và điều kiện hợp tác như độc quyền khu vực hay ký gửi.

---

## 2. Bộ prompt copy dùng ngay

**Mỗi nhóm chạy trong một phiên riêng trong tab Code.** Nhồi cả ba vào một phiên là đến câu thứ 30 agent quên bảng tiêu chí của anh chị.

Ba file skill copy từ [../demo/buoi-03/skill-sales-3-agent.md](../demo/buoi-03/skill-sales-3-agent.md), nhờ Claude tạo giùm, đừng tạo thư mục bằng tay.

### NHÓM A · Chấm điểm lead (skill `lead-scoring`)

**A1. Bắt agent tự khai nó thiếu gì**

```
Đọc hồ sơ sản phẩm và danh sách lead trong thư mục làm việc.
Đây là dữ liệu nền. Xác nhận, chưa làm gì thêm.

Xác nhận theo mẫu:
1. Bạn đọc được bao nhiêu lead.
2. Lead nào thiếu thông tin người phụ trách.
3. Ba loại dữ liệu nào KHÔNG có trong file mà việc chấm điểm lead thường cần.
```

Dùng khi: mở phiên mới, trước mọi việc chấm điểm. Agent trả lời "dữ liệu đầy đủ" là agent sắp bịa.

**A2. Chấm điểm 10 lead theo bảng tiêu chí của mình**

Điền bảng tiêu chí trên giấy trước, chưa mở Claude. Bốn tiêu chí, tổng trọng số 100%, mô tả mốc 5, 3, 1 đủ rõ để người khác chấm lại ra cùng kết quả. Bí thì lấy bộ mẫu Thảo An rồi sửa: Quy mô đơn 25%, Độ khớp định vị 25%, Mức độ quan tâm 30%, Khả năng chốt trong 30 ngày 20%.

```
Chấm điểm 10 lead theo ĐÚNG bộ tiêu chí dưới. Không tự thêm, không tự bớt tiêu chí.

[dán nguyên bảng tiêu chí của bạn, có mô tả mốc 5/3/1]

Công thức: Điểm = (A×trọng số + B×trọng số + C×trọng số + D×trọng số) × 20

Xuất bảng markdown, cột:
Lead | Tên | A | B | C | D | Điểm | Nhóm | Độ tin cậy | Lý do một dòng | Việc cần làm tiếp

Quy tắc bắt buộc:
- Tiêu chí nào chấm bằng suy luận thì ghi số kèm dấu * và chú thích cuối bảng.
- Lead có từ 2 tiêu chí trở lên chấm bằng suy luận thì Độ tin cậy = Thấp.
- Nhóm A từ 75 điểm, Nhóm B 60 đến 74, Nhóm C dưới 60.
- KHÔNG bịa doanh số, ngân sách, hay tên người phụ trách.
```

Dùng khi: mỗi lần xuất một đợt lead mới từ CRM hoặc gom từ inbox.

**A3. Lưu bảng thành file để bước sau đọc lại**

```
Lưu bảng này thành bang-diem-lead.md trong thư mục làm việc.
```

Dùng khi: ngay sau A2. Skill `theo-duoi-chot-don` và `soan-proposal` đọc lại chính file này.

### NHÓM B · Email và tin nhắn (skill `lead-scoring`)

Chạy theo lô 3 tới 4 lead một lần, đừng đòi 10 email trong một lượt.

**B1. Email tiếp cận cá nhân hóa**

```
Viết email tiếp cận cho lead [số]: [tên].

Ràng buộc:
- Bám ĐÚNG ghi chú trao đổi của lead này. Ít nhất một câu phải nhắc lại điều họ đã nói hoặc đã làm.
- Dưới 150 từ. Giọng theo phần giọng văn trong CLAUDE.md.
- Chỉ được nhắc mức chiết khấu có trong file chính sách, ghi rõ điều kiện số lượng đi kèm.
- Không dùng từ trong danh sách "Điều KHÔNG được nói".
- Kết bằng MỘT lời đề nghị bước tiếp cụ thể, khác nhau tùy lead.
- Tài liệu nào chưa chắc có sẵn thì ghi [CẦN XÁC NHẬN], không hứa gửi.
- Cuối email liệt kê [DATA THẬT] và [SUY LUẬN].
```

Dùng khi: cần một loạt email mở lời cho danh sách lead vừa chấm điểm.

**B2. Chuyển email thành tin nhắn Zalo hoặc LinkedIn**

```
Chuyển 10 email trên thành tin nhắn Zalo (hoặc LinkedIn nếu lead là doanh nghiệp lớn).

Ràng buộc:
- Tối đa 4 câu. Không xuống dòng nhiều lần.
- Không mở bằng "Chào anh/chị, em là..." rồi mới vào việc. Vào việc từ câu đầu.
- Không dán bảng giá vào tin nhắn. Chỉ nêu MỘT con số hoặc MỘT lợi ích, rồi hỏi.
- Kết bằng một câu hỏi trả lời được bằng một dòng.
- Giữ nguyên chi tiết riêng của từng lead như trong email.
```

Dùng khi: lead ưa nhắn tin hơn email. Chạy sau B1 để giữ được chi tiết riêng.

### NHÓM C · Gọi điện và xử lý từ chối (skill `theo-duoi-chot-don`)

**C1. Kịch bản gọi 5 phút**

```
Viết kịch bản gọi điện 5 phút cho lead nhóm A.

Cấu trúc theo mốc thời gian, mỗi mốc ghi rõ lời thoại nguyên văn:
0:00 đến 0:30  Mở đầu, xin phép, nêu lý do gọi
0:30 đến 1:30  Ba câu hỏi tìm hiểu, kèm mục đích của từng câu
1:30 đến 3:00  Gắn sản phẩm vào điều họ vừa nói, không đọc thuộc lòng tính năng
3:00 đến 4:00  Nêu mức giá và điều kiện đi kèm, chỉ dùng số trong chính sách
4:00 đến 5:00  Chốt bước tiếp theo, xin cam kết nhỏ

Kèm ô "Nếu khách nói X thì rẽ sang" cho 3 tình huống hay gặp nhất.
Viết như lời nói, đọc lên phải giống người. Không viết như văn bản.
```

Dùng khi: mở phiên mới. Skill tự đọc `bang-diem-lead.md` để biết lead nào nhóm A.

**C2. Mười kịch bản xử lý từ chối**

```
Viết 10 kịch bản xử lý từ chối cho ngành [ngành của bạn], bán sỉ cho [loại khách].

Mỗi kịch bản gồm 4 phần:
1. Lời từ chối, viết đúng cách khách hay nói, không viết kiểu sách vở.
2. Điều họ thực sự lo bên dưới câu đó.
3. Câu trả lời, TỐI ĐA 3 câu, câu cuối là một câu hỏi hoặc một đề xuất bước tiếp.
4. Bằng chứng cần có sẵn trong tay khi trả lời.

Ràng buộc: không hứa điều ngoài chính sách. Chạm điều chưa có chính sách thì ghi
"cần xin ý kiến chủ doanh nghiệp".
```

Dùng khi: chuẩn bị cho sale mới nhận việc, hoặc trước một đợt gọi tập trung.

Hai ô phải kiểm kỹ: **ký gửi** và **độc quyền khu vực**. Cả hai nằm trong mục "Điều chưa có chính sách", nên bắt buộc phải có câu xin ý kiến chủ doanh nghiệp. Agent tự hứa được là prompt của anh chị thiếu hàng rào.

### NHÓM D · Proposal (skill `soan-proposal`)

**D1. Soạn proposal cho một lead cụ thể**

```
Soạn proposal hợp tác sỉ cho lead [số]: [tên]. Người nhận: [tên, chức vụ].

Dàn ý 6 phần, 3 đến 5 trang:
1. Vì sao chúng tôi hợp với tệp khách của bên anh/chị
2. Danh mục sản phẩm và đối tượng phù hợp
3. Bảng báo giá theo chính sách, có ví dụ giỏ hàng cụ thể
4. Điều khoản: thanh toán, vận chuyển, đổi trả, hỗ trợ bán hàng
5. Lộ trình triển khai
6. Bước tiếp theo

Ràng buộc cứng:
- MỌI con số phải truy được về file chính sách hoặc hồ sơ sản phẩm.
- Không cam kết công dụng ngoài phần ghi trên nhãn.
- Không dùng từ trong danh sách "Điều KHÔNG được nói".
- Cuối proposal liệt kê mọi chỗ [CẦN XÁC NHẬN] và [SUY LUẬN].
```

Dùng khi: một lead điểm cao. Nêu rõ đang làm lead nào, đừng bảo skill đọc cả 10 lead, proposal sẽ ra chung chung.

**D2. Bài kiểm tra 30 giây, bắt buộc chạy trước khi gửi**

```
Liệt kê MỌI con số xuất hiện trong proposal vừa rồi.
Mỗi con số ghi rõ lấy từ đâu: tên file, dòng nào.
Con số nào bạn tự tính hoặc tự suy thì ghi [SUY LUẬN].
Con số nào không truy được nguồn thì ghi [BỊA] và đề xuất xóa.
```

Dùng khi: mọi lần trước khi gửi proposal hoặc báo giá. Cột `[BỊA]` có bất kỳ dòng nào thì proposal không được gửi.

---

## 3. Sản phẩm buổi 3 anh chị phải có trên máy

| # | Sản phẩm | Nằm ở đâu |
|---|---|---|
| 1 | 3 file skill đã chỉnh theo ngành và chính sách của mình | `.claude/skills/lead-scoring/SKILL.md`, `.claude/skills/soan-proposal/SKILL.md`, `.claude/skills/theo-duoi-chot-don/SKILL.md` |
| 2 | Danh sách 10 lead đủ 6 cột và bảng chính sách giá | Trong thư mục làm việc. Chưa có thì dùng [../demo/thao-an/danh-sach-lead-si.md](../demo/thao-an/danh-sach-lead-si.md) và [../demo/thao-an/chinh-sach-gia-si.md](../demo/thao-an/chinh-sach-gia-si.md) |
| 3 | `bang-diem-lead.md`: 10 lead, có cột độ tin cậy | Trong thư mục làm việc |
| 4 | 10 email cá nhân hóa và 10 tin nhắn | Trong thư mục làm việc |
| 5 | 1 kịch bản gọi 5 phút và 10 kịch bản xử lý từ chối | Trong thư mục làm việc |
| 6 | `proposal-<mã lead>.md`, 3 tới 5 trang, kèm bảng báo giá | Trong thư mục làm việc |

Nộp vào thư mục cá nhân, đặt tên `buoi03-<tên>-<sản phẩm>.md`. Giữ nguyên định dạng bảng, buổi 4 dùng lại.

---

## 4. Checklist tự kiểm

- [ ] Trọng số do tôi đặt, tôi giải thích được vì sao tiêu chí cao nhất lại cao nhất
- [ ] Bảng điểm có ít nhất một ô đánh dấu suy luận. Đếm ra 0 là chắc chắn đang bịa
- [ ] Không phải 10 trên 10 dòng đều tin cậy Cao
- [ ] Không có tên người phụ trách nào do agent tự đặt
- [ ] Đủ 10 email và 10 tin nhắn
- [ ] **Bài kiểm tra che tên:** che hết tên riêng trong 3 email bất kỳ, người khác vẫn đoán được là lead nào. Không đoán được thì đó là email điền tên, viết lại
- [ ] Lời đề nghị bước tiếp khác nhau giữa các lead, không copy chung một câu
- [ ] Mọi mức chiết khấu nhắc trong email đều có trong chính sách, kèm điều kiện số lượng
- [ ] Kịch bản gọi đủ 5 mốc, đọc to lên nghe giống người nói
- [ ] Đủ 10 kịch bản từ chối, mỗi câu trả lời tối đa 3 câu
- [ ] Ô ký gửi và ô độc quyền khu vực đều có câu xin ý kiến chủ doanh nghiệp
- [ ] Proposal đủ 6 phần, đã chạy prompt D2, cột `[BỊA]` trống
- [ ] Cả 3 skill gọi được bằng một câu tự nhiên mà không nhắc tên skill

---

## 5. Việc làm ở nhà trước buổi 4

| # | Việc | Nộp gì | Hạn |
|---|---|---|---|
| 1 | Gửi thật 5 email trong số 10 email vừa viết. Ghi lại ai trả lời, trả lời gì | Bảng 5 dòng: lead, ngày gửi, có trả lời hay không, nội dung trả lời | Trước buổi 4 |
| 2 | Gọi thật 2 lead nhóm A theo kịch bản 5 phút. Ghi lại chỗ nào kịch bản không dùng được | Ghi chú 2 cuộc gọi, kèm 3 câu khách nói mà kịch bản chưa lường | Trước buổi 4 |
| 3 | Đưa bảng tiêu chí chấm điểm cho một đồng nghiệp, nhờ họ chấm lại 2 lead. Lệch quá 10 điểm thì mô tả mốc 5/3/1 chưa đủ rõ, sửa lại | Bảng so hai lần chấm và bản tiêu chí đã sửa | Trước buổi 4 |
| 4 | Bổ sung mục "Điều chưa có chính sách" sau khi gặp câu hỏi thật của khách | Danh sách đã bổ sung | Trước buổi 4 |
| 5 | **Chuẩn bị cho buổi 4:** chọn **một** insight xương sống từ `insight-khach-hang.md`, viết danh sách kênh đang chạy kèm vai trò từng kênh, và mục tiêu bán hàng bằng con số | Ba dòng ghi ra giấy hoặc file, mang vào buổi 4 | Trước buổi 4 |

---

## 6. Bốn lỗi hay gặp khi làm lại ở nhà

| Lỗi | Dấu hiệu anh chị thấy | Cách xử lý |
|---|---|---|
| Để agent tự nghĩ tiêu chí chấm điểm | Gõ "chấm điểm 10 lead này giúp tôi" rồi lấy nguyên kết quả. Lần chạy sau ra bộ tiêu chí khác | Điền xong bảng tiêu chí trên giấy rồi mới mở Claude. Prompt phải chứa nguyên bảng đó. Agent là máy tính, không phải người quyết định |
| Email điền tên, tưởng là cá nhân hóa | 10 email giống hệt, chỉ khác chỗ "Chị Hạnh" và "Chị Lan" | Chơi trò che tên. Bắt buộc mỗi email phải có ít nhất một câu trích thẳng từ ghi chú trao đổi của lead đó |
| Agent bịa giá và điều kiện | Proposal xuất hiện "chiết khấu 45%", "hỗ trợ 50% chi phí biển hiệu", "giao trong 24h" | Chạy prompt D2. Số nào không tìm thấy nguồn thì xóa hoặc thay bằng `[CẦN XÁC NHẬN]`. Đừng bỏ bước này để tiết kiệm 30 giây |
| Skill không được gọi ra | Gõ "chấm điểm giúp tôi" nhưng Claude trả lời như chưa từng đọc file skill | Mở lại `SKILL.md`, viết lại dòng `description` cho sát những chữ anh chị thật sự gõ, nêu ít nhất 3 câu ví dụ. Đây là dòng duy nhất Claude dùng để chọn skill |

---

CES Global · Creative, Effective, Sustainable
