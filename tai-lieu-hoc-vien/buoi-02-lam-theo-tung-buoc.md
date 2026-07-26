# Buổi 2: Làm theo từng bước

> Cách dùng file này: mỗi phần có hai khúc. Khúc **Lý thuyết** đọc để hiểu mình sắp làm gì và vì sao, có ví von cho dễ nhớ. Khúc **Thao tác** là các bước có sẵn prompt, cứ copy dán vào Claude.
>
> Làm lần lượt, không nhảy cóc. Bước sau dùng kết quả bước trước.
>
> Trước khi bắt đầu: mở Claude Desktop, bấm tab **Code**, mở đúng thư mục làm việc của bạn (thư mục đã tạo ở buổi 1, ví dụ `thao-an-marketing`).
>
> Năm phần, đi từ dễ tới khó:
> - Phần A: dạy Claude biết bạn là ai (CLAUDE.md)
> - Phần B: dựng cấu trúc thư mục cho cả khóa
> - Phần C: ghi mục lục để Claude tìm file nhanh
> - Phần D: đóng gói một việc thành nút bấm (skill)
> - Phần E: đội quân AI (agent, subagent, agent team, token)

---

## PHẦN A. Dạy Claude biết bạn là ai

### Lý thuyết

Hình dung bạn vừa tuyển một cộng tác viên rất giỏi, nhưng mới nhận việc sáng nay. Bạn chưa kịp nói gì đã bắt bạn ấy viết bài bán hàng ngay. Bài viết ra sai không phải vì bạn ấy dở, mà vì **chưa ai đưa cho bạn ấy tờ giới thiệu**: công ty bán gì, cho ai, giọng viết thế nào, từ nào cấm dùng.

Claude lúc mới mở ra cũng đúng như cộng tác viên đó. Nó thông minh, nhưng chưa biết gì về bạn.

**Tờ giới thiệu ấy, trong Claude Code, chính là file `CLAUDE.md`.** Bạn để nó ngay trong thư mục làm việc. Mỗi lần mở phiên, việc đầu tiên Claude làm là đọc nó, y như nhân viên mới tới bàn là cầm tờ giới thiệu đọc trước. Bạn không phải kể lại bối cảnh mỗi lần nữa.

Hai điều cần nhớ:

- **Chỉ đưa vào thứ luôn đúng cho mọi việc.** Bạn là ai, bán gì, giọng thế nào, từ cấm. Còn quy trình cho từng việc cụ thể thì để dành cho skill ở Phần D.
- **Phép thử một câu:** viết xong bài nào, thử thay tên thương hiệu của bạn bằng tên một hãng bất kỳ. Nếu câu vẫn đúng, tức là câu đó chung chung, chưa dùng được. Bài tốt phải gắn chặt với chính thương hiệu bạn.

Một hiểu lầm hay gặp: nhiều người tưởng viết vào `CLAUDE.md` là Claude tuân tuyệt đối như luật. Không phải. Nó là gợi ý rất mạnh mà Claude đọc trước và bám theo, nhưng vẫn có thể lỡ tay sai, nhất là khi bạn viết mơ hồ. Nên viết rõ, và vẫn phải duyệt kết quả.

### Thao tác

**Bước 1. Chứng minh Claude đang chưa biết gì về bạn**

Để làm gì: thấy tận mắt vấn đề trước khi chữa.

Gõ vào Claude:
```
Viết cho tôi một bài đăng Facebook bán hàng cho sản phẩm chính của tôi.
```

Bạn sẽ thấy: một bài chung chung, sai giọng, có khi bịa công dụng. Thử áp phép thử một câu: thay tên thương hiệu vào, bài vẫn đúng, tức là nó chưa biết gì về bạn.

---

**Bước 2. Nhờ Claude phỏng vấn rồi viết hồ sơ thương hiệu**

Để làm gì: tạo file `CLAUDE.md`. Bạn không tự gõ, để Claude hỏi rồi nó viết.

