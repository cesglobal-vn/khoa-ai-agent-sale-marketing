# Buổi 6 · Claude Skill và AI Agent cuối khóa

**Phụ đề:** Đóng gói thành hệ thống dùng được hoặc bán được
**Thời lượng:** 2,5 giờ
**Agent xây được:** không thêm agent mới. Buổi này đóng gói cả 5 agent (Customer Insight, Content Engine, Outbound, Proposal, Closer) cộng luồng tự động hóa của buổi 5 thành một hệ thống bàn giao được.
**File đi kèm:** [demo-script.md](demo-script.md) · [workbook-hoc-vien.md](workbook-hoc-vien.md) · [system-prompt.md](system-prompt.md)

> Ý chính của buổi: 5 buổi qua học viên đã làm ra hơn 40 đầu ra, nhưng chúng đang nằm rải rác trong nhiều thư mục, nhiều cửa sổ chat, và phần lớn cách làm vẫn nằm trong đầu họ. Buổi 1 họ đã viết được một skill cho riêng mình dùng. Hôm nay gom cả bộ thành một Skill và một Playbook mà người khác cầm lên dùng được, không cần hỏi lại người viết. Đó là lúc nó thành tài sản, không còn là kỹ năng cá nhân.

---

## Mục tiêu buổi

Hết 2,5 giờ, học viên phải:

- Nâng skill viết ở buổi 1 thành một Skill bàn giao được: phủ cả bộ việc Sale và Marketing, có vai trò, tiêu chuẩn đầu ra đo được, ranh giới không được vượt và cách xử lý khi thiếu dữ liệu.
- Chứng minh được Skill chạy được ngoài bối cảnh gốc: đưa một yêu cầu mới chưa từng làm, Skill vẫn ra kết quả đúng chuẩn.
- Có AI Agent Playbook: tài liệu để đồng nghiệp hoặc khách hàng vận hành hệ thống mà không cần hỏi lại người viết.
- Sắp xếp toàn bộ tài sản 5 buổi vào một cấu trúc thư mục tìm được trong 10 giây.
- Trình bày được hệ thống trong 5 phút cho sếp hoặc khách, nói bằng kết quả chứ không bằng tên công cụ.
- Có kế hoạch triển khai 14 ngày ghi rõ ngày, việc, người làm, kết quả cần thấy.

---

## Học viên chuẩn bị gì trước buổi

Buổi này không tạo ra dữ liệu mới. Nó gom cái đã có. Thiếu đầu vào là ngồi làm lại, mất thời gian của cả lớp.

| Việc | Bắt buộc | Ghi chú |
|---|---|---|
| Thư mục làm việc của buổi 1, mở được bằng tab Code | Có | Nơi chứa `CLAUDE.md` và toàn bộ file nền của thương hiệu |
| Bộ tài sản buổi 1 | Có | `CLAUDE.md` (câu định vị, 3 thông điệp, 5 nỗi đau, giọng văn, từ cấm), hồ sơ sản phẩm `san-pham-thao-an.md`, Memory đã bật, skill `viet-bai-ban-hang` chạy được, 3 bài bán hàng, 10 hook, 10 CTA, 1 kết nối MCP |
| Bộ tài sản buổi 2 | Có | Bảng insight có trích dẫn, persona, 5 content angle, 5 bài social, 3 brief hình ảnh, 3 visual |
| Bộ tài sản buổi 3 | Có | Lead scoring 10 lead, 10 email, 10 tin nhắn, kịch bản gọi 5 phút, 10 kịch bản xử lý từ chối, proposal nháp |
| Bộ tài sản buổi 4 | Có | Campaign brief, lịch 14 ngày, 10 bài social, 3 email nurturing, landing page section, 3 video script, carousel, 5 brief hình ảnh |
| Bộ tài sản buổi 5 | Có | Automation map, bảng quản lý, luồng post bài chạy được, mẫu thông báo, checklist kiểm soát rủi ro |
| System prompt của 5 agent buổi 2 tới buổi 5 | Có | Buổi này rút ruột chúng, gộp cùng skill `viet-bai-ban-hang` của buổi 1, thành một Skill |
| Máy tính, một thư mục trống đặt tên thương hiệu | Có | Chỗ để gom tài sản |

