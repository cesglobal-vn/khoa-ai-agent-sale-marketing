# AI Agent cho Sale & Marketing · Repo khóa học

Chương trình 6 buổi thực chiến của **CES Global**. Repo này chứa toàn bộ tài liệu để dạy và học: giáo án từng buổi, kịch bản demo của giảng viên, workbook học viên, bộ skill mẫu copy dán được, và một case study chạy xuyên suốt.

> Triết lý: mỗi buổi ra một sản phẩm thật. Kết quả buổi trước là đầu vào buổi sau. Hết 6 buổi, học viên có một bộ tài sản Sale & Marketing dùng được ngay.

---

## Dùng repo này thế nào

**Nếu bạn là giảng viên:** đọc [so-tay-giang-vien/huong-dan-chung.md](so-tay-giang-vien/huong-dan-chung.md) trước. Mỗi buổi chạy theo `giao-an/buoi-0X-*.md`, demo theo `so-tay-giang-vien/buoi-0X-*.md`.

**Nếu bạn là học viên:** mở `workbook/buoi-0X-*.md` và làm theo. Chưa có dữ liệu thật thì dùng case Thảo An trong [demo/thao-an/](demo/thao-an/).

**Nếu bạn muốn xem tổng thể trước:** đọc [00-tong-quan/tong-quan-khoa-hoc.md](00-tong-quan/tong-quan-khoa-hoc.md).

---

## Sáu buổi

| Buổi | Chủ đề | Agent xây được | Sản phẩm chính |
|---|---|---|---|
| [01](giao-an/buoi-01-bon-tang-ngu-canh.md) | Cài Claude Code + 4 tầng ngữ cảnh | Skill đầu tiên | CLAUDE.md + Skill + Memory + 1 kết nối MCP |
| [02](giao-an/buoi-02-customer-insight-agent.md) | Customer Insight Agent | Insight Agent | Bảng insight có trích dẫn + 5 content angle + 5 bài social |
| [03](giao-an/buoi-03-sales-agent.md) | Sales Agent | Outbound + Proposal + Closer | Lead scoring + 10 email + kịch bản gọi + proposal |
| [04](giao-an/buoi-04-content-engine-agent.md) | Content Engine Agent | Content Engine | Chiến dịch 14 ngày đa kênh |
| [05](giao-an/buoi-05-automation-va-mcp.md) | Automation & MCP | Luồng post bài tự động | Automation map + luồng đăng bài chạy được |
| [06](giao-an/buoi-06-claude-skill-va-playbook.md) | Claude Skill & Playbook | Đóng gói cả hệ thống | Claude Skill + AI Agent Playbook + kế hoạch 14 ngày |

Mỗi buổi 2,5 giờ (150 phút), chia: 20 phút framework · 35 phút demo · 65 phút học viên tự làm · 10 phút review · 20 phút hoàn thiện và nộp. Sáu buổi tổng 15 giờ học.

---

## Case study xuyên suốt: Thảo An

Thảo An là thương hiệu **giả định** dùng để demo: mỹ phẩm dưỡng da từ thảo mộc, 3 SKU, bán B2C qua Facebook và Shopee, bán sỉ B2B cho spa và cửa hàng.

Học viên có dữ liệu thật thì thay bằng sản phẩm của mình. Chưa có thì dùng nguyên bộ Thảo An để vẫn hoàn thành đủ sản phẩm mỗi buổi.

Xem [demo/thao-an/README.md](demo/thao-an/README.md). Bộ dữ liệu gồm hồ sơ sản phẩm, review khách, danh sách lead sỉ, chính sách giá sỉ, kế hoạch marketing 30 ngày, bảng đơn hàng mẫu và sơ đồ hệ thống agent.

---

## Luồng post bài

Buổi 5 nối các agent với việc đăng bài thật: từ insight ra caption, ra ảnh, rồi đăng lên kênh, có người duyệt trước khi đăng.

Xem [tai-lieu-hoc-vien/buoi-05-luong-post-bai.md](tai-lieu-hoc-vien/buoi-05-luong-post-bai.md).

---

## Ba nguyên tắc chống bịa

Áp dụng cho mọi agent trong mọi buổi. Đây là điều tách khóa này khỏi các khóa "mẹo prompt".

1. **Chỉ dùng dữ liệu bạn cấp.** Không tự chế số liệu, thành phần, công dụng, giá, tên khách.
2. **Gắn nhãn nguồn.** `[DATA THẬT]` cho thông tin từ nguồn đưa vào, `[SUY LUẬN]` cho phần agent tự suy ra. Thiếu thì ghi thẳng "chưa đủ dữ liệu".
3. **Người duyệt cuối.** Mọi thứ gửi khách đều là nháp. Agent không tự bấm gửi.

---

## Cấu trúc thư mục

```
00-tong-quan/
  tong-quan-khoa-hoc.md   tổng quan chương trình 6 buổi
  chuan-dau-ra.md         bảng đối chiếu chấm sản phẩm học viên

giao-an/
  buoi-01..06-*.md        giảng viên chạy buổi học theo file này, mỗi buổi 1 file

so-tay-giang-vien/
  huong-dan-chung.md      đọc một lần trước khi dạy buổi đầu tiên
  buoi-02..06-*.md        kịch bản 35 phút demo trên case Thảo An

workbook/
  buoi-01..06-*.md        học viên làm theo, có ô điền

tai-lieu-hoc-vien/
  huong-dan-cai-dat.md    phát cho học viên trước buổi, tự cài ở nhà
  buoi-05-luong-post-bai.md  đặc tả luồng đăng bài của buổi 5

demo/
  buoi-01..06/            CLAUDE.md mẫu và SKILL.md mẫu, copy dán được ngay
  thao-an/                dữ liệu mẫu dùng chung cho cả 6 buổi
```

Buổi 1 dùng format bài soạn chi tiết hơn (theo mốc đồng hồ, có lời giảng viết sẵn) vì đó là buổi cài đặt, dễ vỡ trận nhất.

---

CES Global · Creative · Effective · Sustainable