Gõ vào Claude:
```
Tôi muốn bạn viết cho tôi một file CLAUDE.md, đặt ngay trong thư mục này.
Đây là hồ sơ để bạn đọc trước mọi việc tôi giao.

Trước khi viết, hãy phỏng vấn tôi. Hỏi từng câu một, chờ tôi trả lời rồi mới
hỏi câu tiếp:
1. Tôi là ai, bán gì, cho khách nào.
2. Ba việc tôi làm đi làm lại mỗi tuần.
3. Giọng văn của tôi: xưng hô thế nào, có từ nào cấm dùng.
4. Tôi đăng hoặc gửi nội dung ở kênh nào.

Hỏi xong, tóm tắt lại cho tôi xác nhận. Tôi đồng ý rồi bạn mới viết file.
Viết ngắn, dưới 80 dòng.
```

Bạn sẽ thấy: Claude hỏi bạn từng câu, xong viết file `CLAUDE.md` trong thư mục.

Mẹo: trả lời thật, cụ thể. Đừng nói "giọng chuyên nghiệp", hãy nói "xưng shop, gọi khách là bạn, không dùng từ trị bệnh".

---

**Bước 3. Kiểm tra Claude giờ đã hiểu bạn chưa**

Để làm gì: thấy sự khác biệt so với Bước 1.

Gõ vào Claude:
```
Đọc lại file CLAUDE.md trong thư mục này, rồi viết lại cho tôi bài đăng
Facebook bán hàng cho sản phẩm chính. Viết đúng giọng và đúng thông tin
trong hồ sơ của tôi.
```

Bạn sẽ thấy: bài lần này khác hẳn, đúng giọng, đúng sản phẩm. Cùng một Claude, cùng một câu lệnh, khác nhau ở chỗ nó có tờ giới thiệu hay không. Đây là khoảnh khắc quan trọng nhất buổi.

---

## PHẦN B. Dựng cấu trúc thư mục cho cả khóa

### Lý thuyết

Bây giờ Claude đã biết bạn là ai. Việc tiếp theo là **chia phòng cho ngôi nhà.**

Cả khóa này kéo dài 6 buổi. Bạn sẽ tạo ra rất nhiều thứ: hồ sơ sản phẩm và bảng giá, review và tin nhắn khách, bài viết nháp và bài đã đăng, kế hoạch chiến dịch, ảnh và tài liệu. Nếu tất cả nằm chung một chỗ, thư mục sẽ thành một đống lộn xộn. Bạn tìm không ra, và Claude cũng phải mò.

Cách làm đúng là dựng sẵn **một cấu trúc thư mục chuẩn ngay bây giờ**, mỗi loại đồ một phòng. Các buổi sau cứ bỏ đồ vào đúng phòng là xong. Dựng một lần, dùng cho cả khóa.

Đây là cấu trúc đề xuất cho người làm sale và marketing:

```
thu-muc-cua-ban/
├── CLAUDE.md              tờ giới thiệu thương hiệu (đã có ở Phần A)
├── .claude/
│   ├── skills/            các skill bạn lập (Phần D)
│   └── agents/            các trợ lý riêng bạn lập (Phần E)
├── 01-san-pham/          hồ sơ sản phẩm, bảng giá, chính sách sỉ
├── 02-khach-hang/        review, tin nhắn, bình luận, insight khách
├── 03-noi-dung/
│   ├── nhap/             bài đang soạn
│   └── da-dang/          bài đã đăng, để tra lại
├── 04-chien-dich/        kế hoạch và lịch nội dung
└── 05-tai-lieu/          ảnh, brief, file khác
```

Đánh số 01 tới 05 để các phòng luôn xếp đúng thứ tự, dễ nhìn.

### Thao tác

**Bước 4. Nhờ Claude dựng toàn bộ cấu trúc thư mục**

Để làm gì: tạo sẵn các phòng cho cả khóa, chỉ một lần.