Nhắn lớp trước buổi 2 ngày: "Mang đủ 5 buổi. Ai thiếu buổi nào thì tối nay chạy lại prompt buổi đó, đừng để sáng mai mới phát hiện."

---

## Timeline 2,5 giờ

| Khối | Thời lượng | Giảng viên làm gì |
|---|---|---|
| **1. Framework** | 20 phút | Giảng 4 phần: `CLAUDE.md` khác `SKILL.md` ở đâu và ba mục buổi 1 chưa dạy; thế nào là quy trình đóng gói được; playbook cần có gì; chọn chỉ số nào để đo. Không mở Claude, chỉ nói và vẽ bảng. |
| **2. Demo thật** | 35 phút | Chạy nguyên [demo-script.md](demo-script.md) trên case Thảo An. Có đoạn thử Skill trên yêu cầu mới, đây là phần quan trọng nhất, nhắc lớp nhìn kỹ. |
| **3. Làm sản phẩm** | 65 phút | Học viên mở [workbook-hoc-vien.md](workbook-hoc-vien.md). 18 phút đầu gom tài sản; 29 phút giữa viết Skill và thử Skill; 18 phút cuối viết Playbook và kế hoạch 14 ngày. Giảng viên đi vòng, nhắc mốc thời gian mỗi 15 phút. |
| **4. Demo chéo** | 10 phút | Đổi khối review thành demo chéo. Chia cặp hoặc nhóm 3. Mỗi người trình bày agent của mình đúng 5 phút, người còn lại chấm theo rubric bên dưới. Giảng viên đi nghe, không cắt ngang. |
| **5. Hoàn thiện và nộp** | 20 phút | Sửa theo góp ý của bạn cùng nhóm, nộp đủ 6 sản phẩm. Giảng viên chấm tại chỗ, kết khóa và bàn giao. |

---

## Nội dung 20 phút Framework

### Phần 1 · `CLAUDE.md` khác `SKILL.md` ở đâu (5 phút)

Mở bằng câu hỏi: "Anh chị nghỉ phép hai tuần. Đồng nghiệp mở thư mục làm việc của anh chị ra. Họ làm được bài đăng đúng chuẩn không?" Phần lớn trả lời không. Vì thư mục có đủ dữ liệu thương hiệu, còn cách làm vẫn nằm trong đầu anh chị.

Vẽ lên bảng:

```
CLAUDE.md                       SKILL.md
= hồ sơ MỘT thương hiệu         = quy trình mang đi được
- Bán gì, bán cho ai            - Các bước làm việc
- Giọng văn, từ cấm             - Tiêu chuẩn đầu ra
- Buộc vào 1 thương hiệu        - Ranh giới không được vượt
- Đổi khách là viết lại từ đầu  - Đưa đồng nghiệp, đưa khách, dùng lại được
```

Nói gọn với lớp: `CLAUDE.md` là hồ sơ của một thương hiệu, đổi thương hiệu là phải viết lại. `SKILL.md` là quy trình làm việc, gói lại rồi mang sang thương hiệu nào cũng chạy.

Ví dụ thực tế cho dễ hình dung: một agency có 8 khách hàng. Họ sẽ có 8 thư mục làm việc, mỗi khách một `CLAUDE.md` riêng. Nhưng chỉ cần 1 bộ skill dùng chung cho cả 8, vì quy trình viết bài giống nhau, chỉ khác dữ liệu. Nhắc lại điều buổi 1 đã nói qua: đặt bộ skill đó ở `~/.claude/skills/` thì mọi thư mục trên máy đều gọi được.

**Không dạy lại cấu trúc file SKILL.md.** Buổi 1 đã dạy kỹ: đường dẫn `.claude/skills/<tên>/SKILL.md`, frontmatter hai dòng `name` và `description`, và vì sao `description` là dòng quan trọng nhất. Bảo lớp mở luôn file `.claude/skills/viet-bai-ban-hang/SKILL.md` của mình ra, để nguyên trên màn hình. Nói: "Hôm nay ta không viết lại từ đầu. Ta nâng cấp cái này."

