# OUTLINE BUỔI 2: Dạy Claude hiểu việc của bạn, và biết dùng cả đội AI

> **Một câu về buổi này:** hết buổi, anh chị dạy được Claude viết đúng giọng thương hiệu mình, đóng gói một việc lặp lại thành nút bấm, và hiểu khi nào cần cả một đội AI làm việc chứ không chỉ một mình.
>
> **Nguyên tắc thiết kế:** người CHƯA BIẾT GÌ cũng theo được. Mỗi khối mở bằng một nỗi đau anh chị tự cảm, rồi khái niệm mới hiện ra như lời giải. Không định nghĩa khô, không nhảy cóc, không bày hết mọi thứ ra từ đầu.
>
> **Bốn phần, xây dần:** (1) CLAUDE.md cho công việc thật; (2) mục lục để Claude tìm file nhanh; (3) lập skill của riêng mình; (4) hiểu đội AI: agent, trợ lý phụ, đội nhóm, và tiền công token.

---

## Cách buổi này đi dần, không nhồi

Buổi được xây theo hai nửa rõ ràng:

- **Nửa đầu (K1 tới K3): TỰ TAY LÀM.** Anh chị viết CLAUDE.md thật, lập skill thật, mang về dùng ngày mai. Đây là phần chắc nền.
- **Nửa sau (K4): HIỂU ĐỂ DÙNG KHÔN.** Agent, subagent, agent team, token dạy bằng một ẩn dụ duy nhất là một công ty thu nhỏ, mở rộng dần từ cái anh chị đã biết. Phần này nghe và xem là chính, không luyện tay, để không quá sức người mới.

Đẩy skill lên GitHub để buổi sau, vì với lớp chưa quen máy, riêng việc đăng nhập GitHub lần đầu đã cần một mạch riêng. Buổi 2 tập trung hiểu cho vững.

---

## Nhịp 150 phút

| Khối | Nội dung | Phút |
|---|---|---|
| K0 | Mở đầu: một nỗi đau chung | 10 |
| K1 | CLAUDE.md: dạy Claude biết mình là ai | 35 |
| K2 | Thêm mục lục để Claude tìm file nhanh | 12 |
| Giải lao | | 10 |
| K3 | Skill: đóng gói một việc lặp lại thành nút bấm | 38 |
| K4 | Đội quân AI: agent, trợ lý phụ, đội nhóm, tiền công | 35 |
| K5 | Chốt và giao bài | 10 |

Phần tự tay làm nặng nhất (lập skill) đặt ngay sau giải lao lúc não còn khỏe. Phần khái niệm (K4) để cuối, nhẹ nhàng, chỉ nghe và xem.

---

## K0. Mở đầu: một nỗi đau chung (10 phút)

**Câu hỏi khơi:** "Ai từng nhận một bài AI viết, đọc xong thấy đúng ngữ pháp mà sai hẳn giọng thương hiệu mình?"

- Gần như cả lớp giơ tay. Đó là vấn đề của buổi.
- Đặt đích bằng lời thường: hôm nay dạy Claude hiểu đúng việc của anh chị, để nó làm như một nhân viên đã quen việc. Cuối buổi anh chị còn biết cách cho nó thuê thêm trợ lý khi việc nhiều.
- KHÔNG định nghĩa gì. KHÔNG liệt kê "hôm nay học mấy thứ". Chỉ khơi nhu cầu.

---

## K1. CLAUDE.md: dạy Claude biết mình là ai (35 phút)

**Câu hỏi dẫn:** Vì sao cùng một câu lệnh, Claude viết cho người này hay, người kia dở?