Gõ vào Claude:
```
Tạo giúp tôi cấu trúc thư mục chuẩn cho công việc marketing của tôi, ngay
trong thư mục làm việc này. Gồm các thư mục sau, thư mục nào chưa có thì tạo,
đã có thì giữ nguyên:

- .claude/skills
- .claude/agents
- 01-san-pham
- 02-khach-hang
- 03-noi-dung/nhap
- 03-noi-dung/da-dang
- 04-chien-dich
- 05-tai-lieu

Trong mỗi thư mục 01 tới 05, tạo một file ghi-chu.md ngắn một dòng, nói thư
mục đó dùng để chứa gì, để sau này tôi khỏi quên. Xong liệt kê lại cây thư
mục cho tôi xem.
```

Bạn sẽ thấy: Claude tạo đủ các thư mục và liệt kê lại cây thư mục. Từ giờ mỗi loại tài liệu có chỗ riêng.

Mẹo: nếu bạn đã có sẵn file hồ sơ sản phẩm nằm lộn ở ngoài, nhờ thêm `Chuyển file san-pham-cua-toi.md vào thư mục 01-san-pham giúp tôi.`

---

## PHẦN C. Ghi mục lục để Claude tìm file nhanh

### Lý thuyết

Bạn vừa chia phòng xong. Nhưng Claude chưa biết phòng nào chứa gì, trừ khi bạn nói cho nó. Nếu bạn nhờ "lấy bảng giá sỉ" mà không chỉ phòng, nó vẫn phải mở từng phòng để tìm. Vừa chậm, vừa tốn, đôi khi mở nhầm.

Cách chữa: **dán sơ đồ các phòng ngay ở cửa ra vào.** Cửa ra vào ở đây chính là `CLAUDE.md`, vì Claude đọc file này đầu mỗi phiên. Bạn viết vào đó vài dòng mô tả phòng nào chứa gì, thế là nó biết đường đi ngay từ đầu.

Lưu ý một hiểu lầm: nhiều người nghĩ phải tạo một file mục lục riêng, kiểu `index.md`. Không cần. File riêng thì Claude không tự đọc. Viết thẳng vào `CLAUDE.md` mới là chỗ nó luôn đọc.

### Thao tác

**Bước 5. Thêm mục lục cấu trúc thư mục vào CLAUDE.md**

Gõ vào Claude:
```
Quét lại các thư mục vừa tạo trong thư mục làm việc này. Sau đó thêm vào
CLAUDE.md một mục tên "Cấu trúc thư mục", ghi mỗi thư mục một dòng kèm một
câu nói nó chứa gì, dùng khi nào. Chỉ ghi những thư mục có thật.
```

Bạn sẽ thấy: Claude thêm mục "Cấu trúc thư mục" vào `CLAUDE.md`, khớp với các phòng bạn vừa dựng ở Phần B.

---

**Bước 6. Thử xem Claude có tìm đúng phòng không**

Gõ vào Claude:
```
Nếu bây giờ tôi nhờ bạn cập nhật bảng giá sỉ, bạn sẽ mở file trong thư mục
nào, vì sao? Và nếu tôi nhờ xem lại các bài đã đăng thì bạn vào thư mục nào?
```

Bạn sẽ thấy: Claude trả lời đúng tên thư mục, không phải mò. Đó là tác dụng của mục lục vừa thêm.

---

## PHẦN D. Đóng gói một việc thành nút bấm

### Lý thuyết

Có những việc bạn làm đi làm lại mỗi tuần: viết bài bán hàng, soạn email chào sỉ, trả lời tin nhắn hỏi giá. Mỗi lần lại phải dặn Claude từ đầu, mất công, mà kết quả không đều tay.

**Skill là cách đóng gói một việc một lần**, sau đó gọi một câu là nó làm đúng chuẩn. Giống viết sẵn một công thức nấu ăn: lần sau cứ theo công thức, không phải nghĩ lại từng bước.

Phân biệt skill với `CLAUDE.md` cho khỏi lẫn:
- `CLAUDE.md` nói bạn **là ai**. Nó luôn đúng cho mọi việc.
- Skill nói cách **làm một việc**. Nó chỉ được gọi ra khi bạn cần đúng việc đó.

Điểm quan trọng về nơi cất: skill để ở `.claude/skills/<tên>/SKILL.md` **ngay trong thư mục làm việc** (chính là phòng bạn dựng ở Phần B). Hai lý do: một, để skill gắn với đúng dự án này; hai, để sau này đưa lên mạng chia cho đồng đội được. Skill để lung tung nơi khác thì không gắn dự án, không chia được.

