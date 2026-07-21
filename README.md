# AI Agent cho Sale & Marketing · Repo khóa học

Chương trình 6 buổi thực chiến của **CES Global**. Repo này chứa toàn bộ tài liệu để dạy và học: giáo án từng buổi, kịch bản demo của giảng viên, workbook học viên, system prompt của 6 agent, và một case study chạy xuyên suốt.

> Triết lý: mỗi buổi ra một sản phẩm thật. Kết quả buổi trước là đầu vào buổi sau. Hết 6 buổi, học viên có một bộ tài sản Sale & Marketing dùng được ngay.

---

## Dùng repo này thế nào

**Nếu bạn là giảng viên:** đọc [docs/so-tay-giang-vien.md](docs/so-tay-giang-vien.md) trước. Mỗi buổi mở thư mục `buoi-0X-*/`, chạy theo `giao-an.md`, demo theo `demo-script.md`.

**Nếu bạn là học viên:** mở `buoi-0X-*/workbook-hoc-vien.md` và làm theo. Chưa có dữ liệu thật thì dùng case Thảo An trong [case-study/thao-an/](case-study/thao-an/).

**Nếu bạn muốn xem tổng thể trước:** đọc [docs/chuong-trinh-tong-quan.md](docs/chuong-trinh-tong-quan.md).

---

## Sáu buổi

| Buổi | Chủ đề | Agent xây được | Sản phẩm chính |
|---|---|---|---|
| [01](buoi-01-ai-marketing-workspace/) | Cài Claude Code + 4 tầng ngữ cảnh | Skill đầu tiên | CLAUDE.md + Skill + Memory + 1 kết nối MCP |
| [02](buoi-02-customer-insight-agent/) | Customer Insight Agent | Insight Agent | Bảng insight có trích dẫn + 5 content angle + 5 bài social |
| [03](buoi-03-sales-agent/) | Sales Agent | Outbound + Proposal + Closer | Lead scoring + 10 email + kịch bản gọi + proposal |
| [04](buoi-04-content-engine-agent/) | Content Engine Agent | Content Engine | Chiến dịch 14 ngày đa kênh |
| [05](buoi-05-automation-va-mcp/) | Automation & MCP | Luồng post bài tự động | Automation map + luồng đăng bài chạy được |
| [06](buoi-06-claude-skill-va-playbook/) | Claude Skill & Playbook | Đóng gói cả hệ thống | Claude Skill + AI Agent Playbook + kế hoạch 14 ngày |

Mỗi buổi 2,5 giờ (150 phút), chia: 20 phút framework · 35 phút demo · 65 phút học viên tự làm · 10 phút review · 20 phút hoàn thiện và nộp. Sáu buổi tổng 15 giờ học.

---

## Case study xuyên suốt: Thảo An

Thảo An là thương hiệu **giả định** dùng để demo: mỹ phẩm dưỡng da từ thảo mộc, 3 SKU, bán B2C qua Facebook và Shopee, bán sỉ B2B cho spa và cửa hàng.

Học viên có dữ liệu thật thì thay bằng sản phẩm của mình. Chưa có thì dùng nguyên bộ Thảo An để vẫn hoàn thành đủ sản phẩm mỗi buổi.

Xem [case-study/thao-an/README.md](case-study/thao-an/README.md). Bộ dữ liệu gồm hồ sơ sản phẩm, review khách, danh sách lead sỉ, chính sách giá sỉ, kế hoạch marketing 30 ngày và sơ đồ 6 agent.

---

## Luồng post bài

Buổi 5 nối các agent với việc đăng bài thật: từ insight ra caption, ra ảnh, rồi đăng lên kênh, có người duyệt trước khi đăng.

Xem [buoi-05-automation-va-mcp/luong-post-bai.md](buoi-05-automation-va-mcp/luong-post-bai.md).

---

## Ba nguyên tắc chống bịa

Áp dụng cho mọi agent trong mọi buổi. Đây là điều tách khóa này khỏi các khóa "mẹo prompt".

1. **Chỉ dùng dữ liệu bạn cấp.** Không tự chế số liệu, thành phần, công dụng, giá, tên khách.
2. **Gắn nhãn nguồn.** `[DATA THẬT]` cho thông tin từ nguồn đưa vào, `[SUY LUẬN]` cho phần agent tự suy ra. Thiếu thì ghi thẳng "chưa đủ dữ liệu".
3. **Người duyệt cuối.** Mọi thứ gửi khách đều là nháp. Agent không tự bấm gửi.

---

## Cấu trúc thư mục

```
buoi-01-*/
  bai-soan-giao-vien.md   bài soạn theo mốc đồng hồ, có lời giảng đọc lên được
  huong-dan-cai-dat.md    phát cho học viên trước buổi, tự cài ở nhà
  workbook-hoc-vien.md    học viên làm theo, có ô điền
  system-prompt.md        CLAUDE.md mẫu và SKILL.md mẫu, copy dán được ngay

buoi-02..06-*/
  giao-an.md              giảng viên chạy buổi học theo file này
  demo-script.md          kịch bản 35 phút demo trên case Thảo An
  workbook-hoc-vien.md    học viên làm theo, có ô điền
  system-prompt.md        prompt agent của buổi, copy dán được ngay

case-study/thao-an/       dữ liệu mẫu dùng chung cho cả 6 buổi
docs/                     tổng quan chương trình, sổ tay giảng viên, chuẩn đầu ra
```

Buổi 1 dùng format bài soạn chi tiết hơn (theo mốc đồng hồ, có lời giảng viết sẵn) vì đó là buổi cài đặt, dễ vỡ trận nhất.

---

CES Global · Creative · Effective · Sustainable