- **Cho gặp nỗi đau (demo):** giảng viên nhờ Claude viết một bài bán hàng trong thư mục TRỐNG, không có CLAUDE.md. Ra bài chung chung, sai giọng, có khi bịa. Cả lớp soi chỗ sai.
- **Khái niệm nảy ra:** CLAUDE.md là gì, bằng một ví von duy nhất: tờ giới thiệu để trước mặt người mới vào làm. Chỉ một ý. KHÔNG nói phân cấp, KHÔNG nói token ở đây.
- **Khoảnh khắc "à ra thế":** chạy lại cùng câu lệnh trong thư mục CÓ CLAUDE.md. Bài ra khác hẳn, đúng giọng. Lớp thấy tận mắt.
- **Học viên tự làm (phần chính):** nhờ Claude phỏng vấn mình rồi viết CLAUDE.md cho công việc THẬT. Không tự gõ, để Claude hỏi từng câu.
- **Chốt, ghi một câu:** CLAUDE.md chỉ chứa thứ luôn đúng cho mọi việc của mình.

Không giả định anh chị đã hiểu CLAUDE.md từ buổi 1. Ai buổi 1 chỉ làm theo cho xong thì đây là lần đầu thật sự hiểu.

---

## K2. Thêm mục lục để Claude tìm file nhanh (12 phút)

**Câu hỏi dẫn:** Thư mục có 20 file, anh chị nhờ "lấy bảng giá sỉ" mà không nói file nào, chuyện gì xảy ra?

- **Nỗi đau:** Claude quét mò, mở nhầm, chậm.
- **Khái niệm nảy ra:** thêm 5 tới 10 dòng mô tả thư mục vào chính CLAUDE.md. Nói thẳng: KHÔNG cần tạo file mục lục riêng, vì Claude đọc CLAUDE.md mỗi phiên là biết đường ngay.
- **Học viên làm:** thêm mục "Cấu trúc thư mục" vào CLAUDE.md, thử hỏi "cập nhật hồ sơ sản phẩm thì mở file nào".

Phần mở rộng nhẹ của K1, cùng một file, nên ngắn.

---

## GIẢI LAO (10 phút)

---

## K3. Skill: đóng gói một việc lặp lại thành nút bấm (38 phút, đỉnh của buổi)

**Câu hỏi dẫn:** Việc nào anh chị làm đi làm lại mỗi tuần mà lần nào cũng phải dặn Claude từ đầu?

- **Nỗi đau:** dặn lại mỗi lần, mất công, kết quả không đều.
- **Khái niệm nảy ra:** skill là đóng gói quy trình một lần, sau gọi một câu là nó làm đúng chuẩn. Giải thích lại từ đầu bằng ví von công thức nấu ăn. Không giả định đã hiểu skill từ buổi 1.
- **Nhờ Claude làm cố vấn:** hỏi thẳng "với công việc của tôi, tôi nên đóng gói việc nào thành skill, đặt tên gì". Học viên dùng Claude vạch việc cho mình.
- **Lập skill, chạy thử, có giờ sửa lỗi:** đây là lý do K3 được 38 phút. Người mới lập skill lần đầu sẽ vấp, cần thời gian sửa cùng giảng viên.
- **Khoảnh khắc "à ra thế":** gõ một câu ngắn, skill chạy ra đúng bài như mình dặn.

---

## K4. Đội quân AI: agent, trợ lý phụ, đội nhóm, tiền công (35 phút)

Cả khối dùng MỘT ẩn dụ xuyên suốt: **một công ty thu nhỏ.** Bắt đầu từ cái anh chị đã biết, mở rộng dần. Phần này nghe và xem là chính, không luyện tay.

**Câu hỏi dẫn:** "Nãy giờ anh chị làm việc với Claude như giao việc cho đúng một nhân viên. Vậy khi việc phình to quá sức một người thì sao?"

**1. Agent là gì (đã biết rồi, chỉ gọi tên):** "Từ đầu khóa tới giờ, mỗi lần anh chị mở tab Code làm việc với Claude, anh chị đang có một nhân viên: nó tự đọc tài liệu, tự làm, mang kết quả về. Cái đó gọi là agent. Anh chị đã dùng cả buổi rồi, giờ chỉ đặt tên cho nó."