Và một mẹo hay nhất khi viết skill: bắt bước đầu tiên luôn là **kiểm tra đủ thông tin, thiếu thì hỏi lại, không tự bịa**. Nhờ vậy skill không bao giờ chế ra số liệu hay giá cả.

### Thao tác

**Bước 7. Hỏi Claude nên đóng gói việc nào**

Để làm gì: bạn không phải tự đoán. Claude đã đọc hồ sơ của bạn, để nó gợi ý.

Gõ vào Claude:
```
Đọc file CLAUDE.md của tôi. Trong các việc tôi làm hàng tuần, việc nào đáng
đóng gói thành một skill nhất, vì sao? Đề xuất giúp tôi tên skill (viết không
dấu, nối bằng gạch nối) và một dòng mô tả ngắn nó dùng khi nào.
```

Bạn sẽ thấy: Claude chỉ ra một việc cụ thể, đặt sẵn tên và mô tả.

---

**Bước 8. Lập skill, đặt đúng trong thư mục của bạn**

Gõ vào Claude (đổi tên skill thành cái Claude gợi ý):
```
Tạo cho tôi một skill mới, đặt tại đường dẫn:
.claude/skills/ten-skill-cua-toi/SKILL.md
ngay trong thư mục làm việc này.

File mở đầu bằng phần frontmatter kẹp giữa hai dòng ba dấu gạch, gồm 2 dòng:
- name: ten-skill-cua-toi
- description: viết rõ skill này làm gì, nêu 3 lúc tôi sẽ gọi nó ra.

Phần dưới ghi các bước làm việc đó. Bước 1 luôn là kiểm tra đủ thông tin,
thiếu thì hỏi lại tôi, không tự bịa. Đọc CLAUDE.md để lấy giọng và từ cấm.
Cuối cùng cho một ví dụ mẫu hoàn chỉnh.
```

Bạn sẽ thấy: Claude báo đã tạo file `SKILL.md` trong `.claude/skills/`. Skill nằm ngay trong thư mục dự án.

---

**Bước 9. Chạy thử skill**

Gõ vào Claude (đổi tên skill cho đúng):
```
Dùng skill ten-skill-cua-toi làm cho tôi một kết quả.
```

Bạn sẽ thấy: nếu skill viết đúng, Claude hỏi lại các thông tin còn thiếu thay vì bịa. Trả lời nó, rồi nó ra kết quả đúng chuẩn.

Nếu nó viết luôn mà không hỏi: gõ `Sửa skill: bước 1 phải kiểm tra đủ thông tin, thiếu thì dừng và hỏi tôi.` Rồi chạy lại.

---

## PHẦN E. Đội quân AI: agent, subagent, agent team

### Lý thuyết

Đây là phần khái niệm. Ta dùng một hình ảnh duy nhất cho dễ nhớ: **một công ty thu nhỏ.**

**Agent là một nhân viên.** Từ đầu buổi tới giờ, mỗi lần bạn làm việc với Claude trong tab Code, bạn đang có một nhân viên: nó tự đọc tài liệu, tự làm, mang kết quả về. Bạn đã dùng cả buổi rồi, giờ chỉ đặt tên cho nó là agent.

**Subagent là một trợ lý phụ.** Khi có việc phụ nặng, ví dụ đọc 30 review rồi tóm tắt, nhân viên chính không tự ôm hết. Nó thuê một trợ lý phụ làm mảng đó trong phòng riêng, xong chỉ mang bản tóm tắt về. Bàn của nhân viên chính vẫn gọn. Vì sao đáng dùng: giữ phần trò chuyện chính của bạn sạch sẽ, và tiết kiệm tiền vì trợ lý đọc đống tài liệu trong phòng riêng, không chất hết vào phiên chính.

