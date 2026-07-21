# Chương trình tổng quan

Khóa **AI Agent cho Sale & Marketing** của CES Global. Sáu buổi, mỗi buổi 2,5 giờ (150 phút), tổng 15 giờ học trực tiếp.

---

## Khóa này giải bài toán gì

Đội sale và marketing đã dùng AI rồi, nhưng kết quả vẫn rời rạc. Bốn khoảng trống hay gặp:

| Nhóm | Vấn đề |
|---|---|
| Marketing | Ra bài đều tay nhưng rời rạc, không bám nỗi đau khách nên dễ chung chung. |
| Sale | Lead có sẵn mà vẫn phân loại tay, chưa biết ưu tiên ai. Email dễ giống thư rác. |
| Quy trình | Mỗi người hỏi AI một kiểu, lưu một nơi, không có chuẩn đầu ra hay cách đo. |
| Quản lý | Muốn đưa AI vào cả sale lẫn marketing nhưng thiếu cách triển khai, nên AI mãi ở mức thử nghiệm. |

Điểm chung: thiếu một **hệ thống** để AI làm việc theo quy trình, không phải thiếu AI viết nội dung.

---

## Nguyên tắc thiết kế chương trình

1. **Mỗi buổi ra một sản phẩm thật.** Không có buổi nào chỉ nghe giảng.
2. **Sản phẩm buổi trước là đầu vào buổi sau.** Nghỉ một buổi là buổi sau hụt nguyên liệu, nên phải học liền mạch.
3. **Học trên dữ liệu của chính học viên.** Chưa có thì dùng case Thảo An, vẫn hoàn thành đủ.
4. **Chống bịa là môn học, không phải lưu ý.** Ba nguyên tắc chống bịa xuất hiện trong mọi buổi và cuối cùng được đóng gói vào Skill.
5. **Đóng gói được, bàn giao được.** Kết thúc không phải một tập tài liệu học, mà là một hệ thống người khác dùng lại được.

---

## Bản đồ 6 buổi

```
Buổi 1  Bốn tầng ngữ cảnh        CLAUDE.md, Skill, Memory, MCP
   |
Buổi 2  Customer Insight Agent   pain có trích dẫn, persona, content angle
   |         \
   |          \
Buổi 3  Sales Agent (3 agent)     Buổi 4  Content Engine Agent
   |    lead scoring, email,              chiến dịch 14 ngày đa kênh
   |    proposal, xử lý từ chối           |
   \                                      /
    \                                    /
Buổi 5  Automation & MCP        nối tất cả thành luồng tự chạy, đăng bài thật
   |
Buổi 6  Claude Skill & Playbook  đóng gói, bàn giao, kế hoạch 14 ngày
```

---

## Chi tiết từng buổi

### Buổi 1 · Cài Claude Code và bốn tầng ngữ cảnh
Buổi nền móng. Học viên cài công cụ rồi đóng gói thương hiệu của mình thành thứ Claude đọc được trước mọi việc, thay vì giải thích lại từ đầu mỗi lần hỏi.

Bốn tầng:
- **Tầng 1 CLAUDE.md:** bản brief thương hiệu, Claude đọc trước mọi việc.
- **Tầng 2 Skill:** quy trình chuẩn cho một đầu việc, ví dụ viết bài bán hàng.
- **Tầng 3 Memory:** sổ bàn giao giữa các phiên làm việc.
- **Tầng 4 MCP:** nối Claude vào Google Drive hoặc Sheet để đọc dữ liệu thật.

Ra: thư mục làm việc, CLAUDE.md (câu định vị, 3 thông điệp, 5 nỗi đau, giọng văn, từ cấm), Memory đã bật, 1 Skill chạy được, 3 bài bán hàng, 10 hook, 10 CTA, 1 kết nối MCP.

Công cụ: Claude Desktop (tab Code) và Git for Windows. Cần tài khoản trả phí. Học viên cài trước ở nhà theo `huong-dan-cai-dat.md`.

### Buổi 2 · Customer Insight Agent
Đọc bình luận, review, tin nhắn để thấy điều khách thật sự quan tâm, rồi biến thành góc nội dung. AI phải dẫn bằng chứng.

Ra: Customer Insight Agent, 5 content angle từ data thật, 5 bài social, 3 brief hình ảnh, 3 visual đăng được.