Chỗ nâng cấp nằm ở đâu, đọc chậm cho lớp ghi. Skill buổi 1 làm được đúng một việc cho đúng một người. Bốn thứ dưới đây là phần buổi 1 chưa có, và cũng là phần khiến người khác cầm lên dùng được:

1. **Vai trò.** Agent này đóng vai ai trong đội, viết bằng một ví von nghề nghiệp. Ví dụ Thảo An: "viết như dược sĩ tư vấn ở quầy thuốc, giải thích thành phần trước, mời mua sau."
2. **Tiêu chuẩn đầu ra cho TỪNG loại đầu ra.** Buổi 1 chỉ có một chuẩn cho bài Facebook. Giờ có bài social, tin nhắn inbox, email chào sỉ, proposal, brief hình ảnh, mỗi loại một chuẩn riêng, viết bằng số.
3. **Ranh giới không được vượt.** Không chỉ là từ cấm. Còn là: mức chiết khấu nào không được tự quyết, việc nào bắt buộc người làm.
4. **Xử lý khi thiếu dữ liệu.** Gặp chỗ trống thì làm gì, theo thứ tự nào, để người dùng sau biết đường xử lý mà không phải gọi điện hỏi anh chị.

Chốt: "Buổi 1 anh chị viết một skill cho riêng mình dùng. Hôm nay anh chị biến cả bộ thành thứ người khác cầm lên là chạy được, kèm playbook, kèm tiêu chuẩn đầu ra, kèm chỉ số đo."

### Phần 2 · Thế nào là một quy trình đóng gói được (5 phút)

Không phải việc nào cũng đóng gói được. Bắt lớp tự kiểm bằng 4 câu hỏi:

1. **Việc này có lặp lại không?** Làm một lần rồi thôi thì không cần Skill. Tuần nào cũng làm thì cần.
2. **Có mô tả được bằng các bước không?** Nếu bạn không nói được bước 1 làm gì, bước 2 làm gì, thì bạn chưa hiểu quy trình của mình, chưa đóng gói được.
3. **Kết quả đúng trông như thế nào?** Không mô tả được đầu ra chuẩn thì không ai kiểm được. Skill sẽ ra hàng nghìn chữ mà không ai biết đạt hay chưa.
4. **Chỗ nào tuyệt đối không được vượt?** Điều cấm nói, số liệu không được bịa, việc không được tự quyết. Ranh giới phải viết ra, không giữ trong đầu.

Nói rõ với lớp: câu 3 và câu 4 là chỗ 90% người viết Skill bỏ qua. Họ viết được các bước, quên viết tiêu chuẩn và ranh giới. Kết quả là Skill chạy ra thứ nhìn giống việc nhưng dùng không được.

Vẽ phép thử một câu để lớp nhớ: "Đưa Skill cho người mới vào công ty tuần đầu. Họ chạy ra kết quả bạn dám gửi khách không? Không thì Skill chưa xong."

### Phần 3 · Playbook cần có gì để người khác dùng mà không cần hỏi lại (5 phút)

Skill là thứ Claude đọc. Playbook là thứ người đọc. Thiếu Playbook, đồng nghiệp có Skill mà vẫn không biết dùng lúc nào, dùng xong kiểm thế nào.

Bảy mục bắt buộc, thiếu mục nào thì người dùng sẽ quay lại hỏi bạn đúng mục đó:

| Mục | Trả lời câu hỏi | Ví dụ Thảo An |
|---|---|---|
| Mục đích | Hệ thống này giải bài toán gì | Ra đủ nội dung và tin nhắn bán hàng cho 3 SKU, không cần thuê thêm người viết |
| Ai dùng | Vị trí nào, cần biết gì trước | Nhân sự content và nhân sự trực inbox. Không cần biết code |
| Quy trình từng bước | Mở cái gì, gõ gì, làm gì tiếp | 6 bước, mỗi bước ghi rõ đầu vào và đầu ra |
| Tiêu chuẩn đầu ra | Thế nào là đạt | Bài dưới 250 chữ, có hook, có CTA, không chứa từ cấm, mọi số liệu có nhãn nguồn |
| Ranh giới không được vượt | Cấm gì | Không nói "trị mụn", không cam kết thời gian, không tự bấm gửi cho khách |
| Chỉ số đo | Nhìn vào đâu biết hệ thống có hiệu quả | Thời gian làm 1 bài, số bài mỗi tuần, tỉ lệ nháp được duyệt lần đầu |
| Xử lý khi agent ra sai | Sai thì làm gì | Ba mức: sửa prompt, bổ sung dữ liệu, dừng và báo người phụ trách |

Nhấn mạnh: Playbook không phải tài liệu trang trí. Nó là thứ học viên bán được cho khách nếu làm agency. Khách không mua prompt, khách mua quy trình có bảo hành.

### Phần 4 · Chọn chỉ số nào để đo (5 phút)

Đo sai chỉ số thì hệ thống chạy tốt mà không ai tin, hoặc chạy dở mà ai cũng khen.

Chia bảng làm 2 cột, viết lên:

**Chỉ số đo được ngay từ tuần 1 (đo quá trình):**
- Thời gian làm ra 1 đầu ra, trước và sau khi dùng hệ thống. Ví dụ 1 bài social từ 45 phút xuống 12 phút.
- Số đầu ra mỗi tuần. Ví dụ từ 3 bài lên 10 bài.
- Tỉ lệ nháp được duyệt ngay lần đầu, không phải sửa lại. Đây là chỉ số cho biết Skill có đủ chuẩn hay chưa.
- Số lần agent bị bắt lỗi bịa. Mục tiêu là 0.

**Chỉ số kinh doanh (đo sau 4 tuần trở đi):**
- Số lead vào mỗi tuần, gắn được nguồn kênh.
- Tỉ lệ lead thành đơn.
- Chi phí trên mỗi lead.
- Doanh thu theo kênh.

Câu cảnh báo cho lớp: "Đừng hứa với sếp là hệ thống này tăng doanh thu trong 2 tuần. Trong 2 tuần bạn chứng minh được thời gian giảm và số lượng tăng. Doanh thu cần thêm chu kỳ. Hứa đúng cái đo được thì lần sau người ta còn tin bạn."

Chốt phần framework, nối sang demo: "Ba nguyên tắc chống bịa các bạn học từ buổi 1 tới giờ vẫn phải nhớ mỗi lần gõ. Hôm nay chúng ta nhét nó vào Skill. Từ lúc đó nó đi theo hệ thống, không phụ thuộc trí nhớ ai nữa. Đây là điểm quan trọng nhất của buổi cuối."

---

## Tổ chức bộ tài sản: cấu trúc thư mục đề xuất

Sau 5 buổi học viên có hơn 40 đầu ra. Không sắp xếp thì buổi thứ 3 sau khóa là không ai tìm được gì.

Đưa cấu trúc này lên màn hình, bắt học viên tạo ngay trong 18 phút đầu khối làm bài:

```
thao-an-ai-system/
├── CLAUDE.md         hồ sơ thương hiệu, Claude tự đọc trước mọi việc
├── .claude/skills/   nơi skill chạy thật, mỗi skill một thư mục con
├── 00-doc-truoc/     playbook.md · ke-hoach-14-ngay.md
├── 01-nen-tang/      san-pham-thao-an · hook-cta · bai-ban-hang-mau
├── 02-khach-hang/    insight-khach-hang · persona · content-angle
├── 03-ban-hang/      lead-scoring · email-va-tin-nhan · kich-ban-goi-va-tu-choi · proposal-mau
├── 04-chien-dich/    campaign-brief · lich-14-ngay · noi-dung-da-kenh/
├── 05-tu-dong-hoa/   automation-map · luong-post-bai · checklist-rui-ro
├── 06-skill/         ban-doc-SKILL.md · tham-chieu/ (mẫu, checklist, dữ liệu nền)
└── 99-luu-tru/       bản nháp cũ, không xóa nhưng không dùng
```