Có hai cách dùng trợ lý phụ:
- **Nhờ nhanh bằng lời:** cần lúc nào nói lúc đó, không lưu lại. Hợp việc làm một lần.
- **Lập sẵn một trợ lý riêng:** tạo một file định nghĩa, đóng gói một loại trợ lý dùng nhiều lần, ví dụ trợ lý chuyên nghiên cứu đối thủ. Giống tuyển hẳn một nhân viên có chức danh, khác với thuê thời vụ.

Nói cho gọn: **lập agent** là tạo một file định nghĩa một loại trợ lý. **Subagent** là khi trợ lý đó chạy thật. Cùng một thứ, một cái là bản mô tả, một cái là lúc làm việc.

**Agent team là cả một đội.** Khi việc lớn cần nhiều người bàn với nhau, ví dụ soát một chiến dịch từ ba góc cùng lúc, thì cần một đội. Khác trợ lý phụ ở chỗ: các thành viên **nói chuyện trực tiếp với nhau** và chia một bảng việc chung, chứ không chỉ báo về sếp. Lưu ý thật: agent team hiện **còn là tính năng thử nghiệm**, tốn nhiều tiền vì mỗi thành viên là một Claude riêng, và đôi khi kẹt. Trong buổi này bạn **xem giảng viên demo**; muốn tự thử thì để về nhà.

**Token là tiền công.** Nhân viên, trợ lý, cả đội, ai làm cũng tốn công. Công tính theo số chữ họ đọc và viết, đơn vị là token. Thứ bạn gửi đi rẻ hơn thứ Claude viết ra nhiều lần, nên phần đắt là khi bảo nó viết dài. Và tiếng Việt tốn token hơn tiếng Anh vì có dấu. Cuối phần này ta xem cách đo.

### Thao tác

**Bước 10. Nhờ một trợ lý phụ theo cách nhanh (bằng lời)**

Để làm gì: dùng subagent tức thời, không cần lập file.

Gõ vào Claude:
```
Dùng một trợ lý phụ đọc giúp tôi tất cả các file trong thư mục này, rồi chỉ
trả về đúng một đoạn tóm tắt 5 dòng: thư mục này đang có gì, dùng cho việc gì.
```

Bạn sẽ thấy: Claude báo nó dùng một trợ lý phụ, và chỉ mang về 5 dòng tóm tắt, không đổ hết nội dung file ra màn hình.

---

**Bước 11. Lập sẵn một trợ lý riêng dùng nhiều lần (tạo file agent)**

Để làm gì: đóng gói một loại trợ lý bạn sẽ dùng đi dùng lại. Ví dụ trợ lý nghiên cứu đối thủ. File agent nằm trong thư mục làm việc, cùng chỗ với skill, ở `.claude/agents/`.

Gõ vào Claude:
```
Tạo cho tôi một agent mới, đặt tại đường dẫn:
.claude/agents/nghien-cuu-doi-thu.md
ngay trong thư mục làm việc này.

Phần frontmatter kẹp giữa hai dòng ba dấu gạch, ghi:
- name: nghien-cuu-doi-thu
- description: dùng khi cần tìm hiểu đối thủ, xem họ bán gì, mạnh yếu chỗ nào.
- tools: Read, Grep, Glob, WebSearch, WebFetch

Phần dưới viết hướng dẫn cho trợ lý này: nhiệm vụ là nghiên cứu đối thủ trong
ngành của tôi, chỉ đọc và tìm kiếm, không sửa file của tôi, và luôn ghi rõ
nguồn thông tin lấy từ đâu.
```

Bạn sẽ thấy: Claude tạo file `.claude/agents/nghien-cuu-doi-thu.md`. Từ giờ bạn có một trợ lý chuyên nghiên cứu, gọi lúc nào cũng được.

---

**Bước 12. Gọi trợ lý vừa lập ra làm việc**

Gõ vào Claude:
```
Nhờ trợ lý nghien-cuu-doi-thu tìm giúp tôi 3 thương hiệu cùng ngành đang bán
chạy, mỗi thương hiệu nêu họ mạnh ở điểm nào, rồi tóm tắt về cho tôi.
```

Bạn sẽ thấy: Claude gọi đúng trợ lý bạn đã lập, nó đi nghiên cứu trong phòng riêng, mang kết quả gọn về.