### Buổi 3 · Sales Agent
Sale biết nên ưu tiên lead nào và mở lời thế nào. Buổi này xây 3 agent nối nhau: Outbound, Proposal, Closer.

Ra: Sales Research Agent, Lead Scoring Sheet 10 lead, 10 email, 10 tin nhắn, kịch bản gọi 5 phút, 10 kịch bản xử lý từ chối, proposal nháp 3-5 trang.

### Buổi 4 · Content Engine Agent
Từ một insight dựng nguyên chiến dịch 14 ngày, đủ bài viết, email, video và carousel.

Ra: Content Engine Agent, campaign brief, lịch 14 ngày, 10 bài social, 3 email nurturing, landing page section, 3 video script, carousel 6-8 slide, 5 brief hình ảnh.

### Buổi 5 · Automation & MCP Mindset
Nối các việc lặp lại thành luồng tự chạy. Đây là buổi duy nhất agent chạm được ra bên ngoài, nên cũng là buổi siết chặt nhất về kiểm soát.

Ra: automation map, bảng quản lý, automation chạy được hoặc prototype, mẫu thông báo, checklist kiểm soát rủi ro.

### Buổi 6 · Claude Skill & Playbook
Đóng gói tất cả thành Skill và Playbook có hướng dẫn, tiêu chuẩn và chỉ số đo.

Ra: Claude Skill hoàn chỉnh, AI Agent Playbook, bộ tài sản theo project, automation, demo agent 5 phút, kế hoạch triển khai 14 ngày.

---

## Ai phù hợp

| Nhóm | Họ cần gì ở khóa này |
|---|---|
| Chủ doanh nghiệp SME | Đưa AI vào việc thật của đội sale và marketing, triển khai được chứ không dừng ở thử nghiệm. |
| Trưởng phòng Sale / Marketing | Một khung rõ ràng để đưa AI vào quy trình và chuẩn hóa đầu ra của team. |
| Nhân sự content, ads, CRM, sales | Làm nhanh hơn mỗi ngày, thực hành ngay trên sản phẩm và dữ liệu của mình. |
| Agency, freelancer, consultant | Đóng gói AI Agent thành dịch vụ để demo, tư vấn hoặc bán. |

Không yêu cầu biết code.

---

## Công cụ dùng trong khóa

**Lõi AI Agent:** Claude Desktop (tab Code), CLAUDE.md, Claude Skills, Memory, MCP và Connector. Cần tài khoản Claude trả phí. Cài thêm Git for Windows.

**Dữ liệu và tự động hóa:** Google Sheet, Airtable, Notion, Make, Zapier, n8n, dữ liệu xuất từ CRM.

**Dữ liệu thật từ mạng xã hội (buổi 2 và 4):** tikhub, lấy bình luận thật, hashtag đang lên, thư viện quảng cáo đối thủ trên TikTok, Instagram, YouTube. Tính tiền theo lượt gọi, học viên tự đăng ký và tự trả phí. Không có vẫn học đủ, dùng dữ liệu case Thảo An thay thế.

**Đăng bài đa kênh (buổi 4 và 5):** aitoearn, đăng và hẹn giờ lên 14 nền tảng gồm Facebook, TikTok, Instagram, LinkedIn, YouTube, Threads, Pinterest. Cũng cho biết giới hạn ký tự và số ảnh của từng kênh, nên nội dung viết ra là đăng được ngay.

**Nội dung và hình ảnh:** Canva, CapCut, Runway, HeyGen.

Điểm quan trọng không phải học thật nhiều công cụ, mà biết công cụ nào đặt ở bước nào để tạo ra đầu ra thật.

---

## Ba nguyên tắc chống bịa

Áp cho mọi agent trong mọi buổi.

1. **Chỉ dùng dữ liệu bạn cấp.** Không tự chế số liệu, thành phần, công dụng, giá, tên khách.
2. **Gắn nhãn nguồn.** `[DATA THẬT]` cho thông tin từ nguồn đưa vào, `[SUY LUẬN]` cho phần tự suy ra. Thiếu thì ghi "chưa đủ dữ liệu".
3. **Người duyệt cuối.** Mọi thứ gửi khách đều là nháp. Agent không tự bấm gửi.

Đến buổi 6, ba nguyên tắc này được viết thẳng vào Skill, để chúng đi theo hệ thống chứ không phụ thuộc trí nhớ người dùng.