Bốn quy tắc nói cho lớp:

1. Đánh số đầu thư mục để thứ tự không nhảy lung tung.
2. Tên file viết chữ thường, nối bằng gạch nối, nói rõ nội dung. `insight-khach-hang.md` tốt hơn `insight-final-v3.md`.
3. Không dùng chữ "final", "moi", "v2". Bản cũ đẩy vào `99-luu-tru/`.
4. **Phân biệt hai chỗ đặt skill.** Bản chạy thật nằm ở `.claude/skills/<tên-skill>/SKILL.md` ngay trong thư mục gốc, đúng như buổi 1 đã dạy. Thư mục `06-skill/` giữ một bản để người đọc, cộng bộ file tham chiếu. Nói với lớp: "Thư mục bắt đầu bằng dấu chấm bị Windows ẩn đi. Đừng tạo tay, bảo Claude tạo. Còn `06-skill/` là chỗ đồng nghiệp mở ra đọc, không phải chỗ Claude chạy."

---

## Khung demo 5 phút

Học viên trình bày agent của mình. Đúng 5 phút, bấm giờ. Mỗi phút một việc:

| Phút | Nói gì | Sai lầm hay gặp |
|---|---|---|
| **1** | **Bài toán.** Trước đây làm việc này mất bao lâu, ai làm, đau ở chỗ nào. Nói bằng con số. | Kể lể dài dòng về công ty |
| **2** | **Cách làm.** Hệ thống gồm gì, chạy theo mấy bước. Mở sơ đồ, chỉ 3 giây mỗi khối. | Đọc từng dòng system prompt |
| **3** | **Chạy thử.** Gõ một yêu cầu thật, chờ kết quả ra ngay trước mắt người xem. | Chiếu kết quả chuẩn bị sẵn, không dám chạy trực tiếp |
| **4** | **Kết quả.** Đọc to 1 đầu ra tốt nhất. Chỉ ra nhãn nguồn, chỉ ra chỗ ghi "chưa đủ dữ liệu". | Khoe tính năng công cụ thay vì đọc kết quả |
| **5** | **Kế hoạch tiếp.** 14 ngày tới làm gì, ai làm, nhìn vào chỉ số nào để biết ăn thua. | Kết bằng "em xong rồi ạ" |

Nói với lớp trước khi chia nhóm: "Người nghe không quan tâm bạn dùng công cụ gì. Họ quan tâm việc này trước mất 45 phút, giờ mất 12 phút, và kết quả có dám gửi khách không."

---

## Rubric chấm demo

Người cùng nhóm chấm. Thang 2 điểm mỗi tiêu chí, tổng 12 điểm. Ghi vào workbook của người trình bày.

| # | Tiêu chí | 0 điểm | 1 điểm | 2 điểm |
|---|---|---|---|---|
| 1 | **Bài toán rõ** | Không nêu vấn đề | Nêu chung chung | Có con số trước và sau |
| 2 | **Skill chạy được thật** | Không chạy trực tiếp | Chạy nhưng lỗi, phải chữa cháy | Chạy ngay, ra đúng chuẩn |
| 3 | **Chất lượng đầu ra** | Chung chung, thay tên thương hiệu vẫn đúng | Đúng nhưng còn nhạt | Cụ thể, chỉ thương hiệu này viết được |
| 4 | **Ba nguyên tắc chống bịa** | Không thấy đâu | Nhắc miệng nhưng không có trong Skill | Nằm trong Skill, đầu ra có nhãn nguồn |
| 5 | **Playbook bàn giao được** | Không có | Có nhưng thiếu tiêu chuẩn hoặc ranh giới | Đủ 7 mục, người lạ đọc là làm được |
| 6 | **Kế hoạch 14 ngày** | Không có | Có việc nhưng không có người và chỉ số | Đủ ngày, việc, người làm, kết quả cần thấy |

