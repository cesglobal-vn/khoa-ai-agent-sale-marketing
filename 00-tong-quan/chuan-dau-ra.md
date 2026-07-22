# Chuẩn đầu ra: 40+ tài sản

Bảng đối chiếu để giảng viên chấm và học viên tự kiểm. Một học viên hoàn thành khóa là người tick được toàn bộ danh sách này bằng file thật, không phải bằng trí nhớ.

---

## Buổi 1 · Cài Claude Code và bốn tầng ngữ cảnh

| ✓ | Đầu ra | Số lượng | Đạt khi |
|---|---|---|---|
| ☐ | Cài đặt xong | 1 máy | Claude Desktop mở được tab Code, Git đã cài, tài khoản trả phí dùng được |
| ☐ | Thư mục làm việc | 1 | Mở được bằng Claude Code, Claude đọc được file trong đó |
| ☐ | File `CLAUDE.md` (tầng 1) | 1 | Claude trả lời đúng thương hiệu mà không cần nhắc lại. Có câu định vị, 3 thông điệp, 5 nỗi đau, giọng văn, danh sách từ cấm |
| ☐ | Câu định vị | 1 | Một câu, nói được bán gì cho ai và khác biệt ở đâu |
| ☐ | Thông điệp bán hàng | 3 | Mỗi thông điệp gắn với nhóm sản phẩm và tình huống dùng |
| ☐ | Nỗi đau khách | 5 | Viết bằng lời khách, không phải lời marketing |
| ☐ | Memory bật và kiểm tra (tầng 3) | 1 | Đã thử được Claude nhớ đúng, biết đường vào xem và xóa cái nhớ sai |
| ☐ | Skill `viet-bai-ban-hang` (tầng 2) | 1 | Đặt đúng `.claude/skills/<tên>/SKILL.md`, có frontmatter name và description, chạy ra kết quả thật |
| ☐ | Bài viết bán hàng | 3 | Do chính Skill sinh ra, không dính từ cấm, đăng được sau khi soát |
| ☐ | Hook | 10 | Mỗi hook bám 1 nỗi đau |
| ☐ | CTA | 10 | Rõ hành động tiếp theo, hợp kênh |
| ☐ | Kết nối MCP (tầng 4) | 1 | Claude đọc được dữ liệu từ Google Drive hoặc Sheet. Dùng tài khoản demo, không phải tài khoản công ty thật |

**Phép thử quan trọng nhất của buổi 1:** hỏi Claude một điều mà hồ sơ ghi rõ là chưa có (ngân sách quảng cáo, giá trị đơn trung bình). Claude điền bừa một con số nghe hợp lý là **chưa đạt**, dù mọi thứ khác xong hết.

## Buổi 2 · Customer Insight Agent

| ✓ | Đầu ra | Số lượng | Đạt khi |
|---|---|---|---|
| ☐ | Customer Insight Agent | 1 | Chạy lại trên data mới vẫn ra bảng đúng định dạng |
| ☐ | Bảng insight có trích dẫn | 1 | Mỗi dòng có ID nguồn và nguyên văn; chỗ suy ra gắn `[SUY LUẬN]` |
| ☐ | Content angle từ data thật | 5 | Mỗi angle truy được về ít nhất 1 trích dẫn |
| ☐ | Bài social media | 5 | Bám angle, đúng giọng thương hiệu |
| ☐ | Brief hình ảnh | 3 | Đủ để người thiết kế làm mà không hỏi lại |
| ☐ | Visual đăng được | 3 | Đúng tỷ lệ kênh, có nhận diện thương hiệu |

## Buổi 3 · Sales Agent

| ✓ | Đầu ra | Số lượng | Đạt khi |
|---|---|---|---|
| ☐ | Sales Research Agent | 1 | Chấm được lead mới theo đúng bộ tiêu chí đã định |
| ☐ | Lead Scoring Sheet | 10 lead | Có tiêu chí, trọng số, điểm, lý do, hành động kế tiếp |
| ☐ | Email cá nhân hóa | 10 | Cá nhân hóa bằng ghi chú trao đổi thật, không phải điền tên |
| ☐ | Tin nhắn Zalo/LinkedIn | 10 | Ngắn, hợp kênh, có lý do liên hệ rõ |
| ☐ | Kịch bản gọi 5 phút | 1 | Có mở đầu, câu hỏi thăm dò, chuyển tiếp, kết |
| ☐ | Kịch bản xử lý từ chối | 10 | Mỗi lời từ chối có câu trả lời không hứa quá |
| ☐ | Proposal nháp | 3-5 trang | Bảng giá đúng chính sách; chỗ chưa có chính sách thì để trống và ghi cần xin ý kiến |