**2. Subagent là trợ lý phụ (mở rộng một bước):**
- **Nỗi đau thật:** "Anh chị nhờ Claude vừa đi nghiên cứu đối thủ, vừa viết bài, nó làm một lúc thành ra rối, lẫn lộn." Đây là đau có thật, không phải bịa.
- **Khái niệm:** nhân viên chính thuê một trợ lý phụ làm mảng nghiên cứu trong phòng riêng, xong chỉ mang bản tóm tắt về. Bàn của nhân viên chính vẫn gọn.
- **Demo cho xem:** giảng viên nhờ Claude dùng một trợ lý phụ đọc mấy file rồi tóm tắt. Chỉ vào chỗ nó chỉ mang về kết luận. Không bắt lớp làm.

**3. Agent team là một đội (mở rộng bước nữa, chỉ hiểu):**
- **Khái niệm:** nhiều nhân viên nói chuyện trực tiếp với nhau, chia một bảng việc chung, khác trợ lý phụ ở chỗ họ bàn với nhau chứ không chỉ báo về sếp.
- **Ví dụ nghề:** soát một chiến dịch lớn trước khi tung, từ ba góc cùng lúc: một người soi đúng luật, một soi đúng brand, một soi đúng insight, rồi bàn ra một kết luận chung.
- **Ghi rõ hai lần:** đây là tính năng THỬ NGHIỆM, hôm nay chỉ hiểu để sau này dùng, không thực hành.

**4. Token là tiền công (khép ẩn dụ):**
- "Nhân viên, trợ lý, cả đội, ai làm cũng phải trả công. Công tính theo số chữ họ đọc và viết. Đó là token."
- Một mẹo duy nhất cần nhớ: viết gọn thì rẻ, tiếng Việt tốn hơn tiếng Anh.
- Cho Claude ước lượng token một đoạn văn để lớp thấy con số thật, rồi thôi.

Kết khối: "Việc thường thì một nhân viên. Việc phụ nặng thì thêm trợ lý, dùng được ngay. Việc lớn nhiều góc thì cả đội, để dành vì còn thử nghiệm. Và cái gì cũng tốn công, nên viết gọn."

---

## K5. Chốt và giao bài (10 phút)

**Ba thứ tự tay làm mang về (bảng):**
1. CLAUDE.md viết cho công việc thật, có mục cấu trúc thư mục.
2. Một skill của riêng mình, đã chạy thử được.
3. Một mẹo tiết kiệm token.

**Một thứ hiểu để dùng sau:** khi nào cần trợ lý phụ, khi nào cần cả đội.

**Ba nguyên tắc chống bịa** nhắc lại: chỉ dùng dữ liệu mình cấp; gắn nhãn [DATA THẬT] và [SUY LUẬN]; người duyệt cuối.

**Mồi cho buổi sau:** "Skill của anh chị đang nằm trên máy. Buổi sau ta học cách cất nó lên mạng để không sợ mất và chia cho đồng đội." Đây là chỗ GitHub sẽ vào, đúng lúc học viên đã có skill để mà tiếc nếu mất.

---

## Điều đã cân nhắc kỹ

- **Giữ agent, subagent, agent team** theo yêu cầu của giảng viên, nhưng đóng khung là "hiểu để dùng khôn", dạy bằng ẩn dụ công ty để người mới theo được. Không biến thành bài thực hành, vì hai vòng phản biện cảnh báo phần này dễ làm lớp quá tải nếu bắt luyện tay.
- **Agent team ghi rõ là tính năng thử nghiệm**, chỉ hiểu khái niệm.
- **Đẩy GitHub dời buổi sau.** Nếu giảng viên muốn giữ trong buổi 2, cần cắt bớt phần khác vì 150 phút không đủ cho cả GitHub lẫn K4.

---

## Câu hỏi còn treo cho giảng viên

1. K4 giữ ở mức "nghe và xem" như trên có đúng ý không, hay muốn cho lớp thực hành thử tạo một subagent?
2. GitHub để buổi sau, hay vẫn muốn ghép vào buổi 2 và cắt bớt phần nền?