Quy đổi: từ 10 điểm trở lên là đạt. Từ 7 đến 9 là sửa rồi nộp lại trong 20 phút cuối. Dưới 7 là làm lại phần yếu nhất, giảng viên ngồi cùng.

---

## Điểm học viên hay vấp và cách xử lý

**1. Skill viết chung chung nên người khác dùng không ra kết quả.**
Biểu hiện: phần thân Skill ghi "viết bài hay, đúng giọng thương hiệu, thu hút khách hàng". Đưa cho người khác chạy thì ra bài của bất kỳ hãng mỹ phẩm nào.
Xử lý: bắt thay mọi tính từ bằng số hoặc bằng câu kiểm được. "Bài hay" đổi thành "dưới 250 chữ, mở bằng một tình huống da cụ thể, tối đa 2 emoji, kết bằng 1 CTA". Phép thử tại chỗ: đưa Skill cho người bên cạnh chạy thử một yêu cầu. Ra khác nhau nhiều là Skill còn mơ hồ.

**2. Playbook thiếu tiêu chuẩn đầu ra.**
Biểu hiện: Playbook có đủ các bước, nhưng không mục nào nói kết quả đạt trông thế nào. Người dùng chạy xong không biết nên gửi hay nên sửa.
Xử lý: bắt viết bảng 5 dòng "đạt khi" cho từng loại đầu ra chính. Hỏi trực tiếp: "Ai là người bấm nút duyệt? Họ nhìn vào đâu để quyết?" Câu trả lời chính là tiêu chuẩn cần viết.

**3. Demo sa đà khoe công cụ thay vì khoe kết quả.**
Biểu hiện: 5 phút thì 4 phút chiếu giao diện, giải thích chỗ này bấm gì, chỗ kia là file gì. Đến phút cuối mới đọc được nửa bài.
Xử lý: bấm chuông ở phút thứ 2. Bắt chuyển sang chạy thật ngay. Sau demo hỏi lại cả nhóm: "Bạn nhớ được kết quả gì?" Không ai nhớ thì cho làm lại 5 phút.

**4. Skill chỉ chạy đúng trên đúng ví dụ đã demo.**
Biểu hiện: chạy lại đúng yêu cầu trong buổi 4 thì ra đẹp. Đổi sang yêu cầu mới, ví dụ viết bài cho SKU khác hoặc viết tin nhắn cho khách sỉ, thì kết quả lệch chuẩn.
Xử lý: bắt buộc mỗi người chạy 2 phép thử ngoài bối cảnh gốc trước khi nộp. Lệch thì thường do Skill mô tả theo tình huống cụ thể thay vì mô tả theo bước. Sửa bằng cách viết lại các bước ở dạng chung, đẩy phần cụ thể xuống file tham chiếu.

**5. Bỏ ba nguyên tắc chống bịa ra ngoài Skill.**
Biểu hiện: học viên nói "cái đó em nhớ rồi, lúc chạy em tự nhắc". Skill không có dòng nào về nhãn nguồn.
Xử lý: nói thẳng, đây là lỗi nặng nhất của buổi cuối. Trí nhớ không bàn giao được. Bắt dán nguyên khối 3 nguyên tắc vào phần thân Skill, và thêm một dòng vào tiêu chuẩn đầu ra: mọi số liệu phải có nhãn `[DATA THẬT]` hoặc `[SUY LUẬN]`.

**6. Kế hoạch 14 ngày không có tên người, tài sản đổ dồn một thư mục.**
Biểu hiện: cột "ai làm" ghi "team" hoặc để trống; 40 file nằm chung một chỗ, tên kiểu `bai viet moi nhat (2).docx`.
Xử lý: bắt điền tên cụ thể, không có ai khác thì ghi tên mình. Việc không có tên là việc không xảy ra. Bắt tạo đúng 8 thư mục và đổi tên file trong 10 phút. Đây là việc chán nhất buổi nhưng bỏ qua thì Playbook vô dụng.

---

## Sản phẩm nộp cuối buổi

Nộp trong 20 phút cuối. Đúng 6 mục, không thiếu, không thừa:

| # | Sản phẩm | Số lượng | Đạt khi |
|---|---|---|---|
| 1 | Claude Skill hoàn chỉnh | 1 | Nằm đúng ở `.claude/skills/<tên-skill>/SKILL.md`. Đủ 7 mục: vai trò, nguồn dữ liệu, tiêu chuẩn đầu ra cho từng loại, ranh giới không được vượt, quy trình từng bước, xử lý khi thiếu dữ liệu, file tham chiếu. Có 3 nguyên tắc chống bịa nguyên văn trong phần thân |
| 2 | AI Agent Playbook | 1 | Đủ 7 mục: mục đích, ai dùng, quy trình, tiêu chuẩn, ranh giới, chỉ số, xử lý khi sai |
| 3 | Bộ tài sản sắp xếp theo project | 1 | Đúng cấu trúc thư mục, tên file theo quy tắc, mở ra tìm được trong 10 giây |
| 4 | Automation hoặc prototype | 1 | Kế thừa buổi 5, chạy được, có bước người duyệt trước khi gửi hoặc đăng |
| 5 | Demo agent 5 phút | 1 | Đã trình bày và được chấm theo rubric, từ 10 điểm trở lên |
| 6 | Kế hoạch triển khai 14 ngày | 1 | Đủ 4 cột ngày, việc, ai làm, kết quả cần thấy. Có tên người thật |

**Chưa đạt** khi rơi vào một trong các trường hợp:

- Skill không có 3 nguyên tắc chống bịa trong phần thân.
- Skill chạy trên yêu cầu mới thì ra kết quả lệch chuẩn, và học viên chưa sửa.
- Playbook thiếu mục tiêu chuẩn đầu ra hoặc mục ranh giới.
- Kế hoạch 14 ngày không có tên người hoặc không có chỉ số.
- Đầu ra trong demo có số liệu không tìm được trong file nguồn.

---

## Cách kết khóa và bàn giao

Dành 10 phút cuối cùng, sau khi chấm xong.

**Bước 1 · Cho lớp nhìn lại đường đi.** Chiếu bảng 6 buổi. Đọc to danh sách những gì họ đã làm ra: từ một hồ sơ sản phẩm ban đầu, tới hơn 40 đầu ra, tới một Skill đóng gói được. Nói: "Không ai trong phòng này viết một dòng code nào."

**Bước 2 · Nói rõ cái họ mang về là gì.** Ba tầng, viết lên bảng:
- Tầng 1: bộ tài sản dùng ngay được cho 14 ngày tới.
- Tầng 2: Skill và Playbook, cả đội dùng lại được, người mới vào đọc là làm được.
- Tầng 3: nếu làm agency hoặc freelancer, đây là một gói dịch vụ bán được. Khách mua quy trình có tiêu chuẩn, không mua mẹo prompt.

**Bước 3 · Giao việc 14 ngày.** Mỗi người đọc to ngày 1 và ngày 2 trong kế hoạch của mình. Đọc ra miệng thì tỉ lệ làm cao hơn hẳn.

**Bước 4 · Lập nhóm theo dõi.** Hẹn một mốc kiểm lại sau 14 ngày. Mỗi người báo đúng 3 con số: thời gian làm 1 đầu ra, số đầu ra mỗi tuần, tỉ lệ nháp duyệt ngay lần đầu.

**Bước 5 · Nhắc điều cuối.** Câu kết cho cả khóa:

"Hệ thống này không thay bạn ra quyết định. Nó bỏ giúp bạn phần lặp lại, để bạn dồn thời gian vào phần chỉ người làm được: chọn hướng, duyệt nội dung, nói chuyện với khách. Ba nguyên tắc chống bịa giữ nguyên: chỉ dùng dữ liệu bạn cấp, gắn nhãn nguồn, bạn duyệt cuối. Hôm nay ba nguyên tắc đó đã nằm trong Skill của bạn, nên nó không phụ thuộc trí nhớ ai nữa. Đó là khác biệt giữa một người dùng AI giỏi và một đội có hệ thống."

---

CES Global · Creative, Effective, Sustainable