Mẹo: nếu Claude không tự gọi đúng, gõ thẳng `Dùng agent nghien-cuu-doi-thu để...`.

---

**Bước 13. Xem một đội làm việc (agent team, chỉ xem demo)**

Để làm gì: hiểu khi nào cần cả đội. Phần này **giảng viên demo, bạn xem**. Muốn tự thử thì làm ở nhà, vì đây là tính năng thử nghiệm và tốn tiền gấp mấy lần.

Trước hết bật tính năng, nhờ Claude làm giúp:
```
Tạo giúp tôi file .claude/settings.json trong thư mục này, bên trong bật
tính năng agent team bằng dòng cấu hình:
{ "env": { "CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS": "1" } }
```

Rồi giao việc cho một đội ba người:
```
Spawn 3 trợ lý làm việc song song để soát chiến dịch quảng cáo của tôi từ
ba góc:
1. Một người soi đúng luật: có vi phạm quy định quảng cáo mỹ phẩm, có dùng
   từ cấm như trị bệnh không.
2. Một người soi đúng brand: có sai giọng thương hiệu, sai hình ảnh không.
3. Một người soi đúng khách: nội dung có trúng nỗi đau khách không.
Mỗi người báo cáo riêng, sau đó tổng hợp lại cho tôi một bản kết luận nên
sửa gì.
```

Bạn sẽ thấy: Claude tạo một đội, chia việc, ba trợ lý làm song song rồi gộp kết quả. Bấm `Ctrl+T` để thấy bảng việc của đội.

Nhớ: việc thường thì một nhân viên. Việc phụ nặng thì thêm một trợ lý. Việc lớn nhiều góc thì cả đội, và đội thì để dành vì còn thử nghiệm.

---

**Bước 14. Xem mình đã tốn bao nhiêu token**

Gõ vào ô lệnh của tab Code:
```
/context
```

Bạn sẽ thấy: một bảng cho biết phần nào đang chiếm nhiều token. (Nếu không chạy, thử `/usage` hoặc `/cost`. Tên lệnh có thể khác theo phiên bản.)

Sau đó gõ vào Claude:
```
Đoạn văn tiếng Việt này tốn khoảng bao nhiêu token, và nếu dịch sang tiếng
Anh thì tốn bao nhiêu? So sánh giúp tôi:
[dán một đoạn khoảng 100 chữ của bạn vào đây]
```

Bạn sẽ thấy: bản tiếng Việt tốn nhiều token hơn bản tiếng Anh cùng nội dung. Đó là do dấu tiếng Việt.

---

**Bước 15. Ba mẹo tiết kiệm token (chỉ đọc)**

1. Giữ `CLAUDE.md` ngắn, dưới 80 dòng. Vì nó được đọc lại mỗi phiên.
2. Việc phụ nặng thì giao trợ lý phụ như Bước 10, đừng chất hết vào phiên chính.
3. Phiên chạy lâu quá thì gõ `/compact` để dọn bớt, hoặc mở phiên mới cho việc mới.

---

## Xong buổi 2, kiểm lại bạn đã có

Tự tay làm được:
- [ ] File `CLAUDE.md` cho công việc thật, có mục "Cấu trúc thư mục"
- [ ] Cấu trúc thư mục chuẩn cho cả khóa, đủ các phòng 01 tới 05 và `.claude/`
- [ ] Một skill mới trong `.claude/skills/` của thư mục bạn, đã chạy thử được
- [ ] Đã nhờ một trợ lý phụ, và đã lập một agent riêng trong `.claude/agents/`
- [ ] Biết xem token bằng `/context` và một mẹo tiết kiệm

Hiểu để dùng sau:
- [ ] Phân biệt được: một nhân viên, một trợ lý phụ, cả một đội, khi nào cần cái nào
- [ ] Biết agent team còn là tính năng thử nghiệm, chưa dùng cho việc thật

Thiếu mục nào thì làm lại đúng bước đó. Buổi sau ta đổ dữ liệu khách thật vào thư mục `02-khach-hang` và học cách biến nó thành insight.