## Buổi 4 · Content Engine Agent

| ✓ | Đầu ra | Số lượng | Đạt khi |
|---|---|---|---|
| ☐ | Content Engine Agent | 1 | Nhận insight, trả ra lịch và bài đúng ràng buộc |
| ☐ | Campaign brief | 1 | Có mục tiêu số, đối tượng, thông điệp, kênh, cách đo |
| ☐ | Lịch nội dung 14 ngày | 1 | Có nhịp: giáo dục, bằng chứng, xử lý phản đối, ưu đãi |
| ☐ | Bài social media | 10 | Không trùng ý, mỗi bài 1 pain + 1 USP + 1 lời kêu gọi |
| ☐ | Email nurturing | 3 | Có mạch nối, không phải 3 email rời |
| ☐ | Landing page section | 1 | Đủ tiêu đề, lợi ích, bằng chứng, nút hành động |
| ☐ | Video script 30-60 giây | 3 | Có 3 giây mở đầu giữ người xem |
| ☐ | Carousel | 6-8 slide | Mỗi slide 1 ý, slide cuối có lời kêu gọi |
| ☐ | Brief hình ảnh hoặc video | 5 | Đủ để sản xuất mà không hỏi lại |

## Buổi 5 · Automation & MCP

| ✓ | Đầu ra | Số lượng | Đạt khi |
|---|---|---|---|
| ☐ | Automation map | 1 | Rõ kích hoạt, xử lý, đưa ra, ai duyệt, log ở đâu |
| ☐ | Bảng quản lý (Sheet/Airtable/Notion) | 1 | Có cột trạng thái và cột người duyệt |
| ☐ | Automation chạy được hoặc prototype | 1 | Chạy thử được ít nhất 1 lượt từ đầu tới cuối |
| ☐ | Mẫu thông báo hoặc email | 1 | Đủ thông tin để người nhận hành động ngay |
| ☐ | Checklist kiểm soát rủi ro | 1 | Ghi rõ việc nào tuyệt đối không chạy tự động |

## Buổi 6 · Claude Skill & Playbook

| ✓ | Đầu ra | Số lượng | Đạt khi |
|---|---|---|---|
| ☐ | Claude Skill hoàn chỉnh | 1 | Người khác dùng ra được kết quả tương đương mà không hỏi lại |
| ☐ | AI Agent Playbook | 1 | Có quy trình, tiêu chuẩn đầu ra, ranh giới, chỉ số đo |
| ☐ | Bộ tài sản theo project | 1 | Sắp xếp có cấu trúc, tìm được trong 10 giây |
| ☐ | Automation hoặc prototype | 1 | Chuyển giao được, có hướng dẫn chạy |
| ☐ | Demo agent 5 phút | 1 | Trình bày được cho sếp hoặc khách, khoe kết quả không khoe công cụ |
| ☐ | Kế hoạch triển khai 14 ngày | 1 | Có ngày, việc, người làm, kết quả cần thấy |

---

## Đếm tổng

| Nhóm | Số đầu ra |
|---|---|
| Agent và hệ thống | 7 (Insight, Outbound, Proposal, Closer, Content Engine, Automation Orchestrator, và skill `viet-bai-ban-hang` của buổi 1) |
| Nội dung | 18+ bài social, 3 email nurturing, 3 video script, 1 carousel, 1 landing page section, 8 brief hình ảnh |
| Bán hàng | 10 email, 10 tin nhắn, 1 kịch bản gọi, 10 kịch bản xử lý từ chối, 1 lead scoring sheet, 1 proposal |
| Nền tảng | Thư mục làm việc, `CLAUDE.md`, Memory, `insight-khach-hang.md`, campaign brief, `lich-14-ngay.md`, automation map, bảng quản lý, Playbook, kế hoạch 14 ngày |

Tổng cộng vượt 40 tài sản dùng được.

---

## Ba câu hỏi chấm cuối khóa

Ba câu này quan trọng hơn số lượng.

1. **Người khác dùng lại được không?** Đưa Skill và Playbook cho một đồng nghiệp chưa học khóa này, họ có ra được kết quả tương đương không.
2. **Agent có chịu nói "chưa đủ dữ liệu" không?** Thử hỏi một câu mà dữ liệu không trả lời được. Agent điền bừa là chưa đạt, dù mọi thứ khác đẹp.
3. **Có đo được không?** Sau 14 ngày triển khai, học viên nhìn vào đâu để biết việc này có tác dụng hay không.
